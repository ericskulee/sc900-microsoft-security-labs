# Project 2 — Microsoft Entra Capabilities

## Identity Types
| Type | Used By | Example |
|------|---------|---------|
| User | Human employees | eric@company.com |
| Service Principal | Applications | app-project4 |
| Managed Identity | Azure resources | VM accessing Key Vault — no credentials stored |
| External Identity | Partners/guests | vendor@partner.com (B2B) |

## MFA — Three Factor Categories
- **Something you know** — password, PIN
- **Something you have** — Authenticator app, FIDO2 key, smart card
- **Something you are** — fingerprint, face recognition (biometrics)

## MFA Methods — Weakest to Strongest
1. SMS / Voice call — weakest, SIM swapping risk
2. Email OTP — weak
3. Authenticator app (TOTP/push) — good
4. FIDO2 security key — strongest, fully phishing-resistant

## Self-Service Password Reset (SSPR)
- Allows users to reset passwords WITHOUT contacting IT helpdesk
- Reduces IT support costs (password resets = 20% of helpdesk volume)
- Requires **Entra ID P1** license
- Users must register verification methods before they can use SSPR

## Conditional Access — IF/THEN Policy Engine
- **IF** (conditions): user, location, device, app, sign-in risk
- **THEN** (controls): require MFA, block access, require compliant device
- Requires **Entra ID P1** license
- Example: IF user outside corporate network THEN require MFA

## Identity Protection
- Uses machine learning to detect compromised accounts and risky sign-ins
- **User risk** — is this ACCOUNT compromised? (e.g. leaked credentials on dark web)
- **Sign-in risk** — is this SIGN-IN suspicious? (e.g. impossible travel, anonymous IP)
- Requires **Entra ID P2** license

## Privileged Identity Management (PIM)
- Provides **Just-In-Time (JIT)** access to privileged roles
- **Eligible** = must activate when needed — most secure ✅
- **Active** = always on — standing privilege — less secure ❌
- Activation requires: MFA + justification + approval (if configured)
- Full audit trail of every activation
- Requires **Entra ID P2** license

## License Summary
| Feature | License Required |
|---------|----------------|
| Basic MFA | Free |
| SSPR | P1 |
| Conditional Access | P1 |
| Dynamic Groups | P1 |
| Identity Protection | P2 |
| PIM | P2 |

## Key Exam Scenarios
- Most phishing-resistant MFA method → **FIDO2 security key**
- Users reset passwords without IT → **SSPR**
- Require MFA only outside corporate network → **Conditional Access**
- Detect leaked credentials automatically → **Identity Protection**
- Admin roles only active when needed → **PIM (Eligible assignment)**
- User risk vs Sign-in risk → User risk = account compromised, Sign-in risk = suspicious login attempt

# Project 4 — Microsoft Compliance Solutions

## Microsoft Purview — Unified Compliance Platform
- Central hub for all Microsoft compliance tools
- Portal: compliance.microsoft.com (requires Microsoft 365 work account)
- Covers: data governance, compliance management, information protection

## Compliance Manager
- Tracks compliance posture against regulatory frameworks
- **Compliance Score** — measures regulatory compliance as a percentage
- Frameworks: GDPR, NIST 800-53, ISO 27001, SOC 2, HIPAA, PCI-DSS
- Microsoft-managed controls — pre-completed by Microsoft
- Customer-managed controls — YOUR organization must implement
- Different from Secure Score (which measures Azure security posture)

## Sensitivity Labels
- Classify documents and emails by sensitivity level
- Hierarchy: Public > Internal > Confidential > Highly Confidential
- Protection TRAVELS with the document — even outside the organization
- Applied manually by users OR automatically by the system
- Can enforce: encryption, access restrictions, watermarks, headers/footers

## Data Loss Prevention (DLP)
- Prevents sensitive data from leaving the organization
- Detects sensitive information types: credit card numbers, SSNs, passport numbers
- Actions: block sharing, notify user, require justification, alert security team
- Works across: email, Teams, SharePoint, OneDrive, endpoints
- Works WITH Sensitivity Labels — labels help DLP identify what to protect

## Retention Policies
- Automatically KEEP data for required period (legal/regulatory requirements)
- OR automatically DELETE data after set period (privacy compliance)
- **Retention Policy** — broad, applied to entire locations (all mailboxes, all SharePoint sites)
- **Retention Label** — specific, applied to individual items (specific contracts, specific emails)

## eDiscovery
- Find, collect, and preserve electronic data for legal investigations
- **Legal Hold** — prevents data from being deleted when litigation is anticipated
- Searches across: Exchange, SharePoint, Teams, OneDrive
- Three levels: Content Search > eDiscovery Standard > eDiscovery Premium

## Insider Risk Management
- Detects risky behaviors by employees INSIDE the organization
- Scenarios: data theft by departing employees, unusual large downloads, external sharing
- Uses HR signals (resignation) + activity signals (downloads) to detect risk
- Privacy-focused — only shows details to authorized investigators

## Audit
- Records ALL user and admin activities across Microsoft 365
- Who did what, when, from where, on which device
- Used for security investigations and compliance evidence

## Key Exam Scenarios
- Track compliance against GDPR/NIST → **Compliance Manager**
- Classify documents so protection travels with them → **Sensitivity Labels**
- Prevent credit card numbers being emailed externally → **DLP**
- Keep emails for 7 years for legal requirements → **Retention Policy**
- Preserve evidence for litigation → **eDiscovery + Legal Hold**
- Detect employee stealing data before resignation → **Insider Risk Management**
- Who deleted a file and when → **Audit logs**

## License Notes
- Microsoft Purview requires Microsoft 365 work/school account
- Basic compliance features — Microsoft 365 Business Basic+
- Advanced eDiscovery and Insider Risk — Microsoft 365 E5

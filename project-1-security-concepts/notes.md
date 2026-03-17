# Project 1 — Security, Compliance & Identity Concepts

## Zero Trust — Three Core Principles
1. **Verify explicitly** — Always authenticate and authorize using ALL available data points. Never trust based on network location alone.
2. **Use least privilege** — Give users the bare minimum access needed, only when needed (Just-In-Time), only as long as needed (time-bound).
3. **Assume breach** — Operate as if attackers are already inside. Segment access, encrypt everything, monitor everything.

## Shared Responsibility Model
| Layer | On-Prem | IaaS | PaaS | SaaS |
|-------|---------|------|------|------|
| Physical/Network | You | Microsoft | Microsoft | Microsoft |
| Operating System | You | You | Microsoft | Microsoft |
| Applications | You | You | You | Microsoft |
| **Data** | **You** | **You** | **You** | **You** |
| **Identities** | **You** | **You** | **You** | **You** |

> Customer is ALWAYS responsible for Data and Identities in ALL cloud models.

## Authentication vs Authorization
- **Authentication (AuthN)** — proving WHO you are (username + password + MFA). Shown in Sign-in logs.
- **Authorization (AuthZ)** — proving WHAT you are allowed to do (RBAC roles, permissions). Shown in Assigned roles.
- AuthN always comes before AuthZ.

## CIA Triad
- **Confidentiality** — only authorized users can access data (Key Vault, RBAC, Private Endpoints)
- **Integrity** — data is accurate and has not been tampered with (Azure Policy, Activity Logs, Resource Locks)
- **Availability** — data is accessible when needed (Azure Backup, Site Recovery, Availability Zones)

## Defense in Depth — 7 Layers
1. **Physical** — data center physical security (Microsoft managed)
2. **Perimeter** — DDoS protection, firewalls at network edge
3. **Network** — NSGs, network segmentation, deny by default
4. **Compute** — VM access control, endpoint protection, patching
5. **Application** — secure code, no vulnerabilities, secrets in Key Vault
6. **Data** — encryption at rest and in transit, data classification

## Key Exam Scenarios
- Requiring MFA even on corporate network → **Verify explicitly**
- Developer gets read-only access to one database → **Use least privilege**
- Network segmentation to limit breach impact → **Assume breach**
- Customer moves to Microsoft 365 — who manages mailbox access? → **The customer (identities)**


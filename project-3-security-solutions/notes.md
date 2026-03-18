# Project 3 — Microsoft Security Solutions

## Microsoft Defender for Cloud
- **CSPM** — Cloud Security Posture Management — assesses and improves security posture
- **CWPP** — Cloud Workload Protection Platform — active threat detection per resource type
- **Secure Score** — measures Azure resource security posture as a percentage
- **Recommendations** — specific actions to improve Secure Score
- **Multi-cloud** — covers Azure, AWS, GCP, GitHub, Docker Hub
- Free tier provides recommendations. Paid Defender plans add active threat detection.

## Microsoft Sentinel — SIEM + SOAR
- **SIEM** — collects and correlates logs, detects threats, generates alerts
- **SOAR** — automates response to threats via playbooks (Logic Apps)
- Microsoft Sentinel = SIEM + SOAR combined in one cloud-native platform
- Built on **Log Analytics Workspace** — uses **KQL** for queries
- **Data connectors** — ingest logs from Azure, M365, third-party sources
- **Analytics rules** — KQL detection rules that create incidents
- **Playbooks** — automated response workflows built on Logic Apps
- **Hunting** — proactive threat hunting using KQL queries

## Microsoft Defender XDR — Extended Detection and Response
- Unified security operations portal at security.microsoft.com
- Combines signals from:
  - **Defender for Endpoint** — devices (laptops, phones, servers)
  - **Defender for Office 365** — email, Teams, SharePoint
  - **Defender for Identity** — Active Directory and Entra ID
  - **Defender for Cloud Apps** — cloud applications, Shadow IT
- **Microsoft Secure Score** — measures Microsoft 365 security posture
- Different from Defender for Cloud Secure Score (which measures Azure resources)

## Defender for Cloud Apps — CASB
- **CASB** — Cloud Access Security Broker
- Discovers **Shadow IT** — unapproved cloud apps employees are using
- Assesses risk of each discovered app
- Enforces policies on cloud app usage
- Protects sensitive data in cloud apps

## Azure Network Security Services

### Azure DDoS Protection
- **Basic/Network** — FREE, automatically enabled for ALL Azure resources
- **IP Protection** — paid, advanced metrics, alerts, rapid response team

### Azure Firewall
- Fully managed, stateful firewall service
- FQDN filtering — allow/deny based on domain names
- Threat intelligence — auto-blocks known malicious IPs and domains
- Different from NSG — NSG is basic rules, Firewall is Layer 7 inspection

## Key Exam Scenarios
- Cloud-native SIEM + SOAR → **Microsoft Sentinel**
- Automated threat response → **Playbooks** in Sentinel
- Query language in Sentinel → **KQL**
- Unified endpoint + email + identity + cloud app protection → **Defender XDR**
- Discover Shadow IT → **Defender for Cloud Apps (CASB)**
- Managed stateful firewall → **Azure Firewall**
- Free DDoS protection for all Azure resources → **Basic DDoS Protection (automatic)**
- Improve Azure security posture + recommendations → **Defender for Cloud**

## License Notes
- Defender for Cloud free tier — CSPM only (recommendations + Secure Score)
- Defender plans (paid) — add active threat detection per workload
- Defender XDR full features — requires Microsoft 365 E5

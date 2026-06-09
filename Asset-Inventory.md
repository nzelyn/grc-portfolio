# Asset Inventory — NexaCloud Solutions ISMS

**Document ID:** NCS-ISMS-AI-001  
**Version:** 2.2  
**Effective Date:** 01 September 2024  
**Reference Standard:** ISO 27001:2022 Annex A 5.9, 5.12  
**Asset Owner Policy:** Each asset must have a designated owner responsible for classification, access, and disposal  
**Classification:** Confidential

---

## Asset Classification Scheme

| Classification | Description | Examples |
|---|---|---|
| Restricted | Highest sensitivity; very limited distribution | Customer data, encryption keys, board minutes |
| Confidential | Sensitive; internal use by authorized roles | Source code, risk register, security policies, audit reports |
| Internal | General internal use; no customer data | Operational procedures, internal wikis, team documentation |
| Public | Approved for external distribution | Marketing materials, public APIs, product documentation |

---

## Asset Inventory

### Information Assets

| Asset ID | Asset Name | Classification | Type | Owner | Location | Retention | Last Reviewed |
|---|---|---|---|---|---|---|---|
| IA-001 | Customer SIEM event data | Restricted | Database | VP Engineering | AWS RDS — prod | Per contract (min 12 months) | Sep 2024 |
| IA-002 | Customer account and contact data | Restricted | Database | VP Engineering | AWS RDS — prod | Per contract | Sep 2024 |
| IA-003 | AWS KMS encryption keys | Restricted | Cryptographic | CISO | AWS KMS | Rotated annually | Sep 2024 |
| IA-004 | NexaCloud application source code | Confidential | Source Code | VP Engineering | GitHub Enterprise | Indefinite | Sep 2024 |
| IA-005 | ISO 27001 risk register | Confidential | Document | GRC Manager | Confluence | 7 years | Sep 2024 |
| IA-006 | Penetration test reports | Confidential | Report | CISO | SharePoint | 3 years | Sep 2024 |
| IA-007 | Employee personal data (HR records) | Restricted | Database | VP HR | Rippling (SaaS) | Per employment + 7 years | Sep 2024 |
| IA-008 | Payroll and financial records | Restricted | Database | CFO | Workday (SaaS) | 7 years | Sep 2024 |
| IA-009 | Customer contracts and MSAs | Confidential | Document | General Counsel | DocuSign + SharePoint | 10 years | Sep 2024 |
| IA-010 | Security incident logs | Confidential | Logs | SecOps Lead | Jira + S3 | 3 years | Sep 2024 |

---

### Software Assets

| Asset ID | Asset Name | Classification | Version | Owner | License | EOL Date |
|---|---|---|---|---|---|---|
| SA-001 | NexaCloud SIEM Platform | Confidential | 4.2.1 | VP Engineering | Proprietary | N/A |
| SA-002 | AWS (EC2, RDS, S3 etc.) | Internal | Managed | IT Operations | Pay-as-you-go | N/A |
| SA-003 | Okta — Identity Platform | Internal | Enterprise | IT Operations | Annual contract | Oct 2025 |
| SA-004 | GitHub Enterprise | Internal | 3.11 | VP Engineering | Annual contract | Dec 2024 |
| SA-005 | Jira / Confluence (Atlassian) | Internal | Cloud | IT Operations | Annual contract | Jan 2025 |
| SA-006 | Datadog | Internal | Cloud | Engineering | Annual contract | Mar 2025 |
| SA-007 | CrowdStrike Falcon | Internal | Cloud | IT Operations | Annual contract | Jun 2025 |
| SA-008 | KnowBe4 | Internal | Cloud | HR | Annual contract | Sep 2025 |
| SA-009 | Vanta | Confidential | Cloud | GRC | Annual contract | Nov 2025 |
| SA-010 | Tenable.io | Confidential | Cloud | SecOps | Annual contract | Feb 2025 |

---

### Hardware Assets

| Asset ID | Asset Name | Quantity | Classification | Owner | Location | Disposal Method |
|---|---|---|---|---|---|---|
| HW-001 | Apple MacBook Pro (M3) | 140 | Internal | IT Operations | Bangalore + Austin | Secure wipe via MDM + ITAD vendor |
| HW-002 | Dell Latitude 5540 (Windows) | 85 | Internal | IT Operations | Bangalore + Austin | Secure wipe via MDM + ITAD vendor |
| HW-003 | iPhone 15 (corporate-issued) | 45 | Internal | IT Operations | Bangalore + Austin | MDM wipe on return |
| HW-004 | Office network switches (Cisco) | 8 | Internal | IT Operations | Bangalore + Austin | Secure factory reset before disposal |
| HW-005 | Conference room AV systems | 12 | Internal | IT Operations | Bangalore + Austin | Physical destruction |

*Note: No on-premises servers. All compute infrastructure is AWS-managed.*

---

### Service Assets (Subservice Organizations)

| Asset ID | Vendor | Service | Classification | Owner | SOC 2 Available | Last SOC Review |
|---|---|---|---|---|---|---|
| SVC-001 | Amazon Web Services | Cloud infrastructure (IaaS/PaaS) | Restricted | CISO | Yes | Aug 2024 |
| SVC-002 | Okta | Identity and access management | Confidential | IT Operations | Yes | Aug 2024 |
| SVC-003 | GitHub (Microsoft) | Source code management | Confidential | VP Engineering | Yes | Aug 2024 |
| SVC-004 | Atlassian | Project management and documentation | Internal | IT Operations | Yes | Aug 2024 |
| SVC-005 | Datadog | Monitoring and observability | Internal | Engineering | Yes | Aug 2024 |
| SVC-006 | CloudFlare | DDoS protection and CDN augmentation | Internal | Engineering | Yes | Pending |
| SVC-007 | SendGrid (Twilio) | Transactional email (alerts) | Internal | Engineering | Yes | Pending |
| SVC-008 | PagerDuty | On-call alerting | Internal | SecOps | Yes | Pending |

---

*NCS-ISMS-AI-001 v2.2*

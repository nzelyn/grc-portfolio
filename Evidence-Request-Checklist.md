# SOC 2 Evidence Request Checklist — NexaCloud Solutions

**Document ID:** NCS-SOC2-ERC-001  
**Version:** 1.2  
**Prepared By:** GRC Manager  
**Audit Period:** 01 January 2024 — 31 December 2024  
**Auditor:** [External Auditor Name]  
**Due Date:** 15 October 2024

---

## Instructions

- Provide evidence files using the naming convention: `NCS-[TSC]-[ControlID]-[EvidenceType]-[YYYYMM]-v[N]`
- Upload all files to the shared auditor portal folder: `/NexaCloud-SOC2-2024/Evidence/`
- Mark each item as **Provided**, **In Progress**, or **Unavailable** in the Status column
- For Unavailable items, provide a written explanation in the Notes column

---

## CC1 — Control Environment

| Item # | Evidence Required | Source System | Format | Owner | Status | Notes |
|---|---|---|---|---|---|---|
| CC1-001 | Organizational chart showing security reporting structure | HR System (Rippling) | PDF | HR | Provided | |
| CC1-002 | Security committee meeting minutes (Q1-Q4 2024) | Confluence | PDF | GRC | In Progress | Q3-Q4 pending |
| CC1-003 | Security awareness training completion report | KnowBe4 | PDF/CSV | HR | Provided | |
| CC1-004 | Employee code of conduct acknowledgement records | DocuSign | PDF | HR | Provided | |
| CC1-005 | Background check policy and sample check evidence | HR System | PDF | HR | Provided | Names redacted |

---

## CC6 — Logical Access Controls

| Item # | Evidence Required | Source System | Format | Owner | Status | Notes |
|---|---|---|---|---|---|---|
| CC6-001 | Quarterly privileged access review reports (all 4 quarters) | Jira + Okta | PDF | IT Ops | Provided | |
| CC6-002 | MFA enforcement configuration screenshot | Okta Admin | PNG | IT Ops | Provided | |
| CC6-003 | Sample new hire access provisioning tickets (5 samples) | Jira | PDF | IT Ops | Provided | |
| CC6-004 | Sample termination deprovisioning evidence (5 samples) | Jira + Okta logs | PDF | IT Ops | Provided | |
| CC6-005 | AWS IAM role inventory with justifications | AWS IAM + Confluence | CSV + PDF | Engineering | In Progress | |
| CC6-006 | Production access list with role assignments | Okta + AWS IAM | CSV | Security Ops | Provided | |
| CC6-007 | Encryption configuration for RDS and S3 (AWS Config) | AWS Config | PDF/PNG | Engineering | Provided | |
| CC6-008 | Vendor access review log | SharePoint | PDF | GRC | Unavailable | Process being formalized — remediation in progress |

---

## CC7 — System Operations

| Item # | Evidence Required | Source System | Format | Owner | Status | Notes |
|---|---|---|---|---|---|---|
| CC7-001 | Monthly vulnerability scan reports (12 months) | Tenable / AWS Inspector | PDF | Security Ops | Provided | |
| CC7-002 | Patch management SLA compliance report | Jira + CMDB | CSV | IT Ops | In Progress | |
| CC7-003 | Incident log for audit period (P1 and P2 incidents) | Jira | PDF | Security Ops | Provided | |
| CC7-004 | Incident response tabletop exercise report | GRC Documentation | PDF | GRC | Unavailable | Exercise scheduled Nov 2024 |
| CC7-005 | Security monitoring alert configuration (GuardDuty rules) | AWS GuardDuty | PDF | Security Ops | Provided | |
| CC7-006 | CloudTrail log retention configuration | AWS Console | PNG | Engineering | Provided | |

---

## CC8 — Change Management

| Item # | Evidence Required | Source System | Format | Owner | Status | Notes |
|---|---|---|---|---|---|---|
| CC8-001 | Change management policy (approved version) | Confluence | PDF | GRC | Provided | |
| CC8-002 | Sample change tickets with approvals (10 samples) | Jira | PDF | Engineering | Provided | |
| CC8-003 | Production deployment approval workflow config | GitHub Actions | PNG | Engineering | Provided | |
| CC8-004 | Emergency change log (full year) | Jira | PDF | IT Ops | Provided | |
| CC8-005 | Segregation of duties matrix for production access | Confluence | PDF | Engineering | Provided | |

---

## CC9 — Risk Mitigation

| Item # | Evidence Required | Source System | Format | Owner | Status | Notes |
|---|---|---|---|---|---|---|
| CC9-001 | Annual risk assessment report 2023 | GRC Documentation | PDF | GRC | Provided | 2024 refresh in progress |
| CC9-002 | Risk register (current) | Risk Register Tool | XLSX | GRC | Provided | |
| CC9-003 | Vendor SOC 2 report collection (AWS, Okta, Atlassian) | Vendor Portals | PDF | GRC | Provided | |
| CC9-004 | Cyber insurance certificate | Finance | PDF | Finance | Provided | |
| CC9-005 | Business continuity plan (approved) | Confluence | PDF | Engineering | Provided | |
| CC9-006 | DR test results (most recent) | GRC Documentation | PDF | Engineering | Provided | |

---

## A1 — Availability

| Item # | Evidence Required | Source System | Format | Owner | Status | Notes |
|---|---|---|---|---|---|---|
| A1-001 | Monthly uptime reports (12 months) | Datadog | PDF | Engineering | Provided | |
| A1-002 | SLA performance report vs 99.9% commitment | Datadog / StatusPage | PDF | Engineering | Provided | |
| A1-003 | Capacity planning review documentation | Confluence | PDF | Engineering | In Progress | |
| A1-004 | AWS Auto Scaling group configuration | AWS Console | PNG | Engineering | Provided | |
| A1-005 | Incident impact reports for any outages | Jira | PDF | Engineering | Provided | |

---

## Evidence Status Summary

| Status | Count | Percentage |
|---|---|---|
| Provided | 31 | 73% |
| In Progress | 7 | 17% |
| Unavailable | 4 | 10% |
| **Total** | **42** | **100%** |

---

*Document last updated: 15 August 2024 — NCS-SOC2-ERC-001 v1.2*

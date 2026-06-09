# Risk Treatment Plan — NexaCloud Solutions ISMS

**Document ID:** NCS-ISMS-RTP-2024  
**Version:** 2.0  
**Effective Date:** 01 October 2024  
**Reference Standard:** ISO 27001:2022 Clauses 6.1.3, 8.3  
**Document Owner:** GRC Manager  
**Approved By:** CISO

---

## Purpose

This document records the selected treatment for each identified risk in the NexaCloud ISMS risk register and maps treatment controls to ISO 27001:2022 Annex A.

---

## Risk Treatment Decisions

### NCS-RISK-2024-001 — Credential-based compromise of AWS environment

**Risk Level:** Critical (Inherent 20) — Target: Medium (Residual 10)  
**Treatment Option:** Mitigate

| Control | Annex A Reference | Target Date | Owner | Status |
|---|---|---|---|---|
| Enforce MFA for 100% of IAM users and service accounts | 8.5 | 30 Sep 2024 | IT Operations | In Progress |
| Migrate service account secrets to AWS Secrets Manager | 8.3 | 31 Oct 2024 | Engineering | In Progress |
| Enable IAM Access Analyzer to detect overly permissive policies | 8.2 | 30 Sep 2024 | Engineering | Implemented |
| Enable privileged session recording via AWS CloudTrail | 8.15 | 31 Oct 2024 | Security Operations | Planned |
| Implement breakglass procedure for root account | 8.2 | 30 Sep 2024 | IT Operations | Implemented |

---

### NCS-RISK-2024-002 — Ransomware on corporate endpoints

**Risk Level:** Critical (Inherent 20) — Residual: Low (8)  
**Treatment Option:** Mitigate

| Control | Annex A Reference | Target Date | Owner | Status |
|---|---|---|---|---|
| CrowdStrike Falcon deployed on all endpoints | 8.7 | Complete | IT Operations | Implemented |
| Email filtering (Mimecast) blocking malicious attachments | 8.23 | Complete | IT Operations | Implemented |
| Immutable S3 backups with object lock | 8.13 | Complete | Engineering | Implemented |
| Security awareness training — phishing simulation quarterly | 6.3 | Ongoing | HR | Active |
| USB ports blocked via MDM for non-IT users | 7.10 | Complete | IT Operations | Implemented |

---

### NCS-RISK-2024-003 — Unauthorized access to customer data

**Risk Level:** High (Inherent 15) — Target: Medium (10)  
**Treatment Option:** Mitigate

| Control | Annex A Reference | Target Date | Owner | Status |
|---|---|---|---|---|
| Row-level security enforced in PostgreSQL | 8.3 | Complete | Engineering | Implemented |
| Quarterly privileged access reviews | 5.18 | Ongoing | IT Operations | Active |
| GuardDuty anomaly detection for RDS access patterns | 8.16 | Complete | Security Operations | Implemented |
| Penetration test covering multi-tenancy isolation | 8.8 | Nov 2024 | Security Operations | Planned |

---

### NCS-RISK-2024-005 — Data breach via unpatched vulnerability

**Risk Level:** High (Inherent 15) — Target: Low (8)  
**Treatment Option:** Mitigate

| Control | Annex A Reference | Target Date | Owner | Status |
|---|---|---|---|---|
| Weekly Tenable and AWS Inspector vulnerability scans | 8.8 | Active | Security Operations | Active |
| 30-day SLA for critical/high patches; automated Jira tickets | 8.8 | 30 Sep 2024 | IT Operations | In Progress |
| AWS WAF rules updated monthly with OWASP ruleset | 8.20 | Active | Engineering | Active |
| Annual penetration test (next: November 2024) | 8.29 | Nov 2024 | Security Operations | Planned |

---

## Residual Risk Acceptance

The following residual risks are formally accepted by the CISO:

| Risk ID | Residual Score | Justification | Accepted By | Date |
|---|---|---|---|---|
| NCS-RISK-2024-007 (Insider threat) | 8 — Low | Residual risk represents the irreducible minimum; further controls would impair operations | Deepa Venkataraman | 01 Oct 2024 |
| NCS-RISK-2024-012 (PDPB compliance risk) | 6 — Low | PDPB regulations not yet fully in force; NexaCloud monitoring for updates; legal counsel engaged | Deepa Venkataraman | 01 Oct 2024 |

---

## Treatment Plan Review

| Date | Version | Change |
|---|---|---|
| 01 Sep 2023 | 1.0 | Initial treatment plan |
| 01 Oct 2024 | 2.0 | Updated for 2024 risk assessment cycle |

---

*NCS-ISMS-RTP-2024 v2.0*

# Statement of Applicability (SoA) — NexaCloud Solutions

**Document ID:** NCS-ISMS-SOA-001  
**Version:** 2.0  
**Effective Date:** 01 September 2024  
**Reference Standard:** ISO/IEC 27001:2022 Annex A  
**Document Owner:** CISO  
**Approved By:** CEO

---

## Summary

| Category | Total Controls | Applicable | Not Applicable |
|---|---|---|---|
| 5 — Organizational Controls | 37 | 36 | 1 |
| 6 — People Controls | 8 | 8 | 0 |
| 7 — Physical Controls | 14 | 11 | 3 |
| 8 — Technological Controls | 34 | 33 | 1 |
| **Total** | **93** | **88** | **5** |

---

## Applicability Legend

- **A** = Applicable and implemented
- **P** = Applicable, partially implemented (in progress)
- **N/A** = Not applicable (with justification)

---

## 5. Organizational Controls (37 controls)

| Control ID | Control Name | Applicable | Implementation Status | Justification (if N/A) | SOC 2 Mapping |
|---|---|---|---|---|---|
| 5.1 | Policies for information security | A | Implemented | | CC1.3 |
| 5.2 | Information security roles and responsibilities | A | Implemented | | CC1.2 |
| 5.3 | Segregation of duties | A | Implemented | | CC6.3 |
| 5.4 | Management responsibilities | A | Implemented | | CC1.4 |
| 5.5 | Contact with authorities | A | Implemented | | CC2.3 |
| 5.6 | Contact with special interest groups | A | Implemented | | CC2.3 |
| 5.7 | Threat intelligence | A | Implemented | | CC7.2 |
| 5.8 | Information security in project management | A | Implemented | | CC8.1 |
| 5.9 | Inventory of information and other associated assets | A | Implemented | | CC6.1 |
| 5.10 | Acceptable use of information and assets | A | Implemented | | CC1.3 |
| 5.11 | Return of assets | A | Implemented | | CC6.4 |
| 5.12 | Classification of information | A | Implemented | | C1.1 |
| 5.13 | Labelling of information | A | Partially Implemented | | C1.1 |
| 5.14 | Information transfer | A | Implemented | | C1.2 |
| 5.15 | Access control | A | Implemented | | CC6.1 |
| 5.16 | Identity management | A | Implemented | | CC6.2 |
| 5.17 | Authentication information | A | Implemented | | CC6.1 |
| 5.18 | Access rights | A | Implemented | | CC6.2 |
| 5.19 | Information security in supplier relationships | A | Partially Implemented | | CC9.2 |
| 5.20 | Addressing information security within supplier agreements | A | Partially Implemented | | CC9.2 |
| 5.21 | Managing information security in the ICT supply chain | A | Partially Implemented | | CC9.2 |
| 5.22 | Monitoring, review and change management of supplier services | A | Partially Implemented | | CC9.2 |
| 5.23 | Information security for use of cloud services | A | Implemented | | CC6.7 |
| 5.24 | Information security incident management planning and preparation | A | Implemented | | CC7.3 |
| 5.25 | Assessment and decision on information security events | A | Implemented | | CC7.3 |
| 5.26 | Response to information security incidents | A | Implemented | | CC7.4 |
| 5.27 | Learning from information security incidents | A | Implemented | | CC4.1 |
| 5.28 | Collection of evidence | A | Implemented | | CC7.3 |
| 5.29 | Information security during disruption | A | Implemented | | A1.3 |
| 5.30 | ICT readiness for business continuity | A | Implemented | | A1.3 |
| 5.31 | Legal, statutory, regulatory and contractual requirements | A | Implemented | | CC1.3 |
| 5.32 | Intellectual property rights | A | Implemented | | CC1.3 |
| 5.33 | Protection of records | A | Implemented | | CC6.7 |
| 5.34 | Privacy and protection of PII | A | Implemented | | P1-P8 |
| 5.35 | Independent review of information security | A | Implemented | | CC4.2 |
| 5.36 | Compliance with policies, rules and standards | A | Implemented | | CC4.1 |
| 5.37 | Documented operating procedures | A | Implemented | | CC5.3 |

---

## 6. People Controls (8 controls)

| Control ID | Control Name | Applicable | Status | Notes |
|---|---|---|---|---|
| 6.1 | Screening | A | Implemented | Background checks for all new hires |
| 6.2 | Terms and conditions of employment | A | Implemented | Security responsibilities in employment contracts |
| 6.3 | Information security awareness, education and training | A | Implemented | KnowBe4 platform; annual mandatory training |
| 6.4 | Disciplinary process | A | Implemented | Documented in HR policy |
| 6.5 | Responsibilities after termination or change of employment | A | Implemented | Okta auto-deprovisioning; NDA enforcement |
| 6.6 | Confidentiality or non-disclosure agreements | A | Implemented | NDAs signed at hire; vendor NDAs in place |
| 6.7 | Remote working | A | Implemented | Remote work policy published; VPN required |
| 6.8 | Information security event reporting | A | Implemented | Security@nexacloud.io reporting channel |

---

## 7. Physical Controls (14 controls)

| Control ID | Control Name | Applicable | Status | Justification (if N/A) |
|---|---|---|---|---|
| 7.1 | Physical security perimeters | N/A | — | No on-premises data centres; AWS manages physical perimeters; office controls are basic |
| 7.2 | Physical entry | A | Implemented | Badge access to Bangalore and Austin offices |
| 7.3 | Securing offices, rooms and facilities | A | Implemented | Server room equivalent = AWS; offices secured |
| 7.4 | Physical security monitoring | A | Partially Implemented | CCTV in Bangalore; Austin relies on building security |
| 7.5 | Protecting against physical and environmental threats | N/A | — | Delegated to AWS; documented in SoA |
| 7.6 | Working in secure areas | A | Implemented | Clean desk policy; secure areas defined |
| 7.7 | Clear desk and clear screen | A | Implemented | Policy in place; enforced quarterly audits |
| 7.8 | Equipment siting and protection | N/A | — | All compute is AWS-hosted; laptops governed by MDM |
| 7.9 | Security of assets off-premises | A | Implemented | Laptop encryption (BitLocker/FileVault); MDM enrolled |
| 7.10 | Storage media | A | Implemented | No physical media; USB blocked via MDM |
| 7.11 | Supporting utilities | A | Implemented | AWS SLA covers utility resilience |
| 7.12 | Cabling security | A | Implemented | Office network managed; AWS covers DC cabling |
| 7.13 | Equipment maintenance | A | Implemented | MDM for laptops; AWS for servers |
| 7.14 | Secure disposal or re-use of equipment | A | Implemented | Device wipe procedure on offboarding; ITAD vendor contracted |

---

## 8. Technological Controls (34 controls — selected highlights)

| Control ID | Control Name | Applicable | Status | Notes |
|---|---|---|---|---|
| 8.1 | User endpoint devices | A | Implemented | CrowdStrike, MDM, encryption on all endpoints |
| 8.2 | Privileged access rights | A | Implemented | Okta-managed; quarterly review |
| 8.3 | Information access restriction | A | Implemented | Role-based access; least privilege enforced |
| 8.4 | Access to source code | A | Implemented | GitHub RBAC; branch protection rules |
| 8.5 | Secure authentication | A | Implemented | Okta MFA enforced (99% compliance) |
| 8.6 | Capacity management | A | Partially Implemented | AWS Auto Scaling; formal capacity plan in progress |
| 8.7 | Protection against malware | A | Implemented | CrowdStrike on all endpoints |
| 8.8 | Management of technical vulnerabilities | A | Implemented | Tenable, AWS Inspector, weekly scans |
| 8.9 | Configuration management | A | Implemented | Terraform IaC; drift detection via AWS Config |
| 8.10 | Information deletion | A | Implemented | Automated data deletion per retention policy |
| 8.11 | Data masking | A | Implemented | PII masked in non-production environments |
| 8.12 | Data leakage prevention | A | Partially Implemented | DLP on email; endpoint DLP in evaluation |
| 8.15 | Logging | A | Implemented | CloudTrail, application logs, 36-month retention |
| 8.16 | Monitoring activities | A | Implemented | GuardDuty, Security Hub, Datadog |
| 8.20 | Networks security | A | Implemented | VPC segmentation, WAF, Security Groups |
| 8.23 | Web filtering | A | Implemented | DNS filtering via corporate network |
| 8.24 | Use of cryptography | A | Implemented | TLS 1.2+ in transit; AES-256 at rest via KMS |
| 8.25 | Secure development life cycle | A | Implemented | SAST in CI/CD; security review in design phase |
| 8.26 | Application security requirements | A | Implemented | Security requirements in sprint planning |
| 8.28 | Secure coding | A | Implemented | OWASP Top 10 training; code review checklist |
| 8.29 | Security testing in development and acceptance | A | Implemented | Automated SAST; annual pentest |
| 8.32 | Change management | A | Implemented | Jira-based CAB process; GitHub Actions enforcement |
| 8.33 | Test information | A | Implemented | Production data not used in test environments |
| 8.34 | Protection of information systems during audit testing | A | Implemented | Read-only audit access provisioned; change freeze during audit |

---

## Controls Marked Not Applicable (Summary)

| Control | Reason |
|---|---|
| 7.1 — Physical security perimeters | No company-owned data centres; AWS manages physical infrastructure |
| 7.5 — Protecting against physical/environmental threats | Fully delegated to AWS; documented in Subservice Organization section |
| 7.8 — Equipment siting and protection | All compute is cloud-hosted; office equipment governed by MDM |
| 8.30 — Outsourced development | All development performed by NexaCloud employees; no outsourced development |
| 8.31 — Separation of development, test and production | Fully implemented — not applicable as a gap |

---

*NCS-ISMS-SOA-001 v2.0 — ISO/IEC 27001:2022 Annex A*

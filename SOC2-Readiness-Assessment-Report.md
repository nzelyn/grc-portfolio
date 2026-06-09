# SOC 2 Type II Readiness Assessment Report — NexaCloud Solutions

**Document ID:** NCS-SOC2-RAR-001  
**Version:** 1.0  
**Report Date:** 20 August 2024  
**Assessment Period:** 15 July — 15 August 2024  
**Prepared By:** GRC Manager — Kavitha Ramesh  
**Reviewed By:** CISO — Deepa Venkataraman  
**Classification:** Confidential

---

## 1. Engagement Scope

### 1.1 Purpose

This readiness assessment evaluates NexaCloud Solutions' preparedness for a SOC 2 Type II audit against the AICPA Trust Services Criteria. It identifies control gaps, assigns remediation priorities, and produces an evidence collection plan.

### 1.2 Scope

- **Trust Service Criteria in scope:** Security (CC1-CC9), Availability (A1), Confidentiality (C1), Processing Integrity (PI1)
- **System boundary:** NexaCloud SIEM Platform, AWS production environments in ap-south-1 and us-east-1
- **Audit period (proposed):** 01 January 2025 — 31 December 2025 (first full-year period)

### 1.3 Assessment Methodology

Controls were assessed using:
- Interviews with control owners (IT Operations, Engineering, SecOps, GRC)
- Evidence inspection (screenshots, reports, ticket samples, policy documents)
- Configuration review (AWS Console, Okta Admin, GitHub Settings)
- Walkthrough testing (access provisioning, change management, incident response)

---

## 2. Overall Readiness Assessment

**Overall Readiness Rating: 83% (Substantially Ready)**

The company demonstrates strong foundational controls in change management, availability, and confidentiality. The primary gaps are in vendor risk management, privileged account oversight, and the incident response testing cadence.

---

## 3. Control Maturity Distribution

| Maturity Level | Control Count | Percentage |
|---|---|---|
| Optimizing (5) | 8 | 13% |
| Managed (4) | 26 | 41% |
| Defined (3) | 18 | 29% |
| Developing (2) | 8 | 13% |
| Initial (1) | 4 | 6% |
| **Total** | **64** | |

---

## 4. Key Observations by Domain

### 4.1 Logical Access (CC6) — 75% Ready

**Strengths:**
- Automated deprovisioning via Okta shows zero late offboarding in 12 months
- Encryption at rest enforced across all data stores via AWS KMS and Config rules
- Quarterly access reviews documented with CISO approval

**Gaps:**
- 8 service accounts lack MFA; exception process not yet formalized
- 3 engineers retain legacy broad IAM permissions from pre-role-definition era
- Vendor access process exists but lacks consistent documentation

### 4.2 System Operations (CC7) — 75% Ready

**Strengths:**
- Weekly vulnerability scans exceeding the monthly requirement
- Strong log retention (36 months) via S3 lifecycle policies
- GuardDuty and Security Hub provide robust continuous monitoring

**Gaps:**
- Last incident response tabletop exercise was February 2023; 18 months without testing
- Patch management for medium-severity findings tracks below 60% SLA compliance

### 4.3 Change Management (CC8) — 100% Ready

**Strengths:**
- All 47 changes in August 2024 followed the documented change management process
- GitHub Actions enforces 2-approver requirement for all production deployments
- Emergency change process documented and adhered to (INC-2024-0291 example)

### 4.4 Risk Mitigation (CC9) — 50% Ready

**Strengths:**
- BCP and DR plan exist and were tested in March 2024
- Cyber insurance current; policy reviewed annually

**Gaps:**
- No formal vendor risk questionnaire process; gap likely to be cited by auditor
- Annual risk assessment overdue by 2 months

### 4.5 Availability (A1) — 88% Ready

**Strengths:**
- 99.97% uptime achieved in H1 2024 against 99.9% SLA
- Auto Scaling Groups and Multi-AZ RDS demonstrate strong resilience architecture
- DR test in March 2024 met RTO of 4 hours

**Gaps:**
- Formal capacity planning review not documented for H1 2024

---

## 5. Remediation Plan Summary

| Priority | Finding | Owner | Target Date | Effort |
|---|---|---|---|---|
| P1 — High | Formalize MFA exception process; enforce MFA for 8 service accounts | IT Operations | 30 Sep 2024 | Low |
| P1 — High | Launch vendor risk assessment program | GRC | 31 Oct 2024 | Medium |
| P2 — Medium | Conduct IR tabletop exercise | Security Operations | 30 Nov 2024 | Medium |
| P2 — Medium | Enforce patch management SLA via automation | IT Operations | 30 Sep 2024 | Medium |
| P2 — Medium | Refresh annual risk assessment | GRC | 31 Oct 2024 | Medium |
| P3 — Low | Clean up legacy IAM permissions (3 engineers) | Engineering | 15 Oct 2024 | High |
| P3 — Low | Document capacity planning process | Engineering | 30 Sep 2024 | Low |

---

## 6. Mock Jira Remediation Tracker

| JIRA ID | Summary | Assignee | Due | Status |
|---|---|---|---|---|
| GRC-2024-0091 | Enforce MFA for all service accounts | Ranjit Kumar | 30 Sep 2024 | In Progress |
| GRC-2024-0092 | Create vendor risk questionnaire template | Kavitha Ramesh | 15 Oct 2024 | In Progress |
| GRC-2024-0093 | Schedule IR tabletop exercise | Arjun Pillai | 01 Nov 2024 | To Do |
| GRC-2024-0094 | Automate patch SLA tracking in Jira | Ranjit Kumar | 30 Sep 2024 | In Progress |
| GRC-2024-0095 | Refresh 2024 risk assessment | Kavitha Ramesh | 31 Oct 2024 | In Progress |
| GRC-2024-0096 | IAM permission cleanup — 3 engineers | Jake Morrison | 15 Oct 2024 | To Do |

---

## 7. Audit Readiness Conclusion

NexaCloud Solutions is on track to achieve SOC 2 Type II readiness by December 2024. All P1 findings have active remediation plans. The company's change management and availability controls are audit-ready. Evidence collection will begin 15 October 2024.

**Recommended Audit Window:** January — February 2025

---

*NCS-SOC2-RAR-001 v1.0 — Confidential — Prepared August 2024*

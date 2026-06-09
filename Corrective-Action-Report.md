# Corrective Action Report — ISMS

**Document ID:** NCS-ISMS-CAR-2024  
**Version:** 1.0  
**Reporting Period:** Q3 2024  
**Prepared By:** GRC Manager  
**Reference Standard:** ISO 27001:2022 Clause 10.1

---

## Corrective Action Register

| CAPA ID | Source | Finding Summary | Root Cause | Corrective Action | Owner | Due Date | Status | Verification |
|---|---|---|---|---|---|---|---|---|
| CAPA-2024-0031 | Internal Audit IA-2024-003 | Annual risk assessment not performed; infrastructure change not linked to risk review | No formal trigger in ISMS procedure for infrastructure changes to initiate partial risk assessment | Update ISMS procedure to mandate risk review for material changes; perform overdue risk assessment | GRC Manager | 31 Oct 2024 | Open | CISO sign-off on completed risk assessment |
| CAPA-2024-0032 | Internal Audit IA-2024-003 | 35% of reviewed documents lack classification labels | Document templates do not include classification field; no enforcement mechanism | Update all standard document templates in Confluence; issue all-staff communication; quarterly document audit | GRC Manager | 31 Oct 2024 | In Progress | Sample audit of 20 documents showing 95% label compliance |
| CAPA-2024-0033 | Internal Audit IA-2024-003 | CloudFlare, SendGrid, PagerDuty lack formal vendor risk assessments | Vendor onboarding process did not require risk assessment for tools classified as "low risk" | Perform risk assessments for all 3 vendors; update vendor onboarding SOP to require assessment for all Tier 1/2 vendors | GRC Manager | 31 Oct 2024 | In Progress | Completed assessment forms on file |
| CAPA-2024-0034 | Internal Audit IA-2024-003 | Security awareness training at 78% — below 95% ISMS objective | Training not tied to performance review; no escalation for non-completion | Link mandatory training completion to Q4 performance reviews; manager reminders monthly; real-time dashboard | HR Manager | 30 Sep 2024 | In Progress | Training completion report showing 95%+ |
| CAPA-2024-0035 | Internal Audit IA-2024-003 | Post-incident report for INC-2024-0251 not completed within 5-business-day SLA | Jira incident tickets did not automatically set PIR due date; manual process not enforced | Jira automation rule added to set PIR due date as ticket sub-task; SLA breach triggers CISO notification | SecOps Lead | 31 Oct 2024 | Implemented | Confirm automation working via test incident |
| CAPA-2024-0036 | SOC 2 Readiness Assessment | MFA not enforced for 8 service accounts | Service accounts excluded from MFA policy without formal exception documentation | Enforce MFA via Okta for all accounts or document formal exception with compensating controls; quarterly review | IT Operations | 30 Sep 2024 | In Progress | Okta MFA configuration showing 100% coverage or signed exception log |
| CAPA-2024-0037 | SOC 2 Readiness Assessment | Vendor risk program absent — no formal questionnaire process | Vendor risk was informally managed via SOC 2 report collection; no structured questionnaire | Launch vendor risk assessment program: template, scoring methodology, risk register; assess top 10 vendors | GRC Manager | 31 Oct 2024 | Open | Completed vendor questionnaires for top 10 vendors |

---

## Root Cause Category Analysis

| Category | Count | % |
|---|---|---|
| Missing or incomplete procedure | 3 | 43% |
| Process not enforced / no automation | 2 | 29% |
| Resource constraint | 1 | 14% |
| Awareness / training gap | 1 | 14% |

---

## CAPA Status Summary

| Status | Count |
|---|---|
| Open | 2 |
| In Progress | 4 |
| Implemented (pending verification) | 1 |
| Closed | 0 |

---

*NCS-ISMS-CAR-2024 v1.0 — ISO 27001:2022 Clause 10.1*

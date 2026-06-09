# Internal Audit Report — ISO 27001:2022 ISMS

**Document ID:** NCS-ISMS-IAR-2024  
**Audit Ref:** IA-2024-003  
**Audit Date:** 02-06 September 2024  
**Auditor:** GRC Manager (Internal Auditor — ISO 27001 Lead Auditor certified)  
**Auditee:** NexaCloud Solutions ISMS  
**Standard:** ISO/IEC 27001:2022  
**Report Date:** 13 September 2024  
**Classification:** Confidential

---

## 1. Audit Objectives

1. Evaluate conformance of the ISMS with ISO/IEC 27001:2022 requirements
2. Assess effectiveness of implemented Annex A controls
3. Identify areas for improvement prior to Stage 2 certification audit

---

## 2. Audit Scope

| Area | Clauses / Controls | Audit Method |
|---|---|---|
| ISMS Context and Leadership | Clauses 4, 5, 6 | Document review, management interview |
| Risk Assessment and Treatment | Clause 6.1, 8.2, 8.3 | Document review, evidence inspection |
| Logical Access Controls | Annex A 5.15-5.18, 8.2-8.5 | Configuration review, walkthrough |
| Incident Management | Annex A 5.24-5.28 | Document review, case file review |
| Change Management | Annex A 8.32 | Ticket sampling (15 tickets) |
| Supplier Relationships | Annex A 5.19-5.22 | Document review, interview |
| Vulnerability Management | Annex A 8.8 | Report review, scan evidence |

---

## 3. Audit Findings Summary

| Severity | Count |
|---|---|
| Major Nonconformity | 1 |
| Minor Nonconformity | 4 |
| Observation | 7 |

---

## 4. Major Nonconformity

### Finding IA-2024-003-NC-001 (Major)

**Clause/Control:** ISO 27001:2022 Clause 6.1.2 — Information security risk assessment  
**Standard Requirement:** The organization shall retain documented information about the information security risk assessment process and results.

**Finding:** The current risk register (NCS-ISMS-RR-2024) was last formally reviewed and signed off in October 2023. No documented evidence of a risk assessment review was found between October 2023 and the audit date (September 2024). ISO 27001:2022 requires the risk assessment to be performed at planned intervals or when significant changes occur. An AWS infrastructure migration occurred in June 2024 (expanding ap-south-1 capacity) without a triggered risk assessment.

**Evidence Referenced:**
- Risk register version history: last update October 2023
- AWS migration change ticket (CHANGE-2024-0412) — no GRC risk review linked
- ISMS schedule: risk assessment due September 2024 (not yet started at audit date)

**Corrective Action Required:** Perform and document the annual risk assessment by 31 October 2024. Update ISMS procedure to trigger risk assessment reviews for material infrastructure changes.

**Target Close Date:** 31 October 2024  
**Owner:** GRC Manager

---

## 5. Minor Nonconformities

### Finding IA-2024-003-NC-002 (Minor)

**Control:** Annex A 5.13 — Labelling of information  
**Finding:** Information classification labels are defined in the Data Classification Policy but are not consistently applied to internal documents. Of 20 documents reviewed, 7 (35%) lacked a classification label.  
**Corrective Action:** Update document templates to include classification label; issue reminder to all document owners.  
**Target Close Date:** 31 October 2024

---

### Finding IA-2024-003-NC-003 (Minor)

**Control:** Annex A 5.19 — Information security in supplier relationships  
**Finding:** Three active vendors (CloudFlare, SendGrid, PagerDuty) do not have documented vendor risk assessments. NexaCloud's Vendor Risk Management Policy requires annual assessments for all Tier 1 and Tier 2 vendors.  
**Corrective Action:** Complete risk assessments for all Tier 1/2 vendors without documented assessment by 31 October 2024.  
**Target Close Date:** 31 October 2024

---

### Finding IA-2024-003-NC-004 (Minor)

**Control:** Annex A 6.3 — Information security awareness, education and training  
**Finding:** Security awareness training completion for Q2 2024 was 78%, below the ISMS objective of 95%.  
**Corrective Action:** HR to send escalation reminders; managers responsible for team completion; monthly reporting to CISO until target met.  
**Target Close Date:** 30 September 2024

---

### Finding IA-2024-003-NC-005 (Minor)

**Control:** Annex A 5.26 — Response to information security incidents  
**Finding:** The post-incident report for INC-2024-0251 (API latency spike, July 2024) was not completed within the 5-business-day SLA. The report was completed 9 business days after incident closure.  
**Corrective Action:** Remind incident owners of PIR SLA; add PIR due date to incident tickets automatically via Jira automation.  
**Target Close Date:** 31 October 2024

---

## 6. Observations (Non-Conformities — Improvement Opportunities)

| OBS # | Control | Observation | Recommendation |
|---|---|---|---|
| OBS-001 | 8.6 — Capacity management | No formal documented capacity plan for H1 2025 despite strong Auto Scaling controls | Produce capacity planning document before Stage 2 audit |
| OBS-002 | 7.4 — Physical security monitoring | Austin office relies on building security provider; no CCTV or dedicated security logging | Implement CCTV or accept and formally document residual risk |
| OBS-003 | 8.12 — Data leakage prevention | Email DLP is in place; endpoint DLP has been in evaluation for 9 months without decision | Make a Go/No-Go decision on endpoint DLP by December 2024 |
| OBS-004 | 5.35 — Independent review | ISMS has not had an external independent review; internal audit is performed by same team that manages GRC | Consider external ISMS review or rotate internal audit responsibility |

---

## 7. Positive Observations

The following areas demonstrated strong conformance and maturity:

- Change management (Annex A 8.32): 100% of sampled changes followed documented process; GitHub Actions enforces controls technically
- Incident detection and containment: GuardDuty and Security Hub provide automated, near-real-time threat detection
- Encryption controls (Annex A 8.24): TLS 1.2+ enforced in transit; AES-256 at rest via AWS KMS across all data stores
- Offboarding controls (Annex A 5.11): Zero instances of access remaining active more than 24 hours after termination in 12-month period

---

## 8. Corrective Action Summary

| CAPA ID | Finding | Severity | Owner | Due Date | Status |
|---|---|---|---|---|---|
| CAPA-2024-0031 | Annual risk assessment not performed | Major | GRC Manager | 31 Oct 2024 | Open |
| CAPA-2024-0032 | Document labelling inconsistency | Minor | GRC Manager | 31 Oct 2024 | Open |
| CAPA-2024-0033 | Missing vendor risk assessments | Minor | GRC Manager | 31 Oct 2024 | Open |
| CAPA-2024-0034 | Security training below 95% target | Minor | HR Manager | 30 Sep 2024 | Open |
| CAPA-2024-0035 | Post-incident report SLA missed | Minor | Security Operations | 31 Oct 2024 | Open |

---

## 9. Audit Conclusion

The ISMS demonstrates substantial conformance with ISO/IEC 27001:2022. The major nonconformity (risk assessment cadence) is a documentation gap rather than a fundamental control failure. All corrective actions are assigned and on track. The ISMS is on course for Stage 2 certification in Q1 2025, provided the major nonconformity is resolved and closed by November 2024.

---

**Auditor Sign-Off**

| Name | Role | Signature | Date |
|---|---|---|---|
| Kavitha Ramesh | Internal Auditor | [Signed] | 13 Sep 2024 |
| Deepa Venkataraman | CISO / ISMS Owner | [Reviewed] | 16 Sep 2024 |

---

*NCS-ISMS-IAR-2024 — IA-2024-003*

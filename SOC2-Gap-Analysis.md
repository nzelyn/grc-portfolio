# SOC 2 Gap Analysis — NexaCloud Solutions

**Document ID:** NCS-SOC2-GA-001  
**Version:** 1.3  
**Assessment Date:** 15 August 2024  
**Assessor:** GRC Manager  
**Reviewed By:** CISO  
**Status:** Final

---

## Maturity Rating Scale

| Rating | Score | Definition |
|---|---|---|
| Initial | 1 | Ad hoc, undocumented, dependent on individuals |
| Developing | 2 | Partially documented, inconsistently applied |
| Defined | 3 | Documented, consistently applied, not formally tested |
| Managed | 4 | Documented, tested, with metrics and monitoring |
| Optimizing | 5 | Continuously improved, automated where possible |

---

## Gap Analysis Summary

| TSC Category | Controls Assessed | Fully Met | Partially Met | Not Met | Avg Maturity |
|---|---|---|---|---|---|
| CC1 — Control Environment | 5 | 4 | 1 | 0 | 3.8 |
| CC2 — Communication | 3 | 2 | 1 | 0 | 3.3 |
| CC3 — Risk Assessment | 4 | 3 | 1 | 0 | 3.5 |
| CC4 — Monitoring | 4 | 3 | 0 | 1 | 3.0 |
| CC5 — Control Activities | 5 | 4 | 1 | 0 | 3.6 |
| CC6 — Logical Access | 8 | 5 | 2 | 1 | 3.1 |
| CC7 — System Operations | 6 | 4 | 1 | 1 | 3.0 |
| CC8 — Change Management | 5 | 5 | 0 | 0 | 4.2 |
| CC9 — Risk Mitigation | 4 | 2 | 1 | 1 | 2.8 |
| A1 — Availability | 8 | 7 | 1 | 0 | 4.0 |
| C1 — Confidentiality | 7 | 6 | 1 | 0 | 3.9 |
| PI1 — Processing Integrity | 5 | 4 | 1 | 0 | 3.7 |
| **Total** | **64** | **49** | **11** | **4** | **3.5** |

---

## Detailed Control Findings

### CC6 — Logical and Physical Access Controls

| Control ID | Control Description | Status | Maturity | Gap Detail | Remediation Owner | Target Date |
|---|---|---|---|---|---|---|
| CC6.1 | MFA enforced for all system access | Partially Met | 3 | MFA enforced for 94% of users; 8 service accounts exempted without documented exception | IT Operations | 30 Sep 2024 |
| CC6.2 | Privileged access reviewed quarterly | Fully Met | 4 | Quarterly reviews documented in Jira; last review: 01 Aug 2024 | Security Operations | N/A |
| CC6.3 | Access provisioning follows documented workflow | Fully Met | 4 | Okta lifecycle management configured; HR-to-IT onboarding workflow documented | IT Operations | N/A |
| CC6.4 | Access deprovisioning within 24 hours of termination | Fully Met | 5 | Automated Okta deprovisioning; 0 exceptions in last 12 months | IT Operations | N/A |
| CC6.5 | Least privilege enforced for production access | Partially Met | 3 | IAM roles defined; 3 engineers retain legacy broad permissions not yet scoped down | Engineering | 15 Oct 2024 |
| CC6.6 | Physical access controls at data centers | Not Met | N/A | AWS manages physical access; CUECs documented; evidence of AWS SOC 2 review needed | GRC | 01 Sep 2024 |
| CC6.7 | Vendor access reviewed before provisioning | Fully Met | 3 | Vendor access form in place; reviews occur but not consistently documented | GRC | N/A |
| CC6.8 | Encryption at rest enforced for all data stores | Fully Met | 5 | AWS KMS enabled for all RDS and S3; Config rule enforces compliance | Engineering | N/A |

### CC7 — System Operations

| Control ID | Control Description | Status | Maturity | Gap Detail | Remediation Owner | Target Date |
|---|---|---|---|---|---|---|
| CC7.1 | Vulnerability scanning performed monthly | Fully Met | 4 | AWS Inspector and Tenable scans run weekly; reports reviewed by SecOps | Security Operations | N/A |
| CC7.2 | Critical patches applied within 30 days | Partially Met | 3 | 3 systems exceeded 30-day SLA in last quarter; no automated enforcement | IT Operations | 30 Sep 2024 |
| CC7.3 | Incident response plan documented and approved | Fully Met | 4 | IRP v3.2 approved by CISO; available in Security Policy Repository | GRC | N/A |
| CC7.4 | Incident response plan tested annually | Not Met | 2 | Last tabletop exercise: February 2023 (18 months ago); no test in 2024 | Security Operations | 30 Nov 2024 |
| CC7.5 | Security monitoring alerts reviewed daily | Fully Met | 4 | GuardDuty + Security Hub findings reviewed each morning by SecOps | Security Operations | N/A |
| CC7.6 | Log retention for 12 months minimum | Fully Met | 5 | CloudTrail and application logs stored in S3 with lifecycle policy; 36-month retention | Engineering | N/A |

### CC9 — Risk Mitigation

| Control ID | Control Description | Status | Maturity | Gap Detail | Remediation Owner | Target Date |
|---|---|---|---|---|---|---|
| CC9.1 | Formal risk assessment performed annually | Partially Met | 3 | Last formal risk assessment: October 2023; due for refresh | GRC | 31 Oct 2024 |
| CC9.2 | Vendor risk assessments documented | Not Met | 2 | No formal vendor risk questionnaire process; reliance on SOC reports only | GRC | 31 Oct 2024 |
| CC9.3 | Business continuity plan exists and is tested | Fully Met | 4 | BCP v2.0 documented; DR test completed March 2024; RTO achieved | Engineering | N/A |
| CC9.4 | Insurance coverage for cyber events | Fully Met | 4 | Cyber insurance policy renewed June 2024 | Finance | N/A |

---

## Remediation Priority Matrix

| Priority | Finding | Owner | Effort | Impact | Target |
|---|---|---|---|---|---|
| P1 | MFA for all service accounts | IT Operations | Low | High | 30 Sep 2024 |
| P1 | Vendor risk assessment process | GRC | Medium | High | 31 Oct 2024 |
| P2 | IR tabletop exercise | Security Operations | Medium | Medium | 30 Nov 2024 |
| P2 | Patch management SLA enforcement | IT Operations | Medium | Medium | 30 Sep 2024 |
| P3 | Legacy IAM permission cleanup | Engineering | High | Medium | 15 Oct 2024 |
| P3 | Annual risk assessment refresh | GRC | Medium | Medium | 31 Oct 2024 |

---

## Evidence Naming Convention

All evidence files must follow this naming format:

```
NCS-[TSC]-[ControlID]-[EvidenceType]-[YYYYMM]-v[Version]
```

Examples:
- `NCS-CC6-001-AccessReview-202408-v1.xlsx`
- `NCS-CC7-004-VulnScanReport-202408-v1.pdf`
- `NCS-A1-001-UptimeReport-202408-v1.pdf`

---

## Audit Timeline

| Milestone | Target Date | Owner | Status |
|---|---|---|---|
| Gap analysis complete | 15 Aug 2024 | GRC Manager | Complete |
| P1 remediations complete | 30 Sep 2024 | Various | In Progress |
| Evidence collection round 1 | 15 Oct 2024 | GRC Manager | Planned |
| P2 remediations complete | 30 Nov 2024 | Various | Planned |
| Pre-audit readiness review | 15 Dec 2024 | CISO + GRC | Planned |
| Auditor fieldwork begins | 06 Jan 2025 | External Auditor | Planned |
| Draft report received | 14 Feb 2025 | External Auditor | Planned |
| Final SOC 2 report issued | 28 Feb 2025 | External Auditor | Planned |

---

*End of Gap Analysis — NCS-SOC2-GA-001 v1.3*

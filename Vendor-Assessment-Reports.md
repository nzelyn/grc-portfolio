# Vendor Assessment Reports — NexaCloud Solutions

**Document ID:** NCS-GRC-VAR-2024  
**Version:** 1.0  
**Prepared By:** GRC Manager  
**Classification:** Confidential

---

## Assessment 1 — Amazon Web Services

**Assessment Date:** 12 August 2024  
**Service:** Cloud infrastructure (IaaS/PaaS)  
**Tier:** 1 — Critical  
**Assessed By:** GRC Manager via SOC 2 report review + AWS Trust Center documentation

| Domain | Score | Max | % | Notes |
|---|---|---|---|---|
| Governance and Risk Management | 14 | 15 | 93% | ISO 27001 certified; annual risk reviews documented |
| Access Control | 19 | 20 | 95% | IAM, SCPs, MFA on root enforced |
| Data Protection | 20 | 20 | 100% | KMS, encryption at rest/transit, FIPS 140-2 |
| Incident Response | 14 | 15 | 93% | 24-hour notification per AWS customer agreement |
| Vulnerability Management | 9 | 10 | 90% | Bug bounty program; CVE process documented |
| Business Continuity | 10 | 10 | 100% | Multi-AZ, multi-region; 99.99% SLA |
| Compliance | 10 | 10 | 100% | SOC 1, SOC 2, SOC 3, ISO 27001, CSA STAR, FedRAMP |
| **Total** | **96** | **100** | **96%** | **Low Risk** |

**Recommendation:** Approved. No remediation required. CUECs reviewed and documented. Annual SOC 2 report collected.

---

## Assessment 2 — CloudFlare

**Assessment Date:** 08 October 2024  
**Service:** DDoS protection and CDN  
**Tier:** 1 — Critical  
**Assessed By:** GRC Manager via questionnaire + SOC 2 report review

| Domain | Score | Max | % | Notes |
|---|---|---|---|---|
| Governance and Risk Management | 12 | 15 | 80% | Security policy exists; CISO in place; no ISO certification |
| Access Control | 17 | 20 | 85% | MFA enforced; quarterly reviews confirmed |
| Data Protection | 17 | 20 | 85% | Encryption in place; DPA available but basic |
| Incident Response | 9 | 15 | 60% | IRP documented; notification clause vague in contract |
| Vulnerability Management | 7 | 10 | 70% | Scans monthly; pentest summary only (not full report) |
| Business Continuity | 9 | 10 | 90% | Anycast network provides inherent resilience |
| Compliance | 7 | 10 | 70% | SOC 2 Type II available; no ISO 27001 |
| **Total** | **78** | **100** | **78%** | **Medium Risk** |

**Recommendation:** Conditionally approved. Require contract update to include 24-hour incident notification SLA. Obtain full penetration test report at next renewal.

---

## Assessment 3 — SendGrid (Twilio)

**Assessment Date:** 10 October 2024  
**Service:** Transactional email delivery  
**Tier:** 2 — High  
**Assessed By:** GRC Manager via questionnaire

| Domain | Score | Max | % | Notes |
|---|---|---|---|---|
| Governance and Risk Management | 11 | 15 | 73% | Policy in place; annual review confirmed |
| Access Control | 13 | 20 | 65% | MFA not enforced for all admin accounts |
| Data Protection | 12 | 20 | 60% | DPA not yet signed; needs PDPB-compliant language |
| Incident Response | 11 | 15 | 73% | IRP documented and tested; notification process unclear |
| Vulnerability Management | 6 | 10 | 60% | Monthly scans; no pentest evidence provided |
| Business Continuity | 8 | 10 | 80% | BCP exists; DR test completed 2023 |
| Compliance | 7 | 10 | 70% | SOC 2 Type II available |
| **Total** | **68** | **100** | **68%** | **Medium Risk — Remediation Required** |

**Recommendation:** Conditionally approved with 3 open action items. DPA must be signed by 30 November 2024 or service must be suspended. MFA for admin accounts required by January 2025.

---

*NCS-GRC-VAR-2024 v1.0*

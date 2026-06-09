# Vendor Risk Management Policy

**Document ID:** NCS-POL-005  
**Version:** 1.1  
**Effective Date:** 01 September 2024  
**Policy Owner:** GRC Manager  
**Approved By:** CISO  
**Classification:** Internal

---

## 1. Purpose

This policy establishes how NexaCloud Solutions identifies, assesses, manages, and monitors risks associated with third-party vendors and service providers.

---

## 2. Scope

Applies to all vendors, suppliers, and service providers who:
- Have access to NexaCloud systems, networks, or data
- Process or store NexaCloud or customer data on behalf of NexaCloud
- Provide services that are critical to platform availability

---

## 3. Vendor Tiering

| Tier | Criteria | Examples | Review Frequency |
|---|---|---|---|
| Tier 1 — Critical | Processes customer data or is critical to platform uptime | AWS, Okta, GitHub, Datadog | Annual security questionnaire + SOC 2 review |
| Tier 2 — High | Has access to internal systems or confidential data | Jira, Vanta, Tenable, CrowdStrike | Annual SOC 2 review; questionnaire every 2 years |
| Tier 3 — Standard | No access to systems or data; standard commercial relationship | Office supplies, travel booking | No formal security assessment required |

---

## 4. Vendor Onboarding Requirements

All Tier 1 and Tier 2 vendors must satisfy the following before being onboarded:

- Signed NDA and Data Processing Agreement (DPA) where applicable
- Completion of NexaCloud Vendor Security Questionnaire
- Provision of current SOC 2 Type II report (or equivalent — ISO 27001 certificate, CSA STAR)
- Legal review for contracts with data processing or liability clauses above $50,000 annually

---

## 5. Ongoing Monitoring

| Activity | Tier 1 | Tier 2 | Owner |
|---|---|---|---|
| Collect and review updated SOC 2 report | Annual | Annual | GRC Manager |
| Security questionnaire refresh | Annual | Every 2 years | GRC Manager |
| Review vendor security news and breach disclosures | Continuous | Quarterly | GRC Manager |
| Contract and DPA renewal review | Per contract | Per contract | Legal + GRC |

---

## 6. Vendor Risk Register

All Tier 1 and Tier 2 vendors must be recorded in the Vendor Risk Register (see Vendor-Risk-Assessment project). The register tracks:
- Vendor name and service description
- Tier classification
- Last assessment date and score
- Open risk items and remediation status
- Next review date

---

## 7. Vendor Incident Notification

Vendors must notify NexaCloud within 24 hours of any security incident that may affect NexaCloud or its customers. Vendor NDAs and contracts must include this obligation.

---

## 8. Approval

| Role | Name | Date |
|---|---|---|
| GRC Manager | Kavitha Ramesh | 01 Sep 2024 |
| CISO | Deepa Venkataraman | 05 Sep 2024 |

**Framework Alignment:** SOC 2 CC9.2 | ISO 27001:2022 Annex A 5.19-5.22

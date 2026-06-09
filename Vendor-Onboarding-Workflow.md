# Vendor Onboarding Security Workflow — NexaCloud Solutions

**Document ID:** NCS-GRC-VOW-001  
**Version:** 1.0  
**Owner:** GRC Manager

---

## Workflow Overview

```
Step 1: Procurement Request
Requestor submits new vendor request via Jira (VENDOR project)
Include: vendor name, service description, data access type, estimated spend

Step 2: Tier Classification (GRC — 1 business day)
GRC classifies vendor as Tier 1, 2, or 3 based on data access and criticality

Step 3: Tier 3 Vendors
No security assessment required
Proceed to contract review and approval
Estimated total time: 3-5 days

Step 4: Tier 1 / 2 Vendors (GRC — target 10 days)
4a. Send Vendor Security Questionnaire (NCS-GRC-VSQ-001)
4b. Request SOC 2 Type II report (or ISO 27001 certificate)
4c. Request signed NDA
4d. Legal review: DPA if data processing involved
4e. Score questionnaire and calculate risk level

Step 5: Risk Determination
Low Risk: Approve — proceed to contracting
Medium Risk: Conditional approval — document open items; remediation timeline agreed
High Risk: Escalate to CISO — additional review; compensating controls required
Critical Risk: Do not approve — escalate to CISO; seek alternative vendor

Step 6: Contract Finalization
Include security requirements in contract:
- 24-hour incident notification clause
- Right to audit
- Data protection obligations
- Breach liability

Step 7: Onboarding Approval
GRC signs off on vendor security approval
Vendor added to Vendor Risk Register
Access provisioned per Access Control Policy

Step 8: Ongoing Monitoring
Tier 1: Annual questionnaire + SOC 2 review
Tier 2: Annual SOC 2 review; questionnaire every 2 years
Monitor vendor security news and breach disclosures
```

---

## SLA Targets

| Step | Target |
|---|---|
| Tier classification | 1 business day |
| Questionnaire return | 10 business days (vendor) |
| GRC review and scoring | 3 business days |
| Full Tier 1/2 onboarding (security track) | 10 business days total |

---

*NCS-GRC-VOW-001 v1.0*

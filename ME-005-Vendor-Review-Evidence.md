# Mock Evidence Artifact — Annual Vendor SOC 2 Report Review

**Evidence ID:** NCS-CC9-003-VendorSOCReview-202408-v1  
**Control:** CC9.2 — Third-party vendor reports reviewed annually  
**Review Period:** August 2024  
**Reviewed By:** GRC Manager  
**Approved By:** CISO  
**Classification:** Confidential

---

## Vendor SOC 2 Report Review Log

| Vendor | Report Type | Report Period | Review Date | Reviewed By | Opinion | Exceptions | Notes |
|---|---|---|---|---|---|---|---|
| Amazon Web Services | SOC 2 Type II | Oct 2023 — Sep 2024 | 12 Aug 2024 | GRC Manager | Unqualified | 0 | AWS SOC 2 covers all relevant Trust Services |
| Okta | SOC 2 Type II | Jan 2024 — Jun 2024 | 12 Aug 2024 | GRC Manager | Unqualified | 0 | Semi-annual report; next expected Jan 2025 |
| Atlassian (Jira/Confluence) | SOC 2 Type II | Apr 2023 — Mar 2024 | 14 Aug 2024 | GRC Manager | Unqualified | 1 | 1 exception noted (see below) |
| GitHub (Microsoft) | SOC 2 Type II | Oct 2023 — Sep 2024 | 14 Aug 2024 | GRC Manager | Unqualified | 0 | |
| Datadog | SOC 2 Type II | Jan 2024 — Jun 2024 | 15 Aug 2024 | GRC Manager | Unqualified | 0 | |

---

## Exception Detail — Atlassian

**Control:** Atlassian stated that "access reviews were performed quarterly" but one quarter had a 4-week delay due to a staffing gap.

**NexaCloud Assessment:** Low risk. Delay was isolated and disclosed by Atlassian. NexaCloud's use of Jira is limited to non-customer-data-bearing change management. No compensating controls required.

**Resolution:** Noted in vendor risk register. Next Atlassian SOC 2 report will be reviewed upon issuance.

---

## Complementary User Entity Controls (CUECs) Review

For each vendor, GRC confirmed NexaCloud meets applicable CUECs:

| Vendor | CUEC # | CUEC Description | NexaCloud Status |
|---|---|---|---|
| AWS | 1 | Configure IAM policies following least-privilege | Met — IAM roles reviewed quarterly |
| AWS | 2 | Enable AWS CloudTrail in all regions | Met — enabled globally |
| Okta | 1 | Review and manage Okta administrator accounts | Met — quarterly access review |
| GitHub | 1 | Enable 2FA for all organization members | Met — enforced via Org policy |

---

## Sign-Off

| Role | Name | Date |
|---|---|---|
| GRC Manager | Kavitha Ramesh | 15 Aug 2024 |
| CISO | Deepa Venkataraman | 20 Aug 2024 |

---

*This document serves as evidence for SOC 2 Type II audit — Control CC9.2*

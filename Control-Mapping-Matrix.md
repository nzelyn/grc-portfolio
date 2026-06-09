# Multi-Framework Control Mapping Matrix — NexaCloud Solutions

**Document ID:** NCS-GRC-MFCM-001  
**Version:** 1.0  
**Owner:** GRC Manager

---

## Control Mapping Matrix (Selected Controls)

| Control Domain | SOC 2 TSC | ISO 27001:2022 | NIST CSF 2.0 | Shared Evidence | NexaCloud Status | Evidence Location |
|---|---|---|---|---|---|---|
| Identity and Access Management | CC6.1, CC6.2, CC6.3 | 5.15, 5.16, 5.17, 5.18, 8.2, 8.3, 8.5 | PR.AA-01, PR.AA-02, PR.AA-03 | Yes — Okta access reviews, IAM policy exports | Implemented | Jira + Okta Admin |
| MFA Enforcement | CC6.1 | 8.5 | PR.AA-01 | Yes — Okta MFA config screenshot | Implemented | Okta Admin Console |
| Access Deprovisioning | CC6.3 | 5.11, 5.18 | PR.AA-05 | Yes — termination checklist + Okta logs | Implemented | Jira + Rippling |
| Privileged Access Review | CC6.2 | 5.18, 8.2 | PR.AA-03 | Yes — quarterly review reports | Implemented | Jira (quarterly review tickets) |
| Vulnerability Management | CC7.1 | 8.8 | ID.RA-01, PR.IP-12 | Yes — Tenable scan reports | Implemented | SharePoint |
| Patch Management | CC7.1 | 8.8 | PR.IP-12 | Yes — Jira patch tracking | Partially Implemented | Jira |
| Incident Response Plan | CC7.3, CC7.4 | 5.24, 5.25, 5.26 | RS.MA-01, RS.MA-02 | Yes — IRP document + test evidence | Implemented | Confluence |
| Incident Detection and Alerting | CC7.2 | 8.16 | DE.CM-01, DE.AE-02 | Yes — GuardDuty + Security Hub config | Implemented | AWS Console |
| Security Logging | CC7.2 | 8.15 | DE.CM-03, RS.CO-03 | Yes — CloudTrail config + retention policy | Implemented | AWS Console |
| Change Management | CC8.1 | 8.32 | PR.IP-03 | Yes — CAB tickets + GitHub Actions config | Implemented | Jira + GitHub |
| Segregation of Duties | CC5.3 | 5.3 | PR.AA-05 | Yes — SoD matrix | Implemented | Confluence |
| Security Awareness Training | CC1.4 | 6.3 | PR.AT-01 | Yes — KnowBe4 completion report | Partially Implemented | KnowBe4 Dashboard |
| Encryption at Rest | CC6.1 | 8.24 | PR.DS-01 | Yes — AWS KMS config + Config rules | Implemented | AWS Console |
| Encryption in Transit | CC6.1 | 8.24 | PR.DS-02 | Yes — TLS policy + SSL scan results | Implemented | SSL Labs scan |
| Business Continuity / DR | A1.2, A1.3 | 5.29, 5.30 | RC.RP-01, RC.RP-02 | Yes — BCP document + DR test results | Implemented | Confluence |
| Asset Inventory | CC6.1 | 5.9 | ID.AM-01, ID.AM-02 | Yes — Asset inventory spreadsheet | Implemented | Confluence |
| Vendor Risk Management | CC9.2 | 5.19-5.22 | ID.SC-01, ID.SC-02 | Partial — SOC 2 reviews; questionnaires in progress | Partially Implemented | SharePoint |
| Risk Assessment | CC3.1, CC3.2 | 6.1.2, 8.2 | ID.RA-01-06 | Yes — risk register + assessment report | Partially Implemented (overdue) | Confluence |
| Background Checks | CC1.2 | 6.1 | PR.AT-02 | Yes — screening policy + sample evidence | Implemented | HR System |
| Data Classification | C1.1 | 5.12, 5.13 | ID.AM-05 | Yes — Data Classification Policy | Partially Implemented | Confluence |

---

## Compliance Status Summary

| Framework | Controls Assessed | Fully Met | Partially Met | Not Met |
|---|---|---|---|---|
| SOC 2 Type II (64 controls) | 64 | 52 | 11 | 1 |
| ISO 27001:2022 (88 applicable) | 88 | 62 | 20 | 6 |
| NIST CSF 2.0 (selected 40 subcategories) | 40 | 29 | 9 | 2 |

---

## Shared Evidence Opportunities

Controls with shared evidence across all three frameworks — assess once, use for all three:

1. Okta access review reports (CC6.1/CC6.2 + 5.15/5.18 + PR.AA-01/03)
2. CloudTrail log retention configuration (CC7.2 + 8.15 + DE.CM-03)
3. Incident response plan and test evidence (CC7.3 + 5.24-5.26 + RS.MA-01)
4. Change management tickets (CC8.1 + 8.32 + PR.IP-03)
5. BCP and DR test report (A1.2/A1.3 + 5.29/5.30 + RC.RP-01)
6. Vulnerability scan reports (CC7.1 + 8.8 + ID.RA-01)
7. Security awareness training report (CC1.4 + 6.3 + PR.AT-01)
8. Encryption configuration screenshots (CC6.1 + 8.24 + PR.DS-01/02)

These 8 evidence packages satisfy 45+ individual control requirements across the three frameworks.

---

*NCS-GRC-MFCM-001 v1.0*

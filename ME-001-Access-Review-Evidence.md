# Mock Evidence Artifact — Quarterly Access Review

**Evidence ID:** NCS-CC6-001-AccessReview-202408-v1  
**Control:** CC6.2 — Privileged access reviewed quarterly  
**Review Period:** Q3 2024 (01 July — 31 August 2024)  
**Reviewed By:** IT Operations Manager  
**Approved By:** CISO  
**Review Date:** 05 August 2024  
**Classification:** Confidential

---

## Review Scope

This review covers all privileged accounts across production systems including:
- AWS root and IAM administrative accounts
- Okta Super Administrator accounts
- GitHub Organization owners
- NexaCloud production database direct access accounts
- Jira/Confluence administrator accounts

---

## Privileged Account Inventory

| Account | System | Role | Account Type | Last Login | Review Action | Justification |
|---|---|---|---|---|---|---|
| svc-deploy-prod | AWS IAM | DeploymentRole | Service Account | 2024-08-01 | Retain | Used daily by CI/CD pipeline |
| svc-monitoring | AWS IAM | ReadOnlySecurityAudit | Service Account | 2024-08-04 | Retain | Continuous monitoring via Datadog |
| admin-ranjit.kumar | Okta | Super Admin | User Account | 2024-07-28 | Retain | IT Operations Manager — role required |
| admin-priya.nair | Okta | Super Admin | User Account | 2024-08-02 | Retain | IT Operations Engineer — role required |
| admin-jake.morrison | GitHub | Org Owner | User Account | 2024-08-05 | Retain | VP Engineering — role required |
| admin-sarah.okonkwo | GitHub | Org Owner | User Account | 2024-07-31 | Retain | Principal Engineer — role required |
| root-aws-prod | AWS | Root | Root Account | 2024-06-01 | Flagged | Root login detected — requires investigation |
| db-admin-legacy | AWS RDS | db_superuser | Service Account | 2024-05-12 | Revoke | Legacy account; no active owner identified |
| admin-tom.hayes | Jira | Jira Admin | User Account | 2024-03-15 | Revoke | Tom Hayes departed March 2024; account not deprovisioned |

---

## Findings

| Finding # | Severity | Description | Action |
|---|---|---|---|
| ACR-2024-Q3-001 | High | Root AWS account login detected June 2024 without documented business justification | SecOps to review CloudTrail logs; enforce MFA on root; document exception |
| ACR-2024-Q3-002 | Medium | Legacy db-admin-legacy service account with no active owner | Revoke immediately; Engineering to confirm no dependencies |
| ACR-2024-Q3-003 | High | Tom Hayes (departed) account not deprovisioned from Jira | Revoke immediately; HR/IT Ops to review offboarding process |

---

## Actions Taken

| Finding # | Action | Responsible | Completed Date |
|---|---|---|---|
| ACR-2024-Q3-001 | CloudTrail investigation completed; use attributed to ad hoc billing query by Finance; documented and policy reminder sent | Security Operations | 12 Aug 2024 |
| ACR-2024-Q3-002 | db-admin-legacy account revoked via IAM policy; no application dependencies confirmed | IT Operations | 08 Aug 2024 |
| ACR-2024-Q3-003 | tom.hayes Jira account disabled; HR offboarding checklist updated to include Jira step | IT Operations | 06 Aug 2024 |

---

## Sign-Off

| Role | Name | Signature | Date |
|---|---|---|---|
| IT Operations Manager | Ranjit Kumar | [Signed] | 05 Aug 2024 |
| CISO | Deepa Venkataraman | [Signed] | 12 Aug 2024 |

---

*This document serves as evidence for SOC 2 Type II audit — Control CC6.2*

# Mock Evidence Artifact — Change Management Sample Tickets

**Evidence ID:** NCS-CC8-002-ChangeTickets-202408-v1  
**Control:** CC8.1 — Changes to infrastructure and applications follow documented change control process  
**Sample Period:** August 2024 (5 of 47 change tickets selected)  
**Prepared By:** GRC Manager  
**Classification:** Confidential

---

## Change Management Process Overview

All production changes at NexaCloud follow a 4-stage process:

1. **Request:** Engineer submits change ticket in Jira (CHANGE project)
2. **Review:** Change Advisory Board (CAB) reviews tickets every Tuesday 10:00 IST
3. **Approval:** CAB lead or VP Engineering approves; emergency changes require CISO approval
4. **Deployment:** Changes deployed via GitHub Actions with mandatory peer review (2 approvers for production)

---

## Sample Change Tickets

### Ticket CHANGE-2024-0847

| Field | Value |
|---|---|
| Ticket ID | CHANGE-2024-0847 |
| Date Submitted | 01 Aug 2024 |
| Submitted By | Ananya Krishnan (Senior Engineer) |
| Change Type | Standard |
| Environment | Production |
| Description | Upgrade NGINX from 1.24.0 to 1.26.0 on api-gateway-01 to address CVE-2024-44487 |
| Risk Level | Medium |
| Rollback Plan | Revert to NGINX 1.24.0 image; estimated 15 minutes |
| Testing Evidence | Deployed to staging 28 Jul 2024; 72-hour soak test completed |
| CAB Approval | Deepa Venkataraman — 05 Aug 2024 |
| Deployed By | Ananya Krishnan |
| Deployment Date | 08 Aug 2024 02:15 UTC (maintenance window) |
| Post-Deploy Verification | All health checks passing; no customer impact |
| Status | Completed |

---

### Ticket CHANGE-2024-0851

| Field | Value |
|---|---|
| Ticket ID | CHANGE-2024-0851 |
| Date Submitted | 02 Aug 2024 |
| Submitted By | Marcus Osei (DevOps Engineer) |
| Change Type | Standard |
| Environment | Production |
| Description | Increase RDS instance size from db.r6g.xlarge to db.r6g.2xlarge — capacity planning |
| Risk Level | High |
| Rollback Plan | Scale down during maintenance window; estimated 30-minute downtime risk |
| Testing Evidence | Load test completed in staging; throughput validated at 2x current peak |
| CAB Approval | Jake Morrison (VP Engineering) — 06 Aug 2024 |
| Deployed By | Marcus Osei |
| Deployment Date | 10 Aug 2024 03:00 UTC |
| Post-Deploy Verification | DB connections normal; no query latency increase observed |
| Status | Completed |

---

### Ticket CHANGE-2024-0863 (Emergency Change)

| Field | Value |
|---|---|
| Ticket ID | CHANGE-2024-0863 |
| Date Submitted | 13 Aug 2024 18:42 UTC |
| Submitted By | Priya Nair (IT Operations) |
| Change Type | Emergency |
| Environment | Production |
| Description | Disable compromised service account svc-legacy-import — P1 incident response |
| Risk Level | High |
| Risk Justification | Account showing anomalous API calls; potential credential compromise |
| Rollback Plan | Re-enable account if investigation clears; no application dependencies confirmed |
| Emergency Approval | Deepa Venkataraman (CISO) — verbal, documented in ticket |
| Deployed By | Priya Nair |
| Deployment Date | 13 Aug 2024 19:05 UTC |
| Post-Deploy Verification | Anomalous calls ceased; no customer-facing impact confirmed |
| Status | Completed — post-incident review scheduled |

---

## Change Statistics — August 2024

| Change Type | Count | Approved | Rejected | Rolled Back |
|---|---|---|---|---|
| Standard | 38 | 37 | 1 | 0 |
| Emergency | 4 | 4 | 0 | 0 |
| Normal (CAB) | 5 | 5 | 0 | 0 |
| **Total** | **47** | **46** | **1** | **0** |

---

*This document serves as evidence for SOC 2 Type II audit — Control CC8.1*

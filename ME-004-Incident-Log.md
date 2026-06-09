# Mock Evidence Artifact — Incident Log

**Evidence ID:** NCS-CC7-003-IncidentLog-202408-v1  
**Control:** CC7.3 — Security incidents are tracked, investigated, and resolved  
**Period:** Q3 2024 (July 1 — August 31, 2024)  
**Prepared By:** Security Operations  
**Reviewed By:** CISO  
**Classification:** Confidential — Restricted

---

## Incident Summary — Q3 2024

| Severity | Count | Avg Time to Detect | Avg Time to Resolve | SLA Met |
|---|---|---|---|---|
| P1 (Critical) | 1 | 8 minutes | 4.5 hours | Yes (SLA: 8 hours) |
| P2 (High) | 3 | 22 minutes | 11 hours | Yes (SLA: 24 hours) |
| P3 (Medium) | 9 | N/A | 3.2 days | Yes (SLA: 5 days) |
| P4 (Low) | 14 | N/A | 8.1 days | Partial (2 exceeded 14-day SLA) |

---

## Incident Register

| Incident ID | Date | Severity | Title | Detection Source | Root Cause | Status |
|---|---|---|---|---|---|---|
| INC-2024-0234 | 02 Jul 2024 | P3 | Failed login spike from IP 185.220.x.x | GuardDuty | Credential stuffing attempt; blocked by WAF | Closed |
| INC-2024-0251 | 11 Jul 2024 | P2 | Production API latency spike (P95 > 5s) | Datadog alert | Database connection pool exhaustion; misconfigured connection limit | Closed |
| INC-2024-0278 | 22 Jul 2024 | P3 | Phishing email targeting 3 employees | Reported by employee | Spoofed vendor domain; KnowBe4 PAB submission | Closed |
| INC-2024-0291 | 31 Jul 2024 | P1 | Anomalous data exfiltration attempt via svc-legacy-import | GuardDuty + SIEM | Compromised service account credentials | Closed |
| INC-2024-0311 | 13 Aug 2024 | P2 | Unauthorized SSH access attempt to EC2 bastion | AWS CloudTrail | External IP attempting SSH brute force | Closed |
| INC-2024-0328 | 20 Aug 2024 | P2 | Security awareness training phishing simulation — 18 employees clicked | KnowBe4 | Simulated phishing — findings used for targeted training | Closed |

---

## P1 Incident Detail — INC-2024-0291

**Incident Title:** Anomalous data exfiltration attempt via compromised service account  
**Detected:** 31 July 2024, 18:34 UTC  
**Resolved:** 31 July 2024, 23:05 UTC  

**Timeline:**

| Time (UTC) | Event |
|---|---|
| 18:34 | GuardDuty triggers UnauthorizedAccess:IAMUser/InstanceCredentialExfiltration finding |
| 18:42 | SecOps analyst acknowledges alert — begins investigation |
| 18:55 | CISO notified per P1 escalation protocol |
| 19:05 | svc-legacy-import account disabled via emergency change CHANGE-2024-0863 |
| 19:15 | CloudTrail analysis confirms 847MB of S3 data accessed; no customer PII confirmed |
| 20:30 | IR team confirms data accessed = internal log archives; no customer data exfiltrated |
| 23:05 | Incident closed; monitoring enhanced for 7 days |

**Root Cause:** Service account credentials leaked in a developer's GitHub commit in December 2023. Credentials remained active. Threat actor obtained credentials via automated secret scanning tools.

**Corrective Actions:**
- Implemented AWS Secrets Manager for all service account credentials
- Deployed automated git-secrets pre-commit hooks across all repositories
- Conducted retroactive GitHub history scan; 3 additional secrets found and rotated
- Customer notification: Not required (no customer data accessed)

---

*This document serves as evidence for SOC 2 Type II audit — Control CC7.3*

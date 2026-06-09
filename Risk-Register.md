# ISO 27001 Risk Register — NexaCloud Solutions

**Document ID:** NCS-ISMS-RR-2024  
**Version:** 3.0  
**Assessment Date:** 15 September 2024  
**Assessor:** GRC Manager — Kavitha Ramesh  
**Reviewed By:** CISO — Deepa Venkataraman  
**Next Review:** 15 September 2025

---

## Risk Register Summary

| Risk Level | Count |
|---|---|
| Critical (20-25) | 2 |
| High (15-19) | 5 |
| Medium (10-14) | 12 |
| Low (1-9) | 15 |
| **Total** | **34** |

---

## Critical and High Risks

| Risk ID | Title | Asset | Threat | Inherent L | Inherent I | Inherent Score | Treatment | Residual L | Residual I | Residual Score | Owner | Status |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| NCS-RISK-2024-001 | Credential-based compromise of production AWS environment | AWS Production | External attacker exploits stolen or weak credentials to gain admin access to AWS | 4 | 5 | 20 — Critical | Enforce MFA, implement Secrets Manager, privileged session recording | 2 | 5 | 10 — Medium | IT Operations | In Treatment |
| NCS-RISK-2024-002 | Ransomware attack on corporate endpoints | Corporate Endpoints | Ransomware deployed via phishing or drive-by download; encrypts endpoint data | 4 | 5 | 20 — Critical | CrowdStrike EDR, email filtering, security training, immutable S3 backups | 2 | 4 | 8 — Low | IT Operations | Treated |
| NCS-RISK-2024-003 | Unauthorized access to customer SIEM data via privilege escalation | RDS — Customer Data | Insider or external attacker escalates privileges to access other customers' data | 3 | 5 | 15 — High | Row-level security, quarterly access review, GuardDuty alerting | 2 | 5 | 10 — Medium | Engineering | In Treatment |
| NCS-RISK-2024-004 | Third-party supply chain attack via compromised developer tool | GitHub, CI/CD Pipeline | Attacker compromises GitHub Actions dependency or NPM package used in production build | 3 | 5 | 15 — High | Dependency pinning, SAST scanning, software composition analysis (SCA) | 2 | 4 | 8 — Low | Engineering | In Treatment |
| NCS-RISK-2024-005 | Data breach via unpatched vulnerability in production application | EC2 — Application Servers | Attacker exploits known CVE in NGINX, PostgreSQL, or Node.js library before patch applied | 3 | 5 | 15 — High | Weekly vulnerability scans, 30-day patch SLA, WAF, IDS | 2 | 4 | 8 — Low | Security Operations | In Treatment |
| NCS-RISK-2024-006 | AWS availability zone outage causing SLA breach | EC2, RDS — Production | AWS hardware failure or regional event affecting primary AZ | 2 | 5 | 10 — Medium | Multi-AZ RDS, Auto Scaling across AZs, DR in secondary region | 1 | 4 | 4 — Very Low | Engineering | Treated |
| NCS-RISK-2024-007 | Insider threat — intentional data exfiltration by employee | S3 — Log Archives | Disgruntled or financially motivated employee exfiltrates customer or operational data | 2 | 5 | 10 — Medium | DLP monitoring, least privilege, GuardDuty insider threat detection, HR offboarding controls | 2 | 4 | 8 — Low | Security Operations | In Treatment |

---

## Medium Risks (Selected)

| Risk ID | Title | Inherent Score | Residual Score | Owner |
|---|---|---|---|---|
| NCS-RISK-2024-008 | DDoS attack causing platform unavailability | 12 — Medium | 6 — Low | Engineering |
| NCS-RISK-2024-009 | Loss of laptop containing sensitive data | 12 — Medium | 4 — Very Low | IT Operations |
| NCS-RISK-2024-010 | Phishing attack leading to credential theft | 15 — High | 8 — Low | HR / Security |
| NCS-RISK-2024-011 | Misconfigured S3 bucket exposing customer data | 12 — Medium | 6 — Low | Engineering |
| NCS-RISK-2024-012 | Failure to meet PDPB data localisation requirements | 9 — Low | 6 — Low | GRC / Legal |
| NCS-RISK-2024-013 | Third-party vendor data breach (Okta) | 10 — Medium | 8 — Low | GRC |
| NCS-RISK-2024-014 | GitHub source code leaked publicly | 12 — Medium | 4 — Very Low | Engineering |
| NCS-RISK-2024-015 | Inadequate logging — failure to detect breach for 30+ days | 10 — Medium | 4 — Very Low | Security Operations |

---

## Risk Heat Map Reference (5x5 Matrix)

```
Impact
  5 | Low  | Med  | HIGH | CRIT | CRIT
  4 | Low  | Med  | HIGH | HIGH | CRIT
  3 | Low  | Low  | Med  | HIGH | HIGH
  2 | VLow | Low  | Low  | Med  | Med
  1 | VLow | VLow | Low  | Low  | Low
     -----+------+------+------+------
       1      2      3      4      5   Likelihood
```

*Plot each risk using Residual Score position for reporting*

---

*NCS-ISMS-RR-2024 v3.0 — Confidential*

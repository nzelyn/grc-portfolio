# Incident Response Policy

**Document ID:** NCS-POL-003  
**Version:** 3.2  
**Effective Date:** 01 September 2024  
**Review Date:** 01 September 2025  
**Policy Owner:** CISO  
**Approved By:** CEO  
**Classification:** Internal

| Version | Date | Author | Summary |
|---|---|---|---|
| 1.0 | 01 Mar 2022 | GRC Manager | Initial policy |
| 2.0 | 15 Jan 2023 | CISO | Added severity definitions; updated notification timelines |
| 3.0 | 01 Sep 2023 | GRC Manager | Full rewrite post INC-2023-0067 lessons learned |
| 3.2 | 01 Sep 2024 | GRC Manager | Added service account compromise procedures; updated customer notification language |

---

## 1. Purpose

This policy defines NexaCloud Solutions' approach to detecting, classifying, responding to, and recovering from information security incidents. It ensures a consistent, coordinated response that minimizes customer impact and meets regulatory and contractual notification obligations.

---

## 2. Scope

This policy applies to all security incidents affecting systems within the ISMS scope, including:
- Unauthorized access or data breaches
- Malware and ransomware events
- System availability failures (where caused by security events)
- Phishing and social engineering attacks
- Insider threat events
- Third-party vendor security incidents affecting NexaCloud

---

## 3. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| Incident Commander | Leads incident response; typically SecOps Lead or CISO for P1/P2 |
| CISO | Notified for all P1 and P2 incidents; approves customer and regulatory notifications |
| SecOps Analyst | Initial triage, containment, and investigation |
| Engineering | Technical remediation and system recovery |
| Legal / General Counsel | Regulatory notification decisions; evidence preservation guidance |
| HR | Involved in incidents with insider threat component |
| Customer Success | Customer communications and relationship management |
| Any Employee | Report suspected incidents immediately to security@nexacloud.io or Slack #security-alerts |

---

## 4. Incident Severity Classification

| Severity | Criteria | Examples | Initial Response SLA |
|---|---|---|---|
| P1 — Critical | Customer data breach or confirmed exfiltration; sustained availability outage (greater than 1 hour); ransomware with operational impact | Confirmed data breach, ransomware deployment, AWS account takeover | CISO notified within 15 minutes; response team assembled within 30 minutes |
| P2 — High | Suspected data breach (unconfirmed); targeted attack; significant availability degradation | Malware infection, credential stuffing, insider threat confirmed | CISO notified within 1 hour; response team assembled within 2 hours |
| P3 — Medium | Security policy violation; phishing click without credential entry; non-critical system compromise | Phishing simulation click, misconfigured S3 bucket (no data exposed), failed intrusion attempt | SecOps Lead notified; investigation within 4 hours |
| P4 — Low | Policy violation, suspicious activity without confirmed impact, failed attack | Repeated failed logins, anomalous DNS queries, single phishing email | SecOps ticket created; investigation within 1 business day |

---

## 5. Incident Response Phases

### Phase 1 — Identification

- Incidents detected via GuardDuty alerts, Security Hub, Datadog, employee reports, or external notification
- All alerts are triaged within 30 minutes during business hours; on-call rotation covers 24/7 coverage
- Incident ticket opened in Jira (INC project) with initial severity assignment

### Phase 2 — Containment

- Immediate containment actions taken to prevent spread or further damage
- Short-term containment (isolate, block, disable) takes priority over investigation
- Evidence preservation: do not delete or overwrite logs before capturing forensic snapshot
- For P1/P2: CISO notified; decision on customer notification made within 2 hours of containment

### Phase 3 — Eradication

- Root cause identified and confirmed before eradication begins
- Malware removed; unauthorized access revoked; vulnerable systems patched
- Systems verified clean before proceeding to recovery

### Phase 4 — Recovery

- Affected systems restored from known-good state or rebuilt from Infrastructure-as-Code
- Monitoring enhanced on recovered systems for minimum 7 days post-recovery
- Confirmation from system owner that system is functioning normally

### Phase 5 — Post-Incident Review

- Post-incident report completed within 5 business days of incident closure
- Report documents: timeline, root cause, impact, actions taken, lessons learned, preventive actions
- Lessons learned shared with Engineering and SecOps within 10 business days
- Preventive actions tracked as Jira tickets; assigned owners and due dates

---

## 6. Notification Requirements

### Internal Notifications

| Recipient | Trigger | Timeline |
|---|---|---|
| CISO | All P1 and P2 incidents | Within 15-60 minutes (per severity) |
| CEO | P1 incidents involving customer data or reputational risk | Within 1 hour |
| Legal Counsel | Incidents with potential regulatory notification obligation | Within 2 hours |
| Board of Directors | P1 incidents at next scheduled meeting; immediate for data breaches | Within 24 hours |

### Customer Notifications

| Scenario | Timeline |
|---|---|
| Confirmed customer data accessed or exfiltrated | Within 72 hours of confirmation |
| Platform outage impacting customer SLA | Within 1 hour of confirmed impact |
| Suspected but unconfirmed data breach | Notify within 72 hours; update as facts become available |

### Regulatory Notifications

| Regulation | Obligation | Timeline |
|---|---|---|
| India IT Act | Report breach of sensitive personal data | As soon as practicable; legal counsel to advise |
| Customer contracts | Per MSA notification clauses | Typically 72 hours; review individual contracts |

---

## 7. Evidence Handling

- All incident evidence (logs, screenshots, forensic images) must be preserved and stored in the designated secure evidence folder (SharePoint — Incident Evidence — restricted access)
- Chain of custody must be maintained for evidence that may be used in legal proceedings
- Do not discuss incident details in unsecured channels (personal email, personal Slack, SMS)

---

## 8. Exceptions

No exceptions to incident reporting requirements are permitted. All suspected incidents must be reported.

---

## 9. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| CISO | Deepa Venkataraman | [Signed] | 01 Sep 2024 |
| CEO | Rohan Mehta | [Signed] | 05 Sep 2024 |

**Framework Alignment:** SOC 2 CC7.3, CC7.4, CC7.5 | ISO 27001:2022 Annex A 5.24-5.28

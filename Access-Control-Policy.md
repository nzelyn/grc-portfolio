# Access Control Policy

**Document ID:** NCS-POL-001  
**Version:** 3.1  
**Effective Date:** 01 September 2024  
**Review Date:** 01 September 2025  
**Policy Owner:** CISO  
**Approved By:** CEO  
**Classification:** Internal

| Version | Date | Author | Summary of Changes |
|---|---|---|---|
| 1.0 | 01 Mar 2022 | GRC Manager | Initial policy |
| 2.0 | 15 Jan 2023 | GRC Manager | Added MFA requirements; updated provisioning workflow |
| 3.0 | 01 Sep 2023 | CISO | Aligned to ISO 27001:2022; added privileged access section |
| 3.1 | 01 Sep 2024 | GRC Manager | Added service account controls; updated exception process |

---

## 1. Purpose

This policy establishes the principles and requirements for managing access to NexaCloud Solutions' information systems, data, and physical facilities. Its goal is to ensure that access is granted based on business need, follows least-privilege principles, and is regularly reviewed.

---

## 2. Scope

This policy applies to:
- All NexaCloud employees, contractors, and temporary staff
- All information systems within the ISMS scope
- Service accounts and automated system identities
- Third-party vendor access to NexaCloud systems

---

## 3. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| CISO | Policy owner; final authority on access exceptions; approves privileged access requests |
| IT Operations Manager | Access provisioning and deprovisioning; quarterly access reviews |
| Hiring Manager | Initiates access request for new hires; approves access scope |
| ISMS Manager (GRC) | Policy compliance monitoring; exception tracking |
| All Employees | Comply with access policies; report unauthorized access immediately |

---

## 4. Policy Statements

### 4.1 Access Provisioning

- All access requests must be submitted via the IT Service Desk (Jira) with business justification and manager approval before provisioning
- Access must follow the principle of least privilege — grant only the minimum access required for the job function
- Privileged access (admin, root, superuser) requires CISO approval in addition to manager approval
- Access must be provisioned using NexaCloud's identity provider (Okta); direct account creation on individual systems is prohibited except for documented service accounts

### 4.2 Authentication

- Multi-factor authentication (MFA) is mandatory for all user accounts accessing NexaCloud systems, including corporate tools, production infrastructure, and developer systems
- Service accounts that cannot use MFA must have a formally documented exception, approved by the CISO, with compensating controls (IP restriction, secret rotation, anomaly alerting)
- Passwords must meet the minimum complexity requirements defined in the Authentication Standard (NCS-STD-003)
- Shared accounts are prohibited; each individual must have a unique, personally identifiable account

### 4.3 Access Reviews

- Privileged access is reviewed quarterly by IT Operations; review evidence is retained for 12 months
- General user access is reviewed annually at minimum, or following any organizational change
- Access review findings are tracked in Jira; accounts identified for revocation must be disabled within 3 business days
- Access reviews are documented and approved by the CISO

### 4.4 Access Deprovisioning

- All system access must be revoked within 24 hours of employment termination or role change
- IT Operations receives termination notification from HR via automated workflow (Rippling to Okta)
- Manager responsible for confirming that all physical assets (laptop, badge, access cards) are returned on the last day of employment
- For voluntary departures, access is revoked at 17:00 local time on the final day of employment; for involuntary departures, access is revoked immediately at the time of notification

### 4.5 Privileged Access Management

- Privileged accounts must not be used for routine tasks; engineers must use standard accounts for daily work and elevate only when required
- Production database direct access is restricted to an approved list of individuals; all production database sessions are logged
- Root account usage on AWS must be documented in a Jira ticket and reviewed within 24 hours by the CISO
- All privileged sessions on production systems must be conducted via the approved bastion/jump host; direct SSH or RDP is prohibited

### 4.6 Third-Party Access

- Vendor access to NexaCloud systems must be requested through the Vendor Access Request form
- Vendor accounts must be provisioned as individual named accounts — no shared vendor credentials
- Vendor access must be time-limited (maximum 90 days) and renewed only with documented business justification
- All vendor remote access must use VPN or secure remote access solution; vendor access logs are reviewed monthly

---

## 5. Exceptions

Exceptions to this policy require written approval from the CISO. Exceptions must include:
- Business justification
- Risk assessment
- Compensating controls
- Expiry date (maximum 6 months; renewable with re-approval)

Exceptions are tracked in the Exception Register (NCS-GRC-EXCEP).

---

## 6. Enforcement

Violations of this policy may result in:
- Immediate access revocation
- Disciplinary action up to and including termination of employment
- Legal action where applicable

---

## 7. Related Documents

- NCS-STD-003 — Authentication Standard
- NCS-POL-005 — Vendor Risk Management Policy
- NCS-PROC-IT-001 — Access Provisioning Procedure

---

## 8. Approval

| Role | Name | Signature | Date |
|---|---|---|---|
| CISO | Deepa Venkataraman | [Signed] | 01 Sep 2024 |
| CEO | Rohan Mehta | [Signed] | 05 Sep 2024 |

---

**Framework Alignment:**

| Requirement | Reference |
|---|---|
| SOC 2 | CC6.1, CC6.2, CC6.3, CC6.4 |
| ISO 27001:2022 | Annex A 5.15, 5.16, 5.17, 5.18, 8.2, 8.3, 8.5 |

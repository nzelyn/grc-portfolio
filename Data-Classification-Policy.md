# Data Classification Policy

**Document ID:** NCS-POL-004  
**Version:** 2.0  
**Effective Date:** 01 September 2024  
**Review Date:** 01 September 2025  
**Policy Owner:** CISO  
**Approved By:** CEO  
**Classification:** Internal

---

## 1. Purpose

This policy establishes how NexaCloud Solutions classifies, handles, and protects information assets based on their sensitivity and value.

---

## 2. Classification Levels

| Level | Description | Examples | Handling Requirements |
|---|---|---|---|
| Restricted | Highest sensitivity; access strictly limited to named individuals | Customer SIEM event data, encryption keys, board minutes, employee PII, customer contracts | Encrypted at rest and in transit; access logged; no sharing outside named list; deleted per retention policy |
| Confidential | Sensitive business or technical information | Source code, risk register, audit reports, security policies, incident reports, financial forecasts | Encrypted in transit; access restricted by role; not shared externally without NDA |
| Internal | General internal information; not for public release | Operational procedures, internal project documentation, team wikis | Not shared externally; standard access controls apply |
| Public | Approved for external distribution | Marketing materials, product documentation, public website content, job postings | No special handling required |

---

## 3. Data Handling Requirements by Classification

### Restricted

- **Storage:** Encrypted at rest using AES-256 via AWS KMS; customer data must remain within contracted AWS regions
- **Transmission:** TLS 1.2 or higher for all network transmission; no transmission via unencrypted channels
- **Access:** Named individuals only; access logged and reviewed quarterly
- **Sharing:** No external sharing without CISO approval and NDA
- **Retention:** Per customer contract; minimum 12 months, maximum 36 months unless legally required otherwise
- **Disposal:** Cryptographic erasure (key deletion) for cloud storage; certified destruction for physical media

### Confidential

- **Storage:** Encrypted at rest; stored in approved systems only (SharePoint, Confluence, designated S3 buckets)
- **Transmission:** TLS 1.2 or higher; password-protected attachments for email if necessary
- **Access:** Role-based; access reviewed annually
- **Sharing:** External sharing requires NDA and CISO approval
- **Retention:** 7 years for financial and legal documents; 3 years for security documentation unless specified otherwise

### Internal

- **Storage:** Approved internal systems only; no personal cloud storage
- **Transmission:** Standard corporate channels (Google Workspace, Slack, email)
- **Access:** All employees with need to know
- **Sharing:** Not to be shared externally without manager approval
- **Retention:** Per business unit guidelines; minimum 1 year

---

## 4. Special Data Categories

The following data types require Restricted classification regardless of other factors:

| Data Type | Examples | Additional Controls |
|---|---|---|
| Personally Identifiable Information (PII) | Names, email addresses, national IDs of customers or employees | Data minimization; purpose limitation; deletion on request |
| Payment Card Data (PCI) | Credit card numbers, CVV | PCI DSS controls apply; do not store unless essential |
| Health Information | Employee medical records | Access restricted to HR and individual only |
| Authentication Credentials | Passwords, API keys, private certificates | Never stored in plaintext; managed via Secrets Manager |
| Legal Privileged Communications | Attorney-client communications | Legal hold if litigation is pending |

---

## 5. Data Labelling

- All formal documents must include a classification label in the document header or footer
- Source code repositories must include a classification notice in the repository README
- Email containing Restricted or Confidential information should include the classification in the subject line
- Automated labelling via DLP tools is the preferred enforcement mechanism; manual labelling is required where automation is not available

---

## 6. Data Retention and Disposal

| Data Category | Retention Period | Disposal Method |
|---|---|---|
| Customer SIEM event data | Per contract (default 36 months) | Cryptographic erasure |
| Employee HR records | Duration of employment + 7 years | Secure deletion from HR system |
| Security incident records | 3 years | Secure deletion |
| Financial records | 7 years | Secure deletion |
| Audit evidence | 3 years | Secure deletion |
| Source code | Indefinite (active products) | N/A |

---

## 7. Approval

| Role | Name | Date |
|---|---|---|
| CISO | Deepa Venkataraman | 01 Sep 2024 |
| CEO | Rohan Mehta | 05 Sep 2024 |

**Framework Alignment:** SOC 2 C1.1, C1.2 | ISO 27001:2022 Annex A 5.12, 5.13, 8.10, 8.11

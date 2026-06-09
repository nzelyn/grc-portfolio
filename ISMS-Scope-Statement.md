# ISMS Scope Statement — NexaCloud Solutions

**Document ID:** NCS-ISMS-SCOPE-001  
**Version:** 1.2  
**Effective Date:** 01 September 2024  
**Review Date:** 01 September 2025  
**Document Owner:** CISO  
**Approved By:** CEO  
**Reference Standard:** ISO/IEC 27001:2022 Clause 4.3

---

## 1. Purpose

This document defines the boundaries of NexaCloud Solutions' Information Security Management System (ISMS). It identifies the systems, processes, locations, and organizational units within scope.

---

## 2. Organization Context

### 2.1 Internal Factors

| Factor | Description |
|---|---|
| Company size | 250 employees across two locations |
| Business model | SaaS subscription (B2B) |
| Development model | Continuous delivery via DevOps on AWS |
| Risk appetite | Low — customer data protection is a core commercial commitment |
| Security maturity | Developing to Managed (Maturity Level 3) |

### 2.2 External Factors

| Factor | Description |
|---|---|
| Regulatory environment | India IT Act 2000/2008; PDPB (pending); US state privacy laws |
| Customer contractual obligations | SOC 2 Type II required by enterprise customers |
| Competitive landscape | ISO 27001 certification expected by top-tier enterprise prospects |
| Threat environment | Cloud-hosted SaaS — high threat exposure from web attacks, credential theft |

### 2.3 Interested Parties

| Party | Information Security Interest |
|---|---|
| Enterprise customers | Assurance of data confidentiality and platform availability |
| Investors | Risk management governance and compliance posture |
| Employees | Clear security policies and training |
| Regulators | Compliance with applicable data protection laws |
| Certification body | Evidence of ISO 27001:2022 conformance |

---

## 3. ISMS Scope Definition

### 3.1 In-Scope Statement

The ISMS applies to:

**Systems and Services:**
- NexaCloud SIEM Platform (production environment — nexacloud.io)
- AWS production environments: ap-south-1 (Bangalore) and us-east-1 (Virginia)
- All services supporting the platform: EC2, RDS, S3, CloudFront, WAF, GuardDuty, CloudTrail, KMS, IAM, Security Hub, AWS Config
- Corporate identity and access systems: Okta, GitHub Enterprise
- Continuous compliance monitoring: Vanta

**Business Processes:**
- Software development and deployment
- Customer onboarding and data ingestion
- Security operations and incident response
- Vendor and third-party risk management
- Change management

**Locations:**
- Bangalore, India (180 employees) — primary engineering and operations
- Austin, Texas, USA (70 employees) — sales, customer success, and leadership

**Organizational Units:**
- Engineering (95 employees)
- Security Operations (12 employees)
- GRC (6 employees)
- IT Operations (8 employees)
- HR (15 employees)
- Finance (10 employees)

### 3.2 Out-of-Scope Justification

| Item | Exclusion Reason |
|---|---|
| Development and staging environments | Isolated from production; no customer data stored; lower risk |
| Customer-managed infrastructure | Outside NexaCloud's direct control; governed by CUECs |
| NexaCloud marketing website (nexacloud.com) | Static CMS site; no customer data or platform access |
| Physical office security | AWS manages all data centre physical security; offices covered by CUEC |

---

## 4. ISMS Objectives

Per ISO 27001:2022 Clause 6.2, NexaCloud has established the following security objectives for the current ISMS period:

| Objective | Measure | Target | Review Frequency |
|---|---|---|---|
| Reduce mean time to detect incidents | MTTD (minutes) | Less than 30 minutes | Monthly |
| Maintain platform availability | Uptime % | Greater than or equal to 99.9% | Monthly |
| Complete security training for all staff | Training completion % | Greater than or equal to 95% | Quarterly |
| Remediate critical vulnerabilities within SLA | Patch compliance % | 100% within 30 days | Monthly |
| No critical audit findings at certification | Audit findings | 0 critical (major nonconformities) | Annual |

---

## 5. Document Control and Approval

| Version | Date | Author | Change |
|---|---|---|---|
| 1.0 | 01 Mar 2023 | GRC Manager | Initial scope document |
| 1.1 | 15 Sep 2023 | GRC Manager | Added Austin office; updated tooling |
| 1.2 | 01 Sep 2024 | CISO | Pre-certification review; updated objectives |

**Approved By:**

| Role | Name | Date |
|---|---|---|
| CISO | Deepa Venkataraman | 01 Sep 2024 |
| CEO | Rohan Mehta | 05 Sep 2024 |

---

*NCS-ISMS-SCOPE-001 v1.2 — ISO 27001:2022 Clause 4.3*

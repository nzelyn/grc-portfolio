# System Description — NexaCloud Solutions

**Document ID:** NCS-SOC2-SD-001  
**Version:** 2.1  
**Effective Date:** 01 July 2024  
**Review Date:** 01 July 2025  
**Document Owner:** Chief Information Security Officer  
**Approved By:** Chief Executive Officer  
**Classification:** Confidential

---

## Document Control

| Version | Date | Author | Change Summary |
|---|---|---|---|
| 1.0 | 15 Jan 2023 | GRC Manager | Initial draft |
| 1.5 | 03 Jun 2023 | GRC Manager | Updated infrastructure post AWS migration |
| 2.0 | 12 Jan 2024 | CISO | Annual review — added Privacy criteria |
| 2.1 | 01 Jul 2024 | GRC Manager | Pre-audit update — revised availability commitments |

---

## 1. Overview of NexaCloud Solutions

NexaCloud Solutions provides cloud-based security information and event management (SIEM) software delivered as a SaaS platform. Customers use the NexaCloud platform to aggregate, correlate, and respond to security events across their IT environments.

**Primary Service:** NexaCloud SIEM Platform (nexacloud.io)  
**Customer Base:** Mid-market and enterprise companies in financial services, healthcare, and technology  
**Employees:** 250 (Bangalore: 180, Austin: 70)  
**Fiscal Year:** January 1 — December 31

---

## 2. Principal Service Commitments

| Commitment | Target | Measurement Period |
|---|---|---|
| Platform Availability | 99.9% uptime | Monthly |
| Incident Response (P1) | Initial response within 1 hour | Per incident |
| Incident Response (P2) | Initial response within 4 hours | Per incident |
| Data Processing Latency | Events processed within 60 seconds | 95th percentile, daily |
| Scheduled Maintenance Window | Saturdays 02:00–06:00 UTC | Monthly |
| Data Retention | 12 months hot, 36 months cold | Per contract |

---

## 3. System Components

### 3.1 Infrastructure

NexaCloud operates entirely on Amazon Web Services (AWS). No on-premises infrastructure exists.

| AWS Service | Purpose | Region |
|---|---|---|
| EC2 (Auto Scaling Groups) | Application compute | ap-south-1, us-east-1 |
| RDS (PostgreSQL, Multi-AZ) | Customer data storage | ap-south-1, us-east-1 |
| S3 | Log archive, cold storage | ap-south-1, us-east-1 |
| CloudFront | CDN for web application | Global |
| WAF | Web application firewall | Global |
| GuardDuty | Threat detection | ap-south-1, us-east-1 |
| CloudTrail | Audit logging | All regions |
| KMS | Encryption key management | ap-south-1, us-east-1 |
| VPC | Network isolation | ap-south-1, us-east-1 |
| IAM | Identity and access management | Global |
| AWS Config | Configuration compliance | ap-south-1, us-east-1 |
| Security Hub | Centralized security findings | ap-south-1, us-east-1 |

### 3.2 Applications and Tools

| Component | Description | Owner |
|---|---|---|
| NexaCloud Web App | React/Node.js customer portal | Engineering |
| NexaCloud API Gateway | REST API layer | Engineering |
| Event Processing Engine | Python-based event correlation | Engineering |
| Jira (Atlassian Cloud) | Change management and ticketing | IT Operations |
| GitHub Enterprise | Source code management | Engineering |
| Okta | Identity provider and SSO | IT Operations |
| Datadog | Application performance monitoring | Engineering |
| Vanta | Continuous compliance monitoring | GRC |

### 3.3 Personnel in Scope

| Role | Responsibility |
|---|---|
| Engineering (95) | Development, deployment, incident response |
| Security Operations (12) | Threat monitoring, vulnerability management |
| GRC Team (6) | Compliance, policy, audit management |
| IT Operations (8) | Endpoint, vendor tools |
| HR (15) | Policy enforcement, onboarding |

---

## 4. System Boundaries

### In Scope
- NexaCloud SIEM Platform (production environment)
- AWS infrastructure in ap-south-1 and us-east-1
- Corporate identity and access systems (Okta, AWS IAM)
- Source code management (GitHub Enterprise)
- Internal monitoring systems (Datadog, GuardDuty)

### Out of Scope
- Customer internal networks and endpoints
- Third-party integrations built by customers
- Development and staging environments
- Internal productivity tools (Google Workspace, Slack)

---

## 5. Control Environment

### 5.1 Risk Assessment Process
NexaCloud performs a formal risk assessment annually and following any material change. Risk assessments use a 5x5 likelihood-impact matrix. Residual scores of 12 or above require CISO sign-off and Board notification.

### 5.2 Monitoring Cadence
- **Continuous:** AWS Security Hub, GuardDuty, Vanta, Datadog
- **Weekly:** Vulnerability scan review, access anomaly review
- **Monthly:** Privileged access review, patch status review
- **Quarterly:** SOC 2 evidence collection, vendor risk review
- **Annual:** Penetration test, full risk assessment, policy review

---

## 6. Complementary User Entity Controls (CUECs)

1. Customers must use strong, unique credentials when accessing the NexaCloud portal
2. Customers are responsible for managing their own user accounts within the platform
3. Customers must promptly notify NexaCloud of any suspected unauthorized access
4. Customers are responsible for accuracy of data submitted to the platform
5. Customers must review and retain NexaCloud-generated compliance reports

---

## 7. Subservice Organizations

| Vendor | Service | SOC Report |
|---|---|---|
| Amazon Web Services | Cloud infrastructure (IaaS) | SOC 2 Type II |
| Okta | Identity and access management | SOC 2 Type II |
| Atlassian (Jira) | Change management ticketing | SOC 2 Type II |
| GitHub (Microsoft) | Source code management | SOC 2 Type II |
| Datadog | Application monitoring | SOC 2 Type II |

---

*End of System Description — NCS-SOC2-SD-001 v2.1*

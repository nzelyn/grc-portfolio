# Cybersecurity Risk Register — NexaCloud Solutions

**Document ID:** NCS-GRC-RR-2024  
**Version:** 4.1  
**Period:** FY2024  
**Owner:** GRC Manager  
**Reviewed:** 15 September 2024

---

## Scoring Methodology

Risk Score = Likelihood (1-5) x Impact (1-5)  
Critical: 20-25 | High: 15-19 | Medium: 10-14 | Low: 5-9 | Very Low: 1-4

---

## Risk Register

| Risk ID | Risk Title | Category | NIST CSF Function | Asset | Threat | Vulnerability | Inherent L | Inherent I | Inherent Score | Current Controls | Treatment | Residual L | Residual I | Residual Score | Risk Level | Owner | Status |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| RR-001 | Credential-based AWS admin compromise | Access Control | Protect | AWS IAM | Attacker exploits stolen credentials | MFA not enforced on service accounts | 4 | 5 | 20 | Okta MFA for users; GuardDuty | Mitigate | 2 | 5 | 10 | Medium | IT Ops | In Treatment |
| RR-002 | Ransomware on corporate endpoints | Malware | Protect/Respond | Endpoints | Phishing-delivered ransomware | Reliance on user behaviour | 4 | 5 | 20 | CrowdStrike, email filtering, backups | Mitigate | 2 | 4 | 8 | Low | IT Ops | Treated |
| RR-003 | Customer data breach via privilege escalation | Data Protection | Protect | RDS — customer data | Insider or attacker escalates DB privileges | Row-level security not tested | 3 | 5 | 15 | Row-level security, access review | Mitigate | 2 | 5 | 10 | Medium | Engineering | In Treatment |
| RR-004 | Supply chain compromise via CI/CD dependency | Supply Chain | Protect | GitHub/CI-CD | Attacker poisons NPM package or GitHub Action | Dependency pinning not enforced | 3 | 5 | 15 | SAST, manual reviews | Mitigate | 2 | 4 | 8 | Low | Engineering | In Treatment |
| RR-005 | Unpatched vulnerability exploited in production | Vulnerability Mgmt | Protect | EC2/RDS | Attacker exploits known CVE | Patch SLA compliance below 100% | 3 | 5 | 15 | Weekly scans, WAF, IDS | Mitigate | 2 | 4 | 8 | Low | SecOps | In Treatment |
| RR-006 | DDoS attack on platform | Availability | Protect/Respond | CloudFront/EC2 | Volumetric or application DDoS | CDN capacity limits | 3 | 4 | 12 | CloudFront, AWS Shield Standard, WAF | Mitigate | 2 | 3 | 6 | Low | Engineering | Treated |
| RR-007 | Insider data exfiltration | Insider Threat | Detect/Protect | S3, RDS | Disgruntled employee exfiltrates data | Limited DLP enforcement | 2 | 5 | 10 | GuardDuty, least privilege, logging | Mitigate | 2 | 4 | 8 | Low | SecOps | In Treatment |
| RR-008 | Phishing leading to credential theft | Social Engineering | Protect | Okta (credentials) | Targeted spear-phishing email | Users clicking malicious links | 4 | 4 | 16 | MFA, email filtering, training | Mitigate | 2 | 3 | 6 | Low | HR/SecOps | Treated |
| RR-009 | Misconfigured S3 bucket exposing data | Cloud Misconfiguration | Identify/Protect | S3 | Public access to sensitive bucket | Manual bucket creation bypassing IaC | 3 | 4 | 12 | AWS Config rules, Vanta alerts | Mitigate | 2 | 3 | 6 | Low | Engineering | Treated |
| RR-010 | Loss of encrypted laptop | Physical Security | Protect | Corporate laptop | Lost or stolen laptop | Remote work increases exposure | 3 | 3 | 9 | Full disk encryption, MDM remote wipe | Mitigate | 1 | 2 | 2 | Very Low | IT Ops | Treated |
| RR-011 | AWS availability zone failure | Cloud Availability | Recover | EC2/RDS | AWS infrastructure failure | Single-AZ dependency (if present) | 2 | 5 | 10 | Multi-AZ RDS, Auto Scaling, DR region | Mitigate | 1 | 4 | 4 | Very Low | Engineering | Treated |
| RR-012 | Regulatory non-compliance (PDPB/data localisation) | Compliance | Identify | Customer PII | Indian data localisation requirements | Regulations not yet finalized | 3 | 3 | 9 | Legal counsel monitoring; DPA in place | Monitor | 2 | 3 | 6 | Low | GRC/Legal | Monitoring |
| RR-013 | GitHub source code repository leaked | Intellectual Property | Protect | Source code (GitHub) | Secret scanning or accidental public repo | Developer error | 2 | 4 | 8 | Private repos, branch protection, secret scanning | Mitigate | 1 | 3 | 3 | Very Low | Engineering | Treated |
| RR-014 | Inadequate logging — delayed breach detection | Detection | Detect | CloudTrail/SIEM | Attacker operates undetected | Alert coverage gaps | 2 | 5 | 10 | CloudTrail, GuardDuty, Security Hub, Datadog | Mitigate | 1 | 4 | 4 | Very Low | SecOps | Treated |
| RR-015 | Third-party vendor breach (e.g. Okta) | Third-Party Risk | Protect | Okta identity | Vendor compromise affecting NexaCloud | Dependency on vendor security | 2 | 5 | 10 | Annual SOC 2 review, backup auth plan | Transfer/Accept | 2 | 4 | 8 | Low | GRC | Monitored |

---

## Risk Summary

| Level | Inherent Count | Residual Count | Change |
|---|---|---|---|
| Critical (20-25) | 2 | 0 | -2 |
| High (15-19) | 3 | 0 | -3 |
| Medium (10-14) | 6 | 2 | -4 |
| Low (5-9) | 3 | 8 | +5 |
| Very Low (1-4) | 1 | 5 | +4 |

---

## Key Risk Indicators (KRIs)

| KRI | Metric | Current Value | Threshold | Status |
|---|---|---|---|---|
| KRI-001 | Percentage of accounts without MFA | 3.2% (8 service accounts) | Less than 1% | At Risk |
| KRI-002 | Critical/High vulnerabilities open beyond SLA | 0 | 0 | On Target |
| KRI-003 | Security awareness training completion | 85% | 95% | Below Target |
| KRI-004 | Mean time to detect incidents (minutes) | 22 | Less than 30 | On Target |
| KRI-005 | Vendor assessments current (Tier 1/2) | 71% (5 of 7) | 100% | At Risk |
| KRI-006 | Open high-severity CAPA items | 2 | 0 | At Risk |

---

*NCS-GRC-RR-2024 v4.1*

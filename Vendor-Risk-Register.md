# Vendor Risk Register — NexaCloud Solutions

**Document ID:** NCS-GRC-VRR-2024  
**Version:** 1.0  
**Assessment Cycle:** FY2024  
**Owner:** GRC Manager

---

## Vendor Risk Register

| Vendor | Service | Tier | Score (%) | Risk Level | Last Assessment | Next Assessment | Open Issues | SOC 2 | Status |
|---|---|---|---|---|---|---|---|---|---|
| Amazon Web Services | Cloud infrastructure (IaaS) | 1 | 96% | Low | Aug 2024 | Aug 2025 | 0 | SOC 2 Type II (Annual) | Approved |
| Okta | Identity and access management | 1 | 91% | Low | Aug 2024 | Aug 2025 | 0 | SOC 2 Type II (Semi-annual) | Approved |
| GitHub (Microsoft) | Source code management | 1 | 93% | Low | Aug 2024 | Aug 2025 | 0 | SOC 2 Type II (Annual) | Approved |
| Atlassian (Jira/Confluence) | Project management | 2 | 87% | Low | Aug 2024 | Aug 2025 | 1 (minor) | SOC 2 Type II (Annual) | Approved — monitor |
| Datadog | Monitoring and observability | 2 | 90% | Low | Aug 2024 | Aug 2025 | 0 | SOC 2 Type II (Semi-annual) | Approved |
| CloudFlare | DDoS protection and CDN | 1 | 78% | Medium | Oct 2024 | Oct 2025 | 2 | SOC 2 Type II | Approved — remediation required |
| SendGrid (Twilio) | Transactional email | 2 | 72% | Medium | Oct 2024 | Oct 2025 | 3 | SOC 2 Type II | Conditionally approved |
| PagerDuty | On-call alerting | 2 | 85% | Low | Oct 2024 | Oct 2025 | 0 | SOC 2 Type II | Approved |

---

## Open Issues by Vendor

### CloudFlare — 2 Open Issues

| Issue # | Domain | Description | Severity | Required By |
|---|---|---|---|---|
| CF-2024-001 | Incident Response | Vendor notification SLA not contractually documented as 24 hours; current contract says "prompt notification" | Medium | Contract renewal (Dec 2024) |
| CF-2024-002 | Vulnerability Management | Penetration test summary not provided; only summary statement available | Low | Oct 2025 (next assessment) |

### SendGrid — 3 Open Issues

| Issue # | Domain | Description | Severity | Required By |
|---|---|---|---|---|
| SG-2024-001 | Data Protection | DPA not yet signed; standard terms do not include GDPR/PDPB compliant data processing language | High | 30 Nov 2024 |
| SG-2024-002 | Access Control | MFA not enforced for all SendGrid admin accounts per questionnaire response | Medium | 31 Jan 2025 |
| SG-2024-003 | Compliance | No penetration test evidence provided | Low | Next assessment |

---

## Vendor Risk Trend

| Quarter | Low | Medium | High | Critical |
|---|---|---|---|---|
| Q1 2024 | 3 | 0 | 0 | 0 |
| Q2 2024 | 3 | 0 | 0 | 0 |
| Q3 2024 (expanded program) | 5 | 0 | 0 | 0 |
| Q4 2024 (target) | 6 | 2 | 0 | 0 |

---

*NCS-GRC-VRR-2024 v1.0*

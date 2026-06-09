# Risk Assessment Methodology — NexaCloud Solutions ISMS

**Document ID:** NCS-ISMS-RAM-001  
**Version:** 1.1  
**Effective Date:** 01 September 2024  
**Reference Standard:** ISO/IEC 27001:2022 Clause 6.1  
**Document Owner:** GRC Manager

---

## 1. Purpose

This document defines the methodology NexaCloud uses to identify, analyze, and evaluate information security risks across its ISMS scope.

---

## 2. Risk Criteria

### 2.1 Likelihood Scale

| Score | Level | Definition |
|---|---|---|
| 1 | Very Low | Threat event is unlikely in a 12-month period; no historical precedent |
| 2 | Low | Threat event occurs less than once per year in comparable organizations |
| 3 | Medium | Threat event occurs 1-3 times per year in comparable organizations |
| 4 | High | Threat event likely to occur at least once within 12 months |
| 5 | Very High | Threat event expected to occur multiple times within 12 months |

### 2.2 Impact Scale

| Score | Level | Definition |
|---|---|---|
| 1 | Very Low | Negligible impact on operations, reputation, or customers |
| 2 | Low | Minor disruption; no customer impact; resolved within hours |
| 3 | Medium | Moderate disruption; limited customer impact; resolved within 1-2 days |
| 4 | High | Significant disruption; customer impact; reputational damage; regulatory exposure |
| 5 | Very High | Severe disruption; major data breach; regulatory action; existential reputational risk |

### 2.3 Risk Score Formula

```
Risk Score = Likelihood Score x Impact Score
```

### 2.4 Risk Acceptance Thresholds

| Score Range | Risk Level | Action Required |
|---|---|---|
| 20-25 | Critical | Immediate treatment required; CISO and CEO notification; Board reporting |
| 15-19 | High | Treatment required within 30 days; CISO approval of treatment plan |
| 10-14 | Medium | Treatment required within 90 days; GRC Manager oversight |
| 5-9 | Low | Treatment within 6 months; monitor quarterly |
| 1-4 | Very Low | Accept and monitor annually |

---

## 3. Risk Treatment Options

| Option | Definition |
|---|---|
| Mitigate | Apply controls to reduce likelihood or impact |
| Accept | Formally accept residual risk; document business justification |
| Transfer | Shift risk to third party (insurance, vendor contract) |
| Avoid | Eliminate the activity or asset generating the risk |

---

## 4. Risk Register Structure

Each risk entry contains:
- Risk ID (NCS-RISK-YYYY-NNN)
- Risk Title
- Asset affected
- Threat description
- Vulnerability description
- Current controls
- Inherent likelihood and impact scores
- Inherent risk score and level
- Treatment option and planned controls
- Risk owner
- Treatment deadline
- Residual likelihood and impact scores
- Residual risk score and level
- Risk acceptance status

---

## 5. Risk Assessment Schedule

| Activity | Frequency | Trigger |
|---|---|---|
| Full risk assessment | Annual | Fixed schedule (September each year) |
| Partial assessment | Ad hoc | Material change to ISMS scope, infrastructure, or threat landscape |
| Risk register review | Quarterly | Management Review agenda item |
| Individual risk review | Per treatment deadline | Risk owner responsibility |

---

*NCS-ISMS-RAM-001 v1.1*

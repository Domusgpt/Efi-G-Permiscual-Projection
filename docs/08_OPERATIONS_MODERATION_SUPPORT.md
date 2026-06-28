# 08 — Operations, Monitoring, and Support

## Operating principle

Efi-G handles sensitive identity workflows. Operational maturity is part of the product. A weak support desk or unclear review process can destroy trust faster than a weak model.

## Core roles

| Role | Responsibility |
|---|---|
| Founder/Product Lead | roadmap, policy, creator strategy, business model |
| Engineering Lead | architecture, security, deployment, platform reliability |
| ML Lead | model selection, tuning, evaluation, inference cost |
| Trust and Safety Lead | policy, review queues, escalations, reporting |
| Creator Success | onboarding, storefront setup, creator education |
| Support Agent | account help, billing help, basic reporting triage |
| Compliance Counsel | terms, regulatory review, payment and privacy guidance |
| Finance/Ops | payouts, reserves, chargebacks, tax reports |

## Review queues

### Queue A — account and verification

- identity mismatch;
- suspected duplicate account;
- creator onboarding review;
- payout risk;
- age-state uncertainty.

### Queue B — avatar and rights

- avatar source dispute;
- unclear license claim;
- revocation request;
- creator scope issue;
- marketplace listing review.

### Queue C — generation jobs

- blocked prompt appeal;
- output flagged by scanner;
- customer report;
- creator report;
- model failure investigation.

### Queue D — payment and risk

- chargeback;
- refund;
- suspicious spend;
- payout hold;
- processor warning.

## SLA draft

| Case type | Initial response | Target resolution |
|---|---:|---:|
| Safety removal request | 12 hours | 48 hours |
| Payment support | 24 hours | 3 business days |
| Creator onboarding | 3 business days | 7 business days |
| General support | 48 hours | 5 business days |
| Data deletion request | 7 days | 30 days unless law requires otherwise |

## Monitoring metrics

### Product

- signups;
- activation rate;
- first-generation completion;
- average outputs per user;
- credit conversion;
- creator applications;
- marketplace GMV when launched.

### Infrastructure

- API latency;
- job queue depth;
- GPU utilization;
- generation latency;
- failure rate;
- storage errors;
- policy worker uptime.

### Trust and safety

- block rate;
- review rate;
- false positive rate;
- report volume;
- time to removal;
- repeat offender rate;
- creator dispute volume.

### Financial risk

- refund rate;
- chargeback rate;
- processor reserve;
- payout holds;
- failed payments;
- margin per model tier.

## Incident levels

### Sev 1

Data leak, platform-wide policy bypass, payment processor suspension, severe rights failure, or production outage.

### Sev 2

Large review backlog, queue outage, creator payout delay, model misrouting, or repeated generation failure.

### Sev 3

Single-user account issue, low-volume bug, isolated failed job, or support SLA delay.

## Required internal tools

- Admin dashboard.
- Review case system.
- Audit search.
- User impersonation controls for support with strict logging.
- Avatar pause button.
- Marketplace listing pause button.
- Payment risk dashboard.
- Model cost dashboard.
- Deletion lifecycle dashboard.

## Support tone

Support should be privacy-protective, direct, and nonjudgmental. Users and creators are trusting the platform with identity-linked creative assets. Every support interaction should reinforce control, safety, and discretion.

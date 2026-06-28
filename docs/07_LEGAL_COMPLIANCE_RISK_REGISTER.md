# 07 — Legal Compliance Risk Register

This document is a product and engineering risk register, not legal advice. Counsel must review before launch.

## Core legal posture

Efi-G must be built as a permissioned identity-media platform. The company should be able to show that real-person likeness use is based on documented authorization, scoped license terms, revocation mechanics, and responsive removal workflows.

## High-priority risk areas

| Area | Risk | Product response |
|---|---|---|
| Likeness rights | Unauthorized identity use | Verified ownership or license object before generation |
| Removal requests | Slow or opaque handling | Dedicated reporting flow, SLA, audit trail |
| Age assurance | Restricted access by unqualified users | Verification state before sensitive features |
| Creator payouts | Fraud, chargebacks, account abuse | KYC/KYB, payout holds, risk scoring |
| Payments | Processor restrictions and reserves | Specialized processor research, clear category disclosure |
| Privacy | Sensitive data exposure | Data minimization, encryption, retention limits |
| Training data | Unlicensed images or unclear rights | Source tracking and consent event per dataset |
| Marketplace | Scope drift beyond creator terms | Machine-readable license checks |
| IP characters | Unlicensed brand/character use | Partner licensing before official packs |
| Cross-border access | Different local rules | Geo policy, local counsel, compliance gates |

## U.S. federal anchor

Public Law 119-12 creates a direct legal environment around AI-created intimate visual forgeries and platform removal workflows. Key operational implications for Efi-G:

- Build a clear removal request process.
- Record contact, evidence, and decision history.
- Respond quickly to valid reports.
- Remove known identical copies where technically feasible.
- Preserve a good-faith audit trail.

Source: https://www.govinfo.gov/content/pkg/PLAW-119publ12/html/PLAW-119publ12.htm

## Child safety anchor

The platform must maintain a strict zero-tolerance posture on any youth-related restricted content. U.S.-based electronic service providers have reporting obligations when they become aware of apparent child exploitation material on their systems.

Sources:

- https://www.missingkids.org/gethelpnow/cybertipline
- https://www.missingkids.org/theissues/csam

## Payment risk

Mainstream payment processors can be unstable for restricted media categories. Specialized processors should be evaluated early. Key diligence questions:

- Does the processor support the exact business category?
- What reserves are required?
- What monitoring and content rules apply?
- How are creator payouts handled?
- What is the chargeback threshold?
- What review rights does the processor reserve?
- Can the processor support subscriptions, credits, and marketplace payouts?

Research anchors:

- Segpay: https://segpay.com/
- Verotel: https://www.verotel.com/
- Epoch: https://epoch.com/

## Required launch policies

1. Terms of Service.
2. Privacy Policy.
3. Creator Terms.
4. Acceptable Use Policy.
5. Removal and Reporting Policy.
6. Copyright/DMCA Policy.
7. Refund Policy.
8. Marketplace Payout Policy.
9. Data Retention Policy.
10. Law Enforcement Request Policy.

## Counsel review checklist

- Entity structure.
- Processor onboarding category.
- Creator contractor terms.
- Consumer terms.
- Record retention.
- Content category rules.
- Model licensing.
- Dataset licensing.
- State-level age assurance obligations.
- EU/UK access and age assurance requirements.
- Biometric/privacy implications.
- Arbitration and dispute structure.

## Launch recommendation

Launch private studio first, then creator marketplace. Do not launch public marketplace or third-party avatar usage until counsel has reviewed consent, identity, payment, and removal workflows.

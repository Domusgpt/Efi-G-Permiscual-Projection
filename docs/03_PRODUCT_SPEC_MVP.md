# 03 — Product Spec MVP

## MVP objective

Ship a private avatar studio that proves governed generation can be fast, fun, and safe enough to support a marketplace later.

## MVP scope

### Must ship

1. Account creation.
2. Age and identity state flag.
3. User-owned avatar profile.
4. Reference upload flow.
5. Consent and rights record for each avatar.
6. Prompt entry and preset prompt templates.
7. Policy precheck before job submission.
8. Generation job queue.
9. Output gallery.
10. Private vault controls.
11. Manual review/admin queue.
12. Creator waitlist.
13. Basic credits and billing abstraction.
14. Audit ledger for every sensitive event.

### Must not ship first

1. Open public feed.
2. Public search of generated outputs.
3. Unbounded creator avatar marketplace.
4. Open model upload by users.
5. Automated partner/IP licensing.
6. Real-time rooms.
7. Video generation.

## User journeys

### Journey A — private self-avatar

1. User signs up.
2. User completes required verification state.
3. User creates a private avatar.
4. User uploads references.
5. System stores references in a restricted vault.
6. User accepts avatar rights declaration.
7. System creates an avatar license limited to the user.
8. User submits a prompt.
9. Prompt is checked against policy.
10. Job enters queue.
11. Output is stored privately.
12. User can delete, regenerate, favorite, or export.

### Journey B — creator waitlist

1. Creator applies.
2. Creator submits profile and expected audience size.
3. Creator defines desired license categories.
4. Admin reviews risk, quality, and business value.
5. Selected creators receive onboarding support.

### Journey C — internal review

1. System flags a prompt, reference, output, or account event.
2. Admin reviews in a dashboard.
3. Admin records decision and reason code.
4. System updates account, job, or avatar status.
5. Decision is logged.

## Core entities

| Entity | Purpose |
|---|---|
| User | Account, verification state, settings |
| Avatar | Governed identity or character object |
| AvatarLicense | Scope of allowed use |
| GenerationJob | Model request with policy and rights context |
| OutputAsset | Generated image or future media asset |
| ConsentEvent | Signed rights/permission record |
| PolicyDecision | Allow, block, review, or transform |
| CreditLedger | Credits purchased, used, refunded |
| ReviewCase | Human moderation/support case |

## MVP feature priorities

### P0

- Auth.
- Avatar profile.
- Upload vault.
- Generation queue.
- Output gallery.
- Consent ledger.
- Admin review.
- Basic policy engine.

### P1

- Creator waitlist.
- Credit ledger.
- Prompt presets.
- Model routing.
- Abuse reporting.
- Account controls.

### P2

- Creator storefront preview.
- Paid packs.
- Affiliate tracking.
- Advanced analytics.
- API for external asset partners.

## MVP success metrics

- First generation completion rate above 80%.
- Median generation latency within target for selected model tier.
- Fewer than 5% failed jobs due to infrastructure errors.
- Clear ratio of credit revenue to GPU cost.
- Creator waitlist conversion above 10% for qualified outreach.
- Manual review queue under SLA.
- Zero jobs executed without a rights scope and policy decision.

## Product philosophy

The platform should feel playful at the edge and strict at the core. Users should see a simple studio. Internally, every action flows through rights, policy, privacy, billing, and audit layers.

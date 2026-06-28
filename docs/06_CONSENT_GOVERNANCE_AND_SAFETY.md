# 06 — Consent Governance and Safety

## Governance thesis

Efi-G is not only an AI media platform. It is a rights-control system for identity assets. The user experience should feel simple, but internally every avatar and generation must be linked to a rights object.

## Core objects

### ConsentEvent

A signed event recording a user or creator action such as creation, license grant, scope change, pause, revocation, deletion request, or dispute.

### AvatarLicense

A machine-readable permission scope that determines who may use an avatar, for what categories, for how long, under what price, and with what review obligations.

### PolicyDecision

A decision produced before and after generation. Values:

- allow;
- block;
- review;
- transform;
- escalate.

### ReviewCase

A human review file with reason, evidence pointers, decision history, and SLA.

## Rights scope dimensions

| Dimension | Examples |
|---|---|
| Audience | self-only, invited users, customers, public marketplace |
| Duration | one-time, monthly, campaign, indefinite until revoked |
| Categories | creator-defined allowed and blocked categories |
| Output visibility | private, shared link, storefront preview |
| Monetization | free, credit-based, subscription, per-pack |
| Review | automatic, creator review, platform review |
| Revocation | immediate pause, future-only, full removal request |

## Consent ledger principles

1. Append-only events.
2. No silent scope expansion.
3. Scope changes create new versions.
4. Revocation must stop future jobs immediately.
5. Deletion requests must create lifecycle tasks.
6. Admin overrides require reason codes.
7. Marketplace access requires explicit creator publication.

## Safety layers

### Pre-generation

- Age and identity state check.
- Rights scope check.
- Prompt policy check.
- Rate-limit check.
- Credit reserve.
- Model profile compatibility check.

### Generation

- Use only allowed model profiles.
- Record model version and seed.
- Prevent jobs without a license object.
- Stop queue execution if avatar status changes.

### Post-generation

- Asset check.
- Review routing if uncertain.
- Store with visibility metadata.
- Record audit event.
- Support reporting, deletion, and disputes.

## Forbidden categories

The platform must reject illegal, exploitative, coercive, deceptive, youth-related, hateful, threatening, or non-permissioned identity use. Product copy can be permissive, but the rule engine must be strict.

## Creator controls

Creators need a dashboard to:

- pause avatar availability;
- change license categories;
- cap monthly usage;
- set price tiers;
- require review for selected categories;
- see usage analytics;
- export records;
- request deletion;
- open disputes.

## Customer controls

Customers need:

- private gallery controls;
- deletion controls;
- clear license receipts;
- report buttons;
- privacy settings;
- purchase history;
- account export.

## Admin controls

Admins need:

- review queue;
- policy decision history;
- user and creator status controls;
- avatar pause controls;
- asset removal tools;
- payment risk flags;
- audit search;
- incident notes.

## Trust design

The platform should show creators and customers exactly why an action is allowed or blocked. Consent should be visible, understandable, and versioned.

# 04 — Technical Architecture

## Goal

Build a platform where each AI media job is checked by user state, rights scope, policy, cost controls, and audit logging before model execution.

## Recommended stack

- **Web:** Next.js or Remix, Tailwind, admin console.
- **API:** TypeScript with NestJS or Fastify.
- **Database:** PostgreSQL with Prisma or Drizzle.
- **Queue/cache:** Redis.
- **Object storage:** S3-compatible storage such as R2, S3, or MinIO.
- **Workers:** Python workers for Diffusers or ComfyUI pipelines.
- **Observability:** OpenTelemetry, structured logs, metrics dashboard.

## Core services

```text
apps/web              user studio and admin console
apps/api              auth, rights, billing, policy, jobs
apps/worker-generate  model execution
apps/worker-policy    prompt and asset checks
apps/worker-vault     storage lifecycle and deletion
packages/shared       schemas and SDK types
infrastructure        compose, deployment, observability
```

## Generation control path

```text
1. User submits prompt.
2. API loads user state.
3. API loads avatar and license scope.
4. Rights engine checks allowed use.
5. Policy engine checks prompt.
6. Credit engine reserves credits.
7. Job is written to database.
8. Job is pushed to queue.
9. Worker runs the selected model profile.
10. Output is checked.
11. Output is stored or routed to review.
12. Credits are captured or released.
13. Audit event is written.
```

## Fail-closed controls

- No valid user state: block.
- No avatar license: block.
- No policy decision: block.
- No credit reserve: block.
- Missing model profile: block.
- Asset check failure: hold for review.
- Storage write failure: release credits.
- Ledger write failure: do not expose output.

## Data stores

| Store | Purpose |
|---|---|
| PostgreSQL | users, avatars, licenses, jobs, ledger, audit events |
| Redis | queues, rate limits, session cache |
| Object storage | user assets, generated assets, model artifacts |
| Secrets manager | API keys, signing keys, payment keys |

## Security model

- Separate identity state from public profile data.
- Separate source assets from generated assets.
- Separate payout records from avatar license records.
- Log every admin action.
- Use short-lived signed URLs.
- Prefer verification vendors that return status tokens instead of raw documents.
- Use envelope encryption for sensitive object storage.

## First implementation milestone

Build a mock generation path that writes complete job, rights, policy, credit, and audit records before any real model is connected. This proves the control plane before GPU costs begin.

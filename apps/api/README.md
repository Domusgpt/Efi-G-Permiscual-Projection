# apps/api

API service for auth, avatar records, rights checks, policy decisions, credits, generation jobs, review cases, and audit logging.

## First implementation target

Build a mock generation endpoint:

```http
POST /v1/generation-jobs
```

The endpoint should:

1. authenticate user;
2. load avatar license;
3. run policy precheck;
4. reserve credits;
5. create job record;
6. create audit event;
7. enqueue mock worker job;
8. return job id.

No real model should be connected until this path fails closed correctly.

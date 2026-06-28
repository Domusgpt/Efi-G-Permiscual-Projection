# Efi-G Permissual Projection

Efi-G is a permissioned avatar and fantasy-projection platform focused on user-owned identity, creator licensing, privacy, consent, and auditable AI media workflows.

## Principles

- Consent is the product.
- Self-projection is the default use case.
- Creator control is granular and revocable.
- Privacy is designed into the architecture.
- Marketplace growth must not weaken governance.
- Content and identity rules are enforced before generation.

## Repository map

```text
docs/
policies/
schemas/
apps/
infrastructure/
```

## Immediate engineering rule

A generation job must not run unless it is attached to a valid user, valid rights scope, prompt-policy decision, content-safety decision, and immutable audit event.

# 00 — Founding Brief

## Working name

**Efi-G Permissual Projection**

`Permissual` means permissioned, sensual-adjacent, self-authored, and governed. The term positions the company away from unsafe identity copying and toward controlled projection: a person owns the conditions under which their likeness, avatar, or character can be used.

## Company thesis

Modern image and video models make personal fantasy media cheap, fast, and expressive. The unmet market need is not just generation quality; it is trusted governance. Efi-G should become the platform where users and creators can safely project themselves, license avatars, create bounded experiences, and monetize controlled access without surrendering identity rights.

## Strategic wedge

The first wedge is private self-generation. A verified user can create an avatar from their own supplied references, generate limited private outputs, and learn the workflow without a public marketplace. This is faster to launch and lower risk than starting with open creator licensing.

The second wedge is permissioned creator avatars. Creators can publish avatar licenses with category limits, audience controls, price tiers, revocation options, expiration windows, and audit trails.

The third wedge is rooms: controlled interactive spaces where customers, creators, and eventually AI agents interact through licensed avatars and objects.

## Product promise

Efi-G lets people create and share fantasy identity media under rules they understand and control.

## Non-negotiable rules

- Real-person likeness use requires verified permission.
- User and creator data are minimized, separated, encrypted, and auditable.
- Every generation event has a policy decision and rights scope.
- Creators can pause, revoke, or narrow license scope.
- Harmful, illegal, coercive, youth-related, or deceptive identity use is not allowed.
- Marketplace growth cannot bypass safety review.

## First business objective

Build a small, trustworthy, revenue-capable MVP that proves:

1. private generation can be delightful;
2. consent can be technically enforced;
3. creators can define usable rights packages;
4. platform economics can work without racing to unsafe scale.

## First product decision

Do **not** launch as a generic unrestricted media generator. Launch as a rights-governed avatar studio with private generation first and marketplace licensing second.

## First technical decision

The core object is not the image. The core object is the **license-governed generation job**:

```text
user + avatar + license_scope + prompt + safety_policy + model_profile + audit_event -> output
```

If any element is missing or invalid, the job fails closed.

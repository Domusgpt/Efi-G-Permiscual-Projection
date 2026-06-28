# Privacy and Security Baseline

## Privacy posture

Efi-G should collect the minimum data needed to operate identity, rights, billing, safety, and generation workflows. Sensitive source assets and verification state should be isolated from public profiles and marketplace metadata.

## Data classes

| Class | Examples | Handling |
|---|---|---|
| Account | email, username, auth ids | encrypted at rest, access logged |
| Verification state | age/identity status token | vendor-token preferred, raw data minimized |
| Source assets | uploaded avatar references | private vault, limited retention |
| Generated assets | user outputs | visibility scoped, deletion supported |
| Rights records | consent events, license terms | append-only audit trail |
| Billing | payments, credits, payouts | processor-tokenized, finance access only |
| Review records | reports, decisions, notes | restricted admin access |

## Required controls

- MFA for admins.
- Role-based access control.
- Audit logs for admin actions.
- Short-lived signed URLs.
- Encryption at rest for object storage.
- Separate buckets for source and generated assets.
- Deletion lifecycle workflow.
- Data export process.
- Secrets manager.
- Production access approval.

## Retention draft

- Source assets: retain while avatar is active unless user deletes earlier.
- Generated assets: retain per user settings and subscription state.
- Rights records: retain as long as legally and operationally required.
- Billing records: retain according to tax, accounting, and processor requirements.
- Review records: retain according to safety and legal requirements.

## Security monitoring

Track login anomalies, admin actions, storage access, job spikes, payment risk, queue anomalies, and deletion workflow failures.

# Security Review Checklist (Before Enable)

Use this checklist before you turn on an external identity provider for your organization.

> Warning
> Complete this checklist before enabling a provider for production users.

## Access and Rollback

- Confirm at least one trusted admin can still sign in with NexPort credentials.
- Confirm break-glass admin access is documented and tested.
- Confirm you can disable the provider quickly if sign-in issues appear.

## Provider Configuration

- Verify the provider type and tenant/domain values match the intended environment.
- Verify client ID and client secret are current and active.
- Verify redirect URI values in the provider exactly match the values shown in NexPort.
- Verify discovery/authority settings resolve successfully.

## Claims and User Matching

- Verify required identity claims are returned (especially email or unique subject claim).
- Verify claim mapping rules are configured for required user profile fields.
- Verify allow/deny policy rules match your organization access policy.
- Verify at least one known user signs in successfully in a non-production test path.

## Validation and Monitoring

- Run **Validate** (or **Validate All**) and confirm provider health is **Healthy**.
- Confirm health message is clear and has no unresolved warnings.
- Confirm sign-in failures are visible in observability tools for your support team.
- Confirm audit records capture provider selection and sign-in outcomes.

## User Experience and Support Readiness

- Verify the provider display name and order are correct on the sign-in page.
- Verify user-facing error messaging is reviewed by support/operations.
- Verify support has a troubleshooting path and ownership for incident response.

## Go-Live Decision

Enable the provider only after all checklist items are complete and a rollout owner has approved go-live.

## Related Topics

- [Install and Enable Providers](install-and-enable.md)
- [Health and Validation](health-and-validation.md)
- [Troubleshooting](troubleshooting.md)

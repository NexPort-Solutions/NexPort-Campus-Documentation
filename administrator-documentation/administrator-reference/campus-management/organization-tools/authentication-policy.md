# Authentication Policy

Use **Authentication Policy** to configure password and authentication safeguards for your organization.

## Before You Start

- You must have permission to manage organization authentication policy.
- If your organization inherits from a parent organization, inherited values can apply unless override is enabled.

## Open Authentication Policy

1. Sign in as an administrator.
2. Open **Administrator Reference**.
3. Go to **Campus Management** > **Organization Tools** > **Authentication Policy**.

## Configure Policy Settings

The page supports inherited policy visibility for child organizations:

- **Inherited Value**: the value currently coming from parent scope.
- **Actual Value**: the value currently enforced for this organization.

Main settings:

- **Override Parent Auth Policy**: allows this organization to define its own policy values.
- **Require Users to use MFA**: requires MFA for users owned by the organization.
- **Require Admins to use MFA**: requires MFA for administrators.
- **Require Users to confirm Email**: enforces email confirmation for login workflows.
- **Require Password Complexity**: enables complexity checks.
- **Minimum Password Length**: required minimum length when complexity is enabled.
- **Require Uppercase Character**
- **Require Lowercase Character**
- **Require Numeric Character**
- **Require Special Character**
- **Require Password Rotation**: enables password expiration controls.
- **Maximum Password Age (Days)**: number of days until password expiration.
- **Password Expiry Reminder (Days)**: reminder lead time before expiration.
- **Password History Count**: number of recent passwords users cannot reuse.

## Validation Rules

- Numeric values cannot be negative.
- If rotation is enabled, **Maximum Password Age (Days)** must be greater than 0.
- If rotation is enabled and reminder is set, reminder days must be less than maximum age days.
- If complexity is enabled, **Minimum Password Length** must be greater than 0.

## Scope and Effective Enforcement

NexPort Campus enforces effective policy using the strictest applicable controls for a user across:

- The user’s owner organization.
- Organizations where the user has granted admin permissions.
- Organizations where the user has subscribed access.

This helps prevent weaker policy bypass when a user operates in multiple organizational scopes.

## Save and Verify

1. Update policy values.
2. Save changes.
3. Validate expected behavior by testing a password reset or password change for a representative user.

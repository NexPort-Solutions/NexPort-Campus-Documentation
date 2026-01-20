# Rules and Policies

Use rules to control which users can sign in through a provider based on identity claims (for example, email domain or group membership).

> Note
> Screenshot placeholder: Rules and policies editor for an installed provider.

## Rule Types

- **Allow** rules permit matching identities.
- **Deny** rules block matching identities.

## Add a Rule

1. Open **Identity Providers** and select an installed provider.
2. Select **Rules** (or **Policies**, depending on the provider card).
3. Choose **Add Rule**.
4. Select the claim to evaluate (for example, Email, Domain, or Group).
5. Choose a match operator (equals, contains, ends with, etc.).
6. Enter the value to compare against.
7. Choose **Allow** or **Deny**.
8. Save the rule set.

> Tip
> Keep rules narrow and test after each change with a known account.

## Example Policies

- Allow only users with email ending in `@example.com`.
- Deny users who have a specific group claim.
- Allow a trusted domain first, then add targeted denies for exceptions.

## Validate Policy Behavior

After saving rules:

1. Use **Health and Validation** to confirm provider reachability.
2. Perform a sign-in with a test account that matches and one that does not match the rule.
3. Adjust rule values as needed.

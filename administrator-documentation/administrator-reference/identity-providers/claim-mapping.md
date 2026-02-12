# Claim Mapping

Use claim mapping to control which identity-provider (IdP) claims populate NexPort user profile fields when users sign in through an external provider.

## What Claim Mapping Does

- Maps IdP claims to NexPort core profile fields (Email, First Name, Last Name).
- Maps IdP claims to custom profile fields created under **Customize Organization**.
- Supplies values used during first-time external sign-in so required fields can be filled automatically when the claims are available.

> Note
> Screenshot placeholder: Claim mapping section in the provider editor.

## Configure Claim Mapping

1. Open **Manage Campus** → **Identity Providers**.
2. Under **Installed**, open the provider card and select **Edit**.
3. In **Claim Mapping**, enter the claim name for each field you want to map.
4. Select **Save**.

## Verify a Claim Payload

Use the verification panel to preview how your mappings will populate NexPort fields:

1. Open the provider edit screen.
2. Paste a sample claims JSON payload.
3. Review the preview to confirm mapped values.

> Tip
> Use a test account and only paste non-sensitive claim data.

> Note
> Screenshot placeholder: Claim mapping verification panel with claims JSON and preview output.

## Required Fields and First-Time Login

When a user signs in with an external provider for the first time, NexPort attempts to populate required custom profile fields using your claim mappings. If required fields are still empty, the existing required-field workflow prompts the user to complete them.

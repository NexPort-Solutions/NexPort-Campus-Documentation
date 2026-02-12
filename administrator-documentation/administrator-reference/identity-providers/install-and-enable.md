# Install and Enable Providers

Use the **Identity Providers** tool in Manage Campus to install and enable external providers for the active organization.

> Note
> Screenshot placeholder: Identity Providers screen showing Available and Installed tabs.

## Before You Begin

- Confirm you are working in the correct organization.
- Ensure you have permission to manage Identity Providers.
- Gather provider-specific details (client ID, client secret, discovery/authority URL, tenant or domain settings, and redirect URIs).
- If automation is enabled in your environment, ensure a system operator has configured an **Identity Provider Connector**.

## Install a Provider (Organization Admin)

1. In **Manage Campus**, open **Identity Providers**.
2. Select the **Available** tab.
3. Choose a provider and select **Install**.
4. In the wizard, choose the connection method:
   - **Automated (Connector)**: pick a connector supplied by system operators. NexPort pre-populates required settings.
   - **Manual**: enter client details yourself.
5. Follow the provider steps in the wizard:
   - Copy the **redirect URI(s)** displayed by NexPort.
   - Register those redirect URIs with the provider.
   - Enter the provider credentials and required settings.
   - Run the **Pre-Enable Security Review** step and resolve any blocking failures.
6. Select **Save** to install the provider.

> Tip
> Use the redirect URIs shown in the wizard. Do not guess or re-type them from memory.

## Enable or Disable a Provider

Before enabling a provider for production users, complete the [Security Review Checklist (Before Enable)](security-review-checklist.md).

1. Open the **Installed** tab.
2. Locate the provider card.
3. Use the **Enabled** toggle to enable or disable it.
4. Save changes.

If NexPort blocks enable, use the **Review** action on the provider card to see checklist issues and required remediation.

> Tip
> Disable a provider to temporarily block sign-ins without removing configuration.

## Rollback Guidance

Use this sequence when an external sign-in rollout causes unexpected user impact:

1. Disable the affected provider in the **Installed** tab.
2. Confirm users can still sign in using the approved fallback sign-in method.
3. Review the provider **Troubleshooting** page and validation results.
4. Correct configuration, rerun review/validation, and re-enable only after checks pass.

## When You Need a Connector (System Operators)

If the wizard offers a connector option, the connector must exist and have an **active secret** before organization admins can use it.

1. Open **Administration** and select **Identity Providers**.
2. Go to the **Connectors** tab.
3. Select **Add Connector** and complete the connector fields.
4. Open the connector **Secrets** dialog and attach the bootstrap credentials.
5. Ensure the connector is **Enabled**.

For full connector guidance, see [Connectors (System Operators)](connectors.md).

# Provider Options

Each provider type uses a **typed configuration form** so administrators can supply the required OAuth/OIDC settings without editing raw JSON.

> Note
> Screenshot placeholder: Provider options editor for an installed provider.

## What You Can Configure

Provider fields vary by type, but typically include:

- Client ID and client secret (manual setup).
- Discovery or authority URL (OIDC providers).
- Tenant, domain, or organization restrictions.
- Scopes requested during sign-in.
- Additional provider-specific settings.

## Save and Validate

1. Open the provider card under **Installed**.
2. Select **Edit**.
3. Update the required fields.
4. Select **Save**.

NexPort validates required fields at save time and reports any missing or invalid values.

> Note
> Secrets are never displayed after save. Re-enter the secret to update it.

## Client Type Support

External identity providers are currently supported as **confidential clients only**. Public-client (PKCE-only) configurations are not supported yet.

## Automation Notes

If the provider was installed through a connector, some fields may be locked or pre-filled. Use the connector configuration when you need to update automation-driven values.

See [Connectors (System Operators)](connectors.md) for connector management details.

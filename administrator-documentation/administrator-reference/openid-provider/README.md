# NexPort as an Identity Provider (OpenID)

NexPort can act as an **OpenID Connect (OIDC) Identity Provider** so external client applications can authenticate NexPort users.

> Note
> This section covers **NexPort as the IdP**. For external IdPs (Google, Entra, etc.), see [Identity Providers (External)](../identity-providers/README.md).

## In This Section

- Manage OpenID client applications.
- Configure redirect URIs and scopes.
- Rotate secrets safely.
- Understand claims and token lifetimes.
- Troubleshoot common issues.

## Client Type Support

NexPort currently supports **confidential clients only**. Public-client (PKCE-only) applications are not supported yet.

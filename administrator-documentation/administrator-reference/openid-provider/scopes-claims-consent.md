# Scopes, Claims, and Consent

NexPort issues tokens based on the scopes requested by a client application.

> Note
> Screenshot placeholder: Scopes selector in OpenID Applications.

## Common Scopes

- `openid` - Required for OpenID Connect authentication.
- `profile` - Basic profile information (for example, name).
- `email` - User email address.

## Claims in Tokens

Claims returned depend on:

- The scopes requested by the client.
- The user profile attributes available in NexPort.

## Consent Behavior

If consent is enabled for a client:

1. Users see a consent prompt during login.
2. The prompt lists the requested scopes.
3. Users can approve or cancel the request.

> Tip
> Request only the scopes the client app truly needs.

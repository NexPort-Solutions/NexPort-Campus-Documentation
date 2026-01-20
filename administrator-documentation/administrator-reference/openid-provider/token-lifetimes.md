# Token Lifetimes and Refresh

Token lifetimes determine how long access and refresh tokens remain valid. Default values are controlled by system configuration.

> Note
> Screenshot placeholder: Token lifetime settings (if exposed in the UI).

## Access Tokens

Access tokens are short-lived and used to call APIs. Shorter lifetimes reduce risk if a token is leaked.

## Refresh Tokens

Refresh tokens allow clients to request new access tokens without re-prompting users. If your client depends on refresh tokens, ensure it stores them securely.

## When to Adjust Lifetimes

Contact a system operator if you need to change token lifetimes. Adjustments are usually made for:

- High-risk environments that require shorter sessions.
- Long-running integrations that need extended access.

> Tip
> Pair longer lifetimes with stronger client security controls.

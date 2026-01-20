# Troubleshooting

Use the checklist below to resolve the most common OpenID application issues.

> Note
> Screenshot placeholder: OpenID application error or validation message.

## Invalid Redirect URI

- Confirm the client uses an exact match for one of the registered redirect URIs.
- Verify protocol (http vs https), trailing slashes, and case sensitivity.

## Invalid Client Secret

- Regenerate the secret in **OpenID Applications**.
- Update the client application configuration.

## Missing Claims

- Confirm the client requests the correct scopes.
- Ensure the user profile contains the required information.

## User Cannot Sign In

- Verify the OpenID application is **Enabled**.
- Check for incorrect client ID or secret in the client configuration.
- Review logs for errors during the authorization flow.

# Password Policy Requirements and Expiration

This page explains what users should expect when an organization enables password policy controls.

## Who Is Affected

Password policy enforcement applies to users based on the organizational scopes they operate in, including:

- Their owner organization.
- Organizations where they have administrator rights.
- Organizations they access through subscription relationships.

If multiple scopes apply, NexPort Campus uses the strictest effective settings.

## What Happens When a Password Expires

- Password-based sign in is blocked until the password is updated.
- Web users are redirected to update credentials.
- API username/password authentication also fails until password update is complete.

## Password Requirements You May See

Depending on policy, users may be required to:

- Use a minimum password length.
- Include uppercase characters.
- Include lowercase characters.
- Include numbers.
- Include special characters.
- Avoid reusing recent passwords.

If a new password fails policy, the user is shown validation feedback and must choose a compliant password.

## Reset and Recovery

Users can still use the standard account recovery flow from the login page.

1. Open **I cannot access my account**.
2. Select **Reset your password**.
3. Complete reset using the email link.

The new password must satisfy current organization policy requirements.

## Related Topic

- [Access NexPort Campus](access-nexport-campus.md)

# Manage Client Applications

Use **OpenID Applications** to register client apps that rely on NexPort for authentication.

> Note
> Screenshot placeholder: OpenID Applications list with Create button.

## Before You Begin

- Confirm you are in the correct environment (production vs. test).
- Collect the client app redirect URI(s).
- Decide which scopes the client app needs.

## Create an Application

1. Open **Administration** → **OpenID Applications**.
2. Select **Create**.
3. Enter the required fields:
   - **Application name** for display and auditing.
   - **Redirect URI(s)** (exact matches required).
   - **Scopes** requested by the client.
4. (Optional) Complete any additional security settings shown in the form.
5. Save the application.

> Note
> Screenshot placeholder: OpenID application create form showing redirect URIs and scopes.

## View or Edit an Application

1. Open **OpenID Applications**.
2. Select the application.
3. Update fields as needed.
4. Save changes.

## Rotate Client Secrets

1. Open the application details.
2. Select **Set Secret** (or **Rotate Secret**, if shown).
3. Copy the new secret and store it securely.
4. Update the client application configuration.

> Warning
> Secrets are shown only once at creation. Store them immediately.

## Disable or Remove an Application

1. Open the application details.
2. Use **Disable** (or a similar toggle) to block sign-ins without deleting the app.
3. Remove the application only when it is no longer needed.

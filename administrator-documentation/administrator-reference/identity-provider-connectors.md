# Identity Provider Connectors

System operators use the **Identity Provider Connectors** screen to register reusable templates for external authentication providers such as Google and Azure/Entra ID. Each connector stores the metadata and automation mode that the organization-level "Connect Provider" wizard needs in order to create OAuth clients on demand.

> Note
> You must have the **CanManageSystemIntegrations** permission (System Operator) to see this screen.

## Open the Add Connector Screen

1. From the Campus navigation bar, choose **Administration**.
2. Select **Identity Providers** and open the **Connectors** tab.
3. Click **Add Connector** on the toolbar. The popup editor appears with the fields described below.

## Field Reference

| Field | Description | How to collect the information | Required |
| --- | --- | --- | --- |
| Display Name | Friendly label shown to other administrators when they pick a connector (for example, `Google Workspace – Production`). | Decide on a name that clearly identifies the provider and environment (Production, Sandbox, Region). | Yes |
| Description | Optional notes that explain how and when to use the connector. | Summarize any constraints, support contacts, or reminders (for example, "Used by US-East organizations only"). | No |
| Provider Type | Identifies which external identity provider the connector automates. Current options include **Google** and **AzureEntraId**; additional adapters will appear as they are deployed. | Choose the provider that matches the bootstrap credentials you will attach. | Yes |
| Automation Mode | Controls how the registration service interacts with the upstream provider. | Select the mode that matches the provider’s capabilities:<br>**Manual** – use when the provider does not expose automation; organization admins will paste client IDs and secrets manually.<br>**DynamicClientRegistration** – use when the connector’s secret is authorized to create OAuth clients through the provider’s API.<br>**DelegatedAdminConsent** – use when the connector relies on an administrator approving access (for example, Azure admin consent). | Yes |
| Environment Name | Short label that distinguishes connectors for different environments or tenants. | Enter a value such as `Production`, `Sandbox`, `Corporate`, or leave blank if you only have one environment. | No |
| Registration Options (JSON) | Advanced provider-specific settings that refine how automation runs. Typical values include overriding authorization endpoints, default scopes, or prompts. | Create a small JSON object using the structure documented for the provider driver. Examples:<br>`{"defaultScopes":["openid","email"],"authorizationEndpoint":"https://accounts.google.com/o/oauth2/v2/auth"}`<br>`{"authorizationTenant":"contoso.onmicrosoft.com","defaultScopes":["openid","offline_access"]}`<br>Leave blank unless the provider requires non-default scopes or endpoints. | No (only fill in when overrides are required) |
| Enabled | Toggles whether the connector can be selected by organization admins and used by automation. | Leave enabled for active connectors. Disable when you are retiring or testing a connector. | Yes |

> Tip
> Registration options should only include values that the provider automation supports. Keep the JSON minimal and validate that it is valid UTF-8 without trailing commas. Use an online JSON validator if needed.

## After You Save

1. **Attach a Secret** – Select the connector in the grid, choose **Secrets**, and upload or reference the bootstrap credentials (for example, a Google service account JSON or Azure application client secret). The connector stays unusable until it has an active secret.
2. **Verify Automation Mode** – For non-manual modes, ensure the secret grants the permissions required by the provider (admin consent for Azure, client registration scope for Google, etc.).
3. **Share the Connector Details** – Let organization administrators know which connector to choose when they run the **Connect Provider** wizard. Share any restrictions noted in the Description or Environment Name fields.

## Gather Provider Credentials

> Warning
> Do not paste raw secrets into the connector editor. Always store credentials through the **Secrets** dialog so that they are encrypted (Key Vault or DPAPI) and audited correctly.

### Google Workspace / Cloud Identity

1. Sign in to the [Google Cloud Console](https://console.cloud.google.com/) with an administrator account.
2. Create (or reuse) a service account that has the **Cloud Identity API** / **Client Registration** permissions required by your automation workflow.
3. Generate and download a JSON key for the service account.
4. (Optional) Decide whether you need to override scopes, the authorization endpoint, or consent prompts. Prepare a JSON payload similar to:<br>
   ```json
   {"defaultScopes":["openid","email","profile"],"authorizationEndpoint":"https://accounts.google.com/o/oauth2/v2/auth"}
   ```
5. In NexPort Campus, open the connector’s **Secrets** dialog, upload the service-account JSON, and mark it active.
6. Paste any default scope overrides into **Registration Options (JSON)**.

### Azure / Entra ID

1. Sign in to the [Azure Portal](https://portal.azure.com/) and open **Microsoft Entra ID**.
2. Register an application (single tenant or multitenant) that will act as the automation agent.
3. Assign the Microsoft Graph application permissions your automation flow requires (for example, `Application.ReadWrite.All`). Grant admin consent.
4. Create a client secret (or certificate) and note the Tenant ID, Client ID, and client secret value.
5. Capture any tenant-specific settings you need for authorization, such as a dedicated tenant segment (`contoso.onmicrosoft.com`) or consent prompt.
6. In NexPort Campus, open the connector’s **Secrets** dialog and store the client secret securely. The secret payload should include the Tenant ID and Client ID so automation can authenticate.
7. Provide optional overrides in **Registration Options (JSON)**, for example:<br>
   ```json
   {"authorizationTenant":"contoso.onmicrosoft.com","defaultScopes":["openid","offline_access","email"]}
   ```

## Troubleshooting

- **Connector not visible to org admins** – Confirm the connector is **Enabled** and that at least one active secret exists. Organization admins can only see connectors that have a valid secret.
- **Automation fails during the Connect Provider wizard** – Review the connector description and registration options for stale data. Verify the attached secret has not expired and still has the required permissions. Check audit logs for detailed error messages.
- **Need to rotate credentials** – Use the **Secrets** dialog to attach a new secret, mark it active, then revoke the old secret. No changes are needed in the connector editor itself.

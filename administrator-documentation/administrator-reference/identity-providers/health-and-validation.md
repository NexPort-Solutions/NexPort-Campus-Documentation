# Health and Validation

Each installed provider displays a **health status** based on OIDC discovery reachability.

> Note
> Screenshot placeholder: Provider card showing health badge, last success timestamp, and message.

## Status Meanings

- **Healthy**: Discovery succeeded and the provider is reachable.
- **Unhealthy**: Discovery failed (see message for details).
- **Unknown**: No validation has been recorded yet.

## Last Success and Message

- **Last success** shows the most recent successful validation time.
- **Message** shows the last error or warning captured during validation.

## Run Validation

1. Open **Identity Providers**.
2. Select the **Installed** tab.
3. Use **Validate** on a single provider or **Validate All** to check every installed provider.
4. Review the status badge and message.

> Note
> Health checks validate discovery endpoints only. They do not confirm end-user login success.

# Troubleshooting

Use the steps below to diagnose the most common identity provider issues.

> Note
> Screenshot placeholder: Provider error message or validation result details.

## Provider Validation Failed

1. Open the provider card and select **Edit**.
2. Verify required fields are populated.
3. Confirm the discovery/authority URL is correct and reachable.
4. Save and run **Validate** again.

## Discovery Unreachable

1. Confirm the authority URL matches the provider documentation.
2. Check network access from the NexPort environment (firewalls, proxies, allowlists).
3. If the provider recently changed endpoints, update the configuration and re-validate.

## Users Cannot Sign In

1. Ensure the provider is **Enabled** in the Installed tab.
2. Review **Rules and Policies** for deny rules that match the user.
3. Confirm the user is attempting to sign in through the correct provider option.
4. Try a known-good test account to isolate a user-specific issue.

## Invalid Client Secret

1. Regenerate the client secret in the external provider.
2. Update the provider configuration in NexPort.
3. Save and re-validate.

> Tip
> Review audit logs for configuration changes and enable/disable events.

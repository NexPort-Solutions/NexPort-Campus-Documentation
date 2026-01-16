---
description: Understand how tenant features and entitlements are applied to organizations.
---

# Tenant Features and Entitlements

Tenant features determine which capabilities are enabled for every organization
under a tenant. Entitlements are controlled at the tenant level and applied to
all organizations in the tenant tree unless a rule explicitly limits scope.

## Included vs. billable features

- **Included** features are available without additional billing.
- **Billable** features are enabled but tracked for billing purposes.

## How entitlements are applied

1. The tenant profile defines the billing context.
2. Billing rules list which features are included or billable.
3. Organizations under the tenant inherit those entitlements.

If an organization is not linked to a tenant profile, it defaults to the
platform baseline entitlements.

#### © NexPort Solutions. All Rights Reserved.

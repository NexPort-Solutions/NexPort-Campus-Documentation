---
description: Understand how blocked invoices are identified, surfaced, and resolved.
---

# Blocked Invoices

Blocked invoices are invoices that cannot be completed without manual review or
corrections. The system flags these invoices, pauses processing, and notifies
Billing Managers and SysOps.

## Why invoices are blocked

Blocked invoices typically result from missing or conflicting billing data,
invalid configurations, or rule conflicts. The blocked status helps ensure
invoices are not released until issues are resolved.

## Who can resolve blocked invoices

- **Billing Managers** can review blocked invoices and correct issues.
- **SysOps** can assist with platform-level fixes or escalations.

## Resolution flow

1. A billing job flags an invoice as blocked.
2. Billing Managers receive a notification and review the **Blocked Invoices**
   blade.
3. The blocking reason and guidance are displayed.
4. After corrections are made, the invoice is retried automatically.

#### © NexPort Solutions. All Rights Reserved.

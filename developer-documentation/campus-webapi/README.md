---
description: >-
  The Web API documentation page allows developers to test API calls through an
  easy to use web-based interface.
cover: ../../.gitbook/assets/Untitled-1-01.png
coverY: 0
---

# Campus WebAPI

The NexPort Campus WebAPI lets authorized integrations exchange data with NexPort Campus through a JSON-based, RPC-style API. Use the live API explorer and OpenAPI definition as the source of truth for available operations, required fields, response schemas, and permissions.

### API reference

* **Interactive API explorer:** [NexPort Web API](https://www.nexportcampus.com/api/ui/index)
* **OpenAPI/Swagger definition:** [https://www.nexportcampus.com/api/v1/swagger.nex](https://www.nexportcampus.com/api/v1/swagger.nex)
* **API base URL:** `https://www.nexportcampus.com/api/v1`
* **Transport:** HTTPS
* **Request and response format:** JSON

The explorer is useful for reviewing the contract and testing approved requests. Before developing against an operation, review its live description, required parameters, request schema, response schema, and documented error responses.

### Authenticate requests

Obtain an access token before calling protected operations.

1. Send a JSON request to `POST /api/v1/AdminApi/Authenticate` with an authorized Campus user's `username`, `password`, and `grant_type` of `password`.
2. Store the returned `access_token` securely and only for the period required by the integration. The response can include `expires_in`; the request also supports an optional `utc_expiration_date`.
3. Provide the token as the `access_token` query parameter when calling operations that require it. Confirm the requirement in the live operation reference.
4. Use `GET /api/v1/AdminApi/ValidateAccessToken` to check a token's validity or expiration when needed.

The Authenticate operation does not work for System Operators or users assigned the Customer Service role. API authorization is evaluated per operation, so an authenticated user must also hold the Campus permissions required by the endpoint being called.

> **Security note:** Treat usernames, passwords, and access tokens as secrets. Do not embed them in browser-delivered code, source control, screenshots, support tickets, or client-side logs. Because the current API contract passes access tokens in a query parameter, take particular care to prevent URLs from being retained in logs, browser history, telemetry, or referrer data.

### Available API areas

The live v1 definition currently includes these API areas:

* **Admin API** — administrative and organization-management operations.
* **Assessment API** — assessment-related operations.
* **Learning API** — learning, catalog, and enrollment-related operations.
* **Point of Sale API** — invoice, payment, purchase, and redemption operations.
* **Postman API** — Postman-related integration operation.
* **SCORM API** — SCORM-related operations.
* **SSO API** — single-sign-on and classroom access operations.

### Recommended integration workflow

1. Define the Campus data or transaction the external system needs to exchange.
2. Identify the applicable API area and review the matching live operation documentation.
3. Test with an authorized non-production account or safe test data where available.
4. Implement secure token storage, expiration handling, error handling, and retry behavior appropriate to the operation.
5. Validate the integration with the Campus roles and organization structure used in production before release.

### Support

For access, permissions, or API questions, contact NexPort Support at [support@nexportcampus.com](mailto:support@nexportcampus.com). Include the API operation name, request time in UTC, relevant organization context, and a sanitized error response. Never include passwords or access tokens.

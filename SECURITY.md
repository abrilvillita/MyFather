# Security

Report suspected vulnerabilities to **texthumanapp@gmail.com**. Include the affected page, a minimal reproduction, and the expected result. Do not include passwords, payment card details, access tokens, or other users' personal data. Please avoid publishing exploit details before a fix is available.

## Trust boundaries

- Browser identifiers, mode switches, payment return URLs and AI instructions are untrusted.
- The Worker verifies authentication with Supabase and checks that the session still exists.
- Child sessions are locked server-side. Returning to an adult account requires a fresh login.
- Administrative operations require both an administrator role and MFA.
- Only the payment provider's verified notification can fulfill an order. Fulfillment must occur in one database transaction.
- Secrets belong in Cloudflare's encrypted configuration. The administration panel is distributed separately and is not part of this repository.

## Validation

Run `npm ci` and `npm test`. Database upgrade validation must include role-based access tests and transaction rollback tests for duplicate payments and lesson rewards before deployment. Passing unit tests alone does not establish production readiness.

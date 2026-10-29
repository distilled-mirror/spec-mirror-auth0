> ## Documentation Index
> Fetch the complete documentation index at: https://auth0.com/llms.txt
> Use this file to discover all available pages before exploring further.

# Management API Access Tokens

> Learn how Auth0 Management API access tokens work and how to use them.

To call the [Auth0 Management API](https://auth0.com/docs/api/management/v2.md), you must provide an access token (Access Token: Authorization credential, in the form of an opaque string or JWT, used to access an API.) that contains the appropriate audience (Access Token: Authorization credential, in the form of an opaque string or JWT, used to access an API.) and scopes.

## Audience

The audience value for the Management API (Management API: A product to allow customers to perform administrative tasks.) is `https://{yourDomain}/api/v2/`.

## Scopes

Each Management API endpoint requires a specific set of scopes. Refer to the [Management API Explorer](https://auth0.com/docs/api/management/v2.md) for more information.

## Lifetime

The default token lifetime for the Management API is 86,400 seconds (24 hours).

You can [configure the token lifetime](https://auth0.com/docs/secure/tokens/access-tokens/update-access-token-lifetime.md) for each API individually.

## Security

* **Access token**: Once issued, an access token cannot be revoked. Auth0 recommends that you restrict the lifetime of your access tokens to the shortest value possible allowed by your use case.
* **Refresh token (Refresh Token: Token used to obtain a renewed Access Token without forcing users to log in again.)**: You can [revoke a refresh token](https://auth0.com/docs/secure/tokens/refresh-tokens/revoke-refresh-tokens.md) using the Dashboard, the Authentication API, or the Management API.
* **Client secret (Client Secret: Secret used by a client (application) to authenticate with the Authorization Server; it should be known to only the client and the Authorization Server and must be sufficiently random to not be guessable.)**: You can [rotate an application's client secret](https://auth0.com/docs/get-started/applications/rotate-client-secret.md) using the Dashboard or the Management API.

## Quota

Token quotas are determined by subscription tier. You can [review your current quota](https://support.auth0.com/reports/quota) in the Auth0 Support Center. If you have questions about pricing or quotas, please [contact our sales team](https://auth0.com/contact-us).

* Tokens issued for [internal Auth0 audiences](https://auth0.com/docs/secure/tokens/access-tokens/get-access-tokens.md#control-access-token-audience) do not count toward your quota.
* Tokens issued for custom audiences count toward your quota and are subject to [Auth0 Management API Rate Limits](https://auth0.com/docs/troubleshoot/customer-support/operational-policies/rate-limit-policy).

## Learn more

* [Get Management API Access Tokens for Testing](https://auth0.com/docs/secure/tokens/access-tokens/management-api-access-tokens/get-management-api-access-tokens-for-testing)
* [Get Management API Access Tokens for Production](https://auth0.com/docs/secure/tokens/access-tokens/management-api-access-tokens/get-management-api-access-tokens-for-production)
* [Get Management API Access Tokens for Single-Page Applications](https://auth0.com/docs/secure/tokens/access-tokens/management-api-access-tokens/get-management-api-tokens-for-single-page-applications)
* [Changes in Auth0 Management APIv2 Tokens](https://auth0.com/docs/secure/tokens/access-tokens/management-api-access-tokens/changes-in-auth0-management-apiv2-tokens)
* [Migrate to Management API Endpoints with Access Tokens](https://auth0.com/docs/troubleshoot/product-lifecycle/past-migrations/migrate-to-calling-api-with-access-tokens.md)

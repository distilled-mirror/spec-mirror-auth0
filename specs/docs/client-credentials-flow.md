> ## Documentation Index
> Fetch the complete documentation index at: https://auth0.com/llms.txt
> Use this file to discover all available pages before exploring further.

# Client Credentials Flow

> Learn how the Client Credentials flow works and why you should use it for machine-to-machine (M2M) applications.

The Client Credentials Flow (defined in [OAuth 2.0 RFC 6749, section 4.4](https://tools.ietf.org/html/rfc6749#section-4.4)) involves an application exchanging its application credentials, such as client ID (Client ID: Identification value given to your registered resource from Auth0.) and client secret (Client ID: Identification value given to your registered resource from Auth0.), for an access token (Client Secret: Secret used by a client (application) to authenticate with the Authorization Server; it should be known to only the client and the Authorization Server and must be sufficiently random to not be guessable.).

This flow is best suited for Machine-to-Machine (M2M) applications, such as CLIs, daemons, or backend services, because the system must authenticate and authorize the application instead of a user.

## How it works

![Flows - Client Credentials - Authorization sequence diagram(w/Border)](https://mintlify.s3.us-west-1.amazonaws.com/auth0/docs/images/cdy7uua7fh8z/4Ph562CAccmCUkKNXuEIlQ/47581872e40e87b2cca95aecf7f42c5b/diagram.png)

1. Application sends application's credentials to the Auth0 Authorization Server. To learn more about client authentication methods, read [Application Credentials](https://auth0.com/docs/secure/application-credentials.md).
2. Auth0 Authorization Server validates application's credentials.
3. Auth0 Authorization Server responds with an access token.
4. Application can use the access token to call an API on behalf of itself. For more information on this process, see [Validate JSON Web Tokens](https://auth0.com/docs/secure/tokens/json-web-tokens/validate-json-web-tokens.md).
5. API responds with requested data.

## How to implement it

The easiest way to implement the Client Credentials Flow is to follow our [Backend Quickstarts](https://auth0.com/docs/quickstart/backend).

Alternatively, you can use the Auth0 Authentication API to implement the Client Credentials Flow. For more information, read [Call Your API Using the Client Credentials Flow](https://auth0.com/docs/get-started/authentication-and-authorization-flow/client-credentials-flow/call-your-api-using-the-client-credentials-flow.md).

## Learn more

* [Auth0 Rules](https://auth0.com/docs/customize/rules.md)
* [Auth0 Hooks](https://auth0.com/docs/customize/hooks.md)
* [Tokens](https://auth0.com/docs/secure/tokens.md)
* [Token Best Practices](https://auth0.com/docs/secure/tokens/token-best-practices.md)
* [Which OAuth 2.0 Flow Should I Use?](https://auth0.com/docs/get-started/authentication-and-authorization-flow/which-oauth-2-0-flow-should-i-use.md)

> ## Documentation Index
> Fetch the complete documentation index at: https://auth0.com/llms.txt
> Use this file to discover all available pages before exploring further.

# APIs

> Explore key topics for working with APIs in Auth0, including registering APIs, configuring access policies, scopes, and token settings.

An [API](https://auth0.com/features/machine-to-machine) is an entity that represents an external resource, capable of accepting and responding to protected resource requests made by applications. In the [OAuth2 specification](https://tools.ietf.org/html/rfc6749), an API maps to the **Resource Server (Resource Server: Server hosting protected resources. Resource servers accept and respond to protected resource requests.)**.

## Authorize access to your APIs

At some point, your custom APIs will need to allow limited access to their protected resources on behalf of users. Authorization refers to the process of verifying what a user has access to. While often used interchangeably with [authentication](https://auth0.com/docs/authenticate.md), authorization represents a fundamentally different function. To learn more, read [Authentication and Authorization](https://auth0.com/docs/get-started/identity-fundamentals/authentication-and-authorization.md).

In authorization, a user or application is granted access to an API after the API determines the extent of the permissions that it should assign. Usually, authorization occurs after identity is successfully validated through authentication so that the API has some idea of what sort of access it should grant.

## Determine authorization through access control

Authorization can be determined through the use of [policies](https://auth0.com/docs/manage-users/access-control/authorization-policies.md) and [rules](https://auth0.com/docs/manage-users/access-control/rules-for-authorization-policies.md), which can be used with [role-based access control (RBAC)](https://auth0.com/docs/manage-users/access-control/rbac.md). Regardless of whether RBAC is used, requested access is transmitted to the API via scopes and granted access is returned in issued Access Tokens (Access Token: Authorization credential, in the form of an opaque string or JWT, used to access an API.).

The application can then use the Access Token to access the API's protected resources. The same Access Token can be used to access the API's resources without having to authenticate again until it expires.

## API permissions

Since only the API can know all of the possible actions that it can handle, it should have its own internal access control system in which it defines its own permissions. To determine a calling application's effective permissions, an API should combine incoming scopes with the permissions assigned within its own internal access control system and make access control decisions accordingly.

## Configure an API

To protect an API, you must register an API using the Auth0 Dashboard (Auth0 Dashboard: Auth0's main product to configure your services.). To learn more, see [Register APIs](https://auth0.com/docs/get-started/auth0-overview/set-up-apis.md).

Before you register any APIs in the Auth0 Dashboard, one API will already exist: the **Auth0 Management API**. To learn more about the features of the Management API and its available endpoints, see [Management API](https://auth0.com/docs/api/management/v2.md).

# Redocly Caafe

The Redocly Caafe API provides a complete set of tools for cafe operators to manage menus, orders, and revenue.
Use this API to automate your cafe operations and integrate with other services.
This guide helps you get started with the API and understand the typical workflow.

## Get started

To interact with the Redocly Caafe API, you must first register an OAuth2 client and obtain an access token.
The API uses Dynamic Client Registration for easy setup.

### Register an OAuth2 client

Register a new OAuth2 client by sending a `POST` request to the `/oauth2/register` endpoint.
This endpoint does not require authentication for the registration process.

```bash
curl -X POST https://api.cafe.redocly.com/oauth2/register \
  -H "Content-Type: application/json" \
  -d '{
    "name": "My Cafe Application",
    "scopes": ["menu:read", "menu:write", "orders:read", "orders:write", "revenue:read"],
    "grantTypes": ["client_credentials"]
  }'
```

The response includes a `clientId` and a `clientSecret`.
You must store these credentials securely as they are required to obtain access tokens.

### Get an access token

Use your client credentials to request an access token from the token endpoint.

```bash
curl -X POST https://api.cafe.redocly.com/oauth2/token \
  -u "YOUR_CLIENT_ID:YOUR_CLIENT_SECRET" \
  -d "grant_type=client_credentials" \
  -d "scope=menu:read menu:write orders:read orders:write revenue:read"
```

The service returns an `access_token` in the response.
Include this token in the `Authorization` header of your API requests as a Bearer token.

### Interact with the API

After you have an access token, you can start managing your cafe operations.
For example, use the following request to retrieve the current menu:

```bash
curl -X GET https://api.cafe.redocly.com/menu \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN"
```

## Workflow overview

The Redocly Caafe API supports a realistic workflow for managing a cafe.
Typically, you follow these steps:

- **Register client**: Create your API credentials dynamically.
- **Get tokens**: Authenticate using standard OAuth2 flows to get an access token.
- **Manage menu**: Create, update, or delete menu items and upload images.
- **Manage orders**: Monitor and update customer orders in real-time.
- **Track revenue**: Access statistics to monitor business performance.

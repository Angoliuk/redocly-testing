# API documentation guide

This guide explains how to add AsyncAPI and GraphQL documentation to the portal.

## Add AsyncAPI

To add AsyncAPI documentation, follow these steps:

1. Place your AsyncAPI definition file in the `docs/api/` directory.
   For example, use `docs/api/asyncapi.yaml`.
2. Update the `apidocs` section in your `redocly.yaml` file to reference the new definition.

Example configuration:

```yaml
apidocs:
  asyncapi-example:
    definition: docs/api/asyncapi.yaml
```

## Add GraphQL

To add GraphQL documentation, follow these steps:

1. Place your GraphQL schema file in the `docs/api/` directory.
   For example, use `docs/api/graphql.graphql`.
2. Update the `apidocs` section in your `redocly.yaml` file to reference the new definition.

Example configuration:

```yaml
apidocs:
  graphql-example:
    definition: docs/api/graphql.graphql
```

<!-- TODO: verify behavior with product team regarding automatic discovery of these files if apidocs is not present -->

# Documentation

## Glossary

- **Realm**: Redocly's documentation platform for building high-performance documentation sites.
- **Reunite**: Redocly's cloud platform for managing, collaborating on, and deploying documentation projects.
- **MCP**: Model Context Protocol, which allows AI models to interact with Redocly documentation and data.

## Troubleshooting

### Resolve dependency issues with preview

When using the preview feature, you might encounter dependency-related errors.
To resolve these issues, try the following steps:
- Delete the `node_modules` directory and your lockfile.
- Run `npm install` or `bun install` to perform a clean installation of dependencies.
- Verify that your environment uses the correct registry.

### Customize components with eject

The `eject` command allows you to customize the built-in components of the documentation theme.
When you eject a component, the system copies the component source code to your project directory.
Consider the following when you eject components:
- Ejected components do not receive automatic updates from the base theme.
- You must maintain and update ejected components manually.
- Use the `eject` command only when standard configuration options are insufficient.

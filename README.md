# Redocly Portal

This project is a Redocly Realm portal.

## Getting started

This project uses [Bun](https://bun.sh/) for package management.

### Custom registry

The project is configured to use a custom registry as defined in `bunfig.toml`.
The registry URL is `http://dev-verdaccio.redocly.host:8000/`.

Ensure you have access to this registry when installing dependencies.

## Available scripts

You can use the following scripts to develop and build the portal.

### Start development server

To start the development server with hot-reloading, run the following command:

```bash
bun start
```

Alternatively, if you are using npm, run:

```bash
npm start
```

This command runs `realm develop` internally.

### Build for production

To build the project for production, run the following command:

```bash
bun run build
```

Alternatively, if you are using npm, run:

```bash
npm run build
```

This command runs `realm build` internally.

# Uploader — Wasmer static site

This repository is configured as a static website using Wasmer's Static Web Server.

## What this demo does

The page lets a visitor select or drag a file into the browser and see its filename, MIME type, size, and last-modified date. It does not read file contents, upload files, or request credentials.

**Do not use this page to collect Roblox cookies, passwords, session tokens, API keys, or other credentials.**

## Deploy to Wasmer Edge

1. Install the [Wasmer CLI](https://docs.wasmer.io/install).
2. Sign in: `wasmer login`.
3. From the repository root, run: `wasmer deploy`.
4. Follow the CLI prompts to create/select your Wasmer Edge app and namespace.

The manifest serves the repository's root files through the `/public` directory inside the WebAssembly package. The web server configuration is in `settings/config.toml`.

## Test locally

From the repository root, run:

```sh
wasmer run . --net
```

Then open http://localhost:8080.

## Files

- `index.html` — static browser UI
- `wasmer.toml` — Wasmer package manifest
- `settings/config.toml` — Static Web Server configuration

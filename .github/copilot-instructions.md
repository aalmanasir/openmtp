# Copilot Instructions

## Project Overview

This repository contains OpenMTP, an Electron/JavaScript macOS application for Android/MTP file transfer. Treat it as a desktop application with build, packaging, device-transfer, and release-signing concerns.

## Engineering Rules

- Keep changes small and reviewable.
- Do not commit credentials, signing assets, notarization secrets, Apple credentials, GitHub tokens, or local machine paths.
- Preserve existing package scripts and release behavior unless the PR explicitly targets packaging.
- For dependency updates, check build impact across main, renderer, Electron packaging, and lint scripts.
- Prefer existing project conventions over broad refactors.

## Validation

Use the repository scripts where possible:

```bash
yarn lint
yarn build
```

If full packaging or notarization cannot run locally, document that limitation in the pull request.

## Risk Areas

- Electron main/renderer boundaries
- file-transfer and native bridge behavior
- macOS packaging, signing, and notarization
- dependency updates that affect Babel, Webpack, Electron, or native modules

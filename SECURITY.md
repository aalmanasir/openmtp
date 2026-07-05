# Security Policy

## Supported Scope

This repository contains an Electron desktop application for macOS file transfer with Android/MTP devices. Security review should prioritize:

- desktop file-system access
- device-transfer boundaries
- Electron main/renderer process behavior
- dependency and supply-chain risk
- packaging, signing, notarization, and release automation

## Reporting a Vulnerability

Do not open a public issue for a suspected vulnerability.

Use GitHub's private vulnerability reporting or contact the repository owner through a trusted private channel. Include:

- affected feature or file path
- reproduction steps
- expected impact
- whether local files, device data, signing material, credentials, or private logs may have been exposed

## Secret Handling

Never commit signing keys, Apple credentials, notarization secrets, GitHub tokens, recovery codes, `.env` files, or screenshots containing credentials. If a secret is exposed, revoke it immediately and replace it with a new value.

## Response Standard

Security fixes should be reviewed before merge and include validation notes covering build/package impact where relevant.

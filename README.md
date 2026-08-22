# Cooperative Releases

Public release channel for the Cooperative platform.

This repository intentionally contains only release metadata and deployable update packages. The application source repository remains private.

## Channels

- `channels/stable.json` - production-ready releases
- `channels/beta.json` - test/pre-release builds

Installed Cooperative instances may check these channel manifests over HTTPS. They do not need GitHub credentials.

## Security model

A release manifest identifies the version, minimum supported PHP/platform versions, package URL, SHA-256 checksum, release notes, and any explicitly removed paths. Cooperative verifies the package checksum before staging an update.

Automatic installation should only be enabled after the one-click update path has been proven on real shared-hosting environments.

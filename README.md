# Parmenas releases

Public release channel for **Parmenas**, the member-owned co-op platform by [Viable Food](https://viablefood.org).

*Commitments, carried out.*

This repository holds only signed release packages. The application source is private.

## What is here

Each [GitHub Release](../../releases) contains two files:

- `parmenas-vX.Y.Z.zip`: the complete application, ready to upload to shared hosting.
- `parmenas-vX.Y.Z.zip.sig.json`: its signature (version, commit, SHA-256 and an Ed25519 signature).

## How installations use it

A Parmenas installation checks this repository from **Administration → Updates**. When a co-op's administrator chooses **Download and apply**, Parmenas:

1. downloads the package and its signature;
2. verifies the signature against the release key pinned inside the installation, plus the SHA-256 and the archive contents, and refuses anything that does not match;
3. backs up the database, applies the update, and switches to the new version, with rollback available.

No GitHub account or token is needed to receive updates.

## New installations

Download the latest release's `.zip` and follow the Parmenas install guide from Viable Food. Installation needs only cPanel's File Manager, a web browser, and one cron job; no command line is required.

## Security

Only releases signed with the Parmenas release key are accepted by installations. Please report security concerns to Viable Food privately rather than opening a public issue.

# dental-clinic-regalado-updates

Public update manifest repository for **Dental Clinic Regalado**.

This repository contains the update metadata used by installed client environments to check for the latest approved application version and apply updates safely.

## Purpose

The main application source code is kept in a private repository, and the Docker images are published as private images in GHCR.

This public repository exists only to expose a small, non-sensitive update manifest so client installations can:

- check the latest approved version
- know which Docker images should be installed
- update to an exact version instead of relying on mutable tags such as `latest`

## Contents

This repository is expected to contain:

- `update.json` — the current stable update manifest

Example:

```json
{
  "channel": "stable",
  "version": "1.2.3",
  "appImage": "ghcr.io/avelarpablo/dental-clinic-regalado-app:1.2.3",
  "opsImage": "ghcr.io/avelarpablo/dental-clinic-regalado-ops:1.2.3"
}

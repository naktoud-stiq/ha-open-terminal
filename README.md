# Open Terminal for HAOS

Home Assistant OS wrapper for the official Open WebUI Open Terminal image.

## Design

This repository contains only Home Assistant metadata. It does not build
or modify Open Terminal itself.

The Home Assistant app pulls the official image directly from:

`ghcr.io/open-webui/open-terminal`

## Automatic updates

GitHub Actions checks the latest upstream stable release every six hours.

When a newer release is published, the workflow first verifies that the
matching official GHCR image exists. It then updates the Home Assistant
app version.

Home Assistant will consequently see the new version as a normal app
update.

# Open Terminal

This Home Assistant app runs the official Open WebUI Open Terminal image.

## Open WebUI

Configure this using:

Admin Panel -> Settings -> Integrations -> Open Terminal

The Open Terminal service is not exposed through a Home Assistant host port.
Open WebUI communicates with it through the internal Home Assistant app
network.

## Storage

The Home Assistant app data volume is mounted at:

/home/user

Files created there survive app restarts and upgrades.

## Security

This wrapper does not mount:

- the Docker socket
- Home Assistant /config
- the Supervisor API
- the host filesystem

Single-user mode is intentionally enabled while upstream multi-user
file-browser isolation concerns remain unresolved.

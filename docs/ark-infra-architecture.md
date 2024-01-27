# ARK Infrastructure

This document serves as a change log, detailing the updates, modifications, and overall evolution of the ARK data center infrastructure.

## Change Log

- _As of January 28th, 2024_
  - Initial documentation setup.
- _As of January 27th, 2024_
  - Discontinued the use of MAAS for server setup.
  - Transitioned to standard Ubuntu server installations with Cockpit for remote UI access.
  - All four servers can be managed from a single Cockpit instance.
  - The main host and entry point of the network is designated as `ark004`.
  - Installed and configured Portainer for container management.
  - `ark004` is the main host for Portainer, managing other hosts' Docker APIs through the Portainer agent.
  - Enabled the management of Docker containers on any host via the Portainer web UI hosted on `ark004`.

# ARK Infrastructure

This document serves as a change log, detailing the updates, modifications, and overall evolution of the ARK data center infrastructure.

## Change Log

### January 28th, 2024
  - Initial documentation setup.

### January 27th, 2024
  - Discontinued the use of MAAS for server setup.
  - Transitioned to standard Ubuntu server installations with Cockpit for remote UI access.
  - All four servers can be managed from a single Cockpit instance.
  - The main host and entry point of the network is designated as `ark004`.
  - Installed and configured Portainer for container management.
  - `ark004` is the main host for Portainer, managing other hosts' Docker APIs through the Portainer agent.
  - Enabled the management of Docker containers on any host via the Portainer web UI hosted on `ark004`.
  - Added three additional hard disks to `ark001`, totaling 1.5TB of storage for the machine.
  - Created an LVM of all these disks and mounted it as `/mnt/arkdisk`.
  - Set up an NFS server on `ark001` to make the storage accessible from all hosts.
  - Set up NFS clients on all other hosts and mounted the storage as `/mnt/arkdisk` on the clients as well.

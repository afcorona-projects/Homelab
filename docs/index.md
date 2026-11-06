# Homelab Docs

!!! note "The public copy"

    These pages document a home lab and are written every night by Jarvis, a self-hosted assistant that reads Proxmox, TrueNAS, Uptime Kuma, Caddy and Loki. This copy is published from the private one: LAN addresses are swapped for machine names, the home domain is example.com, and private notes stay at home.

Jarvis keeps these pages up to date from the lab itself. Last run: **Nov 06, 2026 5:15 AM**.

## Right now

- **38** of 43 containers and VMs running
- **30** of 30 Uptime Kuma monitors up
- Proxmox host **pve**: Proxmox VE 9.2.25, up 4d 18h, RAM 75.4 GB of 91.7 GB
- TrueNAS pools: Safety 46%, protected 31%, tank 92%, tank2 45%

Nothing needs a look.

## This week in the lab

A new Debian container and associated monitoring were added, while Proxmox VE received a minor version update. The period was marked by significant instability on the pve and CT 119 nodes, characterized by multiple OOM kills and service failures. Additionally, a new Caddy site was configured to point to an internal IP address.

**2026-11-06**

- New container: CT 136 debian at debian
- New Uptime Kuma monitor: Jarvis bot Discord → http://debian:8099/health

**2026-11-04**

- Proxmox VE on pve updated: 9.2.24 → 9.2.25

**2026-11-02**

- New Caddy site: docs.example.com → forgejo:80
- Incident: OOM kill: a process on ai
- Incident: OOM kill: a process on ai
- Incident: OOM kill: a process on ai
- Incident: OOM kill: a process on ai
- Incident: caddy failed on caddy (exit-code)
- Incident: jarvis-docs-caddy failed on pve (exit-code), and 1 other service

**2026-11-01**

- Incident: frigate failed on frigate (timeout)
- Incident: pve-cluster failed on pve (timeout), and 1 other service
- Incident: OOM kill: systemd in CT 119
- Incident: OOM kill: frigate.capture in CT 119
- Incident: OOM kill: frigate.capture in CT 119
- Incident: OOM kill: frigate.capture in CT 119
- Incident: OOM kill: frigate.capture in CT 119
- Incident: bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae36da3bf-79afdded6fc56c6c failed on unifi-os-server (exit-code)

**2026-10-31**

- Jarvis started documenting the lab: 42 containers and VMs.

## Not covered on this run

- ha: Home Assistant isn't set up yet (HA_URL and HA_TOKEN are empty)
- opnsense: OPNsense isn't set up yet (OPNSENSE_URL, OPNSENSE_KEY and OPNSENSE_SECRET are empty)

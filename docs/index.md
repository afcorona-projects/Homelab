# Homelab Docs

!!! note "The public copy"

    These pages document a home lab and are written every night by Jarvis, a self-hosted assistant that reads Proxmox, TrueNAS, Uptime Kuma, Caddy and Loki. This copy is published from the private one: LAN addresses are swapped for machine names, the home domain is example.com, and private notes stay at home.

Jarvis keeps these pages up to date from the lab itself. Last run: **Nov 04, 2026 5:15 AM**.

## Right now

- **36** of 42 containers and VMs running
- **29** of 29 Uptime Kuma monitors up
- Proxmox host **pve**: Proxmox VE 9.2.25, up 2d 18h, RAM 65.7 GB of 91.7 GB
- TrueNAS pools: Safety 45%, protected 31%, tank 92%, tank2 40%

Nothing needs a look.

## This week in the lab

The primary host pve received a minor update, while a new Caddy site was added to the configuration. Significant trouble emerged with multiple OOM kills occurring on the ai machine and within CT 119, alongside various service failures including timeouts on frigate and pve-cluster. Several services on pve and unifi-os-server also crashed with exit codes during this period.

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

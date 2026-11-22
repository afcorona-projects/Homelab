# Homelab Docs

!!! note "The public copy"

    These pages document a home lab and are written every night by Jarvis, a self-hosted assistant that reads Proxmox, TrueNAS, Uptime Kuma, Caddy and Loki. This copy is published from the private one: LAN addresses are swapped for machine names, the home domain is example.com, and private notes stay at home.

Jarvis keeps these pages up to date from the lab itself. Last run: **Nov 22, 2026 5:15 AM**.

## Right now

- **20** of 27 containers and VMs running
- **28** of 29 Uptime Kuma monitors up
- Proxmox host **pve**: Proxmox VE 9.2.32, up 3d 22h, RAM 48.4 GB of 91.7 GB
- TrueNAS pools: Safety 57%, protected 32%, tank 92%, tank2 49%

!!! warning "Needs a look"

    - Uptime Kuma: llama-ai is down

## This week in the lab

**2026-11-22**

- CT 127 AI: start at boot off
- Incident: OOM kill: a process on ai
- Incident: logrotate failed on monitoring (exit-code)

**2026-11-21**

- Proxmox VE on pve updated: 9.2.27 → 9.2.32
- Incident: pve-cluster failed on pve2 (timeout)

**2026-11-20**

- Removed: CT 102 homarr
- Removed: CT 104 patchmon
- Removed: CT 105 kometa
- Removed: CT 106 jelly-seerr
- Removed: CT 107 plex-seerr
- Removed: CT 110 tautulli
- Removed: CT 111 navidrome
- Removed: CT 113 audiobookshelf
- Removed: CT 114 komga
- Removed: CT 117 speedtest-tracker
- Removed: CT 118 qui
- Removed: CT 121 Monitoring
- Removed: CT 122 agregarr
- Removed: CT 123 sparkyfitness
- Removed: CT 129 ntfy
- … and 2 more ([changelog](changelog.md))

**2026-11-19**

- CT 115 Amp-UI: start at boot on

**2026-11-18**

- Kernel on pve: Linux 7.0.14-28-pve → Linux 7.0.14-29-pve
- Incident: OOM kill: a process on pve2
- Incident: jarvis-docs-caddy failed on pve (exit-code), and 1 other service

**2026-11-17**

- VM 204 Amp-T1: CPU 4 → 12 cores

**2026-11-15**

- CT 102 homarr: start at boot off
- CT 104 patchmon: start at boot off
- CT 105 kometa: start at boot off
- CT 106 jelly-seerr: start at boot off
- CT 107 plex-seerr: start at boot off
- CT 110 tautulli: start at boot off
- CT 111 navidrome: start at boot off
- CT 113 audiobookshelf: start at boot off
- CT 114 komga: start at boot off
- CT 117 speedtest-tracker: start at boot off
- CT 118 qui: start at boot off
- CT 121 Monitoring: start at boot off
- CT 122 agregarr: start at boot off
- CT 123 sparkyfitness: start at boot off
- CT 129 ntfy: start at boot off
- … and 6 more ([changelog](changelog.md))

## Not covered on this run

- ha: Home Assistant isn't set up yet (HA_URL and HA_TOKEN are empty)
- opnsense: OPNsense isn't set up yet (OPNSENSE_URL, OPNSENSE_KEY and OPNSENSE_SECRET are empty)

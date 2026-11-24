# Homelab Docs

!!! note "The public copy"

    These pages document a home lab and are written every night by Jarvis, a self-hosted assistant that reads Proxmox, TrueNAS, Uptime Kuma, Caddy and Loki. This copy is published from the private one: LAN addresses are swapped for machine names, the home domain is example.com, and private notes stay at home.

Jarvis keeps these pages up to date from the lab itself. Last run: **Nov 24, 2026 5:15 AM**.

## Right now

- **20** of 26 containers and VMs running
- **28** of 29 Uptime Kuma monitors up
- Proxmox host **pve**: Proxmox VE 9.2.32, up 5d 22h, RAM 51.2 GB of 91.7 GB
- TrueNAS pools: Safety 58%, protected 32%, tank 93%, tank2 49%

!!! warning "Needs a look"

    - Uptime Kuma: llama-ai is down

## This week in the lab

A significant number of containers were removed on November 20th, including homarr, jelly-seerr, plex-seerr, and various monitoring and media tools, while VM 204 Amp-T1 received a CPU upgrade from 4 to 12 cores. Several incidents occurred involving OOM kills on the AI containers and the Proxmox host, alongside a failed logrotate job and a cluster timeout on pve2. Additionally, the Caddy site rom.example.com was mapped to romm, Proxmox VE was updated to version 9.2.32, and the kernel was updated on November 18th.

**2026-11-23**

- Removed: CT 127 AI
- New Caddy site: rom.example.com → romm
- Incident: OOM kill: llama-server in CT 137

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

## Not covered on this run

- ha: Home Assistant isn't set up yet (HA_URL and HA_TOKEN are empty)

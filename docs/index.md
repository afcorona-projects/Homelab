# Homelab Docs

!!! note "The public copy"

    These pages document a home lab and are written every night by Jarvis, a self-hosted assistant that reads Proxmox, TrueNAS, Uptime Kuma, Caddy and Loki. This copy is published from the private one: LAN addresses are swapped for machine names, the home domain is example.com, and private notes stay at home.

Jarvis keeps these pages up to date from the lab itself. Last run: **Nov 26, 2026 5:15 AM**.

## Right now

- **21** of 27 containers and VMs running
- **28** of 29 Uptime Kuma monitors up
- Proxmox host **pve**: Proxmox VE 9.2.32, up 4h 28m, RAM 38.0 GB of 91.7 GB
- TrueNAS pools: Safety 60%, protected 32%, tank 93%, tank2 50%

!!! warning "Needs a look"

    - Uptime Kuma: llama-ai is down

## This week in the lab

Multiple containers including dispatcharr, homarr, patchmon, and others were removed or added, while the Proxmox VE kernel and system version were updated. Several incidents occurred involving failed containers, OOM kills on llama-server and ai, and a timeout in the pve-cluster service.

**2026-11-26**

- Kernel on pve: Linux 7.0.14-29-pve → Linux 7.0.14-30-pve
- Incident: bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae36da3bf-4f47cf8f3c0ba540 failed on unifi-os-server (exit-code)

**2026-11-25**

- New container: CT 138 dispatcharr at dispatcharr
- Incident: scrypted failed on scrypted (exit-code)

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

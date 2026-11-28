# Homelab Docs

!!! note "The public copy"

    These pages document a home lab and are written every night by Jarvis, a self-hosted assistant that reads Proxmox, TrueNAS, Uptime Kuma, Caddy and Loki. This copy is published from the private one: LAN addresses are swapped for machine names, the home domain is example.com, and private notes stay at home.

Jarvis keeps these pages up to date from the lab itself. Last run: **Nov 28, 2026 5:15 AM**.

## Right now

- **21** of 27 containers and VMs running
- **28** of 29 Uptime Kuma monitors up
- Proxmox host **pve**: Proxmox VE 9.2.32, up 2d 4h, RAM 41.6 GB of 91.7 GB
- TrueNAS pools: Safety 61%, protected 32%, tank 93%, tank2 51%

!!! warning "Needs a look"

    - Uptime Kuma: llama-ai is down

## This week in the lab

Over the last week, the Proxmox VE host received a security update while a new dispatcharr container was deployed and an AI container was removed. Significant concerns include multiple container exit-code failures, an OOM kill on the llama-server, and a cluster timeout event on pve2.

**2026-11-28**

- Incident: jarvis-snapshot failed on pve (exit-code)
- Incident: hb-dv-build failed on encoder (exit-code)

**2026-11-27**

- Incident: jarvis-snapshot failed on pve (exit-code)

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

# Homelab Docs

!!! note "The public copy"

    These pages document a home lab and are written every night by Jarvis, a self-hosted assistant that reads Proxmox, TrueNAS, Uptime Kuma, Caddy and Loki. This copy is published from the private one: LAN addresses are swapped for machine names, the home domain is example.com, and private notes stay at home.

Jarvis keeps these pages up to date from the lab itself. Last run: **Nov 13, 2026 5:15 AM**.

## Right now

- **37** of 43 containers and VMs running
- **29** of 29 Uptime Kuma monitors up
- Proxmox host **pve**: Proxmox VE 9.2.26, up 18h 26m, RAM 64.2 GB of 91.7 GB
- TrueNAS pools: Safety 51%, protected 32%, tank 92%, tank2 48%

Nothing needs a look.

## This week in the lab

Several services experienced failures or resource issues, including an OOM kill on fr.embeddi and exit code errors on unifi-os-server and llm. Operational changes included resizing the romm container disk, updating Proxmox and the host kernel, and adding a new container and Caddy site. A Uptime Kuma monitor was removed while a new one was added for the Jarvis bot.

**2026-11-13**

- Incident: bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae36da3bf-13c9ad3618030068 failed on unifi-os-server (exit-code)

**2026-11-12**

- Incident: OOM kill: frigate.embeddi in CT 119

**2026-11-11**

- Incident: llm failed on ai (exit-code)

**2026-11-10**

- New Caddy site: abs.example.com → audiobookshelf:13378

**2026-11-09**

- Uptime Kuma monitor removed: homepage

**2026-11-08**

- Kernel on pve: Linux 7.0.14-26-pve → Linux 7.0.14-28-pve
- Incident: bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae36da3bf-36f4230e97b751c5 failed on unifi-os-server (exit-code)

**2026-11-07**

- CT 116 romm: disk rootfs 30 GB on vm1 → 50 GB on vm1
- Proxmox VE on pve updated: 9.2.25 → 9.2.26

**2026-11-06**

- New container: CT 136 debian at debian
- New Uptime Kuma monitor: Jarvis bot Discord → http://debian:8099/health

## Not covered on this run

- ha: Home Assistant isn't set up yet (HA_URL and HA_TOKEN are empty)
- opnsense: OPNsense isn't set up yet (OPNSENSE_URL, OPNSENSE_KEY and OPNSENSE_SECRET are empty)

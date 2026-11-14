# Homelab Docs

!!! note "The public copy"

    These pages document a home lab and are written every night by Jarvis, a self-hosted assistant that reads Proxmox, TrueNAS, Uptime Kuma, Caddy and Loki. This copy is published from the private one: LAN addresses are swapped for machine names, the home domain is example.com, and private notes stay at home.

Jarvis keeps these pages up to date from the lab itself. Last run: **Nov 14, 2026 5:15 AM**.

## Right now

- **37** of 43 containers and VMs running
- **29** of 29 Uptime Kuma monitors up
- Proxmox host **pve**: Proxmox VE 9.2.26, up 11h 6m, RAM 57.3 GB of 91.7 GB
- TrueNAS pools: Safety 52%, protected 32%, tank 92%, tank2 48%

Nothing needs a look.

## This week in the lab

Multiple services experienced failures or were killed, including unifi-os-server, llm, and frigate due to an OOM event. Infrastructure changes included a Proxmox VE and kernel update, disk expansion for CT 116, and the removal of an Uptime Kuma monitor. A new Caddy site was added for abs.example.com.

**2026-11-14**

- Incident: bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae36da3bf-52594ed44ecba93f failed on unifi-os-server (exit-code)

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

## Not covered on this run

- ha: Home Assistant isn't set up yet (HA_URL and HA_TOKEN are empty)
- opnsense: OPNsense isn't set up yet (OPNSENSE_URL, OPNSENSE_KEY and OPNSENSE_SECRET are empty)

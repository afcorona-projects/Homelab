# Homelab Docs

!!! note "The public copy"

    These pages document a home lab and are written every night by Jarvis, a self-hosted assistant that reads Proxmox, TrueNAS, Uptime Kuma, Caddy and Loki. This copy is published from the private one: LAN addresses are swapped for machine names, the home domain is example.com, and private notes stay at home.

Jarvis keeps these pages up to date from the lab itself. Last run: **Nov 21, 2026 5:15 AM**.

## Right now

- **21** of 27 containers and VMs running
- **29** of 29 Uptime Kuma monitors up
- Proxmox host **pve**: Proxmox VE 9.2.32, up 2d 22h, RAM 73.3 GB of 91.7 GB
- TrueNAS pools: Safety 56%, protected 32%, tank 92%, tank2 49%

Nothing needs a look.

## This week in the lab

A massive cleanup occurred on November 20th with the removal of fifteen containers, following a period where their auto-start settings were disabled. The Proxmox host received a kernel update and a minor version upgrade, though this was accompanied by an OOM kill incident and a cluster timeout error. Additionally, the Amp-T1 virtual machine had its CPU cores increased to twelve to handle its workload.

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

**2026-11-14**

- Incident: bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae36da3bf-52594ed44ecba93f failed on unifi-os-server (exit-code)

## Not covered on this run

- ha: Home Assistant isn't set up yet (HA_URL and HA_TOKEN are empty)
- opnsense: OPNsense isn't set up yet (OPNSENSE_URL, OPNSENSE_KEY and OPNSENSE_SECRET are empty)

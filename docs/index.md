# Homelab Docs

!!! note "The public copy"

    These pages document a home lab and are written every night by Jarvis, a self-hosted assistant that reads Proxmox, TrueNAS, Uptime Kuma, Caddy and Loki. This copy is published from the private one: LAN addresses are swapped for machine names, the home domain is example.com, and private notes stay at home.

Jarvis keeps these pages up to date from the lab itself. Last run: **Nov 16, 2026 5:15 AM**.

## Right now

- **21** of 43 containers and VMs running
- **29** of 29 Uptime Kuma monitors up
- Proxmox host **pve**: Proxmox VE 9.2.27, up 1d 6h, RAM 60.9 GB of 91.7 GB
- TrueNAS pools: Safety 54%, protected 32%, tank 92%, tank2 49%

Nothing needs a look.

## This week in the lab

The Proxmox host and TrueNAS were updated to new versions, while the Amp-T1 VM was configured to start at boot. Several containers were disabled from starting automatically, but multiple services including unifi-os-server, komga, and frigate experienced failures or out-of-memory errors.

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

## Not covered on this run

- ha: Home Assistant isn't set up yet (HA_URL and HA_TOKEN are empty)
- opnsense: OPNsense isn't set up yet (OPNSENSE_URL, OPNSENSE_KEY and OPNSENSE_SECRET are empty)

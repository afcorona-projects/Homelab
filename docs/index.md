# Homelab Docs

!!! note "The public copy"

    These pages document a home lab and are written every night by Jarvis, a self-hosted assistant that reads Proxmox, TrueNAS, Uptime Kuma, Caddy and Loki. This copy is published from the private one: LAN addresses are swapped for machine names, the home domain is example.com, and private notes stay at home.

Jarvis keeps these pages up to date from the lab itself. Last run: **Nov 01, 2026 2:34 PM**.

## Right now

- **36** of 42 containers and VMs running
- **29** of 29 Uptime Kuma monitors up
- Proxmox host **pve**: Proxmox VE 9.2.24, up 4h 5m, RAM 70.1 GB of 91.7 GB
- TrueNAS pools: Safety 43%, protected 31%, tank 93%, tank2 40%

Nothing needs a look.

## This week in the lab

Multiple services on the frigate and pve hosts experienced failures or timeouts, with frigate crashing repeatedly due to out-of-memory kills in container 119. The pve-cluster service also failed on the pve node alongside another unspecified service. A container on the unifi-os-server terminated with an exit code error.

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

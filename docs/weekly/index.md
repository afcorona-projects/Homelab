# Weekly reports

Every Sunday at 5:15 AM Jarvis writes up the lab's week: backups, disks, storage, the library, changes and incidents, and sends the note to your phone.

## This week so far

Since Sat Oct 31, 5:15 AM:

- Backups: all 6 runs clean; 11 guests with no backup in 8 days
- Disks: 2 problems this week: TrueNAS warning: homepage: API key has been revoked and must either be renewed or deleted. Revoke reason: Attempt to use over an insecure transport. Once the maintenance is complete, API client configuration must be u; ZFS pool bad2 on pve: /dev/disk/by-id/ata-CT500MX500SSD1_2213E621E335-part1 has errors (write 8)
- Storage: Safety (TrueNAS) 47% (+37.5 GB this week), full in about 13 weeks at this rate; bad1 (Proxmox host) 0%; bad2 (Proxmox host) 78% (+62.7 GB this week), full in about 2 weeks at this rate; protected (TrueNAS) 32% (+194.8 GB this week); rpool (Proxmox host) 45% (+1.2 GB this week); tank (TrueNAS) 92% (−168.6 GB this week); tank2 (TrueNAS) 46% (+970.6 GB this week), full in about 9 weeks at this rate; vm1 (Proxmox host) 22% (+2.7 GB this week); vm2 (Proxmox host) 44% (+29.8 GB this week), full in about 18 weeks at this rate; vm3 (Proxmox host) 5% (−2 GB this week)
- Library: 38 new movies (22 in 4K), 268 new episodes of 9 shows, 145 of 727 movies still without Latin American Spanish
- Docker images: 14 of 27 containers with a newer image waiting (bazarr, handbrake, hassio_observer, hassio_supervisor, kometa, …)
- Changes: 6 in the lab
- Incidents: 5 (jarvis-docs-caddy failed on pve (exit-code), and 1 other service; caddy failed on caddy (exit-code); OOM kill: a process on ai)

The first report comes on Sunday.

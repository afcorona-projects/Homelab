# Weekly reports

Every Sunday at 5:15 AM Jarvis writes up the lab's week: backups, disks, storage, the library, changes and incidents, and sends the note to your phone.

## This week so far

Since Fri Oct 30, 5:15 AM:

- Backups: all 6 runs clean; 11 guests with no backup in 8 days
- Disks: 2 problems this week: TrueNAS warning: homepage: API key has been revoked and must either be renewed or deleted. Revoke reason: Attempt to use over an insecure transport. Once the maintenance is complete, API client configuration must be u; ZFS pool bad2 on pve: /dev/disk/by-id/ata-CT500MX500SSD1_2213E621E335-part1 has errors (write 8)
- Storage: Safety (TrueNAS) 46%, full in about 13 weeks at this rate; bad1 (Proxmox host) 0%; bad2 (Proxmox host) 76%, full in about 2 weeks at this rate; protected (TrueNAS) 31%; rpool (Proxmox host) 45%; tank (TrueNAS) 92%; tank2 (TrueNAS) 45%, full in about 10 weeks at this rate; vm1 (Proxmox host) 22%; vm2 (Proxmox host) 42%; vm3 (Proxmox host) 5%
- Library: 28 new movies (21 in 4K), 264 new episodes of 8 shows, 143 of 714 movies still without Latin American Spanish
- Docker images: 14 of 27 containers with a newer image waiting (bazarr, handbrake, hassio_observer, hassio_supervisor, kometa, …)
- Changes: 4 in the lab
- Incidents: 6 (jarvis-docs-caddy failed on pve (exit-code), and 1 other service; caddy failed on caddy (exit-code); OOM kill: a process on ai)

The first report comes on Sunday.

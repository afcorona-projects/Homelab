# Weekly reports

Every Sunday at 5:15 AM Jarvis writes up the lab's week: backups, disks, storage, the library, changes and incidents, and sends the note to your phone.

## This week so far

Since Thu Oct 29, 5:15 AM:

- Backups: all 6 runs clean; 11 guests with no backup in 8 days
- Disks: 2 problems this week: TrueNAS warning: homepage: API key has been revoked and must either be renewed or deleted. Revoke reason: Attempt to use over an insecure transport. Once the maintenance is complete, API client configuration must be u; ZFS pool bad2 on pve: /dev/disk/by-id/ata-CT500MX500SSD1_2213E621E335-part1 has errors (write 8)
- Storage: Safety (TrueNAS) 46%; bad1 (Proxmox host) 0%; bad2 (Proxmox host) 74%; protected (TrueNAS) 31%; rpool (Proxmox host) 45%; tank (TrueNAS) 92%; tank2 (TrueNAS) 41%; vm1 (Proxmox host) 22%; vm2 (Proxmox host) 35%; vm3 (Proxmox host) 5%
- Library: 22 new movies (19 in 4K), 253 new episodes of 10 shows, 143 of 708 movies still without Latin American Spanish
- Docker images: 13 of 27 containers with a newer image waiting (bazarr, handbrake, hassio_observer, hassio_supervisor, kometa, …)
- Changes: 2 in the lab
- Incidents: 7 (jarvis-docs-caddy failed on pve (exit-code), and 1 other service; caddy failed on caddy (exit-code); OOM kill: a process on ai)

The first report comes on Sunday.

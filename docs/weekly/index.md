# Weekly reports

Every Sunday at 5:15 AM Jarvis writes up the lab's week: backups, disks, storage, the library, changes and incidents, and sends the note to your phone.

## This week so far

Since Sun Nov 8, 5:15 AM:

- Backups: the one run was clean; 11 guests with no backup in 8 days
- Disks: 2 problems this week: TrueNAS warning: homepage: API key has been revoked and must either be renewed or deleted. Revoke reason: Attempt to use over an insecure transport. Once the maintenance is complete, API client configuration must be u; ZFS pool bad2 on pve: /dev/disk/by-id/ata-CT500MX500SSD1_2213E621E335-part1 has errors (write 2)
- Storage: Safety (TrueNAS) 49% (+45.3 GB this week), full in about 11 weeks at this rate; bad1 (Proxmox host) 0%; bad2 (Proxmox host) 81% (+103.6 GB this week), full in about 2 weeks at this rate; protected (TrueNAS) 32% (+194.8 GB this week); rpool (Proxmox host) 45% (+1.2 GB this week); tank (TrueNAS) 92% (−204.2 GB this week); tank2 (TrueNAS) 47% (+1.1 TB this week), full in about 10 weeks at this rate; vm1 (Proxmox host) 23% (+4.9 GB this week); vm2 (Proxmox host) 43% (+57.6 GB this week), full in about 25 weeks at this rate; vm3 (Proxmox host) 5%
- Library: 4 new movies (3 in 4K), 1 new episode of 1 show, 145 of 738 movies still without Latin American Spanish
- Docker images: 6 of 27 containers with a newer image waiting (hassio_observer, hassio_supervisor, kometa, qbittorrent, patchmon-guacd-1, …); you updated 11 this week
- Changes: 1 in the lab
- Incidents: none

## Past weeks

| Week ending | Backups | Disks | Changes | Incidents |
|---|---|---|---|---|
| [Nov 8, 2026](2026-W45.md) | all 7 runs clean; 11 guests with no backup in 8 days | 2 problems this week: TrueNAS warning: homepage: API key has been revoked and mu | 7 in the lab | 2 (bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae |

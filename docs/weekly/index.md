# Weekly reports

Every Sunday at 5:15 AM Jarvis writes up the lab's week: backups, disks, storage, the library, changes and incidents, and sends the note to your phone.

## This week so far

Since Sun Nov 15, 5:15 AM:

- Backups: all 5 runs clean; 7 guests with no backup in 8 days
- Disks: 2 problems this week: TrueNAS warning: homepage: API key has been revoked and must either be renewed or deleted. Revoke reason: Attempt to use over an insecure transport. Once the maintenance is complete, API client configuration must be u; ZFS pool bad2 on pve: /dev/disk/by-id/ata-CT500MX500SSD1_2213E621E335-part1 has errors (write 2)
- Storage: Safety (TrueNAS) 56% (+40.1 GB this week), full in about 10 weeks at this rate; bad1 (Proxmox host) 0%; bad2 (Proxmox host) 34% (−124.9 GB this week); protected (TrueNAS) 32%; rpool (Proxmox host) 45%; tank (TrueNAS) 92%; tank2 (TrueNAS) 51% (+466.8 GB this week), full in about 13 weeks at this rate; vm1 (Proxmox host) 19% (−31 GB this week); vm2 (Proxmox host) 49% (+29.7 GB this week), full in about 18 weeks at this rate; vm3 (Proxmox host) 5%
- Library: 4 new movies (3 in 4K), 65 new episodes of 2 shows, 148 of 753 movies still without Latin American Spanish
- Docker images: 11 of 28 containers with a newer image waiting (hassio_observer, qbittorrent, bazarr, gluetun, prowlarr, …); you updated 2 this week
- Changes: 20 in the lab
- Incidents: 2 (jarvis-docs-caddy failed on pve (exit-code), and 1 other service; OOM kill: a process on pve2)

## Past weeks

| Week ending | Backups | Disks | Changes | Incidents |
|---|---|---|---|---|
| [Nov 15, 2026](2026-W46.md) | all 20 runs clean; 11 guests with no backup in 8 days | 3 problems this week: TrueNAS warning: homepage: API key has been revoked and mu | 21 in the lab | 6 (komga failed on komga (exit-code), and 2 other services; |
| [Nov 8, 2026](2026-W45.md) | all 7 runs clean; 11 guests with no backup in 8 days | 2 problems this week: TrueNAS warning: homepage: API key has been revoked and mu | 7 in the lab | 2 (bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae |

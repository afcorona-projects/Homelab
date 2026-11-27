# Weekly reports

Every Sunday at 5:15 AM Jarvis writes up the lab's week: backups, disks, storage, the library, changes and incidents, and sends the note to your phone.

## This week so far

Since Sun Nov 22, 5:15 AM:

- Backups: all 4 runs clean; 7 guests with no backup in 8 days
- Disks: 2 problems this week: TrueNAS warning: homepage: API key has been revoked and must either be renewed or deleted. Revoke reason: Attempt to use over an insecure transport. Once the maintenance is complete, API client configuration must be u; ZFS pool bad2 on pve: /dev/disk/by-id/ata-CT500MX500SSD1_2213E621E335-part1 has errors (write 2)
- Storage: Safety (TrueNAS) 60% (+39.3 GB this week), full in about 9 weeks at this rate; bad1 (Proxmox host) 0%; bad2 (Proxmox host) 42% (+36.2 GB this week); protected (TrueNAS) 32%; rpool (Proxmox host) 45%; tank (TrueNAS) 93% (+225 GB this week); tank2 (TrueNAS) 51% (+15.3 GB this week), full in about 17 weeks at this rate; vm1 (Proxmox host) 16% (−31.2 GB this week); vm2 (Proxmox host) 36% (−112.4 GB this week); vm3 (Proxmox host) 5% (+1.7 GB this week)
- Library: 10 new movies (3 in 4K), 89 new episodes of 3 shows, 149 of 762 movies still without Latin American Spanish
- Docker images: 12 of 25 containers with a newer image waiting (hassio_observer, qbittorrent, bazarr, gluetun, prowlarr, …); you updated 1 this week
- Changes: 4 in the lab
- Incidents: 4 (jarvis-snapshot failed on pve (exit-code); bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae36da3bf-4f47cf8f3c0ba540 failed on unifi-os-server (exit-code); scrypted failed on scrypted (exit-code))

## Past weeks

| Week ending | Backups | Disks | Changes | Incidents |
|---|---|---|---|---|
| [Nov 22, 2026](2026-W47.md) | all 8 runs clean; 7 guests with no backup in 8 days | 2 problems this week: TrueNAS warning: homepage: API key has been revoked and mu | 22 in the lab | 5 (logrotate failed on monitoring (exit-code); OOM kill: a p |
| [Nov 15, 2026](2026-W46.md) | all 20 runs clean; 11 guests with no backup in 8 days | 3 problems this week: TrueNAS warning: homepage: API key has been revoked and mu | 21 in the lab | 6 (komga failed on komga (exit-code), and 2 other services; |
| [Nov 8, 2026](2026-W45.md) | all 7 runs clean; 11 guests with no backup in 8 days | 2 problems this week: TrueNAS warning: homepage: API key has been revoked and mu | 7 in the lab | 2 (bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae |

# Weekly reports

Every Sunday at 5:15 AM Jarvis writes up the lab's week: backups, disks, storage, the library, changes and incidents, and sends the note to your phone.

## This week so far

Since Sun Nov 22, 5:15 AM:

- Backups: all 2 runs clean; 7 guests with no backup in 8 days
- Disks: 2 problems this week: TrueNAS warning: homepage: API key has been revoked and must either be renewed or deleted. Revoke reason: Attempt to use over an insecure transport. Once the maintenance is complete, API client configuration must be u; ZFS pool bad2 on pve: /dev/disk/by-id/ata-CT500MX500SSD1_2213E621E335-part1 has errors (write 2)
- Storage: Safety (TrueNAS) 58% (+35.3 GB this week), full in about 9 weeks at this rate; bad1 (Proxmox host) 0%; bad2 (Proxmox host) 42% (+22.4 GB this week); protected (TrueNAS) 32%; rpool (Proxmox host) 45%; tank (TrueNAS) 93% (+225.1 GB this week); tank2 (TrueNAS) 49% (+49.5 GB this week), full in about 19 weeks at this rate; vm1 (Proxmox host) 16% (−69.4 GB this week); vm2 (Proxmox host) 33% (−133.2 GB this week); vm3 (Proxmox host) 5% (−1.5 GB this week)
- Library: 2 new movies (0 in 4K), 3 new episodes of 2 shows, 149 of 756 movies still without Latin American Spanish
- Docker images: 12 of 28 containers with a newer image waiting (hassio_observer, qbittorrent, bazarr, gluetun, prowlarr, …)
- Changes: 2 in the lab
- Incidents: 1 (OOM kill: llama-server in CT 137)

## Past weeks

| Week ending | Backups | Disks | Changes | Incidents |
|---|---|---|---|---|
| [Nov 22, 2026](2026-W47.md) | all 8 runs clean; 7 guests with no backup in 8 days | 2 problems this week: TrueNAS warning: homepage: API key has been revoked and mu | 22 in the lab | 5 (logrotate failed on monitoring (exit-code); OOM kill: a p |
| [Nov 15, 2026](2026-W46.md) | all 20 runs clean; 11 guests with no backup in 8 days | 3 problems this week: TrueNAS warning: homepage: API key has been revoked and mu | 21 in the lab | 6 (komga failed on komga (exit-code), and 2 other services; |
| [Nov 8, 2026](2026-W45.md) | all 7 runs clean; 11 guests with no backup in 8 days | 2 problems this week: TrueNAS warning: homepage: API key has been revoked and mu | 7 in the lab | 2 (bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae |

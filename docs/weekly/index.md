# Weekly reports

Every Sunday at 5:15 AM Jarvis writes up the lab's week: backups, disks, storage, the library, changes and incidents, and sends the note to your phone.

## This week so far

Since Sun Nov 8, 5:15 AM:

- Backups: all 6 runs clean; 11 guests with no backup in 8 days
- Disks: 3 problems this week: TrueNAS warning: homepage: API key has been revoked and must either be renewed or deleted. Revoke reason: Attempt to use over an insecure transport. Once the maintenance is complete, API client configuration must be u; ZFS pool bad2 on pve: /dev/disk/by-id/ata-CT500MX500SSD1_2213E621E335-part1 has errors (write 2)
- Storage: Safety (TrueNAS) 52% (+42.5 GB this week), full in about 11 weeks at this rate; bad1 (Proxmox host) 0%; bad2 (Proxmox host) 80% (+7.6 GB this week), full in about 3 weeks at this rate; protected (TrueNAS) 32%; rpool (Proxmox host) 45%; tank (TrueNAS) 92% (+26.2 GB this week); tank2 (TrueNAS) 48% (+358.2 GB this week), full in about 13 weeks at this rate; vm1 (Proxmox host) 23% (+7.8 GB this week); vm2 (Proxmox host) 45% (+15.5 GB this week), full in about 22 weeks at this rate; vm3 (Proxmox host) 5% (+2.7 GB this week)
- Library: 13 new movies (5 in 4K), 49 new episodes of 5 shows, 145 of 747 movies still without Latin American Spanish
- Docker images: 13 of 28 containers with a newer image waiting (hassio_observer, kometa, qbittorrent, patchmon-guacd-1, radarr, …); you updated 14 this week
- Changes: 2 in the lab
- Incidents: 4 (bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae36da3bf-52594ed44ecba93f failed on unifi-os-server (exit-code); bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae36da3bf-13c9ad3618030068 failed on unifi-os-server (exit-code); OOM kill: frigate.embeddi in CT 119)

## Past weeks

| Week ending | Backups | Disks | Changes | Incidents |
|---|---|---|---|---|
| [Nov 8, 2026](2026-W45.md) | all 7 runs clean; 11 guests with no backup in 8 days | 2 problems this week: TrueNAS warning: homepage: API key has been revoked and mu | 7 in the lab | 2 (bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae |

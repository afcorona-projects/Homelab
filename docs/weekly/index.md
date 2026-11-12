# Weekly reports

Every Sunday at 5:15 AM Jarvis writes up the lab's week: backups, disks, storage, the library, changes and incidents, and sends the note to your phone.

## This week so far

Since Sun Nov 8, 5:15 AM:

- Backups: all 4 runs clean; 11 guests with no backup in 8 days
- Disks: 3 problems this week: TrueNAS warning: homepage: API key has been revoked and must either be renewed or deleted. Revoke reason: Attempt to use over an insecure transport. Once the maintenance is complete, API client configuration must be u; ZFS pool bad2 on pve: /dev/disk/by-id/ata-CT500MX500SSD1_2213E621E335-part1 has errors (write 2)
- Storage: Safety (TrueNAS) 51% (+44 GB this week), full in about 11 weeks at this rate; bad1 (Proxmox host) 0%; bad2 (Proxmox host) 84% (+47.4 GB this week), full in about 1 weeks at this rate; protected (TrueNAS) 32% (+194.8 GB this week); rpool (Proxmox host) 45% (+1.2 GB this week); tank (TrueNAS) 92% (+27.2 GB this week); tank2 (TrueNAS) 48% (+1.1 TB this week), full in about 12 weeks at this rate; vm1 (Proxmox host) 23% (+5 GB this week); vm2 (Proxmox host) 45% (+92.1 GB this week), full in about 19 weeks at this rate; vm3 (Proxmox host) 5%
- Library: 13 new movies (5 in 4K), 41 new episodes of 4 shows, 145 of 747 movies still without Latin American Spanish
- Docker images: 12 of 28 containers with a newer image waiting (hassio_observer, kometa, qbittorrent, patchmon-guacd-1, radarr, …); you updated 12 this week
- Changes: 2 in the lab
- Incidents: 2 (OOM kill: frigate.embeddi in CT 119; llm failed on ai (exit-code))

## Past weeks

| Week ending | Backups | Disks | Changes | Incidents |
|---|---|---|---|---|
| [Nov 8, 2026](2026-W45.md) | all 7 runs clean; 11 guests with no backup in 8 days | 2 problems this week: TrueNAS warning: homepage: API key has been revoked and mu | 7 in the lab | 2 (bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae |

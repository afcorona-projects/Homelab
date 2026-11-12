# TrueNAS

TrueNAS 25.10.7 on truenas.

| Pool | Layout | Size | Used | Status |
|---|---|---|---|---|
| Safety | mirror of 2 | 899.3 GB | 51% | ONLINE |
| protected | raidz2 of 8 | 20.6 TB | 32% | ONLINE |
| tank | disk of 1 | 16.2 TB | 92% | ONLINE |
| tank2 | disk of 1 | 16.2 TB | 48% | ONLINE |

## Shares

| Kind | Name | Path | Notes |
|---|---|---|---|
| NFS | /mnt/protected/emulation | `/mnt/protected/emulation` |  |
| NFS | media | `/mnt/tank/media` |  |
| NFS | media2 | `/mnt/tank2/media` |  |
| SMB | emulation | `/mnt/protected/emulation` |  |
| SMB | media | `/mnt/tank/media` |  |
| SMB | media2 | `/mnt/tank2/media` |  |

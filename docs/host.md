# Proxmox host

## pve

| Setting | Now |
|---|---|
| Proxmox VE | 9.2.32 |
| Kernel | Linux 7.0.14-30-pve |
| CPU | AMD Ryzen 9 9950X 16-Core Processor, 32 threads, 64% in use |
| RAM | 38.0 GB used of 91.7 GB |
| Uptime | 4h 28m |

### ZFS pools

| Pool | Size | Used | Health |
|---|---|---|---|
| bad1 | 464 GB | 0% | ONLINE |
| bad2 | 464 GB | 44% | ONLINE |
| rpool | 460 GB | 45% | ONLINE |
| vm1 | 928 GB | 16% | ONLINE |
| vm2 | 928 GB | 34% | ONLINE |
| vm3 | 928 GB | 5% | ONLINE |

## Proxmox storage

| Storage | Type | Holds | Size | Used |
|---|---|---|---|---|
| bad1 | zfspool | rootdir, images | 449.6 GB | 0% |
| bad2 | zfspool | rootdir, images | 449.6 GB | 45% |
| local | dir | images, vztmpl, iso | 428.2 GB | 44% |
| pbs | pbs | backup | 899.1 GB | 60% |
| vm1 | zfspool | rootdir, images | 899.4 GB | 20% |
| vm2 | zfspool | images, rootdir | 899.3 GB | 51% |
| vm3 | zfspool | images, rootdir | 899.3 GB | 27% |

## Backup jobs

| Job | When | To | Covers | Notes |
|---|---|---|---|---|
| backup-3b30127f-7238 | 2:00 | pbs | 101,108,109,112,200,201,202 |  |

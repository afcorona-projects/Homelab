# Proxmox host

## pve

| Setting | Now |
|---|---|
| Proxmox VE | 9.2.25 |
| Kernel | Linux 7.0.14-26-pve |
| CPU | AMD Ryzen 9 9950X 16-Core Processor, 32 threads, 1% in use |
| RAM | 65.7 GB used of 91.7 GB |
| Uptime | 2d 18h |

### ZFS pools

| Pool | Size | Used | Health |
|---|---|---|---|
| bad1 | 464 GB | 0% | ONLINE |
| bad2 | 464 GB | 74% | ONLINE |
| rpool | 460 GB | 45% | ONLINE |
| vm1 | 928 GB | 22% | ONLINE |
| vm2 | 928 GB | 32% | ONLINE |
| vm3 | 928 GB | 5% | ONLINE |

## Proxmox storage

| Storage | Type | Holds | Size | Used |
|---|---|---|---|---|
| bad1 | zfspool | rootdir, images | 449.6 GB | 0% |
| bad2 | zfspool | images, rootdir | 449.6 GB | 76% |
| local | dir | images, iso, vztmpl | 430.6 GB | 44% |
| pbs | pbs | backup | 899.1 GB | 45% |
| vm1 | zfspool | rootdir, images | 899.7 GB | 27% |
| vm2 | zfspool | rootdir, images | 899.3 GB | 50% |
| vm3 | zfspool | rootdir, images | 899.3 GB | 27% |

## Backup jobs

| Job | When | To | Covers | Notes |
|---|---|---|---|---|
| backup-3b30127f-7238 | 2:00 | pbs | 101,107,108,109,110,111,112,113,200,201,202 |  |

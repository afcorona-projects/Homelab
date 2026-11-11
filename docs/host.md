# Proxmox host

## pve

| Setting | Now |
|---|---|
| Proxmox VE | 9.2.26 |
| Kernel | Linux 7.0.14-28-pve |
| CPU | AMD Ryzen 9 9950X 16-Core Processor, 32 threads, 4% in use |
| RAM | 73.5 GB used of 91.7 GB |
| Uptime | 3d 15h |

### ZFS pools

| Pool | Size | Used | Health |
|---|---|---|---|
| bad1 | 464 GB | 0% | ONLINE |
| bad2 | 464 GB | 84% | ONLINE |
| rpool | 460 GB | 45% | ONLINE |
| vm1 | 928 GB | 23% | ONLINE |
| vm2 | 928 GB | 45% | ONLINE |
| vm3 | 928 GB | 5% | ONLINE |

## Proxmox storage

| Storage | Type | Holds | Size | Used |
|---|---|---|---|---|
| bad1 | zfspool | rootdir, images | 449.6 GB | 0% |
| bad2 | zfspool | rootdir, images | 449.6 GB | 87% |
| local | dir | vztmpl, images, iso | 429.4 GB | 44% |
| pbs | pbs | backup | 899.1 GB | 50% |
| vm1 | zfspool | rootdir, images | 899.7 GB | 27% |
| vm2 | zfspool | images, rootdir | 899.3 GB | 63% |
| vm3 | zfspool | rootdir, images | 899.3 GB | 27% |

## Backup jobs

| Job | When | To | Covers | Notes |
|---|---|---|---|---|
| backup-3b30127f-7238 | 2:00 | pbs | 101,107,108,109,110,111,112,113,200,201,202 |  |

# Proxmox host

## pve

| Setting | Now |
|---|---|
| Proxmox VE | 9.2.27 |
| Kernel | Linux 7.0.14-29-pve |
| CPU | AMD Ryzen 9 9950X 16-Core Processor, 32 threads, 1% in use |
| RAM | 73.4 GB used of 91.7 GB |
| Uptime | 1d 22h |

### ZFS pools

| Pool | Size | Used | Health |
|---|---|---|---|
| bad1 | 464 GB | 0% | ONLINE |
| bad2 | 464 GB | 34% | ONLINE |
| rpool | 460 GB | 45% | ONLINE |
| vm1 | 928 GB | 19% | ONLINE |
| vm2 | 928 GB | 49% | ONLINE |
| vm3 | 928 GB | 5% | ONLINE |

## Proxmox storage

| Storage | Type | Holds | Size | Used |
|---|---|---|---|---|
| bad1 | zfspool | rootdir, images | 449.6 GB | 0% |
| bad2 | zfspool | rootdir, images | 449.6 GB | 35% |
| local | dir | vztmpl, iso, images | 428.5 GB | 44% |
| pbs | pbs | backup | 899.1 GB | 56% |
| vm1 | zfspool | images, rootdir | 899.4 GB | 24% |
| vm2 | zfspool | rootdir, images | 899.3 GB | 67% |
| vm3 | zfspool | images, rootdir | 899.3 GB | 27% |

## Backup jobs

| Job | When | To | Covers | Notes |
|---|---|---|---|---|
| backup-3b30127f-7238 | 2:00 | pbs | 101,108,109,112,200,201,202 |  |

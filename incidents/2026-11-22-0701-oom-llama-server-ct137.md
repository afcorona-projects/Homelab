# OOM kill: llama-server in CT 137

| What | Details |
|---|---|
| When | Nov 22, 2026 7:01 AM |
| Where | pve2 |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
6:54:44 AM [pve2 kernel] mce: [Hardware Error]: Machine check events logged
6:54:44 AM [pve2 kernel] [Hardware Error]: System Fatal error.
6:54:44 AM [pve2 kernel] [Hardware Error]: CPU:1 (19:21:2) MC12_STATUS[Over|UE|MiscV|AddrV|PCC|SyndV|UECC|Deferred|Poison|Scrub]: 0xffffffff8540b000
6:54:44 AM [pve2 kernel] [Hardware Error]: Error Addr: 0x0000000000000000
6:54:44 AM [pve2 kernel] [Hardware Error]: IPID: 0x0000000000000000, Syndrome: 0x0000000000000000
6:54:44 AM [pve2 kernel] [Hardware Error]: Bank 12 is reserved.
6:54:44 AM [pve2 kernel] [Hardware Error]: cache level: RESV, tx: INSN
7:01:57 AM [pve2 kernel] llama-server invoked oom-killer: gfp_mask=0xcc0(GFP_KERNEL), order=0, oom_score_adj=0
7:01:57 AM [pve2 kernel] oom-kill:constraint=CONSTRAINT_MEMCG,nodemask=(null),cpuset=ns,mems_allowed=0,oom_memcg=/lxc/137,task_memcg=/lxc/137/ns/system.slice/llama-server.service,task=llama-server,pid=308949,uid=100000
7:01:57 AM [pve2 kernel] Memory cgroup out of memory: Killed process 308949 (llama-server) total-vm:52192828kB, anon-rss:4070136kB, file-rss:69176kB, shmem-rss:137328kB, UID:100000 pgtables:11544kB oom_score_adj:0
```

## Likely cause

Likely the llama-server process on pve2 was terminated by the kernel oom-killer because it ran out of memory. This event occurred about seven minutes after a hardware error was logged on pve2, but the memory exhaustion is the direct cause of the llama-server crash.

<small>Jarvis's draft from the timeline.</small>

## Impact

Whatever runs on pve2.

## What fixed it

_Not written up yet._

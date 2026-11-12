# OOM kill: frigate.embeddi in CT 119

| What | Details |
|---|---|
| When | Nov 11, 2026 8:40 AM – 8:41 AM |
| Where | CT 119 frigate |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
8:30:26 AM [pve kernel] audit: type=1400 audit(1794414626.779:51088): apparmor="DENIED" operation="sendmsg" class="file" namespace="root//lxc-108_<-var-lib-lxc>" profile="rsyslogd" name="/run/systemd/journal/dev-log" pid=555978 comm="systemd-jo (×117)
8:40:26 AM [pve kernel] python3 invoked oom-killer: gfp_mask=0x100cca(GFP_HIGHUSER_MOVABLE), order=0, oom_score_adj=0
8:40:26 AM [frigate init.scope] frigate.service: A process of this unit has been killed by the OOM killer.
8:40:26 AM [pve kernel] oom-kill:constraint=CONSTRAINT_MEMCG,nodemask=(null),cpuset=ns,mems_allowed=0,oom_memcg=/lxc/119,task_memcg=/lxc/119/ns/system.slice/frigate.service,task=frigate.embeddi,pid=5773,uid=0
8:40:26 AM [pve kernel] Memory cgroup out of memory: Killed process 5773 (frigate.embeddi) total-vm:9942444kB, anon-rss:3980704kB, file-rss:8kB, shmem-rss:8kB, UID:0 pgtables:10712kB oom_score_adj:0
8:41:56 AM [frigate init.scope] frigate.service: State 'final-sigterm' timed out. Killing.
8:41:56 AM [frigate init.scope] frigate.service: Failed with result 'oom-kill'.
```

## Likely cause

Likely the frigate.embeddi process within CT 119 consumed excessive memory, triggering the kernel oom-killer to terminate it. This out-of-memory event caused the frigate.service to fail and eventually be killed after its stop timeout expired.

<small>Jarvis's draft from the timeline.</small>

## Impact

Services on CT 119 frigate: Frigate.

## What fixed it

_Not written up yet._

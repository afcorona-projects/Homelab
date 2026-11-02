# OOM kill: frigate.capture in CT 119

| What | Details |
|---|---|
| When | Oct 28, 2026 12:02 PM |
| Where | CT 119 frigate |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
11:52:24 AM [pve kernel] audit: type=1400 audit(1793213544.499:45149): apparmor="DENIED" operation="sendmsg" class="file" namespace="root//lxc-121_<-var-lib-lxc>" profile="rsyslogd" name="/run/systemd/journal/dev-log" pid=3093687 comm="systemd-j (×87)
12:02:01 PM [pve kernel] mux0:segment invoked oom-killer: gfp_mask=0xcc0(GFP_KERNEL), order=0, oom_score_adj=0
12:02:01 PM [frigate init.scope] frigate.service: A process of this unit has been killed by the OOM killer.
12:02:01 PM [pve kernel] oom-kill:constraint=CONSTRAINT_MEMCG,nodemask=(null),cpuset=ns,mems_allowed=0,oom_memcg=/lxc/119,task_memcg=/lxc/119/ns/system.slice/frigate.service,task=frigate.capture,pid=3227795,uid=0
12:02:01 PM [pve kernel] Memory cgroup out of memory: Killed process 3227795 (frigate.capture) total-vm:1851580kB, anon-rss:134904kB, file-rss:8376kB, shmem-rss:135028kB, UID:0 pgtables:956kB oom_score_adj:0
12:02:01 PM [frigate init.scope] frigate.service: Failed with result 'oom-kill'.
12:02:02 PM [frigate init.scope] system.slice: A process of this unit has been killed by the OOM killer.
```

## Likely cause

Likely the frigate.service in CT 119 consumed too much memory, causing the OOM killer to terminate the frigate.capture process. This resulted in the frigate.service failing with an oom-kill status as the container ran out of available RAM and swap.

<small>Jarvis's draft from the timeline.</small>

## Impact

Services on CT 119 frigate: Frigate.

## What fixed it

_Not written up yet._

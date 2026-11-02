# OOM kill: frigate.capture in CT 119

| What | Details |
|---|---|
| When | Oct 28, 2026 1:03 PM |
| Where | CT 119 frigate |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
12:54:24 PM [pve kernel] audit: type=1400 audit(1793217264.504:45456): apparmor="DENIED" operation="sendmsg" class="file" namespace="root//lxc-121_<-var-lib-lxc>" profile="rsyslogd" name="/run/systemd/journal/dev-log" pid=3093687 comm="systemd-j (×85)
1:03:30 PM [pve kernel] mux0:segment invoked oom-killer: gfp_mask=0xcc0(GFP_KERNEL), order=0, oom_score_adj=0
1:03:30 PM [frigate init.scope] frigate.service: A process of this unit has been killed by the OOM killer.
1:03:30 PM [pve kernel] oom-kill:constraint=CONSTRAINT_MEMCG,nodemask=(null),cpuset=ns,mems_allowed=0,oom_memcg=/lxc/119,task_memcg=/lxc/119/ns/system.slice/frigate.service,task=frigate.capture,pid=3375986,uid=0
1:03:30 PM [pve kernel] Memory cgroup out of memory: Killed process 3375986 (frigate.capture) total-vm:1852604kB, anon-rss:134920kB, file-rss:8388kB, shmem-rss:135028kB, UID:0 pgtables:960kB oom_score_adj:0
1:03:30 PM [frigate init.scope] frigate.service: Failed with result 'oom-kill'.
```

## Likely cause

Likely the frigate.service in CT 119 exhausted its allocated 6 GB RAM and 512 MB swap, triggering the oom-killer to terminate the frigate.capture process. This memory exhaustion caused the frigate.service to fail with an oom-kill result.

<small>Jarvis's draft from the timeline.</small>

## Impact

Services on CT 119 frigate: Frigate.

## What fixed it

_Not written up yet._

# OOM kill: frigate.capture in CT 119

| What | Details |
|---|---|
| When | Oct 28, 2026 2:04 PM |
| Where | CT 119 frigate |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
1:55:01 PM [pve kernel] audit: type=1400 audit(1793220901.040:45831): apparmor="DENIED" operation="sendmsg" class="file" namespace="root//lxc-108_<-var-lib-lxc>" profile="rsyslogd" name="/run/systemd/journal/dev-log" pid=3087238 comm="systemd-j (×85)
2:04:57 PM [pve kernel] mux0:segment invoked oom-killer: gfp_mask=0xcc0(GFP_KERNEL), order=0, oom_score_adj=0
2:04:57 PM [frigate init.scope] frigate.service: A process of this unit has been killed by the OOM killer.
2:04:57 PM [pve kernel] oom-kill:constraint=CONSTRAINT_MEMCG,nodemask=(null),cpuset=ns,mems_allowed=0,oom_memcg=/lxc/119,task_memcg=/lxc/119/ns/system.slice/frigate.service,task=frigate.capture,pid=3523339,uid=0
2:04:57 PM [pve kernel] Memory cgroup out of memory: Killed process 3523339 (frigate.capture) total-vm:1852604kB, anon-rss:134844kB, file-rss:8420kB, shmem-rss:135028kB, UID:0 pgtables:960kB oom_score_adj:0
2:04:57 PM [frigate init.scope] frigate.service: Failed with result 'oom-kill'.
```

## Likely cause

Likely the frigate service in CT 119 consumed all available memory, triggering the kernel oom-killer to terminate the frigate.capture process. This occurred because the container had only 6 GB of RAM and limited swap space, which was insufficient for the workload. The audit denial for rsyslogd is unrelated to the crash and likely stems from AppArmor restrictions on logging access.

<small>Jarvis's draft from the timeline.</small>

## Impact

Services on CT 119 frigate: Frigate.

## What fixed it

_Not written up yet._

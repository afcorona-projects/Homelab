# OOM kill: frigate.capture in CT 119

| What | Details |
|---|---|
| When | Oct 28, 2026 3:06 PM – 3:12 PM |
| Where | CT 119 frigate |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
2:56:24 PM [pve kernel] audit: type=1400 audit(1793224584.517:46138): apparmor="DENIED" operation="sendmsg" class="file" namespace="root//lxc-121_<-var-lib-lxc>" profile="rsyslogd" name="/run/systemd/journal/dev-log" pid=3093687 comm="systemd-j (×112)
3:06:07 PM [pve kernel] go2rtc invoked oom-killer: gfp_mask=0xcc0(GFP_KERNEL), order=3, oom_score_adj=0
3:06:07 PM [frigate init.scope] frigate.service: A process of this unit has been killed by the OOM killer.
3:06:07 PM [pve kernel] oom-kill:constraint=CONSTRAINT_MEMCG,nodemask=(null),cpuset=ns,mems_allowed=0,oom_memcg=/lxc/119,task_memcg=/lxc/119/ns/system.slice/frigate.service,task=frigate.capture,pid=3671392,uid=0
3:06:07 PM [pve kernel] Memory cgroup out of memory: Killed process 3671392 (frigate.capture) total-vm:1852604kB, anon-rss:134848kB, file-rss:8516kB, shmem-rss:135028kB, UID:0 pgtables:956kB oom_score_adj:0
3:06:07 PM [frigate init.scope] frigate.service: Failed with result 'oom-kill'.
3:12:39 PM [frigate alloy] ts=2026-10-28T22:12:39.442696669Z level=info msg="node exited without error" controller_id="" node=labelstore
3:12:39 PM [frigate alloy] ts=2026-10-28T22:12:39.443195131Z level=info msg="node exited without error" controller_id="" node=otel
3:12:39 PM [frigate alloy] ts=2026-10-28T22:12:39.443836474Z level=info msg="node exited without error" controller_id="" node=cluster
3:12:39 PM [frigate alloy] ts=2026-10-28T22:12:39.443854554Z level=info msg="node exited without error" controller_id="" node=ui
3:12:39 PM [frigate alloy] ts=2026-10-28T22:12:39.445017209Z level=info msg="node exited without error" controller_id="" node=http
3:12:39 PM [frigate alloy] ts=2026-10-28T22:12:39.44504389Z level=info msg="node exited without error" controller_id="" node=remotecfg
3:12:39 PM [frigate alloy] ts=2026-10-28T22:12:39.44505532Z level=info msg="node exited without error" controller_id="" node=livedebugging
3:12:39 PM [frigate init.scope] user-0.slice: A process of this unit has been killed by the OOM killer.
3:12:39 PM [frigate init.scope] user.slice: A process of this unit has been killed by the OOM killer.
3:12:39 PM [frigate alloy] ts=2026-10-28T22:12:39.546055621Z level=info msg="node exited without error" controller_id="" node=loki.source.journal.system
3:12:39 PM [frigate alloy] ts=2026-10-28T22:12:39.546120391Z level=info msg="node exited without error" controller_id="" node=loki.write.loki
3:12:39 PM [frigate alloy] ts=2026-10-28T22:12:39.546141661Z level=info msg="node exited without error" controller_id="" node=loki.relabel.journal
3:12:42 PM [frigate container-getty@1] pam_systemd(login:session): Failed to create session: Seat has no VTs but VT number not 0
```

## Likely cause

Likely the frigate.capture process in container 119 exhausted the available memory and swap, triggering the oom-killer to terminate it. This memory exhaustion also caused the OOM killer to terminate other processes in the container, leading to the shutdown of the frigate service and its associated alloy nodes.

<small>Jarvis's draft from the timeline.</small>

## Impact

Services on CT 119 frigate: Frigate.

## What fixed it

_Not written up yet._

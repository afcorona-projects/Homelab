# pve-cluster failed on pve (timeout), and 1 other service

| What | Details |
|---|---|
| When | Oct 28, 2026 10:01 AM – 10:03 AM |
| Where | CT 114 komga |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
9:52:24 AM [pve kernel] audit: type=1400 audit(1793206344.471:43079): apparmor="DENIED" operation="sendmsg" class="file" namespace="root//lxc-121_<-var-lib-lxc>" profile="rsyslogd" name="/run/systemd/journal/dev-log" pid=47751 comm="systemd-jou (×107)
10:01:03 AM [pve alloy] ts=2026-10-28T17:01:03.865692359Z level=info msg="node exited without error" controller_id="" node=labelstore
10:01:03 AM [pve alloy] ts=2026-10-28T17:01:03.86603428Z level=info msg="node exited without error" controller_id="" node=ui
10:01:03 AM [pve alloy] ts=2026-10-28T17:01:03.86603222Z level=info msg="node exited without error" controller_id="" node=otel
10:01:03 AM [pve alloy] ts=2026-10-28T17:01:03.86603337Z level=info msg="node exited without error" controller_id="" node=livedebugging
10:01:03 AM [pve alloy] ts=2026-10-28T17:01:03.885417025Z level=info msg="node exited without error" controller_id="" node=cluster
10:01:03 AM [pve alloy] ts=2026-10-28T17:01:03.887650035Z level=info msg="node exited without error" controller_id="" node=http
10:01:03 AM [pve alloy] ts=2026-10-28T17:01:03.888231208Z level=info msg="node exited without error" controller_id="" node=remotecfg
10:01:03 AM [pve alloy] ts=2026-10-28T17:01:03.97106889Z level=info msg="node exited without error" controller_id="" node=loki.source.journal.host
10:01:03 AM [pve alloy] ts=2026-10-28T17:01:03.971747813Z level=info msg="node exited without error" controller_id="" node=loki.relabel.journal
10:01:03 AM [pve alloy] ts=2026-10-28T17:01:03.973613331Z level=info msg="node exited without error" controller_id="" node=loki.write.default
10:01:41 AM [pve init.scope] pve-cluster.service: State 'stop-sigterm' timed out. Killing.
10:01:41 AM [pve init.scope] pve-cluster.service: Main process exited, code=killed, status=9/KILL
10:01:41 AM [pve init.scope] pve-cluster.service: Failed with result 'timeout'.
10:03:59 AM [komga alloy] ts=2026-10-28T17:03:59.411770322Z level=info msg="node exited without error" controller_id="" node=labelstore
10:03:59 AM [komga alloy] ts=2026-10-28T17:03:59.426911458Z level=info msg="node exited without error" controller_id="" node=otel
10:03:59 AM [komga init.scope] Failed unmounting mnt-media.mount - /mnt/media.
10:03:59 AM [komga alloy] ts=2026-10-28T17:03:59.359488113Z level=info msg="node exited without error" controller_id="" node=ui
10:03:59 AM [komga alloy] ts=2026-10-28T17:03:59.444213314Z level=info msg="node exited without error" controller_id="" node=livedebugging
10:03:59 AM [komga alloy] ts=2026-10-28T17:03:59.486449118Z level=info msg="node exited without error" controller_id="" node=cluster
10:03:59 AM [komga alloy] ts=2026-10-28T17:03:59.489724313Z level=info msg="node exited without error" controller_id="" node=http
10:03:59 AM [komga alloy] ts=2026-10-28T17:03:59.490276465Z level=info msg="node exited without error" controller_id="" node=remotecfg
10:03:59 AM [komga alloy] ts=2026-10-28T17:03:59.531603146Z level=info msg="node exited without error" controller_id="" node=loki.source.journal.system
10:03:59 AM [komga alloy] ts=2026-10-28T17:03:59.53260151Z level=info msg="node exited without error" controller_id="" node=loki.write.loki
10:03:59 AM [komga alloy] ts=2026-10-28T17:03:59.533084093Z level=info msg="node exited without error" controller_id="" node=loki.relabel.journal
… and 2 other kinds of lines (the logs tool or Grafana has them all)
```

## Likely cause

Likely the system was shutting down or rebooting, causing pve-cluster.service to be forcibly killed after timing out and komga's alloy process to exit cleanly. The failed unmount of mnt-media.mount on the komga container suggests the shutdown sequence interrupted active I/O operations.

<small>Jarvis's draft from the timeline.</small>

## Impact

Services on CT 114 komga: Komga.

## What fixed it

_Not written up yet._

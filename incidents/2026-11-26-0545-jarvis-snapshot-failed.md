# jarvis-snapshot failed on pve (exit-code)

| What | Details |
|---|---|
| When | Nov 26, 2026 5:45 AM |
| Where | pve |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
5:45:27 AM [pve init.scope] jarvis-snapshot.service: Failed with result 'exit-code'.
5:45:27 AM [pve init.scope] Failed to start jarvis-snapshot.service - Jarvis snapshot: commit Jarvis's own code to the private repo (Jarvis 4.0 A3).
5:48:22 AM [pve kernel] audit: type=1400 audit(1795700902.380:397): apparmor="DENIED" operation="change_onexec" class="file" info="label not found" error=-2 namespace="root//lxc-134_<-var-lib-lxc>" profile="unconfined" name="ubuntu_pro_apt_news (×2)
```

## Likely cause

Likely the jarvis-snapshot.service failed because it exited with an error code, and a subsequent AppArmor denial prevented the ubuntuproaptnews process from modifying its executable within the lxc-134 container. The root cause is the missing security label required by the unconfined profile, which stopped the service from completing its code commit task.

<small>Jarvis's draft from the timeline.</small>

## Impact

Whatever runs on pve.

## What fixed it

_Not written up yet._

# jarvis-snapshot failed on pve (exit-code)

| What | Details |
|---|---|
| When | Nov 27, 2026 5:45 AM |
| Where | pve |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
5:45:30 AM [pve init.scope] jarvis-snapshot.service: Failed with result 'exit-code'.
5:45:30 AM [pve init.scope] Failed to start jarvis-snapshot.service - Jarvis snapshot: commit Jarvis's own code to the private repo (Jarvis 4.0 A3).
5:48:22 AM [pve kernel] audit: type=1400 audit(1795787302.373:568): apparmor="DENIED" operation="change_onexec" class="file" info="label not found" error=-2 namespace="root//lxc-134_<-var-lib-lxc>" profile="unconfined" name="ubuntu_pro_apt_news (×2)
```

## Likely cause

Likely the jarvis-snapshot.service failed because its execution was blocked by an AppArmor denial in the unconfined namespace associated with the lxc-134 container running ubuntuproaptnews. The system rejected the changeonexec operation because the required security label was not found, preventing the service from proceeding with its commit task.

<small>Jarvis's draft from the timeline.</small>

## Impact

Whatever runs on pve.

## What fixed it

_Not written up yet._

# pve-cluster failed on pve2 (timeout)

| What | Details |
|---|---|
| When | Nov 20, 2026 10:24 PM |
| Where | pve2 |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
10:24:24 PM [pve2 init.scope] pve-cluster.service: State 'stop-sigterm' timed out. Killing.
10:24:24 PM [pve2 init.scope] pve-cluster.service: Main process exited, code=killed, status=9/KILL
10:24:24 PM [pve2 init.scope] pve-cluster.service: Failed with result 'timeout'.
```

## Likely cause

Likely the pve-cluster.service on machine pve2 failed to stop gracefully and was forcibly terminated by the init system. The service entered a stop-sigterm state that timed out, causing the main process to be killed with signal 9.

<small>Jarvis's draft from the timeline.</small>

## Impact

Whatever runs on pve2.

## What fixed it

_Not written up yet._

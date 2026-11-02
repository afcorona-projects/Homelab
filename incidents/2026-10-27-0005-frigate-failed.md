# frigate failed on frigate (timeout)

| What | Details |
|---|---|
| When | Oct 27, 2026 12:05 AM |
| Where | CT 119 frigate |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
12:05:27 AM [frigate init.scope] frigate.service: State 'final-sigterm' timed out. Killing.
12:05:27 AM [frigate init.scope] frigate.service: Failed with result 'timeout'.
```

## Likely cause

Likely the frigate service on CT 119 failed to stop gracefully within the allotted time, causing systemd to force kill it. This timeout occurred during the final-sigterm state, resulting in the service failing with a timeout result.

<small>Jarvis's draft from the timeline.</small>

## Impact

Services on CT 119 frigate: Frigate.

## What fixed it

_Not written up yet._

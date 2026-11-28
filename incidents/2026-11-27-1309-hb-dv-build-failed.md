# hb-dv-build failed on encoder (exit-code)

| What | Details |
|---|---|
| When | Nov 27, 2026 1:09 PM |
| Where | CT 103 Encoder |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
1:09:54 PM [encoder hb-dv-build] mkdir: cannot create directory ‘/scratch/hb-build’: Permission denied
1:09:54 PM [encoder init.scope] hb-dv-build.service: Main process exited, code=exited, status=1/FAILURE
1:09:54 PM [encoder init.scope] hb-dv-build.service: Failed with result 'exit-code'.
```

## Likely cause

Likely the hb-dv-build service failed because the encoder container is running with an LXC ID map that restricts user and group IDs, preventing the process from creating the /scratch/hb-build directory. The permission denied error occurs because the container's internal user does not have write access to the host path under the current ID mapping configuration.

<small>Jarvis's draft from the timeline.</small>

## Impact

Whatever runs on CT 103 Encoder.

## What fixed it

_Not written up yet._

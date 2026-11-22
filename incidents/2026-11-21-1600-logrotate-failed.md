# logrotate failed on monitoring (exit-code)

| What | Details |
|---|---|
| When | Nov 21, 2026 4:00 PM |
| Where | monitoring |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
4:00:11 PM [monitoring] Failed to kill unit rsyslog.service: Unit rsyslog.service not loaded.
4:00:11 PM [monitoring] error: error running shared postrotate script for '/var/log/syslog
4:00:11 PM [monitoring] logrotate.service: Main process exited, code=exited, status=1/FAILURE
4:00:11 PM [monitoring] logrotate.service: Failed with result 'exit-code'.
4:00:11 PM [monitoring] Failed to start logrotate.service - Rotate log files.
```

## Likely cause

Likely the logrotate service failed because it could not execute its postrotate script, which required the rsyslog service to be active but was not loaded at the time. This caused the logrotate process to exit with an error status and prevented the scheduled rotation of the /var/log/syslog file.

<small>Jarvis's draft from the timeline.</small>

## Impact

Whatever runs on monitoring.

## What fixed it

_Not written up yet._

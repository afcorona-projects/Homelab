# scrypted failed on scrypted (exit-code)

| What | Details |
|---|---|
| When | Nov 25, 2026 4:31 AM |
| Where | CT 134 scrypted |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
4:31:35 AM [scrypted docker] time="2026-11-25T12:31:35.384968421Z" level=info msg="stopping event stream following graceful shutdown" error="grpc: the client connection is closing: context canceled" module=libcontainerd namespace=moby
4:31:35 AM [scrypted docker] time="2026-11-25T12:31:35.393306461Z" level=info msg="stopping event stream following graceful shutdown" error="context canceled" module=libcontainerd namespace=plugins.moby
4:31:35 AM [scrypted init.scope] scrypted.service: Main process exited, code=exited, status=1/FAILURE
4:31:35 AM [scrypted init.scope] scrypted.service: Failed with result 'exit-code'.
4:31:36 AM [scrypted docker] time="2026-11-25T12:31:36.021222636Z" level=info msg="Creating a containerd client" address=/run/containerd/containerd.sock timeout=1m0s
4:31:36 AM [scrypted docker] time="2026-11-25T12:31:36.021984271Z" level=warning msg="failed check for fsverity support" error="enable fsverity failed: inappropriate ioctl for device" path=/var/lib/docker/plugins/storage (×2)
4:31:36 AM [scrypted docker] time="2026-11-25T12:31:36.103913402Z" level=info msg="Deleting nftables IPv4 rules" error="running nft: /dev/stdin:1:17-30: Error: Could not process rule: No such file or directory\ndelete table ip docker-bridges\n ^^^^^ (×2)
```

## Likely cause

Likely the scrypted service failed because the containerd client could not establish a connection or the nftables rules deletion encountered a missing file, causing the service to exit with status 1. The warning about fsverity and the error regarding the nftables rule suggest that Docker or the underlying container runtime encountered issues with the storage device or network rules on the scrypted machine, preventing it from starting successfully.

<small>Jarvis's draft from the timeline.</small>

## Impact

Whatever runs on CT 134 scrypted.

## What fixed it

_Not written up yet._

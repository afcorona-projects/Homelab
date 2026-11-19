# jarvis-docs-caddy failed on pve (exit-code), and 1 other service

| What | Details |
|---|---|
| When | Nov 18, 2026 6:53 AM – 6:55 AM |
| Where | CT 120 unifi-os-server |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
6:53:04 AM [pve kernel] RAS: Correctable Errors collector initialized.
6:53:04 AM [pve kernel] gasket: module verification failed: signature and/or required key missing - tainting kernel
6:53:04 AM [pve] Failed to find module 'vfio_virqfd'
6:53:04 AM [pve kernel] faux_driver regulatory: Direct firmware load for regulatory.db failed with error -2
6:53:04 AM [pve kernel] cfg80211: failed to load regulatory.db
6:53:04 AM [pve kernel] i915 0000:03:00.0: [drm] Registered 4 planes with drm panic
6:53:05 AM [pve kernel] ath12k_wifi7_pci 0000:0b:00.0: failed to initialize qmi handle (×6)
6:53:05 AM [pve kernel] ath12k_wifi7_pci 0000:0b:00.0: failed to initialize qmi :-517 (×9)
6:53:05 AM [pve kernel] ath12k_wifi7_pci 0000:0b:00.0: failed to create soc 0 core: -517 (×9)
6:53:05 AM [pve kernel] ath12k_wifi7_pci 0000:0b:00.0: failed to init core: -517 (×9)
6:53:05 AM [pve kernel] amdgpu 0000:7c:00.0: [drm] Registered 4 planes with drm panic
6:53:05 AM [pve kernel] mei i915.mei-gscfi.768-e2c2afa2-3817-4d19-9d95-06b16b588a5d: FW version command failed -5
6:53:12 AM [pve init.scope] Started earlyoom.service - Early OOM Daemon.
6:53:12 AM [pve nfs-blkmap] open pipe file /run/rpc_pipefs/nfs/blocklayout failed: No such file or directory
6:53:14 AM [pve init.scope] jarvis-docs-caddy.service: Main process exited, code=exited, status=255/EXCEPTION
6:53:14 AM [pve init.scope] jarvis-docs-caddy.service: Failed with result 'exit-code'.
6:53:14 AM [pve init.scope] Failed to start jarvis-docs-caddy.service - Copy Caddy's Caddyfile into Jarvis for Jarvis Docs.
6:53:42 AM [pve netavark-dhcp-proxy] timeout met: exiting after 30 secs of inactivity
6:55:24 AM [unifi-os-server uosserver-updater] ERROR Failed to remove /run/uosserver-updater.sock No such file or directory (os error 2)
6:55:36 AM [unifi-os-server uosserver] INFO Waiting for container 'uosserver' to start (timeout: 60s)
6:55:37 AM [unifi-os-server user@1000] bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae36da3bf-7764c6257c6e41d5.service: Main process exited, code=exited, status=1/FAILURE
6:55:37 AM [unifi-os-server user@1000] bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae36da3bf-7764c6257c6e41d5.service: Failed with result 'exit-code'.
6:55:39 AM [unifi-os-server user@1000] Flow 5 (UDP flow): Can't propagate ICMP error from SPLICE unifi-os-server:0 to HOST 127.0.0.1 (×7)
6:55:39 AM [unifi-os-server uosserver] INFO Waiting for systemd to be ready (timeout: 60s)
6:55:54 AM [unifi-os-server netavark-dhcp-proxy] timeout met: exiting after 30 secs of inactivity
```

## Likely cause

Likely the unifi-os-server container failed to start because its required systemd services, such as uosserver-updater and the user service, exited with errors or timeouts during initialization. The netavark-dhcp-proxy also timed out due to inactivity, indicating the container environment was not ready to handle network configuration. These combined service failures prevented the container from reaching a stable running state.

<small>Jarvis's draft from the timeline.</small>

## Impact

Services on CT 120 unifi-os-server: UniFi OS.

## What fixed it

_Not written up yet._

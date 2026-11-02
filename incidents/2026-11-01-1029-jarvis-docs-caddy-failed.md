# jarvis-docs-caddy failed on pve (exit-code), and 1 other service

| What | Details |
|---|---|
| When | Nov 01, 2026 10:29 AM – 10:31 AM |
| Where | CT 120 unifi-os-server |
| Found by | Jarvis Docs' nightly scan of Loki for OOM kills and failed services |

## Timeline

```text
10:29:02 AM [pve kernel] RAS: Correctable Errors collector initialized.
10:29:02 AM [pve kernel] gasket: module verification failed: signature and/or required key missing - tainting kernel
10:29:02 AM [pve] Failed to find module 'vfio_virqfd'
10:29:02 AM [pve kernel] bluetooth hci0: Direct firmware load for qca/rampatch_usb_00190200.bin failed with error -2
10:29:02 AM [pve kernel] Bluetooth: hci0: failed to request rampatch file: qca/rampatch_usb_00190200.bin (-2)
10:29:03 AM [pve kernel] i915 0000:03:00.0: [drm] Registered 4 planes with drm panic
10:29:03 AM [pve kernel] faux_driver regulatory: Direct firmware load for regulatory.db failed with error -2
10:29:03 AM [pve kernel] cfg80211: failed to load regulatory.db
10:29:03 AM [pve kernel] amdgpu 0000:7c:00.0: [drm] Registered 4 planes with drm panic
10:29:03 AM [pve kernel] ath12k_wifi7_pci 0000:0b:00.0: failed to initialize qmi handle (×8)
10:29:03 AM [pve kernel] ath12k_wifi7_pci 0000:0b:00.0: failed to initialize qmi :-517 (×12)
10:29:03 AM [pve kernel] ath12k_wifi7_pci 0000:0b:00.0: failed to create soc 0 core: -517 (×12)
10:29:03 AM [pve kernel] ath12k_wifi7_pci 0000:0b:00.0: failed to init core: -517 (×12)
10:29:11 AM [pve nfs-blkmap] open pipe file /run/rpc_pipefs/nfs/blocklayout failed: No such file or directory
10:29:12 AM [pve init.scope] jarvis-docs-caddy.service: Main process exited, code=exited, status=255/EXCEPTION
10:29:12 AM [pve init.scope] jarvis-docs-caddy.service: Failed with result 'exit-code'.
10:29:12 AM [pve init.scope] Failed to start jarvis-docs-caddy.service - Copy Caddy's Caddyfile into Jarvis for Jarvis Docs.
10:29:41 AM [pve netavark-dhcp-proxy] timeout met: exiting after 30 secs of inactivity
10:31:25 AM [unifi-os-server uosserver-updater] ERROR Failed to remove /run/uosserver-updater.sock No such file or directory (os error 2)
10:31:27 AM [pve kernel] audit: type=1400 audit(1793557887.920:549): apparmor="DENIED" operation="sendmsg" class="file" namespace="root//lxc-109_<-var-lib-lxc>" profile="rsyslogd" name="/run/systemd/journal/dev-log" pid=16162 comm="systemd-journ (×62)
10:31:45 AM [unifi-os-server uosserver] INFO Waiting for container 'uosserver' to start (timeout: 60s)
10:31:48 AM [unifi-os-server user@1000] bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae36da3bf-13c02b4ac5978155.service: Main process exited, code=exited, status=1/FAILURE
10:31:48 AM [unifi-os-server user@1000] bd6890ba914464281443b114c638d97ba040751c5d0b168cdcdec79ae36da3bf-13c02b4ac5978155.service: Failed with result 'exit-code'.
10:31:48 AM [unifi-os-server user@1000] Flow 1 (UDP flow): Can't propagate ICMP error from SPLICE unifi-os-server:0 to HOST 127.0.0.1 (×17)
10:31:50 AM [unifi-os-server uosserver] INFO Waiting for systemd to be ready (timeout: 60s)
… and 1 other kinds of lines (the logs tool or Grafana has them all)
```

## Likely cause

Likely the unifi-os-server container failed to start because the uosserver service encountered an error removing its socket file and subsequently timed out waiting for systemd to become ready. This startup failure was compounded by network flow propagation errors and AppArmor denials for rsyslogd, preventing the service from initializing correctly.

<small>Jarvis's draft from the timeline.</small>

## Impact

Services on CT 120 unifi-os-server: UniFi OS.

## What fixed it

_Not written up yet._

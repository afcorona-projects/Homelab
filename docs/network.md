# Network and routes

Caddy (CT 101) sites, from the copy of its Caddyfile taken Nov 09, 2026 5:10 AM.

```mermaid
flowchart LR
  caddy(["Caddy · CT 101"])
  njf_example_com["jf.example.com"] --> caddy
  caddy --> njellyfin_8096["CT 109 jellyfin<br/>jellyfin:8096"]
  nha_example_com["ha.example.com"] --> caddy
  caddy --> nha_80["VM 203 ha<br/>ha:80"]
  nfrigate_example_com["frigate.example.com"] --> caddy
  caddy --> nfrigate_8971["CT 119 frigate<br/>frigate:8971"]
  njarvis_example_com["jarvis.example.com"] --> caddy
  caddy --> nopenwebui_8080["CT 130 openwebui<br/>openwebui:8080"]
  nprr_example_com["prr.example.com"] --> caddy
  caddy --> nplex_seerr_5055["CT 107 plex-seerr<br/>plex-seerr:5055"]
  ndocs_example_com["docs.example.com"] --> caddy
  caddy --> nforgejo_80["CT 135 forgejo<br/>forgejo:80"]
```

| Name | Goes to | Machine | Notes |
|---|---|---|---|
| jf.example.com | jellyfin:8096 | [CT 109 jellyfin](guests/ct-109.md) |  |
| ha.example.com | ha:80 | [VM 203 ha](guests/vm-203.md) | home only, DNS challenge |
| frigate.example.com | frigate:8971 | [CT 119 frigate](guests/ct-119.md) | home only, DNS challenge |
| jarvis.example.com | openwebui:8080 | [CT 130 openwebui](guests/ct-130.md) | home only, DNS challenge |
| prr.example.com | plex-seerr:5055 | [CT 107 plex-seerr](guests/ct-107.md) |  |
| docs.example.com | forgejo:80 | [CT 135 forgejo](guests/ct-135.md) | home only, DNS challenge |

DNS overrides aren't documented yet: OPNsense isn't set up yet (OPNSENSE_URL, OPNSENSE_KEY and OPNSENSE_SECRET are empty).

## Uptime Kuma monitors

| Monitor | Address | Status | Machine |
|---|---|---|---|
| bazarr | http://arr:6767 | up | [VM 200 arr](guests/vm-200.md) |
| ErsatzTV | http://ersatztv:8409 | up | [CT 124 ersatztv](guests/ct-124.md) |
| Frigate | http://frigate:5000 | up | [CT 119 frigate](guests/ct-119.md) |
| Grafana | http://monitoring:3000 | up | [CT 121 Monitoring](guests/ct-121.md) |
| Home Assistant | http://ha | up | [VM 203 ha](guests/vm-203.md) |
| Jarvis bot Discord | http://debian:8099/health | up | [CT 136 debian](guests/ct-136.md) |
| jarvis-mcp | http://jarvis:8000/health | up | [CT 131 jarvis](guests/ct-131.md) |
| Jellyfin | http://jellyfin:8096 | up | [CT 109 jellyfin](guests/ct-109.md) |
| Jellyseerr | http://jelly-seerr:5055 | up | [CT 106 jelly-seerr](guests/ct-106.md) |
| Komga | http://komga:25600 | up | [CT 114 komga](guests/ct-114.md) |
| llama-ai | http://ai:8080/health | up | [CT 127 AI](guests/ct-127.md) |
| Loki | http://monitoring:3100/ready | up | [CT 121 Monitoring](guests/ct-121.md) |
| n8n | http://n8n:5678/healthz | up | [CT 128 n8n](guests/ct-128.md) |
| Navidrome | http://navidrome:4533 | up | [CT 111 navidrome](guests/ct-111.md) |
| ntfy | http://ntfy/v1/health | up | [CT 129 ntfy](guests/ct-129.md) |
| ntfy | http://ntfy | up | [CT 129 ntfy](guests/ct-129.md) |
| openwebui | http://openwebui:8080/health | up | [CT 130 openwebui](guests/ct-130.md) |
| openwebui-https | https://jarvis.example.com | up |  |
| plex | http://plex:32400/identity | up | [CT 108 plex](guests/ct-108.md) |
| Plexseerr | http://plex-seerr:5055 | up | [CT 107 plex-seerr](guests/ct-107.md) |
| prowlarr | http://arr:9696 | up | [VM 200 arr](guests/vm-200.md) |
| qbittorrent | http://arr:8080 | up | [VM 200 arr](guests/vm-200.md) |
| radarr | http://arr:7878 | up | [VM 200 arr](guests/vm-200.md) |
| romm | http://romm | up | [CT 116 romm](guests/ct-116.md) |
| sabnzbd | http://arr:8085 | up | [VM 200 arr](guests/vm-200.md) |
| SearXNG | http://searxng:8888/healthz | up | [CT 132 searxng](guests/ct-132.md) |
| sonarr | http://arr:8989 | up | [VM 200 arr](guests/vm-200.md) |
| Tautulli | http://tautulli:8181 | up | [CT 110 tautulli](guests/ct-110.md) |
| UniFi OS | https://unifi-os-server:11443 | up | [CT 120 unifi-os-server](guests/ct-120.md) |

# Network Layout

## Access Zones

| Zone | Meaning | Examples |
|---|---|---|
| LAN | Local home network | SSH, DNS, local testing |
| VPN | Tailscale private network | Nextcloud, Vaultwarden, Grafana |
| Public Internet | Exposed services only | Website, Minecraft |

## Current Access Model

- SSH: LAN/VPN only
- DNS ad blocker: LAN/VPN only
- Nextcloud: VPN only
- Vaultwarden: VPN only
- Grafana/Prometheus: VPN only
- Minecraft: local only for now
- Website: planned public
- Reverse proxy: planned

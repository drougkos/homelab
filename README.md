# Homeserver Lab

Ubuntu Server homelab focused on self-hosting, security, monitoring, and infrastructure documentation.

## Goals

- Build a CV-worthy self-hosted lab
- Learn Linux server administration
- Use Docker Compose for service deployment
- Secure private services with VPN-only access
- Monitor system health with Prometheus + Grafana
- Document every service with setup, access, ports, backups, and risks

## Current Services

| Service | Purpose | Access | Status |
|---|---|---|---|
| DNS Ad Blocker | LAN DNS filtering | LAN/VPN | Working |
| Tailscale | Secure remote access | Private VPN | Working |
| Prometheus + Grafana | Monitoring | VPN/LAN only | Working |
| Nextcloud | Personal cloud/NAS | VPN only | Working |
| Vaultwarden | Password manager | VPN only | Working |
| Minecraft Server | Game server | Local now, public later | Working locally (will launch online when domain is bought so to not expose ports and ip) |
| UFW Firewall | Host firewall | Server-level | Working |
| SSH | Server administration | LAN/VPN restricted | Working |
| Reverse Proxy | Public/private routing | Planned/In progress | Planned |
| Personal Website | Portfolio/CV website | Public later | Planned |


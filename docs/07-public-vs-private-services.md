# Public vs Private Services

## Purpose

This document defines which services are safe to expose publicly and which should remain private.

The goal is to avoid exposing sensitive services while still allowing selected public-facing projects.

## Service Classification

| Service | Classification | Reason |
|---|---|---|
| Personal Website | Public | Intended portfolio/CV site |
| Employer Demo | Public or Restricted | May be shown to recruiters/employers |
| Minecraft Server | Soon Public | Hosting for friends |
| Nextcloud | Private | Contains personal files |
| Vaultwarden | Private | Contains passwords |
| Grafana | Private | Reveals system information |
| Prometheus | Private | Exposes metrics and internal details |
| DNS Ad Blocker | Private | DNS resolvers should not be public |
| SSH | Private | Admin access |
| Reverse Proxy | Public Entry Point | Routes selected public services |

## Public Services

Public services are allowed to be reachable from the internet.

Current/planned public services:

| Service | Domain/Subdomain | Notes |
|---|---|---|
| Personal Website | `drougkos.dev` | Main portfolio |
| Website www | `www.drougkos.dev` | Redirect or mirror |
| Employer Demo | `demo.drougkos.dev` | Optional |
| Minecraft | `mc.drougkos.dev` | Optional |

## Private Services

Private services should only be accessible from LAN or Tailscale.

| Service | Access Method |
|---|---|
| Vaultwarden | Tailscale only |
| Nextcloud | Tailscale only |
| Grafana | LAN/Tailscale only |
| Prometheus | LAN/Tailscale only |
| DNS Ad Blocker Admin | LAN/Tailscale only |
| SSH | LAN/Tailscale only |

## Access Rules

### Public

Public services must have:

- HTTPS
- Reverse proxy
- Minimal exposed ports
- Updated containers
- No default credentials
- Logging enabled
- Backups if data matters

### Private

Private services should have:

- No public port forwarding
- Firewall restrictions
- VPN-only access
- Strong passwords
- 2FA where possible
- Regular backups

## Reverse Proxy Policy

The reverse proxy should only route intentionally public services.

Example public routes:

```txt
drougkos.dev          -> personal website
www.drougkos.dev      -> personal website
demo.drougkos.dev     -> demo service

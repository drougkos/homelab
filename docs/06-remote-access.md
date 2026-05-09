# Remote Access

## Purpose

Remote access is used to manage and access the homeserver without exposing unnecessary services to the public internet.

## Current Remote Access Method

The main remote access method is Tailscale.

Tailscale provides a private VPN-style network between trusted devices.

## Why Tailscale Is Used

- No need to expose the home public IP
- No need to open router ports for private services
- Works across different networks
- Easy access from phone/laptop/desktop
- Better security model for admin services

## Trusted Devices

| Device | Purpose |
|---|---|
| Main Windows PC | Server administration |
| Phone | Access private services remotely |
| Server | Hosts services |

## Services Accessed Remotely

| Service | Access Method | Public? |
|---|---|---|
| SSH | Tailscale/LAN | No |
| Nextcloud | Tailscale | No |
| Vaultwarden | Tailscale | No |
| Grafana | Tailscale/LAN | No |
| Prometheus | Tailscale/LAN | No |
| DNS Ad Blocker | Tailscale/LAN | No |

## SSH Access

SSH should be allowed only from trusted networks.

Preferred access:

```bash
ssh <user>@<tailscale-ip-or-hostname>

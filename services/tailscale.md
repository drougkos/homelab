# Tailscale

## Purpose

Tailscale provides secure private remote access to the homeserver without exposing the home public IP.

It is used to access private services from trusted devices.

## Status

Working.

## Access Model

| Service | Access Through Tailscale? | Public? |
|---|---|---|
| SSH | Yes | No |
| Nextcloud | Yes | No |
| Vaultwarden | Yes | No |
| Grafana | Yes | No |
| Prometheus | Yes | No |
| DNS Ad Blocker | Yes/LAN | No |

## Why Tailscale Is Used

- Avoids exposing public IP
- Avoids unnecessary router port forwarding
- Allows secure access from trusted devices
- Works from phone, laptop, and desktop
- Useful for admin services and private apps

## Important Commands

Check Tailscale status:

```bash
tailscale status

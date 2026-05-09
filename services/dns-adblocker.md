# DNS Ad Blocker

## Purpose

The DNS ad blocker provides network-level DNS filtering for devices on the LAN or VPN.

It blocks ads, trackers, and unwanted domains before devices connect to them.

## Status

Working.

## Access

| Method | Address | Public? |
|---|---|---|
| LAN DNS | `<server-lan-ip>:53` | No |
| Tailscale DNS | `<server-tailscale-ip>:53` | No |
| Admin UI | `http://<server-ip>:<admin-ui-port>` | No |
| Public Internet | Not used | No |

## Access Policy

The DNS ad blocker should only be reachable from trusted networks.

Allowed:

- LAN devices
- Tailscale devices

Not allowed:

- Public internet
- Unknown external clients

## Ports

| Port | Protocol | Purpose | Exposure |
|---:|---|---|---|
| 53 | TCP/UDP | DNS queries | LAN/VPN only |
| `<admin-ui-port>` | TCP | Web admin interface | LAN/VPN only |

## Docker Location

```txt
/srv/docker/dns-adblocker

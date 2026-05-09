# SSH

## Purpose

SSH is used for remote administration of the Ubuntu server.

It allows secure command-line access from trusted devices such as my main Windows PC or devices connected through Tailscale.

## Status

Working.

## Access

| Method | Address | Public? |
|---|---|---|
| LAN | `ssh <user>@<server-lan-ip>` | No |
| Tailscale | `ssh <user>@<server-tailscale-ip-or-hostname>` | No |
| Public Internet | Not used | No |

## Port

| Port | Protocol | Purpose | Exposure |
|---|---|---|---|
| 22 | TCP | SSH administration | LAN/VPN only |

## Important Commands

Check SSH service:

```bash
sudo systemctl status ssh
```
Restart SSH:

```bash
sudo systemctl restart ssh
```

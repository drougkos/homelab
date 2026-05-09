# Nextcloud

## Purpose

Nextcloud is used as a self-hosted personal cloud/NAS service.

It provides file storage, synchronization, and remote access to personal files from trusted devices.

## Status

Working / Testing.

Update this status after confirming all clients can access it correctly.

## Access

| Method | Address | Public? |
|---|---|---|
| LAN | `http://<server-lan-ip>:<nextcloud-port>` | No |
| Tailscale | `http://<server-tailscale-ip>:<nextcloud-port>` | No |
| Public Internet | Not used | No |

## Access Policy

Nextcloud should currently stay private.

Allowed:

- LAN devices
- Tailscale devices

Not allowed:

- Public internet access
- Random external users

Nextcloud may be exposed publicly later only after HTTPS, reverse proxy, updates, backups, and hardening are properly configured.

## Docker Location

```txt
/srv/docker/nextcloud

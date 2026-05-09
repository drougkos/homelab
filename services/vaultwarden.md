# Vaultwarden

## Purpose

Vaultwarden is a self-hosted password manager compatible with Bitwarden clients.

It is used to store and manage passwords in a private, self-hosted environment.

## Status

Working.

## Access

| Method | Address | Public? |
|---|---|---|
| LAN | Not directly exposed if bound to `127.0.0.1` | No |
| Tailscale | `https://<tailscale-hostname>` or `http://<tailscale-ip>:<port>` | No |
| Public Internet | Not used | No |

## Access Policy

Vaultwarden should remain private.

Allowed:

- Trusted Tailscale devices
- Localhost access on the server
- Possibly LAN access only if intentionally configured

Not allowed:

- Public internet access
- Unknown external users
- Public signup

## Docker Location

```txt
/srv/docker/vaultwarden

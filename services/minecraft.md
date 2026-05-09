# Minecraft Server

## Purpose

The Minecraft server is used to self-host a multiplayer game server on the homeserver.

It is currently used as a local/private service and may later be exposed publicly or through a reverse proxy/tunnel depending on the final access design.

## Status

Working locally.

## Access

| Method | Address | Public? |
|---|---|---|
| LAN | `<server-lan-ip>:25565` | No |
| Tailscale | `<server-tailscale-ip>:25565` | No / Optional |
| Public Internet | Not currently used | No |

## Access Policy

Current access should stay private/local.

Allowed:

- LAN players
- Tailscale players, if configured

Not currently allowed:

- Public internet players
- Unknown external users

Future public access is possible, but should only be enabled intentionally.

## Docker Location

```txt
/srv/docker/minecraft

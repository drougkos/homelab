# UFW Firewall

## Purpose

UFW is used to control which ports are reachable on the server.

The goal is to expose only the minimum required services and keep private/admin services restricted to LAN or Tailscale.

## Status

Working.

## Current Policy

- Allow SSH only from trusted networks
- Allow DNS only from LAN/VPN
- Keep admin dashboards private
- Avoid public exposure unless the service is intentionally public

## Important Commands

Check firewall status:

```bash
sudo ufw status verbose
```

Allowing TCP Port:

```bash
sudo ufw allow <port>/udp
```

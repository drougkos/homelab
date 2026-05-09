# Security Model

## Current Security Controls

- UFW firewall enabled
- SSH access restricted
- Private services not exposed publicly
- Tailscale used for remote private access
- Docker Compose used for isolated services
- Vaultwarden signup disabled
- Sensitive `.env` files excluded from Git

## Private Services

These should not be public:

- Vaultwarden
- Nextcloud admin panel
- Grafana
- Prometheus
- DNS admin interface

## Public Services

These may become public later:

- Personal website
- Minecraft server
- Selected demo services

## Secrets Policy

Never commit:

- `.env`
- passwords
- admin tokens
- database passwords
- Tailscale keys
- Cloudflare tokens
- private SSH keys
- Vaultwarden admin token

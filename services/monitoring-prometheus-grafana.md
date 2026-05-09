# Monitoring: Prometheus + Grafana

## Purpose

This monitoring stack is used to observe the homeserver's health, resource usage, and basic system performance.

It helps detect problems early, understand server load, and provide visibility into the infrastructure.

## Status

Working.

## Stack Components

| Component | Purpose |
|---|---|
| Prometheus | Collects and stores metrics |
| Grafana | Displays metrics in dashboards |
| Node Exporter | Exposes Linux host metrics to Prometheus |

## Access

| Service | Address | Public? |
|---|---|---|
| Grafana | `http://<server-ip>:3000` | No |
| Prometheus | `http://<server-ip>:9090` | No |
| Node Exporter | `http://<server-ip>:9100/metrics` | No |

## Access Policy

Monitoring services should stay private.

Allowed:

- LAN access
- Tailscale access

Not allowed:

- Public internet access

Grafana, Prometheus, and Node Exporter can reveal sensitive system information, so they should not be exposed publicly.

## Docker Location

```txt
/srv/docker/monitoring

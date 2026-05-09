
---

## `docs/08-lessons-learned.md`

```md
# Lessons Learned

## Overview

This homelab helped me practice real server administration, Docker deployments, networking, firewall rules, private remote access, monitoring, and self-hosted services.

## Linux Server Administration

I learned how to:

- Work on an Ubuntu Server without relying on a desktop GUI
- Use SSH for remote administration
- Navigate privileged directories
- Understand when to use `sudo`, `sudo -i`, and normal user access
- Check service status with `systemctl`
- Diagnose failed services
- Launch and test services using Docker and Docker compose
Useful commands:

```bash
sudo systemctl status <service>
sudo journalctl -xe
hostname -I
ip a

sudo docker ps
sudo docker compose up -d
sudo docker compose down
sudo docker compose logs -f

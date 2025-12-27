# Homelab Marketplace

Community marketplace for homelab applications - discover, share, and install apps for your homelab infrastructure.

## Overview

This repository contains curated application definitions for the [Homelab Assistant](https://github.com/cbabil/homelab). Each app is defined in YAML format and can be easily deployed to your homelab environment.

## Available Apps

| App | Version | Category | Description |
|-----|---------|----------|-------------|
| [Authelia](apps/security/authelia) | 1.0.0 | security | Authentication and authorization server with 2FA and SSO |
| [Grafana](apps/monitoring/grafana) | 1.0.0 | monitoring | Analytics and monitoring platform for visualizing metrics |
| [Heimdall](apps/utility/heimdall) | 1.0.0 | utility | Application dashboard for organizing self-hosted services |
| [Jellyfin](apps/media/jellyfin) | 1.0.0 | media | Free media server for streaming movies, TV shows, and music |
| [n8n](apps/automation/n8n) | 1.0.0 | automation | Workflow automation for connecting apps and automating tasks |
| [Netdata](apps/monitoring/netdata) | 1.0.0 | monitoring | Real-time performance and health monitoring |
| [Nextcloud](apps/storage/nextcloud) | 1.0.0 | storage | Self-hosted file sync, sharing, and collaboration platform |
| [Pi-hole](apps/networking/pihole) | 1.0.0 | networking | Network-wide ad blocking via DNS |
| [Portainer CE](apps/utility/portainer) | 1.0.0 | utility | Container management UI for Docker and Kubernetes |
| [Prometheus](apps/monitoring/prometheus) | 1.0.0 | monitoring | Monitoring and alerting toolkit for metrics collection |
| [Traefik](apps/networking/traefik) | 1.0.0 | networking | Reverse proxy and load balancer with auto HTTPS |
| [Uptime Kuma](apps/monitoring/uptime-kuma) | 1.0.0 | monitoring | Self-hosted uptime monitoring and status page |

> See [Releases](https://github.com/cbabil/homelab-marketplace/releases) for downloadable app packages.

## Repository Structure

```
apps/
├── media/
│   ├── plex/
│   │   └── app.yaml
│   ├── jellyfin/
│   │   └── app.yaml
│   └── ...
├── networking/
│   ├── pihole/
│   │   └── app.yaml
│   └── ...
├── monitoring/
│   ├── grafana/
│   │   └── app.yaml
│   └── ...
└── ...
```

## App Definition Format

Each app is defined in an `app.yaml` file:

```yaml
id: app-name
name: App Name
description: Short description of the app
version: "1.0.0"
category: media
tags:
  - streaming
  - entertainment

docker:
  image: organization/image:tag
  ports:
    - container: 8080
      host: 8080
      protocol: tcp
  volumes:
    - container: /config
      host: ./config
      mode: rw
  environment:
    - name: TZ
      value: UTC
      required: false

requirements:
  memory: "512MB"
  cpu: "0.5"
  storage: "1GB"

featured: false
```

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on submitting new apps.

## Security

See [SECURITY.md](SECURITY.md) for our security policy and how to report vulnerabilities.

## License

MIT License - see [LICENSE](LICENSE) for details.

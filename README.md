# Homelab Marketplace

Community marketplace for homelab applications - discover, share, and install apps for your homelab infrastructure.

## Overview

This repository contains curated application definitions for the [Homelab Assistant](https://github.com/cbabil/homelab). Each app is defined in YAML format and can be easily deployed to your homelab environment.

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

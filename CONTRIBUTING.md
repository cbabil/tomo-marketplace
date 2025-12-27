# Contributing to Homelab Marketplace

Thank you for your interest in contributing to the Homelab Marketplace!

## How to Contribute

### Submitting a New App

1. **Fork this repository**
2. **Create a new branch**: `git checkout -b add-app-name`
3. **Create the app directory**: `apps/<category>/<app-name>/`
4. **Add your `app.yaml`** following the schema below
5. **Submit a Pull Request**

### App Schema Requirements

Your `app.yaml` must include:

```yaml
# Required fields
id: unique-app-id          # lowercase, hyphens only
name: "Display Name"       # Human-readable name
description: "..."         # Brief description (max 200 chars)
version: "1.0.0"          # Semantic version
category: media           # One of: media, networking, monitoring, security, storage, utility

# Docker configuration (required)
docker:
  image: org/image:tag    # Must be a valid Docker image

# Optional but recommended
tags: []                  # List of relevant tags
requirements:
  memory: "512MB"
  cpu: "0.5"
  storage: "1GB"
```

### Categories

Use one of these categories:
- `media` - Media servers, streaming, entertainment
- `networking` - DNS, VPN, reverse proxies
- `monitoring` - Metrics, logging, alerting
- `security` - Authentication, scanning, protection
- `storage` - Backup, file sharing, databases
- `utility` - Tools, automation, misc

### Review Checklist

Before submitting, ensure:

- [ ] App ID is unique and follows naming convention
- [ ] Docker image exists and is from a trusted source
- [ ] No hardcoded credentials or secrets
- [ ] Ports don't conflict with common services
- [ ] Description is clear and accurate
- [ ] Category is appropriate
- [ ] YAML is valid (use a linter)

### Code of Conduct

- Be respectful and constructive
- Focus on the technical merits
- Help others improve their submissions

### Questions?

Open a [Discussion](https://github.com/cbabil/homelab-marketplace/discussions) for questions or ideas.

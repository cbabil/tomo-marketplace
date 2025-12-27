# Security Policy

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.x.x   | :white_check_mark: |

## Reporting a Vulnerability

We take security seriously. If you discover a security vulnerability in this repository, please report it responsibly.

### How to Report

1. **Do NOT** create a public GitHub issue for security vulnerabilities
2. Email security concerns to the repository owner
3. Include as much detail as possible:
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact
   - Suggested fix (if any)

### What to Expect

- Acknowledgment within 48 hours
- Regular updates on the progress
- Credit in the security advisory (if desired)

### Scope

This security policy covers:
- App definition YAML files in this repository
- Docker configurations and compose files
- Any scripts or automation in this repository

### App Submission Security Requirements

All submitted apps must:
1. Use official or well-maintained Docker images
2. Not contain hardcoded credentials or secrets
3. Not request unnecessary elevated privileges
4. Document any required permissions clearly
5. Use HTTPS for all external connections where possible

## Security Best Practices for Contributors

1. **Never commit secrets** - Use environment variables
2. **Pin image versions** - Avoid `latest` tags
3. **Minimize privileges** - Don't use `--privileged` unless necessary
4. **Review dependencies** - Check image sources before adding

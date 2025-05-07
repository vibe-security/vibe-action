# Vibe Security Action
[![GitHub Marketplace](https://img.shields.io/badge/Marketplace-Vibe%20Security%20Action-blue?logo=github)](https://github.com/marketplace/actions/vibe-security)

Run comprehensive security scans on your codebase using open-source tools like Semgrep, SQLMap, and Trivy—all in one step, directly from your GitHub Actions workflows.

## Features
- Code scanning (Semgrep)
- SQL injection testing (SQLMap)
- Filesystem/Container scanning (Trivy)
- Friendly, emoji-rich output
- Zero manual dependency management

## Usage
Add to your workflow:
```yaml
name: Vibe Security Workflow
on:
  push:
    branches:
      - main
jobs:
  scan:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v3
      - name: Run Vibe Security scan
        uses: vibe-security/vibe-action@v1
```

## Inputs
_No inputs required for standard scan._

## Outputs
- Reports are saved as workflow artifacts or in the working directory.

## Contact
For questions or support, open an issue on [GitHub Action](https://github.com/vibe-security/vibe-action) or [Docker](https://github.com/vibe-security/vibe-docker) or contact [@SHA888](https://github.com/SHA888).

## Example
```yaml
name: Vibe Security Scan
on: [push, pull_request]
jobs:
  security:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: vibe-security/vibe-action@v1
```

## License
MIT

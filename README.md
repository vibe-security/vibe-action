# Vibe Security GitHub Action

Run comprehensive security scans in your CI/CD pipelines using open-source tools like Semgrep, SQLMap, and Trivy—all in one step, directly from GitHub Actions workflows.

## Features
- Code scanning (Semgrep)
- SQL injection testing (SQLMap)
- Container and filesystem scanning (Trivy)
- Simple, emoji-rich output
- Zero manual dependency management

## Usage
```yaml
name: Vibe Security Workflow
on:
  push:
    branches: [main]
jobs:
  scan:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v3
      - name: Run Vibe Security scan
        uses: vibe-security/vibe-action@v1
```

## License
MIT

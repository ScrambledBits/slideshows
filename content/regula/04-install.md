---
weight: 60
---
## Installation Guide 2025

### Snyk IaC
```bash
# Install Snyk CLI
npm install -g snyk
# Authenticate
snyk auth
# Test IaC
snyk iac test terraform-plan.json
```

### Checkov
```bash
# Python/pip
pip install checkov
# Homebrew
brew install checkov
# Docker
docker run bridgecrew/checkov -d .
```

### Trivy
```bash
# Homebrew
brew install trivy
# Docker
docker run aquasec/trivy config .
# GitHub Action
uses: aquasecurity/trivy-action@master
```

{{% note %}}
Modern IaC security tools offer streamlined installation processes. Snyk IaC integrates through their CLI with npm installation and cloud authentication. Checkov provides multiple installation methods including pip, Homebrew, and Docker. Trivy offers the simplest setup with native package managers and excellent Docker support. All tools provide GitHub Actions for seamless CI/CD integration.
{{% /note %}}

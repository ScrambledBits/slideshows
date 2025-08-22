---
weight: 50
---

## Usage Workflows 2025

### Development Workflow
1. **Write IaC configurations** (Terraform, CloudFormation, etc.)
2. **Pre-commit hooks** for early detection
3. **IDE integration** for real-time feedback
4. **Local scanning** before commits

### CI/CD Pipeline Integration
```yaml
# GitHub Actions example
- name: Run Checkov
  uses: bridgecrewio/checkov-action@master
  with:
    directory: .
    framework: terraform

- name: Run Trivy
  uses: aquasecurity/trivy-action@master
  with:
    scan-type: 'config'
    scan-ref: '.'
```

### Enterprise Governance
- **Policy management** through centralized dashboards
- **Compliance reporting** for auditors
- **Exception handling** for approved risks

{{% note %}}
Modern IaC security follows a shift-left approach. Developers get immediate feedback through IDE integration and pre-commit hooks. CI/CD pipelines automatically scan every commit with tools like Checkov and Trivy. Enterprise teams manage policies centrally through dashboards, generate compliance reports, and handle risk exceptions through proper governance workflows. This multilayer approach catches issues early while maintaining organizational oversight.
{{% /note %}}

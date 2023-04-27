---
weight: 80
---
### Pros and Cons of TFSwitch
{{% section %}}
{{< lines >}}
#### Pros:
- Simple installation and management of multiple Terraform versions
- User-friendly interactive CLI for selecting and switching between versions
- Works on macOS, Linux, and Windows (via WSL)
- Can use an optional configuration file (e.g., ".tfswitchrc") for setting default versions
{{< /lines >}}

------

{{< lines >}}
#### Cons:
- No automatic version switching based on project configuration (e.g., ".terraform-version" file)
- Does not support uninstalling Terraform versions directly
- No support for version aliases
{{< /lines >}}
{{% /section %}}

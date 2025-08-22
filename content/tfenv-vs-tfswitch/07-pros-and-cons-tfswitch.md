---
weight: 80
---
### Pros and Cons of TFSwitch
{{% section %}}
{{< lines >}}
#### Pros:
- Simple installation and management of multiple Terraform versions
- User-friendly interactive CLI for selecting and switching between versions
- Works on macOS, Linux, and native Windows
- Can use an optional configuration file (e.g., ".tfswitchrc") for setting default versions
- Automatic version switching based on .tfswitchrc files
{{< /lines >}}

------

{{< lines >}}
#### Cons:
- Does not support .terraform-version files (uses .tfswitchrc instead)
- Does not support uninstalling Terraform versions directly
- No support for version aliases
{{< /lines >}}
{{% /section %}}

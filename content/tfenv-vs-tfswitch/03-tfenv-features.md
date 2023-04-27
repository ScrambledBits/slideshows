---
weight: 40
---

## Features of TFEnv

{{< lines >}}
- Version management.
- Automatic version switching.
- Easy installation.
- Inspired by rbenv.
- Written in Bash.
{{< /lines >}}

{{% note %}}
- Version management:
It allows users to easily manage multiple Terraform versions on their local machine. It enables users to list, install, and uninstall versions. It supports version aliases, which allows users to specify custom names for installed Terraform versions.

- Automatic version switching:
Can automatically switch to the appropriate Terraform version based on a project's configuration. By including a ".terraform-version" file in a project's directory, tfenv will use the specified version when running Terraform commands in that directory. This feature ensures that users are always working with the correct Terraform version for each project, without having to manually switch versions.

- Installation:
tfenv can be installed using various package managers, such as Homebrew for macOS or Git for Linux and macOS. The installation process is straightforward and well-documented, making it accessible for users of all experience levels.

- Inspired by rbenv:
tfenv was inspired by rbenv, a popular Ruby version manager. It uses a similar approach to managing Terraform versions, making it easy for users familiar with rbenv to get started with tfenv.

- Written in Bash:
tfenv is written in Bash, which makes it easy to install and use on most Linux distributions. It also means that it can be easily extended with Bash scripts, allowing users to add custom functionality as needed.
{{% /note %}}

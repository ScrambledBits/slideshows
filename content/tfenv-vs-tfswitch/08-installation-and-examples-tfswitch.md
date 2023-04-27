---
weight: 90
---

{{% section %}}
### How to install TFSwitch

#### Through Homebrew on macOS/Linux
```bash
brew install warrensbox/tap/tfswitch
```

#### Script
```bash
curl -L https://raw.githubusercontent.com/warrensbox/terraform-switcher/release/install.sh | bash
```

#### Manual
Download the binary from the [releases page](https://github.com/warrensbox/terraform-switcher/releases) and put it in `/usr/local/bin` or any other location on your PATH.

------

### Using TFEnv

- Run the interactive CLI:
```bash
tfswitch
```
- Select a version:
```bash
tfswitch 0.12.31
```
- List all installed versions:
```bash
tfswitch -l
```
- List all available versions:
```bash
tfswitch -l --all
```

------

- Set a default version:
```bash
tfswitch -b 0.12.31
```
- Set a default version for a specific directory:
```bash
tfswitch -b 0.12.31 /path/to/directory
```
- Set a default version using a configuration file:
```bash
tfswitch -b 0.12.31 --rcfile .tfswitchrc
# or
echo "0.12.31" > .tfswitchrc
tfswitch --rc
```
{{% /section %}}

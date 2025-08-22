---
weight: 60
---
{{% section %}}
### How to install TFEnv

#### Through Homebrew on macOS/Linux
```bash
brew install tfenv
```

------

#### Manual

- Check out tfenv into any path (here is `${HOME}/.tfenv`)
```shell
git clone --depth=1 https://github.com/tfutils/tfenv.git ~/.tfenv
```

- Add `~/.tfenv/bin` to your `$PATH` any way you like
```shell
echo 'export PATH="$HOME/.tfenv/bin:$PATH"' >> ~/.bash_profile
```

------

### Using TFEnv

- List all available versions
```shell
tfenv list-remote
```
- Install a specific version
```shell
tfenv install 1.13.0
```
- Switch to a specific version
```shell
tfenv use 1.13.0
```

------

- Uninstall a specific version
```shell
tfenv uninstall 1.12.32
```
- Install the latest version
```shell
tfenv install latest
```
- Use the latest version
```shell
tfenv use latest
```
{{% /section %}}

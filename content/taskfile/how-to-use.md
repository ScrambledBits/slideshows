---
weight: 50
---
{{% section %}}
## How to install


(Refer to the [Official documentation](https://taskfile.dev/installation/))
{{% note %}}
One of the great things about Taskfile is that it's easy to install and use. You can download a single binary, add to $PATH and you're done! Or you can also install using Homebrew, Snapcraft, NPM and others if you want, even set it up in CI tools like Github Actions.
{{% /note %}}

------

### Hombrew (MacOS and Linux)
{{< code lang="shell" line-numbers="true" >}}
brew install go-task/tap/go-task # Maintained by the developers
# OR
brew install go-task # Official hombrew repository
{{< /code >}}

------

### Snap
{{< code lang="shell" line-numbers="true" >}}
sudo snap install task --classic
{{< /code >}}

------

### NPM
{{< code lang="shell" line-numbers="true" >}}
npm install -g @go-task/cli
{{< /code >}}

------

### Github actions
{{< code lang="yaml" line-numbers="true" >}}
- name: Install Task
  uses: arduino/setup-task@v2
  with:
    version: 3.x
    repo-token: ${{ secrets.GITHUB_TOKEN }}
{{< /code >}}

{{% /section %}}

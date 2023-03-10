---
weight: 30
---
{{% section %}}
## Features of `Taskfile`

{{< lines >}}
- Easy installation
- Available on CIs
- Truly cross-platform
- Great for code generation
{{< /lines >}}

{{% note %}}
- Easy installation: just download a single binary, add to $PATH and you're done! Or you can also install using Homebrew, Snapcraft, or Scoop if you want.
- Available on CIs: by adding a simple command to install on your CI script and you're ready to use Task as part of your CI pipeline;
- Truly cross-platform: while most build tools only work well on Linux or macOS, Task also supports Windows thanks to this shell interpreter for Go.
- Great for code generation: you can easily prevent a task from running if a given set of files haven't changed since last run (based either on its timestamp or content).
{{% /note %}}

{{% /section %}}

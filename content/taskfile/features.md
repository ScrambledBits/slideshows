---
weight: 30
---
{{% section %}}
## Features of `Taskfile`

{{< lines >}}
- **Schema Version 3**: Modern YAML structure with enhanced features
- **Multiple Variable Types**: STRING, BOOL, INT, FLOAT, ARRAY, MAP support
- **Template Functions**: Built-in functions like `uuid`, `randInt`, `toYaml`
- **Platform Targeting**: Platform-specific tasks `[windows]`, `[linux, darwin]`
- **Watch Mode**: Native filesystem monitoring with `fsnotify`
- **Remote Taskfiles**: Include tasks from remote repositories (experimental)
- **Requirements & Validation**: Enum validation for variables
- **Performance**: Enhanced speed with native filesystem APIs
{{< /lines >}}

{{% note %}}
Task v3.44+ includes significant modern features. Schema version 3 provides enhanced YAML structure with support for multiple variable types including arrays and maps. Template functions enable dynamic content generation with built-in utilities. Platform targeting allows OS-specific task execution. Watch mode uses native filesystem APIs for better performance. Remote Taskfiles enable sharing tasks across projects. Requirements validation ensures proper variable values. The latest versions deliver substantial performance improvements over polling-based approaches.
{{% /note %}}

{{% /section %}}

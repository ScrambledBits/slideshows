---
title: "Examples"
date: 
draft: false
weight: 50
outputs: ["Reveal"]
layout: "list"
---

## Practical Examples

### Docker Container Development
```bash
# Standard Docker commands work seamlessly
docker run -d -p 3000:3000 node:18
docker compose up -d

# Fast volume mounting with VirtioFS
docker run -v $(pwd):/app node:18 npm install
# 2-5× faster than Docker Desktop
```

### Linux Machine Creation
```bash
# Create Ubuntu machine via CLI
orb create ubuntu mydev

# Or use GUI for interactive setup
# Full Ubuntu environment in seconds
# Shared clipboard, drag-and-drop support
```

### Performance Comparison
| Operation | Docker Desktop | OrbStack |
|-----------|----------------|----------|
| Startup time | 30-60 seconds | 2 seconds |
| File I/O | Standard | 2-5× faster |
| Memory usage | 2-4 GB | 100-500 MB |
| CPU usage | 5-15% | <0.1% |

{{% note %}}
These examples showcase OrbStack's practical advantages. Docker operations use identical syntax but execute significantly faster due to VirtioFS file sharing. Linux machine creation takes seconds instead of minutes, with full desktop integration including clipboard sharing and drag-and-drop. The performance table shows concrete improvements: 2-second startup versus Docker Desktop's 30-60 seconds, dramatically reduced resource usage, and 2-5× faster file operations that directly impact development workflow speed.
{{% /note %}}

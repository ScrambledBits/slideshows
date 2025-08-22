---
title: "What is OrbStack?"
draft: false
weight: 20
outputs: ["Reveal"]
layout: "list"
---

## What is OrbStack?

**OrbStack** is a fast, lightweight Docker engine and Linux machine runner specifically designed for macOS.

### Key Positioning
- **Drop-in replacement** for Docker Desktop
- **macOS-native** Swift application
- **Performance leader**: 2-5× faster file I/O
- **Resource efficient**: <0.1% background CPU usage
- **Quick startup**: 2 seconds from launch

### Core Capabilities
- **Docker containers** with full compatibility
- **Linux machines** for development environments  
- **VirtioFS file sharing** for near-native performance
- **Rosetta integration** on Apple Silicon

{{% note %}}
OrbStack is fundamentally different from generic container tools. It's a macOS-native application built with Swift that serves as a direct Docker Desktop replacement. The key differentiator is performance - OrbStack achieves 2-5× faster file I/O through VirtioFS and uses minimal system resources. It starts in just 2 seconds and maintains less than 0.1% background CPU usage. OrbStack handles both Docker containers and full Linux machines, making it perfect for developers who need both capabilities.
{{% /note %}}

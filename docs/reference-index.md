# Reference Index

Detailed documentation for Hugo slideshow development.

## Expanded Commands

### Development Server
```bash
hugo server -D --watch
```
Starts Hugo development server with:
- Draft content enabled (`-D`)
- File watching for auto-reload (`--watch`) 
- Serves on `http://localhost:1313`

### Build Commands
```bash
# Production build
hugo

# Include draft content
hugo -D

# Build to custom directory
hugo -d /path/to/output
```

### Content Creation
```bash
# Create new slideshow
hugo new content/SLIDESHOW_NAME/_index.md

# Create individual slide
hugo new content/SLIDESHOW_NAME/01-intro.md
```

## Content Structure Details

### Slideshow Organization
```
content/
├── _index.md                    # Main landing page
├── slideshow-name/
│   ├── _index.md               # Slideshow intro
│   ├── 01-introduction.md      # First slide
│   ├── 02-features.md          # Second slide
│   ├── ...
│   └── img/                    # Slideshow images
└── another-slideshow/
```

### Front Matter Example
```yaml
---
title: "Slideshow Title"
date: 2023-05-11T12:45:12-06:00
draft: false
weight: 10
outputs: ["Reveal"]
layout: "list"
---
```

## Configuration Details

### Theme Settings (config.toml)
```toml
[params.reveal_hugo]
theme = "blood"
controls_tutorial = true
slide_number = true
transition = "convex"
margin = 0.04
highlight_theme = "monokai-sublime"
```

## Extended Shortcodes

Available in `layouts/shortcodes/`:
- `asciinema`: Terminal recordings
- `audio`: Audio embeddings  
- `chart`: Chart.js integration
- `drawio`: Diagram embeddings
- `emoji`: Emoji support
- `img`: Image handling
- `quote`: Styled quotes
- `typed`: Typing animations
- `video`: Video embeddings

## Module Management
```bash
# Update reveal-hugo theme
hugo mod get -u

# Initialize modules
hugo mod init github.com/username/repo

# Tidy modules
hugo mod tidy
```
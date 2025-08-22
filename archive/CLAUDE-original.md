# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Hugo-based slideshow repository using the reveal-hugo theme to create presentation slides from Markdown content. The site generates multiple technical presentations on topics like Diagrams as code, Taskfile, TFEnv vs TFSwitch, AWS Fargate, Regula, OrbStack, and Envoy Proxy.

## Common Commands

### Development Server
```bash
hugo server -D --watch
```
Starts the Hugo development server with draft content enabled and file watching.

### Build Site
```bash
hugo
```
Builds the static site for production. Output goes to `public/` directory.

### Build with Drafts
```bash
hugo -D
```
Builds the site including draft content.

### Create New Slideshow
```bash
hugo new content/SLIDESHOW_NAME/_index.md
```
Creates a new slideshow section with the base archetype.

## Content Structure

- **`content/`**: Contains all slideshow content organized by topic
- **`content/_index.md`**: Main landing page listing all available slideshows
- **Each slideshow directory**:
  - `_index.md`: Slideshow introduction/landing slide
  - Numbered markdown files (e.g., `01-what-is-x.md`, `02-features.md`) for individual slides
  - Optional `img/` subdirectory for slideshow-specific images

## Configuration

- **`config.toml`**: Hugo site configuration with reveal-hugo theme settings
- **Theme**: Uses `github.com/dzello/reveal-hugo` for Reveal.js integration
- **Slide theme**: "blood" theme with "convex" transitions
- **Base URL**: `https://scrambledbits.github.io/slideshows/`

## Slide Content Guidelines

- Each slideshow should have a descriptive `_index.md` with proper front matter
- Individual slides use standard Markdown with Hugo shortcodes
- Reveal.js specific features available through shortcodes in `layouts/shortcodes/`
- Images stored in `static/images/` or slideshow-specific `img/` directories

## Custom Shortcodes

Available shortcodes for enhanced slide content:
- `{{< slide >}}`: Slide-specific settings
- `{{< lines >}}`: Text formatting
- `{{% note %}}`: Speaker notes
- Various utility shortcodes for charts, videos, code blocks

## Module Management

Uses Go modules (`go.mod`) to manage the reveal-hugo theme dependency. Update with:
```bash
hugo mod get -u
```
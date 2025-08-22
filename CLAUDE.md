# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project
Hugo slideshow site using reveal-hugo theme. Generates presentations from Markdown.

## Commands
- **Dev**: `hugo server -D --watch`
- **Build**: `hugo`
- **Build+drafts**: `hugo -D` 
- **New slideshow**: `hugo new content/SLIDESHOW_NAME/_index.md`
- **Update modules**: `hugo mod get -u`

## Structure
- `content/`: Slideshow directories
- `content/_index.md`: Main landing page
- Each slideshow: `_index.md` + numbered slides (`01-topic.md`)
- Images: `static/images/` or slideshow `img/` dirs
- Config: `config.toml` (reveal-hugo theme, "blood" theme)

## Shortcodes
- `{{< slide >}}`: Slide settings
- `{{< lines >}}`: Text format  
- `{{% note %}}`: Speaker notes
- Additional: charts, videos, code (see `layouts/shortcodes/`)

*See [docs/reference-index.md](docs/reference-index.md) for detailed examples*
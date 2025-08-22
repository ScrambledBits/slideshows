# Specialized Agent Team for Hugo Slideshow Project

This directory contains specialized Claude Code agents designed to work collaboratively on the Hugo-based technical slideshow website.

## Agent Overview

### 🔬 **technical-research-specialist**
**Primary Focus**: Deep research and information gathering for technical topics
- Comprehensive research on DevOps, infrastructure, and emerging technologies
- Multi-source verification and fact-checking
- Latest feature discovery and version comparison analysis
- Research package delivery to content creation agent

### 🏗️ **hugo-site-specialist**
**Primary Focus**: Hugo framework and site structure management
- Hugo configuration (config.toml) optimization
- Site structure and content hierarchy planning
- Module management and reveal-hugo theme integration
- Build pipeline and GitHub Pages deployment optimization

### 🎭 **reveal-presentation-specialist**
**Primary Focus**: Reveal.js presentation framework and slide mechanics
- Reveal.js configuration and theme customization
- Slide transitions, animations, and presentation features
- Navigation, controls, and presentation UX optimization
- Integration between Hugo and Reveal.js functionality

### ✍️ **content-creation-specialist**
**Primary Focus**: Technical content creation with research integration
- Technical writing for DevOps/infrastructure topics
- Slideshow structure planning and narrative development
- Content optimization for presentation format
- **Collaborates closely with technical-research-specialist**

### 🧩 **shortcode-development-specialist**
**Primary Focus**: Custom Hugo shortcodes and template development
- Development and maintenance of 20+ custom shortcodes
- JavaScript library integration (Chart.js, Asciinema, Typed.js)
- Interactive element development for presentations
- Template optimization and HTML generation

### 🎨 **media-integration-specialist**
**Primary Focus**: Multimedia content optimization and interactive media
- Image, video, and audio optimization for presentations
- Terminal recording integration (Asciinema) for DevOps demos
- Chart and diagram creation (Chart.js, draw.io integration)
- Performance optimization for GitHub Pages deployment

### 🔧 **devops-tools-specialist**
**Primary Focus**: Technical validation and hands-on tool expertise
- Technical accuracy verification through practical testing
- Example code and configuration validation
- Tool comparison analysis with real-world testing
- **Works with technical-research-specialist for validation**

## Collaboration Workflow

### Research-Content Pipeline
1. **content-creation-specialist** identifies research needs
2. **technical-research-specialist** conducts comprehensive research
3. **devops-tools-specialist** validates practical implementation
4. **content-creation-specialist** creates final presentation content

### Technical Infrastructure
- **hugo-site-specialist** manages site configuration and structure
- **reveal-presentation-specialist** optimizes presentation mechanics
- **shortcode-development-specialist** develops custom functionality
- **media-integration-specialist** handles multimedia optimization

## Usage Guidelines

### Automatic Delegation
Agents are configured for automatic delegation based on task recognition. Claude will automatically use the most appropriate agent for your requests.

### Explicit Invocation
You can explicitly request a specific agent by mentioning their name:
- "Use the technical-research-specialist to research the latest Terraform features"
- "Have the content-creation-specialist create a new slideshow about Kubernetes"

### Best Practices
1. **Research First**: Always let research agent gather information before content creation
2. **Validate Technically**: DevOps tools expert should validate all technical examples
3. **Optimize for Presentation**: Consider both technical accuracy and slide presentation format
4. **Coordinate Changes**: Site structure changes should involve multiple agents

## Quality Standards
- All technical information must be research-verified and practically tested
- Content must be current, version-appropriate, and implementable
- Presentations must be optimized for both technical accuracy and audience engagement
- All multimedia content must be performance-optimized for GitHub Pages

## Current Project Context
- Hugo-based slideshow site using reveal-hugo theme
- Technical presentations on DevOps tools: Terraform, Docker, AWS, Kubernetes, etc.
- GitHub Pages deployment to `scrambledbits.github.io/slideshows/`
- Target audience: DevOps engineers and infrastructure professionals
# CLAUDE.md - Context for AI Assistants

This file provides context for AI assistants working on this repository in future sessions.

## Repository Overview

This is a collection of simple, standalone web-based tools inspired by [Simon Willison's tools page](https://tools.simonwillison.net/). The repository is hosted at `https://tools.ben.report`.

## Philosophy & Design Principles

### One-Shot Tools
Each tool in this repository follows the "one-shot" philosophy:
- **Self-contained**: Each tool is a single HTML file with embedded CSS and JavaScript
- **No build process**: Tools can be opened directly in a browser with zero setup
- **Immediate functionality**: Everything works on first run with no installation required
- **Low-stakes**: Tools solve simple, practical problems without over-engineering

### Technical Constraints

**Single-File Architecture**
- All tools MUST be standalone HTML files
- CSS and JavaScript are embedded inline (no external dependencies)
- No frameworks or build tools (no React, Vue, webpack, etc.)
- Use vanilla JavaScript only

**Design Standards**
- Minimum 16px base font size for readability
- Consistent typography using Inter font family
- Responsive design that works on mobile and desktop
- Clean, semantic HTML structure

**Styling Approach**
- Reuse the existing design system from index.html where appropriate
- CSS variables for theming (light/dark mode support encouraged)
- Color palette: `#f4f5ef` (bg), `#2a4644` (fg), `#568f81` (accent), etc.
- Minimal, focused UI that prioritizes usability over aesthetics

### User Experience
- Tools should be immediately understandable without documentation
- Support data persistence using localStorage when relevant
- Include export/import functionality for user data
- Provide clear visual feedback for user actions

## Repository Structure

```
/
├── index.html                        # Landing page listing all tools
├── playlist-covers.html              # Playlist cover generator
├── recipes.html                      # Recipe/meal planning tracker
├── chromecast-screensaver-crop.html  # Chromecast photo prep tool
├── epub-locs.html                    # EPUB LOC estimator
├── CNAME                             # GitHub Pages custom domain
└── README.md                         # Public-facing documentation
```

## Current Tools

### Playlist Cover Generator (playlist-covers.html)
- Generates 960x960 geometric pattern images for music playlists
- 4x4 grid of rotatable tiles with customizable colors
- Click-to-rotate interaction pattern
- Canvas-based rendering with PNG export

### Recipe Tracker (recipes.html)
- Weekly meal planner with lunch/dinner grid
- Meal database with protein categorization and ingredients
- Color-coded meal assignment across the week
- Export/import for both meal database and weekly plans
- Dark mode support

### Chromecast Screensaver Crop Tool (chromecast-screensaver-crop.html)
- Adds letterboxing to photos for Chromecast Ambient Mode
- Configurable aspect ratios and custom dimensions
- Adjustable blur and brightness for letterbox bars
- Canvas-based image processing with live preview
- Direct download of processed images

### EPUB LOC Estimator (epub-locs.html)
- Calculates estimated Kindle Location numbers from EPUB files
- Parses EPUB structure using JSZip library
- Displays book metadata and chapter breakdown
- LOC lookup functionality to find specific locations
- CSV export for chapter data

## Guidelines for Adding New Tools

When adding a new tool to this repository:

1. **Create a standalone HTML file** following the single-file architecture
2. **Reuse the navigation and styling** from existing tools for consistency
3. **Add the tool to index.html** in the tools list with a brief description
4. **Update README.md** with a section describing the new tool and its features
5. **Include proper metadata**: title, viewport, favicon reference
6. **Consider dark mode**: Use CSS variables from the existing theme system
7. **Keep it simple**: Resist the urge to over-engineer or add unnecessary features

## Design System Reference

The main color palette (from CSS variables):
- `--bg: #f4f5ef` (light) / `#2a4644` (dark)
- `--fg: #2a4644` (light) / `#f4f5ef` (dark)
- `--bg-accent-1: #8aa899` (muted green)
- `--fg-accent-1: #568f81` (darker green)
- `--bg-accent-2: #f8f8f6` (off-white)
- `--fg-accent-2: #455e58` (dark teal)

Typography:
- Font family: Inter (with system fallbacks)
- Base size: 16px
- Line height: 1.5
- Letter spacing: -0.004em

## Common Patterns

**localStorage keys**: Use descriptive prefixes (e.g., `recipeTracker_meals`, `recipeTracker_plan`)

**Export/Import**: JSON format with pretty-printing (`JSON.stringify(data, null, 2)`)

**Theme toggle**: Reuse the existing SVG-based theme toggle button pattern

**Navigation**: Link back to `/index.html` for the tools list, and `https://ben.report` for the main site

## What This Repository Is NOT

- Not a showcase for cutting-edge web frameworks
- Not a place for complex, multi-file applications
- Not a portfolio of highly-polished, production apps
- Not optimized for performance at scale

## What This Repository IS

- A collection of practical, useful micro-tools
- An experiment in simplicity and self-contained design
- Tools built with AI assistance in a "one-shot" manner
- Low-friction utilities that solve real, small problems

## Maintenance Notes

- Tools are hosted via GitHub Pages (main branch)
- Custom domain: tools.ben.report (configured via CNAME)
- No CI/CD pipeline needed - just commit and push
- Each tool should remain independently functional forever

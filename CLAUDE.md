# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a personal GitHub Pages website (samegavi.github.io) for Sam Amegavi featuring creative writing, mini projects, and teaching materials. The site is built using vanilla HTML, CSS, and JavaScript with no build system or package management.

## Architecture and Structure

The repository follows a simple directory-based structure for different content sections:

- **Root (`/`)**: Main landing page with animated name display and navigation
- **`writing/`**: Contains creative writing pieces, particularly the story "Akwete" 
  - `index.html`: Main writing page with story content
  - `akwete_story.txt`: Text source file for the story
  - Various HTML files for different story presentations
- **`miniprojects/`**: Portfolio of creative projects and experiments
  - `index.html`: Dynamic gallery of projects with embedded content and external links
  - Project data is managed in JavaScript arrays within the HTML file
- **`teaching/`**: Academic/educational content with image gallery functionality
  - `index.html`: Image gallery with lightbox functionality for teaching materials
- **`demo/`**: Contains experimental projects like NoRainbowsky visualizations

## Development Approach

### No Build System
- Direct HTML/CSS/JavaScript files served statically
- No package.json, build scripts, or dependency management
- Changes are made directly to HTML files and served immediately

### Content Management
- **Mini Projects**: Project data is stored as JavaScript objects in `miniprojects/index.html:211-284`
- **Stories**: Text content stored in separate `.txt` files and embedded in HTML templates
- **Styling**: All CSS is embedded within `<style>` tags in individual HTML files

### Styling Patterns
- Consistent use of system fonts and modern CSS features
- Color schemes using predefined palettes (e.g., `#FF6B6B`, `#4ECDC4`, `#45B7D1`)
- Responsive design with mobile-first breakpoints
- CSS animations for visual effects (bouncing letters, color changes, hover states)

## Key Features

### Landing Page (`index.html`)
- Animated letter-by-letter bouncing name display
- Color-changing text animations
- Corner navigation links with "NEW" tags

### Mini Projects Gallery
- Dynamic project cards with embedded iframes and images
- Mobile-responsive preview frames for web projects
- External link integration with proper `target="_blank"` and `rel="noopener"`
- Automatic project sorting by date

### Writing Section
- Typography-focused design with serif fonts for readability
- Drop caps and justified text formatting
- Story content synchronized between `.txt` source and HTML presentation

## Common Development Tasks

Since this is a static site with no build system, development involves:
1. Edit HTML files directly for content changes
2. Update JavaScript data structures for new projects/content
3. Test locally by opening HTML files in browser
4. Commit changes directly to git for GitHub Pages deployment

## Content Structure Conventions

- Project descriptions support HTML links for references
- Dates formatted as "Month YYYY" (e.g., "February 2025")
- External links include proper attribution and `target="_blank"`
- Story content maintains paragraph structure with proper spacing
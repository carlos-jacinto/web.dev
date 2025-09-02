# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the web.dev repository - a static web application project using vanilla HTML, CSS, and JavaScript with Bootstrap 5 as the primary CSS framework.

## Development Commands

This is a static web project with no build process. To develop:

- Open `public/index.html` directly in a browser for development
- Use a local web server for testing: `python -m http.server 8000` (from the `public/` directory)
- Or use any static file server like Live Server extension in VS Code

## Architecture

### Directory Structure

- **`public/`** - Main application directory containing all web assets
  - **`index.html`** - Main entry point with Bootstrap and modular JS setup
  - **`index.js`** - Main JavaScript entry point (ES6 modules)
  - **`lib/vendor/bootstrap/`** - Bootstrap 5 CSS and JS files
  - **`theme/`** - Custom theme and styling files
  - **`components/`** - Reusable UI components (planned/empty)
  - **`pages/`** - Individual page files
    - **`builder/`** - Contains builder-related pages
  - **`assets/images/`** - Image assets including favicon.svg
- **`src/`** - Currently empty, may contain future source files

### Technology Stack

- **Frontend**: Vanilla HTML5, CSS3, JavaScript ES6+ modules
- **CSS Framework**: Bootstrap 5 (complete bundle including utilities, grid, and components)
- **Module System**: Native ES6 modules via `<script type="module">`
- **Icons**: SVG favicon included

### Key Implementation Details

- Bootstrap 5 is loaded via local files (not CDN)
- Uses deferred script loading for optimal performance
- Responsive design with Bootstrap's grid system
- Custom theming system in place via `theme/theme.css`
- Modular architecture prepared for component-based development

## Key Information

- No build tools, bundlers, or package managers currently used
- Static deployment ready - all files can be served directly
- Bootstrap JavaScript bundle includes Popper.js for interactive components
- Main branch: `main`
- Development server should serve from `public/` directory as root
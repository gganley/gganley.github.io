# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a Jekyll-powered personal blog hosted on GitHub Pages at blog.ganley.dev.

## Commands

```bash
# Install dependencies
bundle install

# Run local development server (http://localhost:4000)
bundle exec jekyll serve

# Build site without serving
bundle exec jekyll build
```

## Architecture

- **`_layouts/`**: HTML templates. `default.html` is the base layout; `post.html` extends it for blog posts.
- **`_posts/`**: Blog posts in Markdown with YYYY-MM-DD-title.md naming convention.
- **`assets/css/style.css`**: Site styling.
- **`_config.yml`**: Jekyll configuration (theme: minima, plugins: jekyll-feed, jekyll-seo-tag).

## Deployment

Push to `master` triggers GitHub Actions workflow (`.github/workflows/jekyll-gh-pages.yml`) which builds and deploys to GitHub Pages.

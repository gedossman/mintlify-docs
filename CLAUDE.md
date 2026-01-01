# CLAUDE.md

# Mintlify documentation official for Claude.MD

## Working relationship
- You can push back on ideas-this can lead to better documentation. Cite sources and explain your reasoning when you do so
- ALWAYS ask for clarification rather than making assumptions
- NEVER lie, guess, or make up information

## Project context
- Format: MDX files with YAML frontmatter
- Config: docs.json for navigation, theme, settings
- Components: Mintlify components

## Content strategy
- Document just enough for user success - not too much, not too little
- Prioritize accuracy and usability of information
- Make content evergreen when possible
- Search for existing information before adding new content. Avoid duplication unless it is done for a strategic reason
- Check existing patterns for consistency
- Start by making the smallest reasonable changes

## Frontmatter requirements for pages
- title: Clear, descriptive page title
- description: Concise summary for SEO/navigation

## Writing standards
- Second-person voice ("you")
- Prerequisites at start of procedural content
- Test all code examples before publishing
- Match style and formatting of existing pages
- Include both basic and advanced use cases
- Language tags on all code blocks
- Alt text on all images
- Relative paths for internal links

## Git workflow
- NEVER use --no-verify when committing
- Ask how to handle uncommitted changes before starting
- Create a new branch when no clear branch exists for changes
- Commit frequently throughout development
- NEVER skip or disable pre-commit hooks

## Do not
- Skip frontmatter on any MDX file
- Use absolute URLs for internal links
- Include untested code examples
- Make assumptions - always ask for clarification


**** CLAUDE Agent Analysis:
This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Mintlify documentation site. Mintlify is a documentation platform that renders MDX files into a polished documentation website.

## Commands

```bash
# Install Mintlify CLI globally
npm i -g mint

# Start local development server (runs at http://localhost:3000)
mint dev

# Update CLI to latest version (use if dev environment has issues)
mint update
```

## Architecture

- **docs.json** - Central configuration file defining navigation structure, theme colors, logos, and site settings
- **MDX files** - Documentation pages written in MDX (Markdown + JSX components)
- **snippets/** - Reusable content fragments that can be included in multiple pages
- **api-reference/openapi.json** - OpenAPI spec for auto-generated API documentation

## Key Concepts

- Navigation is defined in `docs.json` under the `navigation` key with tabs and groups
- Pages are referenced by their path without the `.mdx` extension (e.g., `"essentials/settings"`)
- The `index.mdx` file is the homepage
- Changes pushed to the default branch auto-deploy via the Mintlify GitHub app

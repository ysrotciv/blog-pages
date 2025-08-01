# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

All commands are run from the root of the project:

- `npm run dev` - Start local dev server at localhost:4321
- `npm run build` - Build production site to ./dist/
- `npm run preview` - Preview build locally before deploying
- `npm run astro` - Run Astro CLI commands

## Architecture

This is an Astro-based blog with the following key structure:

### Content Management
- Blog posts are stored in `src/content/blog/` as Markdown/MDX files
- Content schema is defined in `src/content.config.ts` with required frontmatter fields:
  - `title` (string)
  - `description` (string) 
  - `pubDate` (date)
  - `updatedDate` (optional date)
  - `heroImage` (optional image)
- Use `getCollection()` to retrieve posts from the blog collection

### Routing & Pages
- File-based routing in `src/pages/`
- Dynamic blog post routes handled by `src/pages/blog/[...slug].astro`
- Blog index at `src/pages/blog/index.astro`
- RSS feed generated at `src/pages/rss.xml.js`

### Components & Layout
- Reusable components in `src/components/`
- Blog post layout in `src/layouts/BlogPost.astro`
- Global site constants in `src/consts.ts` (SITE_TITLE, SITE_DESCRIPTION)

### Assets
- Static assets in `public/`
- Blog images and other assets in `src/assets/`
- Uses Astro's built-in image optimization

### Configuration
- Site URL configured in `astro.config.mjs` (currently example.com)
- Includes MDX and sitemap integrations
- TypeScript with strict configuration
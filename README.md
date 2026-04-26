# OpenLor

OpenLor is Lor's personal Astro blog for public notes, articles, project learnings, and ideas.

- Site: <https://openlor.org/>
- GitHub: <https://github.com/gobylor>
- Default language: `zh_CN`
- Content license: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

## Stack

This site is customized from the Fuwari Astro theme and uses:

- [Astro](https://astro.build/) for static site generation
- [Tailwind CSS](https://tailwindcss.com/) for styling
- [Pagefind](https://pagefind.app/) for static search
- RSS and sitemap generation for publishing

## Development

Install dependencies with pnpm, then run commands from the project root:

| Command | Action |
| --- | --- |
| `pnpm install` | Install dependencies |
| `pnpm dev` | Start local development server |
| `pnpm check` | Run Astro type/content checks |
| `pnpm build` | Build production output and Pagefind index |
| `pnpm preview` | Preview the production build locally |
| `pnpm new-post <filename>` | Create a new draft post under `src/content/posts/` |

## Content

Posts live in `src/content/posts/`. New posts are drafts by default; set `draft: false` in frontmatter when a post is ready to publish.

Common frontmatter fields:

```yaml
---
title: My Post
published: 2026-04-27
description: Short summary
image: ''
tags: []
category: Notes
draft: true
lang: zh_CN
---
```

The About page content lives in `src/content/spec/about.md`.

## Deployment

The production site URL is configured in `astro.config.mjs` as `https://openlor.org/`. Build output is written to `dist/`.

Cloudflare deployment settings remain in `wrangler.jsonc` with the project name `openlor`.

## License

Site content is published under CC BY-NC-SA 4.0 unless otherwise noted. Project code follows the license in `LICENSE`.

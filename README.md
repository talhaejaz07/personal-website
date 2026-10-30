# Personal Website

This repository contains the planning and, as work progresses, the source code for a personal website with a blog.

## Project status

The Astro website and blog are live at `https://ejazhome.com/` on Cloudflare Pages. The site presents PSX investing as a major interest alongside technology, engineering, and green energy, and links to X and YouTube. It uses the approved Barlow Condensed, DM Sans, and optional DM Mono typography with a near-black, off-white, and vivid red palette.

## Hosting

The site is hosted on Cloudflare Pages at `https://ejazhome.com/`. The `ejaz-home` Tunnel is shared with Paperless and n8n and remains in use for those applications; the website is served directly by Pages.

## Project records

- [Project plan and task tracker](PROJECT_PLAN.md) — scope, decisions, tasks, and progress.
- [Agent instructions and task history](AGENTS.md) — required project workflow and completed-task history.
- [Website and blog writing guidelines](WRITING_GUIDELINES.md) — guidance to read before creating or editing public-facing copy.
- [Design system and review](DESIGN_SYSTEM.md) — editorial styling, mobile layout rules, shared components, and verification evidence.

## Development

Install dependencies with `npm install`, then start the local development server with `npm run dev`. Use `npm run build` to generate the static site in `dist/`, and `npm run preview` to preview that build locally.

Blog posts live in `src/pages/blog/` and must use `src/layouts/BlogPostLayout.astro`. The layout automatically adds a collapsed, expandable table of contents below the cover using the post's H2–H6 headings. No manual list or per-post setup is needed. Section links and the disclosure work without JavaScript; supported browsers animate expansion, with reduced-motion preferences respected. Posts without section headings omit the empty panel.

## Cloudflare Pages deployment

The Cloudflare Pages project is connected to this GitHub repository with `main` as its production branch. Its build command is `npm run build`, and its build output directory is `dist/` (repository root). Cloudflare builds and deploys pushes to `main`; pull requests receive preview deployments.










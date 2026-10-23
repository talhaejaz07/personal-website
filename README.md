# Personal Website

This repository contains the planning and, as work progresses, the source code for a personal website with a blog.

## Project status

The empty Astro scaffold is in place. It generates a static site; page content, the blog authoring workflow, design, and production hosting setup are still being decided.

## Planned hosting

The site now runs in Docker on the owner's Ubuntu home server. Nginx serves it on LAN port `8085`; `http://192.168.18.100:8085/` returned HTTP 200 during the LAN check. The Cloudflare Tunnel route for `ejazhome.com` is the remaining publishing step.

## Project records

- [Project plan and task tracker](PROJECT_PLAN.md) — scope, decisions, tasks, and progress.
- [Agent instructions and task history](AGENTS.md) — required project workflow and completed-task history.

## Development

Install dependencies with `npm install`, then start the local development server with `npm run dev`. Use `npm run build` to generate the static site in `dist/`, and `npm run preview` to preview that build locally.

## Home server deployment

Pushes to `main` trigger GitHub Actions to build the Astro site and publish the Docker image to GitHub Container Registry. The home server pulls the public image without registry credentials. Its dedicated Watchtower container checks for a new image every 60 seconds and updates only the `personal-website` container. Its existing Watchtower service for other apps is unchanged.

To publish a change, push it to `main`. GitHub Actions builds and publishes the image, and the server updates within about a minute after the build completes. The site is available on port `8085`; the Cloudflare Tunnel service URL is `http://192.168.18.100:8085`.

For a first-time server setup or a manual refresh, run:

```sh
cd /home/talha/personal-website
git pull --ff-only
docker compose pull personal-website
docker compose up -d
```








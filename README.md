# Personal Website

This repository contains the planning and, as work progresses, the source code for a personal website with a blog.

## Project status

The first Astro homepage is live at `https://ejazhome.com/`. It introduces Talha's PSX investing focus, links to X and YouTube, and highlights technology and green-energy interests. The site uses the approved Barlow Condensed, DM Sans, and optional DM Mono typography with a graphite, ivory, and coral palette. A live HTTPS check returned HTTP 200 with the expected page title and hero portrait.

## Hosting

The site runs in Docker on the owner's Ubuntu home server. Nginx serves it on LAN port `8085`; the Cloudflare Tunnel maps `ejazhome.com` to `http://192.168.18.100:8085`. Public HTTPS access is working.

## Project records

- [Project plan and task tracker](PROJECT_PLAN.md) — scope, decisions, tasks, and progress.
- [Agent instructions and task history](AGENTS.md) — required project workflow and completed-task history.

## Development

Install dependencies with `npm install`, then start the local development server with `npm run dev`. Use `npm run build` to generate the static site in `dist/`, and `npm run preview` to preview that build locally.

## Home server deployment

Pushes to `main` trigger GitHub Actions to build the Astro site and publish the Docker image to GitHub Container Registry. The home server pulls the public image without registry credentials. A systemd timer checks for new images every 60 seconds and updates only the `personal-website` container. The existing Watchtower service for other apps remains unchanged.

To publish a change, push it to `main`. GitHub Actions builds and publishes the image, and the server updates within about a minute after the build completes. The site is available on port `8085`; the Cloudflare Tunnel service URL is `http://192.168.18.100:8085`.

Install the timer once on the Ubuntu server, from the project directory:

```sh
cd /home/talha/personal-website
sudo install -m 644 deploy/systemd/personal-website-update.service /etc/systemd/system/personal-website-update.service
sudo install -m 644 deploy/systemd/personal-website-update.timer /etc/systemd/system/personal-website-update.timer
sudo systemctl daemon-reload
sudo systemctl enable --now personal-website-update.timer
```

For a manual refresh, run:

```sh
docker compose pull personal-website
docker compose up -d --no-deps personal-website
```










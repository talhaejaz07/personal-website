# Personal Website — Project Plan and Task Tracker

This is the living project record for the personal website. It documents the work we agree to do, tracks who is doing it, and records decisions and completed work. Update it as the project changes so it remains the shared source of truth.

## Project at a glance

- **Project:** Personal website
- **Goal:** Plan, build, verify, and publish a personal website that represents its owner and serves the goals we agree on.
- **Current state:** The blank Astro scaffold is running on the home server and is publicly reachable at `https://ejazhome.com/` through Cloudflare Tunnel. A live request returned HTTP 200 and the page title “Personal Website”.
- **Technology:** Astro with npm, generating a static site; supporting integrations and blog authoring workflow are still to be decided.
- **Audience:** Friends and general visitors.
- **Purpose:** Introduce who the owner is, showcase social profiles, and share writing through a blog.
- **Content direction:** Lead with the owner's interest in PSX stock investing. He regularly shares investment posts on X and videos on YouTube, and also posts personal thoughts on X. Technology and a greener future, especially solar and batteries, are additional interests. The detailed bio remains private planning reference; only owner-approved selections belong on the site.
- **Initial topic areas:** PSX investing and financial analysis as the main editorial focus; technology and the green-energy future (including solar and batteries) as secondary themes.
- **Visual direction:** Still to be planned with the owner.
- **Last updated:** 2026-10-23

## Working agreements

- Keep this document current when a task is started, completed, deferred, or descoped.
- Do not mark a task complete until its outcome is available to review.
- Record the owner for each task. “User” means you; “Assistant” means work I carry out with your direction.
- Add user-completed work to the activity log, including a short outcome and date. If the exact date is unknown, use `date not provided` instead of guessing.
- Record important choices in the decision log, including the reason and any consequences.
- Add new work to the task tracker before doing it when practical. Split large tasks into smaller reviewable items.
- Keep secrets, passwords, private keys, and other credentials out of this file.

## Scope and requirements

### Agreed goals

- Help visitors get to know the owner through personal interests, voice, and writing.
- Give friends and general visitors a clear way to read the blog and follow social profiles.
- Build a personal brand centered on identity and interests, without job-search positioning.
- Decide which pages, content, visual style, and brand assets to include.
- Decide whether extra features such as a contact form or downloadable materials belong on the site.
- For the blog, how posts should be written and organized (for example, Markdown files in the project or a content-management system).
- Any requirements for languages, accessibility, privacy, maintenance, budget, or launch date.

### Initial scope

Create a personal website with a blog using Astro, check it on common screen sizes, and maintain the existing deployment. The site will introduce the owner, showcase social profiles, and share writing for friends and general visitors. It is an expression of the owner's personal identity and interests, without job-search positioning.

### Draft first-release sitemap

This outline is a proposal for owner review.

- **Home:** Short introduction centered on PSX investing, links to X and YouTube, and recent writing.
- **About:** Personal background and interests, written in the owner's voice.
- **Blog:** Post index and individual articles.
- **Socials:** A curated list of social profiles, starting with [X](https://x.com/TalhaEjaz07ee) and [YouTube](https://www.youtube.com/@TalhaEjaz). More can be added later.

A separate projects or résumé page is outside the current plan. We can add a personal-interest page later if the owner wants one.

### Not yet specified

- Required pages and final copy
- Design references, colors, typography, and imagery
- Supporting dependencies and blog content-management/authoring approach
- Analytics, cookies, privacy notices, and form handling
- Browser/device support targets
- Launch timing and ongoing maintenance expectations

## Project phases

These phases are a starting plan. We can revise them as requirements become clear.

1. **Discover and define** — Agree on the website's purpose, audience, content, constraints, and success criteria.
2. **Plan the experience** — Define pages, navigation, key user journeys, content needs, and visual direction.
3. **Choose the implementation approach** — Select the tools, project structure, hosting, and deployment method based on the requirements.
4. **Build the foundation** — Set up the project, shared layout, navigation, responsive behavior, and reusable styles/components.
5. **Create pages and content** — Implement the agreed pages and add approved text, images, links, and metadata.
6. **Review and refine** — Check functionality, content, responsive layouts, accessibility basics, search metadata, and performance; resolve issues found.
7. **Prepare and launch** — Configure the production environment and domain, deploy, and verify the published site.
8. **Maintain** — Record follow-up fixes and content updates; keep dependencies and deployment instructions understandable.

## Task tracker

Status values: `Not started`, `In progress`, `Blocked`, `Done`, `Deferred`, `Descoped`.

| ID | Phase | Task | Owner | Status | Notes / completion evidence |
|---|---|---|---|---|---|
| PIPE-01 | Prepare and launch | Build and publish the site image on each push to main, then automatically update the home-server container | Assistant | Done | GitHub Actions run for `b2aa7f1` succeeded; the enabled systemd timer pulled and ran that exact image revision. Site returned HTTP 200; original CasaOS Watchtower is healthy. |
| HOST-02 | Prepare and launch | Start the Docker service on the home server and confirm LAN access | User + Assistant | Done | Container running on port 8085; workstation received HTTP 200 from `192.168.18.100:8085` |
| HOST-01 | Prepare and launch | Add a Docker/Nginx production service on port 8085 | Assistant | Done | Multi-stage Astro build and static Nginx service added |
| BUILD-00 | Build the foundation | Initialize an empty Astro project scaffold | Assistant | Done | Installed Astro and added the root route, config, TypeScript config, npm scripts, and lockfile; no page content added |
| DOC-README-01 | Discover and define | Add a repository README describing project status, decisions, and project records | Assistant | Done | Added `README.md` |
| SOCIAL-01 | Plan the experience | Choose social profiles to feature in the first release | User | Done | X: `@TalhaEjaz07ee`; YouTube: `@TalhaEjaz` |
| DISC-01 | Discover and define | Confirm the website's purpose, audience, and desired visitor actions | User + Assistant | Done | Personal identity, social profiles, and writing for friends and general visitors; no job-search positioning |
| DISC-02 | Discover and define | Gather required content, pages, links, assets, and any existing brand material | User | In progress | X and YouTube links collected; PSX investing confirmed as the main focus, with technology and solar/batteries as secondary interests. Need approved short public bio and any images or brand references |
| DISC-03 | Discover and define | Agree on constraints, success criteria, target launch timing, and maintenance needs | User + Assistant | Not started | |
| PLAN-01 | Plan the experience | Draft the sitemap and navigation | Assistant, with User review | In progress | Draft proposes Home, About, Blog, and Socials; X and YouTube selected; review the structure and remaining content |
| PLAN-02 | Plan the experience | Agree on visual direction and page-level requirements | User + Assistant | Not started | |
| PLAN-03 | Plan the experience | Identify accessibility, privacy, SEO, and performance requirements | Assistant, with User review | Not started | |
| TECH-01 | Choose the implementation approach | Select the site framework | User + Assistant | Done | Astro selected on 2026-10-23 |
| TECH-03 | Choose the implementation approach | Choose supporting dependencies and blog authoring/content workflow | User + Assistant | Not started | Consider Markdown files in the project or a CMS |
| TECH-02 | Choose the implementation approach | Select domain, hosting, and deployment workflow | User + Assistant | Done | `ejazhome.com` uses the existing Cloudflare Tunnel to reach the home server; GitHub Actions and the server systemd timer publish updates |
| BUILD-01 | Build the foundation | Set up the project structure and shared site shell | Assistant | Not started | |
| BUILD-02 | Build the foundation | Implement responsive layout, navigation, and shared styles | Assistant | Not started | |
| BUILD-03 | Create pages and content | Build each agreed page and add owner-approved content and assets | Assistant, with User content/review | Not started | Add one task row per page/features once scope is agreed |
| BLOG-01 | Create pages and content | Implement the blog index, post pages, and agreed post-authoring workflow | Assistant, with User content/review | Not started | Depends on TECH-03 |
| REVIEW-01 | Review and refine | Review content, links, layout, and behavior on target screen sizes | User + Assistant | Not started | |
| REVIEW-02 | Review and refine | Address agreed accessibility, metadata, and performance findings | Assistant | Not started | |
| LAUNCH-01 | Prepare and launch | Configure production settings and deployment | Assistant, with User input as needed | Done | Docker on port 8085; GitHub Actions publishes the image and a systemd timer updates the server |
| LAUNCH-02 | Prepare and launch | Verify the live site and record launch details | User + Assistant | Done | User configured the Cloudflare Tunnel route `ejazhome.com` → `http://192.168.18.100:8085`; public HTTPS check returned HTTP 200 and title “Personal Website” on 2026-10-23 |
| MAINT-01 | Maintain | Record follow-up improvements and maintenance tasks | User + Assistant | Not started | Ongoing |

## User task record

Use this section to track work you complete or provide. Add the newest entry at the top. Link to files or relevant task IDs when possible.

| Date | Related task ID | Work you completed / provided | Outcome or evidence | Follow-up |
|---|---|---|---|---|
| 2026-10-23 | SOCIAL-01 | Chose X and YouTube as the social profiles to show for now | [X](https://x.com/TalhaEjaz07ee), [YouTube](https://www.youtube.com/@TalhaEjaz) | Add other profiles later if wanted |
| 2026-10-23 | DISC-01 | Clarified that the website is for personal expression, social profiles, and a blog; the audience is friends and general visitors | Agreed on a personal, interest-led site without job-search positioning | Share social profile links and content preferences in DISC-02 |
| 2026-10-23 | LAUNCH-02 | Added the `ejazhome.com` published application route in Cloudflare Tunnel | Screenshot shows the route to `http://192.168.18.100:8085`; live HTTPS check returned HTTP 200 | Continue site content and design work |
| 2026-10-23 | TECH-01 | Chose Astro after confirming the site will include a blog | Astro selected as the site framework | Decide the blog authoring workflow in TECH-03 |

## Activity log

Record meaningful project progress here, including implementation and review work done by either of us. Add newest entries at the top.

| Date | Owner | Task ID | Update |
|---|---|---|---|
| 2026-10-23 | User | SOCIAL-01 | Selected X (`@TalhaEjaz07ee`) and YouTube (`@TalhaEjaz`) for the first release; other links may be added later. |
| 2026-10-23 | User + Assistant | DISC-01 | Agreed the website should express who the owner is, showcase social profiles, and share writing with friends and general visitors. It will not use job-search framing. |
| 2026-10-23 | Assistant | PLAN-01 | Drafted a first-release sitemap with Home, About, Blog, and Socials, pending the owner's social links and review. |
| 2026-10-23 | User + Assistant | LAUNCH-02 | User configured the Cloudflare Tunnel route `ejazhome.com` to `http://192.168.18.100:8085`; a live HTTPS request returned HTTP 200 with title “Personal Website”. |
| 2026-10-23 | User + Assistant | PIPE-01 | Verified the GitHub Actions build for `b2aa7f1` published to GHCR and the systemd timer deployed that exact revision. The site returned HTTP 200 and the original CasaOS Watchtower is healthy. The timer polls every 60 seconds; the conflicting second Watchtower was removed and the original service restored. |
| 2026-10-23 | User + Assistant | HOST-02 | Launched `personal-website` on the Ubuntu server; container is up and the workstation received HTTP 200 from `http://192.168.18.100:8085/`. |
| 2026-10-23 | Assistant | HOST-01 | Added Docker build and Compose configuration to serve Astro's generated static files with Nginx on host port 8085. |
| 2026-10-23 | Assistant | BUILD-00 | Initialized a blank Astro scaffold with npm scripts and dependencies; added an empty root page and documented local commands. |
| 2026-10-23 | Assistant | DOC-README-01 | Added `README.md` with the current project status, selected framework, proposed hosting direction, and links to project records. |
| 2026-10-23 | User + Assistant | TECH-01 | Selected Astro for the personal website and blog; added a blog implementation task and an open question for the authoring workflow. |
| 2026-10-23 | Assistant | — | Created this project plan and initial task tracker. No existing project files were present. |

## Decision log

Record decisions that affect scope, design, implementation, or launch. Add newest entries at the top.

| Date | Decision | Reason | Impact / follow-up |
|---|---|---|---|
| 2026-10-23 | Feature X (`@TalhaEjaz07ee`) and YouTube (`@TalhaEjaz`) as the initial social links. | The owner selected these profiles for now. | Show them on the Home and Socials pages; additional profiles can be added later. |
| 2026-10-23 | Shape the website around personal identity, social profiles, and blog writing for friends and general visitors. | The owner wants the site to show who they are and share their writing. | Use an interest-led personal brand without job-search positioning; review the proposed Home, About, Blog, and Socials pages. |
| 2026-10-23 | Publish container images with GitHub Actions and use a systemd timer on the home server to pull updates every 60 seconds. | The server should update from Git pushes without exposing a new inbound service; running a second Watchtower conflicted with CasaOS's existing Watchtower. | The timer updates only `personal-website`; GHCR package is publicly pullable. |
| 2026-10-23 | Host the static Astro site on the Ubuntu home server and publish through the existing Cloudflare Tunnel at `ejazhome.com`. | The owner already runs a Cloudflare Tunnel and configured a published application route for the website. | The route sends requests to `http://192.168.18.100:8085`; public HTTPS returned HTTP 200. |
| 2026-10-23 | Use Astro to build the personal website and blog. | The owner plans to add a blog; Astro can generate static pages suitable for the home server. | Choose supporting dependencies and the blog authoring workflow in TECH-03. |
| 2026-10-23 | Use this file as the shared project plan and task tracker. | Requested by the project owner. | Keep the tracker and logs updated as work proceeds. |

## Open questions and blockers

Add questions that need an answer and blockers that prevent progress. Remove or mark entries resolved when addressed.

- [ ] Which pages and content should the first version include?
- [ ] What design references, style, or assets should guide it?
- [ ] Should blog posts be authored as Markdown files in the project, or through a CMS?
- [ ] Is there a target date or other constraint we should plan around?















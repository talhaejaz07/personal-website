# Project instructions

- Before starting project work, read `PROJECT_PLAN.md`. Reading it is compulsory; follow its current scope, decisions, task tracker, and open questions.
- Keep `PROJECT_PLAN.md` updated as tasks are started, completed, deferred, or descoped, including work the user completes or provides.
- Record the history of every project task in the **Task history** section below. Add one entry per task, including user-provided decisions and work, with its date, task ID, owner, outcome/status, and commit/push reference. Add new entries at the top; never erase completed history. Record the current task as `this commit` before its commit hash exists, then treat the resulting Git commit and push as its reference.
- After each task the user requests is completed, commit the project changes and push them to the GitHub repository. If GitHub access or a configured remote is unavailable, report the blocker and leave the changes committed locally when possible.

## Task history

| Date | Task ID | Owner | Task and outcome/status | Commit / push reference |
|---|---|---|---|---|
| 2026-10-23 | HOME-01 | Assistant, with User-provided portrait | Built the first responsive Astro homepage from the approved design and content direction; used the supplied portrait in the hero and added X/YouTube links. Production build succeeded. Done. | This commit; push after completion |
| 2026-10-23 | PLAN-02 | User + Assistant | Drafted and presented the proposed typography and palette, then the user approved the full system. Marked the design direction approved in the project plan. Done. | `db83f96`, `70cf4d1`, `1eff378`, `a5fc331` |
| 2026-10-23 | DISC-02 | User + Assistant | User provided detailed personal background as planning reference and clarified it should not all appear on the site. Recorded only broad candidate themes and a privacy note in the project plan; full text/private details were not copied to the public repo. In progress pending selection of public bio and topic priorities. | `ed5f795`, `db3f10a` |
| 2026-10-23 | SOCIAL-01 | User | Selected X (`@TalhaEjaz07ee`) and YouTube (`@TalhaEjaz`) for the first release; other social profiles can be added later. Done. | This commit; push after completion |
| 2026-10-23 | PLAN-01 | Assistant, with User review | Drafted Home, About, Blog, and Socials for the first release; waiting on social profile links and page/content review. In progress. | This commit; push after completion |
| 2026-10-23 | DISC-01 | User + Assistant | Agreed the site should introduce who the owner is, showcase social profiles, and share writing with friends and general visitors; no job-search framing. Done. | This commit; push after completion |
| 2026-10-23 | LAUNCH-02 | User + Assistant | User configured the Cloudflare Tunnel published application route for `ejazhome.com`; public HTTPS request returned HTTP 200 and “Personal Website”. Done. | This commit; push after completion |
| 2026-10-23 | PIPE-01 | User + Assistant | Added push-triggered GitHub Actions publishing to GHCR and a site-only systemd update timer. Verified the server pulled and ran image revision `b2aa7f1`; the site returned HTTP 200 and the original CasaOS Watchtower is healthy. Done. | `023d973`, `6c0f3c5`, `b2aa7f1`; completion record in this commit |
| 2026-10-23 | HOST-02 | User + Assistant | Started the Docker service on the home server and confirmed LAN access returned HTTP 200. Done. | This commit; push after completion |
| 2026-10-23 | HOST-01 | User + Assistant | Added Dockerfile, Nginx config, Compose service, and ignore rules for the static Astro site on port 8085. Done. | This commit; push after completion |
| 2026-10-23 | BUILD-00 | User + Assistant | Initialized a minimal, empty Astro project with npm scripts, config, dependencies, and a blank root route. Done. | This commit; push after completion |
| 2026-10-23 | DOC-README-01 | User + Assistant | Added a README for the project status, agreed framework, proposed hosting direction, and project records. Done. | `996905b`, `663985d` |
| 2026-10-23 | DOC-AGENTS-02 | User + Assistant | Added the requirement to maintain a complete task history in this file. Done. | `43919fe` |
| 2026-10-23 | REPO-01 | User + Assistant | Connected this workspace to `talhaejaz07/personal-website` and pushed the project files. Done. | `9b1f38a`, `edbac83` |
| 2026-10-23 | DOC-AGENTS-01 | User + Assistant | Made project plan reading compulsory and added commit/push-after-each-task instructions. Done. | `9b1f38a` |
| 2026-10-23 | TECH-01 | User + Assistant | Selected Astro after the owner confirmed the site will include a blog. Done. | `edbac83` |
| 2026-10-23 | PLAN-INIT | Assistant | Created the project plan, initial scope, task tracker, and logs. Done. | `edbac83` |
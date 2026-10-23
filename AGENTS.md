# Project instructions

- Before starting project work, read `PROJECT_PLAN.md`. Reading it is compulsory; follow its current scope, decisions, task tracker, and open questions.
- Keep `PROJECT_PLAN.md` updated as tasks are started, completed, deferred, or descoped, including work the user completes or provides.
- Record the history of every project task in the **Task history** section below. Add one entry per task, including user-provided decisions and work, with its date, task ID, owner, outcome/status, and commit/push reference. Add new entries at the top; never erase completed history. Record the current task as `this commit` before its commit hash exists, then treat the resulting Git commit and push as its reference.
- After each task the user requests is completed, commit the project changes and push them to the GitHub repository. If GitHub access or a configured remote is unavailable, report the blocker and leave the changes committed locally when possible.

## Task history

| Date | Task ID | Owner | Task and outcome/status | Commit / push reference |
|---|---|---|---|---|
| 2026-10-23 | HOST-02 | User + Assistant | Started the Docker service on the home server and confirmed LAN access returned HTTP 200. Done. | This commit; push after completion |
| 2026-10-23 | HOST-01 | User + Assistant | Added Dockerfile, Nginx config, Compose service, and ignore rules for the static Astro site on port 8085. Done. | This commit; push after completion |
| 2026-10-23 | BUILD-00 | User + Assistant | Initialized a minimal, empty Astro project with npm scripts, config, dependencies, and a blank root route. Done. | This commit; push after completion |
| 2026-10-23 | DOC-README-01 | User + Assistant | Added a README for the project status, agreed framework, proposed hosting direction, and project records. Done. | `996905b`, `663985d` |
| 2026-10-23 | DOC-AGENTS-02 | User + Assistant | Added the requirement to maintain a complete task history in this file. Done. | `43919fe` |
| 2026-10-23 | REPO-01 | User + Assistant | Connected this workspace to `talhaejaz07/personal-website` and pushed the project files. Done. | `9b1f38a`, `edbac83` |
| 2026-10-23 | DOC-AGENTS-01 | User + Assistant | Made project plan reading compulsory and added commit/push-after-each-task instructions. Done. | `9b1f38a` |
| 2026-10-23 | TECH-01 | User + Assistant | Selected Astro after the owner confirmed the site will include a blog. Done. | `edbac83` |
| 2026-10-23 | PLAN-INIT | Assistant | Created the project plan, initial scope, task tracker, and logs. Done. | `edbac83` |







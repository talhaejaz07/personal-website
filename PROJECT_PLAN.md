# Personal Website — Project Plan and Task Tracker

This is the living project record for the personal website. It documents the work we agree to do, tracks who is doing it, and records decisions and completed work. Update it as the project changes so it remains the shared source of truth.

## Project at a glance

- **Project:** Personal website
- **Goal:** Plan, build, verify, and publish a personal website that represents its owner and serves the goals we agree on.
- **Current state:** The Astro homepage, blog index, and first MEBL article are live on the home server at `https://ejazhome.com/` through Cloudflare Tunnel. Homepage, blog, post, and title images returned HTTP 200 on 2026-10-23.
- **Technology:** Astro with npm, generating a static site; blog posts are authored as Markdown pages in `src/pages/blog/`.
- **Audience:** Friends and general visitors.
- **Purpose:** Introduce who the owner is, showcase social profiles, and share writing through a blog.
- **Content direction:** PSX investing is a major part of the owner's interests and existing content. He also wants to write about, and may make videos on, technology, engineering, green energy (including solar and batteries), and other subjects that interest him. The site should present investing as a major topic without making it seem like the only topic. The detailed bio remains private planning reference; only owner-approved selections belong on the site.
- **Initial topic areas:** PSX investing and financial analysis; technology, engineering, and green energy (including solar and batteries); and other topics the owner chooses to explore.

### Current visual system

The owner updated the color direction on 2026-10-23 using a reference screenshot, explicitly asking to take only its colors. Keep the existing site structure, typography, and content. Use near-black, off-white, and vivid red as the foundation while keeping long articles easy to read.

**Typography**
- **Display and hero headlines — Barlow Condensed, 600/700:** Use mostly uppercase for short hero statements and section titles. Its narrow, bold shapes echo the reference. Avoid it for paragraphs.
- **Body and interface — DM Sans, 400/500; use 600 for controls:** Use sentence case for article titles and body copy. Keep paragraph measure around 60–75 characters and line-height around 1.6 for comfortable long-form reading.
- **Financial data — DM Mono, 400/500, optional:** Use only for tickers, prices, ratios, dates, and compact data labels. Keep prose in DM Sans.
- **Small labels — DM Sans, 600, uppercase, modest tracking:** Use for categories such as “PSX NOTES” or “LATEST VIDEO”; do not apply wide tracking to paragraphs or tiny text.

**Color palette**
| Role | Color | Suggested use |
|---|---|---|
| Near-black | `#100F0F` | Main dark sections, header/footer, hero background |
| Dark surface | `#1B1918` | Cards and image overlays on dark sections |
| Off-white | `#F2F0EF` | Main reading background |
| White | `#FFFFFF` | Article cards and clean content panels |
| Vivid red | `#D94B3D` | Brand accent, links, outlines, small highlights |
| Deep red | `#B73A2E` | Accent text/buttons on light backgrounds where stronger contrast is needed |
| Text on light | `#201E1D` | Main body text on off-white/white |
| Muted text | `#706B69` | Secondary text on light backgrounds |
| Text on dark | `#F2F0EF` | Main text on near-black |
| Gain | `#2F7657` | Positive returns only |
| Loss | `#A64545` | Negative returns only |

Keep vivid red as the recognizable identity color, not as a signal for profit/loss. Pair every gain/loss color with a plus/minus sign or label so meaning does not rely on color alone. Use deep red for smaller text on light backgrounds and vivid red for accents on dark backgrounds.
- **Visual direction (updated 2026-10-23):** Keep the existing layout and typography (Barlow Condensed, DM Sans, and DM Mono). The owner selected only the near-black, off-white, and vivid red palette from a reference and explicitly excluded its layout and other design features. Retain green/red only for investment performance data.
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

- **Home:** Introduce PSX investing as a major interest alongside technology, engineering, and green energy; link to X and YouTube and feature recent writing.
- **About:** Personal background and interests, written in the owner's voice.
- **Blog:** Post index and individual articles.
- **Socials:** A curated list of social profiles, starting with [X](https://x.com/TalhaEjaz07ee) and [YouTube](https://www.youtube.com/@TalhaEjaz). More can be added later.

A separate projects or résumé page is outside the current plan. We can add a personal-interest page later if the owner wants one.

### Not yet specified

- Required pages and final copy
- Design references, colors, typography, and imagery
- Whether a CMS is needed later, beyond the current Markdown workflow
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
| COMMENTS-01 | Maintain | Add comments to individual blog posts | User + Assistant | Deferred | The owner decided the current readership is too small to justify a comment section and its moderation. Revisit if readership grows. Remark42 with Google sign-in was discussed as a possible future self-hosted option; no implementation now. |
| BLOG-05 | Maintain | Replace the induction-cooking article with the owner's supplied Markdown verbatim | User + Assistant | Done | Replaced the article body with the attached Markdown unchanged (12,797 bytes; SHA-256 matched the source). Updated only surrounding metadata and layout so the supplied heading appears once. Local build and GitHub Actions succeeded; the live article, Blog listing, and both images returned HTTP 200. Pushed `d76471e` to `main`. |
| CONTENT-03 | Review and refine | Broaden website copy to reflect investing plus technology, engineering, green energy, and other interests | User + Assistant | Done | Updated homepage, Blog index, writing guide, README, and project content direction. PSX investing remains a major topic; technology, engineering, green energy, and other interests are also represented. Existing blog post text remains unchanged. Pushed commit `ae548bd` to `main`. |
| CONTENT-02 | Review and refine | Review and revise public website copy outside blog posts against the writing guidelines | User + Assistant | Done | Revised vague or repetitive copy on the homepage and blog index, including page descriptions, topic summaries, and social-channel copy. Reviewed shared article navigation labels and kept them; all blog post Markdown remains unchanged. Pushed commit `a28595f` to `main`. |
| CONTENT-01 | Create pages and content | Consolidate writing guidance and add a reminder for future website and blog copy | User + Assistant | Done | Consolidated the three supplied files into `WRITING_GUIDELINES.md`, added the required read-before-writing reminder to `AGENTS.md`, linked the guide from the README, and pushed commit `14822f2` to `main`. |
| BLOG-03 | Maintain | Replace the MEBL article cover and card artwork | User + Assistant | Done | Converted the supplied 1254×1254 card image and 1774×887 cover to versioned WebP assets. Updated the MEBL post, shared card references, cover dimensions/ratio, alt text, and Open Graph image; article copy is unchanged. Pushed commit `99729aa` to `main`, triggering the existing publishing workflow. |
| BLOG-04 | Create pages and content | Finalise the induction-cooking article with current Pakistan price data | User + Assistant | Done | Rewrote the article, updated October 2026 LPG and current domestic piped-gas rates, corrected cost assumptions, added source links and cover/card WebP artwork, and clarified the LPG refill-cost note. Local build and GitHub Actions succeeded; the public post, Blog listing, and both images returned HTTP 200. Pushed `370d160` and final copy correction `1e8bc46` to `main`. |
| DESIGN-06 | Review and refine | Make the homepage header transparent | Assistant | Done | Added a transparent background override to Home only. Nav text colors are unchanged; blog and article headers retain their near-black background. Build and GitHub Actions passed; the live homepage computes to transparent while the blog header remains near-black. |
| DESIGN-05 | Review and refine | Clean up homepage footer spacing and correct the content layout | Assistant | Done | Reset inherited footer flex styles on Home so the social section and copyright row stack in the centered 1,200px content area. `npm run build` succeeded; GitHub Actions passed; public page serves the new CSS and rendered footer at 1,200px wide without horizontal overflow. |
| DESIGN-04 | Review and refine | Fix homepage header spacing and improve primary button text contrast | Assistant | Done | Reset inherited header padding/alignment on Home and use a deep-red primary button with off-white text. `npm run build` succeeded; GitHub Actions run 46 succeeded; public homepage returned HTTP 200 and serves the corrected stylesheet. |
| DESIGN-03 | Review and refine | Apply the owner-selected near-black/off-white/red palette and repair the homepage header layout | Assistant | Done | Updated Home, Blog, article, cards, and logo assets; versioned icon URLs to bypass Cloudflare cache. `npm run build` succeeded, GitHub Actions completed successfully, and public Home, Blog, article, CSS, and icons returned HTTP 200. |
| PIPE-01 | Prepare and launch | Build and publish the site image on each push to main, then automatically update the home-server container | Assistant | Done | GitHub Actions run for `b2aa7f1` succeeded; the enabled systemd timer pulled and ran that exact image revision. Site returned HTTP 200; original CasaOS Watchtower is healthy. |
| HOST-02 | Prepare and launch | Start the Docker service on the home server and confirm LAN access | User + Assistant | Done | Container running on port 8085; workstation received HTTP 200 from `192.168.18.100:8085` |
| HOST-01 | Prepare and launch | Add a Docker/Nginx production service on port 8085 | Assistant | Done | Multi-stage Astro build and static Nginx service added |
| BUILD-00 | Build the foundation | Initialize an empty Astro project scaffold | Assistant | Done | Installed Astro and added the root route, config, TypeScript config, npm scripts, and lockfile; no page content added |
| DOC-README-01 | Discover and define | Add a repository README describing project status, decisions, and project records | Assistant | Done | Added `README.md` |
| DOC-AGENTS-03 | Discover and define | Restore and preserve the complete project task history in `AGENTS.md` | Assistant | Done | Restored the complete prior task history after a documentation commit left the file empty; added and pushed the repair record |
| SOCIAL-01 | Plan the experience | Choose social profiles to feature in the first release | User | Done | X: `@TalhaEjaz07ee`; YouTube: `@TalhaEjaz` |
| DISC-01 | Discover and define | Confirm the website's purpose, audience, and desired visitor actions | User + Assistant | Done | Personal identity, social profiles, and writing for friends and general visitors; no job-search positioning |
| DISC-02 | Discover and define | Gather required content, pages, links, assets, and any existing brand material | User | In progress | X and YouTube links collected; PSX investing confirmed as the main focus, with technology and solar/batteries as secondary interests. Need approved short public bio and any images or brand references |
| DISC-03 | Discover and define | Agree on constraints, success criteria, target launch timing, and maintenance needs | User + Assistant | Not started | |
| PLAN-01 | Plan the experience | Draft the sitemap and navigation | Assistant, with User review | In progress | Draft proposes Home, About, Blog, and Socials; X and YouTube selected; review the structure and remaining content |
| PLAN-02 | Plan the experience | Agree on visual direction and page-level requirements | User + Assistant | Done | Owner approved the Barlow Condensed + DM Sans + optional DM Mono system and near-black/off-white/red palette on 2026-10-23 |
| PLAN-03 | Plan the experience | Identify accessibility, privacy, SEO, and performance requirements | Assistant, with User review | Not started | |
| TECH-01 | Choose the implementation approach | Select the site framework | User + Assistant | Done | Astro selected on 2026-10-23 |
| TECH-03 | Choose the implementation approach | Choose supporting dependencies and blog authoring/content workflow | User + Assistant | Done | Chose Astro Markdown pages in `src/pages/blog/`; article frontmatter supplies index and homepage card metadata, while Astro renders static HTML |
| TECH-02 | Choose the implementation approach | Select domain, hosting, and deployment workflow | User + Assistant | Done | `ejazhome.com` uses the existing Cloudflare Tunnel to reach the home server; GitHub Actions and the server systemd timer publish updates |
| HOME-01 | Create pages and content | Build the homepage using the approved visual system and owner-provided portrait | Assistant | Done | Responsive homepage added with PSX investing as the primary focus, X/YouTube links, secondary technology/green-energy interests, and an optimized transparent portrait. Build succeeded; live HTTPS returned HTTP 200 with the expected title and portrait asset on 2026-10-23 |
| HERO-02 | Create pages and content | Use the owner's updated portrait image in the homepage hero | User + Assistant | Done | Replaced the previous hero portrait with the newly supplied transparent image, optimized as an 1100×1100 WebP (150,568 bytes). Build succeeded; live homepage returned HTTP 200 and the hero asset returned HTTP 200 at 150,568 bytes on 2026-10-23 |
| FAVICON-01 | Create pages and content | Recolor and add the owner-provided logo as the site favicon | User + Assistant | Done | Recolored the mark to off-white and vivid red, retained the transparent logo master, created a 64×64 favicon and 180×180 Apple touch icon on near-black, and linked both in the page head. Build succeeded; live homepage and both icons returned HTTP 200 on 2026-10-23 |
| BUILD-01 | Build the foundation | Set up the project structure and shared site shell | Assistant | Not started | |
| BUILD-02 | Build the foundation | Implement responsive layout, navigation, and shared styles | Assistant | Not started | |
| BUILD-03 | Create pages and content | Build each agreed page and add owner-approved content and assets | Assistant, with User content/review | Not started | Add one task row per page/features once scope is agreed |
| BLOG-01 | Create pages and content | Implement the blog index, post pages, and agreed post-authoring workflow | Assistant, with User content/review | Done | Added `/blog/` and `/blog/mebl-stock-analysis/` as Markdown-driven static pages. Kept the supplied article text unchanged; 16:9 cover and square card image returned HTTP 200. Build succeeded and LAN/public pages returned HTTP 200 on 2026-10-23 |
| BLOG-02 | Create pages and content | Add a Blog link to the homepage header and show up to three latest posts on the homepage | Assistant | Done | Added the header link and date-sorted latest-three card section; the MEBL post appears on Home. Build succeeded and LAN/public homepage returned HTTP 200 on 2026-10-23 |
| REVIEW-01 | Review and refine | Review content, links, layout, and behavior on target screen sizes | User + Assistant | Not started | |
| REVIEW-02 | Review and refine | Address agreed accessibility, metadata, and performance findings | Assistant | Not started | |
| LAUNCH-01 | Prepare and launch | Configure production settings and deployment | Assistant, with User input as needed | Done | Docker on port 8085; GitHub Actions publishes the image and a systemd timer updates the server |
| LAUNCH-02 | Prepare and launch | Verify the live site and record launch details | User + Assistant | Done | User configured the Cloudflare Tunnel route `ejazhome.com` → `http://192.168.18.100:8085`; public HTTPS check returned HTTP 200 and title “Personal Website” on 2026-10-23 |
| MAINT-01 | Maintain | Record follow-up improvements and maintenance tasks | User + Assistant | Not started | Ongoing |

## User task record

Use this section to track work you complete or provide. Add the newest entry at the top. Link to files or relevant task IDs when possible.

| Date | Related task ID | Work you completed / provided | Outcome or evidence | Follow-up |
|---|---|---|---|---|
| 2026-10-24 | BLOG-05 | Supplied a Markdown file for the induction-cooking blog post and explicitly asked for its text to be used unchanged. | Replaced the article body byte-for-byte; verified matching 12,797-byte body, successful build/deployment, live article and Blog listing, and cover/card images. | Done |
| 2026-10-24 | BLOG-04 | Supplied an earlier article on induction cooktops and asked to update facts, improve the writing, and finalise it for publication today. | Rewrote and published the article with linked current sources, corrected cost comparisons, and new cover/card artwork. | Done |
| 2026-10-24 | COMMENTS-01 | Decided the current readership is too small to justify a comment section. | Deferred comment implementation; discussed Remark42 with Google sign-in as a possible future self-hosted option. | Revisit if readership grows |
| 2026-10-24 | CONTENT-03 | Clarified that investing should be a major part of the website, while writing and possibly making videos about technology, engineering, green energy, and other interests should also be represented. | Updated homepage and Blog index copy, writing guidelines, README, and project content direction; preserved current blog post text. | Done |
| 2026-10-24 | CONTENT-02 | Asked to review website copy outside the blog posts and update any text that clashes with the writing guidelines. | Revised vague or repetitive homepage and blog index copy; blog post text remains unchanged. | Done |
| 2026-10-24 | CONTENT-01 | Supplied good and weak writing examples plus general writing instructions, and asked for one cleaned-up guide with a reminder for future site writing. | Consolidated their transferable guidance for the site's personal voice, audience, and investing topics in `WRITING_GUIDELINES.md`. | Done |
| 2026-10-24 | BLOG-03 | Supplied new 2:1 and 1:1 images for the MEBL article and its cards. | Converted and applied as the MEBL article cover and shared card image; pushed to `main` in commit `99729aa`. | Done |
| 2026-10-23 | DESIGN-06 | Asked to remove `background: var(--near-black)` from `.site-header`, clarified that nav link colors should remain unchanged, then limited the change to the homepage. | Homepage header background computes to transparent; nav color is unchanged, and the blog header remains near-black. | Done |
| 2026-10-23 | DESIGN-05 | Shared a screenshot circling the footer and asked to clean up spacing and fix text crowding against the edges. | Footer rows now stack in the centered 1,200px container; verified on the live site with no horizontal overflow. | Done |
| 2026-10-23 | DESIGN-04 | Shared a screenshot circling the overlapping homepage header items and the dark text on the red hero button; asked to correct the header and lighten the button text. | Fixed the homepage grid overrides and changed the button to deep red with off-white text; public homepage and deployed CSS confirmed over HTTPS. | Done |
| 2026-10-23 | DESIGN-03 | Selected a near-black, off-white, and vivid red palette from a supplied reference and asked to use only its colors; reported that the homepage header was jumbled and requested updating palette references in Markdown docs. | Palette and responsive homepage header updated; README and project plan now reflect the new palette. Public Home, Blog, and article pages, the new CSS asset, and versioned icons returned HTTP 200. | Done |
| 2026-10-23 | BLOG-01 / BLOG-02 | Requested a blog page, Blog header link, homepage section with up to three latest posts, and supplied the complete MEBL article plus 16:9 and square title images; clarified that the article text must not be changed | Published the exact supplied copy as a Markdown article. The 16:9 image is the cover and the square image is used for cards; public Home, Blog, and article pages returned HTTP 200 | Done |
| 2026-10-23 | HERO-02 | Supplied an updated portrait and requested it be used in the hero section | Replaced the previous portrait; live homepage and 150,568-byte hero WebP returned HTTP 200 after deployment | Done |
| 2026-10-23 | FAVICON-01 | Provided the Talha Ejaz logo and asked to recolor it to the approved scheme, shrink it, and use it as the favicon | Logo recolored to off-white and red; live favicon and Apple touch icon returned HTTP 200 after deployment | Done |
| 2026-10-23 | HOME-01 | Supplied a portrait to use in the homepage hero and asked for a homepage based on the approved design reference | Portrait placed in the hero; homepage follows the approved fonts/colors and leads with PSX investing, with social links and supporting interests | Review the homepage and suggest any content or layout changes |
| 2026-10-23 | PLAN-02 | Approved the proposed typography and color scheme | Approved Barlow Condensed + DM Sans + optional DM Mono and the near-black/off-white/red palette, with green/red reserved for investment performance | Implement the approved visual system in the site foundation |
| 2026-10-23 | SOCIAL-01 | Chose X and YouTube as the social profiles to show for now | [X](https://x.com/TalhaEjaz07ee), [YouTube](https://www.youtube.com/@TalhaEjaz) | Add other profiles later if wanted |
| 2026-10-23 | DISC-01 | Clarified that the website is for personal expression, social profiles, and a blog; the audience is friends and general visitors | Agreed on a personal, interest-led site without job-search positioning | Share social profile links and content preferences in DISC-02 |
| 2026-10-23 | LAUNCH-02 | Added the `ejazhome.com` published application route in Cloudflare Tunnel | Screenshot shows the route to `http://192.168.18.100:8085`; live HTTPS check returned HTTP 200 | Continue site content and design work |
| 2026-10-23 | TECH-01 | Chose Astro after confirming the site will include a blog | Astro selected as the site framework | Markdown authoring workflow recorded in TECH-03 |

## Activity log

Record meaningful project progress here, including implementation and review work done by either of us. Add newest entries at the top.

| Date | Owner | Task ID | Update |
|---|---|---|---|
| 2026-10-24 | User + Assistant | BLOG-05 | Replaced the induction-cooking article with the attached Markdown byte-for-byte, adjusted the layout to show the supplied title once, and verified the deployed article, Blog listing, and images. Local build and GitHub Actions succeeded; all public routes returned HTTP 200. Pushed `d76471e` to `main`. |
| 2026-10-24 | User + Assistant | BLOG-04 | Rewrote and published the induction-cooking article, updated its price assumptions and sources, added wide and square artwork, and verified the live post, Blog listing, and images. Local build and GitHub Actions succeeded; public routes returned HTTP 200. Pushed `370d160` and final copy correction `1e8bc46` to `main`. |
| 2026-10-24 | User + Assistant | COMMENTS-01 | Deferred a comment system because the current readership does not justify the added infrastructure and moderation; recorded Remark42 as a possible future option. |
| 2026-10-24 | User + Assistant | CONTENT-03 | Completed the content-direction update across the homepage, Blog index, writing guidelines, README, and project plan. Existing blog post text remains unchanged. Pushed commit `ae548bd` to `main`. |
| 2026-10-24 | User + Assistant | CONTENT-03 | Started broadening the site copy and project records after the owner clarified that writing/video topics should include interests beyond investing. |
| 2026-10-24 | User + Assistant | CONTENT-02 | Completed the public-copy review and tightened the homepage and blog index text. Kept all blog post Markdown unchanged. Pushed commit `a28595f` to `main`. |
| 2026-10-24 | User + Assistant | CONTENT-02 | Started reviewing public-facing homepage and blog index text against `WRITING_GUIDELINES.md`; keep article copy unchanged. |
| 2026-10-24 | User + Assistant | CONTENT-01 | Completed `WRITING_GUIDELINES.md` for public-facing site and blog copy, added the read-before-writing instruction in `AGENTS.md`, and linked the guide from `README.md`. Pushed commit `14822f2` to `main`. |
| 2026-10-24 | User + Assistant | CONTENT-01 | Started consolidating the three supplied writing reference files into one project guide and adding a reminder to read it before future website copy or blog writing. |
| 2026-10-24 | User + Assistant | BLOG-03 | Completed the MEBL artwork update with versioned 1774×887 cover and 1254×1254 card WebP assets. Updated the article cover ratio, alt descriptions, and Open Graph image while leaving article copy unchanged. Pushed commit `99729aa` to `main`, triggering the existing publishing workflow. |
| 2026-10-24 | User + Assistant | BLOG-03 | Started replacing the MEBL post's cover and shared card artwork with the owner's newly supplied 2:1 and 1:1 images; preserve the article copy. |
| 2026-10-23 | Assistant | DESIGN-06 | Added a transparent background override to the homepage header only. Preserved the original nav text color and blog/article header backgrounds. `npm run build` succeeded; GitHub Actions passed; live homepage and Blog computed styles confirmed the homepage is transparent and Blog remains near-black. |
| 2026-10-23 | Assistant | DESIGN-05 | Inspected the live footer and traced its two-column jumble to global `.site-footer` flex rules leaking into the homepage footer. Reset the home footer to a block layout so its social and copyright rows stack inside the centered 1,200px content container. `npm run build` succeeded, GitHub Actions passed, and the live footer is deployed with no horizontal overflow. |
| 2026-10-23 | Assistant | DESIGN-04 | Measured the live header and traced the overlap to global blog CSS adding large horizontal padding and `space-between` to the homepage grid. Reset those inherited settings on Home and changed the primary button to deep red with off-white text. `npm run build` succeeded, GitHub Actions run 46 succeeded, and the public homepage returned HTTP 200 with the corrected stylesheet. |
| 2026-10-23 | Assistant | DESIGN-03 | Replaced the old palette with near-black, off-white, and vivid red across the homepage, blog index, article, cards, and favicon assets. Rebuilt the homepage header into a balanced desktop grid and a two-row mobile layout. Updated palette records in README and PROJECT_PLAN. Production build and GitHub Actions succeeded; public Home, Blog, article, stylesheet, and versioned icon URLs returned HTTP 200. |
| 2026-10-23 | Assistant | BLOG-01 / BLOG-02 | Added the Blog header link, date-sorted latest-three section on Home, Markdown blog index, and MEBL stock analysis page. Preserved the article copy as supplied. Used the square image for cards and the 16:9 image for the post cover. `npm run build` succeeded; LAN and public Home/Blog/article pages and the two images returned HTTP 200. |
| 2026-10-23 | Assistant | DOC-AGENTS-03 | Restored the complete `AGENTS.md` task history from commit `7b62106` after a documentation commit left the file empty; added a repair record and task references. |
| 2026-10-23 | User + Assistant | BLOG-01 / BLOG-02 | User supplied the MEBL article and two appropriately sized title images, requested a Blog header link, a blog index, and up to three latest post cards on Home, and specified the post text must remain unchanged. Started implementing the Markdown-based blog workflow. |
| 2026-10-23 | Assistant | HERO-02 | Replaced the hero image with the newly supplied transparent portrait. Converted it to an 1100×1100 WebP (150,568 bytes), visually checked it, and confirmed the live hero asset returned HTTP 200 at the expected size after server revision `b70ba1d`. |
| 2026-10-23 | Assistant | FAVICON-01 | Recolored the supplied logo to off-white and vivid red, retained a transparent master, generated compact favicon and Apple touch assets on near-black, and linked both in the page head. The logo accents were recolored again to match the updated vivid red palette as part of DESIGN-03. |
| 2026-10-23 | Assistant | HOME-01 | Built a responsive Astro homepage using the approved visual system and owner-provided portrait. Added PSX-focused hero copy, external X/YouTube calls to action, focus cards, channel section, concise introduction, metadata, and footer. Converted the transparent PNG to WebP for the hero; production build succeeded and the public page returned HTTP 200 with the expected title and portrait asset. |
| 2026-10-23 | User | PLAN-02 | Approved the proposed typography and color scheme: Barlow Condensed + DM Sans + optional DM Mono, near-black/off-white/red palette, and restrained green/red for investment performance. |
| 2026-10-23 | User + Assistant | PLAN-02 | User supplied the target visual reference and requested typography and color recommendations. Proposed Barlow Condensed + DM Sans + optional DM Mono, with near-black, off-white, vivid red, and restrained gain/loss colors; pending owner approval. |
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
| 2026-10-24 | Defer blog comments until readership grows enough to justify them. | The current audience is too small to warrant comment infrastructure and ongoing moderation. | Keep the blog without comments for now; reconsider if readership grows. Remark42 with Google sign-in is a possible future self-hosted option. |
| 2026-10-24 | Feature PSX investing prominently while representing technology, engineering, green energy, and other interests as content topics too. | The owner clarified that he wants to write about, and may make videos on, interests beyond investing. | Ensure homepage and Blog copy reflect this range without implying investing is the only subject. |
| 2026-10-24 | Use `WRITING_GUIDELINES.md` as the shared reference for future public-facing website and blog writing. | The owner supplied three writing reference files and asked for one cleaned-up guide with a reminder for future work. | Read the guide before writing or editing site copy; follow task-specific instructions and exact-copy requirements first. |
| 2026-10-23 | Use near-black (`#100F0F`), off-white (`#F2F0EF`), and vivid red (`#D94B3D`) as the website palette. | The owner selected only these colors from a supplied reference and explicitly excluded its layout and other design features. | Keep the existing site layout and typography; use deep red for small text on light backgrounds and reserve performance colors for financial data. |
| 2026-10-23 | Author blog posts as Markdown pages under `src/pages/blog/`. | The site uses Astro and the owner asked to publish a first long-form post. | Astro generates static post pages; frontmatter drives the blog index and homepage cards without client-side JavaScript. |
| 2026-10-23 | Preserve the MEBL article text exactly as supplied by the owner. | The owner explicitly instructed not to change the blog text. | Present the provided title, analysis, tables, YouTube links, and disclaimer without editorial changes. |
| 2026-10-23 | Use the newly supplied transparent portrait as the homepage hero image. | The owner requested this image for the hero section. | Optimized the portrait as `public/images/talha-ejaz-hero.webp`; verify the live site after deployment. |
| 2026-10-23 | Use the owner-provided TE logo as the favicon, recolored in off-white and vivid red on a near-black tile. | The owner requested a smaller, palette-matched version of the supplied transparent logo for the favicon. | Keep the transparent recolored master in `public/images`; serve `public/favicon.png` and `public/apple-touch-icon.png` from the page head. |
| 2026-10-23 | Use the owner-provided portrait in a dark, editorial hero and structure the homepage around PSX investing, social channels, and supporting interests. | The owner requested the portrait for the hero and a homepage inspired by the supplied reference; the project plan establishes PSX investing as the leading content focus. | First homepage uses the approved visual system and links to X and YouTube; review the page before expanding into the blog and other pages. |
| 2026-10-23 | Approve the proposed Barlow Condensed + DM Sans + optional DM Mono type system and near-black/off-white/red palette, with gain/loss colors reserved for investment performance. | The owner approved the visual recommendations for the site. | Use this system as the design foundation; verify text contrast and responsive typography during implementation. |
| 2026-10-23 | Feature X (`@TalhaEjaz07ee`) and YouTube (`@TalhaEjaz`) as the initial social links. | The owner selected these profiles for now. | Show them on the Home and Socials pages; additional profiles can be added later. |
| 2026-10-23 | Shape the website around personal identity, social profiles, and blog writing for friends and general visitors. | The owner wants the site to show who they are and share their writing. | Use an interest-led personal brand without job-search positioning; review the proposed Home, About, Blog, and Socials pages. |
| 2026-10-23 | Publish container images with GitHub Actions and use a systemd timer on the home server to pull updates every 60 seconds. | The server should update from Git pushes without exposing a new inbound service; running a second Watchtower conflicted with CasaOS's existing Watchtower. | The timer updates only `personal-website`; GHCR package is publicly pullable. |
| 2026-10-23 | Host the static Astro site on the Ubuntu home server and publish through the existing Cloudflare Tunnel at `ejazhome.com`. | The owner already runs a Cloudflare Tunnel and configured a published application route for the website. | The route sends requests to `http://192.168.18.100:8085`; public HTTPS returned HTTP 200. |
| 2026-10-23 | Use Astro to build the personal website and blog. | The owner plans to add a blog; Astro can generate static pages suitable for the home server. | Choose supporting dependencies and the blog authoring workflow in TECH-03. |
| 2026-10-23 | Use this file as the shared project plan and task tracker. | Requested by the project owner. | Keep the tracker and logs updated as work proceeds. |

## Open questions and blockers

Add questions that need an answer and blockers that prevent progress. Remove or mark entries resolved when addressed.

- [ ] Which pages and content should the first version include?
- [ ] Is there a target date or other constraint we should plan around?

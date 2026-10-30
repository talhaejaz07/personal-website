# Design system — DESIGN-07

2026-10-29 · Styling and layout refinement

## Intent and boundaries

The site should feel like a considered personal publication: confident enough to support company research and engineering analysis, but quiet enough to suit the owner's direct, personal writing. Its character comes from proportion, typography, alignment, and the supplied portrait and article artwork. The owner's follow-up makes mobile visitors the priority. This redesign preserves public-facing text, article Markdown, links, metadata, and supplied images. Astro and Cloudflare Pages remain the foundation.

## What the review found

The previous hierarchy gave nearly every section a large condensed headline with tightly compressed leading, sometimes below 0.8. Meanwhile, navigation and supporting labels shrank to 7–10px. This made decorative statements compete with the actions and information visitors needed to read. Angular background shapes, large translucent initials, repeated shadows, and frequent bright red headings amplified that imbalance.

There was also a structural cause of past layout inconsistencies: eager Markdown imports brought the article layout's global CSS into Home and the blog index. Repeated header, footer, navigation, and root declarations then depended on stylesheet order. The implementation addresses this source of interference alongside the visual changes.

## Composition and spacing

The new language uses open editorial columns, thin rules, square image edges, and deliberate empty space. Focus items and article previews sit on the page rather than in repeated elevated boxes. Red marks selected points of emphasis; it no longer carries every headline.

The shared maximum page width is **1,240px**. Side gutters use `clamp(20px, 4.5vw, 80px)`, giving a 320px viewport a usable 280px content column. Major section spacing scales from **72px to 132px**. Related elements use smaller, consistent gaps so hierarchy remains apparent without extra decoration.

The desktop hero separates copy and portrait into two columns beneath the retained transparent Home header. The portrait sits on a quiet dark surface with a short red rule. Below 760px, it follows the introduction and links. Small-screen navigation gets its own row rather than smaller targets. Article grids move from three columns to two or one as space permits; the homepage writing list becomes one column below 760px.

## Typography

The established families remain, with clearer roles and more comfortable leading:

| Role | Treatment |
|---|---|
| Display | Barlow Condensed, predominantly weight 600, preserving supplied sentence case; hero up to 104px, approximately 52–72px on narrow screens |
| Section headings | Barlow Condensed, generally 50–76px on desktop and 44–56px on mobile; leading around 1.04–1.08 |
| Article titles | Barlow Condensed, 40–80px across breakpoints, with 1.05 leading |
| Body and interface | DM Sans; homepage supporting copy 15–16px, article prose 18px desktop and 17px mobile |
| Metadata | DM Mono for dates, category labels, and compact supporting information; generally 10–11px |
| Navigation and actions | DM Sans, 11–13px, with generous interactive areas |

Article prose has a maximum width of **720px** and 1.8 line-height. Card titles use 30–35px type with 1.12 leading. Fallbacks remain available, with a size-adjusted display fallback and wrapping to avoid clipping. Five same-origin WOFF2 assets total **99,560 bytes**, with Open Font License notices retained. Barlow Condensed 600 and variable DM Sans are preloaded; Google Fonts stylesheet links are removed. Browser inspection confirmed four used fonts loaded locally.

## Color and interaction

The retained core palette is near-black `#100F0F`, off-white `#F2F0EF`, vivid red `#D94B3D`, deep red `#B73A2E`, and ink `#201E1D`. Muted copy uses `#706B69` on light surfaces and `#B9B3AF` on the principal dark background. Rules use subdued neutral tones.

Deep red supports links on light backgrounds; vivid red supplies small accents on near-black. The YouTube card label changed to off-white after checking its original red-on-card contrast, which was only about 3.96:1. Hover states use subtle color, underline, or arrow changes. Focus outlines stay visible, the skip links remain, and reduced-motion preferences disable transitions and smooth scrolling. These choices are specific improvements, not a claim of complete WCAG AAA conformance.

## Reading and maintenance

The shared `BlogCard` keeps square artwork intact, places its category below the image, and gives titles and descriptions room to breathe. Article pages preserve title → cover → body order. Tables scroll within the reading column, with practical cell widths and tabular numerals, rather than widening the page. Links remain underlined in prose.

`global.css` owns tokens and the shared foundation. `home.css` is scoped beneath `.home-page`; journal and article rules in `journal.css` are scoped beneath `.journal-page` and `.article-page`. Component styling stays with `BlogCard`. Future additions must follow these boundaries: a Markdown layout may be imported indirectly, so its presence must never restyle unrelated pages.

## Verification record

The production build passed all five routes. A 20-case browser matrix—every route at 320, 390, 768, and 1,440px—passed page-overflow checks, showed one visible H1 per page, and retained navigation targets of at least 44×44px. Home also passed 360, 430, and 1,024px. These are simulated viewports, not physical-device tests. All 20 checked local page/asset URLs returned HTTP 200. Keyboard ArrowRight moved a table's local scroll position by 40px; focus outlines and the skip link were verified. Reduced-motion emulation confirmed automatic scrolling and zero-duration button transitions. Non-style Astro source, article Git blobs, and existing images remain unchanged. MEBL's working checkout uses CRLF while its stored Git content is unchanged. Implementation `210f02f` was pushed to `main` and deployed through the existing Cloudflare Pages pipeline. All five live pages and 23 checked page/asset URLs returned HTTP 200 and matched the local production build byte-for-byte.


## Homepage hero update — 2026-10-30 (HERO-03)

The owner supplied a dark portrait-and-name reference and requested a more attractive hero. This supersedes the earlier separate portrait column for the hero only. Large Barlow Condensed name lettering and a red interests subtitle share a stage with the existing transparent portrait. The rectangular image panel and decorative research labels are removed. Narrow screens retain the overlap with the face above the name and supporting copy below. Existing palette, fonts, portrait bytes, supporting copy, all other sections, and articles remain intact. No client-side scripts or new assets were added.

Validation: all five routes build; browser checks at 320, 360, 390, 430, 760, 768, 1024, and 1440px show no page overflow and a fitting H1. Hero navigation and actions meet 44px targets, and scroll navigation reaches Focus. Viewports are simulated browser sizes.

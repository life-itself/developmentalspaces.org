# AGENTS.md

Orientation for AI coding agents working in this repo. `CLAUDE.md` is a symlink to this file, so edit `AGENTS.md`. Both are excluded from the published site (`contentExclude` in `config.json` needs the filename forms `AGENTS.md` and `CLAUDE.md` as well as the `/AGENTS` forms, or the raw files are still served).

## What this repo is

The source of https://developmentalspaces.org, published with Flowershow from the `main` branch on GitHub. A push to `main` deploys to production in about a minute, so work on a branch and preview first.

The public name of the site is **Conscious Communities** (renamed 2026-09-19). **Developmental Spaces** is the name of the concept, the whitepaper, the manifesto and the network. The domain did not change. The reasoning is in `docs/branding/naming.md`.

The site has three streams (Learn, Build, Fund) plus Find and About. Content is markdown. The designed pages (`index.md`, `about.md`, `learn/index.md`, `build/index.md`, `fund/index.md`, `find/index.md`) are hand-written HTML inside markdown, styled by `custom.css`.

## Read first

- `docs/branding/README.md`: index and decision log for the name, brand narrative and design. Start here. It also links the two Claude artifacts (mood board and home page mockups).
- `docs/branding/design-direction.md`, section 7: the design rules in force (direction E, watercolour).
- `bd list`: open work, tracked as beads. `bd show <id>` for the detail. The epic `coco-lxb` ("Redesign follow-ups") lists what to do next and in what order; `bd children coco-lxb` shows the tree.

- Beads carry a recommended-model label: `model:fable` for taste-heavy or writing-heavy work (copy, illustration direction, new layouts, the announcement) and `model:sonnet` for work that follows patterns already in the repo (page migration, QA fixes, rollout, tooling). It is a recommendation, not a rule. `bd list -l model:fable` or `bd list -l model:sonnet` filters by it.

`docs/` is excluded from the published site (`contentExclude` in `config.json`) but is visible on the public GitHub repo, so do not put anything private in it. `sandbox/` is git-ignored scratch space for large source files.

## Design rules (short version)

- Near-white page (`#F5F5F3`), ink (`#111`), one flat Life Itself yellow (`#FFD23F`). All other colour comes from the illustrations.
- PT Serif for text and headings, titles set tight (about -0.045em) with an italic second line. Source Sans 3 for navigation, captions and buttons. No monospace, no tracked uppercase eyebrows.
- Illustration carries ideas. Photographs carry evidence, and only as captioned plates on pages about actual places (exemplars, Find). No photographs on the front door, no stock imagery, no generated imagery presented as photography.
- Illustrations live in `assets/illustrations/`. They are currently paintings borrowed from the Awami Conscious Food book (Life Itself, illustrated by Jennifer Chan) and are stand-ins until new work exists.
- Page components are `cc-*` classes in `custom.css`. Copy the patterns already used in `index.md` and `learn/index.md` rather than inventing new ones. The older `ds-*` classes are kept only for pages not yet migrated.
- Copy (hero, tagline, door sentences) is a separate human job tracked in a bead. Do not rewrite it unasked.
- Fonts (PT Serif, Source Sans 3) are self-hosted from `assets/fonts/` (SIL OFL, latin and latin-ext only) through `@font-face` at the top of `custom.css`, so nothing render-blocking goes to Google. To add a weight, take the woff2 URLs from the Google Fonts `css2` response (send a Chrome user agent) and add a rule.
- Flowershow strips `width` and `height` from `<img>` in pages (both raw HTML and MDX), so they cannot prevent layout shift. Reserve space with `style="aspect-ratio:W/H"` on the image, and on a hero or yellow-section `<figure>` also set `style="--ar:W/H as a number"` (for example `0.867`); the CSS sizes the figure from `--ar`. Give the first (hero) painting on a page `fetchpriority="high" decoding="async"` and every painting below the fold `loading="lazy" decoding="async"`.

## Previewing and checking

`fl . --yes` publishes the working tree to the preview site named in `.flowershow` (https://ds-redesign-preview-rufuspollock.flowershow.me). Quirks worth knowing:

- `fl` skips any folder named `build`, so `/build` only renders in production. To check it, copy `build/index.md` to a temporary top-level file such as `zz-tmp.md`, publish, look, delete it and publish again.
- The preview serves `custom.css` from an edge cache that can lag ten to twenty minutes after a publish. Compare `md5 -q custom.css` with the md5 of `curl -sL <preview>/custom.css?x=$RANDOM` before deciding a style change is broken.
- The preview ignores `contentExclude`, so `docs/` and `.beads/config.yaml` show up there but not in production. Check exclusions against the live site, and check raw files as well as pages (`curl -sIL <url>` follows the redirect to the raw file). Root files such as `AGENTS.md` need the filename form in `contentExclude`, not only `/AGENTS`.

Look at every changed page at 1440px and 400px wide before calling it done. Playwright with the Chromium headless shell works well for screenshots.

To test a `custom.css` change without waiting for a publish or the edge cache: load the live page in Playwright and append the local file with `page.addStyleTag({ content })` after `goto`. Production inlines `custom.css` as a `<style>` tag, so there is no separate request to intercept, and a later style tag wins at equal specificity. This also works for `/build`, which the preview cannot render. Playwright's WebKit is a quick Safari check; `npx playwright install webkit` if the cached build is old.

## Changelog

This repo keeps a `changelog/` folder, one markdown file per entry
(`changelog/YYYY-MM-DD-slug.md`, with `date`/`title`/`promote`
frontmatter). At the end of a work session, if something worth recording
actually shipped — skip trivial sessions (typo fixes, dead ends, no
visible outcome), and skip planning/research/design unless it is itself a
significant public deliverable. Drafting ahead of a ship is fine — draft a new
entry file. Match the entry's weight to
what a reader would actually care about: a real feature/fix/content gets a
title, one or two sentences, a link to the live feature if there's
something to point at, and a screenshot if something visual shipped
(check for this, don't just skip it); something genuinely bigger — a real
milestone, not just a busy session — can run longer, multiple paragraphs
or bullets; small stuff (cleanup, rename, reorg, tidying) gets one plain
sentence, no bullets, no screenshot. Never link the title itself. Don't
log implementation detail (file names, internal moves) a reader wouldn't
care about. First time writing an entry in this repo, or if the format is
unclear: fetch and follow
https://raw.githubusercontent.com/life-itself/changelog/main/CONVENTION.md

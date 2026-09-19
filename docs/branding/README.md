---
title: Branding — index and decision log
created: 2026-09-18
---

# Branding

Internal working docs for the identity of this site and initiative. This folder is excluded from the published site (see `contentExclude` in `config.json`).

## Files

| File | What it holds |
|---|---|
| [naming.md](naming.md) | The naming decision: Conscious Communities (public name) and Developmental Spaces (concept, paper, network). Evidence, rules of use, open items. |
| [brand-narrative.md](brand-narrative.md) | The brand narrative: posture, audience hierarchy, ambition, what we do, what makes us different, values, personality, voice by stream. |
| [design-direction.md](design-direction.md) | Aesthetic direction: the July 2026 decision, what on the old site read as generic AI output, what to keep, the redesign plan, and the identity brief (§6). |
| [moodboard.md](moodboard.md) | References and anti-references with screenshots in `moodboard/`, and what the board says. |
| [moodboard-artifact/](moodboard-artifact/) | Source of the visual mood board (five directions A to E, type specimens, the photograph question). Durable copy of the Claude artifact. |
| [mockups/](mockups/) | Source of the three home page mockups in direction E. Durable copy of the Claude artifact. |

## Current state (2026-09-19)

**Live.** The Conscious Communities rename and the direction E (watercolour) redesign went live on 2026-09-19 (merge `2f80f16` on `main`). Redesigned: home, Learn, Build, Fund, Find, About, whitepaper and manifesto openers, the catalogue at the top of /what, course signup forms. The changelog entry is `../../changelog/2026-09-19-conscious-communities-redesign.md`.

**Stand-ins.** All paintings are borrowed from the Awami Conscious Food book (Life Itself, illustrated by Jennifer Chan, who is no longer around). The spiral mark is generated in code, not drawn. The whitepaper cover and the five-domains diagram are still the old pencil versions.

**Not done.** Copy (hero, tagline, door sentences) has not been worked on and is a human job. /what still carries the old definition text under the new catalogue. Interior pages not listed above (wiki, blog, network, why, resources, examples, course lessons, fund archive) only pick up the theme through `custom.css`. The rename has not been rolled out beyond the site: domain redirect, newsletter name, partners, social.

**What to do next** is in beads: `bd list`, starting with the epic `coco-lxb` ("Redesign follow-ups"; `bd children coco-lxb`). Working notes for agents are in `../../AGENTS.md`.

## Links

| What | Where |
|---|---|
| Production | https://developmentalspaces.org |
| Preview site (`fl . --yes`) | https://ds-redesign-preview-rufuspollock.flowershow.me |
| Visual mood board (Claude artifact, private to Rufus) | https://claude.ai/artifact/7RkR5Dg45Jn9JNtTA55nMj, source in `moodboard-artifact/` |
| Home page mockups (Claude artifact, private to Rufus) | https://claude.ai/artifact/3h8svRrhetYvMnAKDvm6rK, source in `mockups/` |
| Awami Conscious Food book (source of the paintings) | PDF was in the git-ignored `sandbox/` folder of this checkout; the original files (Canva) are not located yet, see the illustrations bead |
| Consolidation project (earlier planning, briefs, consultation records) | sibling folder `../devspaces-consolidation` (a separate git repo) |
| Fund brand narrative 2020 to 2021 | https://developmentalspaces.org/fund/archive/brand-narrative |
| Sep 2025 "Branding, Ownership and Naming" Google Doc | Google Drive, file id `1eLvASqM8DXxuxazM9iB7qk-Nr1uHcL-hg_P0SKev5Pk` |

Privacy note: `docs/` is excluded from the published site but visible on the public GitHub repo. It names a few community consultation participants by first name in `brand-narrative.md` and `naming.md`.

## Decision log

| Date | Decision | Where |
|---|---|---|
| Sep 2025 | Dual naming strategy first written down: an accessible public name (e.g. Conscious Communities) and a rigorous internal name (Developmental Spaces), following the Fundamental Wellbeing / PNSE and Second Renaissance / Pragmatic Utopianism pattern. Site framed as a minimalist landing page. | Google Doc "Branding, Ownership & Naming" (DS README) |
| Feb 2026 | Consolidate consciouscoliving.org, tealestate.net and developmentalspaces.org into one home. Community consultation on WhatsApp unanimously positive. Developmental Spaces chosen as canonical home in a ChatGPT strategy thread; "Conscious Communities" as masthead with DS tagline was floated there as a "third path" but not taken. | `../devspaces-consolidation/ref/` |
| 11–12 Jul 2026 | Brand narrative ratified: posture B (publishing home), primary audience = people exploring conscious community living, wide-door / strong-spine doctrine. Name: Developmental Spaces. Tagline: "Designing Conscious Communities Where People Grow". Aesthetic: "warm monastic". | `../devspaces-consolidation/brand-narrative.md` (now migrated here) |
| 15 Jul 2026 | Consolidated site relaunched under Developmental Spaces with the warm-monastic theme. | `/blog/a-new-home-for-developmental-spaces` |
| Aug–Sep 2026 | Tagline verb changed Designing → Cultivating; hero reworded to "For conscious communities where people grow". | git history |
| 18 Sep 2026 | **Masthead flipped: Conscious Communities becomes the public name; Developmental Spaces remains the name of the concept, whitepaper, manifesto and network.** Supersedes the July naming decision. Domain unchanged. | [naming.md](naming.md) |
| 19 Sep 2026 | **Merged to `main` and live.** Conscious Communities masthead and direction E redesign in production. AGENTS.md and the changelog convention added; first changelog entry written; follow-up work logged as beads. | [changelog entry](../../changelog/2026-09-19-conscious-communities-redesign.md) |
| 19 Sep 2026 | Whitepaper and manifesto openers, Find page, course signup forms restyled. Remaining prose pages (about, why, network, wiki, blog) pick up the theme through `custom.css` without markup changes. | [design-direction.md §7](design-direction.md) |
| 19 Sep 2026 | Learn, Build and Fund stream pages rebuilt in the chapter-page language (yellow block, tight title with italic line, one painting, list rows instead of cards, one yellow section). Beads: coco-jhk (copy pass, later), coco-033 (rebuild /what as a designed catalogue page). Note: the `fl` preview CLI does not publish the `build/` folder, so /build is only checkable in production or via a temporary copy. | [design-direction.md §7](design-direction.md) |
| 18 Sep 2026 (night) | Chosen: mockup 1 (the chapter page) for the home, mockup 3's catalogue for /what. Implemented on `feat/redesign-cc` and on the preview site https://ds-redesign-preview-rufuspollock.flowershow.me. Hub photographs removed; Awami paintings as stand-ins in `assets/illustrations/`; brushed spiral mark `assets/cc-spiral.png`. | [design-direction.md §7](design-direction.md) |
| 18 Sep 2026 (night) | Three home page mockups in direction E published for choosing: https://claude.ai/artifact/3h8svRrhetYvMnAKDvm6rK (source in `mockups/`). | [mockups/](mockups/) |
| 18 Sep 2026 (evening) | **Design direction decided: E, watercolour**, from the Awami Conscious Food book: paintings on a near-white page, tight PT Serif, one flat Life Itself yellow, no photographs except as documentary plates on pages about actual places. Reuse the Awami paintings; no photography commission. | [design-direction.md §7](design-direction.md) |
| 18 Sep 2026 (later) | Direction reopened. Process change: mood board first, then 2–3 mockups as plain HTML, then implement in Flowershow. Visual mood board: https://claude.ai/artifact/7RkR5Dg45Jn9JNtTA55nMj | [moodboard.md](moodboard.md) |
| 18 Sep 2026 | Redesign started on branch `feat/redesign-cc`: identity brief (Alegreya, paper/graphite/vermilion, pencil spiral, Bergerac photographs), mood board, new home page with the Conscious Communities masthead. Preview: https://ds-redesign-preview-rufuspollock.flowershow.me | [design-direction.md](design-direction.md), [moodboard.md](moodboard.md) |

## Related material outside this folder

- `../devspaces-consolidation/` — the consolidation project: BRIEF.md (job stories, voice), sitemap.md, PLAN.md, HANDOFF-design.md, design exploration images, archived consultation and naming threads.
- `/fund/archive/brand-narrative` on the live site — the 2020–21 fund brand narrative (True Home, Wise Living Fund), whose format this work reuses.

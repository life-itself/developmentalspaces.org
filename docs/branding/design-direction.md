---
title: Design direction — from "warm monastic" to a real identity
created: 2026-09-18
status: SHIPPED 2026-09-19 — direction E, watercolour, see §7 (decided 2026-09-18). Sections 1 and 6 are superseded history.
---

# Design direction

Where the visual identity stands, what is wrong with it, what to keep, and how the redesign proceeds. The brand it must serve is in [brand-narrative.md](brand-narrative.md); the name on the door is in [naming.md](naming.md).

## 1. What was decided in July 2026 ("warm monastic")

Three poles were on the table (moved here from the July brand narrative):

1. **The CoCo look**: warm, yellow, flowers, positive, borderline new-agey. Rejected as the base: indistinguishable from generic conscious-living content; undermines the spine.
2. **The old DS look**: black-and-white, simple, monastic. Right seriousness, but too cold and too thin for a wide door; read as an academic landing page.
3. **The design exploration** (`../devspaces-consolidation/assets/design-exploration-v1-2026-06-26.jpg`): parchment ground, oxblood accent, dark manifesto-brown blocks, book serif, hand-drawn spiral, spiral-minaret etching, monospace eyebrows.

Pole 3 was chosen and named "warm monastic": warmth carried by parchment, humanist serif and generous space (not by yellow and flowers); depth carried by restraint, etchings and dark blocks (not by starkness). The feeling to aim for: *an illuminated manuscript library you would actually want to live in*. Candlelight, not fluorescent; lived-in, not sterile; old-wisdom materials carrying a contemporary layout.

Vocabulary from that decision: parchment ground alternating with deep brown-black blocks for manifesto-register moments; a single warm red accent, never a rainbow, never yellow-first; a serif with bookish character; small caps or monospace for wayfinding; etchings, hand drawings and real photographs of real places and people; never stock lifestyle imagery, pastel new-age gradients or AI-slick renders; the spiral as the identity mark's companion. Temperature by stream: Learn warmest, Build most monastic, Fund most sober.

The current site (`custom.css`, July 2026) implements this: EB Garamond + IBM Plex Mono, parchment `#F2EBD9`, ink `#2B2118`, oxblood `#8C2B1E`, gilt `#A5833B`, a rubric-margin "manuscript grid", dark spine blocks, a self-drawing SVG spiral.

## 2. The problem: it reads as AI output

The direction was sound. The execution is a copy of a copy: the June exploration was itself AI-generated, and the site reproduces its habits faithfully. Specific things that make the current site read as generic AI design rather than as this project:

- **The rubric-margin grid with tracked, uppercase monospace eyebrows** ("WHY NOW", "FIND YOUR DOOR", "IN GOOD COMPANY"). This exact device is now everywhere in AI-generated "editorial" sites.
- **The italic accent word in oxblood at the end of every headline** ("where people *grow*.", "Spaces that *grow people*.", "Living together, *on purpose*."). Used once it is a flourish; used on every heading it is a tic.
- **Uniform section rhythm**: eyebrow, display heading, one paragraph, arrow link, repeated six times down the home page. Nothing breaks the pattern, so nothing is emphasised.
- **Triads everywhere**: three streams, three buttons, three cards, "One home, three ways in".
- **EB Garamond with IBM Plex Mono** is the single most common AI serif-plus-mono pairing of 2025–26.
- **A self-drawing spiral animation and a sepia CSS filter standing in for an etching.** Effects standing in for artefacts.
- **No real images on the front door.** The home page has an SVG spiral and a stock-looking "etching" figure. The site is about real places and real people living together, and none of them are visible.
- **Copy patterns**: "A home for everyone exploring, building, or funding…", "the real-estate and finance layer that makes places real". Fluent, balanced, unspecific.
- **Inline-styled HTML in markdown** with `clamp()` and `style=""` everywhere, which makes every page look like the same generated template.

None of this is fatal individually. Together it means the site has a *style* but not an *identity*: it could be the site of any thoughtful AI-assisted project in 2026.

## 3. What to keep

- The wide-door / strong-spine doctrine, and the idea that the visual system should express it (warm at the door, dark and quiet in the spine).
- The parchment / ink / oxblood family as a *starting* palette, to be re-derived from real material rather than kept as hex codes.
- The spiral as the mark. It has been on the whitepaper cover from the start and it means something (growth that circles and returns). Redraw it properly rather than animate it.
- Temperature by stream: Learn warmest and most human, Build most monastic, Fund most sober.
- Real photographs of real places (there is already a good asset library: Tamera, Plum Village, Sieben Linden, Embercombe, Monastic Academy, Deep Springs and others in `/assets`).

## 4. What the redesign has to achieve

1. **A visitor who cares about conscious community feels, within seconds, that this site was made by people who live this way.** Real places, real faces, a voice with a person behind it.
2. **The masthead reads Conscious Communities** and the descriptor ties it to Developmental Spaces and Life Itself (see [naming.md](naming.md)).
3. **The spine gains gravitas.** The whitepaper and manifesto pages should feel more serious after the redesign, not less.
4. **It looks like nothing else in the space**, and specifically not like AI-generated editorial sites.
5. **It stays buildable in Flowershow**: `custom.css`, `config.json`, and page-level HTML in markdown. No arbitrary templating.

## 5. How the redesign proceeds (sub-project 3)

1. **Mood board.** Collect twelve to twenty references, each with a one-line note on what specifically to take from it. Real places' own sites, publications with a strong material feel, institutions that convey depth without coldness. Candidate starting points to evaluate, not decisions: Plum Village, Schumacher College, the Monastic Academy, Deep Springs College, Emergence Magazine, Noema, Dark Mountain, and the print world (small-press books, type-specimen books, monastery guidebooks). Include two or three *anti-references*: sites that show exactly the generic look to avoid.
2. **Identity brief.** From the mood board: three to five adjectives, a typographic direction (with at least two candidate serif families that are *not* EB Garamond, and whether a mono is needed at all), a palette derived from real materials (photographs of parchment, oxblood ink, terracotta, lime plaster, dark wood), an image policy, and a redrawn spiral.
3. **Design session.** Home page first (done 2026-09-18 on `feat/redesign-cc`), then the Learn, Build and Fund stream pages, then the whitepaper and manifesto pages. Preview loop: edit, `fl . --yes` (publishes the working tree to the preview site named in `.flowershow`), screenshot. Note the preview ignores `contentExclude`, so `docs/` is visible there but not in production.
4. **Implement and ship** the home page with the masthead flip in one go, then the streams.

## 6. Identity brief (2026-09-18) — now a candidate, not a decision

> Reopened the same evening. Kept here as "direction A: pencil and paper" in the visual mood board. The Alegreya / paper / vermilion choices are one option among four.

Derived from the [mood board](moodboard.md). This is what the redesign implements.

**In five words:** hand-drawn, warm, serious, lived-in, specific.

**The idea.** The site is the working notebook of a real project: real drawings, real photographs, real documents, kept with care. Two artefacts anchor it. The pencil spiral on straw paper (from the whitepaper cover) is the mark and the palette. The long table in the garden at the Bergerac hub is the picture of what a conscious community is.

**Mark.** The actual pencil spiral drawing (`DS-logo-clean.png`), not a redrawn or animated version. Small in the nav; large and cropped as a graphic element. It carries continuity from the whitepaper into the renamed site.

**Type.** One family with real character, used for everything: **Alegreya** (Juan Pablo del Peral, Google Fonts) for headings and text, **Alegreya Sans** for navigation, labels, captions and buttons, **Alegreya SC** where small caps are wanted. Calligraphic, bookish, distinct from the Garamond and Cormorant defaults, and not part of the AI serif canon. No monospace anywhere. No tracked uppercase eyebrows. Italic used for emphasis and captions, not as a decorative accent word in every headline.

**Palette** (from the cover, plus photographs):

| Token | Value | Use |
|---|---|---|
| paper | `#F1E7C3` | the ground at the front door; straw paper, warmer and yellower than the old parchment but not yellow-first |
| cream | `#FAF6EA` | reading pages, cards, long text |
| graphite | `#26231F` | ink; also the one dark "spine" block (graphite, not brown) |
| vermilion | `#D8321E` | the single accent: links on hover, the masthead word, one rule, one button |
| pencil | `#5E5850` | captions, secondary text, hand-drawn rules |

No gilt, no gold, no gradients. Photographs carry all other colour.

**Image policy.** Photographs of Life Itself places and gatherings, captioned with place and year. The Samarra etching for the spine. The whitepaper cover as itself. Never stock, never generated, never a CSS filter pretending to be an etching.

**Layout habits.** Left-aligned, asymmetric, generous margins. Sections separated by a hand-drawn pencil rule (an SVG with a slightly irregular line), not gradients. Numbered contents rather than three matching cards. One dark block per page at most. Captions under every photograph. No inline styles: components live in `custom.css`.

**Per stream.** Learn: most photographs, cream reading ground. Build: the etching, the cover, text-forward, the one dark block. Fund: tables and documents, quiet.

**Masthead.** Nav: spiral mark + "Conscious Communities" in Alegreya. Footer lockup: *Conscious Communities · developmental spaces where people grow · an initiative of Life Itself and friends.*

## 7. Direction decided: E, watercolour (2026-09-18, evening)

Agreed with Rufus after the visual mood board and the Awami book. This supersedes §1 (warm monastic) and §6 (the Alegreya / paper / vermilion brief), which are kept as history.

**The recipe.** Loose watercolour illustration on a near-white page, held by a hard, tight-set black serif and flat yellow blocks. The Awami Conscious Food book (Life Itself, 2026; illustration by Jennifer Chan) proves the balance: soft paintings, severe type, one colour. Watercolour plus type plus yellow is one register, which is what the first redesign pass lacked when it mixed drawings with photographs.

**Rules**

- **Base: E.** Page `#F5F5F3` (near-white, not cream). Ink `#111`. One flat yellow, Life Itself's (`#FFD23F` or the exact brand value). All other colour comes from the paintings. Narrow text columns, a lot of air, paintings bleeding off the page edge.
- **Spine from C.** Whitepaper and manifesto pages: fewer paintings, the serif tight and severe, the yellow block as the only relief.
- **Mark.** A spiral in the same brushed hand as the book's blue circle, to be made. The pencil spiral stays on the current whitepaper until the cover is redone in watercolour. Samarra is good in itself and can appear inside as a plate; it is not a cover.
- **Type.** PT Serif throughout (nearest web cousin of the book's Literaturnaya): titles tracked tight (about -0.04em) with an italic second line, body at reading size. Prata for the masthead only if more elegance is wanted. A plain sans (Source Sans 3) for navigation, captions, buttons. No monospace, no tracked uppercase eyebrows.
- **Yellow stays.** It is the family tie to Life Itself and the book has proved it. No second brand colour.
- **Illustration carries ideas; photographs carry evidence.** Paintings on the home page, stream pages, concept pages, courses. Photographs only where a page is about an actual place (exemplars, Find, posts about a specific space), and there always as a plate inside the designed page: uniform size, captioned with place and year, never full-bleed, never the hero. No photographs of the Bergerac hub as a stand-in for the idea; the site is about the general idea.
- **No photography commission.** Not happening; the design must not depend on it.

**Illustration supply, in order**

1. **Reuse the Awami paintings.** They are Life Itself's own work and on theme (a monk with a bowl, a cook, a long table, a building, a road from field to bowl, vegetables, colour ribbons, a blue circle, the cover wash). They carry the mockups and plausibly the launch. Jennifer Chan is no longer around, so this is the working library.
2. **Procedural washes.** Claude can make the abstract parts in code (canvas or SVG): washes, circles, ribbons, grain. Good for backgrounds and shapes, not for figures.
3. **Image model with the Awami paintings as style references** (Midjourney, Flux or similar), prompts written by Claude, curated ruthlessly by Rufus. For drafts and gaps only; uncurated output drifts into generic "AI watercolour", the thing being avoided.
4. **Commission** a small set of new pieces when possible: a spiral, a circle of people, a house with many doors, the five domains, the three streams, and a new whitepaper cover in the same hand.

**Copy** is a separate, human job (see the mood board's copy section). Mockups use placeholder copy that avoids the known problems but is not final.

**Process from here.** Done 2026-09-18: three plain HTML mockups (the chapter page, the road, the catalogue) at https://claude.ai/artifact/3h8svRrhetYvMnAKDvm6rK, source in `mockups/`. They share one stylesheet and generate the washes, the cover and a brushed spiral mark in canvas. Chosen: mockup 1 for the home, mockup 3's catalogue for /what. Ported into Flowershow the same night (home `index.md`, `what.md`, `custom.css`, `assets/illustrations/`). Next: the Learn, Build and Fund stream pages, then whitepaper and manifesto, in the same language; then the copy pass. Original plan: two or three plain HTML mockups of the home page sharing one stylesheet, with the Awami paintings and a procedural wash, to settle layout and type. Pick one. Then port into Flowershow on `feat/redesign-cc`, replacing the first-pass home page and CSS. Then stream pages, then whitepaper and manifesto.

## Sources

- `../devspaces-consolidation/brand-narrative.md` §The taste (2026-07-12) — the origin of the warm-monastic decision.
- `../devspaces-consolidation/HANDOFF-design.md` — constraints for the Flowershow platform and the contrast reference (archipelago.place is a deliberately different visual world; rhyme, do not converge).
- `../devspaces-consolidation/assets/` — the June 2026 exploration, DS logo, whitepaper cover, spiral, tower etching.

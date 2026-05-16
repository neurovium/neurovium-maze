# CLAUDE.md — Project Specification for neurovium.github.io

## Overview

Personal academic website for **Nima Dehghani** — physics, computational
neuroscience, and NeuroAI researcher at MIT, leading **N⁴** (NeuroPhysics ·
NeuroComputation · NeuroDynamics, encompassed by NeuroAI). Hosted on GitHub
Pages at `neurovium.github.io` (mirror: `neurovium.ai`).

The site is not a CV. It is an **epistemic labyrinth**:

- **The Maze** — the discrete, structural infrastructure of concrete output.
  Papers are *rooms*; the Paper Maze is the corridor of rooms.
- **The Garden** (Borges) — the fluid, infinite realm of the underlying ideas.
  Concepts are *forking paths* that run *inside* the Maze. The Idea Garden is
  the concept cloud; a Concept Fork inside a paper opens a side panel that can
  *warp* the reader to a different room that shares that concept.

It still serves two practical purposes: a professional academic presence, and
a code companion for published papers (each paper page is citable in a
"Code Availability" section).

## Technology

- **Jekyll** + GitHub Pages (auto-build on push). No custom plugins
  (`jekyll-feed`, `jekyll-seo-tag`, `jekyll-sitemap` only).
- All interactivity is vanilla JS (`assets/js/main.js`, `assets/js/quotes.js`).
- One CSS file: `assets/css/style.css`. No frameworks.
- Math: **KaTeX** (CDN, conditional via `katex: true` front matter) for the
  hero N⁴ equation and the Research commuting diagram. **MathJax v3** (CDN,
  conditional via `math: true`) for LaTeX inside paper/post bodies.

## Design System — editorial / labyrinth

> Source of truth: the Neurovium Design System bundle from claude.ai/design,
> ported into `assets/css/style.css`. **This overwrites all earlier
> dark-amber / Syne / DM-Sans design decisions.** Do not reintroduce them.

### Aesthetic
Quiet, exact, literary — a researcher speaking to other researchers with the
eye of someone who has read Borges, Bachelard, Calvino. Warm printed-paper
canvas, warm near-black ink. Two motifs braid through every surface:

| | **Maze** (papers) | **Borges / Garden** (concepts) |
|---|---|---|
| Geometry | orthogonal hairlines, grid, corridor | radial ink-wash blooms, branching |
| Type | mono coordinates + sans body | serif italic asides, fork-glyph links |
| Motion | snap horizontal slide | column cleave (50/50), warp |
| Colour | hairline + ink only | one ink-wash orb per fork |

The page floor is always Maze; the Garden activates *on top of* it.

### Colour
All tokens are CSS custom properties in `:root` (see `style.css`). There is
**no saturated brand action colour — ink is the action colour.** The site
canvas is the warm `--paper-rust` (#ead7be); the sidebar is `#f0dfc6`; cards
are the lighter `--card-bg` (#faf3e4) embossed slabs.

- Base: `--paper`, `--paper-soft`, `--paper-deep`, `--vellum`, `--paper-rust`
- Ink: `--ink` #1a1814, `--ink-soft`, `--body`, `--muted`, `--muted-soft`
- Hairlines: `--hairline`, `--hairline-strong`
- Atmospheric ink-wash orbs (the *only* colour voltage, used **only** as soft
  radial gradients — never fills, text, or borders): `--wash-oxblood`,
  `--wash-slate`, `--wash-plum`, `--wash-teal`, `--wash-dust`,
  `--wash-amber`, `--wash-rust`.
- Concept Fork accent: `--fork` #7a2e3a (oxblood) — a 1px highlight band +
  6px dot on inline `.fork-link`s. The only "colour" most readers click.

### Typography
- **Display: Spectral, weight 300** (Google Fonts). Editorial serif. **Never
  bold display copy.** Italic Spectral 300 is the Borges register (epigraphs,
  paper subtitles, fork links).
- **Body / UI: Inter** 400/500, `letter-spacing: 0.16px`.
- **Mono: JetBrains Mono** 500 for corridor coordinates, section indices,
  BibTeX, code, kicker meta (UPPERCASE, `letter-spacing: 0.08em`).
- Display headlines are **sentence case**. No emoji, ever. The decorative
  mark is the fork glyph `⌥` / the dot-and-branch SVG.

### Components (class names in `style.css`)
- `.app` grid shell: `.side` sidebar (296px) + `.main`. Mobile: `.topbar`
  with hamburger; `.side` slides out over `.sidebar-backdrop`.
- `.ebtn--primary` / `.ebtn--outline` — embossed 3D slab pill CTAs.
  `.btn--*` — plain pills. Pill (`9999px`) is the only button shape.
- `.card` / `.pcard` — embossed slab paper card: media (image or
  `--wash-color` placeholder) + body with mono `Room NN · year · venue`
  kicker, serif title, tag pills.
- `.tag-filter` / `.filter` — concept-door filter bar (multi-select,
  intersection; built client-side from `data-tags`).
- `.paper` — the room: crumb, teaser (16:9, `--wash-color`), Summary, Links
  pill bar, Code & Data, prose body, "Doors · concepts", `.corridor`
  prev/next room nav (← / → keyboard).
- `.fork-panel` — Borges side panel on `--vellum` with an ink-wash orb;
  slides in (`.paper-shell.has-fork` → 50/50), lists rooms sharing the
  concept, has a "Follow this path into the Maze" warp link.
- `.garden` — concept cloud (word size ∝ #rooms); hovering a concept dims
  non-matching room cards.
- `.news` — short-form feed cards (text / link / embed kinds).
- `.foot` — thin footer row.

### Motion
Ease tokens `--ease`, `--ease-glide`; durations 180 / 320 / 600 ms. Scroll
reveal via IntersectionObserver (`.reveal` → `.is-visible`). No bounce, no
parallax, no scroll-jacking. Respects `prefers-reduced-motion`.

### Anti-patterns (do NOT do)
No bluish-purple gradient backgrounds. No emoji cards. No left-border-accent
cards. No neon CTAs. No bold Spectral. No sharp 0px corner buttons. No fake
chart / sparkle SVG decoration. No glassmorphism on cards (backdrop blur only
on the mobile topbar). One ink-wash orb per panel; two per page is the ceiling.

## Site Structure

```
neurovium.github.io/
├── _config.yml
├── _layouts/
│   ├── default.html        # app shell: topbar, sidebar, main, footer
│   ├── paper.html          # paper-room + corridor nav + fork panel
│   ├── post.html           # blog post (prose)
│   └── papers-index.html   # Paper Maze grid + tag filter
├── _includes/
│   ├── head.html           # meta, KaTeX/MathJax conditionals
│   ├── sidebar.html         # brand glyph, nav, embossed social, N⁴ set, foot
│   ├── social-icons.html    # (legacy reusable icon set; sidebar inlines its own)
│   ├── paper-card.html      # embossed slab card; accepts paper, room
│   └── footer.html          # thin .foot row
├── _data/
│   ├── concepts.yml         # concept → {wash, blurb, papers[]}  (drives Garden + forks)
│   └── news.yml             # short-form feed items
├── _papers/                 # collection — one .md per paper (has id + wash)
├── _posts/                  # blog posts
├── assets/
│   ├── css/style.css        # the entire design system
│   ├── js/main.js           # sidebar, reveal, KaTeX, epigraph, fork, corridor
│   ├── js/quotes.js         # rotating hero epigraphs (single source of truth)
│   └── img/{brand,logo,icons,papers,profile}/
├── index.html               # home: hero (brand mark, ∞ divider, N⁴ eq,
│                             #   embossed CTAs, rotating epigraph) + Latest
├── about.md                 # /about/  — photo, bio, neuron-circuit image
├── papers.html              # /papers/ — Paper Maze
├── garden.html              # /garden/ — Idea Garden concept cloud
├── news.html                # /news/   — short-form feed
├── research.html            # /research/ — logo + commuting diagram + N⁴
├── blog.html                # /blog/   — post index
└── CLAUDE.md
```

Sidebar nav order (fixed): **Home · News · Research · Paper Maze · Idea
Garden · Blog · About**. (Presentations dropped.)

## Paper Front Matter

```yaml
---
layout: paper
id: spindle-async                 # stable id; referenced by _data/concepts.yml
wash: "--wash-slate"              # ink-wash orb token for teaser + cards
title: "…"
subtitle: "…"                     # optional, italic
authors: "Dehghani, …"
date: 2010-01-01                  # orders the Maze corridor (prev/next)
venue: "J. Neurophysiology"
year: 2010
image: /assets/img/papers/foo.jpeg   # optional; placeholder used if absent
tags: [Spindle, MEG, EEG]         # 3–6, surgical — these are Maze doors
arxiv: "" doi: "" pdf: "" repo: "https://github.com/…"
blog: "/blog/…/"                  # optional companion post
slides: ""                        # optional
mirrors:
  - name: "Student fork"
    url:  "https://github.com/…"
bibtex: |
  @article{…}
description: "Plain-language summary (2–3 sentences)."
math: true                        # load MathJax if the body has LaTeX
---
Markdown body. Wrap a concept in a Concept Fork to open the Borges panel:
… most spindles begin as a
<span class="fork-link" data-fork="focal asynchronous oscillation">focal asynchronous oscillation</span> …
```

The `data-fork` value must match a key in `_data/concepts.yml`. The fork
panel pulls that concept's blurb and the *other* rooms (papers) that share it,
with a warp link to the first.

## How to add things

**A paper** — create `_papers/slug.md` with the front matter above (include
`id` and `wash`), add a teaser to `assets/img/papers/`, write the body, add
Concept Fork spans for its key ideas, commit. It appears automatically in the
Paper Maze, Latest, and (via its tags/concepts) the Garden.

**A concept** — add an entry to `_data/concepts.yml`
(`name: {wash, blurb, papers: [ids]}`), then wrap that phrase in paper bodies
with `<span class="fork-link" data-fork="name">…</span>`.

**A blog post** — `_posts/YYYY-MM-DD-slug.md` with `layout: post`, `title`,
`date`, `tags`, optional `paper:` (path to the room it opens). Note: existing
legacy posts lack date-prefixed filenames / front matter and won't be picked
up until normalised.

**A news item** — append to `_data/news.yml` (`kind: text|link|embed`).

**A hero epigraph** — edit `assets/js/quotes.js` (single source of truth).

## Implementation Notes

- No custom plugins (GitHub Pages). Tag filtering and the fork/garden logic
  are client-side JS reading `data-*` attributes and an inline
  `#concepts-data` JSON island.
- Reach for CSS custom properties; never inline hex.
- Image placeholders: `.card__placeholder` (dark grid + `--wash-color`),
  never broken `<img>`.
- Everything is responsive; the sidebar is the tricky part (slides out
  below 760px). Keep it lean, accessible (heading order, alt text,
  keyboard-navigable filters and corridor), and check contrast on the warm
  canvas.
- Font substitution flag: Spectral substitutes the licensed Waldenburg /
  GT Sectra. Confirm with Nima or supply a license to swap.
- Brand mark PNGs in `assets/img/brand/` are large (~2–3 MB). If page weight
  matters, export optimised/WebP versions and update the `<img src>`.

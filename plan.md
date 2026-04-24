Build a minimal, deliberately-plain personal website for a DevOps/MLOps engineer,
deployable as-is to GitHub Pages.

## Technical constraints

- Static site. Plain HTML5 and a single CSS file. No build step, no JavaScript
  frameworks, no bundlers, no npm. If JavaScript is needed for anything, it must
  be vanilla and inline or in a single small .js file — but prefer zero JS.
- File structure:
    /index.html
    /about.html
    /now.html
    /writing/index.html       (index of posts — can be empty list with placeholder)
    /writing/hello-world.html (one sample post using lorem ipsum)
    /projects/index.html
    /projects/pathfinding-visualizer.html   (real project, see below)
    /projects/monorepo-migration.html       (placeholder — lorem ipsum body)
    /styles.css
    /404.html
- Must work with GitHub Pages served from the repo root. Use relative links only.
  No trailing-slash assumptions. Include a CNAME-ready structure but no CNAME file.
- Include a minimal README.md explaining how to run locally
  (`python3 -m http.server`) and how to deploy (push to main, enable Pages).

## Aesthetic direction

Think Dan Luu, Julia Evans (text side), Rachel by the Bay, Simon Willison.
Deliberately plain. The writing should carry the weight, not the design.

- Single column, max-width ~680px, centered.
- System font stack: ui-monospace, SFMono-Regular, Menlo, monospace for code;
  system-ui, -apple-system, sans-serif for body. Pick ONE — I lean toward a
  serif body (Georgia, 'Iowan Old Style', serif) because it reads well for
  long-form and is uncommon among engineer sites, which makes it distinctive
  without being loud.
- Font size ~18px, line-height ~1.6, generous margins.
- Light mode default. Include a prefers-color-scheme dark variant in CSS only
  — no toggle button.
- Color palette: near-black text on off-white (#fafafa or similar), one single
  accent color for links (a muted blue or rust — pick one and commit). Visited
  links slightly different. No gradients, no shadows, no border-radius beyond
  2px, no animations.
- Header: just the person's name as a link to home, and a small horizontal nav
  (Writing · Projects · Now · About). No logo, no hero image, no tagline banner.
- Footer: one line. Name, year, a "source on GitHub" link placeholder.

## Content — use lorem ipsum for prose, but structure should be real

### / (index.html)
- Name as h1.
- One short paragraph (lorem ipsum, ~3 sentences) — placeholder for a
  self-introduction.
- Three sections below, each with a heading and 2-3 item list:
    - "Recent writing" — link to 1 sample post with date
    - "Projects" — link to the 2 project pages
    - "Now" — one line summary linking to /now.html

### /about.html
- h1 "About"
- 4-5 paragraphs of lorem ipsum, structured as: origin, current work,
  what I'm learning, what I'm looking for, how to reach me.
- At the bottom: a plain list of contact links (email placeholder,
  GitHub placeholder, LinkedIn placeholder). No icons.

### /now.html
- h1 "Now"
- Short note at top: "What I'm working on and thinking about, updated
  occasionally. Inspired by nownownow.com."
- A dated heading ("Updated: [today's date]") and 3-4 bullet points of lorem
  ipsum describing current focus areas.

### /writing/index.html
- h1 "Writing"
- One short intro sentence (lorem ipsum).
- A reverse-chronological list. Each entry is: date (YYYY-MM-DD), title as
  link, one-line description. Include 1 real link (hello-world.html) and
  2-3 "coming soon" placeholder entries without links.

### /writing/hello-world.html
- A post template. h1 title, date subtitle, then ~6 paragraphs of lorem ipsum
  with at least one h2 subheading, one blockquote, one code block, and one
  unordered list — so the CSS for all of these is exercised and visible.
- Back link to /writing/ at top and bottom.

### /projects/index.html
- h1 "Projects"
- Intro sentence (lorem ipsum).
- List of 2 projects, each with title (link), date range, one-line summary.

### /projects/pathfinding-visualizer.html
- h1 "Pathfinding Visualizer"
- Subtitle/date: something like "2021 · React"
- Sections: "What it is", "Why I built it", "What I'd do differently now" —
  all with lorem ipsum bodies. This framing (especially the third section) is
  important; please keep those exact section headings.

### /projects/monorepo-migration.html
- h1 "Monorepo migration with Swarm, GitOps, and Vault"
- Subtitle: "2024-2025 · Professional work"
- Sections: "The problem", "The shape of the solution", "Tradeoffs",
  "What I learned" — all lorem ipsum bodies. Keep these section headings.

### /404.html
- h1 "404"
- One line: "This page does not exist. Back to home."

## CSS specifics

- Use CSS custom properties for colors so dark mode is a small override block
  at the bottom of the file.
- Style exactly these elements: body, h1, h2, h3, p, a, a:visited, a:hover,
  ul, ol, li, blockquote, code, pre, hr, nav, header, footer, .post-meta
  (for dates under post titles).
- Code blocks: light gray background, small padding, no syntax highlighting.
- Blockquotes: left border only, indented, slightly muted text color.
- No utility classes beyond what's necessary. No framework.

## Deliverables

All files written out in full. No "..." placeholders in code. A brief note at
the end explaining (a) how to enable GitHub Pages for this repo and (b) the
three or four spots where lorem ipsum should be replaced first for maximum
effect (suggest: index intro, about page, and the pathfinding "Why I built it"
section).
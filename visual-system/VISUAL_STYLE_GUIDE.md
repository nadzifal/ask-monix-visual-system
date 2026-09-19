# Ask Monix Visual Style Guide

Status: **LOCKED / PRIMARY VISUAL GUIDE**

This is the practical visual translation of the approved Ask Monix moodboard.

If a future screen looks technically correct but does not feel like this guide, the visual implementation is not finished.

---

## 1. Overall visual feeling

Ask Monix should feel like:

**Calm Modern Intelligence Workspace**

Not:
- enterprise BI dashboard
- admin panel
- editorial magazine
- futuristic AI interface
- decorative analytics poster

The visual tone must be:

- calm
- crisp
- intelligent
- modern
- trustworthy
- focused
- human
- restrained

Key phrase:

> **Less reading to understand more.**

---

## 2. Canvas

Base canvas:

`#F9FAF8`

Use a crisp warm-white background.

Do not make the whole UI beige, cream, gray, dark, or tinted heavily.

The surface should feel light and open.

### Rule

Open canvas is the default.

Cards are exceptions.

---

## 3. Typography

Primary family:

**Inter / Geist-class sans-serif**

Use system fallback only when those are unavailable.

### Main analytical headline

Desktop target:
- 30–36px
- weight 700–800
- line-height 1.08–1.15
- tight but readable tracking

Mobile target:
- 26–30px

Headline style:

- sentence case
- bold core claim
- one selective semantic highlight
- short supporting sentence below
- no serif
- no all-caps main headlines

Example:

**Pelemahan Angle A tidak merata**

Penurunan paling terlihat pada **Account B** di beberapa creator.

### Supporting copy

- 14–16px
- regular/medium
- muted gray
- line-height 1.45–1.55

### Metric number

- 22–30px depending on hierarchy
- semibold/bold
- never oversized hero numbers

### Labels

- 11–13px
- muted
- compact
- no overuse of uppercase

ALL CAPS is only for tiny eyebrow/state labels when necessary.

---

## 4. Headline grammar

Approved pattern:

**semantic accent rail → bold claim → selective semantic color → support sentence**

Example negative:

| element | treatment |
|---|---|
| rail | muted red |
| claim | deep ink |
| important phrase | red |
| supporting sentence | muted gray |

Positive uses botanical green.

Mixed/uncertain uses amber or neutral.

### Accent rail

- 3–4px wide
- short/local
- aligned only to the analytical headline
- never stretch across the whole section

Do not turn the rail into decoration.

---

## 5. Color system

### Primary
Botanical green  
`#0F7A46`

### Ink
`#0F172A`

### Background
`#F9FAF8`

### Surface
`#FFFFFF`

### Secondary text
`#667085`

### Muted text
`#8A94A3`

### Negative / weakening
`#E23D55`

### Negative soft
`#FFF0F2`

### Mixed / uncertain
`#D98B12`

### Mixed soft
`#FFF7E8`

### Positive soft
`#EAF7EF`

### Border
`#E5E9E7`

---

## 6. Semantic color rule

This is mandatory:

> **Arrow = what numerically happened. Color = what that movement means for business outcome.**

Example:

`Total Konten ↑9%`

may still be **red** if output increased while impressions worsened.

Do not automatically color every positive number green.

---

## 7. Lines and dividers

Lines are one of the biggest sources of visual rigidity.

Use them sparingly.

Allowed:
- local row separator
- chart grid
- focus outline
- headline rail
- compact metric grouping

Avoid:
- full-page horizontal rules after every section
- vertical dividers between every metric
- decorative lines
- spreadsheet-like grids

### Test

If spacing can separate the content, do not add a line.

---

## 8. Cards and surfaces

Default:
**no card**

Use a card only when it does one of these jobs:

1. groups an interaction
2. creates a focus state
3. contains dense information
4. communicates a meaningful state

### Card styling

- white surface
- 8–12px radius
- thin border only if needed
- almost no shadow
- compact padding
- no floating dashboard tile aesthetic

### Never

Do not put:
- every metric
- every section
- every message
- every next step

inside a separate card.

---

## 9. Shadows

Default:
**none**

If a focused interaction truly needs elevation:

`0 6px 18px rgba(15, 23, 42, 0.045)`

Do not use:
- heavy shadows
- glow
- neon edges
- layered elevation everywhere

---

## 10. Whitespace

Whitespace must be active.

It creates:
- hierarchy
- reading order
- calmness
- semantic grouping

Do not create empty space only for visual luxury.

### Preferred spacing rhythm

Use an 8px-based rhythm:

- 8
- 12
- 16
- 20
- 24
- 32
- 40
- 48

### Reading rhythm

Primary answer → strongest evidence → interpretation → deeper detail → next action.

---

## 11. Dashboard visual behavior

Dashboard is **LOCKED**.

It should look deliberate and stable.

The first viewport should communicate:

1. brand condition
2. human-language interpretation
3. core metrics
4. direction to investigate

Do not use:
- giant hero
- big page title
- six equal KPI cards
- numbered flow tabs
- excessive widgets

Core metrics appear as one family:

- Impressions
- Total Konten
- Total FYP
- FYP Rate

Support metrics are quieter:

- Impression / Konten
- Active Creator

---

## 12. Investigation visual behavior

Investigation is not a dashboard repeated four times.

### History
Feels temporal.

The eye should move through time.

### PIC
Feels decomposed.

The eye should locate where change is concentrated.

### Angle
Feels relational.

The relationship **Output → Hasil** should be visible as structure.

### Creator × Account
Feels like an execution map.

Patterns across creators and accounts should be visible before reading every number.

---

## 13. Scan vs inspect

### Scan

Purpose:
find the pattern.

Show only:
- direction
- pattern
- primary signal

### Inspect

Purpose:
understand magnitude and evidence.

Show:
- absolute value
- delta
- interpretation
- context
- uncertainty
- evidence boundary

Do not surface complete KPI detail during scan.

---

## 14. Charts

Charts must earn their place.

Use when movement or relationship is clearer visually than verbally.

Rules:
- thin lines
- minimal grid
- one primary y-axis
- raw value in tooltip
- no decorative area chart
- no 3-axis comparison
- no chart merely because data exists

---

## 15. Buttons and actions

Primary action:
- botanical/deep green
- compact
- clear verb
- no oversized CTA

Examples:

`Telusuri →`

`Lihat PIC →`

`Lihat Angle →`

`Bandingkan dengan Account A →`

Actions should follow evidence, not float independently.

---

## 16. Focus state

Selected/focused content should use:

- subtle tint
- local border
- local semantic rail
- clear but calm emphasis

Do not use:
- heavy glow
- thick border
- giant badge
- drop-shadow spotlight

---

## 17. Unknown / insufficient evidence

Unknown is a visual state.

Use:
- neutral gray
- restrained wording
- explicit reason

Examples:
- Allocation plan belum tersedia
- Coverage belum lengkap
- Observation window belum matang
- Sampel belum cukup

Do not show unknown as green/stable.

---

## 18. Anti-patterns

Immediate visual fail:

- serif headline
- botanical illustration
- dark/neon UI
- cinematic gradient
- giant KPI cards
- dashboard card grid
- oversized rounded rectangles
- excessive pills
- decorative icons everywhere
- stepper 1–5 across investigation
- repeated green "Next investigation" card
- all metrics equally loud
- too many separator lines

---

## 19. Moodboard fidelity test

Before approving a screen, ask:

### Does it feel calm?
If not, reduce competing elements.

### Does it feel modern?
If not, make relationships/state carry more of the structure.

### Does it feel intelligent?
If not, surface the analytical relationship rather than more decoration.

### Does it feel too rigid?
If yes, reduce lines, borders, cards, repeated patterns, and equal weighting.

### Does it feel too empty?
If yes, increase semantic structure, not decoration.

---

## 20. Final visual principle

> **Jangan membuat data terlihat cantik. Buat intelligence-nya terlihat.**

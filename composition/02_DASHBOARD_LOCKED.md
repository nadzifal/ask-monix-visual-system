# Dashboard — Locked Product Surface

## North star

> Begitu melihat Dashboard, user langsung tahu brand-nya sedang kenapa dan langsung tahu cara menelusurinya.

## Reading flow

**Scope → Kondisi brand → Angka → Pergerakan → Yang perlu ditelusuri → Yang sedang dikerjakan**

## Scope

One-line contextual control:

`White Inc ▾ · 1–18 September 2026 · vs 1–18 Agustus 2026 ▾`

No giant "Dashboard" page title.

## Business condition

States:

- Menguat
- Melemah
- Stabil
- Mixed

Treatment:

- small
- muted
- no giant warning badge
- accompanied by human-language reading

Principle:

> angka tanpa kalimat terlalu kaku; kalimat tanpa angka terlalu liar.

## Core metrics

One unified metric family:

1. Impressions
2. Total Konten
3. Total FYP
4. FYP Rate

Supporting metrics directly beneath:

5. Impression / Konten
6. Active Creator

Do not turn six metrics into six equal cards.

## Metric semantics

- Arrow = numeric direction
- Color = business meaning
- FYP Rate delta = percentage points
- Active Creator delta = absolute count
- Impressions readable in Indonesian human format
- Comparator is global, not repeated everywhere

## Performance Trend

Purpose: show movement before deep investigation.

Rules:

- multi-metric selector
- default one metric
- raw values in tooltip
- no three y-axes
- clean thin lines
- minimal grid
- normalized compare only when scale difference requires it

## Management Attention

Heading:

**Perlu diperhatikan**

Rules:

- maximum 3
- materiality/usefulness, not "all red metrics"
- no severity badges
- one active rich concern
- other concerns compact
- CTA: `Telusuri →`

## Operational State

Heading:

**Sedang berjalan**

Examples:

- RATAP Aktif
- Active Work
- Menunggu Hasil

Counts are not inherently good/bad.

No traffic-light styling.

## Hard failures

- giant KPI cards
- card-grid dashboard
- long report prose
- decorative hero
- too many competing primary messages
- generic "Performance Intelligence" title replacing analytical reading

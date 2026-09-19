# North Star Lock — Dashboard (v2)

Status: **LOCKED / DO NOT REINTERPRET**

Date locked: 19 September 2026 (v1). **Superseded 19 September 2026 (v2)** — v1
matched composition/hierarchy but was assessed against the real product and
judged "correct order, not yet okay" on visual craft. v2 replaces it as the
authoritative reference.

## Approved reference

`references/north-stars/dashboard_v2_approved.webp`

This is the implementation target. It is denser and more crafted than v1: a
real product shell (branded nav, top control bar), a six-metric family
(not four), a real multi-series chart with axis/legend/annotation, and
three bottom panels (not two).

## What changed from v1

- **Metric family is six, not four**, in this order: Total Konten,
  Impressions, Total FYP, FYP Rate, Active Creator, Impression/Konten.
  Active Creator and Impression/Konten are no longer demoted to a smaller
  secondary row — they're part of the one connected family.
- **An explicit flow connector** sits between Total Konten and Impressions
  in the metric strip itself — output on the left, outcome on the right,
  visually paired without a separate "evidence strip" element.
- **Every metric carries an icon chip** (document, eye, lightning, percent,
  people, bar-chart) and a "vs [previous value]" line under the delta, not
  just the delta.
- **The brand-state block gained three more signals**: a small dot-cluster
  + "BRAND STATE" eyebrow above the headline, an inline sparkline + delta
  chip beside it, and — only when a change point is actually detected in
  the data — a separate "Momentum menurun/menguat" callout card. This is a
  real detector output (the same `ChangePointDetector` History already
  uses), not decoration; when nothing credible is detected, the card is
  absent rather than faked.
- **The chart is a real chart**: Y-axis gridlines and labels, a
  multi-series legend (Impression/Konten/FYP) that toggles independent
  overlay lines, and an annotation line + label at the detected onset date
  when momentum is present. Because Impression, Konten and FYP live on
  wildly different scales (verified against production: hundreds vs.
  millions), the axis always describes Impressions; a toggled-on secondary
  series is normalized to its own min/max for shape comparison and the UI
  says so explicitly. This is an intentional, documented adaptation from
  the mockup's literal shared-axis look — the mockup's own dual-line
  rendering was not re-verified against real numbers of this magnitude.
- **Three bottom panels, not two**: "Perlu diperhatikan" (unchanged
  analytically, now with icon chips), a new **"Kondisi operasional"** panel
  (real signals — content-production level, creator-activity level, and
  content-distribution shift, each compared to the brand's own previous
  period, not an absolute cross-brand threshold — see "Distribusi konten"
  below), and a new **"Lanjuti investigasi"** panel linking directly into
  each Investigation stage (History/PIC/Angle/Creator × Account) from the
  Dashboard.
- **Top bar is a real control cluster**: brand chip with avatar, a
  functional date-range control, a functional PIC filter, a search icon
  (present but honestly inert — not wired to anything yet), and a user
  avatar.

## "Distribusi konten" — why it is a relative signal, not an absolute one

Real production data (measured 2026-09-19) shows brand creator rosters
ranging from 2 to 60+ people. An absolute "top-3 creators = X% of content"
threshold would flag every small-roster brand as "concentrated" every
period regardless of whether anything actually changed. The shipped signal
instead compares the brand's own top-5-creator content share this period
against its own share last period. A shift is meaningful; a level is not
comparable across brands.

## Locked visual character

Unchanged from v1 — still:

- calm
- beautiful
- immediately readable
- refined rather than decorative
- strong visual hierarchy
- functional iconography (now genuinely present, not just permitted)
- warm-white canvas
- deep ink
- botanical green
- restrained semantic red / amber
- elegant spacing rhythm
- light surfaces, only as much shadow as a floating control/popover needs
- no visual spectacle
- no generic SaaS/admin feel

## Locked Dashboard reading

Unchanged core question:

> **White Inc lagi gimana?**

The v2 composition communicates, in this order:

1. brand + period + filter controls
2. brand condition (dot cluster, headline, inline trend, momentum if real)
3. six-metric family with output → outcome connector
4. performance movement (multi-series chart)
5. management attention
6. operational condition (now with real per-signal status, not a single
   disclaimer line)
7. investigation entry points (direct links into each stage)

## Locked mobile order

Unchanged from v1:

1. Header / brand / period / controls
2. Brand condition
3. Total Konten + Impressions
4. Total FYP + FYP Rate
5. Active Creator + Impression / Konten
6. Performance trend
7. Perlu diperhatikan
8. Kondisi operasional
9. Lanjuti investigasi

The six metrics collapse to a 2-column grid in the order above — Konten
and Impressions (the connected output → outcome pair) stay adjacent.

## Hard rules (unchanged)

Do not:

- flatten the six-metric family back into a smaller demoted set
- fabricate a momentum card or annotation when no credible change point
  was detected
- fabricate "Kondisi operasional" status against a metric with no real
  calculation behind it
- add navigation items in "Lanjuti investigasi" (or anywhere) that point
  to pages that don't exist or aren't functional
- give a not-yet-functional control (search) the same visual weight/
  affordance as a working one

## Change control

Any future change to first-view hierarchy, the six-metric family, the
three-panel bottom row, or the chart's scale-handling approach must be
treated as a deliberate design change, not an implementation cleanup.

Default implementation instruction:

> **Match the v2 north star. Do not redesign it.**

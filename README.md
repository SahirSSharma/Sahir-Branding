# Sahir-Branding

Reference captures of the **Resend** design language — the UI and animated logo work I want my own branding (TritonPlan and future projects) to feel like. This repo is the source-of-truth moodboard: raw captures plus a breakdown of *why* it works, so the aesthetic can be reproduced, not just admired.

## Asset inventory

| File | What it is |
|---|---|
| `CleanShot 2026-08-31 at 21.30.30.mp4` | Screen recording (~5s, 120fps) of Resend's **3D cube logo** tumbling/rotating, rendered as a dark app icon |
| `CleanShot 2026-08-31 at 21.30.47@2x.png` | Still of the cube logo icon — cube with square apertures cut into each visible face |
| `CleanShot 2026-08-31 at 21.31.03@2x.png` | Resend dashboard **metrics chart** for `tritonplan.com` — 7,932 emails, 100% deliverability, Aug 17–31 |
| `CleanShot 2026-08-31 at 21.31.34.mp4` | Screen recording (~5s, 120fps) of a second animated icon — **concentric hexagons** medallion, same material/lighting system |

## Design language breakdown

### 1. The logo marks (cube + hexagon)

- **Geometry over illustration.** Both marks are pure geometric primitives — a cube with square cutouts punched through its faces, and three nested hexagon rings. No gradients-as-decoration, no color, no mascot. The identity *is* the form.
- **Rendered as physical objects, not flat vectors.** The marks are 3D-rendered with real materials: matte, slightly rough black plastic/metal. Identity comes from light behavior, not fill color.
- **Monochrome, near-black on black.** The object is dark-on-dark; it's defined almost entirely by **specular edge highlights** — thin white light catching bevels and rims as the object rotates. White is used only where light would physically hit.
- **The squircle container.** Each mark sits inside an iOS-style rounded-square app icon with (a) a subtle film-grain/noise texture on the dark background, (b) a soft radial vignette so the center is slightly lighter than the corners, and (c) a faint contact shadow under the object. This makes the icon feel like a photographed artifact instead of a graphic.

### 2. Motion

- **Slow, weighty tumble.** The cube rotates on multiple axes at once — a lazy end-over-end tumble, roughly one full revolution over the ~5s loop. The hexagon medallion flips/spins on its vertical axis and settles.
- **The animation is the reveal.** At many frames the mark is abstract (a black slab, an edge-on sliver); it only resolves into the recognizable logo at certain angles. That tension is the charm — the logo is a *moment* in a continuous motion, not a frozen asset.
- **Light does the storytelling.** As the object turns, highlights sweep across bevels. Nothing else in frame moves. High frame rate (120fps capture) + slow motion = the "expensive object" feel.

### 3. The dashboard UI (metrics chart)

Sampled values from the screenshot:

| Token | Value | Used for |
|---|---|---|
| Background | `#000000` | Page and card — true black, no dark-gray theme |
| Accent green | `#6FD392` (mint) | The single data line, legend dot, 100% stat |
| Muted text | `#858788` | Axis labels, small caps section labels |
| Foreground | `#FFFFFF` / near-white | Big stat numbers, primary text |

- **One accent color, total.** The entire screen is grayscale except the mint-green data line. Color = data, nothing else.
- **Stat hierarchy:** tiny letter-spaced ALL-CAPS gray label (`EMAILS`, `DELIVERABILITY RATE`) over a huge light-weight white number (`7,932`, `100%`). No boxes around stats — whitespace does the grouping.
- **Chart styling:** hairline dashed gridlines in very dark gray, right-aligned axis, straight (not smoothed) line segments, a barely-there green→transparent fill under the line, no dots on data points, no chart border.
- **Chrome is minimal:** one pill-shaped dropdown (`All Events ⌄`) with a hairline border, rounded-corner card edges, generous padding everywhere.

### 4. The recipe (how to reproduce the feel)

1. True black canvas, one mint/green accent, gray for everything secondary.
2. Make the logo a simple 3D geometric solid; give it a matte dark material and let white specular edges define it.
3. Package marks as squircle icons with grain, vignette, and contact shadow.
4. Animate with a slow multi-axis tumble; let the mark be unrecognizable for part of the loop.
5. In UI: huge thin numerals, small caps gray labels, hairline dashed gridlines, zero decorative color.

## Notes

- Captures taken 2026-08-31 with CleanShot X (first recording includes the webcam overlay bubble — crop before reusing as reference footage).
- The dashboard screenshot contains real `tritonplan.com` sending stats; treat this repo as private reference material.

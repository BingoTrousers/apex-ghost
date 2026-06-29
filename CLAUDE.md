# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Dev server

```bash
python3 -m http.server 8080
```

Opens at http://localhost:8080. No build step — the site is a single static HTML file.

## Architecture

Everything lives in `index.html`. There is no framework, bundler, or build tool.

- **Styles** — a small `<style>` block at the top of `<head>` defines CSS classes for interactive states (hover, nav scroll). All layout and visual styles are inline on each element.
- **Data** — car specs and race log entries are hardcoded directly in the HTML. There is no JS data layer; to update stats, race results, or car info, edit the relevant HTML section.
- **Interactivity** — a `<script>` block at the bottom of `<body>` handles two things: the nav scroll effect (transparent → frosted glass at 80px scroll depth) and the dynamic footer year.

## Design tokens

| Token | Value | Usage |
|---|---|---|
| Background warm | `#f7f4ef` | Primary bg, card bg |
| Background cool | `#f0ede8` | Alternate section bg |
| Ink | `#0d0c0b` | Primary text, dark elements |
| Blue accent | `#1F72FF` | Primary brand colour, Car 01 |
| Green accent | `#00C97A` | Status indicators, Car 02, Next Race |
| Gold accent | `#E8C43A` | Car 03 |
| Muted text | `#8a8784` / `#c4c2be` | Secondary / tertiary text |

## Fonts

- **Exo 2** (Google Fonts) — headings and UI labels; used at weights 300–900, upright and italic
- **Space Mono** (Google Fonts) — data/telemetry readouts, codes, monospaced values

## Sections (in order)

| `id` | Purpose |
|---|---|
| *(no id — nav)* | Fixed nav, scroll-aware background |
| *(no id — hero)* | Full-viewport hero with HUD stat bar |
| `#machines` | Three car cards (HACHI-ROKU · TYPE-R · SUCCESSOR) |
| `#touge` | Philosophy / The Pass section |
| `#telemetry` | 8-cell telemetry readout grid |
| `#events` | Race log table (6 rows) |
| `#next-race` | Upcoming race details + footer |

## Origin

Converted from a Claude Design project (`Apex Ghost Racing.dc.html`, project `03238078-d04d-4d12-986d-feedf3899077`). The original used Claude Design's React runtime (`support.js`) with `{{ }}` templating and `<sc-for>` loops; this repo is the standalone static conversion with all data inlined.

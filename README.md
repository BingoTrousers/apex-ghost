# Apex Ghost Racing

Concept landing page for a fictional Japanese mountain racing team. Built as a portfolio piece — single static HTML file, no build step, no framework.

**Live site:** [BingoTrousers.github.io/apex-ghost](https://BingoTrousers.github.io/apex-ghost) *(enable GitHub Pages if not already)*

## Dev server

```bash
python3 -m http.server 8080
# → http://localhost:8080
```

## Design

- **Aesthetic:** JDM touge racing — warm off-white palette (`#f7f4ef`), electric blue (`#1F72FF`), monospace telemetry data, Japanese kanji accents
- **Typography:** Exo 2 (headings/UI) + Space Mono (data readouts) via Google Fonts
- **Sections:** Hero → The Lineup (3 cars) → The Pass (philosophy) → Live Telemetry → Race Log → Next Race

## Machines

| No. | Codename | Type | Year | Role |
|---|---|---|---|---|
| 01 | HACHI-ROKU | Twin-cam coupe | '86 | Technique |
| 02 | TYPE-R | B-type hot hatch | '97 | Attack |
| 03 | SUCCESSOR | GT sport coupe | '12 | Pursuit |

## Origin

Converted from a [Claude Design](https://claude.ai/design) prototype. The original used Claude Design's React runtime with template variables and `<sc-for>` loops; this repo is the standalone static conversion with all data inlined.

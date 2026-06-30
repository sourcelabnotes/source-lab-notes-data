# Source Ledger Public Data

This repository is the public data package for Source Ledger.

Source Ledger tests prediction claims by recording clues before outcomes are known, waiting for the stated horizon, subtracting estimated costs, and publishing both the hits and the misses.

This repository publishes **normalized observations and scorecards**, not raw third-party datasets. The goal is to make Source Ledger claims auditable without redistributing someone else's product.

## Start Here

- [Current scorecard summary](current/README.md)
- [Data dictionary](DATA_DICTIONARY.md)
- [Methodology](METHODOLOGY.md)
- [Source catalog](SOURCE_CATALOG.csv)
- [Current pattern observations](current/current_pattern_observations.csv)
- [Current pattern episodes](current/current_pattern_episodes.csv)

## Files

| Path | Purpose |
| --- | --- |
| `2026-06-27/charts/hero_strategy_scorecard.csv` | Downloadable chart data for the launch post. |
| `2026-06-27/charts/hero_strategy_scorecard.png` | Launch-post hero chart image. |
| `2026-06-27/charts/hero_strategy_scorecard.svg` | Vector fallback for the launch-post chart. |
| `2026-06-27/charts/hero_strategy_scorecard.mmd` | Mermaid source for the launch-post chart. |
| `2026-06-28/charts/methodology_scoring_example.csv` | Downloadable chart data for the methodology post. |
| `2026-06-28/charts/methodology_scoring_example.png` | Methodology-post worked-example chart image. |
| `2026-06-28/charts/methodology_scoring_example.svg` | Vector fallback for the methodology-post chart. |
| `2026-06-28/charts/methodology_scoring_example.mmd` | Mermaid source for the methodology-post chart. |
| `2026-06-28/charts/hero_strategy_scorecard.csv` | Downloadable chart data for the first scorecard-finding post draft. |
| `2026-06-28/charts/hero_strategy_scorecard.png` | First scorecard-finding post hero chart image. |
| `2026-06-28/charts/hero_strategy_scorecard.svg` | Vector fallback for the first scorecard-finding chart. |
| `2026-06-28/charts/hero_strategy_scorecard.mmd` | Mermaid source for the first scorecard-finding chart. |
| `2026-06-29/charts/hero_signal_scorecard.csv` | Downloadable chart data for the current scorecard draft. |
| `2026-06-29/charts/hero_signal_scorecard.png` | Current scorecard hero chart image. |
| `2026-06-29/charts/hero_signal_scorecard.svg` | Vector fallback for the current scorecard chart. |
| `2026-06-29/charts/hero_signal_scorecard.mmd` | Mermaid source for the current scorecard chart. |
| `2026-07-01/charts/hero_signal_scorecard.csv` | Downloadable chart data for Source Ledger Scorecard #001. |
| `2026-07-01/charts/hero_signal_scorecard.png` | Source Ledger Scorecard #001 hero chart image. |
| `2026-07-01/charts/hero_signal_scorecard.svg` | Vector fallback for the Scorecard #001 chart. |
| `2026-07-01/charts/hero_signal_scorecard.mmd` | Mermaid source for the Scorecard #001 chart. |
| `current/current_signal_family_scorecard.csv` | Persistent scorecard by broad pattern or clue family. |
| `current/current_asset_signal_scorecard.csv` | Persistent asset-specific scorecard by asset, pattern, and horizon. |
| `current/current_row_level_signal_evidence.csv` | Timestamped row-level replay evidence showing asset, clue, source class, observed price, later result, and reason. |
| `current/current_pattern_observations.csv` | Timestamped clue observations normalized for public audit. |
| `current/current_pattern_episodes.csv` | Persistence groups connecting repeated observations of the same clue/source-class/asset. |
| `current/current_source_health_scorecard.csv` | Persistent source-class health and freshness scorecard. |
| `current/current_research_leads.csv` | Persistent list of research leads that need more evidence. |

## Refreshing Current Scorecards

Run:

```sh
node --no-warnings scripts/build_source_lab_pattern_audit.mjs
node --no-warnings scripts/export_source_lab_notes_scorecards.mjs
```

Then copy or sync the generated CSVs from:

```text
trading/crypto-pop-lab/substack/data-exports/current/
```

to:

```text
trading/crypto-pop-lab/substack/public-data/current/
```

The pattern-observation file is the cleanest answer to "where and when was this clue seen?" The pattern-episode file shows whether the clue appeared once or persisted across checks.

The current scorecard files are research evidence only. They can show what looked promising, failed, or needs more testing, but they are not investment advice and do not recommend any current action.

## Current Public CSV Links

Launch post:

```text
https://gist.github.com/sourcelabnotes/0ec98e863022bfd175172d797d4046b7/raw/cf70fd7205ecd5598239dff0a8dfec81a2655514/hero_strategy_scorecard.csv
```

Methodology post:

```text
https://gist.github.com/sourcelabnotes/c0144d30ca6d919dda666dc5966b2dc8/raw/8991df643f7755000fae1d32034c04435e640151/methodology_scoring_example_clean.csv
```

The current public Gist may still use `hero_strategy_scorecard.csv` for older scorecard chart links. New local scorecard packages use `hero_signal_scorecard.csv` as the preferred public filename and keep `hero_strategy_scorecard.csv` only as a compatibility alias.

Use link text like:

```text
Download the CSV behind this chart
```

That is clearer for readers than showing a raw GitHub URL.

## Boundary

This repository should contain only public, reader-facing assets. Do not upload local SQLite databases, practice-trade logs, raw screenshots, raw HTML, credentials, internal notes, private dashboard exports, account information, or files that expose local filesystem paths.

## Reuse Note

Source Ledger publishes these normalized files so readers can inspect, download, and reuse the scorecards. Public files describe source classes and data types rather than named-provider source ids, and they do not grant rights in any third-party product, dashboard, API, or dataset.

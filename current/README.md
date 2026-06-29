# Current Source Lab Notes Scorecards

Generated: 2026-06-29T14:24:47.757Z

Database tournament run: `cpl-tournament-2026-06-29T01-03-52-205Z`

Backtest runs included for asset-specific rows: `cpl-backtest-2026-06-25T21-05-39-000Z-76b94298`, `cpl-backtest-2026-06-25T21-05-12-000Z-2a365d7a`

Estimated cost subtracted: 0.25 percentage points.

## Plain-English Read

The current public scorecard is still early research evidence, not investment advice. The clearest pattern-level lead is **Weak market, later bounce** with an average 4-hour result after costs of **+1.02%** across **125** examples. The strongest asset-specific slice is **AVAX / Weak market rejection**, with **+1.45%** after costs across **11** examples.

## Files

- `current_signal_family_scorecard.csv`
- `current_asset_signal_scorecard.csv`
- `current_row_level_signal_evidence.csv`
- `current_pattern_observations.csv`
- `current_pattern_episodes.csv`
- `current_source_health_scorecard.csv`
- `current_research_leads.csv`

The row-level evidence file has 2254 replay rows. Use it to see the asset, timestamp, clue label, source mode, observed price, later return, and reason for each scored example.

The pattern audit files have 16541 timestamped clue observations grouped into 1672 persistence episodes. Use them to see when a clue was first seen, whether it persisted across later snapshots, which source it came from, and how it was scored.

## Top Research Leads

| lead_type | asset | pattern_label | sample_count | avg_net_return_pct | hit_rate_pct | sample_quality | interpretation |
| --- | --- | --- | --- | --- | --- | --- | --- |
| asset_specific | AVAX | Weak market rejection | 11 | 1.45 | 72.73 | Early sample | Positive so far, but needs more examples. |
| asset_specific | DOT | Weak market rejection | 11 | 1.43 | 81.82 | Early sample | Positive so far, but needs more examples. |
| asset_specific | LINK | Weak market rejection | 11 | 1.31 | 90.91 | Early sample | Positive so far, but needs more examples. |
| asset_specific | HBAR | Weak market rejection | 11 | 1.14 | 100 | Early sample | Positive so far, but needs more examples. |
| asset_specific | SOL | Weak market rejection | 11 | 1.04 | 90.91 | Early sample | Positive so far, but needs more examples. |
| asset_specific | DOGE | Weak market rejection | 11 | 1.03 | 90.91 | Early sample | Positive so far, but needs more examples. |
| pattern |  | Weak market, later bounce | 125 | 1.02 | 80 | Stronger sample | Worth watching, but only for this pattern and horizon. |
| asset_specific | SHIB | Weak market rejection | 11 | 0.91 | 81.82 | Early sample | Positive so far, but needs more examples. |

## Source Health

| source_id | current_status | latest_record_count | freshness_score | evidence_mode |
| --- | --- | --- | --- | --- |
| blockmedia_ko | ok | 10 | Stale for current checkpoint evidence | api_or_scripted_collection |
| coinbase_exchange_public | ok | 13 | Current enough for latest checkpoint | api_or_scripted_collection |
| coinbase_exchange_public_backtest | ok | 2179 | Stale for current checkpoint evidence | api_or_scripted_collection |
| coindesk_japan_ja | ok | 10 | Stale for current checkpoint evidence | api_or_scripted_collection |
| coingecko_demo_api | ok | 28 | Current enough for latest checkpoint | api_or_scripted_collection |
| coinpost_ja | ok | 7 | Stale for current checkpoint evidence | api_or_scripted_collection |
| crypto_pop_lab_strategy_tournament | ok | 8 | Recent context, not current checkpoint evidence | api_or_scripted_collection |
| defillama_free_api | ok | 4 | Current enough for latest checkpoint | api_or_scripted_collection |
| dexscreener_public_api | ok | 13 | Current enough for latest checkpoint | api_or_scripted_collection |
| forklog_ru | ok | 16 | Stale for current checkpoint evidence | api_or_scripted_collection |
| santiment_sanapi | ok | 9 | Stale for current checkpoint evidence | api_or_scripted_collection |
| tokenpost_ko | ok | 20 | Stale for current checkpoint evidence | api_or_scripted_collection |
| upbit_public | ok | 5 | Current enough for latest checkpoint | api_or_scripted_collection |
| visual_coingecko | ok | 11 | Stale for current checkpoint evidence | visual_capture |
| visual_nansen | ok | 15 | Stale for current checkpoint evidence | visual_capture |
| visual_santiment | ok | 16 | Recent context, not current checkpoint evidence | visual_capture |
| visual_santiment_sanbase | ok | 11 | Recent context, not current checkpoint evidence | visual_capture |
| visual_santiment_sanbase_visual_dashboard_via_chrome_accessibility_tree | ok | 23 | Recent context, not current checkpoint evidence | visual_capture |
| visual_santiment_sanbase_visual_dashboard_via_chrome_extension | ok | 11 | Recent context, not current checkpoint evidence | visual_capture |
| visual_visual_dashboard | ok | 10 | Stale for current checkpoint evidence | visual_capture |

## Caveat

These CSVs score patterns that were recorded in the local research database. Backtest and tournament rows are research evidence only. They can suggest what to test next, but they are not investment advice and do not recommend any current action.

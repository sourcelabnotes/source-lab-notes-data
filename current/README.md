# Current Source Ledger Scorecards

Generated: 2026-06-30T19:32:02.094Z

Public package id: `package-e3f903d9b208de`

Replay batches included for asset-specific rows: 2

Estimated cost subtracted: 0.25 percentage points.

Public source boundary: this package identifies evidence by broad source class, not by named provider or raw source id. Provider names and raw source payloads stay in the local research database.

## Plain-English Read

The current public scorecard is still early research evidence, not investment advice. The clearest pattern-level lead is **Weak market, later bounce** with an average 4-hour result after costs of **+1.02%** across **125** examples. The strongest asset-specific slice is **AVAX / Weak market rejection**, with **+1.45%** after costs across **11** examples.

## Files

- `current_signal_family_scorecard.csv` (clue-family scorecard)
- `current_asset_signal_scorecard.csv` (asset-by-clue scorecard)
- `current_row_level_signal_evidence.csv`
- `current_pattern_observations.csv`
- `current_pattern_episodes.csv`
- `current_source_health_scorecard.csv`
- `current_research_leads.csv`

The row-level evidence file has 2254 replay rows. Use it to see the asset, timestamp, clue label, source mode, observed price, later return, and reason for each scored example.

The pattern audit files have 18382 timestamped clue observations grouped into 2022 persistence episodes. Use them to see when a clue was first seen, whether it persisted across later snapshots, which source class it came from, and how it was scored.

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

| source_class_id | source_class | current_status | latest_record_count | freshness_score | evidence_mode |
| --- | --- | --- | --- | --- | --- |
| source_class_chain_and_protocol_context | Chain and protocol context | ok | 4 | Current enough for latest checkpoint | api_or_scripted_collection |
| source_class_dex_activity_and_liquidity | Decentralized exchange activity and liquidity | ok | 13 | Current enough for latest checkpoint | api_or_scripted_collection |
| source_class_exchange_price_data | Exchange price and historical market data | ok | 2192 | Current enough for latest checkpoint | market_data_or_historical_replay |
| source_class_foreign_language_attention | Foreign-language news attention | ok | 63 | Stale for current checkpoint evidence | api_or_scripted_collection |
| source_class_market_data_and_trending | Market data and public attention rankings | ok | 39 | Current enough for latest checkpoint | api_or_scripted_collection |
| source_class_dashboard_ranking | Refreshed third-party dashboard ranking | ok | 71 | Stale for current checkpoint evidence | visual_capture |
| source_class_regional_premium_or_discount | Regional premium or discount | ok | 5 | Current enough for latest checkpoint | api_or_scripted_collection |
| source_class_social_onchain_development_context | Social, on-chain, and development context | ok | 9 | Stale for current checkpoint evidence | api_or_visual_capture |
| source_class_source_feature | Third-party source feature | ok | 8 | Recent context, not current checkpoint evidence | api_or_scripted_collection |
| source_class_wallet_or_large_holder_context | Wallet or large-holder context | ok | 15 | Stale for current checkpoint evidence | visual_capture |

## Caveat

These CSVs score patterns that were recorded in the local research database. Backtest and tournament rows are research evidence only. They can suggest what to test next, but they are not investment advice and do not recommend any current action.

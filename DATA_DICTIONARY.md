# Source Lab Notes Data Dictionary

Updated: June 29, 2026

## Core Idea

Source Lab Notes scores clues.

A clue is something visible at a point in time that someone might claim helps predict later crypto movement. The scorecard asks:

> When this clue was visible, what happened 1 hour, 4 hours, or 24 hours later after estimated costs?

## Current Files

| File | Grain | Use |
| --- | --- | --- |
| `current/current_signal_family_scorecard.csv` | One row per broad clue family or test rule. | Start here for the simplest current scorecard. |
| `current/current_asset_signal_scorecard.csv` | One row per asset, clue, and horizon slice. | Check whether a clue behaved differently by asset. |
| `current/current_row_level_signal_evidence.csv` | One row per historical replay observation. | Inspect the older row-level replay evidence behind the aggregate scorecards. |
| `current/current_pattern_observations.csv` | One row per timestamped clue observation. | Audit where a clue was seen, when, source category, source record id, freshness, and later outcome. |
| `current/current_pattern_episodes.csv` | One row per persistence episode. | See whether a clue appeared once or persisted across later snapshots. |
| `current/current_source_health_scorecard.csv` | One row per source. | Check whether sources were reachable and current enough to count. |
| `current/current_research_leads.csv` | One row per lead worth more testing. | See what looks worth studying next. |
| `SOURCE_CATALOG.csv` | One row per source category or source id. | Understand source categories, access methods, and disclosure boundaries. |

## Important Terms

| Term | Meaning |
| --- | --- |
| `clue` | A recorded piece of information that might help predict later movement. |
| `signal` | A clue that people might casually call a signal. Source Lab Notes treats this as a claim to test, not a fact. |
| `observation` | One clue captured at one timestamp for one asset/source/pattern. |
| `episode` | Repeated observations of the same clue/source/asset grouped together when they appear close in time. |
| `horizon` | The time window checked after the clue appeared, usually 1 hour, 4 hours, or 24 hours. |
| `estimated_cost_pct` | Estimated trading-cost hurdle subtracted before calling a result useful. Current default: 0.25 percentage points. |
| `raw_return_pct` | Price move before estimated costs. |
| `after_cost_pct` or `net_return_pct` | Price move after subtracting estimated costs. |
| `sample_count` | Number of scored examples in a row or slice. |
| `hit_rate_pct` | Percent of examples that ended positive after costs. |
| `source_freshness_status` | Whether the source looked current enough at the observation time. |

## Key Fields In Pattern Observations

| Field | Meaning |
| --- | --- |
| `observation_id` | Stable id for this normalized observation. |
| `episode_id` | Id of the persistence episode this observation belongs to. |
| `pattern_id` | Stable internal id for the clue definition. |
| `pattern_label` | Reader-facing clue name. |
| `signal_family` | Broad clue family, such as social attention, regional premium, broad market context, or price movement. |
| `asset` | Asset symbol. |
| `source_id` | Source identifier or source category used for audit. |
| `source_table` | Local source table used to normalize the observation. |
| `source_record_id` | Local source record id. |
| `evidence_mode` | How the evidence was captured, such as historical replay, scheduled API/source feature, or visual capture. |
| `observed_at_utc` | Time the clue was observed. |
| `run_id` | Local run id used to trace the collection or replay process. |
| `observation_role` | Whether this was a single observation, first seen, continuing, latest seen, or last seen. |
| `source_freshness_status` | Whether the source was current, recent, stale, historical replay, or had a source issue. |
| `source_freshness_note` | Plain-English source freshness note. |
| `clue_value` | Numeric clue value when available. |
| `clue_unit` | Unit for the numeric clue value. |
| `clue_text` | Short normalized clue text. |
| `direction_hint` | Source or rule label for the clue direction. |
| `context_label` | Additional source context. |
| `price_at_observation` | Price at or near the observation time, when available. |
| `forward_1h_raw_pct` | 1-hour later price move before costs, when available. |
| `forward_4h_raw_pct` | 4-hour later price move before costs, when available. |
| `forward_24h_raw_pct` | 24-hour later price move before costs, when available. |
| `estimated_cost_pct` | Cost hurdle subtracted from the 4-hour move. |
| `forward_4h_after_cost_pct` | 4-hour result after estimated costs. |
| `positive_after_costs_4h` | `1` if the 4-hour after-cost result was positive, `0` if not, blank if unavailable. |
| `audit_note` | Plain-English note on how to treat the row. |

## Key Fields In Pattern Episodes

| Field | Meaning |
| --- | --- |
| `episode_id` | Stable id for the persistence episode. |
| `pattern_id` | Stable id for the clue definition. |
| `pattern_label` | Reader-facing clue name. |
| `signal_family` | Broad clue family. |
| `asset` | Asset symbol. |
| `source_id` | Source identifier or category. |
| `evidence_mode` | How the evidence was captured. |
| `first_seen_at` | First time this clue/source/asset episode appeared. |
| `last_seen_at` | Last time this clue/source/asset episode appeared. |
| `observation_count` | Number of observations in this episode. |
| `duration_hours` | Time from first to last observation. |
| `episode_status` | Whether the episode is open, closed after a gap, or closed historical replay. |
| `max_gap_hours` | Maximum gap used to connect observations. Current default: 6 hours. |
| `score_basis` | Which observation is used for default scoring. Current default: first seen. |
| `first_observation_id` | Observation id used as the default scoring anchor. |
| `last_observation_id` | Last observation in the episode. |
| `first_forward_4h_after_cost_pct` | 4-hour after-cost result from the first observation. |
| `positive_after_costs_4h` | Whether the first observation's 4-hour after-cost result was positive. |
| `audit_note` | Plain-English note. |

## Caveats

- These files are research evidence, not investment advice.
- Some rows come from historical replay and some from point-in-time source collection.
- A positive average can still be too early, too narrow, or too dependent on one outlier.
- A source can be useful historically but stale for the latest checkpoint.
- These files publish normalized observations, not full third-party raw data.

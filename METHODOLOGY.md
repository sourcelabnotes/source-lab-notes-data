# Source Ledger Methodology

Updated: June 29, 2026

## What We Are Testing

Source Ledger tests whether a visible clue helped predict later crypto movement.

The basic loop is:

1. Record a clue before the result is known.
2. Preserve the timestamp, asset, source class, and clue definition.
3. Wait for the stated horizon.
4. Measure what happened later.
5. Subtract estimated costs.
6. Publish the hits, misses, and caveats.

## Why We Use Clue Instead Of Signal

Many traders and tools call these things signals. Source Ledger uses the softer word clue because the whole project is testing whether the clue deserved to be trusted.

## Observations And Episodes

An observation is one captured clue at one time.

An episode connects repeated observations of the same clue/source-class/asset when they appear close together in time. The current default maximum gap is 6 hours.

The default scoring basis is first seen. If a clue remains visible across several checks, later observations are kept for audit and persistence context, but the episode is not treated as a brand-new discovery every time.

## Time Horizons

The current scorecards focus on:

- 1 hour
- 4 hours
- 24 hours

The 4-hour window is usually the most stable fit for the current collection cadence.

## Estimated Cost

The default cost hurdle is 0.25 percentage points. This is a simple friction estimate, not a claim about exact execution costs for every venue or asset.

The point is to avoid calling a clue useful when it predicted a move too small to matter after ordinary trading friction.

## Source Boundaries

This repository publishes normalized observations and scorecards, not raw third-party datasets.

Public files may include:

- source classes or categories,
- plain-English source descriptions,
- pseudonymous public record/run ids,
- access method,
- timestamp,
- asset,
- clue label,
- source freshness status,
- later outcome,
- and audit notes.

Public files should not include:

- named-provider source ids unless there is a clear editorial reason,
- raw local source table names or source record ids,
- raw screenshots,
- raw HTML,
- private dashboard exports,
- account information,
- credentials,
- full copied third-party tables,
- wallet connection outputs,
- or local SQLite databases.

## How To Read A Result

A clue looks more interesting when:

- the sample is large enough to discuss,
- the average result remains positive after costs,
- the median does not contradict the average,
- the hit rate is not merely random-looking,
- the result is not carried by one large outlier,
- the clue beats a plain baseline,
- and the result holds for the relevant asset or source category.

A clue is weaker when:

- the good result disappears after costs,
- it only worked once,
- it only worked for one asset with a tiny sample,
- it needed too much after-the-fact explanation,
- or the source was stale or unverified.

## Standard Disclaimer

This is research, not investment advice. Nothing in this repository is a recommendation to buy, sell, or hold any asset.

# Previous-Day Levels — PDH/PDL + Breakout/Rejection Signals

A TradingView Pine Script® (v6) intraday indicator built from a personal
research library of 154 price-action strategy families. It plots the prior
day's high, low (and optional mid), and generates close-confirmed breakout
and wick-rejection signals at each level — no repainting.

## What it plots

- **PDH / PDL** — previous trading day's high and low, extended as lines
  into the current day
- **PD Mid** (optional) — midpoint of the previous day's range

## Signals (all confirmed on bar close only)

| Signal | Condition |
|---|---|
| PDH / PDL breakout | Fresh close through the level |
| PDH / PDL rejection | Wick sweeps the level on first touch, close back inside |
| Mid rejection up / down | Same rejection logic at the optional mid line |

## Alerts

Six built-in `alertcondition()` events (breakout ×2, rejection ×2,
mid rejection ×2) — wire them to TradingView alerts / webhooks.

## Inputs

| Input | Default | Notes |
|---|---|---|
| Show PDH/PDL lines | on | — |
| Show previous-day mid line | off | Enabling also enables mid-rejection signals |
| Breakout signals | on | — |
| Rejection signals | on | — |

## Install

1. Copy the contents of `previous-day-levels.pine`
2. Paste into the TradingView Pine Editor → **Add to chart**
3. Use on intraday timeframes (prior-day levels are tracked from daily bars)

## Research mapping

| Code | Strategy family | Evidence |
|---|---|---|
| PA-004 | Previous-day High/Low Breakout | C — rule described in the research library; no reproducible public experiment cited |
| PA-005 | Previous-day High/Low Rejection | C — rule described in the research library; no reproducible public experiment cited |

Evidence grade ≠ profitability. Rules are coded from the published strategy
description; no profitability claim.

## Disclaimer

Educational and research tool only. **Not investment advice.** Backtest any
rule with costs (commission + slippage) before risking capital.

Compilation: not yet verified in TradingView Pine Editor.

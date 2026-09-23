# Inside Bar Breakout — Mother-Bar Boundary Break

A TradingView Pine Script® (v6) intraday indicator built from a personal
research library of 154 price-action strategy families. It detects inside
bars (a bar fully contained in the previous bar's range), marks the mother
bar's high/low, and signals the first close-confirmed break of the mother
bar boundary — no repainting. Consecutive inside bars keep the original
mother bar as the reference.

## What it plots

- **Mother high / Mother low** — extremes of the mother bar (blue linebr),
  shown while the setup is active
- **Inside-bar markers** — small gray diamonds above each inside bar

## Signals (all confirmed on bar close only)

| Signal | Condition |
|---|---|
| Breakout up / down | First close above mother-bar high / below mother-bar low within N bars after an inside bar |

The setup expires after the configured number of bars (default 3) since the
inside bar — stale compression is not traded.

## Alerts

Two built-in `alertcondition()` events (breakout ×2) — wire them to
TradingView alerts / webhooks.

## Inputs

| Input | Default | Notes |
|---|---|---|
| Max bars since inside bar | 3 | 1–20 |
| Show mother high/low lines | on | — |
| Mark inside bars | on | — |
| Breakout signals | on | — |

## Install

1. Copy the contents of `inside-bar-breakout.pine`
2. Paste into the TradingView Pine Editor → **Add to chart**
3. Works on any timeframe; cleanest on 5–30 minute intraday bars

## Research mapping

| Code | Strategy family | Evidence |
|---|---|---|
| PA-045 | Inside Bar Breakout | C — rule described in the research library; no reproducible public experiment cited |

Evidence grade ≠ profitability. Rules are coded from the published strategy
description; no profitability claim.

## Disclaimer

Educational and research tool only. **Not investment advice.** Backtest any
rule with costs (commission + slippage) before risking capital.

Compilation: not yet verified in TradingView Pine Editor.

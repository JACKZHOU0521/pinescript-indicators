# Opening Range Breakout — OR High/Low + Breakout Signals

A TradingView Pine Script® (v6) intraday indicator built from a personal
research library of 154 price-action strategy families. It marks the first
N minutes of the trading day, plots the range high/low, and generates
close-confirmed breakout and retest-failure signals — no repainting.

## What it plots

- **OR High / OR Low** — highest high and lowest low of the first N minutes
  (default 30) after the exchange day open; lines appear once the window closes
- **OR Mid** (optional) — midpoint of the opening range

## Signals (all confirmed on bar close only)

| Signal | Condition |
|---|---|
| Breakout up / down | First close above OR high / below OR low after the window closes |
| Retest failure (long / short) | Broke out earlier today, then closed back inside the range |

## Alerts

Four built-in `alertcondition()` events (breakout ×2, retest failure ×2) —
wire them to TradingView alerts / webhooks.

## Inputs

| Input | Default | Notes |
|---|---|---|
| Opening window (minutes) | 30 | 5–240 |
| Show OR high/low lines | on | — |
| Show OR mid line | off | — |
| Breakout signals | on | — |
| Retest-failure signals | on | — |

## Install

1. Copy the contents of `opening-range-breakout.pine`
2. Paste into the TradingView Pine Editor → **Add to chart**
3. Use on intraday timeframes; works on regular and 24/7 symbols
   (on 24/7 symbols the "day open" is 00:00 exchange time)

## Research mapping

| Code | Strategy family | Evidence |
|---|---|---|
| PA-001 | Opening Range Breakout | B — multiple public ORB samples are reproducible |

Evidence grade ≠ profitability. "B" means the underlying experiment is public
and reproducible, not that it makes money. Rules are coded from the published
strategy description; no profitability claim.

## Disclaimer

Educational and research tool only. **Not investment advice.** Backtest any
rule with costs (commission + slippage) before risking capital.

Compilation: verified in TradingView Pine Editor (Pine v6) on 2026-09-23 — compiles with zero errors.

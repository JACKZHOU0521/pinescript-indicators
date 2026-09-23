# Lunch Range Breakout — Midday Box + Breakout Signals

A TradingView Pine Script® (v6) intraday indicator built from a personal
research library of 154 price-action strategy families. It builds a
consolidation box over a configurable midday window, freezes it when the
window ends, and generates close-confirmed breakout signals for the rest of
the session — no repainting.

## What it plots

- **Lunch high / Lunch low** — highest high and lowest low inside the midday
  window (default 11:30–13:00); lines appear once the window closes and reset
  each day

## Signals (all confirmed on bar close only)

| Signal | Condition |
|---|---|
| Breakout up / down | First close above lunch high / below lunch low after the window closes |

## Alerts

Two built-in `alertcondition()` events (breakout ×2) — wire them to
TradingView alerts / webhooks.

## Inputs

| Input | Default | Notes |
|---|---|---|
| Window start hour / minute | 11:30 | Exchange time |
| Window end hour / minute | 13:30 | Exchange time |
| Show lunch high/low lines | on | — |
| Breakout signals | on | — |

Notes:

- The window is evaluated in **exchange time** (the symbol's own timezone),
  not your local time.
- Common presets: 11:30–13:30 (US equities midday), 12:00–14:00 (European
  lunch), 11:00–13:00 (shorter box).

## Install

1. Copy the contents of `lunch-range-breakout.pine`
2. Paste into the TradingView Pine Editor → **Add to chart**
3. Use on intraday timeframes

## Research mapping

| Code | Strategy family | Evidence |
|---|---|---|
| PA-013 | Lunch Range Breakout | C — rule described in the research library; no reproducible public experiment cited |

Evidence grade ≠ profitability. Rules are coded from the published strategy
description; no profitability claim.

## Disclaimer

Educational and research tool only. **Not investment advice.** Backtest any
rule with costs (commission + slippage) before risking capital.

Compilation: verified in the TradingView Pine Editor (Pine Script v6) on 2026-09-23 — compiled with 0 errors, added to chart, no runtime errors observed.

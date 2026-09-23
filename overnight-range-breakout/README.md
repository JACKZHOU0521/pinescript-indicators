# Overnight Range Breakout — Overnight High/Low + Breakout Signals

A TradingView Pine Script® (v6) intraday indicator built from a personal
research library of 154 price-action strategy families. It tracks a
configurable overnight session window, plots the frozen overnight high/low
into the day session, and generates close-confirmed breakout signals —
no repainting.

## What it plots

- **ON High / ON Low** — highest high and lowest low inside the overnight
  session window (default 20:00–08:00); lines appear once the session ends

## Signals (all confirmed on bar close only)

| Signal | Condition |
|---|---|
| ON breakout up / down | First close above overnight high / below overnight low after the session ends |

## Alerts

Two built-in `alertcondition()` events (breakout up / down) — wire them to
TradingView alerts / webhooks.

## Inputs

| Input | Default | Notes |
|---|---|---|
| Session start hour / minute | 20:00 | Exchange time; window wraps across midnight |
| Session end hour / minute | 08:00 | Exchange time |
| Show overnight high/low lines | on | — |
| Breakout signals | on | — |

Notes:

- The session window is evaluated in **exchange time** (the symbol's own
  timezone), not your local time.
- Common presets: 20:00–08:00 (overnight), 16:00–09:30 (post-market +
  pre-market for US equities), 00:00–07:00 (Asia box in UTC terms —
  adjust to the symbol's exchange timezone).

## Install

1. Copy the contents of `overnight-range-breakout.pine`
2. Paste into the TradingView Pine Editor → **Add to chart**
3. Use on intraday timeframes

## Research mapping

| Code | Strategy family | Evidence |
|---|---|---|
| PA-006 | Overnight Range Breakout | C — rule described in the research library; no reproducible public experiment cited |

Evidence grade ≠ profitability. Rules are coded from the published strategy
description; no profitability claim.

## Disclaimer

Educational and research tool only. **Not investment advice.** Backtest any
rule with costs (commission + slippage) before risking capital.

Compilation: not yet verified in TradingView Pine Editor.

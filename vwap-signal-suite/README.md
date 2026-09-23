# VWAP Signal Suite — Session VWAP + Deviation Bands

A TradingView Pine Script® (v6) intraday indicator built from a personal
research library of 154 price-action strategy families. It plots session VWAP
with rolling standard-deviation bands and generates close-confirmed signals —
no repainting.

## What it plots

- **Session VWAP** — resets each trading day, weighted by typical price (hl2) × volume
- **Deviation bands** — ±1σ (inner) and ±2σ (outer) bands based on a rolling
  standard deviation of `close − VWAP` (default 30-bar window, adjustable)

## Signals (all confirmed on bar close only)

| Signal | Condition |
|---|---|
| VWAP cross up / down | Close crosses the VWAP line |
| Pullback reclaim up / down | Price taps an inner band, then closes back toward VWAP |
| Extreme deviation up / down | Close beyond the ±2σ outer band (mean-reversion watch zone) |

## Alerts

Six built-in `alertcondition()` events (VWAP cross ×2, pullback reclaim ×2,
extreme deviation ×2) — wire them to TradingView alerts / webhooks.

## Install

1. Copy the contents of `vwap-signal-suite.pine`
2. Paste into the TradingView Pine Editor → **Add to chart**

## Research mapping

| Code | Strategy family | Evidence |
|---|---|---|
| PA-030 | VWAP Cross Momentum | B — publicly reproducible experiment |
| PA-031 | VWAP Pullback Continuation | B — publicly reproducible experiment |
| PA-032 | VWAP Deviation Mean Reversion | B — publicly reproducible experiment |

Evidence grade ≠ profitability. "B" means the underlying experiment is public
and reproducible, not that it makes money.

## Disclaimer

Educational and research tool only. **Not investment advice.** Backtest any
rule with costs (commission + slippage) before risking capital.

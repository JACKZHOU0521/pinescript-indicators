# Gap and Go — Gap Hold + Opening-Swing Breakout

A TradingView Pine Script® (v6) intraday indicator built from a personal
research library of 154 price-action strategy families. It measures the
opening gap versus the prior close, checks that the gap "holds" (price never
fills it), and signals the first close-confirmed break of the opening swing
in the gap direction — no repainting.

## What it plots

- **Prior close** — previous daily close (gray linebr)
- **Swing high / Swing low** — highest high and lowest low of the opening
  swing (default first 15 minutes); lines appear once the window closes

## Signals (all confirmed on bar close only)

| Signal | Condition |
|---|---|
| Gap-and-go up | Gap ≥ min % and session low never touched prior close, then first close above swing high |
| Gap-and-go down | Gap ≤ −min % and session high never touched prior close, then first close below swing low |

No signal fires if the gap fills before the breakout — the "holds" filter is
the core of the pattern.

## Alerts

Two built-in `alertcondition()` events (gap-and-go ×2) — wire them to
TradingView alerts / webhooks.

## Inputs

| Input | Default | Notes |
|---|---|---|
| Min gap % | 0.5 | 0.1–10 |
| Opening swing (minutes) | 15 | 1–120 |
| Show prior close / swing lines | on | — |
| Gap-and-go signals | on | — |

## Install

1. Copy the contents of `gap-and-go.pine`
2. Paste into the TradingView Pine Editor → **Add to chart**
3. Use on intraday timeframes; gaps are rare on 24/7 symbols (crypto/forex),
   so this indicator is most useful on equities

## Research mapping

| Code | Strategy family | Evidence |
|---|---|---|
| PA-008 | Gap-and-Go | C — rule described in the research library; no reproducible public experiment cited |

Evidence grade ≠ profitability. Rules are coded from the published strategy
description; no profitability claim.

## Disclaimer

Educational and research tool only. **Not investment advice.** Backtest any
rule with costs (commission + slippage) before risking capital.

Compilation: not yet verified in TradingView Pine Editor.

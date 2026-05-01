# TradeChecks â€” Confluence//Desk v15

A self-contained trading decision-support dashboard built as a personal project to consolidate pre-trade analysis into one place. No frameworks, no npm, no build pipeline â€” a single HTML file you open in a browser.

---

## What it does

Before entering a trade, the dashboard runs through a structured set of checks across six areas:

**Market Regime**
Identifies the dominant market condition (trending, ranging, volatile) to filter which signals are relevant and adjust scoring weights accordingly.

**Technical Signals**
Composite score across RSI, EMA, Bollinger Bands, ATR, CVD momentum, and multi-timeframe alignment. Each indicator is weighted by its reliability in the current regime.

**Microstructure**
Order book depth, taker buy/sell flow, open interest trend, liquidity sweep detection, and whale account activity. Flags structural conditions that invalidate an otherwise valid technical signal.

**Sentiment & Macro**
Fear & Greed Index, BTC dominance, halving cycle position, retail long/short ratio, and live funding rates. Provides the broader context that determines whether the technical setup has tailwind or headwind.

**Session Quality**
Scores the current trading window based on session overlap, historical volatility patterns, and market breadth. Surfaces the next prime window if conditions are currently unfavourable.

**Risk & Position Sizing**
Calculates suggested entry zone, stop loss, take profit, max safe leverage, liquidation distance, trades-before-bust, and position size â€” all derived from user-defined account risk parameters rather than fixed defaults.

---

## Why single-file

Keeping everything in one HTML file was a deliberate constraint, not a shortcut.

It forces clarity: no abstraction layers, no hidden state, no build-time magic. Every piece of logic is visible and auditable in one place. The result is a tool that is fast to load, easy to inspect, and trivial to deploy â€” you drop the file anywhere and it works.

This mirrors the architectural philosophy behind AEM Edge Delivery Services, where simplicity and proximity to the raw output is a feature, not a limitation. Writing this project reinforced that constraint-driven design often produces more resilient systems than framework-driven design.

---

## Stack

- Vanilla HTML, CSS, JavaScript â€” zero dependencies
- Live market data via WebSocket and fetch calls to public crypto APIs
- Responsive layout built with CSS Grid and custom properties
- No build tools, no package manager, no transpilation

---

## Screens

**Overview** â€” multi-asset comparison grid with composite signal scores, critical flags, and session quality at a glance. Click any asset to open the full analysis.

**Detail** â€” full pre-trade checklist for a selected asset, including all six scoring areas, a situation verdict, and calculated risk parameters ready to use.

---

## Version history

This is v15. The project started as a simple checklist and evolved through 15 iterations as I identified gaps in my pre-trade process and refined the scoring logic. Earlier versions are preserved in the commit history.

---

## Status

Active personal project â€” updated as market conditions and trading approaches evolve.

*Not financial advice. Built for personal use and learning.*

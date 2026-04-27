# Synvoya Confluence (SMC)

> The most comprehensive free SMC/ICT indicator for TradingView. One indicator replaces ten.

---

## Features

| Module | What It Does | Included |
|---|---|---|
| **Market Structure** | Dual-layer BOS/CHoCH (Internal + Swing). Williams Fractal-style swing markers (▽△). HH/HL/LH/LL classification labels. Connector lines between pivots. | ✅ |
| **Order Blocks** | Bullish & bearish OBs with mitigation tracking. Auto-converts mitigated OBs into Breaker Blocks. | ✅ |
| **Fair Value Gaps** | Full FVG lifecycle — Active → Partial → Mitigated → Inverted (iFVG). CE midline (50% of gap). ATR-auto threshold. | ✅ |
| **Liquidity Levels** | Equal Highs / Equal Lows detection (ATR-adaptive). Sweep labels. Inducement (IDM) markers. | ✅ |
| **Premium / Discount** | Real-time zone shading with equilibrium line and live "72% Prem / 28% Disc" readout. | ✅ |
| **Sessions & Killzones** | Asia, Pre-London, London, Pre-NY, NY Open, NY AM, Lunch, NY PM. Silver Bullet windows (3). 8 ICT macro times. Auto-DST via NY timezone. | ✅ |
| **Asia H/L Extension** | Dashed H/L lines extending past Asia session close — key reference for NY Open direction bias. | ✅ |
| **Key Levels** | PDH/PDL, PWH/PWL, PMH/PML, Monday H/L, NY Midnight Open. All bounded with right-side labels. | ✅ |
| **CRT (Candle Range Theory)** | Detects CRT candles on 15m+ timeframes. Auto-extending H/L reference lines that freeze on touch. | ✅ |
| **ADR (Average Daily Range)** | 14-day ADR with live consumption % label. Judas swing levels (NY Midnight ± ADR/3). Optional projection lines. | ✅ |
| **SMT Divergence** | Auto-detects correlated pair: EU↔GU, XAU↔XAG, NAS↔SPX. Labels divergence at swing points. | ✅ |
| **Multi-TF Dashboard** | Bias table: Weekly / Daily / 4H / 1H direction (▲/▼/—) + active session name. | ✅ |
| **Legend** | Toggleable 25-row abbreviation key — explains every acronym on the chart. | ✅ |
| **Candle Coloring** | Direction mode (default) or structure-bias mode. | ✅ |
| **Alerts** | 8 conditions: Bullish BOS, Bearish BOS, Bullish CHoCH, Bearish CHoCH, FVG Touch, Liquidity Sweep, CRT Formation, SMT Divergence. | ✅ |

---

## Why One Indicator?

SMC/ICT traders typically need 8–10 separate indicators: LuxAlgo SMC, a separate FVG script, a session highlighter, CRT scanner, key levels indicator, SMT script, ADR script, and more. They overlap, conflict, and slow your charts down.

Synvoya Confluence puts every tool in one place. Every module is independently toggleable — show only what you need.

---

## Installation

1. Open [TradingView](https://www.tradingview.com)
2. Go to **Indicators → Community Scripts**
3. Search **"Synvoya Confluence"**
4. Click **Add to Chart**

---

## Compatibility

Works on any pair and any timeframe. Optimized for:

- **Forex** — EURUSD, GBPUSD, USDJPY, all major/minor pairs
- **Gold** — XAUUSD
- **Indices** — NAS100, SPX500, US30, DAX
- **Crypto** — BTC, ETH, all major tokens

Sessions and macros use `America/New_York` timezone internally — correct across all broker timezones and auto-adjusts for DST.

---

## SMC/ICT Glossary

| Term | Meaning |
|---|---|
| **BOS** | Break of Structure — price breaks beyond a previous swing high/low, confirming trend continuation |
| **CHoCH** | Change of Character — price breaks against the trend, signaling a potential reversal |
| **iBOS** | Internal Break of Structure — same as BOS but on the internal (minor) swing layer |
| **iCHoCH** | Internal Change of Character — CHoCH on the internal swing layer |
| **OB** | Order Block — the last opposing candle before an impulsive move; institutional entry zone |
| **BB** | Breaker Block — a mitigated OB that flips to act as the opposite zone |
| **FVG** | Fair Value Gap — 3-candle price imbalance; price tends to return to fill it |
| **iFVG** | Inverse FVG — a fully mitigated FVG that flips to resistance/support in the opposite direction |
| **CE** | Consequent Encroachment — the 50% midpoint of an FVG; the institutional entry level |
| **EQH / EQL** | Equal Highs / Equal Lows — clusters of similar prices where stop orders rest (liquidity) |
| **IDM** | Inducement — a minor swing used as a liquidity trap before the real move |
| **CRT** | Candle Range Theory — a candle that sweeps both the high and low of the prior candle |
| **ADR** | Average Daily Range — typical daily move distance; used to gauge exhaustion |
| **SMT** | Smart Money Technique — correlated pairs diverge at swing points, signaling reversal |
| **PDH / PDL** | Previous Day High / Low |
| **PWH / PWL** | Previous Week High / Low |
| **PMH / PML** | Previous Month High / Low |

---

## Technical

- **Language:** Pine Script v6
- **Type:** Overlay indicator, single file
- **Draw object limits:** 500 lines / 500 boxes / 500 labels (declared at indicator level)
- **Security calls:** 9 (well within TradingView's 40-call limit)
- **Timeframe gate:** High-noise items (HH/HL labels, fractal connectors, CRT) suppressed below 15m to prevent chart clutter

---

## Author

**Synvoya** — [synvoya.com](https://synvoya.com)

## License

Open source under TradingView Community Scripts terms.

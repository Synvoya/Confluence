# Synvoya Confluence (SMC)

> The most comprehensive free SMC/ICT indicator for TradingView. One indicator replaces ten.

---

## Features

| Module | What It Does | Included |
|---|---|---|
| **Market Structure** | Dual-layer BOS/CHoCH (Internal + Swing). HH/HL/LH/LL classification labels. Connector lines between pivots. | ✅ |
| **Fractal Markers** | Williams-Fractal-style swing markers (▽△) on every TF (no HTF gate). Dedicated bull/bear color inputs — distinct from BOS/CHoCH structure colors. | ✅ |
| **Order Blocks** | Bullish & bearish OBs with mitigation tracking. Auto-converts mitigated OBs into Breaker Blocks. | ✅ |
| **Fair Value Gaps** | Full FVG lifecycle — Active → Partial → Mitigated → Inverted (iFVG). CE midline (50% of gap). ATR-auto threshold. | ✅ |
| **Liquidity Levels** | Equal Highs / Equal Lows detection (ATR-adaptive). Sweep labels. Inducement (IDM) markers. | ✅ |
| **Premium / Discount** | Real-time zone shading with equilibrium line and live "72% Prem / 28% Disc" readout. | ✅ |
| **Market Sessions** | Asia, Pre-London, London, Pre-NY, NY (combined or split into NY Open / NY AM / Lunch / NY PM). Uses actual market hours (London open 03:00 NY = 08:00 BST/GMT, NYSE open 09:30 NY). Auto-DST via NY timezone. | ✅ |
| **ICT Killzones** | Optional opt-in feature for ICT traders. Asia (20:00–00:00 NY), London Open (02:00–05:00), NY AM (07:00–10:00), NY PM (13:30–16:00). Toggleable separately from sessions. | ✅ |
| **Silver Bullet & Macros** | 3 Silver Bullet windows + 8 ICT macro times. | ✅ |
| **Asia H/L Extension** | Dashed H/L lines extending past Asia session close — key reference for NY Open direction bias. | ✅ |
| **Key Levels** | PDH/PDL, PWH/PWL, PMH/PML, Monday H/L, NY Midnight Open. All bounded with right-side labels. | ✅ |
| **CRT (Candle Range Theory)** | Detects CRT candles on 15m+ timeframes. Auto-extending H/L reference lines that freeze on touch. | ✅ |
| **ADR (Average Daily Range)** | 14-day ADR with live consumption % label. Judas swing levels (NY Midnight ± ADR/3). Optional projection lines. | ✅ |
| **SMT Divergence** | Auto-detects correlated pair: EU↔GU, XAU↔XAG, NAS↔SPX. Labels divergence at swing points. | ✅ |
| **Multi-TF Dashboard** | Dual-bias confluence table: W/D/4H/1H × Struct (5/5 pivot BOS) + EMA (9/21 cross, configurable). Live session name (wall-clock based, not bar-time). Live NY Time clock. | ✅ |
| **EMA Trend Lines** | Optional plot of the same fast/slow EMAs used for the dashboard EMA bias column. Visible on chart as two lines — see the cross visually, not just the dashboard arrow. Default OFF. | ✅ |
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

## Dashboard — Reading the Confluence

The dashboard shows **two bias signals per timeframe**, side-by-side:

| TF  | Str | EMA |
|-----|:---:|:---:|
| W   |  ▲  |  ▲  |
| D   |  ▲  |  ▼  |
| 4H  |  ▲  |  ▼  |
| 1H  |  ▼  |  ▼  |
| Session | London |   |
| NY Time | 03:39  |   |

- **Str** — 5/5 pivot BOS detection. Same logic as the chart's market structure module. Sticky — flips only on real structural breaks.
- **EMA** — EMA cross (default 9/21, configurable in Settings). Faster trend filter — flips within 3-5 bars of a real reversal.

**How to read:**
- **Both ▲** = high-confidence bullish
- **Both ▼** = high-confidence bearish
- **Str ▲ + EMA ▼** = pullback within bullish structure (potential entry zone)
- **Str ▼ + EMA ▲** = bear structure breaking, recovery starting

**Session and NY Time** rows use live wall-clock (not bar-open time) — reflect what's actually happening NOW, not what session the current HTF bar opened in.

---

## Technical

- **Language:** Pine Script v6
- **Type:** Overlay indicator, single file
- **Draw object limits:** 500 lines / 500 boxes / 500 labels (declared at indicator level)
- **Security calls:** 9 (well within TradingView's 40-call limit) — dashboard biases bundled into 4 tuple calls (one per TF returning [Struct, EMA])
- **Timeframe gate:** High-noise items (HH/HL labels, fractal connectors, CRT) suppressed below 15m to prevent chart clutter
- **All times:** NY-localized (`America/New_York`) — auto-DST, broker-timezone independent

---

## Author

**Synvoya** — [synvoya.com](https://synvoya.com)

## License

Open source under TradingView Community Scripts terms.

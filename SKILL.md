---
name: MarketAnalysis-FormatChatAiAgent
description: Market analysis format standard - Astronacci + Fibonacci + Fear & Greed, universal for XAUUSD/BTC/forex/index
---

# Market Analysis Format — AI Agent

## 🔴 CRITICAL: ABSOLUTE FORMAT — DO NOT IMPROVISE

This format has been through 20+ iterations and the user gets FURIOUS every time the format is wrong. READ THIS BEFORE ANY OUTPUT:

1. **Bold `** **`** for: main title, all section titles
2. **Code block ` ``` `** for: technical table, history data — nothing else
3. **Plain text** for: Fundamental paragraph, Price Movement, Waiting Sell/Buy Area, Mirroring Assistant Intraday
4. **Links MUST be embedded** in the Fundamental text using `[text](link)` — never put links separately at the end
5. **Fear & Greed MUST** be in every Fundamental with link to alternative.me
6. **History Data MUST appear** even if it's just Waiting Order
7. Never send plain text output (without bold / without code block). The user gets ANGRY when this happens
8. Never send over-formatted output (code block in entry area, etc.)
9. Applies to ALL pairs (XAUUSD, BTC, EURUSD, etc.)

Market analysis format using Astronacci + Fibonacci standard. Works for any pair.

## Agent Persona

- **Tone: ngeselin, deadpan sarkas** — not overly friendly, not robotic
- **BUKAN alay** — no wkwk, no excessive emoji, no cute talk
- **Langsung gas, no small talk** — output langsung tanpa pengantar
- **Do not** ask the user what they want — just execute

## Trigger Behavior

When user says "analisa xauusd", "analisa btc", "analisa eurusd", or similar:
1. **LANGSUNG output** — jangan nanya apa pun
2. **Jangan kasih pengantar** — no "siap", "oke", "gua cek dulu"
3. **Langsung fetch data dan output sesuai template**
4. **Dilarang nanya timeframe/scalping/swing/entry** — langsung gas
5. For non-gold assets: adapt the template accordingly (same structure)

### When to Create New Analysis

- First analysis of the day = **Live Analyst1**. Full fundamental + fib + table.
- **Do NOT** create a new analysis before the current entry hits **TP2** or **SL**. Unless user explicitly asks.
- Each subsequent analysis increments the number: Analyst1, Analyst2, Analyst3, etc.
- Entries still running (TP3/TP4) must NOT be removed — move to **Mirroring Running Area** (code block format)
- Entries not yet hit → **Waiting, Sell/Buy Area** (plain text format)
- Only create a new analysis if the user ASKS for it

### Running Entry Handling

**When there is a running position:** the output must have BOTH:
1. **Mirroring Running Area** (code block) — shows current running entries with Hit/Running/Safe status
2. **Mirroring Waiting Area** (plain text) — shows new waiting entries that haven't been triggered

**When there is NO running position:**
- **Waiting, Sell Area** (plain text) — new sell entries
- **Waiting, Buy Area** (plain text) — new buy entries

## Installation

```
hermes skills install https://raw.githubusercontent.com/Mftrferdinand/MarketAnalysis-FormatChatAiAgent/main/SKILL.md
```

Or clone into `~/.hermes/skills/`:
```
git clone https://github.com/Mftrferdinand/MarketAnalysis-FormatChatAiAgent ~/.hermes/skills/research/MarketAnalysis-FormatChatAiAgent
```

## Output Format

### Full Template (XAUUSD) — EXACT Output Example

**XAUUSD - $3,985 Live Analyst1**
**1 July 2026, 09:52 WIB**

**Fundamental Economic Global**
Gold dropped to $3,985 after failing to hold above $4,000. [The Fed hawkish stance](https://news.google.com/articles/...) remains the main pressure. [Fear Greed Index](https://alternative.me) 11 (Extreme Fear).

**Technical Market Analysis**
Price $3,985 below SMA20 ($4,221) and Fib 78.6% ($4,097) — bearish.

```
Level                    Price
Swing High 30d           $4,591
SMA20                    $4,221
Fib 78.6%                $4,097
Current Price            $3,985
Swing Low 30d            $3,955
BB Lower                 $3,906
```

RSI 36.5 — Bearish
Volume — Normal

**Price Movement Analysis**
Price dropped from $4,047 to $3,985 — failed to hold above $4,000. Astronacci Wave 3 down, currently testing intraday swing low at $3,983. If it breaks, target $3,955 (Wave 5). Potential bounce to $4,030 if it holds.

**Waiting, Sell Area**
✷ ENTRY SELL : 4,030 - 4,033
✷ TAKE PROFIT 1 : 4,021
✷ TAKE PROFIT 2 : 4,011
✷ TAKE PROFIT 3 : 3,981
✷ TAKE PROFIT 4 : 3,931
✷ STOP LOSS : 4,041

**Waiting, Buy Area**
✧ ENTRY BUY : 3,982 - 3,985
✧ TAKE PROFIT 1 : 3,993
✧ TAKE PROFIT 2 : 4,003
✧ TAKE PROFIT 3 : 4,033
✧ TAKE PROFIT 4 : 4,083
✧ STOP LOSS : 3,973

**Mirroring Assistant Intraday**
Bearish dominant. Price at swing low $3,983 — if it breaks, target $3,955. Sell bounce to $4,030-4,033. Buy support zone $3,982-3,985 for scalping, tight SL $3,973.

**XAUUSD History Data**

```
XAUUSD, 1 July 2026
✷ A1 : Waiting Order
```

### Trade Update Format

**XAUUSD Live Trade Update**

```
Entry Sell M15 : Running
✷ Entry : X,XXX - X,XXX Hit
✷ TP1 : X,XXX Running
✷ TP2 : X,XXX Running
✷ TP3 : X,XXX
✷ TP4 : X,XXX
✷ SL : X,XXX Safe
```

**Update at HH:MM WIB :**
[price update, distance to TP/SL]

### History Data Labels

- `TP4 : 1000 Pips` = TP1 to TP4 all hit
- `TP3 : 500 Pips` = TP3 hit
- `TP2 : 200 Pips` = TP2 hit
- `TP1 : 100 Pips` = only TP1 hit
- `SL` = Stop loss hit directly
- `Running` = entry hit, position still open
- `Waiting Order` = entry not yet triggered

### RR Ratio (M15 Only)

- Entry range: 30 pips
- SL: 100 pips from mid entry
- TP1: 100 pips (1:1)
- TP2: 200 pips (1:2)
- TP3: 500 pips (1:5)
- TP4: 1000 pips (1:10)
- Mid entry = (low + high) / 2

## SL Status Variations

- `Safe` : SL not yet hit
- `Alright, TP1 Hit` : TP1 hit first, then SL hit
- `All Good :p` : All TPs hit
- `Sorry, SL Hit` : Direct SL hit

## Mandatory Rules

### Markdown Rules

- **ALL titles** and **section titles** use bold markdown `** **`
- **Technical table** and **History Data** use code block ` ``` `
- **Fundamental** — news links embedded in text using `[text](link)`
- **Waiting, Sell/Buy Area** — plain text, DO NOT put in code block
- **Mirroring Assistant Intraday** — plain text

### Title Format

- **XAUUSD - $PRICE Live Analyst1** (bold)
- **DATE, TIME WIB** (bold second line)
- Date format: DD MONTH YYYY, 24HR WIB
- Analysis number increments: Analyst1, Analyst2, Analyst3, etc.

### When to Create New Analysis

- First analysis of the day = **Live Analyst1** (full fundamental + fib + table)
- **Do NOT** create a new analysis before the current entry hits **TP2** or **SL**. Unless user explicitly asks.
- Each subsequent analysis increments the number: Analyst1, Analyst2, Analyst3, etc.
- Entries still running (TP3/TP4) must NOT be removed — move to **Mirroring Running Area** (code block format)
- Entries not yet hit → **Waiting, Sell/Buy Area** (plain text format)
- Only create a new analysis if the user ASKS for it

### Fundamental Section

- MUST fetch news from news scraper first
- 2-3 sentences: inflation, interest rates, geopolitics, NFP/CPI/FOMC
- Source links embedded in text
- MUST include Fear & Greed Index

### Entry Area

- Entry range: 30 pips
- SL: 100 pips from mid entry
- TP1: 100 (1:1), TP2: 200 (1:2), TP3: 500 (1:5), TP4: 1000 (1:10)
- Find nearest support/resistance zones from current price

### History Data in Output

- Only show current day's data
- Previous days' data only if user requests
- Waiting Order MUST still be shown
- If only Waiting Order exists, History Data section MUST still appear

## Data Sources

- Gold spot: gold-api.com + fxratesapi
- Gold futures: Yahoo Finance GC=F
- Fear & Greed: alternative.me
- News: Google News RSS

## Skill Overlap

⚠️ `research/market-research` (SUPERSEDED) — do not use.
⚠️ Old `market-ecosystem` skill — already merged. Do not use.

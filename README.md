# MarketAnalysis-FormatChatAiAgent

**Complete market analysis format for AI chat agents.** Astronacci + Fibonacci + Fear & Greed + structured entries with fixed risk management. Works for XAUUSD, BTC, forex, indices, crypto — any market.

👉 **Install for Hermes Agent:**
```
hermes skills install https://raw.githubusercontent.com/Mftrferdinand/MarketAnalysis-FormatChatAiAgent/master/SKILL.md
```

## What This Is

A structured market analysis template designed for AI chat agents (Hermes, Claude, ChatGPT, etc.) to deliver **consistent, disciplined analysis** every time. No improvisation. No broken formats.

Each output includes:
- **Fundamental Economic Global** — macro news with embedded links, Fear & Greed Index
- **Technical Market Analysis** — Fibonacci retracement, SMA20, Bollinger Bands, RSI, volume
- **Price Movement Analysis** — last 6 hours with Astronacci / Elliott Wave structure
- **Waiting, Sell/Buy Area** — entry zones with fixed RR (30 pip range, 100 pip SL)
- **Mirroring Assistant Intraday** — directional bias, support/resistance
- **XAUUSD History Data** — daily performance tracking
- **Trade Update Format** — live position tracking with TP/SL status

## Why Use This

| Problem | Solution |
|---------|----------|
| AI agents output inconsistent format | Fixed template with bold + code block rules |
| No risk management | **Fixed RR:** Entry 30 pips, SL 100 pips, TP1 100 (1:1), TP2 200 (1:2), TP3 500 (1:5), TP4 1000 (1:10) |
| No news context | Fundamental section **requires** live news scrape with embedded links |
| Wave analysis missing | Astronacci/Elliott Wave structure in Price Movement |
| No trade history | Daily History Data tracks every entry outcome |
| Emotional trading | Risk management rules + trade psychology notes are built into the skill |

## Sample Output

```
**XAUUSD - $3,985 Live Analyst1**
**1 July 2026, 09:52 WIB**

**Fundamental Economic Global**
Gold dropped to $3,985 after failing to hold above $4,000. The Fed hawkish stance remains the main pressure. Fear Greed Index 11 (Extreme Fear).

**Technical Market Analysis**
Price $3,985 below SMA20 ($4,221) and Fib 78.6% ($4,097) — bearish.

Level                    Price
Swing High 30d           $4,591
SMA20                    $4,221
Fib 78.6%                $4,097
Current Price            $3,985
Swing Low 30d            $3,955
BB Lower                 $3,906

RSI 36.5 — Bearish
Volume — Normal

**Waiting, Sell Area**
✷ ENTRY SELL : 4,030 - 4,033
✷ TAKE PROFIT 1 : 4,021
✷ TAKE PROFIT 2 : 4,011
✷ TAKE PROFIT 3 : 3,981
✷ TAKE PROFIT 4 : 3,931
✷ STOP LOSS : 4,041
```

## Installation

### For Hermes Agent
```
hermes skills install https://raw.githubusercontent.com/Mftrferdinand/MarketAnalysis-FormatChatAiAgent/master/SKILL.md
```

### Manual clone
```
git clone https://github.com/Mftrferdinand/MarketAnalysis-FormatChatAiAgent ~/.hermes/skills/research/MarketAnalysis-FormatChatAiAgent
```

### For other AI agents (Claude, ChatGPT, Codex, etc.)
Copy the template structure from `SKILL.md` into your system prompt or agent instructions.

## Key Features

- **Astronacci / Elliott Wave** analysis built into Price Movement section
- **Fibonacci** retracement levels from 30d swing high/low
- **Fixed risk parameters** — never deviate from 30 pip entry, 100 pip SL
- **RR ladder** — TP1 (1:1), TP2 (1:2), TP3 (1:5), TP4 (1:10)
- **Live data integration** — gold spot, futures, Fear & Greed Index, news
- **Persona built-in** — tone, trigger behavior, running entry handling
- **Trade Psychology notes** — trust the system, avoid revenge trading

## For All Markets

This format works for:
- **XAUUSD / Gold** — primary design target
- **BTC / Crypto** — adapt Fibonacci levels, news sources
- **Forex** — EURUSD, GBPUSD, etc.
- **Indices** — S&P 500, Dow Jones, Nikkei
- **Any asset** with price data

## Author

Created by Mftrferdinand.

## License

MIT — Free to use, modify, and share.

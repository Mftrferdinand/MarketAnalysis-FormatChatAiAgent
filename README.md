# MarketAnalysis-FormatChatAiAgent

**Complete market analysis format for AI chat agents.** Astronacci + Fibonacci + structured entries with tight risk management. Works for XAUUSD, BTC, forex, indices — any market.

👉 **Install for Hermes Agent:**
```
hermes skills install https://raw.githubusercontent.com/Mftrferdinand/MarketAnalysis-FormatChatAiAgent/master/SKILL.md
```

## What This Is

A structured market analysis template designed for AI chat agents (Hermes, Claude, ChatGPT, etc.) to deliver **consistent, disciplined analysis** every time. No improvisation. No broken formats.

## Final Format (v3 — 3 July 2026)

```
**XAUUSD Research and Analysis**
$4,178 : 03/07/26, 13:15 WIB

**Fundamental Economic Global**
|Gold continues its rally to $4,178 after weak US NFP data at 114K vs 172K expected, weakening the dollar. Fed Chair Warsh indicated inflation risks have eased, dovish narrative strengthening. ISM Manufacturing softened to 53.8 and gold acceptance above $4,000 after weak data.

**Technical Market Analysis**
Price $4,178 sits right above SMA20 ($4,171) — testing dynamic resistance.

Level                    Price
Swing High 30d           $4,510
SMA20                    $4,171
Current Price            $4,178
Fib 61.8%                $4,203
Fib 78.6%                $4,097
Swing Low 30d            $3,962
BB Lower                 $3,932

RSI 42.0 — neutral area, leaving oversold zone, recovery momentum continues
Volume — spike in NFP session indicates high market participation, confirming breakout validity

**Price Movement Analysis**
Price rebounded from $4,062 to $4,178 after weak NFP data.

**Assistant Intraday Outlook**
Limited bearish bias with bullish potential if price holds above SMA20. Resistance at $4,203 (Fib 61.8%). Support at $4,097 (Fib 78.6%). Bullish invalidation level above $4,221.

**Waiting, Sell Area 4,200 - 4,210**
✷ Take Profit 1 : 4,190
✷ Take Profit 2 : 4,180
✷ Take Profit 3 : 4,150
✷ Take Profit 4 : 4,100
✷ Stop Loss : 4,221

**Waiting, Buy Area 4,085 - 4,095**
✷ Take Profit 1 : 4,105
✷ Take Profit 2 : 4,115
✷ Take Profit 3 : 4,145
✷ Take Profit 4 : 4,195
✷ Stop Loss : 4,075

PROTECT YOUR CAPITAL, MANAGE YOUR RISK, USE SL, AIM FOR REALISTIC TP
```

## Format Rules

| Element | Rule |
|---------|------|
| Title | Line 1: **BOLD** — **XAUUSD Research and Analysis** |
|  | Line 2: plain — $PRICE : DD/MM/YY, HH:MM WIB |
| Fundamental | 2-3 sentences with **min 3-4 embedded links** |
| Technical | Fibonacci + SMA20 + BB + code block table |
| RSI | 1 line: `RSI XX.X — [status], [interpretation]` |
| Volume | 1 line: `Volume — [interpretation]` |
| Price Movement | 2-3 sentences, Astronacci Wave analysis |
| Outlook | Observational only, ABOVE Waiting Areas |
| Entry Area | Bold title with range, plain TP1-4 + SL with ✷ |
| ✷ symbol | Used for BOTH Sell and Buy |
| Footer | Code block: `PROTECT YOUR CAPITAL, MANAGE YOUR RISK, USE SL, AIM FOR REALISTIC TP` |
| No history data | Footer replaces history data entirely |

## Key Features

- **Astronacci / Elliott Wave** analysis built into Price Movement section
- **Fibonacci** retracement levels from 30d swing high/low
- **Fixed risk parameters** — 30 pip entry, 100 pip SL, TP1-4 ladder
- **Min 3-4 news links** per analysis — never rely on single source
- **Observational language** — no "buy/sell/entry" directives
- **Clean format** — bold titles, code block tables, consistent footer

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

# Template Example — XAUUSD Full Analysis

Below is a complete example of the output format. Every analysis MUST follow this structure exactly.

This is the FINAL format — markdown with bold titles, code blocks for table and history, embedded links, ✷/✧ symbols for entries.

---

**XAUUSD - $3,985 Live Analyst1**
**1 July 2026, 09:52 WIB**

**Fundamental Economic Global**
Gold dropped to $3,985 after failing to hold above $4,000. [The Fed hawkish stance](https://news.google.com/articles/...) remains the main pressure.

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

```
XAUUSD, 1 July 2026
✷ A1 : Waiting Order
```

---

## Analyst Numbering Example

Analyst number berlanjut antar hari, hanya naik jika order KE ENTRY:

Day 1 (29 June):
```
XAUUSD, 29 June 2026
✷ A1 : Waiting Order
```

Day 1 (29 June, analysis 2 — user requested):
```
XAUUSD, 29 June 2026
✷ A1 : TP2 : 200 Pips
✷ A2 : Waiting Order
```

Day 2 (30 June — A1 hit order, A2 not hit):
```
XAUUSD, 30 June 2026
✷ A3 : Waiting Order
```
(A2 tidak ke entry → number tidak naik untuk A2, tapi A1 ke entry → A3 adalah analysis berikutnya)

Day 3 (1 July — A3 hit order):
```
XAUUSD, 1 July 2026
✷ A4 : Waiting Order
```

Day 4 (2 July — A4 NOT hit):
```
XAUUSD, 2 July 2026
✷ A4 : Waiting Order
```
(A4 tidak ke entry → number tetap A4, bukan A5)

Day 5 (3 July — A4 hit order):
```
XAUUSD, 3 July 2026
✷ A5 : Waiting Order
```

## Trade Update Example

**XAUUSD Live Trade Update**

```
Entry Sell M15 : Running
✷ Entry : 4,030 - 4,033 Hit
✷ TP1 : 4,021 Hit
✷ TP2 : 4,011 Running
✷ TP3 : 3,981
✷ TP4 : 3,931
✷ SL : 4,041 Safe
```

**Update at 11:30 WIB :**
Price at $4,015 — TP1 hit, TP2 at $4,011 is 4 pips away. SL at $4,041 is safe (26 pips above).

## Entry with Running Position Example

When there are active running positions, the output includes BOTH running area and waiting area:

**Mirroring Running Area**
```
Entry Sell M15 : Running
✷ Entry : 4,030 - 4,033 Hit
✷ TP1 : 4,021 Hit
✷ TP2 : 4,011 Running
✷ TP3 : 3,981
✷ TP4 : 3,931
✷ SL : 4,041 Safe
```

**Mirroring Waiting Area**
✷ ENTRY SELL : 4,120 - 4,123
✷ TAKE PROFIT 1 : 4,110
✷ TAKE PROFIT 2 : 4,100
✷ TAKE PROFIT 3 : 4,070
✷ TAKE PROFIT 4 : 4,020
✷ STOP LOSS : 4,133

## History Data Labels

| Label | Meaning |
|---|---|
| TP4 : 1000 Pips | TP1 to TP4 all hit |
| TP3 : 500 Pips | TP3 hit |
| TP2 : 200 Pips | TP2 hit |
| TP1 : 100 Pips | Only TP1 hit |
| SL | Stop loss hit directly |
| Running | Entry hit, position still open |
| Waiting Order | Entry not yet triggered |
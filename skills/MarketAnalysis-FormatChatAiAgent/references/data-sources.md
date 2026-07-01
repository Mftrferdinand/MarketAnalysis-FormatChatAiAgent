# Data Sources — Market Analysis Format

Working fetch commands verified in this session.

## Gold Spot Price

```bash
# gold-api.com (fast, no key needed)
curl -s 'https://api.gold-api.com/price/XAU' -H 'Content-Type: application/json'

# fxratesapi.com (fallback)
curl -s 'https://api.fxratesapi.com/latest?base=XAU'
```

Average both for spot price.

## Gold Futures + Indicators (Yahoo Finance)

```bash
# Full chart data (3mo daily)
curl -s 'https://query1.finance.yahoo.com/v8/finance/chart/GC%3DF?range=3mo&interval=1d'
```

Python snippet to extract swing high/low, SMA20, RSI14, BB, volume, fib levels:

```python
import json, urllib.request, math

url = 'https://query1.finance.yahoo.com/v8/finance/chart/GC%3DF?range=3mo&interval=1d'
req = urllib.request.Request(url, headers={'User-Agent': 'Mozilla/5.0'})
data = json.loads(urllib.request.urlopen(req, timeout=15).read().decode())
chart = data['chart']['result'][0]
quotes = chart['indicators']['quote'][0]
closes = [c for c in quotes['close'] if c is not None]
highs  = [h for h in quotes['high'] if h is not None]
lows   = [l for l in quotes['low'] if l is not None]
vols   = [v for v in quotes['volume'] if v is not None]

recent = closes[-30:]
swing_high = max(recent)
swing_low  = min(recent)
diff = swing_high - swing_low
sma20 = sum(closes[-20:]) / 20

gains, losses = [], []
for i in range(1, 15):
    d = closes[-15+i] - closes[-16+i]
    if d > 0: gains.append(d)
    else:     losses.append(-d)
avg_g, avg_l = sum(gains)/14, (sum(losses)/14) if losses else 0
rsi = 100 - 100/(1 + avg_g/avg_l) if avg_l else 100

mean = sum(closes[-20:]) / 20
var  = sum((x - mean)**2 for x in closes[-20:]) / 20
std  = math.sqrt(var)

avg_vol = sum(vols[-10:]) / 10
vol_ratio = vols[-1] / avg_vol if avg_vol else 0
weekly_pct = ((closes[-1] - closes[-8]) / closes[-8]) * 100 if len(closes) >= 8 else 0

print(f'Swing High 30d: ${swing_high:.2f}')
print(f'Swing Low 30d:  ${swing_low:.2f}')
print(f'SMA20:          ${sma20:.2f}')
print(f'RSI14:          {rsi:.1f}')
print(f'BB Upper:       ${mean+2*std:.2f}')
print(f'BB Lower:       ${mean-2*std:.2f}')
print(f'Fib 0%:         ${swing_high:.2f}')
print(f'Fib 78.6%:      ${swing_high-diff*0.786:.2f}')
print(f'Fib 100%:       ${swing_low:.2f}')
print(f'Volume ratio:   {vol_ratio:.1f}x')
print(f'Weekly change:  {weekly_pct:.2f}%')
```

## Fear & Greed Index

```bash
curl -s 'https://api.alternative.me/fng/?limit=1'
```

Returns: `value` (0-100), `value_classification` (Extreme Fear / Fear / Neutral / Greed / Extreme Greed).

## Google News RSS

```bash
curl -s 'https://news.google.com/rss/search?q=gold+price+XAUUSD&hl=en-US&gl=US&ceid=US:en'
curl -s 'https://news.google.com/rss/search?q=Federal+Reserve+rate+gold&hl=en-US&gl=US&ceid=US:en'
```

Parse with Python's `xml.etree.ElementTree`. Extract `<item>` → `<title>` + `<link>`.
Links are Google News redirect URLs — usable as-is in markdown `[text](link)`.

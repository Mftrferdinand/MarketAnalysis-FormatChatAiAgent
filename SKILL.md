# XAUUSD Market Analysis Format — AES

XAUUSD analysis format dengan standard Astronacci + Fibonacci. Bisa dipake buat pair lain juga. Author: @mftrferdinand.

## Cara Install

```
hermes skills install https://raw.githubusercontent.com/mftrferdinand/hermes-xauusd-skill/main/SKILL.md
```

Atau clone repo ini ke `~/.hermes/skills/`:
```
git clone https://github.com/mftrferdinand/hermes-xauusd-skill ~/.hermes/skills/research/xauusd-aes
```

## Format Output Final

### Template Lengkap (XAUUSD)

**XAUUSD - $HARGA Live Analyst1**
**TANGGAL, JAM WIB**

**Fundamental Economic Global**
2-3 kalimat berita makro/geopolitik/Fed. Link sumber di-embed di kalimat pake format [teks](link). Wajib include Fear & Greed Index.

**Technical Market Analysis**
Harga $XXXX di bawah SMA20 ($XXXX) — bearish/uptrend.

```
Level                    Harga
Swing High 30d           $X,XXX
Fib 61.8%                $X,XXX
SMA20                    $X,XXX
Fib 78.6%                $X,XXX
Harga Saat Ini           $X,XXX
Swing Low 30d            $X,XXX
BB Lower                 $X,XXX
```

RSI XX.X — Bearish/Netral
Volume — Normal/Elevated

**Price Movement Analysis**
2-3 kalimat analisis pergerakan harga 6 jam terakhir. Astronacci wave analysis. Support/resistance terdekat.

**Waiting, Sell Area**
✷ ENTRY SELL : X,XXX - X,XXX
✷ TAKE PROFIT 1 : X,XXX
✷ TAKE PROFIT 2 : X,XXX
✷ TAKE PROFIT 3 : X,XXX
✷ TAKE PROFIT 4 : X,XXX
✷ STOP LOSS : X,XXX

**Waiting, Buy Area**
✧ ENTRY BUY : X,XXX - X,XXX
✧ TAKE PROFIT 1 : X,XXX
✧ TAKE PROFIT 2 : X,XXX
✧ TAKE PROFIT 3 : X,XXX
✧ TAKE PROFIT 4 : X,XXX
✧ STOP LOSS : X,XXX

**Mirroring Assistant Intraday**
1-2 kalimat bias, target harga, support/resistance.

**XAUUSD History Data**

```
XAUUSD, TANGGAL
✷ A1 : TP2 : 200 Pips
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

**Update sekarang JAM WIB :**
[update harga, jarak ke TP/SL]

### Labels History Data

- `TP4 : 1000 Pips` = TP1 sampe TP4 kena semua
- `TP3 : 500 Pips` = sampe TP3 kena
- `TP2 : 200 Pips` = sampe TP2 kena
- `TP1 : 100 Pips` = cuma TP1 kena
- `SL` = kena SL langsung
- `Running` = entry ke-hit, posisi jalan
- `Waiting Order` = entry belum kena

### RR Ratio (M15 Only)

- Entry range: 30 pips
- SL: 100 pips dari mid entry
- TP1: 100 pips (1:1)
- TP2: 200 pips (1:2)
- TP3: 500 pips (1:5)
- TP4: 1000 pips (1:10)
- Mid entry = (low + high) / 2

## SL Variations

- `Safe` : Belum kena SL
- `Okelah, TP1 Tadi` : TP1 Hit dulu, baru SL Hit
- `Tak Kena :p` : Semua TP Hit
- `Yah Maaf, Kena` : Langsung SL Hit

## Aturan Wajib

### Markdown Rules

- **SEMUA judul** dan **section title** pakai bold markdown `** **`
- **Tabel teknikal** dan **History Data** pakai code block ` ``` `
- **Fundamental** — link berita di-embed di kalimat pake `[teks](link)`
- **Waiting, Sell/Buy Area** — teks biasa, JANGAN di code block
- **Mirroring Assistant Intraday** — teks biasa

### Judul

- **XAUUSD - $HARGA Live Analyst1** (bold)
- **TANGGAL, JAM WIB** (bold baris bawah)
- Format tanggal: DD MONTH YYYY, 24JAM WIB
- Nomor analisa bertambah tiap kali: Analyst1, Analyst2, Analyst3, dst.

### Kapan Bikin Analisa Baru

- Analisa pertama hari ini = Analyst1 (lengkap fundamental + fib + tabel)
- Jangan bikin analisa baru sebelum entry kena TP2 atau SL (kecuali user minta)
- Entry yang masih running (TP3/TP4) jangan dihapus — masuk ke Mirroring Running Area

### Fundamental

- WAJIB ambil berita dari news scraper dulu
- 2-3 kalimat: inflasi, suku bunga, geopolitik, NFP/CPI/FOMC
- Link sumber di-embed di kalimat
- Wajib include Fear & Greed Index

### Entry Area

- Entry range: 30 pips
- SL 100 pips dari mid entry
- TP1 100 (1:1), TP2 200 (1:2), TP3 500 (1:5), TP4 1000 (1:10)
- Cari zone support/resistance terdekat dari harga

### History Data in Output

- Hanya tampilkan data hari ini doang
- Data hari sebelumnya hanya kalo user minta
- Waiting Order TETAP ditampilkan
- Kalo hanya ada Waiting Order, section History Data TETAP muncul

## Data Sources

- Gold spot: gold-api.com + fxratesapi
- Gold futures: Yahoo Finance GC=F
- Fear & Greed: alternative.me
- News: Google News RSS

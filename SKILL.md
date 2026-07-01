---
name: market-analysis-format-aes
description: Market analysis format standard by @mftrferdinand - Astronacci + Fibonacci + Fear & Greed, universal untuk XAUUSD/BTC/forex/index
---

# XAUUSD Market Analysis Format — AES

## 🔴 CRITICAL: Format Pal absolute — JANGAN NGACO

Format ini sudah melalui 20+ iterasi dan user MARAH BESAR tiap kali format salah. BACA INI DULU SEBELUM OUTPUT APA PUN:

1. **Bold `** **`** untuk: judul utama, semua section titles
2. **Code block ` ``` `** untuk: tabel teknikal, history data — bukan yang lain
3. **Teks biasa** untuk: Fundamental paragraf, Price Movement, Waiting Sell/Buy Area, Mirroring Assistant Intraday
4. **Link WAJIB di-embed** di teks Fundamental pake `[teks](link)` — jangan taruh link terpisah di akhir
5. **Fear & Greed WAJIB** tiap Fundamental dengan link alternative.me
6. **History Data TETAP muncul** walau cuma Waiting Order
7. Jangan pernah kirim output teks polos (tanpa bold / tanpa code block). User MARAH kalo itu terjadi
8. Jangan pernah kirim output yang kelebihan markdown (code block di entry area, dll)
9. Berlaku untuk SEMUA pair (XAUUSD, BTC, EURUSD, dll)

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

### Template Lengkap (XAUUSD) — Contoh Output PERSIS

**XAUUSD - $3,985 Live Analyst1**
**1 Juli 2026, 09:52 WIB**

**Fundamental Economic Global**
Gold turun ke $3,985 setelah gagal bertahan di atas $4,000. [The Fed hawkish](https://news.google.com/articles/...) masih jadi tekanan utama. [Fear Greed Index](https://alternative.me) 11 (Extreme Fear).

**Technical Market Analysis**
Harga $3,985 di bawah SMA20 ($4,221) dan Fib 78.6% ($4,097) — bearish.
```
Level                    Harga
Swing High 30d           $4,591
SMA20                    $4,221
Fib 78.6%                $4,097
Harga Saat Ini           $3,985
Swing Low 30d            $3,955
BB Lower                 $3,906
```
RSI 36.5 — Bearish
Volume — Normal

**Price Movement Analysis**
Harga turun dari $4,047 ke $3,985 — gagal bertahan di atas $4,000. Wave 3 turun Astronacci, saat ini menguji swing low intraday $3,983. Kalo tembus, target $3,955 (wave 5). Potensi bounce ke $4,030 kalo bertahan.

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
Bearish dominan. Harga di swing low $3,983 — kalo tembus, target $3,955. Sell bounce ke $4,030-4,033. Buy zona support $3,982-3,985 untuk scalping, SL ketat $3,973.

**XAUUSD History Data**
```
XAUUSD, 1 Juli 2026
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

## Skill Overlap

⚠️ `research/market-research` (SUPERSEDED) — jangan dipake. `research/market-analysis-format` ini yang bener.
⚠️ Old `market-ecosystem` skill — sudah dimerger ke sini. Jangan pake yang lama.

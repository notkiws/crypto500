# Top 500 Crypto — data harian

Situs statis (satu file `index.html`, tanpa server) berisi 500 coin teratas by market cap:

- harga penutupan mingguan 4 minggu terakhir + % per minggu
- harga penutupan harian 7 hari terakhir + % per hari
- rata-rata 7 hari + % vs harga pembukaan minggu
- harga hari ini vs 1 tahun lalu (dan %)
- harga hari ini vs harga hari launch (dan %)

Data: CoinGecko Free API (daftar top 500, harga live, market cap, sparkline 7 hari) + API publik
Binance / MEXC / Gate untuk candle harian asli dan harga hari listing pertama.

File di repo ini di-generate otomatis oleh job harian di VPS; `data.json` adalah payload yang
sama dengan yang dipakai halaman, dan `Top500_Crypto_latest.xlsx` versi Excel-nya.

Sel kosong ditandai `-`: coin tanpa pasangan USDT di Binance/MEXC/Gate, ticker yang bentrok
dengan aset lain (datanya dibuang, bukan dipakai), atau coin yang memang baru listing
sehingga harga 1 tahun lalu belum ada.

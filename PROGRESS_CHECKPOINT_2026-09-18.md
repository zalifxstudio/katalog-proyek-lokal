# Katalog Proyek Lokal — Checkpoint

Disimpan: 18 September 2026, WIB

## Tujuan

Memperbarui `index.html` dari snapshot 8 September dengan proyek dan produk baru yang benar-benar punya bukti source/paket, sekaligus memperbaiki entri yang path-nya sudah tidak valid karena folder sumbernya dipindah.

## Perbaikan bug

- 3 entri punya path lokal yang sudah tidak ada lagi karena folder aslinya dipindah ke bawah `D:\CODEX\kids-printable-product-library\`:
  - Junior Detective Case Files → `active-products\junior-detective-case-files` (kini menyebut 2 kasus: Case 01 & Case 02)
  - Big Sibling Mission Kit → `active-products\big-sibling-mission-kit`
  - Feelings Detective — A4 Prototype → `archived-prototypes\feelings-detective-a4-prototype`

## Selesai

- `index.html` diperbarui dari 119 menjadi **135 entri**: 38 game, 34 aplikasi, 8 web/PWA, 14 desktop, 41 produk aset.
- Ditambahkan 16 entri baru terkurasi (1 game, 2 desktop, 13 produk aset): Mosaic Quest, KecilBisa Calistung Reusable, Screen-Free Travel Busy Book 100, Halloween Cute Art Collection 120, Christmas Cute Art Collection 120, Guided Drawing & Coloring Worksheets 100, Kids Reward & Chore Charts 100, Affirmation Cards Self-Love & Confidence 100, Noura Waveform Studio, Feelings & Courage Activities Ages 4-7, ZXSTUDIO Original Glyph Icons 100, Nibblish Visual Routine Cards EN, Nibblish My Feelings Emotion Cards EN, Nibblish Playdough Learning Mats EN, Worksheet Edukasi 233 English Edition, Suno Auto-Mastering.
- ~30 folder kandidat lain yang ditemukan lewat audit (agregator/indeks, pilot <50% target, plan tanpa implementasi, batch mentah tanpa QC/packaging, tool internal, situs sudah live) SENGAJA tidak dimasukkan — lihat catatan investigasi sesi ini untuk daftar per-folder dan alasannya.
- Snapshot halaman diperbarui menjadi 18 September 2026; notice ditambah frasa "folder indeks/agregator" pada daftar yang disaring.

## Validasi tercatat

- Validasi JavaScript array `P`: 135/135 entri tepat enam string; jenis ∈ {Game, Aplikasi, Web, Desktop, Produk Aset} dan sumber ∈ {CODEX, Claude} semua sah; tidak ada nama duplikat.
- Semua 19 path lokal yang baru ditambahkan/diperbaiki diverifikasi ada di disk saat validasi (termasuk 2 path CODEX yang mengandung Unicode ✦).
- `git diff --check` lulus (hanya peringatan line-ending Git, sama seperti refresh sebelumnya).

## Status publikasi

- Menunggu commit + push ke `origin/main`, lalu verifikasi GitHub Pages `built` dan hash HTML publik cocok dengan lokal (ikuti proses yang sama seperti checkpoint 8 September).

## Langkah berikutnya

1. Pada refresh berikutnya, tinjau folder `poster-kamar-anak-imagegen` (poster kamar anak, 400/1000), `microstock-portfolio-2026`, dan sub-produk `AI_STOCK_AND_WALLPAPER_PRODUCTS`/`NIBBLISH-PRODUCT-PORTFOLIO\07-SCHOOL-READY-MORNING-ROUTINE-EN` bila sudah mencapai target dan dikemas — saat ini masih di bawah ambang bukti selesai.
2. Jalankan validasi array, path lokal, `git diff --check`, lalu publish hanya setelah persetujuan pengguna bila kebijakan berubah dari "commit+push langsung" untuk repo ini.

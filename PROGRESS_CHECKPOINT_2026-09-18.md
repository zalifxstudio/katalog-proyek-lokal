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

- `index.html` diperbarui dari 119 menjadi **136 entri**: 38 game, 34 aplikasi, 8 web/PWA, 15 desktop, 41 produk aset.
- Ditambahkan 16 entri dari rescan CODEX/Claude terkini (1 game, 2 desktop, 13 produk aset): Mosaic Quest, KecilBisa Calistung Reusable, Screen-Free Travel Busy Book 100, Halloween Cute Art Collection 120, Christmas Cute Art Collection 120, Guided Drawing & Coloring Worksheets 100, Kids Reward & Chore Charts 100, Affirmation Cards Self-Love & Confidence 100, Noura Waveform Studio, Feelings & Courage Activities Ages 4-7, ZXSTUDIO Original Glyph Icons 100, Nibblish Visual Routine Cards EN, Nibblish My Feelings Emotion Cards EN, Nibblish Playdough Learning Mats EN, Worksheet Edukasi 233 English Edition, Suno Auto-Mastering.
- Audit lanjutan terhadap 17 folder tanggal lama yang belum pernah ditinjau lintas 3 sesi refresh sebelumnya (`D:\CODEX\2026-04-24` s.d. `2026-07-17`, total ~40 subfolder): 1 produk baru ditemukan — **Redmi Fast Transfer** (desktop, source+test+EXE v1.2.0 lengkap di `2026-07-14\bu\work\RedmiFastTransfer`, pendekatan transfer via ADB manual — berbeda dari Phone File Organizer yang otomatis via MTP). Sisanya dikonfirmasi bukan produk baru: cache sesi Codex CLI (`chrome-profile`/`chrome-headless-profile`), duplikat/precursor konten yang sudah tercatat sebagai situs live yang dikecualikan (ruqyah-jodoh-guide, roadmap-120-hari, pulih-bersih, pola-33, qarun-komik, rabiah-komik, administrasi-guru-fasha, introvert-social-guide, shalat-syafii-web), snapshot build lama dari tool desktop yang sudah tercatat (PC Optimizer, Security Monitor rilis Mei), materi CSV pendukung PintarQuiz/ShalatKu, dan dua eksperimen kosong/scratch (`buat-aplikasi-flutter-untuk-tebak-gambar` kosong, `buat-aplikasi-yang-bisa-melihat-preview` demo Node.js tanpa produk).
- ~30 folder kandidat lain (dari rescan pertama sesi ini) yang berupa agregator/indeks, pilot <50% target, plan tanpa implementasi, batch mentah tanpa QC/packaging, tool internal, atau situs sudah live SENGAJA tidak dimasukkan.
- Snapshot halaman diperbarui menjadi 18 September 2026; notice ditambah frasa "folder indeks/agregator" pada daftar yang disaring.

## Validasi tercatat

- Validasi JavaScript array `P`: 136/136 entri tepat enam string; jenis ∈ {Game, Aplikasi, Web, Desktop, Produk Aset} dan sumber ∈ {CODEX, Claude} semua sah; tidak ada nama duplikat.
- Semua 20 path lokal yang ditambahkan/diperbaiki diverifikasi ada di disk saat validasi (termasuk 2 path CODEX yang mengandung Unicode ✦).
- `git diff --check` lulus (hanya peringatan line-ending Git, sama seperti refresh sebelumnya).

## Status publikasi

- Commit `06ff75d` (135 entri, fix 3 path) sudah dipush dan live — GitHub Pages `built`, hash SHA-256 publik = lokal, diverifikasi via curl.
- Commit kedua (136 entri, tambah Redmi Fast Transfer dari audit folder tanggal lama) menyusul di sesi yang sama — verifikasi ulang build+hash setelah push.

## Langkah berikutnya

1. Pada refresh berikutnya, tinjau folder `poster-kamar-anak-imagegen` (poster kamar anak, 400/1000), `microstock-portfolio-2026`, dan sub-produk `AI_STOCK_AND_WALLPAPER_PRODUCTS`/`NIBBLISH-PRODUCT-PORTFOLIO\07-SCHOOL-READY-MORNING-ROUTINE-EN` bila sudah mencapai target dan dikemas — saat ini masih di bawah ambang bukti selesai.
2. Folder tanggal lama sebelum 2026-04-24 (kalau ada) dan periode 2026-07-18 s.d. 2026-08-24 belum diaudit khusus di sesi ini (sebagian sudah tersentuh lewat entri yang sudah tercatat) — cek kalau mau benar-benar tuntas menyeluruh.
3. Jalankan validasi array, path lokal, `git diff --check`, lalu publish hanya setelah persetujuan pengguna bila kebijakan berubah dari "commit+push langsung" untuk repo ini.

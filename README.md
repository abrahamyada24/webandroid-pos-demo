# litepos.id — situs profil, langganan, dan download APK

Situs statis (HTML + CSS, tanpa build) untuk LitePOS.

## Halaman
`index.html` (profil) · `harga.html` · `download.html` · `kontak.html` · `syarat.html` · `privasi.html` · `refund.html`

Semua isian yang belum final ditandai `[ISI: ...]` (highlight kuning). Cari dengan `grep -rn "ISI" *.html`.
Halaman legal masih DRAFT dan sebaiknya ditinjau sebelum publish.

## Merilis APK
1. Taruh APK bertanda tangan di `downloads/`, mis. `downloads/litepos-1.0.0.apk`.
2. Hitung hash: `sha256sum downloads/litepos-1.0.0.apk`.
3. Salin `downloads/latest.json.example` menjadi `downloads/latest.json`, isi versi, tanggal, ukuran (byte), hash, dan path file.
Halaman Download otomatis membaca `latest.json`; tanpa file itu tombol tetap nonaktif.

## Langganan (belum dibangun)
Tombol di `harga.html` masih nonaktif. Rencana: backend kecil untuk membuat transaksi BorderPay,
menerima webhook, dan mengaktifkan lisensi. Gunakan mode Test dulu sampai KYC disetujui.

## Preview lokal
`python3 -m http.server 8000`

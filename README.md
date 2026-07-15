# QRIS Generator

Aplikasi pengubah **QRIS statis → QRIS dinamis** sesuai nominal — satu file, tanpa server. Berjalan sepenuhnya di perangkat (localStorage).

## Fitur
- **Unggah QRIS statis** (gambar) — otomatis dibaca dengan pemindai QR (jsQR), atau tempel kodenya.
- **Keypad nominal** → QRIS dinamis sesuai input: mode diubah ke sekali-pakai (tag 01→12), nominal disisipkan (tag 54), CRC dihitung ulang (CRC-16/CCITT) sesuai EMVCo/QRIS.
- **QR ditampilkan** untuk dipindai pembeli (GoPay, OVO, DANA, m-banking, dll).
- **Riwayat transaksi** tiap pembuatan nominal. **Hemat memori:** riwayat terhapus otomatis setelah **1 hari**.
- **Cetak PDF**: slip QRIS (nama toko + nominal + QR) dan laporan riwayat transaksi (jsPDF).
- **Nama toko/organisasi** tampil di layar & PDF.

## Menjalankan lokal
Cukup buka `index.html` di browser — tidak perlu build.

## Deploy (Cloudflare Pages)
Situs statis tanpa build:
- **Build command:** _(kosongkan)_
- **Build output directory:** `/` (root)

## Catatan
Data merchant asli pada QRIS tidak diubah — hanya mode, nominal, dan CRC. Nama toko bersifat label tampilan/PDF.

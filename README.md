# 🌤️ BMKG Weather Alert

Sistem monitoring cuaca BMKG dengan notifikasi WhatsApp dan web dashboard interaktif. Dibangun menggunakan Google Apps Script untuk kemudahan deployment dan maintenance.

## 🌟 Fitur Utama

- 🔍 Pencarian lokasi berdasarkan nama wilayah (Desa/Kelurahan/Kecamatan/Kabupaten/Kota)
- 📊 Tampilan dashboard responsif dengan data cuaca 3 hari ke depan
- 📱 Notifikasi WhatsApp otomatis untuk area yang dipilih
- 🕒 Update data setiap 3 jam (8 kali sehari)
- 📍 Mencakup seluruh wilayah administrasi Indonesia
- 📝 Pencatatan log pencarian dan pengiriman notifikasi

## 📋 Prasyarat

- Akun Google
- Spreadsheet untuk menyimpan data (template disediakan)
- Akun WhatsApp API (Mpedia)

## 🛠️ Instalasi

1. Buat project baru di Google Apps Script
2. Copy file `Code.gs` dan `Index.html` ke project
3. Siapkan spreadsheet dengan struktur yang diperlukan:
   - Sheet `wilayah`: Data kode dan nama wilayah
   - Sheet `cuaca`: Log pencarian
   - Sheet `log_kirimcuaca`: Log pengiriman WhatsApp
   - Sheet `kirim_cuaca`: Konfigurasi nomor tujuan
4. Update konfigurasi di `Code.gs`:
   - `SPREADSHEET_ID`
   - `WA_API_KEY`
   - `WA_SENDER`
5. Deploy sebagai web app

## 🌐 Penggunaan

### Web Dashboard
1. Akses URL web app yang telah di-deploy
2. Masukkan nama wilayah (minimal 3 karakter)
3. Pilih wilayah dari daftar yang muncul
4. Lihat informasi cuaca lengkap

### Notifikasi WhatsApp
1. Tambahkan data di sheet `kirim_cuaca`:
   - Kolom A: Kode wilayah
   - Kolom B: Nomor WhatsApp
2. Set up trigger untuk fungsi `scheduledWeatherNotification`
3. Notifikasi akan terkirim sesuai jadwal

## 📊 Format Data

### Data Cuaca
- Suhu Udara (°C)
- Kelembapan Udara (%)
- Kondisi Cuaca
- Kecepatan Angin (km/jam)
- Arah Angin
- Jarak Pandang (km)

## 🤝 Kontribusi

Contributions, issues, dan feature requests sangat diterima.

## 📝 Lisensi

[MIT](LICENSE)

## 🙏 Kredit

Data cuaca disediakan oleh [BMKG (Badan Meteorologi, Klimatologi, dan Geofisika)](https://www.bmkg.go.id/)

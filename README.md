# Absensi 8 Digital — Proyek Android

Proyek Android Studio yang membungkus file HTML Absensi 8 Digital menjadi aplikasi Android offline.

## Fitur
- Membuka aplikasi tanpa internet.
- Menyimpan data absensi di penyimpanan lokal WebView (`localStorage`).
- Rekap PDF disimpan ke folder Download pada Android 10 ke atas.
- Nama dan daftar siswa mengikuti file HTML sumber.

## Cara termudah membangun APK lewat GitHub Actions
1. Buat repository GitHub baru dan unggah semua isi folder proyek ini (bukan folder pembungkus di luarnya).
2. Buka tab **Actions** di repository. Jika diminta, aktifkan Actions.
3. Pilih workflow **Build Absensi 8 Digital APK**, lalu tekan **Run workflow**.
4. Setelah workflow selesai dengan status hijau, buka hasil run tersebut.
5. Di bagian **Artifacts**, unduh `Absensi8Digital-APK.zip` dan ekstrak untuk mendapatkan `app-debug.apk`.

Workflow otomatis sudah disertakan di `.github/workflows/build-apk.yml`.

## Cara membangun APK lewat Android Studio
1. Buka folder proyek ini di Android Studio.
2. Tunggu Gradle Sync selesai. Jika diminta, pasang Android SDK Platform 35.
3. Pilih **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
4. APK biasanya muncul di `app/build/outputs/apk/debug/app-debug.apk`.

## Catatan
- ZIP ini adalah proyek sumber; APK belum dikompilasi di lingkungan pembuatan file ini karena Android SDK/Gradle tidak tersedia dan akses internet untuk mengunduhnya diblokir.
- Data absensi disimpan di perangkat. Menghapus data aplikasi dapat menghapus data absensi.
- Untuk penggunaan permanen, lakukan backup data absensi secara berkala.

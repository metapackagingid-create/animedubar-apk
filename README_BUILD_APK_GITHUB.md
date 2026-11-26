# Animedubar Android APK — GitHub Actions Cloud Build (100% Gratis + OneSignal Aktif Penuh)

Paket ini berisi source code lengkap Aplikasi HP Pelanggan **Animedubar** (UI persis desain referensi Bstation + Fullscreen Netflix Cinema Player + Dual Subtitle + Sinkronisasi Apps Script v4) siap di-build otomatis menjadi file **`.apk`** di **GitHub Actions Cloud Build** tanpa perlu install Android Studio di laptop.

## Cara Build APK Otomatis (5 Menit, 100% Gratis)

1. **Buat Repositori GitHub Baru** (misalnya `animedubar-apk` di akun `metapackagingid-create`).
2. **Ekstrak ZIP ini**, lalu upload **seluruh isi foldernya** (termasuk folder tersembunyi `.github/workflows/build-apk.yml`, `www/`, `scripts/`, `package.json`, `capacitor.config.json`) ke root repositori tersebut.
3. **Masukkan Secrets (Agar OneSignal & Server Apps Script Aktif Otomatis di APK):**
   * Buka repositori GitHub -> **Settings** -> **Secrets and variables** -> **Actions** -> **New repository secret**:
     * `BACKEND_WEBAPP_URL` = URL Web App Google Apps Script Anda (`https://script.google.com/macros/s/.../exec`)
     * `ONESIGNAL_APP_ID` = App ID dari dashboard **OneSignal.com** (Gratis — pilih platform Android FCM)
4. **Jalankan Cloud Build:**
   * Buka tab **Actions** di repositori GitHub -> pilih workflow **Build Animedubar Android APK** -> klik **Run workflow**.
   * Tunggu ±3–4 menit hingga ikon centang hijau muncul.
5. **Download File `.apk`:**
   * Klik hasil build hijau tersebut -> gulir ke bawah ke bagian **Artifacts** -> klik **`Animedubar-App-Pelanggan-APK`** untuk mengunduh **`Animedubar-App-Pelanggan.apk`** lalu instal langsung di HP Android Anda!

## Catatan Pengaktifan OneSignal Android (FCM)
* Di dashboard OneSignal, hubungkan **Firebase Cloud Messaging (FCM)** gratis dengan Package Name: **`com.animedubar.app`**.
* Saat pengguna menginstal APK dan menekan **"Setuju dan Lanjutkan"**, plugin native `onesignal-cordova-plugin` otomatis meminta izin notifikasi Android & mendaftarkan perangkat ke OneSignal secara penuh!

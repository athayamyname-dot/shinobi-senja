# Shinobi Senja: proyek APK Android

Proyek ini membungkus game **Legenda Shinobi Senja** menjadi aplikasi Android. Game berjalan offline. Kalau HP tersambung internet, font judul ikut dimuat, tapi tanpa internet game tetap bisa dimainkan.

- Layar penuh, mode mendatar (landscape), dan layar tidak mati saat bermain
- Tombol **Back** Android: menjeda atau melanjutkan game, menutup menu, dan keluar dari layar judul
- Game otomatis dijeda saat aplikasi diminimalkan
- Progres tersimpan di HP
- Getar saat terkena serangan

## Cara 1: Rakit APK otomatis lewat GitHub (gratis, tanpa instal apa pun)

1. Buat akun di github.com, lalu buat repositori baru (misalnya `shinobi-senja`).
2. Pada halaman repositori, klik **Add file → Upload files**. Unggah **seluruh isi** folder ini (`app`, `build.gradle`, `settings.gradle`, `gradle.properties`, `README.md`), lalu klik **Commit changes**.
3. Folder `.github` kadang tidak ikut terunggah karena tersembunyi. Kalau begitu:
   - Buka tab **Actions → set up a workflow yourself**.
   - Beri nama file `build-apk.yml`.
   - Salin isi file `.github/workflows/build-apk.yml` dari folder ini ke editor, lalu klik **Commit**.
4. Buka tab **Actions**. Proses "Build APK" akan berjalan sekitar 3–6 menit. Kalau tidak berjalan sendiri, pilih "Build APK" lalu klik **Run workflow**.
5. Setelah muncul centang hijau, klik proses tersebut. Di bagian **Artifacts**, unduh **ShinobiSenja-APK**. File yang terunduh berupa .zip; ekstrak untuk mendapatkan `ShinobiSenja.apk`.

## Cara 2: Android Studio

Buka folder ini lewat **File → Open** di Android Studio, tunggu proses sinkronisasi selesai, lalu pilih **Build → Build APK(s)**.

## Memasang APK di HP

1. Kirim `ShinobiSenja.apk` ke HP (lewat WhatsApp ke diri sendiri, Google Drive, atau kabel USB).
2. Ketuk file tersebut. Kalau muncul peringatan, izinkan **"Instal aplikasi tidak dikenal"** untuk aplikasi yang membuka file (misalnya File Manager atau Chrome).
3. Ketuk **Instal**, lalu buka **Shinobi Senja**.

Peringatan dari Play Protect itu normal untuk aplikasi buatan sendiri yang tidak berasal dari Play Store. Pilih "Tetap instal".

## Catatan

- APK ini ditandatangani dengan kunci debug, cocok untuk dipakai sendiri atau dibagikan ke teman. Untuk diterbitkan di Google Play, kamu perlu membuat kunci rilis sendiri dan file AAB.
- Untuk memperbarui game, ganti file `app/src/main/assets/index.html` lalu naikkan `versionCode` di `app/build.gradle`.
- Minimal Android 7.0.

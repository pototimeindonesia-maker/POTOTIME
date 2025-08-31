
# POTOTIME Android WebView — GitHub Actions Build

Build APK **tanpa Android Studio**, langsung di GitHub Actions.

## Langkah cepat
1. Buat repo baru di GitHub (public/private bebas).
2. Upload seluruh isi folder ini (atau push via Git).
3. Buka tab **Actions** → Jalankan workflow **Android APK (CI)** (workflow_dispatch).
4. Tunggu selesai → ambil file **Artifacts** bernama `POTOTIME-app-debug` → di dalamnya ada `app-debug.apk`.

## Ubah URL awal
`app/src/main/java/id/buatmomen/pototime/MainActivity.kt`
```kotlin
private val HOME_URL = "https://buatmomen.id/user/login.php"
```

## Catatan
- Workflow ini memakai:
  - Java 17
  - Android SDK API 34 + build-tools 34.0.0
  - Gradle 8.7 (tanpa gradle wrapper)
- Kalau ingin **release APK/AAB** (signed), beri tahu aku—nanti kubuat workflow rilis + signing (bisa pakai GitHub Secrets).


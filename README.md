# Otak Flash AI (by Trav Team)

Cara build:
1. Buka folder ini di Android Studio (Hedgehog/Iguana atau lebih baru, JDK 17).
2. Tunggu Gradle Sync selesai.
3. Build > Build Bundle(s) / APK(s) > Build APK(s)
   atau jalankan: ./gradlew assembleDebug
   APK: app/build/outputs/apk/debug/app-debug.apk

Backend yang dibutuhkan:
- POST {server_url}/login   body {"username","password"} -> {"token": "..."}
- POST {server_url}/ask-ai  header Authorization: Bearer <token>
  body {"image": "<base64 jpeg>", "prompt": "..."} -> {"answer": "..."}
Default server_url: http://10.0.2.2:8080 (emulator -> localhost PC).

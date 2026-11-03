# frameX TV - Android TV Streaming App

Aplikasi Android TV yang ringan dan hemat memori untuk streaming film dan serial TV menggunakan embed provider [framextv.cc](https://framextv.cc/).

---

## ✨ Fitur Utama

- 🎮 **100% Remote D-Pad Navigation**: Navigasi intuitif untuk remote Android TV (Atas, Bawah, Kiri, Kanan, OK/Enter, Back).
- ⚡ **Ringan & Hemat RAM**:
  - Decode gambar dibatasi sesuai resolusi layar (`cacheWidth` 260px untuk poster, 640px untuk banner).
  - List kartu menggunakan dynamic recycling (`ListView.builder`) sehingga memori RAM tetap rendah (~60-80MB) bahkan di Android TV Box spek RAM 1–2 GB.
  - Video player berbasis WebView yang membersihkan memori secara instan saat kembali ke beranda.
- 🎬 **Integrasi frameXTV Embed**:
  - Movie Stream: `https://framextv.cc/embed/{tmdbId}?autoplay=1`
  - TV Series Stream: `https://framextv.cc/embed/{tmdbId}/{season}/{episode}?autoplay=1`
  - Multi-Provider Switcher: **Barbarian I**, **Archer II**, **Goblin III**, **P.E.K.K.A IV**, atau Auto.
- 🔍 **Katalog & Pencarian**:
  - Trending Hari Ini, Film Populer, Serial TV Populer, dan Rating Tertinggi.
  - Pencarian judul dengan keyboard virtual di layar yang ramah remote TV.
  - Pemilih Musim (Season) dan Episode serial TV.

---

## 📲 Cara Memasang APK ke Android TV

File APK hasil kompilasi berada di:
```text
build\app\outputs\flutter-apk\app-release.apk
```

### Opsi 1: Menggunakan Flashdisk (USB)
1. Salin file `app-release.apk` ke flashdisk / USB drive.
2. Colokkan flashdisk ke port USB di Android TV Anda.
3. Buka aplikasi File Manager di TV (misal: *FX File Explorer* atau *X-plore*).
4. Klik file `app-release.apk` dan pilih **Install**.

### Opsi 2: Menggunakan ADB Wireless (Tanpa Kabel)
1. Aktifkan **Developer Options** & **Wireless Debugging** di Android TV.
2. Dari terminal di PC ini, jalankan:
   ```powershell
   adb connect <IP_ANDROID_TV>:5555
   adb install -r build\app\outputs\flutter-apk\app-release.apk
   ```

### Opsi 3: Menggunakan Aplikasi "Send Files to TV"
1. Install aplikasi *Send Files to TV* di ponsel/PC dan di Android TV.
2. Kirim file APK langsung melalui jaringan WiFi lokal dan install.

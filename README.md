# 🏁 Speed GPS AIO — NotFound Workshop

<p align="center">
  <img src="https://img.shields.io/badge/Brand-NotFound%20Workshop-00e5ff?style=for-the-badge" alt="NotFound Workshop" />
  <img src="https://img.shields.io/badge/Product-Speed%20GPS%20AIO-ff2a6d?style=for-the-badge" alt="Speed GPS AIO" />
  <img src="https://img.shields.io/badge/Firmware-v1.0.1-05ffa1?style=for-the-badge" alt="v1.0.1" />
  <img src="https://img.shields.io/badge/Platform-ESP32-orange?style=for-the-badge" alt="ESP32" />
</p>

---

## 📖 Tentang Produk

**Speed GPS AIO** adalah instrumen speedometer digital cerdas berbasis GPS 10Hz dan ESP32 buatan **NotFound Workshop**. Didesain universal untuk segala jenis sepeda motor (bebek, matic, sport, 2-tak, maupun moge) dengan fitur komprehensif mulai dari pemantauan harian, fitur drag race profesional standar internasional (Dragy / RaceBox), hingga pembaruan firmware online langsung via **GitHub OTA**.

> [!NOTE]
> Repository ini adalah **Official Binary Release Hub** untuk firmware **Speed GPS AIO**. Seluruh file binary firmware resmi yang siap di-flash via OTA atau kabel USB dapat diunduh langsung di tab [Releases](../../releases).

---

## ⚡ Fitur Utama

- **🚀 10Hz Real-Time GPS Tracking**: Menggunakan modul Ublox M8N / NEO-6M dengan pembaruan kecepatan nyata (*true ground speed*) 10 kali per detik.
- **🖥️ 2.4" TFT ILI9341 8-Bit Parallel Display**: Tampilan tajam 320x240 piksel berkecepatan 60 FPS tanpa kedip (*smooth anti-flicker sprites*).
- **🏁 Drag Race Professional (1-Foot Rollout)**: Pengukuran presisi 0-60 km/h, 0-100 km/h, 201 Meter, dan 402 Meter dengan standar eliminasi *rollout* 1 kaki (30.48 cm) setara Dragy / RaceBox.
- **🌈 8-LED WS2812B NeoPixel Shift Light**: Dilengkapi variasi animasi pembuka (*startup animation*), shift light bertingkat, serta lampu hazard / sein terintegrasi.
- **🚦 Indikator Kendaraan Terisolasi**: Membaca saklar Netral `[ N ]` dan Lampu Sein `[ < ] [ > ]` dengan proteksi optocoupler dan logika polaritas yang dapat dibalik via software (*Active LOW / Active HIGH*).
- **🌐 Web Dashboard Interaktif (WiFi Hotspot `192.168.4.1`)**:
  - **Tab 1 (Balap & Grafik)**: Leaderboard catatan waktu balap dan grafik kurva telemetri interaktif (*touch scrubber*).
  - **Tab 2 (Pengaturan)**: Kustomisasi penuh skala RPM, speed, kecerahan LED, nama rider, running text, dan opsi rotasi layar.
  - **Tab 3 (Data & Servis)**: Unduh log CSV telemetri, reset jarak oli & v-belt, serta panel OTA update.
- **☁️ Cyberpunk OTA Version Picker (ala RaceBox 2.4)**:
  - Hubungkan ke Hotspot HP (`SSID: 404`, `Password: 11111111`).
  - Pilih versi firmware langsung di layar speedometer dengan navigasi sentuh.
  - Progress bar download Cyberpunk dengan animasi NeoPixel real-time.
  - Reboot bersih otomatis setelah update selesai.

---


## ☁️ Panduan Update Firmware Online (OTA)

1. Nyalakan **Personal Hotspot / Tethering di HP** Anda dengan konfigurasi:
   - **SSID:** `404`
   - **Password:** `11111111`
2. Pada spidometer, masuk ke layar **WIFI CONFIG** (tahan tombol sentuh di menu utama).
3. **Tap 1x**: Berpindah ke tab **`[ OTA UPDATE ]`**.
4. **Hold 2 Detik**: Spidometer akan otomatis menghubungkan ke hotspot `404` dan memuat daftar rilis firmware dari server.
5. **Pilih Versi Firmware**:
   - **Tap 1x**: Menggeser pilihan kartu rilis (misal `v1.0.1`, `v1.0.0`, dll).
   - **Hold 2 Detik**: Memulai download dan flashing firmware terpilih.
6. Tunggu hingga progress bar mencapai 100% dan indikator LED berwarna hijau. Spidometer akan me-reboot dirinya sendiri ke versi baru secara otomatis!

---

## 💾 Unduh Firmware Langsung (Direct Download)

File binary firmware dapat diunduh manual untuk flashing via USB cable (menggunakan ESP Flash Download Tool):

| Versi | Status | Aset Binary | Catatan Rilis |
| :--- | :--- | :--- | :--- |
| **v1.0.1** | **Latest (Recommended)** | [firmware.bin](../../releases/download/v1.0.1/firmware.bin) | Perbaikan driver LCD 8-Bit Parallel, UI OTA RaceBox 2.4, Clean Reboot |
| **v1.0.0** | Stable | [firmware.bin](../../releases/download/v1.0.0/firmware.bin) | Rilis awal |

---

## 📜 Riwayat Versi (Changelog)

- **v1.0.1 (Latest)**:
  - 🖥️ Perbaikan driver LCD ILI9341 8-Bit Parallel.
  - 🚀 Implementasi menu pilih firmware OTA interaktif ala RACEBOX 2.4 (kartu versi, badge LATEST/CURRENT/ROLLBACK).
  - 🔄 Mekanisme clean shutdown sebelum reboot untuk mencegah hang/freeze.
  - 🌐 Opsi rotasi layar landscape dan sinkronisasi Hotspot target.
- **v1.0.0**:
  - Rilis awal Speed GPS AIO Basic.

---

<p align="center">
  <b>NotFound Workshop &copy; 2026. All Rights Reserved.</b><br/>
  <i>Engineered for Racers & Motorcycle Enthusiasts.</i>
</p>


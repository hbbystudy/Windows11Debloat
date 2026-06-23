"""# Windows11Debloat - Kustomisasi Autounattend.xml & Debloat Script

Repositori ini berisi panduan, catatan konfigurasi, dan skrip optimasi untuk instalasi bersih (Clean Install) Windows 11 64-bit yang telah di-debloat dan disesuaikan khusus untuk perangkat **MSI**. Konfigurasi ini dirancang agar sistem berjalan lebih ringan, responsif, menjaga privasi, namun tetap mempertahankan fungsionalitas esensial (seperti Microsoft Store untuk bermain Minecraft).

---

## 🛠️ Ringkasan Konfigurasi Utama

### ⌨️ Wilayah & Input Keyboard
* **EN us** (English - United States)
* **JP jp** (Japanese - Japan)

### 🔑 Lisensi & Aktivasi
* **Menggunakan Product Key yang tersimpan di BIOS/UEFI Firmware**
    * *Catatan:* Opsi ini diaktifkan khusus jika laptop kamu memiliki lisensi Windows bawaan resmi dari brand (MSI) agar aktivasi berjalan otomatis setelah instalasi selesai.

### 🌐 Pengaturan Setup (Windows PE & OOBE)
* **Windows PE Stage:** Default
* **Computer Name:** `MSI` (Nama default laptop)
* **Time Zone:** Otomatis mendeteksi wilayah.
* **WLAN / Wi-Fi Setup:** **OFF** saat setup awal.
* **Internet Bypass:** Diizinkan menginstal Windows 11 tanpa koneksi internet (*Allow Windows 11 to be installed without internet connection*). Kamu perlu menekan tombol *"I don't have internet"* jika setup meminta koneksi.
* **Akun Pengguna:** Menggunakan opsi interaktif untuk menambahkan akun lokal terlebih dahulu, yang nantinya ditujukan untuk masuk menggunakan **Akun Microsoft** (*diperlukan untuk sinkronisasi Minecraft*).

---

## 🔒 Privasi & Keamanan (Express Settings)
* **Express Settings:** **DISABLE ALL** (Semua pelacakan dimatikan). Windows tidak akan mengirim data diagnostik, personalisasi input, maupun riwayat lokasi ke Microsoft untuk menjaga privasi maksimal.
* **Sticky Keys:** **OFF** (Dimatikan agar tidak mengganggu saat bermain game).

---

## 🚀 Tweak Sistem & Performa

* **Disable Smart App Control** (Mencegah pemblokiran aplikasi pihak ketiga yang aman).
* **Enable Long Paths** (Mendukung jalur folder yang panjang lebih dari 260 karakter).
* **Allow PowerShell Script Execution** (Mengizinkan eksekusi skrip PowerShell untuk mempermudah debloat lanjut).
* **Do not update Last Access Time stamp** (Meningkatkan performa berkas/I-O pada SSD).
* **Prevent Device Encryption** (Mencegah enkripsi BitLocker otomatis pada drive).
* **Hide Edge First Run Experience** (Mematikan pop-up selamat datang Microsoft Edge yang mengganggu).
* **Disable Edge Startup Boost & Background Mode** (Menghentikan Edge berjalan di latar belakang secara diam-diam).
* **Delete Empty `C:\\Windows.old` Folder** (Otomatis membersihkan folder sisa instalasi lama).
* **Disable Automatic Sign-on of last user after a restart** (Keamanan ekstra setelah perangkat di-restart).

---

## 🎨 Antarmuka & Efek Visual
Konfigurasi visual ini disesuaikan secara khusus untuk menjaga kenyamanan mata dan estetika, tanpa membebani performa sistem:
* Menampilkan thumbnail, bukan ikon (*Show thumbnails instead of icons*).
* Menampilkan konten jendela saat digeser (*Show window contents while dragging*).
* Menghaluskan tepi font layar (*Smooth edges of screen fonts*).
* Mengaktifkan fitur **Peek**.
* Menyimpan pratinjau thumbnail taskbar (*Save taskbar thumbnail previews*).
* Menggunakan bayangan untuk label ikon di desktop (*Use drop shadows for icon labels on the desktop*).
* Menampilkan persegi panjang seleksi transparan (*Show translucent selection rectangle*).

---

## 🖥️ Menu Mulai, Taskbar & Ikon Desktop

### Start Menu & Taskbar
* **Hidden Widgets** (Mematikan/menyembunyikan Widget).
* **No Bing Results** (Mematikan pencarian Bing di dalam Start Menu atau Search Box).
* **Folders on Start:** Default.
* **Password Expiration:** Default (None / Tidak pernah kedaluwarsa).

### Ikon Desktop & Pintasan
* ❌ **Hapus pintasan Microsoft Edge** di Desktop.
* ✔️ Menampilkan **Control Panel** di Desktop.
* ✔️ Menampilkan **This PC** di Desktop.

---

## 📦 Daftar Aplikasi Bawaan (Bloatware yang Dipertahankan)
Hanya menyisakan aplikasi esensial untuk kebutuhan dasar dan produktivitas harian:
* 📷 **Camera**
* 📝 **Notepad (Modern)**
* ✂️ **Snipping Tool**
* 🎨 **Paint**
* 🖼️ **Photos**
* 📌 **Sticky Notes**
* 🎵 **Windows Media Player (Modern)**
* 🎮 **Xbox Apps** (Penting untuk ekosistem gaming/Minecraft)
* ⏰ **Clock**
* 🧮 **Calculator**
* 🛍️ **Microsoft Store** (Wajib untuk mengunduh Minecraft & Launcher)
* 📱 **Your Phone / Phone Link**
* 💻 **Windows Terminal**

---

## ⚡ Skrip Tambahan: Chris Titus Tech (CTT) Tools
Untuk debloat dan optimasi pasca-instalasi yang lebih mendalam, gunakan **Chris Titus Tech Windows Utility**. 

### Cara Menjalankan CTT Tool:
1. Buka **Windows Terminal** atau **PowerShell** sebagai Administrator.
2. Salin dan tempel perintah berikut, lalu tekan `Enter`:

```powershell
iwr -useb [https://christitus.com/win](https://christitus.com/win) | iex
```

### Saya Tidak Bertanggung jawab kalau anda menggunakan file 
* `autounattend.xml`

* KARENA INI UNTUK PENGGUNAKAN PRIBADI JADI JIKA INGIN CUSTOM `autounattend.xml` SILAHKAN KE LINK DI BAWAH INI
* ```txt
  https://schneegans.de/windows/unattend-generator/
  ```

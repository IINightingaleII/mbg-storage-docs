# Buku Panduan Merakit & Memasang Aplikasi (Untuk Pemula)

Halo! Jika Anda bukan orang teknis atau staf IT, tidak perlu khawatir. Panduan ini dibuat selangkah demi selangkah, sangat pelan, dan menggunakan bahasa sehari-hari. 

Anggap saja kita sedang merakit perabotan baru; kita harus menyiapkan "obeng" dan "palu" nya terlebih dahulu sebelum perabotannya bisa dipakai.

---

## 🛠️ TAHAP 1: Menyiapkan "Alat Perkakas" Wajib
Agar aplikasi gudang ini bisa hidup, komputer atau laptop Anda membutuhkan dua program gratis. Kita akan mendownload dan memasangnya sekarang.

### A. Memasang Python (Sebagai Mesin Pengolah Data)
1. Buka internet (Google Chrome atau Mozilla).
2. Ketik dan kunjungi alamat web ini: 👉 **[python.org/downloads](https://www.python.org/downloads/)**
3. Klik tombol besar berwarna kuning bertuliskan **Download Python**.
4. Setelah file berhasil didownload, klik dua kali file tersebut untuk membukanya.
5. ⚠️ **SANGAT PENTING (JANGAN TERLEWAT):** Saat layar instalasi pertama kali muncul, perhatikan bagian paling bawah layar. Akan ada kotak centang kecil bertuliskan **"Add Python to PATH"** atau **"Add python.exe to PATH"**. **Kotak ini WAJIB DICENTANG!** *(Jika tidak dicentang, komputer tidak akan mengenali mesin ini nantinya).*
6. Setelah dipastikan sudah dicentang, baru klik tulisan **Install Now** di bagian tengah.
7. Biarkan proses berjalan hingga muncul tulisan *Setup was successful*. Klik tombol **Close**.

### B. Memasang Node.js (Sebagai Pembuat Tampilan Web)
1. Buka internet lagi dan kunjungi alamat ini: 👉 **[nodejs.org](https://nodejs.org/)**
2. Anda akan melihat dua tombol hijau besar. Pilih dan klik tombol hijau yang ada tulisan **LTS (Recommended For Most Users)**.
3. Setelah file didownload, buka file tersebut.
4. Cara pasangnya sangat mudah. Cukup klik **Next**, centang tulisan *I accept the terms*, klik **Next** lagi, lalu klik **Install**.
5. Tunggu prosesnya selesai, lalu klik **Finish**. 

*Selesai! Alat perkakas Anda sudah terpasang semua di komputer.*

---

## 📂 TAHAP 2: Mendownload Isi Aplikasi Kita
Sekarang saatnya kita merakit isi aplikasi gudang ini. Kita akan menggunakan layar hitam yang biasa disebut CMD (Command Prompt). Layarnya memang terlihat seperti layar hacker di film, tapi tenang saja, kita hanya butuh mengetik kalimat pendek!

1. Buka folder tempat Anda menyimpan file aplikasi **MBG Storage** ini.
2. Di bagian paling atas folder tersebut (bagian memanjang yang menunjukkan lokasi folder, misal: *C:\Users\NamaAnda\Documents\MBG*), klik satu kali bagian kosong di kotak putih tersebut.
3. Hapus tulisan lokasinya, lalu ketik huruf: `cmd`
4. Tekan tombol **Enter** di keyboard. Layar hitam akan otomatis terbuka!

**Sekarang, ikuti ketikan ini di layar hitam tersebut:**

### Langkah Merakit Tampilan Depan (Layar Pertama)
Di layar hitam yang baru saja terbuka, ketik kalimat ini pelan-pelan lalu tekan Enter:
> `npm install`

*(Komputer akan otomatis mendownload gambar-gambar dan tombol untuk aplikasi Anda. Proses ini butuh koneksi internet dan bisa memakan waktu 1-3 menit. Biarkan saja sampai berhenti).*

### Langkah Merakit Mesin Belakang (Layar Kedua)
Buka satu layar hitam (CMD) lagi dari folder Anda (seperti cara nomor 2, 3, 4 di atas). Di layar hitam yang KEDUA ini, ketik perintah berikut satu per satu (tekan Enter setelah mengetik satu baris):

1. Masuk ke folder mesin:
   > `cd backend`
2. Bikin ruangan khusus untuk mesinnya:
   > `python -m venv venv`
3. Hidupkan ruangan khususnya:
   > `.\venv\Scripts\activate.bat`
4. Download buku panduan mesinnya dari internet:
   > `pip install -r requirements.txt`

*(Tunggu lagi 1-3 menit sampai semua proses download persenannya mencapai 100% dan berhenti).*

🎉 **SELAMAT! APLIKASI ANDA SUDAH SELESAI DIRAKIT DAN SIAP DINYALAKAN KAPAN SAJA!**

---

## 🚀 TAHAP 3: Cara Menyalakan Aplikasi (Rutinitas Sehari-hari)
Langkah di Tahap 1 dan Tahap 2 di atas **cukup Anda lakukan satu kali seumur hidup** saat pertama kali memasang aplikasi.

Untuk hari-hari berikutnya, jika Anda baru menyalakan komputer dan mau membuka aplikasi kasir/gudang ini, Anda HANYA PERLU melakukan langkah di bawah ini:

### 1. Nyalakan Mesin Data (Biarkan CMD Pertama Terbuka)
Buka CMD di folder aplikasi Anda, lalu ketik berurutan:
> `cd backend`
> `.\venv\Scripts\activate.bat`
> `python -m uvicorn app.main:app --reload --port 8000`

### 2. Nyalakan Tampilan (Biarkan CMD Kedua Terbuka)
Buka satu CMD lagi di folder aplikasi Anda, lalu ketik:
> `npm run dev`

### 3. Buka Web Anda!
Biarkan kedua layar hitam (CMD) tersebut tetap terbuka, jangan ditutup (Anda bisa menyembunyikan/minimize saja ke bawah). 
Buka Google Chrome Anda, lalu ketik alamat ini di tempat Anda biasa mengetik www.google.com:
👉 **localhost:3000**

Aplikasi Anda akan muncul! Untuk masuk, gunakan kata sandi ini:
- **Kepala Gudang**: Username `admin` / Password `password123`
- **Staf Dapur**: Username `dapur` / Password `password123`

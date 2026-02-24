# 🛒 Mini E-Commerce App: Solusi Belanja Pintar

![Flutter](https://img.shields.io/badge/Flutter-%2302569B.svg?style=for-the-badge&logo=Flutter&logoColor=white)
![Dart](https://img.shields.io/badge/dart-%230175C2.svg?style=for-the-badge&logo=dart&logoColor=white)
![Provider](https://img.shields.io/badge/Provider-State_Management-blueviolet?style=for-the-badge)

## Deskripsi Aplikasi

**Mini E-Commerce App** adalah solusi digital interaktif yang dirancang untuk mensimulasikan pengalaman berbelanja modern. Fokus utama dari proyek aplikasi ini adalah mendemonstrasikan manajemen *state* yang kompleks menggunakan `Provider`, memungkinkan sinkronisasi data secara *real-time* antara katalog produk, fitur pencarian, dan keranjang belanja tanpa kendala performa.

---

## Fitur Utama & Fungsionalitas

Aplikasi ini telah mendukung alur belanja yang lengkap dengan detail sebagai berikut:

### 1. Katalog & Pencarian Pintar (Read & Filter)
Aplikasi menyajikan daftar produk secara dinamis di dalam Grid. Pengguna dapat mencari produk berdasarkan nama menggunakan *Search Bar* atau menyaring produk berdasarkan kategori menggunakan *Choice Chips* yang reaktif.

### 2. Manajemen Keranjang (Create & Update)
Pengguna dapat menambahkan produk ke dalam keranjang belanja dari halaman utama. Di dalam keranjang, pengguna memiliki kendali penuh untuk menambah (`+`) atau mengurangi (`-`) kuantitas setiap barang.

### 3. Keamanan Hapus & Notifikasi (Delete)
Setiap perubahan pada keranjang memberikan umpan balik langsung (*SnackBar*). Pengguna juga dapat menghapus item dari keranjang atau mengosongkan keranjang sepenuhnya dengan konfirmasi lapisan keamanan menggunakan `AlertDialog`.

### 4. Sistem Checkout & Validasi (Checkout)
Aplikasi menyediakan halaman penyelesaian pesanan (Checkout) yang menampilkan ringkasan belanja beserta total harga. Terdapat form pengiriman yang dilindungi oleh sistem validasi, memastikan pesanan tidak dapat diproses jika data pengguna kosong.

---

## 🛠️ Widget & Teknologi Teknis

Dalam pengembangan aplikasi ini, beberapa arsitektur dan widget inti Flutter digunakan untuk mendukung performa maksimal:

- **`Provider` (`ChangeNotifier`, `Consumer`)** : Jantung dari aplikasi ini. Digunakan untuk mengelola *state* keranjang belanja dan filter pencarian secara global tanpa terjebak dalam *prop drilling*.
- **`GridView.builder`** : Merender katalog produk dalam format grid dua kolom secara *lazy-loading* sehingga ramah memori.
- **`ChoiceChip`** : Menyediakan elemen antarmuka (UI) interaktif untuk melakukan filter kategori produk dengan indikator visual saat dipilih.
- **`Form` & `TextFormField`** : Menangani input data pengguna di halaman checkout lengkap dengan validasi form otomatis.

---

## Dokumentasi Program (Alur Aplikasi)

Berikut adalah penjelasan alur antarmuka (UI) saat menggunakan aplikasi ini:

* **Halaman Utama (Katalog Produk)**
  Ini adalah menu utama (Home) dari aplikasi. Pengguna akan melihat kolom pencarian, deretan kategori produk, dan grid katalog. Saat item ditambahkan dengan menekan tombol **Tambah**, indikator angka (badge) merah pada logo keranjang di pojok kanan atas akan otomatis bertambah.
    
* **Halaman Keranjang (Cart)**
  Setelah menekan ikon keranjang, pengguna akan masuk ke rincian pesanan. Di sini, sistem secara otomatis mengkalkulasi total harga berdasarkan harga produk dikali kuantitas. Jika keranjang kosong, layar akan menampilkan pesan *"Keranjang Anda kosong"*. Terdapat tombol **Checkout** di bagian bawah layar.

* **Halaman Checkout**
  Di halaman ini, pengguna melihat ringkasan pesanan akhir. Pengguna diwajibkan mengisi `Nama Lengkap` dan `Alamat Pengiriman`. Jika form disubmit dalam keadaan kosong, peringatan warna merah akan muncul. Jika data valid, *Pop-up Dialog* pesanan berhasil akan muncul dan keranjang akan dikosongkan secara otomatis.

---

## Dokumentasi Program (Langkah Penggunaan)

Berikut adalah panduan langkah demi langkah (*user journey*) dalam menggunakan aplikasi Mini E-Commerce:

1. **Halaman Utama (Home Page) & Pencarian**
Saat membuka aplikasi, jelajahi produk menggunakan kolom pencarian atau filter kategori. Klik "Tambah" pada *card* produk untuk memasukannya ke keranjang.

<div align="center">
    <img width="250" height="500" alt="Halaman Utama" src="https://placehold.co/250x500/e2e8f0/475569?text=Halaman+Utama\nKatalog" />
    <img width="250" height="500" alt="Filter Kategori" src="https://placehold.co/250x500/e2e8f0/475569?text=Fitur+Pencarian\n& Filter" />
</div>

<br>

2. **Mengelola Keranjang Belanja**
Klik ikon keranjang di pojok kanan atas. Anda dapat menambah atau mengurangi jumlah item menggunakan tombol `+` dan `-`, atau menghapusnya sama sekali menggunakan ikon tong sampah merah.

<div align="center">
    <img width="250" height="500" alt="Keranjang Belanja" src="https://placehold.co/250x500/e2e8f0/475569?text=Halaman\nKeranjang" />
</div>

<br>

3. **Proses Checkout & Validasi**
Klik tombol "Checkout" untuk masuk ke halaman pengiriman. Isi form yang tersedia. Jika ada kolom yang terlewat, sistem akan memberikan peringatan keamanan.

<div align="center">
    <img width="250" height="500" alt="Form Checkout" src="https://placehold.co/250x500/e2e8f0/475569?text=Halaman\nCheckout" />
    <img width="250" height="500" alt="Validasi Form" src="https://placehold.co/250x500/e2e8f0/475569?text=Peringatan\nValidasi" />
</div>

<br>

4. **Konfirmasi Pesanan**
Setelah form diisi dengan benar dan tombol "Konfirmasi Pesanan" ditekan, *Pop-up* sukses akan muncul. Menekan tombol "Kembali ke Beranda" akan membawa Anda kembali ke halaman awal dengan keranjang yang sudah direset.

<div align="center">
    <img width="250" height="500" alt="Pesanan Sukses" src="https://placehold.co/250x500/e2e8f0/475569?text=Pop-up\nPesanan+Berhasil" />
</div>

---
*Dikembangkan oleh Faris - Mahasiswa Sistem Informasi, Fakultas Teknik, Universitas Mulawarman.*

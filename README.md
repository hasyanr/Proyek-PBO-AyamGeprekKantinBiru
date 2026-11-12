# SmartTrade-In

### Aplikasi Desktop Jual Beli dan Tukar Tambah Barang Elektronik Bekas

## Deskripsi Proyek

**SmartTrade-In** merupakan aplikasi desktop berbasis Java yang dirancang untuk memfasilitasi proses jual beli dan tukar tambah barang elektronik bekas, seperti smartphone, laptop, dan tablet.

Aplikasi ini membantu penjual menentukan harga barang berdasarkan kondisi perangkat serta memudahkan pembeli mencari dan membeli barang elektronik bekas dengan informasi harga dan kondisi yang lebih transparan.

## Tujuan Proyek

1. Mempermudah proses jual beli barang elektronik bekas.
2. Memberikan estimasi harga berdasarkan skor kondisi barang.
3. Menyediakan katalog barang yang terorganisasi dan mudah dicari.
4. Menerapkan konsep Pemrograman Berorientasi Objek menggunakan Java.

## Teknologi yang Digunakan

| Komponen | Teknologi |
|---|---|
| Bahasa Pemrograman | Java |
| GUI | Java Swing (JFrame Form) |
| Database | MySQL |
| Koneksi Database | JDBC |
| IDE | NetBeans |
| Pemodelan | UML Class Diagram |

## Fitur Utama

- Login dan registrasi pengguna.
- CRUD data barang (Create, Read, Update, Delete).
- Penilaian kondisi barang dengan skor 1–100.
- Penentuan grade kondisi A, B, atau C.
- Perhitungan estimasi harga otomatis.
- Katalog barang elektronik.
- Pencarian dan pengurutan barang.
- Transaksi pembelian.
- Pembaruan status barang setelah pembelian.

## Jenis Barang

SmartTrade-In mendukung tiga jenis barang elektronik:

1. Smartphone
2. Laptop
3. Tablet

## Database

Aplikasi menggunakan database MySQL dengan lima tabel utama:

| Nama Tabel | Fungsi |
|---|---|
| `customers` | Menyimpan data pengguna |
| `barang` | Menyimpan data barang elektronik |
| `penilaian` | Menyimpan skor, grade, dan estimasi harga |
| `transaksi` | Menyimpan data transaksi |
| `detail_transaksi` | Menyimpan rincian barang yang dibeli |

### Relasi Database

- Satu customer dapat melakukan banyak transaksi (One-to-Many).
- Satu transaksi dapat memiliki beberapa detail barang (One-to-Many).
- Satu barang memiliki satu data penilaian (One-to-One).

## Struktur Package Proyek

```text
SmartTrade-In/
│
└── Source Packages/
    │
    └── smarttrade.in/
        │
        ├── SmartTradeIn.java
        │
        ├── smarttrade.in.contract/
        │
        ├── smarttrade.in.database/
        │
        ├── smarttrade.in.exception/
        │
        ├── smarttrade.in.main/
        │
        ├── smarttrade.in.repository/
        │
        ├── smarttrade.in.service/
        │
        └── smarttrade.in.view/
```

### Penjelasan Package

| Package | Fungsi |
|---|---|
| `smarttrade.in` | Package utama proyek yang berisi SmartTradeIn.java |
| `smarttrade.in.contract` | Menyimpan interface aplikasi |
| `smarttrade.in.database` | Mengatur koneksi database MySQL menggunakan JDBC |
| `smarttrade.in.exception` | Menyimpan custom exception untuk menangani kesalahan |
| `smarttrade.in.main` | Menjadi bagian utama untuk menjalankan aplikasi |
| `smarttrade.in.repository` | Mengelola operasi penyimpanan dan pengambilan data |
| `smarttrade.in.service` | Mengelola proses bisnis dan logika aplikasi |
| `smarttrade.in.view` | Menyimpan tampilan GUI menggunakan Java Swing |

## Penerapan Konsep Pemrograman Berorientasi Objek

| Konsep PBO | Implementasi |
|---|---|
| Class dan Object | BarangElektronik, Customer, Transaksi |
| Constructor | Pembuatan objek barang dan customer |
| Encapsulation | Atribut private, getter, dan setter |
| Inheritance | Smartphone, Laptop, dan Tablet mewarisi BarangElektronik |
| Overriding | Perhitungan harga trade-in berbeda untuk setiap jenis barang |
| Overloading | Method `cariBarang()` dengan parameter berbeda |
| Abstract Class | BarangElektronik |
| Interface | DapatDinilai dan DapatDijual |
| Polymorphism | Berbagai jenis barang diproses menggunakan referensi BarangElektronik |
| Exception Handling | Custom exception dan try-catch |
| JDBC | Koneksi dan pengelolaan database MySQL |

## Exception Handling

Aplikasi dirancang untuk menangani beberapa kondisi kesalahan:

- Skor kondisi barang di luar rentang 1–100.
- Harga barang tidak valid.
- Barang yang ingin dibeli tidak ditemukan.
- Stok barang sudah habis.
- Input pengguna bukan angka.
- Email pengguna sudah terdaftar.

Custom exception:

- `BarangTidakDitemukanException`
- `StokTidakCukupException`
- `EmailSudahTerdaftarException`

## Alur Kerja Aplikasi

1. Pengguna melakukan registrasi atau login.
2. Penjual memasukkan informasi barang elektronik.
3. Sistem melakukan penilaian kondisi barang.
4. Sistem menentukan skor, grade, dan estimasi harga.
5. Barang disimpan ke database dan ditampilkan dalam katalog.
6. Pembeli mencari dan memilih barang.
7. Pembeli melakukan transaksi pembelian.
8. Sistem mencatat transaksi dan memperbarui status barang.

## Pembagian Tugas

### Anggota 1

- Membuat database MySQL dan koneksi JDBC.
- Membuat class model barang.
- Membuat interface DapatDinilai dan DapatDijual.
- Membuat PenilaianService.
- Membuat repository.
- Membuat custom exception.
- Mengimplementasikan overloading dan validasi data.
- Melakukan pengujian backend dan menyusun laporan.

### Anggota 2

- Membuat class Customer, Transaksi, DetailTransaksi, dan Penilaian.
- Membuat BarangService dan TransaksiService.
- Membuat LoginFrame dan MainFrame.
- Membuat KatalogFrame.
- Membuat PenjualFrame.
- Membuat TransaksiFrame.
- Mengintegrasikan GUI dengan service dan repository.
- Melakukan pengujian GUI dan mempersiapkan presentasi.

## Mata Kuliah

**Pemrograman Berorientasi Objek (PBO)**

Proyek SmartTrade-In dibuat sebagai implementasi konsep Pemrograman Berorientasi Objek menggunakan bahasa Java, database MySQL, JDBC, dan antarmuka Java Swing.

## Identitas
- Nama  : Ismi Zakia
- NPM   : 2210010020
- Kelas : 5B Non Reguler Banjarmasin
# Penghitung Umur

**Penghitung Umur** adalah aplikasi berbasis GUI (Graphical User Interface) yang menghitung umur berdasarkan tanggal lahir yang dimasukkan oleh pengguna. Aplikasi ini dibangun menggunakan **Java Swing** dan menggunakan komponen **JDateChooser** dari pustaka *toedter.calendar*.

## Fitur

- Memilih tanggal lahir menggunakan kalender (JDateChooser).
- Menampilkan hasil umur dalam format:
  - **Tahun**
  - **Bulan**
  - **Hari**
- Validasi input untuk memastikan pengguna memilih tanggal sebelum perhitungan dilakukan.

## Prasyarat

- **Java Development Kit (JDK)** versi 8 atau lebih baru.
- Pustaka eksternal **JCalendar** (toedter.calendar):
  - Unduh dari [https://toedter.com/jcalendar/](https://toedter.com/jcalendar/).
  - Tambahkan ke proyek Anda sebagai pustaka eksternal.

## Cara Menjalankan

1. **Kloning atau unduh proyek ini.**
2. **Tambahkan pustaka JCalendar** ke proyek Anda:
   - Di NetBeans:
     - Klik kanan pada proyek → **Properties** → **Libraries** → **Add JAR/Folder**.
     - Pilih file JAR dari pustaka JCalendar.
3. **Kompilasi dan jalankan program**:
   - Di NetBeans: Klik kanan pada file utama → **Run File**.
   - Di terminal:
     ```bash
     javac -cp .;path/to/jcalendar.jar PenghitungUmurFrame.java
     java -cp .;path/to/jcalendar.jar PenghitungUmurFrame
     ```

## Penjelasan Kode

### Komponen Utama
1. **JFrame**:
   - Digunakan sebagai jendela utama aplikasi.

2. **JDateChooser**:
   - Komponen untuk memilih tanggal lahir.

3. **JTextField**:
   - Menampilkan hasil umur dalam tahun, bulan, dan hari. Tidak dapat diedit secara manual oleh pengguna.

4. **JButton**:
   - `Hitung`: Untuk menghitung umur berdasarkan tanggal lahir.
   - Menampilkan pesan kesalahan jika tanggal belum dipilih.

5. **Period (java.time)**:
   - Digunakan untuk menghitung selisih waktu antara tanggal lahir dan tanggal saat ini.

### Validasi
- Memastikan pengguna memilih tanggal sebelum melakukan perhitungan.
- Menampilkan pesan kesalahan menggunakan **JOptionPane** jika tidak ada tanggal yang dipilih.

## Contoh Penggunaan

1. Jalankan aplikasi.
2. Pilih tanggal lahir Anda melalui komponen kalender.
3. Klik tombol **Hitung** untuk melihat hasil umur Anda.
4. Umur akan ditampilkan dalam format:
   - **Tahun**
   - **Bulan**
   - **Hari**

## Struktur Kode
- `main`: Titik masuk program.
- `PenghitungUmurFrame`: Kelas utama yang berisi logika perhitungan umur dan pengaturan GUI.
- Komponen utama:
  - `JDateChooser`: Untuk memilih tanggal.
  - `JTextField`: Untuk menampilkan hasil.
  - `JButton`: Untuk memproses perhitungan.

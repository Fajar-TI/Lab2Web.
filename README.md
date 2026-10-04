# Lab2Web.
Tugas Post Test Praktikum 2
# Lab2Web — Praktikum 2: HTML Lanjutan

**Mata Kuliah:** Pemrograman Web
**Dosen Pengampu:** Agung Nugroho
**Nama:** Fajar Dwi Santoso
**NIM:** 312510141
**Program Studi:** Teknik Informatika
**Kampus:** Universitas Pelita Bangsa, Bekasi

---
## Langkah-langkah Praktikum

### 1. Membuat Tabel Data Mahasiswa

**Penjelasan:** Tabel dibuat dengan elemen `<table>`. Baris dibuat dengan `<tr>`, sel judul kolom dengan `<th>`, dan sel data dengan `<td>`. Atribut `border="1"` menampilkan garis tepi tabel.

```html
<!DOCTYPE html>
<html>
<head><title>HTML Lanjutan</title></head>
<body>
<h1>Data Mahasiswa</h1>
<table border="1">
 <tr><th>NIM</th><th>Nama</th><th>Program Studi</th></tr>
 <tr><td>31241001</td><td>Andi</td><td>Teknik Informatika</td></tr>
 <tr><td>31241002</td><td>Budi</td><td>Teknik Informatika</td></tr>
</table>
</body>
</html>
```

**Tugas tambahan:** menambahkan minimal tiga data mahasiswa.

**Hasil:**

<img width="432" height="207" alt="Screenshot 2026-10-04 114136" src="https://github.com/user-attachments/assets/13d2c418-bf60-45ab-91a2-635db6f8cb64" />
---

### 2. Mengembangkan Tabel dengan `thead`, `tbody`, dan `tfoot`

**Penjelasan:** Tabel dikelompokkan menjadi tiga bagian agar lebih terstruktur:

- `<caption>` : judul tabel.
- `<thead>` : bagian kepala tabel (judul kolom).
- `<tbody>` : bagian isi tabel.
- `<tfoot>` : bagian kaki tabel (ringkasan, misalnya rata-rata).
- `colspan` : menggabungkan beberapa kolom menjadi satu sel.

```html
<table border="1">
 <caption>Nilai Praktikum</caption>
 <thead><tr><th>No</th><th>Nama</th><th>Nilai</th></tr></thead>
 <tbody>
 <tr><td>1</td><td>Andi</td><td>85</td></tr>
 <tr><td>2</td><td>Budi</td><td>90</td></tr>
 </tbody>
 <tfoot><tr><td colspan="2">Rata-rata</td><td>87.5</td></tr></tfoot>
</table>
```

**Eksperimen:** mengubah data, menambahkan baris, dan menggunakan `colspan` untuk menggabungkan sel.

**Hasil:**

<img width="440" height="194" alt="Screenshot 2026-10-04 114156" src="https://github.com/user-attachments/assets/a19dc005-6112-4a7f-823d-ae499d31aefe" />
---

### 3. Membuat Form Registrasi Mahasiswa

**Penjelasan:** Form dibuat dengan `<form>`. Setiap input diberi `<label>` yang terhubung melalui atribut `for` dan `id`. Jenis input yang digunakan:

| Tipe Input | Fungsi |
|---|---|
| `text` | Teks biasa (nama lengkap) |
| `email` | Alamat email (format divalidasi browser) |
| `password` | Teks tersembunyi (titik/bintang) |
| `date` | Pemilih tanggal |

Tombol `submit` mengirim form, sedangkan `reset` mengosongkan semua isian.

```html
<h1>Form Registrasi Mahasiswa</h1>
<form>
 <label for="nama">Nama Lengkap</label><br>
 <input type="text" id="nama" name="nama"><br><br>
 <label for="email">Email</label><br>
 <input type="email" id="email" name="email"><br><br>
 <label for="password">Password</label><br>
 <input type="password" id="password" name="password"><br><br>
 <label for="tanggal">Tanggal Lahir</label><br>
 <input type="date" id="tanggal" name="tanggal"><br><br>
 <button type="submit">Daftar</button>
 <button type="reset">Reset</button>
</form>
```

**Hasil:**

<img width="524" height="320" alt="Screenshot 2026-10-04 114238" src="https://github.com/user-attachments/assets/47159e41-ef91-4213-9e67-126e24982144" />
---

### 4. Radio Button dan Checkbox

**Penjelasan:**

- **Radio button** (`type="radio"`) : hanya **satu** pilihan dalam satu grup. Grup ditentukan oleh `name` yang sama (`jk`).
- **Checkbox** (`type="checkbox"`) : boleh memilih **lebih dari satu** pilihan.

```html
<h2>Jenis Kelamin</h2>
<input type="radio" id="laki" name="jk" value="L">
<label for="laki">Laki-laki</label>
<input type="radio" id="perempuan" name="jk" value="P">
<label for="perempuan">Perempuan</label>

<h2>Keahlian</h2>
<input type="checkbox" id="html" name="skill" value="HTML">
<label for="html">HTML</label>
<input type="checkbox" id="css" name="skill" value="CSS">
<label for="css">CSS</label>
<input type="checkbox" id="js" name="skill" value="JavaScript">
<label for="js">JavaScript</label>
```

**Hasil:**

<img width="501" height="208" alt="Screenshot 2026-10-04 114253" src="https://github.com/user-attachments/assets/b97dcd35-ca9e-40a1-a124-60c58afe1b31" />
---

### 5. Select dan Textarea

**Penjelasan:**

- `<select>` dengan `<option>` : menu dropdown untuk memilih satu opsi dari daftar.
- `<textarea>` : kolom input teks **multibaris**. Ukurannya diatur dengan `rows` (jumlah baris) dan `cols` (jumlah kolom).

```html
<label for="prodi">Program Studi</label>
<select id="prodi" name="prodi">
 <option value="">-- Pilih Prodi --</option>
 <option value="ti">Teknik Informatika</option>
 <option value="si">Sistem Informasi</option>
</select>
<br><br>
<label for="alamat">Alamat</label><br>
<textarea id="alamat" name="alamat" rows="5" cols="40"></textarea>
```

**Hasil:**

<img width="442" height="208" alt="Screenshot 2026-10-04 114310" src="https://github.com/user-attachments/assets/95ae61d0-9517-4aca-820d-63ee9d940c93" />
---

### 6. Validasi Form Dasar

**Penjelasan:** HTML5 menyediakan validasi bawaan tanpa JavaScript:

| Atribut | Fungsi |
|---|---|
| `required` | Input wajib diisi |
| `minlength` | Jumlah karakter minimal |
| `min` / `max` | Nilai angka minimum / maksimum |
| `type="email"` | Memastikan format email valid |

```html
<form>
 <label for="nama">Nama</label>
 <input type="text" id="nama" name="nama" required minlength="3">
 <label for="email">Email</label>
 <input type="email" id="email" name="email" required>
 <label for="umur">Umur</label>
 <input type="number" id="umur" name="umur" min="17" max="60" required>
 <button type="submit">Kirim</button>
</form>
```

**Pengamatan:** saat tombol **Kirim** ditekan tanpa mengisi data, browser menampilkan pesan validasi dan menahan pengiriman form sampai isian memenuhi aturan.

**Hasil:**

<img width="386" height="203" alt="Screenshot 2026-10-04 114326" src="https://github.com/user-attachments/assets/e791e919-4d56-4a52-9ef5-deeff13b6fcc" />
---

### 7. Membuat Halaman Semantic HTML

**Penjelasan:** Semantic HTML memakai elemen yang maknanya jelas sehingga struktur halaman mudah dipahami oleh developer, browser, mesin pencari, dan screen reader.

```html
<!DOCTYPE html>
<html>
<head><title>Portal Mahasiswa</title></head>
<body>
<header><h1>Portal Mahasiswa</h1></header>
<nav>
 <a href="#">Beranda</a>
 <a href="#">Profil</a>
 <a href="#">Kontak</a>
</nav>
<main>
 <section>
 <h2>Informasi Akademik</h2>
 <article>
 <h3>Praktikum HTML Lanjutan</h3>
 <p>Mahasiswa mempelajari tabel, form, semantic HTML,
 multimedia, dan validasi.</p>
 </article>
 </section>
 <aside>Informasi tambahan mahasiswa.</aside>
</main>
<footer><p>&copy; 2026 Teknik Informatika</p></footer>
</body>
</html>
```

**Hasil:**

<img width="561" height="307" alt="Screenshot 2026-10-04 114345" src="https://github.com/user-attachments/assets/a951e953-9f0d-42a7-82d4-c18facee50bc" />
---

### 8. Menambahkan Multimedia

**Penjelasan:** Elemen `<audio>` dan `<video>` memutar media langsung di browser. Atribut `controls` menampilkan tombol kontrol (play, pause, volume). Teks di dalam elemen menjadi *fallback* jika browser tidak mendukung.

Struktur folder media:

```
praktikum-2-html-lanjutan/
├── index.html
└── media/
    ├── audio.mp3
    └── video.mp4
```

```html
<h2>Audio</h2>
<audio controls>
 <source src="media/audio.mp3" type="audio/mpeg">
 Browser tidak mendukung audio.
</audio>

<h2>Video</h2>
<video controls width="480">
 <source src="media/video.mp4" type="video/mp4">
 Browser tidak mendukung video.
</video>
```

**Hasil:**

<img width="1364" height="507" alt="Screenshot 2026-10-04 115227" src="https://github.com/user-attachments/assets/464cf42b-4585-4580-a5e5-5c2a94d80b89" />
---

## Proyek Mini: Form Biodata Mahasiswa

**Deskripsi:** Halaman biodata mahasiswa yang menggabungkan seluruh materi praktikum:

| Komponen | Implementasi |
|---|---|
| Semantic structure | `header`, `nav`, `main`, `section`, `footer` |
| Tabel data | Tabel biodata (NIM, Nama, Program Studi) |
| Form | Input teks, email, select, dan textarea |
| Validasi dasar | Atribut `required` pada seluruh input |
| Multimedia | Elemen `<video>` / `<audio>` |

```html
<!DOCTYPE html>
<html>
<head><title>Biodata Mahasiswa</title></head>
<body>
<header><h1>Biodata Mahasiswa</h1></header>
<nav>
 <a href="index.html">Beranda</a>
 <a href="#biodata">Biodata</a>
 <a href="#form">Form</a>
</nav>
<main>
<section id="biodata">
 <h2>Data Mahasiswa</h2>
 <table border="1">
 <tr><th>Data</th><th>Keterangan</th></tr>
 <tr><td>NIM</td><td>312510141</td></tr>
 <tr><td>Nama</td><td>Fajar Dwi Santoso</td></tr>
 <tr><td>Program Studi</td><td>Teknik Informatika</td></tr>
 </table>
</section>

<section id="form">
 <h2>Form Biodata</h2>
 <form>
 <label for="nama">Nama</label>
 <input type="text" id="nama" name="nama" required>
 <br><br>
 <label for="email">Email</label>
 <input type="email" id="email" name="email" required>
 <br><br>
 <label for="prodi">Program Studi</label>
 <select id="prodi" name="prodi" required>
 <option value="">-- Pilih --</option>
 <option value="ti">Teknik Informatika</option>
 <option value="si">Sistem Informasi</option>
 </select>
 <br><br>
 <label for="alamat">Alamat</label><br>
 <textarea id="alamat" name="alamat" required></textarea>
 <br><br>
 <button type="submit">Simpan</button>
 <button type="reset">Reset</button>
 </form>
</section>

<section id="multimedia">
 <h2>Video Perkenalan</h2>
 <video controls width="480">
 <source src="media/video.mp4" type="video/mp4">
 Browser tidak mendukung video.
 </video>
</section>
</main>
<footer><p>&copy; 2026 Teknik Informatika</p></footer>
</body>
</html>
```

> Kode modul belum memuat elemen multimedia, sehingga bagian `<section id="multimedia">` ditambahkan sendiri agar memenuhi ketentuan tugas.

**Hasil:**

<img width="1365" height="638" alt="Screenshot 2026-10-04 114634" src="https://github.com/user-attachments/assets/b82828fc-4b6d-426e-8c15-5a77194eaed5" />

<img width="1365" height="376" alt="Screenshot 2026-10-04 114645" src="https://github.com/user-attachments/assets/6bc87757-b772-47d1-af3e-a1ab34902f81" />

---

## Jawaban Pertanyaan

**1. Apa fungsi `<table>`, `<tr>`, `<th>`, dan `<td>`?**
- `<table>` : membuat tabel.
- `<tr>` (*table row*) : membuat satu baris dalam tabel.
- `<th>` (*table header*) : membuat sel judul kolom/baris.
- `<td>` (*table data*) : membuat sel berisi data.

**2. Apa perbedaan `<th>` dan `<td>`?**
`<th>` adalah sel judul; teksnya otomatis **tebal dan rata tengah**, serta bermakna sebagai header bagi screen reader. `<td>` adalah sel data biasa dengan teks normal rata kiri.

**3. Apa fungsi `colspan` pada tabel?**
`colspan` menggabungkan beberapa kolom menjadi satu sel. Contoh: `colspan="2"` membuat sel melebar selama dua kolom, seperti sel "Rata-rata" pada `tfoot`.

**4. Apa fungsi `<form>` dalam HTML?**
`<form>` adalah wadah untuk mengumpulkan input dari pengguna dan mengirimkannya ke server atau halaman tertentu (melalui atribut seperti `action` dan `method`).

**5. Apa perbedaan radio button dan checkbox?**
Radio button hanya membolehkan **satu** pilihan dari satu grup (grup ditentukan oleh `name` yang sama). Checkbox membolehkan memilih **banyak** pilihan sekaligus dan setiap checkbox bisa dicentang atau tidak secara independen.

**6. Mengapa `<label>` sebaiknya terhubung dengan `id` input melalui atribut `for`?**
- Mengklik teks label otomatis memfokuskan atau memilih input terkait (area klik lebih luas, terutama pada radio/checkbox).
- Meningkatkan aksesibilitas karena screen reader dapat membacakan label bersama inputnya.
- Menjelaskan relasi antara teks dan input secara jelas dalam kode.

**7. Apa perbedaan `<textarea>` dengan `input type="text"`?**
`<textarea>` untuk teks **multibaris** dan panjang (misalnya alamat atau komentar), ukurannya diatur dengan `rows` dan `cols`, serta memiliki tag penutup. `input type="text"` untuk teks **satu baris** pendek (misalnya nama) dan merupakan elemen *self-closing*.

**8. Apa fungsi semantic HTML?**
- `<header>` : bagian kepala halaman atau bagian (judul, logo).
- `<nav>` : kumpulan tautan navigasi.
- `<main>` : isi utama halaman (satu per halaman).
- `<section>` : pengelompokan konten berdasarkan topik.
- `<article>` : konten mandiri yang dapat berdiri sendiri (artikel, berita).
- `<aside>` : konten pendamping/sampingan.
- `<footer>` : bagian kaki halaman atau bagian (hak cipta, kontak).

Manfaatnya: kode lebih mudah dibaca, lebih ramah SEO, dan lebih aksesibel.

**9. Apa fungsi `required`, `min`, `max`, dan `minlength`?**
- `required` : input wajib diisi sebelum form dikirim.
- `min` : nilai minimum yang diperbolehkan (untuk angka/tanggal).
- `max` : nilai maksimum yang diperbolehkan (untuk angka/tanggal).
- `minlength` : jumlah karakter minimal pada input teks.

**10. Apa perbedaan elemen `<audio>` dan `<video>`?**
`<audio>` memutar **suara saja** (misalnya mp3) dan hanya menampilkan pemutar kontrol tanpa tampilan visual. `<video>` memutar **gambar bergerak beserta suara** (misalnya mp4) dan memiliki area tampilan yang ukurannya bisa diatur dengan `width` dan `height`.

---

## Cara Menjalankan

1. Clone repository:
   ```bash
   git clone https://github.com/<username>/Lab2Web.git
   ```
2. Masuk ke folder proyek:
   ```bash
   cd Lab2Web
   ```
3. Buka `index.html` dengan browser (klik dua kali, atau gunakan ekstensi *Live Server* di VS Code).

## Kesimpulan

Melalui Praktikum 2 ini, saya mempelajari cara menyusun data dengan tabel, membuat form dengan berbagai jenis input, menerapkan validasi dasar HTML5, menyusun halaman dengan semantic HTML, serta menyisipkan audio dan video. Seluruh materi digabungkan dalam proyek mini Biodata Mahasiswa yang menunjukkan bagaimana elemen-elemen tersebut bekerja bersama dalam satu halaman web.

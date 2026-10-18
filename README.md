# Lab4Web - Praktikum 4: CSS Lanjutan (Web Layout)

<div align="center">
  <p>Repositori ini memuat hasil pengerjaan <b>Praktikum 4: CSS Lanjutan</b> untuk mata kuliah Pemrograman Web.</p>
  <p>Praktikum ini disusun secara bertahap mengikuti panduan modul untuk memahami struktur layout web, <i>Box Element</i>, <i>CSS Floating</i>, <i>Clearfix</i>, dan elemen semantik HTML5.</p>
</div>

<hr>

##  Data Mahasiswa

> **Nama** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Satrio Erlangga  
> **NIM** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: 312510006  
> **Kelas** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: I253C  
> **Program Studi**: Teknik Informatika  
> **Mata Kuliah** &nbsp;&nbsp;: Pemrograman Web  
> **Dosen** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Agung Nugroho, S.Kom., M.Kom.

<hr>

##  Langkah-Langkah Praktikum

### 1. Membuat Box Element dan CSS Float Property
Membuat file `lab4_box.html` dan menerapkan atribut `float: left` pada elemen div agar elemen tersusun berdampingan secara horizontal.

**Salinan Kode CSS (`lab4_box.html`):**
```html
<style>
    div { float: left; padding: 10px; }
    .div1 { background: red; }
    .div2 { background: yellow; }
    .div3 { background: green; }
</style>
```
Hasil Tampilan (Gambar 4.5):

<img width="113" height="86" alt="Cuplikan layar 2026-10-18 080008" src="https://github.com/user-attachments/assets/9aaa671a-a6ba-490e-b7aa-2f86a39f2c07" />


2. Mengatur Clearfix Element
Menambahkan div keempat (.div4) dan menggunakan properti clear: left untuk mengembalikan aliran normal dokumen setelah elemen di-float.

Salinan Kode CSS Tambahan (lab4_box.html):

```CSS
.div4 {
    background-color: blue;
    clear: left;
    float: none;
}
```
Hasil Tampilan (Gambar 4.6):

<img width="957" height="93" alt="Cuplikan layar 2026-10-18 080156" src="https://github.com/user-attachments/assets/2c0659b9-88f5-42aa-9d6c-ca13bb5d3037" />

3. Membuat Kerangka Layout Sederhana
Membuat file home.html dengan struktur elemen semantik HTML5 (<header>, <nav>, <section>, <aside>, <footer>) tanpa CSS.

Salinan Kode HTML Kerangka (home.html):

```HTML
<div id="container">
    <header>
        <h1>Layout Sederhana</h1>
    </header>
    <nav>
        <a href="home.html" class="active">Home</a>
        <a href="artikel.html">Artikel</a>
        <a href="about.html">About</a>
        <a href="kontak.html">Kontak</a>
    </nav>
    <section id="hero"></section>
    <section id="wrapper">
        <section id="main"></section>
        <aside id="sidebar"></aside>
    </section>
    <footer>
        <p>&copy; 2026 - Universitas Pelita Bangsa</p>
    </footer>
</div>
```
Hasil Tampilan (Gambar 4.9):

<img width="151" height="82" alt="Cuplikan layar 2026-10-18 080807" src="https://github.com/user-attachments/assets/76024e43-a236-4711-b522-6eae9a8828fb" />

4. Mengatur CSS Dasar dan Header
Membuat file style.css, mengatur Reset CSS, lebar kontainer, dan format bagian header.

Salinan Kode CSS (style.css):

```CSS
* { margin: 0; padding: 0; }
#container { width: 980px; margin: 0 auto; box-shadow: 0 0 1em #cccccc; }
header { padding: 20px; }
header h1 { margin: 20px 10px; color: #b5b5b5; }
```
Hasil Tampilan (Gambar 4.10):
<img width="186" height="86" alt="Cuplikan layar 2026-10-18 081422" src="https://github.com/user-attachments/assets/3216c41e-bb68-4615-b51b-ddf95974bb67" />

5. Membuat Navigasi
Menambahkan gaya pada menu navigasi dengan mengubahnya menjadi blok menu horizontal berwarna biru.

Salinan Kode CSS Tambahan (style.css):

```CSS
nav { display: block; background-color: #1f5faa; }
nav a { padding: 15px 30px; display: inline-block; color: #ffffff; text-decoration: none; font-weight: bold; }
nav a.active, nav a:hover { background-color: #2b83ea; }
```
Hasil Tampilan (Gambar 4.11):
<img width="959" height="106" alt="Cuplikan layar 2026-10-18 081524" src="https://github.com/user-attachments/assets/a798eeb8-92ef-40cc-8111-64be6d6b8af5" />

6. Membuat Hero Panel
Mengisi bagian <section id="hero"> pada HTML dengan konten perkenalan dan menambahkan CSS untuk latar belakang dan ukuran huruf besar.

Salinan Kode HTML & CSS Tambahan:

```HTML
<!-- Pada home.html -->
<section id="hero">
    <h1>Hello World!</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
    <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
</section>
```
```CSS
/* Pada style.css */
#hero { background-color: #e4e4e5; padding: 50px 20px; margin-bottom: 20px; }
#hero h1 { margin-bottom: 20px; font-size: 35px; }
#hero p { margin-bottom: 20px; font-size: 18px; line-height: 25px; }
```
Hasil Tampilan (Gambar 4.12):
<img width="959" height="338" alt="Cuplikan layar 2026-10-18 082250" src="https://github.com/user-attachments/assets/e6202f11-bdb5-41d2-b91b-524d6f31d83d" />

7. Mengatur Layout Main, Sidebar Widget, dan Footer
Membagi ruang halaman untuk konten utama (#main) dan bilah sisi (#sidebar), menyisipkan list kontak di HTML, serta memberikan atribut clear pada <footer>.

Salinan Kode HTML & CSS Tambahan:

```HTML
<!-- Pada home.html (Bagian Sidebar) -->
<aside id="sidebar">
    <div class="widget-box">
        <h3 class="title">Widget Header</h3>
        <ul>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
        </ul>
    </div>
</aside>
```
```CSS
/* Pada style.css */
#wrapper { margin: 0; }
#main { float: left; width: 640px; padding: 20px; }
#sidebar { float: left; width: 260px; padding: 20px; }
footer { clear: both; background-color: #1d1d1d; padding: 20px; color: #eee; }
```
Hasil Tampilan (Gambar 4.13 & 4.14):
<img width="958" height="376" alt="Cuplikan layar 2026-10-18 082403" src="https://github.com/user-attachments/assets/f478ca53-09c7-435e-af59-d81ef203cabd" />

8. Menambahkan Konten Box pada Main Content
Membuat struktur 3 kolom di dalam elemen main menggunakan float dengan persentase lebar 33.333333%.

Salinan Kode HTML & CSS Tambahan:

```HTML
<!-- Pada home.html (Di dalam section id="main") -->
<div class="row">
    <div class="box">
        <img src="[https://dummyimage.com/120/db7d25/fff.png](https://dummyimage.com/120/db7d25/fff.png)" class="image-circle">
        <h3>Heading</h3>
        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
        <a href="#" class="btn btn-default">View detail</a>
    </div>
    <!-- (Box diulang 3x sesuai modul) -->
</div>
```
```CSS
/* Pada style.css */
.box { display: block; float: left; width: 33.333333%; padding: 0 10px; text-align: center; }
.image-circle { border-radius: 50%; }
.row:after, .row:before { content:''; display:table; }
.row:after { clear:both; }
```
Hasil Tampilan (Gambar 4.15):
<img width="959" height="377" alt="Cuplikan layar 2026-10-18 082636" src="https://github.com/user-attachments/assets/919031b8-e58c-438c-be8a-d311f06c2009" />

9. Menambahkan Konten Artikel
Menambahkan blok artikel ke dalam #main dengan gambar thumbnail yang di-float ke kiri dan ke kanan.

Salinan Kode HTML & CSS Tambahan:

```HTML
<!-- Pada home.html (Di bawah class row) -->
<hr class="divider" />
<article class="entry">
    <h2>First featurette heading.</h2>
    <img src="[https://dummyimage.com/150/7b8a70/fff.png](https://dummyimage.com/150/7b8a70/fff.png)" alt="">
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit...</p>
</article>
```
```CSS
/* Pada style.css */
.divider { border-top: 1px solid #eeeeee; margin: 40px 0; }
.entry { margin: 15px 0; }
.entry img { float: left; border-radius: 5px; margin-right: 15px; }
.entry .right-img { float: right; margin-left: 15px; }
```
Hasil Tampilan (Gambar 4.16):
<img width="947" height="443" alt="Cuplikan layar 2026-10-18 083010" src="https://github.com/user-attachments/assets/988a8706-e7b0-4e57-8bd7-1367ee466c49" />

 Pertanyaan dan Tugas
1. Tambahkan Layout untuk menu About (Single Layout)
Membuat halaman about.html yang diformat menjadi sebuah Single Layout (tanpa sidebar) untuk mendeskripsikan profil mahasiswa. Pada layout ini, struktur <aside> dihapus sehingga elemen kontainer utama menggunakan keseluruhan lebar layar.

Salinan Kode (about.html):

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About - Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Tentang Saya</h1>
        </header>
        
        <nav>
            <a href="home.html">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html" class="active">About</a>
            <a href="kontak.html">Kontak</a>
        </nav>
        
        <section id="single-layout">
            <article class="entry">
                <h2>Profil Mahasiswa</h2>
                <img src="https://dummyimage.com/150/428bca/fff.png&text=Profil" alt="Foto Profil">
                <p>Halo! Nama saya <b>Satrio Erlangga</b>, seorang mahasiswa Teknik Informatika angkatan 2025 dari Universitas Pelita Bangsa, kelas I253C (NIM: 312510006).</p>
                <p>Halaman About ini dibuat sebagai pemenuhan Tugas Praktikum 4 (CSS Lanjutan) mata kuliah Pemrograman Web yang diajar oleh Bapak Agung Nugroho. Halaman ini menggunakan struktur "Single Layout" di mana lebar konten memanfaatkan seluruh ruang kontainer tanpa adanya Sidebar (aside).</p>
                
                <h3>Portfolio Singkat</h3>
                <br>
                <ul>
                    <li>✅ Lab1Web: HTML Dasar</li>
                    <li>✅ Lab2Web: HTML Lanjutan</li>
                    <li>✅ Lab3Web: CSS Dasar</li>
                    <li>✅ Lab4Web: CSS Lanjutan & Web Layouting</li>
                </ul>
            </article>
        </section>

        <footer>
            <p>&copy; 2026 Universitas Pelita Bangsa - Satrio Erlangga</p>
        </footer>
    </div>
</body>
</html>
```
Hasil Tampilan (Tugas 1 - About):
<img width="552" height="353" alt="Cuplikan layar 2026-10-18 073813" src="https://github.com/user-attachments/assets/3617ffc9-0904-444f-ad10-6efc781df542" />

2. Tambahkan Layout untuk menu Contact (Berisi form isian)
Membuat halaman kontak.html yang terintegrasi dengan struktur layout utama (tetap mempertahankan main content dan sidebar). Bagian konten utama diisi dengan formulir (<form>) HTML interaktif.

Salinan Kode (kontak.html):

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kontak - Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Hubungi Kami</h1>
        </header>
        
        <nav>
            <a href="home.html">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html" class="active">Kontak</a>
        </nav>
        
        <section id="wrapper">
            <section id="main">
                <h2>Kirim Pesan</h2>
                <br>
                <form action="#" method="POST">
                    <div class="form-group">
                        <label for="nama">Nama Lengkap:</label>
                        <input type="text" id="nama" name="nama" placeholder="Masukkan nama Anda" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Alamat Email:</label>
                        <input type="email" id="email" name="email" placeholder="contoh@email.com" required>
                    </div>
                    <div class="form-group">
                        <label for="pesan">Pesan (Message):</label>
                        <textarea id="pesan" name="pesan" rows="6" placeholder="Tuliskan pesan Anda di sini..." required></textarea>
                    </div>
                    <button type="submit" class="btn btn-large">Kirim Pesan Sekarang</button>
                </form>
            </section>
            
            <aside id="sidebar">
                <div class="widget-box">
                    <h3 class="title">Informasi Kontak</h3>
                    <p><b>Alamat:</b><br>Universitas Pelita Bangsa, Cikarang Pusat, Kabupaten Bekasi, Jawa Barat.<br><br><b>Email:</b> satrio@example.com</p>
                </div>
            </aside>
        </section>

        <footer>
            <p>&copy; 2026 Universitas Pelita Bangsa - Satrio Erlangga</p>
        </footer>
    </div>
</body>
</html>
```
Hasil Tampilan (Tugas 2 - Kontak):
<img width="554" height="350" alt="Cuplikan layar 2026-10-18 073857" src="https://github.com/user-attachments/assets/de28d325-be34-4abf-969c-94bca1e85ca8" />

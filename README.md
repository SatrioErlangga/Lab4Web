# Lab4Web - Praktikum 4: CSS Lanjutan (Web Layout)

<div align="center">
  <p>Repositori ini memuat hasil pengerjaan <b>Praktikum 4: CSS Lanjutan</b> untuk mata kuliah Pemrograman Web.</p>
  <p>Fokus utama praktikum ini adalah memahami struktur pembuatan tata letak (layout) web menggunakan konsep <i>Box Element</i>, <i>CSS Floating</i>, serta penerapan <i>HTML5 Semantic Elements</i>.</p>
</div>

<hr>

## Data Mahasiswa

> **Nama** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Satrio Erlangga  
> **NIM** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: 312510006  
> **Kelas** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: I253C  
> **Program Studi**: Teknik Informatika  
> **Instansi** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Universitas Pelita Bangsa  
> **Mata Kuliah** &nbsp;&nbsp;: Pemrograman Web  
> **Dosen** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;: Agung Nugroho, S.Kom., M.Kom.

<hr>

## Langkah-Langkah Praktikum & Hasil

### 1. Eksperimen Box Element dan Clearfix
Menerapkan konsep tata letak dasar berbasis kotak (*box element*) menggunakan tag `<div>` yang disejajarkan dengan atribut `float: left`, serta memulihkan aliran dokumen ke bawah menggunakan atribut `clear: left`.

**Salinan Kode (`lab4_box.html`):**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Box Element</title>
    <style>
        div { float: left; padding: 10px; }
        .div1 { background: red; }
        .div2 { background: yellow; }
        .div3 { background: green; }
        .div4 { background-color: blue; clear: left; float: none; color: white; }
    </style>
</head>
<body>
    <header>
        <h1>Box Element</h1>
    </header>
    <section>
        <div class="div1">Div 1</div>
        <div class="div2">Div 2</div>
        <div class="div3">Div 3</div>
        <div class="div4">Div 4 (Ini adalah Clearfix)</div>
    </section>
</body>
</html>
```
Hasil Tampilan Screenshot 1:
<img width="957" height="86" alt="Cuplikan layar 2026-10-18 073422" src="https://github.com/user-attachments/assets/ca768357-b717-4c62-bc99-202703a8d8d5" />



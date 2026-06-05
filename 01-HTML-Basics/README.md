# 📖 HTML Basics - Panduan Lengkap

**HTML (HyperText Markup Language)** adalah fondasi dari setiap website. Pelajari struktur dasar, tags, dan best practices.

---

## 📋 Daftar Isi

1. [Apa itu HTML?](#apa-itu-html)
2. [Struktur Dasar HTML](#struktur-dasar-html)
3. [Tags dan Elements](#tags-dan-elements)
4. [Semantic HTML](#semantic-html)
5. [Forms dan Input](#forms-dan-input)
6. [Best Practices](#best-practices)

---

## Apa itu HTML?

HTML adalah bahasa markup yang digunakan untuk membuat struktur halaman web. HTML tidak adalah bahasa pemrograman, tetapi bahasa untuk mendefinisikan konten.

### Contoh HTML Sederhana:

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Halaman Pertama Saya</title>
</head>
<body>
    <h1>Selamat Datang!</h1>
    <p>Ini adalah paragraf pertama saya.</p>
</body>
</html>
```

---

## Struktur Dasar HTML

### Element-Element Penting:

| Element | Fungsi |
|---------|--------|
| `<!DOCTYPE html>` | Deklarasi tipe dokumen |
| `<html>` | Root element |
| `<head>` | Informasi meta tentang dokumen |
| `<title>` | Judul halaman (tampil di tab) |
| `<body>` | Konten yang ditampilkan |
| `<meta>` | Metadata halaman |

### Penjelasan Struktur:

```html
<!DOCTYPE html>                    <!-- Deklarasi HTML5 -->
<html lang="id">                   <!-- Root element dengan bahasa -->
<head>                             <!-- Section header -->
    <meta charset="UTF-8">        <!-- Encoding karakter -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Meta untuk responsive -->
    <title>Judul Halaman</title>   <!-- Judul di tab browser -->
</head>
<body>                             <!-- Section konten -->
    <!-- Konten halaman di sini -->
</body>
</html>
```

---

## Tags dan Elements

### Headings (Judul)

```html
<h1>Ini Heading 1 (Paling Penting)</h1>
<h2>Ini Heading 2</h2>
<h3>Ini Heading 3</h3>
<h4>Ini Heading 4</h4>
<h5>Ini Heading 5</h5>
<h6>Ini Heading 6 (Paling Kecil)</h6>
```

**Catatan:** Gunakan hanya satu `<h1>` per halaman!

### Paragraf dan Text

```html
<!-- Paragraf -->
<p>Ini adalah paragraf.</p>

<!-- Bold (Penting) -->
<strong>Teks penting</strong>  <!-- Semantic -->
<b>Teks bold</b>              <!-- Non-semantic -->

<!-- Italic (Penekanan) -->
<em>Teks italic</em>           <!-- Semantic -->
<i>Teks italic</i>             <!-- Non-semantic -->

<!-- Line break -->
Baris pertama<br>
Baris kedua

<!-- Horizontal line -->
<hr>
```

### List (Daftar)

```html
<!-- Unordered List (Bullet) -->
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>

<!-- Ordered List (Numbered) -->
<ol>
    <li>Pertama</li>
    <li>Kedua</li>
    <li>Ketiga</li>
</ol>

<!-- Nested List -->
<ul>
    <li>Buah
        <ul>
            <li>Apel</li>
            <li>Jeruk</li>
        </ul>
    </li>
    <li>Sayuran</li>
</ul>
```

### Links (Tautan)

```html
<!-- Link Internal -->
<a href="/halaman-lain.html">Klik di sini</a>

<!-- Link External -->
<a href="https://www.google.com" target="_blank">Buka Google</a>

<!-- Link dengan Title -->
<a href="/about" title="Tentang Kami">About</a>
```

### Images (Gambar)

```html
<!-- Gambar Lokal -->
<img src="/images/foto.jpg" alt="Deskripsi Foto">

<!-- Gambar dari Internet -->
<img src="https://example.com/image.jpg" alt="Gambar" width="300" height="200">

<!-- Gambar dengan Link -->
<a href="/halaman-detail">
    <img src="/images/thumbnail.jpg" alt="Thumbnail">
</a>
```

---

## Semantic HTML

Semantic HTML menggunakan tags yang memiliki makna, bukan hanya untuk styling.

### Tags Semantic Penting:

```html
<!-- Header Section -->
<header>
    <h1>Nama Website</h1>
    <nav>
        <a href="/">Home</a>
        <a href="/about">About</a>
        <a href="/contact">Contact</a>
    </nav>
</header>

<!-- Main Content -->
<main>
    <!-- Article -->
    <article>
        <h2>Judul Artikel</h2>
        <p>Konten artikel...</p>
        <footer>
            <p>Ditulis oleh: John Doe</p>
        </footer>
    </article>
    
    <!-- Aside (Sidebar) -->
    <aside>
        <h3>Artikel Terkait</h3>
        <ul>
            <li><a href="#">Artikel 1</a></li>
            <li><a href="#">Artikel 2</a></li>
        </ul>
    </aside>
</main>

<!-- Footer -->
<footer>
    <p>&copy; 2026 Nama Website. All rights reserved.</p>
</footer>
```

### Keuntungan Semantic HTML:
- ✅ SEO lebih baik
- ✅ Accessibility lebih baik
- ✅ Kode lebih mudah dibaca
- ✅ Maintainability lebih baik

---

## Forms dan Input

### Form Dasar:

```html
<form action="/submit" method="POST">
    <!-- Text Input -->
    <label for="nama">Nama:</label>
    <input type="text" id="nama" name="nama" required>
    
    <!-- Email Input -->
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    
    <!-- Password Input -->
    <label for="password">Password:</label>
    <input type="password" id="password" name="password" required>
    
    <!-- Radio Button -->
    <label>
        <input type="radio" name="gender" value="male"> Laki-laki
    </label>
    <label>
        <input type="radio" name="gender" value="female"> Perempuan
    </label>
    
    <!-- Checkbox -->
    <label>
        <input type="checkbox" name="agree" required> Saya setuju dengan terms
    </label>
    
    <!-- Dropdown Select -->
    <label for="country">Negara:</label>
    <select id="country" name="country">
        <option value="">Pilih Negara</option>
        <option value="id">Indonesia</option>
        <option value="my">Malaysia</option>
        <option value="sg">Singapore</option>
    </select>
    
    <!-- Textarea -->
    <label for="message">Pesan:</label>
    <textarea id="message" name="message" rows="5" cols="50"></textarea>
    
    <!-- Submit Button -->
    <button type="submit">Kirim</button>
    <button type="reset">Reset</button>
</form>
```

---

## Best Practices

### 1. Gunakan Semantic HTML
```html
<!-- ❌ Salah -->
<div class="header">...</div>
<div class="nav">...</div>

<!-- ✅ Benar -->
<header>...</header>
<nav>...</nav>
```

### 2. Selalu Gunakan Alt Text pada Gambar
```html
<!-- ❌ Salah -->
<img src="foto.jpg">

<!-- ✅ Benar -->
<img src="foto.jpg" alt="Foto profil pengguna">
```

### 3. Gunakan Label untuk Form
```html
<!-- ❌ Salah -->
<input type="text">

<!-- ✅ Benar -->
<label for="username">Username:</label>
<input type="text" id="username" name="username">
```

### 4. Struktur Heading yang Benar
```html
<!-- ❌ Salah -->
<h1>Judul</h1>
<h3>Subheading</h3>  <!-- Melompat dari h1 ke h3 -->

<!-- ✅ Benar -->
<h1>Judul</h1>
<h2>Subheading</h2>
<h3>Sub-subheading</h3>
```

### 5. Gunakan Meta Tags
```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Deskripsi halaman untuk SEO">
    <meta name="keywords" content="keyword1, keyword2">
</head>
```

---

## 📝 Latihan

Buat halaman HTML dengan:
1. Header dengan judul dan navigation
2. Main content dengan artikel
3. Sidebar dengan list
4. Form untuk subscribe
5. Footer

---

## 🔗 Resource Lebih Lanjut

- [MDN HTML Documentation](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [HTML5 Specification](https://html.spec.whatwg.org/)
- [W3C HTML Validator](https://validator.w3.org/)

---

[← Kembali ke Main](../README.md) | [Lanjut ke CSS →](../02-CSS-Styling/README.md)
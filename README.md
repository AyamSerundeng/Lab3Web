# Lab3Web - CSS Dasar

**Nama:** Khairi Ramadhan Yudhatama (312510099)  
**Kelas:** Pemrograman Web (I251A)  
**Dosen:** Agung Nugroho, S.Kom., M.Kom.  
**Mata Kuliah:** Pemrograman Web  
**Universitas:** Universitas Pelita Bangsa

---

## Tujuan Praktikum

Memahami cara penggunaan CSS Dasar yang meliputi:

- CSS Internal
- CSS Inline
- CSS Eksternal
- CSS Selector (ID Selector & Class Selector)

---

## Instruksi Praktikum

1. Persiapkan text editor (VSCode).
2. Buat file baru dengan nama `lab2_css_dasar.html`.
3. Buat struktur dasar dokumen HTML.
4. Ikuti langkah-langkah praktikum secara berurutan.
5. Lakukan validasi dokumen CSS melalui [https://jigsaw.w3.org/css-validator/](https://jigsaw.w3.org/css-validator/).

---

## Langkah-langkah Praktikum

### 1. Membuat Dokumen HTML

Buat file baru bernama `lab2_css_dasar.html` dengan struktur dasar HTML sebagai berikut:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CSS Dasar</title>
  </head>
  <body>
    <header>
      <h1>CSS Internal dan <i>Inline CSS</i></h1>
    </header>
    <nav>
      <a href="lab2_css_dasar.html">CSS Dasar</a>
      <a href="lab2_css_eksternal.html">CSS Eksternal</a>
      <a href="lab1_tag_dasar.html">HTML Dasar</a>
    </nav>
    <!-- CSS ID Selector -->
    <div id="intro">
      <h1>Hello World</h1>
      <p>
        Kami sedang belajar HTML dan CSS dasar, pada mata kuliah
        <b>Pemrograman Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran
        pertama yang kami dapat adalah membuat tampilan web sederhana dalam
        rangka mengenal tag-tag dasar HTML dan CSS.
      </p>
      <!-- CSS Class Selector -->
      <a class="button btn-primary" href="#intro">Informasi selengkapnya.</a>
    </div>
  </body>
</html>
```

Setelah file dibuat, buka di browser untuk melihat hasilnya.

**Screenshot hasil langkah 1:**

<!-- Upload screenshot di sini -->

<img width="941" height="479" alt="Screenshot 2026-10-07 072715" src="https://github.com/user-attachments/assets/d5c53436-a135-46b3-8428-e29a1c9ca7ec" />


---

### 2. Mendeklarasikan CSS Internal

Tambahkan deklarasi CSS Internal di dalam bagian `<head>` dokumen HTML:

```html
<head>
  <title>CSS Dasar</title>
  <style>
    body {
      font-family: "Open Sans", sans-serif;
    }
    header {
      min-height: 80px;
      border-bottom: 1px solid #77ccef;
    }
    h1 {
      font-size: 24px;
      color: #0f189f;
      text-align: center;
      padding: 20px 10px;
    }
    h1 i {
      color: #6d6a6b;
    }
  </style>
</head>
```

Simpan perubahan, lalu refresh browser untuk melihat hasilnya.

**Penjelasan:**

- `body` → mengatur font default seluruh halaman.
- `header` → mengatur tinggi minimum dan border bawah.
- `h1` → mengatur ukuran font, warna, rata tengah, dan padding.
- `h1 i` → mengatur warna khusus pada elemen italic di dalam heading.

**Screenshot hasil langkah 2:**

<!-- Upload screenshot di sini -->

<img width="937" height="402" alt="Screenshot 2026-10-07 073155" src="https://github.com/user-attachments/assets/d01f9843-d437-4c1b-b179-c44ea9172198" />


---

### 3. Menambahkan Inline CSS

Tambahkan deklarasi **Inline CSS** pada tag `<p>`:

```html
<p style="text-align: center; color: #ccd8e4;"></p>
```

Simpan kembali dan refresh browser.

**Penjelasan:**
Inline CSS ditulis langsung di dalam atribut `style` pada elemen HTML. Cara ini memiliki prioritas lebih tinggi dibanding CSS Internal maupun Eksternal.

**Screenshot hasil langkah 3:**

<!-- Upload screenshot di sini -->

<img width="949" height="388" alt="Screenshot 2026-10-07 075207" src="https://github.com/user-attachments/assets/ee3b9bea-8dbe-425e-83c3-efb8729c0619" />


---

### 4. Membuat CSS Eksternal

#### a. Buat file CSS baru

Buat file baru dengan nama `style_eksternal.css` dan isikan kode berikut:

```css
nav {<img width="949" height="388" alt="Screenshot 2026-10-07 075207" src="https://github.com/user-attachments/assets/efdbea69-2e94-47e4-b3f7-673cffd92f77" />

  background: #20a759;
  color: #fff;
  padding: 10px;
}

nav a {
  color: #fff;
  text-decoration: none;
  padding: 10px 20px;
}

nav .active,
nav a:hover {
  background: #0b6b3a;
}
```

#### b. Hubungkan file CSS ke HTML

Tambahkan tag `<link>` di dalam bagian `<head>`:

```html
<head>
  <!-- menyisipkan css eksternal -->
  <link rel="stylesheet" href="style_eksternal.css" type="text/css" />
</head>
```

Simpan dan refresh browser.

**Penjelasan:**

- CSS Eksternal ditulis di file terpisah (`.css`).
- File dihubungkan ke HTML menggunakan tag `<link>`.
- Keuntungan: kode CSS dapat digunakan kembali di banyak halaman.

**Screenshot hasil langkah 4:**

<!-- Upload screenshot di sini -->

<img width="957" height="550" alt="Screenshot 2026-10-07 075651" src="https://github.com/user-attachments/assets/e38f79e4-84fe-4a75-8569-50523fc679e4" />


---

### 5. Menambahkan CSS Selector (ID & Class)

Tambahkan kode berikut ke dalam file `style_eksternal.css`:

```css
/* ID Selector */
#intro {
  background: #418fb1;
  border: 1px solid #099249;
  min-height: 100px;
  padding: 10px;
}

#intro h1 {
  text-align: left;
  border: 0;
  color: #fff;
}

/* Class Selector */
.button {
  padding: 15px 20px;
  background: #bebcbd;
  color: #fff;
  display: inline-block;
  margin: 10px;
  text-decoration: none;
}

.btn-primary {
  background: #e42a42;
}
```

Simpan dan refresh browser.

**Penjelasan:**

- **ID Selector** (`#intro`) → menargetkan elemen yang memiliki atribut `id="intro"`. Satu ID hanya boleh digunakan sekali dalam satu halaman.
- **Class Selector** (`.button` dan `.btn-primary`) → menargetkan elemen yang memiliki class tersebut. Class dapat digunakan berkali-kali pada banyak elemen.
- `#intro h1` merupakan **descendant selector** (h1 yang berada di dalam elemen `#intro`).

**Screenshot hasil langkah 5:**

<!-- Upload screenshot di sini -->

<img width="955" height="529" alt="Screenshot 2026-10-07 075838" src="https://github.com/user-attachments/assets/bce9514c-2bbb-4c72-9c29-aa1bce1aee36" />


---

# HematEnergi

Website Edukasi Hemat Energi - Rumah Ramah Lingkungan
**SDG 7 (Energi Bersih dan Terjangkau) dan SDG 13 (Penanganan Perubahan Iklim)**
Sasaran pengguna: masyarakat umum, terutama keluarga dan pelajar.

## Anggota Kelompok
1. Shelcy Loista Br Tarigan - 2515091109 - Pengembang Halaman Utama (Beranda)
2. Michael Perimsa Sitepu - 2515091144 - Peneliti Konten dan Pengembang Halaman Edukasi
3. Andreas Hilkia Jupriono Siregar - 2515091058 - Penyusun Panduan dan Desainer Interaksi
4. Ni Luh Meitri Anggia Oka - 2515091056 - Penulis Artikel dan Pengelola Referensi Data
5. Ni Kadek Juniartini - 2515091100 - Pengembang CSS, Tata Letak, dan Responsivitas

## Deskripsi Website
**Tujuan:** mengedukasi masyarakat agar menghemat listrik dan beralih ke energi bersih.
**Manfaat:** tagihan listrik turun, lingkungan lebih terjaga, emisi karbon berkurang.

| Halaman | Fungsi |
|---|---|
| index.html (Beranda) | Pengenalan website, hero, dan menu ke konten utama |
| edukasi.html | Konsep, isu, dan fakta tentang energi |
| panduan.html | Langkah praktis hemat energi di rumah |
| artikel.html | Artikel edukatif beserta sumbernya |
| tentang.html | Tim pengembang, tujuan, dan referensi |

## Teknologi
HTML5, CSS3 (eksternal), Flexbox, CSS Grid, CSS Media Queries.
Tanpa framework CSS dan tanpa JavaScript.

## Penjelasan Implementasi

### 1. HTML5 Semantik
```html
<header class="navbar">
  <nav aria-label="Navigasi utama">...</nav>
</header>
<main>
  <section class="hero">...</section>
</main>
```
Fungsi: `header` untuk bagian kepala, `nav` untuk menu, `main` untuk isi utama,
dan `section` untuk membagi topik, sehingga struktur halaman jelas.

### 2. Navigasi Antarhalaman
```html
<li><a href="edukasi.html">Edukasi</a></li>
<li><a href="panduan.html">Panduan</a></li>
```
Fungsi: tautan relatif menghubungkan kelima halaman. Menu yang sama dipasang
di semua halaman agar konsisten. Halaman aktif diberi `aria-current="page"`.

### 3. CSS Eksternal dan Variabel
```css
:root {
  --primary-dark: #2E7032;
  --bg-cream: #F5F6ED;
}
```
Fungsi: warna disimpan sebagai variabel agar seluruh halaman memakai warna
yang sama dan mudah diganti dari satu tempat.

### 4. Flexbox (menu navigasi)
```css
.nav-links {
  display: flex;
}
```
Fungsi: item menu berjajar menyamping dengan rapi.

### 5. CSS Grid (hero dan kartu)
```css
.hero-grid {
  display: grid;
  grid-template-columns: 1.1fr 1fr;
}
.cards-grid {
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
}
```
Fungsi: hero dibagi dua kolom (teks dan gambar). Kartu menyesuaikan jumlah
kolom otomatis sesuai lebar layar.

### 6. Media Queries (responsif)
```css
@media (max-width: 640px) {
  .nav-container { flex-direction: column; }
  .cards-grid { grid-template-columns: 1fr; }
}
```
Fungsi: pada layar HP (640 px ke bawah), menu menurun ke bawah dan kartu
menjadi satu kolom. Pada 900 px (tablet), kartu menjadi dua kolom.
Pengujian dilakukan pada 1440 px, 768 px, dan 375 px.

## Struktur Folder
```
hemat-energi/
|-- index.html
|-- edukasi.html
|-- panduan.html
|-- artikel.html
|-- tentang.html
|-- css/
|   `-- style.css
|-- images/
|   |-- panel-surya.jpg
|   |-- rumah-ramah-energi.jpg
|   |-- energi-terbarukan.jpg
|   `-- energi-bersih.jpg
`-- README.md
```

## Website dan Repository
- Website: https://shelcyloista077-cloud.github.io/hemat-energi/
- Repository: https://github.com/shelcyloista077-cloud/hemat-energi

## Referensi
**Konten:**
- United Nations. *What Is Renewable Energy?* https://www.un.org/en/climatechange/what-is-renewable-energy
- U.S. Department of Energy. *Solar Photovoltaic System Design Basics.* https://www.energy.gov/cmei/systems/solar-photovoltaic-system-design-basics
- Archify. *5 Hal untuk Diperhatikan agar Ventilasi Optimal.* https://www.archify.com/id/archifynow/5-hal-untuk-diperhatikan-agar-ventilasi-optimal-dan-rumah-selalu-sejuk-alami
- PBB Indonesia. *Hari Energi Bersih Internasional.* https://indonesia.un.org/id/257848-hari-energi-bersih-internasional-26-januari

**Aset gambar:** dihasilkan melalui Google Gemini (AI), diakses 29 Oktober 2026.
- panel-surya.jpg: https://share.gemini.google/chWu0bvwSyTv
- rumah-ramah-energi.jpg: https://share.gemini.google/PnFWqxEuQZNT
- energi-terbarukan.jpg: https://share.gemini.google/6wPMg0OWCKjz
- energi-bersih.jpg: https://share.gemini.google/Y3cqtNZfQvC8

**Font:** Poppins dan Nunito (Google Fonts).
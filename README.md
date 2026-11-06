# MLF Project: Website Portofolio

Website portofolio dan form booking untuk **MLF Project** (fotografi & videografi: wisuda, event, olahraga, wedding) di Indramayu, Cirebon, dan Kuningan.

Website ini statis: hanya HTML, CSS, dan sedikit JavaScript, tanpa build step.

## Struktur

```
.
├── index.html          # seluruh halaman (CSS & JS ada di dalamnya)
├── assets/img/         # foto galeri dan logo
├── README.md
└── .gitignore
```

## Menjalankan di komputer

Buka `index.html` langsung di browser, atau jalankan server lokal:

```bash
python3 -m http.server 8000
# lalu buka http://localhost:8000
```

## Deploy gratis dengan GitHub Pages

1. Buat repository di GitHub, lalu push semua file ini ke branch `main`.
2. Buka **Settings → Pages**.
3. Pada **Build and deployment**, pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, lalu **Save**.
4. Tunggu 1-2 menit. Alamat website akan tampil di halaman yang sama: `https://<username>.github.io/<nama-repo>/`.

## Cara mengubah isi

| Yang diubah | Cari di `index.html` |
|---|---|
| Nomor WhatsApp | `6283821468728` (format `62` tanpa `+` dan tanpa `0` di depan; ada beberapa tempat, gunakan find & replace) |
| Harga paket | bagian `<section id="paket">` |
| Opsi paket di form booking | `<select id="f-paket">` (atribut `data-p` adalah harga dalam rupiah) |
| Syarat dan ketentuan | tag `<details>` di bagian paket |
| Foto galeri | ganti file di `assets/img/` dengan nama sama, atau ubah tag `<img>` di `<section id="karya">` |
| Warna | variabel CSS di bagian `:root` paling atas |

Tips foto: perkecil dulu ke sisi terpanjang sekitar 900-1200 px dan kualitas JPEG 75-80 agar halaman cepat dibuka di HP.

## Form booking

Form tidak menyimpan data di server. Saat tombol **Kirim lewat WhatsApp** ditekan, data disusun menjadi pesan dan dibuka lewat tautan `wa.me` ke nomor admin.

## Catatan

- Font dimuat dari Google Fonts (Bricolage Grotesque dan Instrument Sans); jika gagal dimuat, halaman memakai font sistem.
- Pastikan klien (terutama foto wedding, wisuda, dan foto sekolah) setuju fotonya tampil di portofolio.

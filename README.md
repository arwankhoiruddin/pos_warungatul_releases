# POS Warung Atul — Repositori Rilis

Repositori **publik** ini hanya berisi berkas rilis APK aplikasi kasir **POS Warung Atul**
(Android). Aplikasi memeriksa rilis terbaru di sini lalu menawarkan pembaruan langsung
dari dalam aplikasi (Pengaturan → Pembaruan aplikasi).

## Aturan tag rilis

```
v<versionName>+<versionCode>      contoh: v1.0.1+3
```

* `versionName` dan `versionCode` harus sama dengan yang ada di `app/build.gradle.kts`.
* **`versionCode` adalah pembanding utama.** Aplikasi menawarkan pembaruan bila
  `versionCode` rilis lebih besar dari versi yang terpasang.
* Setiap rilis **wajib** memuat satu aset berakhiran `.apk` — aset itulah yang diunduh.
* Nama aset yang disarankan: `pos-warungatul-<versionName>-release.apk`.

## Cara aplikasi memeriksa pembaruan

```
GET https://api.github.com/repos/arwankhoiruddin/pos_warungatul_releases/releases/latest
```

Tanpa token (repositori publik), lalu mengunduh `browser_download_url` dari aset `.apk`.
Catatan API GitHub: tanpa token dibatasi 60 permintaan/jam per alamat IP — lebih dari cukup
karena pemeriksaan hanya terjadi saat kasir membuka layar Pengaturan.

## Rilis

| Tag | Isi | Catatan |
| --- | --- | --- |
| `v1.0.0+1` | APK debug (uji internal) | Ditandatangani kunci debug, untuk mencoba alur pembaruan. |

Repositori kode sumber aplikasi bersifat privat; yang publik hanya berkas rilis di sini.

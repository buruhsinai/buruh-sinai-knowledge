# Indeks Sumber

Folder ini adalah lapisan **SUMBER** dalam model 4 lapis Qiladat Knowledge Engine:

```
PERTANYAAN → KONSEP → SUMBER → SINTESIS
```

Isinya menaut ke halaman-halaman nyata di repo website (`buruhsinai/qiladat`, di-hosting lewat GitHub Pages di `https://buruhsinai.github.io/qiladat/`). Bukan Issue, bukan konten baru — murni pointer ke apa yang sudah ada.

## Kategori sumber

1. [Dien](./website-dien.md) — ranah keislaman: pondok, syair, rangkuman, media
2. [Produk](./website-produk.md) — katalog produk global
3. [Kesehatan](./website-kesehatan.md) — terapi, produk kesehatan, media
4. [Artikel](./website-artikel.md) — indeks & detail artikel
5. [Alat](./website-alat.md) — 560 alat interaktif dalam 21 kategori

## Belum tercakup (catatan untuk nanti)

Ditemukan saat audit terakhir — folder-folder ini ada di repo `qiladat` tapi belum punya file sumber sendiri:

- `sains/` — ranah sains (astronomi, produk, media) — **belum ada file sumber sama sekali**, perlu dibuat
- `arsip/` — arsip global
- `info/` — info global
- `css/` (root) — stylesheet bersama, bukan konten, mungkin tidak perlu file sumber

## ⚠️ Temuan bug navigasi (perlu keputusan)

Link navigasi antar-ranah di dalam website (misalnya di `dien/index.html`) memakai path absolut dari root, contoh `href="/kesehatan/"`. Karena repo `qiladat` di-hosting sebagai *project site* GitHub Pages (bukan *user/organization site*), URL sebenarnya berada di sub-path `/qiladat/...` — bukan di root domain. Akibatnya link seperti `/kesehatan/` akan mengarah ke `https://buruhsinai.github.io/kesehatan/` (salah, hilang `/qiladat/`), bukan ke halaman yang benar.

Ini bug di website itu sendiri, di luar cakupan folder `sumber/` — tapi berarti navigasi antar-ranah di situs Pages kemungkinan rusak sampai path-nya diperbaiki jadi relatif (`../kesehatan/`) atau ditambah custom domain.

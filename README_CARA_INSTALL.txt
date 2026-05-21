STRUKTUR GITHUB
===============

Upload file seperti ini di root repository:

index.html
manifest.webmanifest
sw.js
offline.html
README_CARA_INSTALL.txt
icons/
  icon-192.png
  icon-512.png


URL APPS SCRIPT
===============

URL Apps Script sudah dimasukkan ke index.html:

https://script.google.com/a/~/macros/s/AKfycbzbHGvXwHUwDju-KxgvUtaHD0CWmnou97ZixVRJQHewTAkkdu4yvwMxyTVqBS6sgWtz/exec


CARA UPDATE APLIKASI
====================

Setiap kali Anda mengubah file aplikasi di GitHub, naikkan versi di sw.js.

Contoh:

const CACHE_NAME = "ykpi-pwa-shell-v2";

ubah menjadi:

const CACHE_NAME = "ykpi-pwa-shell-v3";

Setelah file GitHub diperbarui, pengguna akan melihat layar:
"Update Aplikasi Tersedia"

Aplikasi akan terkunci dan tidak bisa digunakan sebelum tombol Update Sekarang diklik.
Saat tombol diklik, animasi update berjalan 5 detik, lalu aplikasi reload otomatis.


CATATAN
=======

- Tombol Muat Ulang sudah dihapus.
- Tombol Install tetap tersedia jika browser mendukung instalasi PWA.
- Pastikan GitHub Pages aktif pada branch main dan folder /root.
- Apps Script harus tetap memakai:
  .setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL)

---
marp: true
---

# **Dasar Sistem Administrasi**

    NRP   : 3122600004
    Nama  : Rizal Maulana
    Kelas : 2 D4 IT A
    Dosen : Dr. Ferry Astika Saputra, ST, M.Sc


---

# Sumber Perangkat Lunak

 Debian GNU/Linux menggunakan metodologi repository untuk mendistribusi aplikasinya. metodologi ini menggunakan centralisasi software dan menggunakan tampilan untuk mengelola dan mengupgrade sistem kita.

---

## file sources.list

Alamat internet repositori debian disimpan difile **/etc/apt/sources.list**, detailnya tipe filenya **/etc/apt/sources.list.d/xxx.list**. 
untuk memodifikasi file sources.list, kita bisa menggunakan command dibawah ini 

    apt edit-sources 
    nano /etc/apt/sources.list

---

## Tentang repositori, branch, dan bagian/komponen

Debian mengatur softwarenya kedalam packages didalam banyak repositori. repositori itu dipisahkan ke beberapa branch dan bagian/komponen. 

Ada 4 bagian di dalam repositori debian : 
- main : Paket tersebut mematuhi Pedoman Perangkat Lunak Bebas Debian (DFSG), yang menjamin kebebasan dan keterbukaannya.
- non-free-fireware : non-free-firewares termasuk secara default saat debian 12 terbit
- contrib : mematuhi DFSG dengan paket non-free
- non-free : tidak mematuhi aturan DFSG

**DFSG** (Debian Free Software Guidelines) : filosofi prinsip dari perangkat lunak bebas menurut debian

---

## Backport Packages 
Debian juga menyediakan repositori spesial yang bernama backport. backport berisi beberapa aplikasi dengan versi terbaru. repositori ini secara default tidak aktif, tapi tidak menimbul resiko disistem kita. 

mekanisme backport mengizinkan aplikasi di debian development repositori untuk di rombak ulang menjadi versi yang stabil

---

## Memodifikasi Repositori

Untuk memodifikasi cukup edit file sources.list

    apt edit-sources

---

# APT di Terminal

APT (Advanced Package Tool), Debian juga support "aptitude", package manager lain, dengan syntax dan perilaku yang berbeda 

## Perintah untuk pencarian dan menampilkan informasi

| Perintah || Deskripsi |
|---|---|---|
| apt show foo | | menampilkan informasi tentang package |
| apt search foo || mencari package yang sesuai dengan yang dicari |
| apt-cache policy foo || menampilkan versi yang tersedia |
| apt full-upgrade || update paket yang terinstall, dengan menambahkan/menghapus paket yang diperlukan |
| apt remove foo || menghapus paket foo, tapi tidak dengan file konfigurasi |
| apt autoremove || auto menghapus paket yang tidak dibutuhkan |
| apt purge foo || membersihkan paket foo dan file konfigurasinya |
| apt clean || membersihkan local cache dari instalasi paket |
| apt autoclean || membersihkan local cache dari absolute paket |
| apt-mark showmanual || menandai paket agar instalasinya manual |

---

# Software : Simplifikasi Package Manager

Di debian ada aplikasi **Software** yang berguna untuk searching, install, delete atau update paket paket yang berisi aplikasi kita, 
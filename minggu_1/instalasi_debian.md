    NRP   : 3122600004
    Nama  : Rizal Maulana
    Kelas : 2 D4 IT A
    Dosen : Dr. Ferry Astika Saputra, ST, M.Sc

# Instalasi Debian di MAC

1. Pastikan sudah menginstall Virtual Box dan sudah mendownload file ISO debian, kemudian klik tombol baru
![](./assets/1.png)

2. Masukan nama dan sistem virtualnya, lalu pilih file ISO dan centang skip instalasi tak didampingi
![](./assets/2.png)

3. set besar ram dan prosesor pada sistem virtual
![](./assets/3.png)

4. kemudian set besar disk 
![](./assets/4.png)

5. kemudian lanjut sampai sistem virtual sudah ada di dashboard awal
![](./assets/5.png)
![](./assets/6.png)

6. kemudian start untuk konfigurasi sistem debiannya
![](./assets/7.png)
![](./assets/8.png)
![](./assets/9.png)
![](./assets/10.png)
![](./assets/11.png)
![](./assets/12.png)
![](./assets/13.png)
![](./assets/14.png)
![](./assets/15.png)
![](./assets/16.png)
![](./assets/17.png)
![](./assets/18.png)
![](./assets/19.png)
![](./assets/20.png)

7. contoh semua konfigurasi yang diatas dan tekan lanjutkan, setelah semua sudah maka kita bisa melihat tampilan awal debian 
![](./assets/21.png)


### Perbedaan antara Debian 12 (Bookworm) dan Debian 11 (Bullseye) dalam bentuk tabel:

| Perbedaan                             | Debian 12 (Bookworm)    | Debian 11 (Bullseye)    |
|---------------------------------------|--------------------------|-------------------------|
| Versi Kernel                          | 5.16.x                    | 5.10.x                  |
| Kebutuhan Sistem                     | Mungkin lebih tinggi     | Lebih rendah            |
| Penerapan systemd                     | Secara default           | Secara default          |
| Perbedaan Package                    | Mungkin lebih baru       | Stabil dan teruji       |

Perlu dicatat bahwa informasi ini mungkin berubah seiring waktu, tergantung pada pembaruan dan evolusi distribusi Debian. Disarankan untuk merujuk langsung ke situs web resmi Debian untuk informasi terkini tentang perbedaan antara versi yang berbeda.

### Jelaskan fungsi dari file "/etc/groups" beserta formatnya!

File "/etc/group" adalah file konfigurasi pada sistem Linux yang menyimpan informasi tentang grup pengguna. Setiap baris dalam file ini mewakili satu grup dan berisi beberapa kolom yang dipisahkan oleh titik dua (:). Formatnya adalah sebagai berikut:

```
nama_grup:kata_sandi:ID_grup:daftar_anggota
```

1. **Nama Grup**: Merupakan nama dari grup pengguna tersebut.
2. **Kata Sandi**: Biasanya digunakan untuk menyimpan kata sandi yang telah dienkripsi. Namun, dalam praktiknya, kata sandi grup jarang digunakan dan sering dibiarkan kosong atau diisi dengan tanda "x".
3. **ID Grup**: Merupakan identifikasi numerik unik untuk grup tersebut.
4. **Daftar Anggota**: Merupakan daftar pengguna yang tergabung dalam grup tersebut, dipisahkan oleh koma.

Contoh entri dalam file "/etc/group":

```
users:x:100:john,mary
```

- Nama Grup: `users`
- Kata Sandi: `x` (biasanya kosong atau diisi dengan "x")
- ID Grup: `100`
- Daftar Anggota: `john,mary`

File "/etc/group" digunakan oleh sistem untuk mengelola izin akses dan hak penggunaan atas file dan direktori yang ada dalam sistem. Dengan menggunakan grup, administrator sistem dapat mengatur hak akses secara lebih terorganisir dan memudahkan manajemen pengguna dan hak aksesnya.

### Jelaskan perbedaan penggunaan perintah "su" dengan "su -"!

Perintah "su" dan "su -" digunakan untuk beralih (switch) ke pengguna (user) lain pada sistem Linux atau Unix. Namun, keduanya memiliki perbedaan dalam cara mereka menjalankan shell dan mengatur lingkungan saat beralih ke pengguna lain. Berikut adalah penjelasan perbedaannya:

1. **su**:
   - Perintah "su" (singkat dari "switch user") digunakan untuk beralih ke pengguna lain tanpa mengubah lingkungan shell atau direktori kerja saat ini.
   - Ketika menggunakan "su", Anda hanya memasukkan nama pengguna yang ingin Anda beralih, dan tidak memerlukan tanda hubung (-) setelahnya.
   - Contoh penggunaan: `su username`

2. **su -**:
   - Perintah "su -" (atau "su -l", singkat dari "switch user and login shell") digunakan untuk beralih ke pengguna lain dan menjalankan shell dengan lingkungan yang sepenuhnya baru, termasuk direktori kerja dan variabel lingkungan yang diatur ulang sesuai dengan pengguna baru.
   - Ketika menggunakan "su -", tanda hubung (-) menandakan untuk menjalankan shell dengan lingkungan yang baru.
   - Perintah ini berguna ketika Anda ingin masuk ke sesi shell baru sebagai pengguna lain, sehingga semua pengaturan lingkungan, seperti PATH atau variabel lingkungan lainnya, diatur ulang sesuai dengan pengguna baru.
   - Contoh penggunaan: `su - username`

Dengan menggunakan "su -", pengguna dapat membuat lingkungan shell yang sama seperti saat pengguna tersebut masuk secara langsung ke sistem, sementara "su" hanya beralih pengguna tanpa mengubah lingkungan shell saat ini.

### Jelaskan fungsi dari "sudo" !

"Sudo" adalah perintah yang digunakan dalam sistem operasi Linux dan Unix untuk memberikan akses ke perintah yang memerlukan izin administratif (biasanya dijalankan oleh pengguna root) kepada pengguna biasa. Kata "sudo" sendiri merupakan singkatan dari "superuser do".

Fungsi utama dari "sudo" adalah memberikan pengguna tertentu hak istimewa untuk menjalankan perintah dengan hak akses root atau izin administratif tertentu, tanpa perlu masuk sebagai pengguna root secara langsung. Hal ini membantu meningkatkan keamanan sistem dengan membatasi akses root hanya kepada pengguna yang membutuhkannya, sementara mempertahankan kontrol atas tindakan yang dilakukan oleh pengguna tersebut.

Beberapa fungsi "sudo" meliputi:

1. **Izin Administratif**: "Sudo" memungkinkan pengguna untuk menjalankan perintah dengan izin administratif tertentu yang biasanya hanya tersedia untuk pengguna root.

2. **Audit Log**: Sudo mencatat setiap penggunaan yang berhasil dan gagal dari perintah sudo dalam log audit, yang memungkinkan administrator untuk melacak dan menganalisis aktivitas pengguna.

3. **Kontrol Akses**: Administrator dapat mengonfigurasi file konfigurasi sudo (biasanya "/etc/sudoers") untuk mengatur akses mana yang diberikan kepada pengguna tertentu, termasuk perintah spesifik mana yang diizinkan dan apa yang diizinkan dalam perintah tersebut.

4. **Privilege Escalation**: Pengguna biasa dapat menggunakan "sudo" untuk sementara meningkatkan hak akses mereka untuk menjalankan perintah yang memerlukan izin administratif, seperti instalasi perangkat lunak atau pengelolaan konfigurasi sistem.

5. **Security**: Dengan menggunakan "sudo", administrator sistem dapat membatasi akses root hanya kepada pengguna yang membutuhkannya, sehingga meminimalkan risiko kesalahan atau penyalahgunaan yang mungkin terjadi.

"Sudo" adalah alat yang sangat penting dalam administrasi sistem Linux yang membantu dalam menjaga keamanan dan integritas sistem dengan memberikan kontrol yang lebih baik atas hak akses administratif.

### Jelaskan langkah-langkah penambahan user anda sebagai user sudo ! Gunakan perintah "su -" lalu setelah masuk sebagai root, jalankan perintah "visudo". Tambahkan user anda di bawah user root pada bagian " # User privilege specification"

Berikut adalah langkah-langkah untuk menambahkan pengguna Anda sebagai pengguna sudo:

1. Masuk sebagai pengguna root dengan perintah `su -`:
   ```
   su -
   ```

2. Setelah masuk sebagai root, jalankan perintah `visudo` untuk mengedit file konfigurasi sudoers:
   ```
   visudo
   ```

3. Di dalam editor yang terbuka, cari bagian yang berjudul "User privilege specification" atau "# User privilege specification".

4. Di bawah baris yang menyatakan izin untuk pengguna root, tambahkan baris baru untuk menambahkan pengguna Anda. Baris tersebut harus memiliki format seperti ini:
   ```
   nama_pengguna ALL=(ALL:ALL) ALL
   ```
   Di mana "nama_pengguna" adalah nama pengguna Anda.

   Misalnya, jika nama pengguna Anda adalah "rizal", baris yang ditambahkan akan terlihat seperti ini:
   ```
   rizal ALL=(ALL:ALL) ALL
   ```
![](./assets/22.png)
5. Setelah menambahkan baris baru, simpan perubahan dengan menekan tombol `Ctrl + X`, lalu ketik `Y` untuk mengonfirmasi penyimpanan, dan tekan Enter.

6. Setelah menyimpan, Anda dapat keluar dari editor dan kembali ke shell root.

Dengan langkah-langkah di atas, Anda telah menambahkan pengguna Anda sebagai pengguna sudo, yang berarti pengguna tersebut memiliki izin untuk menjalankan perintah sebagai superuser atau root menggunakan perintah "sudo". Pastikan untuk menjaga keamanan akses sudoers dan hanya memberikan akses tersebut kepada pengguna yang dapat dipercaya.
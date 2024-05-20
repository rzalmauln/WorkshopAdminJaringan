    NRP   : 3122600004
    Nama  : Rizal Maulana
    Kelas : 2 D4 IT A
    Dosen : Dr. Ferry Astika Saputra, ST, M.Sc

## Docker 101 Tutorial Playground

Tutorial dalam membangun sebuah container untuk aplikasi sederhana

1. kunjungi website https://www.docker.com/101-tutorial/, kemudian login dan masuk ke link play with docker https://labs.play-with-docker.com/

2. jalankan kode berikut 
![](assets/1.png)

3. akan muncul akses tutorial seperti ini di port 80
![](assets/2.png)

4. kemudian download file yang ada di tutorial
![](assets/3.png)

5. kemudian drag and drop ke labs play-with-docker, lalu coba klik editor jika berhasil maka terdapat file app.zip 
![](assets/4.png)

6. kemudian unzip file zip 
![](assets/5.png)

7. kemudian bisa lakukan pengecekan
![](assets/6.png)

8. selanjutnya jika sudah berhasil kalian buat Dockerfile seperti ini 
![](assets/7.png)
![](assets/8.png)

9. setelah disimpan kemudian jalankan dockernya
![](assets/9.png)

10. kalian bisa akses aplikasi todo list sederhana ini di port 3000
![](assets/10.png)

11. kemudian kita coba lakukan perubahan di file app/src/static/js/app.js,
![](assets/11.png)
kemudian lakukan perubahan html
![](assets/12.png)
dan jalankan kembali 
![](assets/13.png)
pasti akan terjadi error seperti dibawah karena sejatinya service kita sebenarnya belum terupdate sepenuhnya
![](assets/14.png)

12. jalankan kode dibawah untuk mendapatkan container id
![](assets/15.png)
jalankan kode docker stop
![](assets/16.png)
jalankan kode docker rm
![](assets/17.png)
dari sini service container kita bisa sepenuhnya terupdate dengan menjalankan kode yang sama seperti diatas 
![](assets/18.png)

13. kemudian pergi ke docker hub untuk membuat sebuah repo, beri nama sesuai tutorial
![](assets/19.png)

14. kemudian kembali ke terminal lakukan login dan push ke repo
![](assets/20.png)
![](assets/21.png)

15. kemudian buat new instance di terminal pwd dan jalankan image yang tadi sudah dipush ke repo
![](assets/22.png)
![](assets/23.png)

16. ini hasilnya jika berhasil
![](assets/24.png)

17. lakukan kode dibawah ini
![](assets/25.png)![](assets/26.png)![](assets/27.png)

18. membuat sebuah volume guna tetap menyimpan data jika image terhapus
![](assets/27.1.png)
![](assets/28.png)
![](assets/29.png)
![](assets/30.png)
![](assets/29.png)

19. jika ingin melihat detail volume yang sudah dibuat dengan kode dibawah ini
![](assets/31.png)

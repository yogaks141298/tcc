Yoga Kurnia Subekti  
175410033  
#

## Fork
Fork adalah membuat clone dari suatu repo di GitHub milik upstream author, diletakkan ke milik kontributor. Fork hanya dilakukan sekali saja. Pada dasarnya, proses untuk fork ini meliputi:

Fork repo di web GitHub.
Clone fork tersebut di komputer lokal.
Kontributor harus mem-fork repo upstream author sehingga di repo kontributor muncul repo tersebut. Proses forking ini dijelaskan dengan langkah-langkah berikut:

1. Login ke GitHub https://github.com/yogaks141298/belajarfork
    ![1](image/1.PNG)
2. telah proses, repo dari upstream author sudah berada di account GitHub kita (kontributor)
![2](image/2.PNG)

Setelah itu, konfigurasikan repo lokal kontributor. Pada kondisi saat ini, di komputer lokal sudah terdapat repo playground-1 yang berada pada direktori dengan nama yang sama. Untuk keperluan berkontribusi, ada 2 nama repo yang harus diatur:

1. origin: menunjuk ke repo milik kontributor di GitHub, hasil dari fork.
2. upstream: menunjuk ke repo milik upstream author (repo asli) di account oldstager.  

Repo origin sudah dituliskan konfigurasinya pada saat melakukan proses clone dari repo kontributor. Konfigurasi repo upstream harus dibuat.
![3](image/3.PNG)
Tambahkan remote upstream:
$ git remote add upstream https://github.com/yogaks141298/belajarfork.git

Hasil:

        $ git remote -v  
        origin  https://github.com/edipermadi99/belajarfork.git (fetch)  
        origin  https://github.com/edipermadi99/belajarfork.git (push)  
        upstream https://github.com/yogaks141298/belajarfork.git (fetch)  
        upstream https://github.com/yogaks141298/belajarfork.git (push)  
        $
## Mengirimkan Pull Request
Setiap kali melakukan perubahan, kirim perubahan tersebut. Pengiriman ini disebut dengan Pull Request. Pada posisi ini, kontributor bisa mengirimkan kontribusi dengan cara mengirimkan pull request (PR) ke upstream author. Secara umum, langkah-langkahnya adalah sebagai berikut:

1. Kontributor akan bekerja di repo lokal (create, update, delete isi)
2. Commit
3. Push ke repo kontributor
4. Kirimkan PR ke repo upstream author.
5. Upstream author me-review dan kemudian menyetujui (merge) ke master atau menolak PR.
6. Jika disetujui dan di-merge ke repo master dari upstream author, sinkronkan repo di komputer lokal dan repo GitHub kontributor.
Berikut ini adalah contoh pengiriman perubahan isi README.md dengan menambahkan kontributor.

## Membuat Perubahan di Repo Lokal
Sebelum melakukan perubahan, pastikan:
1. Sudah ada koordinasi secara manual tentang perubahan-perubahan yang akan dilakukan.
2. Setelah melakukan perubahan-perubahan, pastikan bahwa isi repo lokal tersinkronisasi dengan repo dari upstream author.
3. Cara melakukan sinkronisasi:
        $ git fetch upstream
        From https://github.com/yogaks141298/belajarfork  
        * [new branch]      master     -> upstream/master
4. Lakukan perubahan-perubahan, setelah itu push ke origin (milik kontributor)
![4](image/4.PNG)

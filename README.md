Nama : Imam Taftazani Ridanif

Kelas : TI.20.A2

Nim : 312010307

# PENGGUNAAN GIT

## APA ITU GIT?

* Git adalah salah satu sistem pengontrol versi (Version ControlSystem) pada proyek perangkat lunak yang diciptakan oleh Linux Torvalds.
* Pengontrol versi bertugas mencatat setiap perubahan pada fileproyek yang dikerjakan oleh banyak orang maupun sendiri.
* Git dikenal juga dengan distributed revision control (VCS terdistribusi),artinya penyimpanan database Git tidak hanya berada dalam satutempat saja.

## INSTALASI GIT
* Download **Git**, buka website resminya Git `(git-scm.com)`.
* Kemudian unduh Git sesuai dengan arsitektur komputer kita. Kalau menggunakan 64bit, unduh yang 64bit. Begitu juga kalau menggunakan 32bit.
* Selamat, Git sudah terinstal di Windows. Untuk mencobanya,silahkan buka **CMD** atau **PowerShell**, kemudian ketik perintah
``git --version``

![13](https://user-images.githubusercontent.com/72736958/96374711-804d8100-119e-11eb-8c56-9781b5934545.PNG)

## Menambahkan Global Config
* Pada saat pertama kali menggunakan git, perlu dilakukan konfigurasi ``user.name dan user.email``
* konfigurasi ini bisa dilakukan untuk global repostiry atau individual repository.
* apabila belum dilakukan konfigurasi, akan mengakibatkan terjadi kegagalan saat menjalankan perintah `git commit`
* Config Global Repository
`$ git config --global user.name “nama_user"`
`$ git config --global user.email “nama_user”`

![14](https://user-images.githubusercontent.com/72736958/96374716-91968d80-119e-11eb-858e-7cdd74567a04.PNG)

## Perintah Dasar Git
* `git init`, perintah untuk membuat repository local
* `git add`, perintah untuk menambahkan file baru, atau perubahan pada file pada staging sebelum proses commit.
* `git commit`, perintah untuk menyimpan perubahan kedalam database git.
* `git push -u origin master`, perintah untuk mengirim perubahan pada repository local menuju server repository.
* `git clone [url]`, perintah untuk membuat working directory yang diambil dari repositry sever.
* `git remote add origin [url]`, perintah untuk menambahkan remote server/reopsitory server pada local repositry ``(working directory)``
* `git pull`, perintah untuk mengambil/mendownload perubahan terbaru dari server repository ke local repository

## Membuat Reposiory Local
* Buka direktory aktif, misal: **d:\labs_pemrograman1** (buka menggunakan Windows Explorer)
* klik kanan pada direktory aktif tersebut, dan pilih menu **Git Bash**, sehingga muncul git bash commad
* Buat direktory project praktikum pertama dengan nama **latihan1**
``$ mkdir latihan1
$ cd latihan1``
* Sehingga terbentuk satu direktori baru dibawahnya, selanjutnya masuk kedalam direktori tersebut dengan perintah **cd** ``(change directory)``
* direktory aktif menjadi: **d:\labs_pemrograman1\latihan1

![11](https://user-images.githubusercontent.com/72736958/96374318-38c5f580-119c-11eb-8001-2e8ee1ebfa8b.PNG)

## Membuat Reposiory Local
* Jalankan perintah **git init**, untuk membuat repository local.
`$ git init`
* Repository baru berhasil di inisialisasi, dengan terbentuknya satu direktori hidden dengan nama .**git**
* Pada direktori tersebut, semua perubahan pada `working directory` akan disimpan.

![10](https://user-images.githubusercontent.com/72736958/96374311-2ea3f700-119c-11eb-82dd-fe33fbdcc7cf.PNG)

## Menambahkan File baru pada repository
* Untuk membuat file dapat menggunakan text editor, lalu menyimpan filenya pada direktori aktif (repository)
* disini kita akan coba buat satu file bernama README.md (text file)
`$ echo “# Latihan 1” >> README.md`
* File **README.md** berhasil dibuat.

![7](https://user-images.githubusercontent.com/72736958/96373743-abcd6d00-1198-11eb-9b8a-e1bd94c9945d.PNG)

## Menambahkan File baru pada repository
* Untuk menambahkan file yang baru saja dibuat tersebut gunakan perintah git add.
`$ git add README.md`
* File **README.md** berhasil ditambahkan.



## `Commit` (Menyimpan perubahan ke database)
* Untuk menyimpan perubahan yang ada kedalam database repository local, gunakan perintah git commit -m “komentar commit”
`$ git commit -m “File pertama saya”`
* Perubahan berhasil disimpan.

![6](https://user-images.githubusercontent.com/72736958/96373733-99533380-1198-11eb-856c-138db676d59d.PNG)

## Membuat repository server
* Server reopsitory yang akan kita gunakan adalah (http://github.com)
* Anda harus membuat akun terlebih dahulu.
* Pada laman github, klik tombol start a project, atau
* Dari menu (icon +) klik New Repository



* Isi nama repositorynya, misal: labpy1.
* lalu klik tombol Create repository

## Menambahkan Remote Repository
* Remote Repository merupakan repository server yang akan digunakan untuk menyimpan setiap perubahan pada local repository, sehingga dapat diakses oleh banyak user.
* Untuk menambahkan remote repository server, gunakan perintah **git remote add origin [url]**
`$ git remote add origin https://github.com/imamtaftazani/latihanVCS.git`

![5](https://user-images.githubusercontent.com/72736958/96373716-83457300-1198-11eb-9fff-6286da029d1e.PNG)

## Push (Mengirim perubahan ke server)
* Untuk mengirim perubahan pada local repository ke server gunakan perintah git push.
`$ git push -u origin master`
* Perintah ini akan meminta memasukkan username dan password pada akun github.com

![12](https://user-images.githubusercontent.com/72736958/96374322-42e7f400-119c-11eb-861d-fc37ec3ce6e9.PNG)

## Melihat hasilnya pada server repository
* Buka laman github.com, arahkan pada repositorinya.
* Maka perubahan akan terlihat pada laman tersebut.



## Clone Repository
* Clone repository, pada dasarnya adalah meng-copy repository server dan secara otomatis membuat satu direktory sesuai dengan nama repositorynya (working directory).
* Untuk melakukan cloning, gunakan perintah `git clone [url]`

![15](https://user-images.githubusercontent.com/72736958/96374991-6ca31a00-11a0-11eb-9204-9004f46d2a0a.PNG)

## Kegunaan file README.md
* Apabila kita menggunakan github, untuk memberikan penjelasan awal pada project yang kita buat, maka dapat menggunakan sebuah file yang bernama README.md
* Pada file tersebut kita dapat membuat dokumentasi awal dari setiap project yang kita buat untuk memberikan penjelasan atau sekedar cara penggunaan dari aplikasi yang kita kembangkan.
* Penulisan file README.md berbasis teks, dan untuk pemformatannya menggunakan Markdown format.
* untuk lebih jelasnya, dapat anda pelajari cara penggunaan markdown pada url berikut: https://guides.github.com/features/mastering-markdown/





### Author : Imam Taftazani Ridanif


![animasi-bergerak-komputer-0116](https://user-images.githubusercontent.com/72736958/96375090-269a8600-11a1-11eb-9cde-74d5fa08d6e2.gif)

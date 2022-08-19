# Agenda
1. Pengenalan Version Control
2. Pengenalan Git
3. Repository
4. The Three Tree
5. Working Directory
6. Staging Index
7. Commit
8. Reset Commit
9. Dan lain-lain

# Sebelum Ada Version Control System
1. Saat kita mengerjakan pekerjaan, kita sering sekali melakukan revisi. Misal saja kita membuat dokumen proposal atau skripsi.
2. Biasanya kita akan simpan dokumen pertama dengan nama document_1, setelah mendapat revisi, kita akan simpan dengan nama document_2, jika masih ada reivisi, kita akan simpan dengan nama document_3, dan seterusnya.
3. Kenapa kita lakukan hal tersebut? Agar kita bisa menegtahui perubahan yang terjadi antar ervisi document, dan jika sewaktu-waku kita perlu menggunakan revisi yang sebelumnya, kita bisa menggunakannya dengan mudah.

# Version Control System
1. Version Control adalah sebuah system yang merekam perubahan pada file dari waktu ke waktu, sehingga kita bisa melihat versi sebelumnya jika diinginkan.
2. Version Control sangat populer dikalangan programmer, karena programmer selalu membuat kode program dalam bentuk kode tulisa. Dengan version control, programmer bisa merekam semua perubahan yang terjadi, sehingga jika terjadi kesalalhan, programmer bisa dengan mudah kembali ke versi sebelumnya.
3. Tapi tidak hanya untuk file dalam bentuk text, jika misal kita adalah seorang Grapic Designer, kita juga biisa memanfaatkan Version Control untuk merekam perubahan dari file gambar atau layput, sehingga kita tidak perlu membackup tiap perubahan secara manual.

# Tipe Version Control
1. Secara garis besar, version control dibagi menjadi 3 jenis :
> Local Version Control,
> Centralized Version Control, dan
> Distributed Version Control

# Local Version Control
1. Local version control merupakan version control yang berjalan hanya di local komputer.
2. Pendekatan ini biasa digunakan karena sederhana dan tidak buth server, karena semua riwayat pekerjaan disimpan di local komputer.
3. Setiap perubahan versi yang terjadi pada file hanya disimpan di local komputer.

## Diagram Local Version Control

# Centralized Version Control
1. Masalah yang terjadi pada Local Version Control adalah, jika komputer rusak, maka seluruh data bisa hilang.
2. Selain itu agak sulit untuk berkolaborasi dengan pengguna lain Centralized Version Control.
3. Crealized Version Control menyimpan seluruh data revisi di Server.
4. Pengguna bisa mengakses data ke Server untuk melihat file.
5. Kekurangannya adalah, jika pengguna offlien, mereka tidak bisa melihat riwayat file karena semua riwayat hanya ada di Server.
6. Jika Server down, maka seluruh pengguna tidak bisa melakukan perubahan dan mmelihat revisi file.
7. Contoh Centralized Version Control adalah Subversion.

## Diagram Centralized Version Control

# Distributed Version Control
1. Distributed Version Control adalah alternatif lain dari Centralized Version Control.
2. Dalam DVCs, client tidak hanya mengambil file versi terakhir, namun seluruh riwayat revisi di copy seluruhnya.
3. Hal ini menjadikan jika terjadi masalah dengan Server, client masih tetap bekerja, memanipulasi file, sampai melihat riwayat perubahan.
4. Bahkan dalam DVCs, Server bisa lebih dari satu, karena tiap server isinya sama, full backup data.
5. Contoh DVCs adalah Git, Mercurial dan lain-lain.

## Diagram Crentralized Version Control

# Distributed Version Control
1. Distributed Version Control adalah alternatif lain dari Centralized Version Control.
2. Dalam DVCs, Client tidak hanya mengambil file versi terakhir, namun seluruh riwayat revisi di copy seluruhnya.
3. Hal ini menjadikan jika terjadi masalah dengan Server, client masih tetap bekerja, memanipulasi file, sampai melihat riwayat perubahan.
4. Bahkan dalam DVCs, Server bisa lebih dari satu, karena tiap server isinya sama, full backup data.
5. Control DVCs adalah Git, Mecurial dan lain-lain

## Diagram Distributed Version Control.

# Sejarah Git 
1. Git muncul dengan latar belakang OpenSource project Linux Kerne.
2. Tahun 1991-2002, Linux Kernel di develop hanya dengan memanfaatkan patch dan archived files
3. Tahun 2002, Linux Kernel mulai menggunakan DVCs bernama BitKeeper
4. Di tahun 2005, hubungan antara perusahaan pemilik BitKeeper dengan komunitas Linux Kerner kurang baik, sehingga pembuat Linux, Linus Torvalds mulai membuat DVCs sendiri.
5. Git Pertama kali diperkenalkan tahun 2005, semakin kesini Git semakin populer dan sekarang menjadi DVCs yang paling populer di dunia.
6. Git sangat cepat, ringan dan baik dalam me-manage projext dengan ukuran besar.

# Pengenalan Git
1. Jadi, Git adalah salah satu DVCs yang ada.
2. Git tidak membutuhkan server untuk melakukan perubahan atau melihat riwayat revisi, hal ini dikarenakan dalam Git, semua riwayat project akan selalu di duplikat, baik itu di server ataupun di local komputer.
3. Artinya sebenarnya Git juga bisa digunakan sebagai Local Version Control.
4. Setiap perubahan yang terjadi di Git akan selalu dibuat signature (tanda) nya menggunakan algoritma hashing SHA-1. Hal ini menjadikan perubahan sekecil apapun pasti bisa dideteksi oleh git.
5. Semua hal yang terjadi di git secara otomatis akan di catat, hal ini menjadikan perubahan apapun di Git, pasti selalu bisa dikembalikan ke versi sebelumnya.

# Memastikan Git Berjalan
1. Git merupakan aplikasi berbasis terminal/command line, oleh karena itu, untuk menggunakan Git, kita perlu membuat terminal/command line.
2. Untuk mengecek versi Git yang terinstall di local komputer kita, kita bisa gunakan perintah: git --version

# Repository
1. Repository merupakan sebutan project di Git.
2. Kita bisa membuat folder kosong atau folder yang sudah berisi file, lalu membuatnya sebagai Git Repository.
3. Atau kita bisa melakukan clone Git Repository yang sudah ada dari Server Git.

## Kode : Git Init (Gambar)

## Praktek (gambar)

## Kode : Git Status (Gambar)

## Praktek (gambar)

# The Three States
1. Harap diperhatikan, ini adalah hal utama yang wjib dimengerti di Git agar selanjutannya bisa mengerti dengan baik.
2. Git memiliki tiga state terhadap file kita: modified, staged, dan committed.
3. Modified artinya kita mengubah(menambah, mengedit, menghapus) file, namun belum disimpan secara permanen ke repository.
4. Staged artinya kita menandai modifikasi yang kita lakukan terhadap file akan disimpan secara permanen ke repository.
5. Committed artinya data sudah aman disimpan di repository.

# Three Selection
1. Tiga state sebelumnya di dalam Git dilakukan di section yang berbeda-beda, yaitu Working Directory, Staging Area dan Repository.
2. Saat kita melakukan modifikasi file, itu dilakukan di working directory.
3. Staging Area merupakan section dimana file sudah disiapkan untuk disimpan secara permanen, di Staging Area semua informasi perubahan file akan disimpan.
4. Repository merupakan tempat dimana semua file dan database riwayat  versi file disimpan.

## Diagram Three Tree (Gambar)

# Workflow
1. Sekarang kita sudah tahu tentang arsitektur Three Tree, sekarang pertanyaannya, bagaimana alur kerja menggunakan Git.
2. Secara sederhaa, setiap perubahan akan kita lakukan di working directory.
3. Jikka ada yang mau kita siapkan untuk disimpan secara permanen, kita akan bawa perubahan tersebut ke staging index.
4. Selanjutnya, kita bisa melakukan penyimpanan versi baru secara permanen ke repository.

# Snapshot
1. Pada materi sebelumnya kita selalu menyebutkan versi pada perubahan file.
2. Sebenarnya perubahan yang dilakukan bisa jadi dilakukan secara bersaman untuk beberapa file, hal ini berarti sebenarnya tidak ada yang namanya versi file, hal ini berarti sebenarnya tidak ada yang namanya versi file.
3. Semua perubahan yang terjadi akan diremakn, dan kita sebut namanya adalah snapshot.
4. Snapshot berisikan semua perubahan yang terjadi disemua file yang kita commit.
5. Setiap snapshot akan menghasilkan has.

# Hash




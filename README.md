##### ```Anggota Tim:```
##### 1. Sarah Al Qibthiyyah ~ G64140017
##### 2. Widia Sereniti ~ G64140051
##### 3. Rachel ~ G64140092
 
# "Cloud Computing"
![N|Solid](https://3.bp.blogspot.com/-MNau1n1R45Q/V9BA_xR1L5I/AAAAAAAABqA/23Whp_hR3u09g8O-qbPmUkSu5mO-do1LQCLcB/s1600/clou8d.png)
 
## Sekilas Tentang
OwnCloud adalah sebuah paket perangkat lunak client-server untuk menciptakan layanan file hosting. Secara fungsional, OwnCloud sangat mirip dengan Dropbox, namun OwnCloud memungkinkan orang untuk menginstal dan mengoperasikan tanpa biaya pada server pribadi.  Kita dapat menyimpan file, folder, kontak, audio, galeri foto, kalender, dan dokumen lainnya serta dapat mengakses dimana saja dan kapan saja.
 
## Instalasi
- Requirement awal pada instalasi OwnCloud pada Windows adalah membuat SSH dengan menggunakan PuTTy [Download Putty](http://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html).
- Mula-mula install aplikasi di bawah ini :
    | No. | Yang Harus diinstal |
    | ------ | ------ |
    | 1 | apache2|
    | 2 | mysql-server |
    | 3 | php |
    | 4 | libapache2-mod-php |
    | 5 | php-mysql |
    | 6 | php-gd php-mcrypt php-mbstring php-xml php-ssh2 |
    | 7 | php-curl |
    | 8 | unzip |
    | 9 | phpmyadmin (opsional)|
   
- Langkah instalasi Requirement awal dalam CLI.
     ## Step 1 OwnCloud Installation
    ```sh
    $ sudo curl https://download.owncloud.org/download/repositories/stable/Ubuntu_16.04/Release.key | sudo apt-key add –
    ```
    ```sh
    $ echo 'deb https://download.owncloud.org/download/repositories/stable/Ubuntu_16.04/ /' | sudo tee /etc/apt/sources.list.d/owncloud.list
     ```
     ```sh
    $ sudo apt-get update
    $ sudo apt-get install owncloud
    $ sudo systemctl reload apache2
    ```
    ## Step 2 MySQL Database Configuration
    ```sh
    $ mysql -u root -p
    mysql > CREATE DATABASE owncloud;
    mysql > GRANT ALL ON owncloud.* to 'owncloud'@'localhost' IDENTIFIED BY 'set_database_password';
    mysql > FLUSH PRIVILEGES;
    mysql exit;              #keluar dari perintah mysql database
    ```
   
    ## Step 3 OwnCloud Configuration
    ```sh
    https://server_domain_or_IP/owncloud
    ```
## Maintenance (opsional)
- Menghapus data yang tidak diperlukan secara berkala
- Melakukan back up data ke user lain

## Otomatisasi
Skrip shell untuk otomatisasi instalasi, konfigurasi, dan maintenance.

## Cara Pemakaian

Tampilan aplikasi web
Fungsi-fungsi utama
Isi dengan data real/dummy (jangan kosongan) dan sertakan beberapa screenshot
## Pembahasan
- 
- Kelebihan
1.Memungkinkan antar karyawan untuk berkirim file antar grup mapun personal.
2.Singkronisasi file kapan saja (real time) dengan berbagai device.
3.Upload data yang tidak dibatasi selama kapasitas hardisk server data mencukupi.
4.Jumlah pengguna yang bisa bergabung tidak terbatas.
5.Adanya Kalender dan Pengingat Tugas.
6.Adanya fitur Preview Dokumen.
7.Adanya fitur Galeri Photo dan Video.
8.Pengembangan yang luas karena disupport oleh berbagai plugin tambahan.

- Kekurangan
1.Masalah keamanan.
2.Adanya ganguan pada saat mengakses data, entah disebabkan oleh koneksi yang bermasalah, server yang sedang ‘down’.
3.Tidak bisa melakukan register, hanya admin yang dapat melakukan register terhadap user lain.
4.Tidak bisa diakses secara offline.

- Perbandingan OwnCloud dengan aplikasi GitLab
## Referensi

## Referensi
- Install Vanilla Forums on Ubuntu 16.04 | https://www.1and1.co.uk/cloud-community/learn/application/misc/install-vanilla-forums-on-ubuntu-1604/
- PHPmyadmin Documentation | https://help.ubuntu.com/lts/serverguide/phpmyadmin.html
- Vanilla Forums Open Source Theme | https://open.vanillaforums.com/addon/browse/themes/
- Vanilla Forums Help | https://open.vanillaforums.com/discussion/12702/could-not-instantiate-mail-function
- PHP Curl Instalation | http://stackoverflow.com/questions/33775897/how-do-i-install-the-ext-curl-extension-with-php-7
- Vanilla Forum Reviews 2016 | https://www.comparakeet.com/forum-software/vanilla-forums-review/
kilas Tentang OwnCloud adalah sebuah paket perangkat lunak client-server untuk menciptakan layanan file hosting. Secara fungsional, OwnCloud sangat mirip dengan Dropbox, namun OwnCloud memungkinkan orang untuk menginstal dan mengoperasikan tanpa biaya pada server pribadi. Kita dapat menyimpan file, folder, kontak, audio, galeri foto, kalender, dan dokumen lainnya serta dapat mengakses dimana saja dan kapan saja. ## Instalasi - Requirement awal pada instalasi Vanilla Forum mirip seperti pada proses intalasi Wordpress pada praktikum 1 berikut requirement yang diperlukan : | No. | Yang Harus diinstal | | ------ | ------ | | 1 | apache2| | 2 | mysql-server | | 3 | php | | 4 | libapache2-mod-php | | 5 | php-mysql | | 6 | php-gd php-mcrypt php-mbstring php-xml php-ssh2 | |

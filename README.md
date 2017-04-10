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

![N|Solid](https://scontent-sit4-1.xx.fbcdn.net/v/t1.0-9/17796149_1280047775414195_1748431531079642747_n.jpg?oh=5f95b1969dc85a134c33fa953d953932&oe=5955051B)
   
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
```
Usage:
 command [options] [arguments]

Options:
 -h, --help            Display this help message
 -q, --quiet           Do not output any message
 -V, --version         Display this application version
     --ansi            Force ANSI output
     --no-ansi         Disable ANSI output
 -n, --no-interaction  Do not ask any interactive question
     --no-warnings     Skip global warnings, show command output only
 -v|vv|vvv, --verbose  Increase the verbosity of messages: 1 for normal output,
                       2 for more verbose output and 3 for debug

Available commands:
 check                 check dependencies of the server
                       environment
 help                  Displays help for a command
 list                  Lists commands
 status                show some status information
 upgrade               run upgrade routines after installation of
                       a new release. The release has to be
                       installed before.
```
```
Usage:
 maintenance:mode [options]

Options:
     --on              enable maintenance mode
     --off             disable maintenance mode
 -h, --help            Display this help message
 -q, --quiet           Do not output any message
 -V, --version         Display this application version
     --ansi            Force ANSI output
     --no-ansi         Disable ANSI output
 -n, --no-interaction  Do not ask any interactive question
     --no-warnings     Skip global warnings, show command output only
 -v|vv|vvv, --verbose  Increase the verbosity of messages: 1 for normal output,
                       2 for more verbose output and 3 for debug
```

## Cara Pemakaian

Tampilan aplikasi web
Fungsi-fungsi utama
Isi dengan data real/dummy (jangan kosongan) dan sertakan beberapa screenshot

![N|Solid](https://scontent-sit4-1.xx.fbcdn.net/v/t1.0-9/17634345_1280061972079442_3785126364327019108_n.jpg?oh=9886bab52e4088a40d55fc401db57d5e&oe=5964EE68)
![N|Solid](https://scontent-sit4-1.xx.fbcdn.net/v/t1.0-9/17760164_1280061925412780_6347901786084891445_n.jpg?oh=5c7ec7bf6d31108a32cfae8c6c2e8c80&oe=59562EC4)
![N|Solid](http://i.imgur.com/aMc5OCh.png)
![N|Solid](http://i.imgur.com/7uyllHd.png)
![N|Solid](http://i.imgur.com/iPtmo0t.png)
![N|Solid](http://i.imgur.com/Ux201Ju.png)

## Pembahasan
- Kelebihan
  - Memungkinkan antar karyawan untuk berkirim file antar grup mapun personal.
  - Singkronisasi file kapan saja (real time) dengan berbagai device.
  - Upload data yang tidak dibatasi selama kapasitas hardisk server data mencukupi.
  - Jumlah pengguna yang bisa bergabung tidak terbatas.
  - Adanya Kalender dan Pengingat Tugas.
  - Adanya fitur Preview Dokumen.
  - Adanya fitur Galeri Photo dan Video.
  - Pengembangan yang luas karena disupport oleh berbagai plugin tambahan.

- Kekurangan
  - Adanya ganguan pada saat mengakses data, entah disebabkan oleh koneksi yang bermasalah, server yang sedang ‘down’.
  - Tidak bisa melakukan register, hanya admin yang dapat melakukan register terhadap user lain.
  - Tidak bisa diakses secara offline.

- Perbandingan OwnCloud dengan aplikasi GitLab
  - Owncloud: dapat menyimpan file, kontak, foto, kalender dan lain-lain pada server pilihan kita dan data dapat diakses melalui mobile device, desktop, atau web browser kapanpun dan dimanapun. Gitlab: hanya dapat menympan file berupa code data hanya dapat diakses melalui desktop. Data yang tersimpan dapat dienkripsi untuk keamanan.
  - Owncloud: Dapat menyimpan data secara langsung (drag and drop) melalui browser tanpa harus meng-install owncloud client. Gitlab: Untuk menyimpan data perlu melakukan skrip push ke git.
  - Owncloud: Dapat mengatur tampilan tema sesuai keinginan kita. Gitlab: Tidak dapat mengatur tampilan tema.
  - Owncloud: Dapat mengatur task, atau list yang harus dilakukan. Gitlab: Tidak memiliki fitur task, atau list yang harus dilakukan.
  - Owncloud: Hanya dapat berbagi data ke user lain. Gitlab: Dapat memberi peran berbeda kepada 5 user berbeda.
  - Owncloud: Dapat mengakses data dari google drive atau dropbox melalui owncloud. Gitlab: Tidak dapat mengakses data dari luar Gitlab.

## Referensi
- Deskripsi OwnCloud | https://en.wikipedia.org/wiki/OwnCloud
- Kelebihan OwnCloud | http://www.chip.co.id/chipversity/general/16346/owncloud_solusi_sharing_file_dengan_teknologi_private_cloud_storage
- Langkah Instalasi | https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-owncloud-on-ubuntu-16-04
- Otomasisasi | https://doc.owncloud.org/server/9.0/admin_manual/configuration_server/occ_command.html

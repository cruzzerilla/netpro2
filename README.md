## Anggota
1. Aditya Eka Bagaskara (1301164222)
2. Ilham Ibnu Purnomo (1301164089)
3. Adisca Naufal Ristanto(1301164358)

## Soal No 1

1. Kami membuat server ini untuk diterapkan pada sebuah startup atau perusahaan yang menginginkan dapat berkomunikasi antar pegawai, menyimpan data perusahaan, serta sharing data antar pegawai pada perusahaan tersebut. Setelah diterapkan server ini pada perusahaan, diharapkan perusahaan tersebut akan lebih mudah dalam pengelolaan data.

2. Perusahaan ini membutuhkan web server untuk menampilkan situs web dari perusahaan itu sendiri, database server untuk menyimpan data-data perusahaan, FTP server untuk berbagi data antar pegawai, mail server untuk kebutuhan email perusahaan dan email untuk pegawai, serta server monitoring untuk menganalisa apakah server masih cukup layak untuk digunakan atau perlu tambahan kapasitas.

3. Pihak yang terlibat dalam proses instalasi dan maintenance pada jaringan ini adalah kami sendiri dan network engineer.

## Soal No 2

![Topologi](https://raw.githubusercontent.com/adityaeka26/network-programming-2/master/images/topologi.png)

Kami memakai vps dalam pengerjaan proyek ini. Topologi yang digunakan adalah topologi tree. Alasan kami memakai topologi tree karena topologi ini mudah dalam pengelolaan, dan mudah melakukan identifikasi dan isolasi kesalahan-kesalahan yang terjadi dalam jaringan yang dibangun.

### Spesifikasi Server
- Disk Space : 50 GB
- CPU : 2 Core
- RAM : 2 GB
- OS : CentOS 7

## Soal No 3

Server yang kami bangun dijalankan menggunakan Virtual Machine dengan sistem operasi CentOS 7. Untuk melakukan konfigurasi, kami menggunakan ssh supaya bisa dilakukan secara remote dari device lain yang terhubung dalam 1 jaringan.

![SSH](https://raw.githubusercontent.com/adityaeka26/network-programming-2/master/images/ssh.png)

### Web Server
Web Server kami menggunakan Apache karena untuk konfigurasinya lebih mudah dibanding nginx. Web Server dijalankan pada port 80 atau http.

![Web Server](https://raw.githubusercontent.com/adityaeka26/network-programming-2/master/images/web-server.png)

### Database Server
Database Server yang kami gunakan adalah MariaDB yang merupakan database yang dikembangkan dari MySQL. Untuk GUI-nya, kami menggunakan phpMyAdmin yang merupakan tools berbasis php yang bisa digunakan untuk mengatur database MySQL atau MariaDB.

![Database Server](https://raw.githubusercontent.com/adityaeka26/network-programming-2/master/images/database-server.png)

### FTP Server
FTP Server yang kami gunakan adalah vsftpd. Vsftpd merupakan FTP Server yang cukup mudah konfigurasinya. Pada server kami, folder yang dapat diakses oleh FTP adalah folder /home/user

![FTP Server](https://raw.githubusercontent.com/adityaeka26/network-programming-2/master/images/ftp-server.png)

### Mail Server
Untuk membangun mail server, kami menggunakan 3 service, yaitu Postfix, Dovecot, dan Squirrelmail. Postfix berfungsi untuk mengirim email, Dovecot berfungsi untuk menerima email, dan Squirrelmail berfungsi sebagai GUI berbasis web untuk me-manage email atau biasa disebut sebagai webmail.

![Mail Server](https://raw.githubusercontent.com/adityaeka26/network-programming-2/master/images/mail-server.png)

### Server Monitoring
Server Monitoring yang kami gunakan adalah Cacti. Cacti membutuhkan beberapa service lain supaya dapat berjalan, yaitu web server (Apache), database server (MariaDB), SNMP, dan RRDTool. Web server berfungsi sebagai GUI untuk memonitor server, sedangkan database server berfungsi untuk menyimpan data monitoring supaya bisa dicek kembali di lain waktu.

![Server Monitoring](https://raw.githubusercontent.com/adityaeka26/network-programming-2/master/images/server-monitor-cacti.png)
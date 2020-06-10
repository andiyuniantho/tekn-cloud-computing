<br>Docker Swarm, Docker Compose dan Docker Networks ?<br/>
<br>Docker Compose adalah alat untuk mendefinisikan dan menjalankan<br/> <br>aplikasi multi-kontainer. Aplikasi multi-kontainer adalah aplikasi di mana banyak wadah bekerja sama untuk menyediakan fungsionalitas yang diperlukan.

Anda menentukan aplikasi Anda di file Menulis.

Anda dapat menjalankan aplikasi Anda dengan perintah `docker-compose`. Perintah `docker-compose` mengambil file Compose Anda sebagai input dan memastikan bahwa keadaan aplikasi Anda adalah apa yang Anda jelaskan dalam file Compose (kami menyebutnya keadaan yang diinginkan).

Docker Compose dapat menjalankan aplikasi multi-kontainer Anda di SINGLE HOST ONLY, ia tidak dapat menjalankan aplikasi Anda di cluster komputer.

Jika Anda ingin menjalankan aplikasi pada CLUSTER KOMPUTER, maka Anda membutuhkan Docker Swarm.<br/>
<br>Docker Networks adalah toolset untuk menentukan bagaimana wadah Anda terhubung satu sama lain.<br/>

<br>Ini adalah keputusan desain arsitektur untuk menentukan wadah mana yang saling berbicara di jaringan yang sama, berapa banyak jaringan yang harus dipisahkan oleh aplikasi Anda dan teknologi apa yang Anda gunakan untuk membuat gateway antara jaringan-jaringan ini.

Anda menentukan konfigurasi jaringan Anda di file Menulis. (Anda dapat membuat dan mengelola jaringan Docker dengan perintah `docker network`, tetapi lebih baik untuk menentukan konfigurasi Anda dalam bentuk kode di file Tulis.)

Anda biasanya mendefinisikan jaringan Anda sendiri, ini disebut jaringan yang ditentukan pengguna. Anda dapat membaca lebih lanjut di sini Ikhtisar.<br/>

<br>Compose dan Swarm memiliki tipe jaringan default yang berbeda.<br/>

<br>Jaringan default dalam skenario Menulis adalah jaringan jembatan. Bridge adalah tipe jaringan built-in di Docker, ini memisahkan wadah Anda dari sisa mesin host. Ketika Anda memulai aplikasi multi-kontainer dengan `docker-compose`, maka jaringan yang ditentukan pengguna akan dibuat sebagai jembatan jaringan.

Jenis jaringan default dalam mode Swarm adalah jaringan overlay. Jaringan overlay adalah jaringan yang merutekan permintaan di beberapa mesin di cluster Swarm. Ketika Anda memulai aplikasi Anda menggunakan file Tulis dalam mode Swam (perintah untuk melakukannya adalah `docker stack deploy`), maka jaringan yang ditentukan pengguna Anda akan dibuat sebagai jaringan overlay.<br/>
<br>Apa itu IaaS (Infrastruktur sebagai Layanan)?<br/>
<br>Infrastruktur-sebagai-a-Layanan, yang biasa disebut sebagai “IaaS,” adalah bentuk komputasi awan yang memberikan sumber daya komputasi, jaringan, dan penyimpanan yang mendasar kepada konsumen sesuai permintaan, melalui internet, dan dengan pembayaran dasar you-go. IaaS memungkinkan pengguna akhir untuk skala dan menyusutkan sumber daya sesuai kebutuhan, mengurangi kebutuhan untuk pengeluaran modal tinggi di muka atau infrastruktur “milik” yang tidak perlu, terutama dalam hal beban kerja “runcing”. Berbeda dengan PaaS dan SaaS (bahkan model komputasi yang lebih baru seperti container dan serverless), IaaS memberikan kontrol sumber daya tingkat terendah di cloud.

IaaS muncul sebagai model komputasi yang populer di awal 2010-an, dan sejak saat itu, iaaS telah menjadi model abstraksi standar untuk banyak jenis beban kerja. Namun, dengan munculnya teknologi baru, seperti wadah dan serverless, dan munculnya pola aplikasi layanan mikro yang terkait, IaaS tetap mendasar tetapi berada di bidang yang lebih ramai dari sebelumnya.<br/>

<br>Platform dan arsitektur IaaS<br/>
<br>IaaS terdiri dari kumpulan sumber daya fisik dan virtual yang menyediakan blok bangunan dasar yang dibutuhkan konsumen untuk menjalankan aplikasi dan beban kerja di cloud.<br/>

<br>Pusat data fisik: Penyedia IaaS akan mengelola pusat data besar, biasanya di seluruh dunia, yang berisi mesin fisik yang diperlukan untuk memberi daya pada berbagai lapisan abstraksi di atasnya dan yang disediakan untuk pengguna akhir melalui web. Dalam sebagian besar model IaaS, pengguna akhir tidak berinteraksi langsung dengan infrastruktur fisik, tetapi disediakan sebagai layanan untuk mereka.<br/>
<br>Komputasi: IaaS biasanya dipahami sebagai sumber daya komputasi tervirtualisasi, jadi untuk keperluan artikel ini, kami akan mendefinisikan komputasi IaaS sebagai mesin virtual. Penyedia mengelola hypervisors dan pengguna akhir kemudian dapat secara provisi menyediakan "instance" virtual dengan jumlah komputasi dan memori yang diinginkan (dan terkadang penyimpanan). Sebagian besar penyedia menawarkan CPU dan GPU untuk berbagai jenis beban kerja. Cloud Compute juga biasanya dipasangkan dengan layanan pendukung seperti penskalaan otomatis dan penyeimbangan beban yang memberikan skala dan karakteristik kinerja yang menjadikan cloud diinginkan.<br/>
<br>Jaringan: Jaringan di cloud adalah bentuk Software Defined Networking di mana perangkat keras jaringan tradisional, seperti router dan switch, dibuat tersedia secara terprogram, biasanya melalui API. Kasus penggunaan jaringan yang lebih maju melibatkan pembangunan kawasan multi-zona dan cloud pribadi virtual, yang keduanya akan dibahas secara lebih rinci nanti.<br/>
<br>Penyimpanan: Tiga jenis utama penyimpanan cloud adalah penyimpanan blok, penyimpanan file, dan penyimpanan objek. Penyimpanan blok dan file biasa dilakukan di pusat data tradisional tetapi seringkali dapat kesulitan dengan skala, kinerja, dan karakteristik cloud yang didistribusikan. Dengan demikian, dari ketiganya, penyimpanan objek telah menjadi mode penyimpanan paling umum di cloud mengingat bahwa itu sangat terdistribusi (dan dengan demikian tangguh), ia memanfaatkan perangkat keras komoditas, data dapat diakses dengan mudah melalui HTTP, dan skala tidak hanya dasarnya tak terbatas tetapi skala kinerja linear ketika cluster tumbuh.<br/>

<br>BMaaS vs. IaaS<br/>
<br>Bare-metal-as-a-Service (BMaaS) memberikan tingkat kontrol yang bahkan lebih rendah daripada IaaS tradisional. Dalam lingkungan BMaaS, sumber daya masih disediakan berdasarkan permintaan, tersedia melalui internet, dan ditagih berdasarkan pembayaran saat Anda bepergian (biasanya dalam kenaikan bulanan atau per jam).

Tidak seperti IaaS tradisional, BMaaS tidak menyediakan komputasi, jaringan, dan penyimpanan yang sudah tervirtualisasi kepada pengguna akhir; sebaliknya, ia memberikan akses langsung ke perangkat keras yang mendasarinya. Tingkat akses ini menawarkan hampir semua pengguna akhir kendali atas spesifikasi perangkat keras mereka. Mengingat perangkat keras tidak tervirtualisasi atau mendukung beberapa mesin virtual, ia juga menawarkan kepada pengguna akhir potensi kinerja terbesar, sesuatu yang bernilai signifikan untuk kasus penggunaan seperti komputasi HPC dan GPU, basis data berkinerja tinggi, beban kerja analitik, dan banyak lagi.

Untuk pengguna akhir yang terbiasa beroperasi di pusat data tradisional, lingkungan BMaaS juga akan merasakan yang paling akrab dan mungkin memetakan pola arsitektur beban kerja yang ada.

Namun, keuntungan ini juga dapat mengorbankan manfaat IaaS tradisional, yaitu kemampuan untuk benar-benar menyediakan secara cepat dan skala sumber daya secara horizontal dengan hanya membuat salinan contoh dan menyeimbangkan beban di antaranya.<br/>
<br>IaaS vs PaaS vs SaaS<br/>
<br>Cara termudah dan paling umum untuk memahami perbedaan antara kategori kasar -aaS dari IaaS, PaaS, dan SaaS biasanya dengan memahami elemen tumpukan yang dikelola oleh vendor dan yang dikelola oleh pengguna akhir.

Dalam pengaturan TI tradisional, tergantung pada pengguna akhir untuk mengelola seluruh tumpukan end-to-end, dari perangkat keras fisik untuk server dan jaringan, hingga melalui virtualisasi, sistem operasi, middleware, dan sebagainya.

IaaS, PaaS, dan SaaS masing-masing menawarkan lapisan abstraksi progresif setelah itu. IaaS mengabstraksi komputasi fisik, jaringan, penyimpanan, dan teknologi yang diperlukan untuk memvirtualisasikan sumber daya tersebut. PaaS melangkah lebih jauh dan memisahkan manajemen sistem operasi, middleware, dan runtime. SaaS menyediakan seluruh aplikasi pengguna akhir sebagai-a-Service, mengabstraksi seluruh sisa stack.<br/>

<br>IaaS vs. containers vs. serverless<br/>
<br>Baru-baru ini, diskusi seputar beban kerja cloud menjadi semakin didominasi oleh kontainer dan serverless. Dalam banyak hal, IaaS adalah langkah dalam perjalanan menuju cita-cita awan platonis.

IaaS memang menawarkan pengguna akhir lebih banyak granularity untuk membayar apa yang mereka gunakan, tetapi mereka jarang membayar hanya untuk apa yang mereka gunakan. Bahkan server virtual sering melibatkan proses yang berjalan lama dan pemanfaatan kapasitas yang kurang sempurna.

IaaS mengabstraksi banyak komponen tingkat rendah sehingga pengembang dapat fokus pada logika bisnis yang membedakan bisnis, tetapi masih membutuhkan pengguna akhir untuk mengelola sistem operasi, middleware, dan runtimes.

IaaS seringkali lebih banyak sumber daya dan efisien secara finansial daripada komputasi tradisional, tetapi memunculkan VM masih bisa memakan waktu, dan setiap VM membawa overhead dalam bentuk sistem operasi.

Model TI ini mampu mendukung hampir semua hal dari perspektif beban kerja tetapi memiliki ruang untuk evolusi dalam hal filosofi dan nilai-nilai tertentu yang mendasari yang menjadikan cloud, cloud.

Kontainer dan serverless adalah dua model cloud baru yang menantang model IaaS tradisional untuk supremasi di sekitar kelas aplikasi dan beban kerja asli cloud tertentu.

Dalam beberapa kasus, wadah telah mulai menggantikan VM sebagai unit standar proses atau penyebaran layanan, dengan alat orkestrasi seperti Kubernetes yang mengatur seluruh ekosistem cluster.

Serverless menjadi yang terjauh dari model apa pun, mengabstraksi hampir semua hal kecuali logika bisnis, meningkatkan permintaan dengan sempurna, dan benar-benar memenuhi janji untuk membayar hanya untuk apa yang Anda gunakan.

Ketika dunia bergerak lebih ke arah arsitektur layanan-mikro — di mana aplikasi didekomposisi menjadi bagian-bagian kecilnya, disebarkan secara mandiri, mengelola data mereka sendiri, dan berkomunikasi melalui API — wadah dan pendekatan tanpa server hanya akan menjadi lebih umum.

Saat ini, IaaS tradisional, sejauh ini, merupakan model komputasi yang paling matang di cloud dan mengendalikan sebagian besar pangsa pasar di ruang ini, tetapi kontainer dan serverless akan menjadi teknologi untuk menonton dan mulai menggunakan secara oportunis di tempat yang masuk akal.<br/>

<br>IaaS dan IBM Cloud<br/>
<br>IBM menawarkan platform cloud stack penuh yang mencakup lapisan IaaS penuh untuk komputasi, jaringan, dan penyimpanan yang tervirtualisasi. Selain itu, dan unik dalam industri ini, IBM Cloud juga menawarkan BMaaS untuk pengguna yang menginginkan kontrol tambahan atas perangkat keras yang mendasarinya.

IBM juga berkomitmen untuk memberikan solusi untuk aplikasi dan beban kerja asli cloud yang, selain IaaS, termasuk Layanan Cloud IBM Kubernetes dan Fungsi Cloud IBM untuk aplikasi tanpa server.

Untuk memulai cloud IaaS, buat akun IBM Cloud dan berikan server virtual pertama Anda.<br/>

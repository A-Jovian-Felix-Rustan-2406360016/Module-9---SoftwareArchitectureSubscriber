Subscriber Reflection : 
1. AMQP (Advanced Message Queuing Protocol) adalah sebuah protokol standar terbuka pada level application layer yang digunakan untuk mengirim pesan satu sama lain. Dengan adanya protokol ini, memungkinkan pengirim dan penerima untuk saling berkomunikasi walaupun mereka dibuat dengan bahasa pemrograman dan berjalan di platform yang berbeda. Penggunaan AMQP ini juga menjamin pesan terkirim dengan aman dan memiliki sistem antrian yang baik. Dalam tutorial ini, kita juga menggunakan AMQP di crosstown_bus untuk berinteraksi dengan RabbitMQ.

2. guest:guest@localhost:5672 adalah sebuah connection url yang digunakan aplikasi untuk terhubung ke RabbitMQ, berikut penjelasan detailnya : 
- guest (pertama) : username default untuk login ke RabbitMQ
- guest (kedua) : password default untuk username tersebut
- localhost : menunjukkan lokasi server RabbitMQ. Hal ini berarti server tersebut berjalan di komputer yang sama dengan aplikasi kita.
- 5672 : port standar yang digunakan oleh RabbitMQ untuk komunikasi melalui protokol AMQP.

Screenshot slow subscriber graph : 
![Slow Subscriber Simulation](resources/SlowSubscriber.png)

Explanation : 
Simulasi Slow Subscriber ini bertujuan untuk menunjukkan salah satu fungsi utama message broker seperti RabbitMQ untuk menangani load balancing dan asynchronous processing. Setelah saya menjalankan publisher 3 kali secara cepat, kita dapat melihat hasil grafik pada gambar mengalami kenaikan yaitu puncaknya di 2.0. Hal ini menunjukkan bahwa terjadi perbedaan kecepatan antara publisher dalam mengirim dan subscriber dalam menerimanya sehingga pesan tertumpuk di rabbitMQ. Namun, kenaikan tersebut tidak terlihat signifikan karena dalam tutorial ini kita hanya menggunakan thread::sleep(ten_millis) dimana kecepatan subscriber setelah sengaja dilambatkan masih hampir sama cepatnya dengan publisher sehingga hanya mentok di angka 2 meskipun sudah mengirim 15 pesan (3 kali run).
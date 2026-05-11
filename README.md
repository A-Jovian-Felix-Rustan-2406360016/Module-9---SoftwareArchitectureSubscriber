Subscriber Reflection : 
1. AMQP (Advanced Message Queuing Protocol) adalah sebuah protokol standar terbuka pada level application layer yang digunakan untuk mengirim pesan satu sama lain. Dengan adanya protokol ini, memungkinkan pengirim dan penerima untuk saling berkomunikasi walaupun mereka dibuat dengan bahasa pemrograman dan berjalan di platform yang berbeda. Penggunaan AMQP ini juga menjamin pesan terkirim dengan aman dan memiliki sistem antrian yang baik. Dalam tutorial ini, kita juga menggunakan AMQP di crosstown_bus untuk berinteraksi dengan RabbitMQ.

2. guest:guest@localhost:5672 adalah sebuah connection url yang digunakan aplikasi untuk terhubung ke RabbitMQ, berikut penjelasan detailnya : 
- guest (pertama) : username default untuk login ke RabbitMQ
- guest (kedua) : password default untuk username tersebut
- localhost : menunjukkan lokasi server RabbitMQ. Hal ini berarti server tersebut berjalan di komputer yang sama dengan aplikasi kita.
- 5672 : port standar yang digunakan oleh RabbitMQ untuk komunikasi melalui protokol AMQP.
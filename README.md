# Tutorial 8 - Advanced Programming - Subscriber
**Akmal Ramadhan - 2206081534 - Kelas A**

## Apa itu `amqp`?
`amqp` atau Advanced Message Queuing Protocol (AMPQ) adalah protokol komunikasi jaringan yang berfungsi untuk mengirimkan pesan antara aplikasi, organisasi, atau komponen yang berbeda. AMQP dapat mendukung _programming load balancing_ dan _monitoring_ karena adanya pemisahan pertukaran (yang _producer_ kirim) dan antrean (yang _customer_ dengar). 

Pada `main.rs`, AMQP diimplementasikan untuk _message queuing_ yang menghubungkan `UserCreatedHandler` dengan `main` menggunakan `CrosstownBus`. `UserCreatedHandler` dapat menerima pesan yang dikirimkan ke _queue_ dengan topik `"user_created"`.

## Apa arti dari `guest:guest@localhost:5672` ?
`guest:guest@localhost:5672` adalah URL yang mengoneksikan ke _server_ AMQP.

- `guest` pertama merujuk pada _username_ untuk autentikasi RabbitMQ.
- `guest` kedua merujuk pada _password_ untuk autentikasi RabbitMQ.
- `localhost` artinya bahwa _server_ AMQP berjalan di mesin yang sama dengan jalannya program.
- `5672` adalah _default port server_ AMQP dan akan digunakan oleh _server_ RabbitMQ untuk menerima koneksi dari _client_.

## Referensi
- Module 8 - Software Architecture oleh Ade Azurat dan Tim Pengajar.
- [About - AMQP](https://www.amqp.org/about/what)
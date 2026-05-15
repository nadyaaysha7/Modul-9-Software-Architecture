## Understanding Publisher and Message Broker

A. Dalam satu kali eksekusi (run), program publisher ini akan mengirimkan sebanyak 5 (lima) data atau event ke message broker. Kelima data tersebut dikirimkan secara berurutan dalam bentuk struct UserCreatedEventMessage yang mencakup informasi ID dan nama pengguna (Amir, Budi, Cica, Dira, dan Emir) ke dalam sebuah antrean (queue) yang diberi nama "user_created".

B. Penggunaan URL "amqp://guest:guest@localhost:5672" yang sama persis dengan program subscriber menandakan bahwa kedua program tersebut terhubung ke server message broker (RabbitMQ) lokal yang sama. Kesamaan alamat koneksi ini sangat krusial dalam arsitektur event-driven, karena hal ini memastikan pesan yang dipublikasikan oleh publisher masuk ke "ruangan" yang tepat, sehingga program subscriber dapat menemukan, mendengarkan (listen), dan memproses pesan-pesan tersebut dari sumber yang sama.

## RabbitMQ

![img.png](img.png)

## Event

![img_1.png](img_1.png)

## Monitoring

![img_2.png](img_2.png)
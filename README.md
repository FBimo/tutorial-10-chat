# Tutorial 2 Module 10

<details>
<summary>2.1. Original Code and How It Run</summary>

Server
![2.1 Original code and how it run](image.png)
Client-1
![2.1 Original code and how it run - 1](image-1.png)
Client-2
![2.1 Original code and how it run - 2](image-2.png)
Client-3
![2.1 Original code and how it run - 3](image-3.png)

Kita perlu menambahkan kode di bawah ini pada `Cargo.toml`
```
[[bin]]
name = "server"

[[bin]]
name = "client"
```

Dengan itu, Cargo akan mengetahui bahwa ada beberapa target biner dalam proyek ini, yaitu server dan client. Dengan menspesifikasikannya dalam `Cargo.toml`, kita memberitahu Cargo untuk membangun eksekutor terpisah untuk masing-masing biner ini saat kita menjalankan `cargo build` atau `cargo run`.

Untuk menjalankan program, 

1. Navigasi ke direktori proyek yang berisi `Cargo.toml`.
2. Jalankan server dengan mengeksekusi `cargo run --bin server`.
3. Jalankan tiga _client_ dengan membuka tiga jendela terminal terpisah dan mengeksekusi `cargo run --bin client`.
4. Setiap _client_ akan terhubung ke server dan meminta kita untuk mengetikkan sebuah pesan/_chat_.
5. Ketikkan sebuah pesan di setiap terminal _client_ dan tekan _Enter_.
6. Amati bahwa pesan tersebut dikirim ke server yang kemudian menyiarkannya ke semua _client_ yang terhubung.
7. Kita akan melihat pesan yang diterima oleh setiap _client_, termasuk yang dikirim oleh dirinya sendiri.

Ketika kita mengetik pesan di setiap _client_, pesan tersebut dikirim ke server, yang kemudian menyiarkannya ke semua _client_ yang terhubung. Setiap _client_ menerima pesan yang disiarkan, termasuk pesan yang dikirimnya sendiri, sehingga terjadi interaksi mirip obrolan antara semua _client_.

</details>

<!-- <details>
<summary>1.3. Multiple Spawn and Removing Drop.</summary>

</details> -->

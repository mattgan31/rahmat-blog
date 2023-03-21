---
title: "Macam Query Pada Laravel"
description: Macam-macam bentuk Query pada Laravel
date: 2023-03-21T11:45:12+07:00
image:
math:
license:
hidden: false
comments: true
draft: true
categories:
  - Programming
tags:
  - Laravel
  - Website
---

## Apa itu Eloquent ORM ?

Eloquent ORM merupakan fungsi ActiveRecord pada Laravel yang cantik dan sederhana untuk dapat bekerja dengan database Anda. Setiap tabel database memiliki "Model" yang sesuai digunakan untuk berinteraksi dengan tabel tersebut.

Untuk dapat menggunakan Eloquent ORM pada Laravel pastikan kamu sudah melakukan konfigurasi database melalui file `.env` yang tersedia pada project Laravel kamu

## Bentuk-bentuk ORM pada Laravel

Berikut adalah bentuk-bentuk ORM yang terdapat pada Laravel

### Mendapatkan semua data pada tabel

Untuk mendapatkkan semua data pada tabel database, dapat berbentuk seperti berikut

```php
Product::all();

# SELECT * FROM products
```

Mari kita bedah syntax diatas tersebut,

1. Pada `Product` merupakan nama model yang kita gunakan dan tentunya model tersebut memiliki tabel database ya
2. Lalu pada `all()` merupakan fungsi untuk mendapatkan semua data yang ada pada tabel database.

### Mendapatkan data berdasarkan `id`

Untuk melihat detail data dan juga melakukan edit dan delete, kita perlu mendapatkan data yang kita mau dengan parameter data uniknya sebagai contoh yaitu id pada produk. Berikut adalah contoh ORM untuk mendapatkan data berdasarkan `id`

```php
Product::find(1);

# SELECT * FROM products WHERE id=1;
```

Mari kita bedah syntax tersebut,

1. Seperti contoh sebelumnya, kita perlu memanggil file modelnya terlebih dahulu.
2. Kemudian pada `find(1)`, yaitu fungsi untuk mencari berdasarkan id yang dimana contohnya `id` tersebut ialah `1`

### Mendapatkan data berdasarkan kondisi kolom tertentu

Pada kasus tertentu kita diperlukan untuk mendapat data berdasarkan value pada kolom tertentu misalkan pada produk, kita ingin menampilkan produk yang memiliki harga tertentu. Berikut adalah contohnya

```php
Product::where('price', '>', 100000);

# SELECT * FROM products WHERE price > 100000;
```

1. Seperti biasa kita perlu memanggil modelnya terlebih dahulu,
2. Dilanjut dengan `where` dengan parameter yang diinginkan, misalkan pada contoh kita ingin mencari produk yang memiliki harga diatas 100000 maka kita menuliskan `('price', '>', 100000)`

### Custom query builder

Pada beberapa kasus, kita hanya memerlukan untuk menampilkan data hanya dari sebagian kolom yang diinginkan saja. Untuk contohnya bisa dilihat pada syntax berikut

```php
DB::table('products')
    ->select('product_name', 'price')
    ->get();
```

Syntax diatas kita memanggil tabel `products` dan memanggil kolom `product_name` dan `price` saja.

Itu saja yang bisa dicatat pada kesempatan kali ini, semoga catatan ini berguna bagi kita semua. Terimakasih

---
title: "Pemrograman Golang Dasar"
description: "Belajar dasar mengenai pemrograman Golang"
date: 2023-04-03T08:56:58+07:00
image: "cover.png"
math:
license:
hidden: false
comments: true
draft: false
categories:
  - Programming
tag:
  - git
  - github
---

Pada kesempatan kali ini, saya mau membuat catatan kecil mengenai pemrograman golang

## Asal-usul pemgrogaman Golang

Pemrograman Golang (atau disebut juga Go) dikembangkan oleh tiga orang, yaitu Robert Griesemer, Rob Pike, dan Ken Thompson, yang semuanya adalah mantan insinyur Google. Pengembangan Golang dimulai pada tahun 2007 dan pertama kali diumumkan pada tahun 2009.

Awalnya, Golang dibuat untuk menangani beberapa masalah yang ditemukan dalam pengembangan perangkat lunak pada saat itu, seperti kesulitan dalam menangani aplikasi berskala besar, masalah performa, dan kompleksitas bahasa pemrograman. Dalam membangun Golang, tim pengembang juga ingin menciptakan bahasa yang mudah dipelajari dan dipahami oleh para pengembang, sambil tetap mempertahankan kinerja dan keamanan yang baik.

Sejak dirilis, Golang telah menjadi bahasa pemrograman populer di kalangan pengembang perangkat lunak, terutama untuk pengembangan aplikasi server-side dan program dengan kecepatan tinggi. Saat ini, Golang terus berkembang dan menjadi semakin populer, terutama di industri teknologi seperti Google, Uber, Dropbox, dan banyak lagi.

## Syntax basic pada Golang

Setiap pemrograman memiliki kemiripan dan perbedaannya masing-masing, dan perbedaan dan kemiripan itulah yang membuat suatu bahasa pemrograman itu menarik

### Package & Import

Golang menggunakan konsep `package` untuk mengorganisir kode, setiap file harus berada didalam sebuah `package`. Package dapat diimpor oleh file lain dengan menggunakan keyword `import`.

Contoh:

```go
package main

import(
    "fmt"
)
```

### Membuat fungsi

Fungsi merupakan blok kode yang dapat dipanggil dan dijalankan secara independen. Fungsi pada golang diidentifikasikan dengan menggunakan keyword `func`.

Contoh:

```go
func helloWorld(){
    fmt.Println("Hello World!")
}
```

### Variabel

Golang memiliki keunikan, kamu dapat mengidentifikasikan tipe datanya ataupun tidak yang nantinya variabel tersebut memiliki tipe data sesuai dengan value didalamnya, kamu perlu menggunakan titik dua ":" persis sebelum tanda sama dengan "=".

Contoh:

```go
var name string = "John Doe"

num := 20
```

### Pengkondisian

Sama seperti bahasa pemrograman lainnya, golang juga memiliki syntax pengkondisian seperti if-else ataupun switch-case

Contoh:

```go
// if-else
if age >= 18 {
    fmt.Println("You are an adult")
} else {
    fmt.Println("You are not an adult")
}

// switch-case
switch day {
    case "Monday":
        fmt.Println("Today is Monday")
    case "Tuesday":
        fmt.Println("Today is Tuesday")
    default:
        fmt.Println("Today is another day")
}
```

## Penutup

Terimakasih sudah mampir ke blog saya ini, mohon maaf apabila terdapat kekurangan dalam penulisan. Disini saya selain sedang belajar koding, saya mencoba belajar menulis juga. Mohon dimaklumi ya :)

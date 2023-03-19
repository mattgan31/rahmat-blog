---
title: "Cara Membuat Model Laravel"
description: "Model dalam sebuah project laravel"
date: 2023-03-19T18:42:53+07:00
image: cover.png
math:
hidden: false
comments: true
draft: true
categories:
  - Programming
tags:
  - Laravel
  - Website
---

# Membuat File Model Untuk Laravel

Apa fungsi dari file Model ? Model merupakan bagian yang mengatur serta paling dekat dengan database. Pada Laravel, model dapat digunakan untuk mengatur table yang digunakan, mengatur akses kolom yang diperbolehkan untuk diisi melalui controller dan masih banyak lagi

## Hal yang dapat dilakukan untuk membuat Model

Untuk membuat file model kamu dapat menjalankan command berikut pada direktori project kamu

```
php artisan make:model Product
```

maka akan ter-generate file model baru pada direktori "aplikasimu/app/Models/[nama-model].php". File akan berisi seperti berikut

{{< highlight php "linenos=table" >}}

<?php

namespace App\Models;

use Illuminate\Database\Eloquent\Factories\HasFactory;
use Illuminate\Database\Eloquent\Model;

class Product extends Model
{
    use HasFactory;
}
{{< / highlight >}}

Namun ada cara lain yang lebih praktis

## Membuat model sekaligus controller

Kamu dapat membuat file Model sekaligus Controller untuk mempermudah developer dalam generate file-file tersebut, yang perlu kamu lakukan ialah kamu perlu menjalankan command berikut

```
php artisan make:model Product -c -r
```
Maka akan terbentuk file model dan controller, untuk file controller tersimpan pada direktori "aplikasimu/app/Http/Controllers/[nama-controller].php"

Untuk file controller, maka akan berisi seperti berikut
{{< highlight php "linenos=table" >}}
<?php

namespace App\Http\Controllers;

use App\Models\Product;
use Illuminate\Http\Request;

class ProductController extends Controller
{
    /**
     * Display a listing of the resource.
     */
    public function index()
    {
        //
    }

    /**
     * Show the form for creating a new resource.
     */
    public function create()
    {
        //
    }

    /**
     * Store a newly created resource in storage.
     */
    public function store(Request $request)
    {
        //
    }

    /**
     * Display the specified resource.
     */
    public function show(Product $product)
    {
        //
    }

    /**
     * Show the form for editing the specified resource.
     */
    public function edit(Product $product)
    {
        //
    }

    /**
     * Update the specified resource in storage.
     */
    public function update(Request $request, Product $product)
    {
        //
    }

    /**
     * Remove the specified resource from storage.
     */
    public function destroy(Product $product)
    {
        //
    }
}

{{< / highlight >}}

Perlu diperhatikan, pada controller yang dibuat pada perintah diatas. Akan berisi fungsi-fungsi CRUD untuk mempermudah pada file route nantinya.

Sekian penulisan tentang model pada laravel ini, semoga tulisan ini dapat bermanfaat bagi banyak orang.

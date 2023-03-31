---
title: "Perintah Git Yang Sering Digunakan"
description:
date: 2023-03-27T10:32:48+07:00
image:
math:
license:
hidden: false
comments: true
draft: true
categories:
- Programming
tag:
- git
- github
---

## Apa itu Git ?

Git merupakan sebuah platform version control untuk menghandle versi pada pengembangan perangkat lunak/software, git ini gratis dan open source.
Untuk mempermudah kamu dalam pengembangan perangkat lunak, kamu perlu mempelajari git tersebut. Github merupakan salah satu dari turunan git namun dibuat secara cloud/online

## Buat akun github

Untuk dapat menggunakan github, kamu memerlukan akun github tersebut. Kamu dapat membuatnya melalui [github.com](https://github.com/) lalu klik Signup dan ikuti perintahnya.

## Perintah git yang sering digunakan

Berikut adalah penjelasan singkat mengenai cara penggunaan beberapa fungsi Git yang sering digunakan di industri:

### git clone
Clone: Untuk melakukan clone, buka terminal/command prompt dan ketik perintah `git clone <url repository>` di mana `<url repository>` adalah URL repository yang ingin diduplikasi ke dalam repository lokal. Setelah perintah selesai dieksekusi, repository akan tersedia di direktori lokal.

### git add
Add: Untuk menambahkan file atau folder ke dalam staging area, buka terminal/command prompt dan masuk ke dalam direktori repository menggunakan perintah cd. Setelah itu, ketik perintah `git add <nama file>` atau `git add .` untuk menambahkan semua file yang ada ke dalam staging area.
### git commit
Commit: Setelah melakukan add, ketik perintah `git commit -m "<pesan commit>"` untuk menyimpan perubahan ke dalam repository Git. `<pesan commit>` adalah pesan yang menjelaskan perubahan apa yang dilakukan pada kode.
### git push
Push: Untuk mengirim perubahan ke repository yang berada di server, ketik perintah git push. Jika ini pertama kali melakukan push, Anda perlu menentukan branch mana yang ingin digunakan dengan perintah `git push -u <nama remote> <nama branch>`.
### git pull
Pull: Untuk mengambil perubahan terbaru dari repository yang berada di server, ketik perintah `git pull`. Hal ini akan mengambil perubahan terbaru dari server dan menggabungkannya dengan kode yang ada di repository lokal.

### git branch
Branch: Untuk membuat branch baru, ketik perintah `git branch <nama branch>`. Setelah itu, pindah ke branch baru menggunakan perintah `git checkout <nama branch>`.
### git merge
Merge: Untuk menggabungkan perubahan dari cabang yang berbeda ke dalam cabang utama, pindah ke branch utama menggunakan perintah `git checkout <nama branch utama>`. Setelah itu, ketik perintah `git merge <nama branch>` untuk menggabungkan perubahan dari branch yang berbeda ke dalam branch utama.

### git rebase
Rebase: Untuk melakukan rebase, pindah ke branch yang ingin di-rebase menggunakan perintah `git checkout <nama branch>`. Setelah itu, ketik perintah `git rebase <nama branch target>` untuk mengubah sejarah commit pada branch yang sedang dikerjakan.

### git tag
Tag: Untuk menandai commit tertentu dengan label tertentu, ketik perintah `git tag <nama tag> <hash commit>` di mana `<nama tag>` adalah label yang ingin ditandai dan `<hash commit>` adalah hash commit yang ingin ditandai.

### git cherry-pick
Cherry-pick: Untuk melakukan cherry-pick, pindah ke branch yang ingin ditambahkan commit tertentu menggunakan perintah `git checkout <nama branch>`. Setelah itu, ketik perintah `git cherry-pick <hash commit>` untuk menambahkan commit tertentu ke branch yang sedang dikerjakan.

## Penutup
Sekian tulisan dari saya, harapan saya tulisan ini bermanfaat terutama bagi diri saya maupun orang lain. Terimakasih

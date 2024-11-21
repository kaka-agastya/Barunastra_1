# Barunastra_1

[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/tbEHDGEc)
# Git and Github Introduction

| Nama  | Division        | Sub-Division  |
| ----- | ---------- | ---------- |
| Name here   | ELC/PGR | Sub-div |

# Cara Menggunakan Git & Github

## A. Prosedur Awal
### 1. Melakukan instal Git ke PC/Laptop
	https://git-scm.com/downloads
### 2. Membuat akun Github
	https://github.com/join
### 3. Melakukan setting pada Git Bash atau Terminal
   ```
   git config --global user.name (masukkan username)
   git config --global user.email (masukkan email)
   ```
### 4. Membuat SSH Keys pada laman Github
   #### a. Buka laman Github lalu menuju Settings -> SSH and GPG keys -> New SSH Key
   #### b. Untuk key sendiri dapat dibuat dengan cara membuka Git Bash dan memasukkan command line berikut
   ```
   ssh-keygen -t ed25519 -C (masukkan email)
   ### Kemudian pencet enter 2x ###
   ```
   #### c. Copy clip SSH key yang telah dibuat dengan command line berikut
   ```
   clip < ~/.ssh/id_ed25519.pub
   ```
   #### d. Kemudian paste atau Ctrl+V ke bagian key pada setting New SSH Key di Github

## B. Membuat Repository
### 1. Bukan laman Github
	https://github.com/new
### 2. Masukkan nama repository yang diinginkan beserta tipenya (private atau public) kemudian klik create repository
### 3. Buka repository yang telah dibuat
### 4. Klik Code -> SSH -> pencet tombol berbentuk 2 kotak untuk meng-copy link SSH
### 5. Untuk menghubungkan dengan file local bisa menggunakan dua cara sebagai berikut (kedua cara ini juga bisa digunakan untuk mendownload repository yang telah ada isinya ke file local):
   #### a. Manual 
   ##### i. Membuat folder di File Explorer dengan judul folder sama seperti repository
   ##### ii. Klik kanan dan buka Git Bash
   ##### iii. Masukkan command line berikut pada Git Bash

   	git init
   	git remote add origin (link SSH yang telah di-copy)
   	git branch -M main
   ##### iv. Agar memastikan folder di local sama dengan folder di Github, masukkan command line berikut pada Git Bash
	
 	git pull origin (branch yang ingin didownload)
   #### b. Git Clone
   ##### i. Buka Git Bash pada folder parent yang diinginkan dan masukkan command line berikut

	git clone (link SSH yang telah di-copy)
   ##### ii. Folder/Repository akan muncul pada File Explorer / Folder parent yang telah dipilih
   ##### iii. Kemudian buka folder tersebut
   ##### iv. Klik kanan dan buka Git Bash
   ##### v. Masukkan command line berikut pada Git Bash

	git branch -M main

## C. Mengunggah File di Local ke Github
### 1. Folder yang telah dibuat tersebut dapat secara bebas diisi dengan apa saja, tetapi baru tersimpan di local dan perlu diupload ke Github
### 2. Buka folder di local yang telah dibuat dan diisi
### 3. Klik kanan dan buka Git Bash
### 4. Masukkan command line berikut pada Git Bash
```
git add .
git commit -m "(ketikkan deskripsi dengan bebas)"
git push origin (branch yang ingin diupload)
```

## D. Membuat Branch Baru di Github
### 1. Branch adalah versi lainnya dari suatu folder di Github, dengan branch dapat melakukan perubahan versi di folder atau memasukkan isi yang lain tanpa menganggu branch utama
### 2. Buka folder yang diingikan yang telah terhubung dengan Github
### 3. Klik kanan dan buka Git Bash
### 4. Masukkan command line berikut pada Git Bash
	git checkout -B (nama branch yang diinginkan)
### 5. Untuk pindah ke branch yang telah dibuat dapat menggunakan command line berikut
	git checkout (nama branch yang telah dibuat)

## E. Menghapus Branch di Github
### 1. Pindah ke branch lain yang tidak dihapus dengan command line berikut
	git checkout (nama branch yang diinginkan)
### 2. Masukkan command line berikut untuk menghapus branch yang dipilih
	git branch -d (nama branch yang ingin dihapus)

## F. Menggabungkan Branch di Github
### 1. Pindah ke branch yang ingin menjadi branch utama dari branch yang ingin digabungkan dengan command line berikut
	git checkout (nama branch yang diinginkan)
### 2. Gabungkan branch dengan command line berikut
	git merge (nama branch yang ingin digabungkan)

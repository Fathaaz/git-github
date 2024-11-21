# Git and Github Introduction

| Nama  | Division        | Sub-Division  |
| ----- | ---------- | ---------- |
| Name here   | ELC/PGR | Sub-div |

## Early Procedure
### 1. Melakukan instalasi Git ke PC/Laptop
	https://git-scm.com/downloads
### 2. Membuat akun Github
	https://github.com/join
### 3. Melakukan setting pada Terminal
   ```
   git config --global user.name (masukkan username)
   git config --global user.email (masukkan email)
   ```
### 4. Membuat SSH Keys dan Menghubungkannya Pada Github
#### a. Membuat Key pada Terminal dengan Menggunakaan Command Line Berikut
   ```
   ssh-keygen -t ed25519 -C (masukkan email)
   ### Lalu pencet enter 2x ###
   ```
   #### b. Copy SSH Key yang Telah Dibuat dengan Command Line Berikut
   ```
   cat ~/.ssh/id_ed25519.pub
   ```
   #### c. Menambahkan SSH Key yang Telah Dibuat ke Github
   ```
Masuk ke laman berikut:
https://github.com/settings/ssh/new
Lalu copy paste SSH Key yang telah dibuat
```

![Screenshot 2024-11-20 213628](https://github.com/user-attachments/assets/d80bf2ce-314f-4c7c-a0ca-cc5c730d875a)


## Create Repository
### 1. Buat Repository Baru 
```
https://github.com/new
Masukkan nama dan tipenya (Public atau Private)
```
### 2. Buka Repository yang Telah Dibuat

### 3. Salin link SSH
```
Klik Code, lalu klik bagian SSH kemudian pencet tombol berbentuk 2 persegi untuk langsung meng-copy
```
### 4. Untuk Menghubungkan File Lokal dengan Repositori yang Telah Dibuat Digunakan Cara Berikut

#### a. Buka Terminal pada File Local yang Diinginkan lalu gunakan Command Berikut 
```
git clone (Link ssh yang telah di copy tadi)
```
#### b. Jika Langkah Sebelumnya Berhasil akan Muncul Folder Baru 
#### c. Buka Folder Tersebut lalu Buka Terminal atau Gunakan Command Line Berikut.
```
cd (Lokasi Folder Baru )
```
#### d. Masukkan command line berikut pada Git Bash
```
git branch -m main
```

## Push File from Local to Github

## Create New Branch in Github 

## Delete Branch in Github

## Merging Branch in Github

## Other Procedure

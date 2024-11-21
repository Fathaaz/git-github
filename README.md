# Git and Github Introduction

| Nama  | Division        | Sub-Division  |
| ----- | ---------- | ---------- |
| Fatharanni Faza   | ELC | Electrical Design |

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
### 1. Pada Folder Baru Tadi Dapat Diisi File Apa saja (Dalam langkah ini file yang akan diupload adalah Tes.txt)
### 2. Pada Terminal di Folder Baru Tadi Masukkan Command Line Berikut
```
git add . 
git commit -m "(Deskripsi perubahan)"
git push origin (branch yang ingin dituju)
```
### 3. Jika Langkah Di Atas Berhasil akan Muncul File Baru Pada Branch yang Dituju

## Create New Branch in Github 
### 1. Branch adalah versi lainnya dari suatu folder di Github, memungkinkan pekerjaan terpisah tanpa mengganggu branch utama (main)
### 2. Buka folder yang diinginkan yang telah terhubung dengan github
### 3. Buat branch dengan menggunakan command berikut (Dalam langkah ini nama branch adalah Tes
```
git checkout -b (Nama branch yang ingin dibuat)
```
### 4. Untuk memastikan kita telah pindah ke branch yang baru digunakan command line berikut
```
git checkout (Nama branch yang baru dibuat)
```
### 5. Upload branch yang baru dibuat ke Github
```
git push origin (Nama brannch yang baru dibuat)
```
### 6. Apabila langkah berhasil akan muncul branch baru pada repository

## Delete Branch in Github
### 1. Pada folder tadi buka terminal
### 2. Pindah ke branch lain (Selain yang akan dihapus)
```
git checkout (nama branch lain)
```
### 3. Untuk menghapus branch yang diinginkan gunakan command berikut 
```
git branch -d (nama branch yang ingin dihapus)
```
### 4. Untuk menghapus branch di Github gunakan command berikut
```
git push origin --delete (nama branch pada Github yang sama dengan lokal yang ingin dihapus)
```
### 5. Apabila berhasil pada repository branch tadi akan hilang

## Merging Branch in Github
### 1. Pada terminal pindah ke branch utama yang ingin digabungkan dengan command berikut
```
git checkout (nama branch utama)
```
### 2. Gabungkan branch dengan menggunakan command berikut
```
git merge (nama branch yang ingin digabungkan dengan branch utama)
```
## Other Procedure

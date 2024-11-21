# Git and Github Introduction

| Nama  | Division        | Sub-Division  |
| ----- | ---------- | ---------- |
| Fatharanni Faza   | ELC | Electrical Design |

## Early Procedure
### 1. Melakukan instalasi Git ke PC/Laptop
	https://git-scm.com/downloads
 ![screenshot-1732147697821](https://github.com/user-attachments/assets/4869d690-5eae-4456-a8ea-e3fe0da6c0ce)
### 2. Membuat akun Github
	https://github.com/join
 ![screenshot-1732147814907](https://github.com/user-attachments/assets/309c90cd-8883-4085-8ae2-536ab54f01c0)
### 3. Melakukan setting pada Terminal
   ```
   git config --global user.name (masukkan username)
   git config --global user.email (masukkan email)
   ```
![Screenshot 2024-11-21 124034](https://github.com/user-attachments/assets/e0060b5b-243a-4e75-985f-73e741b1fa57)
### 4. Membuat SSH Keys dan Menghubungkannya Pada Github
#### a. Membuat Key pada Terminal dengan Menggunakaan Command Line Berikut
   ```
   ssh-keygen -t ed25519 -C (masukkan email)
   ### Lalu pencet enter 2x ###
   ```
 ![Screenshot 2024-11-21 072328](https://github.com/user-attachments/assets/e3b171e1-6490-4ec9-8741-95c37a8bd3d4)
   #### b. Copy SSH Key yang Telah Dibuat dengan Command Line Berikut
   ```
   cat ~/.ssh/id_ed25519.pub
   ```
![Screenshot 2024-11-21 072335](https://github.com/user-attachments/assets/fc4c73b1-de8f-40ad-ac3a-9e5cfe5a5dd3)
   #### c. Menambahkan SSH Key yang Telah Dibuat ke Github
   ```
Masuk ke laman berikut:
https://github.com/settings/ssh/new
Copy paste SSH Key yang telah dibuat
Lalu klik Add SSH Key
```
![Screenshot 2024-11-21 072554](https://github.com/user-attachments/assets/26330a4e-3105-4123-afe5-b2bdb783d0a6)

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
### 1. Pada terminal pindah ke branch yang ingin digabungkan dengan command berikut
```
git checkout (nama branch tujuan yang ingin digabungkan)
```
### 2. Untuk memastikan branch up to date gunakan command line berikut
```
git pull origin (nama branch tujuan yang ingin digabungkan)
```
### 3. Gabungkan branch dengan menggunakan command berikut
```
git merge (nama branch yang ingin digabungkan dengan branch tujuan)
```
### 4. Upload merge yang telah dilakukan ke github
```
git push origin (nama branch tujuan)
```
## Other Procedure

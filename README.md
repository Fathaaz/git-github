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

## Push File from Local to Github

## Create New Branch in Github 

## Delete Branch in Github

## Merging Branch in Github

## Other Procedure

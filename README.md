# Git and Github Introduction

| Nama  | Division        | Sub-Division  |
| ----- | ---------- | ---------- |
| Name here   | ELC/PGR | Sub-div |

# NewFile
```
#include <stdio.h>
int main(){
    int a = 1, b = 2; // deklarasi variabel
    // /*same as 
    // int a = 1;
    // int b = 2;

    int calculate;
    calculate = a + b ; //1 + 2

    printf ("hello world!");
    printf("%d",calculate);
}
```
 1. Library stdio.h adalah library standar untuk fungsi input output.
### 2. Pada awalnya variabel a dideklarasikan sebagai 1 dan variabel b dideklarasikan sebagai 2.
### 3. Kemudian dideklarasikan variabel calculate, yang merupakan hasil tambah dari a + b (1+2).
### 4. Lalu program akan mencetak output berupa hello world!3.
### 5. Selain penambahan dapat juga dibuat menjadi perkalian seperti program berikut.
```
int main(){
    int a = 1, b = 2; // deklarasi variabel
    // /*same as 
    // int a = 1;
    // int b = 2;

    int calculate;
    calculate = a * b ; //1 x 2 = 2

    printf ("hello world!");
    printf("%d",calculate);
}
```
### 6. Dengan outputnya adalah hello world!2.
# dataTypeAndVariable 0
```
    #include <stdio.h>
    #include <stdint.h> //segment on checking the documentation of said standard library

    int main(){
        uint8_t eightBitVariable = 250; //when we only need a variable that have a maximum value of 255
        //                                 //we can save memory by only using that said amount of memory size
        unsigned int unsignedInt = 255; 

    printf("%d, size of eightBitVariable : %d",eightBitVariable,sizeof(eightBitVariable));
    printf("\n%d, size of the unsignedIt : %d \n",unsignedInt,sizeof(unsignedInt));

        ///*
        int integer1;
        printf("enter a number : ");
        scanf("%d",&integer1);
        printf("integer1 is = %d",integer1);
        ///*
    }
```
### 1. Library stdio.h adalah library standar untuk fungsi input output dan library stdint.h mendefinisikan tipe data tetap seperti uint8_t.
### 2. uint8_t eightBitVariable = 250;: Menginisialisasi variabel eightBitVariable dengan tipe uint8_t yang hanya menggunakan 8-bit (1 byte) memori dan dapat menyimpan nilai dari 0 sampai 255. Unsigned int unsignedInt = 255;: Menginisialisasi variabel unsignedInt dengan tipe unsigned int yang menyimpan nilai dari 0 sampai 255 dengan menggunakan 32-bit (4 byte).
### 3. Kemudian program menampilkan nilai eightBitVariable dan ukuran memori yang digunakannya (1 byte), serta menampilkan nilai unsignedInt dan ukuran memori yang digunakannya (4 byte).
### 4. Lalu didefinisikan integer1 yang selanjutnya akan mencetak enter a number : , dan menerima input dari pengguna. & pada &integer1 digunakan untuk menyimpan alamat dari input yang diberikan pengguna.
### 5. Selanjutnya program mencetak input pengguna dengan menggunakan %d yang diambil dari integer1.
### 6. Berikut adalah program sederhana dengan outputnnya adalah input pengguna, size dari input (int).
```

int main() {
    int number1;

    // Membaca input dari pengguna
    printf("Masukkan angka pertama: ");
    scanf("%d", &number1);

    printf("%d, size of number1 : %d\n", number1, sizeof(number1));

    return 0;
}
```
# dataTypeAndVariable 1

### 1. Untuk mengambil input dan mencetak output dibutuhkan format specifier, format specifier berbeda-beda tergantung tipe datanya misalnya, int (4 byte biasanya) menggunakan %d atau %i , unsigned int menggunakan %u, long int (4 byte) menggunakan %ld atau %li, dan unsgined long int menggunakan %lu. Unsgined adalah tipe data yang hanya memuat nilai tidak negatif (0,1,2,...).
### 2. Kemudian untuk nilai yang memiliki angka di belakang koma dapat digunakan tipe data float (4 byte) atau double (8 byte) berupa %f dan %lf. Serta char untuk abjad atau bilangan kecil (1 byte).
### 3. Kemudian terdapat bilangan basis 2,8,10, ataupun 16. Dengan bilangan basis 2 adalah basis yang digunakan oleh komputer (0 dan 1) , ataupun bilangan basis 10 yang digunakan dalam kehiidupan (0-9). Semakin ke kiri angka semakin besar misalnya bilangan basis 2 110 maka berarti 0 x 2^0 + 1 x 2^1 + 1 x 2^2 = 6
### 4. float floatValue = 23.4f; Mendeklarasikan variabel float dengan nilai 23.4, float floatValue1 = 20;: Mendeklarasikan variabel float dengan nilai 20, float floatValue2 = 30;: Mendeklarasikan variabel float dengan nilai 30, float dividedValue;: Mendeklarasikan variabel float untuk menyimpan hasil pembagian.



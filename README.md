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
2. Pada awalnya variabel a dideklarasikan sebagai 1 dan variabel b dideklarasikan sebagai 2.
3. Kemudian dideklarasikan variabel calculate, yang merupakan hasil tambah dari a + b (1+2).
4. Lalu program akan mencetak output berupa hello world!3.
5. Selain penambahan dapat juga dibuat menjadi perkalian seperti program berikut.
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
6. Dengan outputnya adalah hello world!2.
# dataTypeAndVariable 0
```
#include "stdio.h" 

/*
    Format Specifiers :
    %d or %i for signed integer ( 4 bytes usually)
    %u unsigned integer (4)
    %ld %li long signed integer (8)
    %lu unsigned long integer (8)
    %f float (4) (23 bits mantissa)
    %lf double (8) (52 bits mantissa), %Lf long double
    %c for char (1) , %s for string

    // little segment on binary and its families
    1001(base 2) = 11(base 8 ) = 9 (base 16) = 9 (base 10) 
    11 (base 10) = B (base 16)

    Base 2 = 0 and 1 for 1 digit of its value (its main use is to represent all things in computer)
    Base 8 = 0 to 7 for 1 digit of its value
    base 16 = 0 1 2 3 4 5 6 7 8 9 A B C D E F for 1 digit of its value
    Base 10 (decimal) = 0 to 9 for 1 digit of its value (standard human counting representation)

    (left = base n, right = base 10)
    Base 2 (111 3 bits) = 7 , 101 = 5 , 000001 = 1
    Base 8 (7)   = 7 , 10  = 8 , 000010 = 8
    base 16 (F)  = 15, FF  = 255, 
    
    //convert any base to decimal = 

*/
int main()
{
    
    
    float floatValue = 23.4f;
    float floatValue1 = 20;
    float floatValue2 = 30;

    float dividedValue;

    printf("%f", floatValue);
    dividedValue = floatValue1/floatValue2;
    printf("\n%.2f",dividedValue);
    
}
```
1. Untuk mengambil input dan mencetak output dibutuhkan format specifier, format specifier berbeda-beda tergantung tipe datanya misalnya, int (4 byte biasanya) menggunakan %d atau %i , unsigned int menggunakan %u, long int (4 byte) menggunakan %ld atau %li, dan unsgined long int menggunakan %lu.
Unsgined adalah tipe data yang hanya memuat nilai tidak negatif (0,1,2,...).
2. Kemudian untuk nilai yang memiliki angka di belakang koma dapat digunakan tipe data float (4 byte) atau double (8 byte) berupa %f dan %lf.
Serta char untuk abjad atau bilangan kecil (1 byte).
3. Kemudian terdapat bilangan basis 2,8,10, ataupun 16. Dengan bilangan basis 2 adalah basis yang digunakan oleh komputer (0 dan 1) , ataupun bilangan basis 10 yang digunakan dalam kehiidupan (0-9). Semakin ke kiri angka semakin besar misalnya bilangan basis 2 110 maka berarti 0 x 2^0 + 1 x 2^1 + 1 x 2^2 = 6
4. Lalu di deklarasikan variabel floatValue dengan nilai 23.4,variabel floatValue1 dengan nilai 20, variabel floatValue2 dengan nilai 23.4 dan variabel dividedValue dari pembagian floatValue1 dan floatValue 2.
5. Jika ingin mencetak 2 angka dibelakang koma digunakan format specifier %.2f begitupun jika nilai lain.

# dataTypeAndVariable 1
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
1. Library stdio.h adalah library standar untuk fungsi input output dan library stdint.h mendefinisikan tipe data tetap seperti uint8_t.
2. uint8_t eightBitVariable = 250;: Menginisialisasi variabel eightBitVariable dengan tipe uint8_t yang hanya menggunakan 8-bit (1 byte) memori dan dapat menyimpan nilai dari 0 sampai 255. Unsigned int unsignedInt = 255;: Menginisialisasi variabel unsignedInt dengan tipe unsigned int yang menyimpan nilai dari 0 sampai 255 dengan menggunakan 32-bit (4 byte).
3. Kemudian program menampilkan nilai eightBitVariable dan ukuran memori yang digunakannya (1 byte), serta menampilkan nilai unsignedInt dan ukuran memori yang digunakannya (4 byte).
4. Lalu didefinisikan integer1 yang selanjutnya akan mencetak enter a number : , dan menerima input dari pengguna. & pada &integer1 digunakan untuk menyimpan alamat dari input yang diberikan pengguna.
5. Selanjutnya program mencetak input pengguna dengan menggunakan %d yang diambil dari integer1.
6. Berikut adalah program sederhana dengan outputnnya adalah input pengguna, size dari input (int).
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
# Array
```
#include <stdio.h>


//data_type array_name [length];
//int       arr        [5]   = { 1,2,3,4,5 } 1 = arr[0]
//arr[0] = 1, arr[1] = 2, arr[2] = 3, arr[3] = 4, arr[4] = 5;         

int main(){

    int arr2[] = {5,6,7,8};
    printf("arr2[0] = %d, with its array size of = %d",arr2[0],sizeof(arr2));
    int arrLen = sizeof(arr2)/sizeof(arr2[3]);
    printf("\nthe length of arr2[] = %d",arrLen);  
    
    //multidimensional Array == int arr[3][4] 3 rows and 4 columns
    int twoDArr2[][5] = {{1,2,3,4,5} , {6,7,8,9,10} , {11,12,13,14,15} , {16,17,18,19,20}};
    // printf("%d",twoDArr2[][5]);
    printf("\nelement of the last row and column = %d",twoDArr2[3][4]);
    twoDArr2[3][4] = 10;
    printf("\nelement of the last row and column after assigning new value= %d",twoDArr2[3][4]);
    //*/
}
```

1.  Untuk membuat array didefinisikan tipe datanya, nama lalu panjang arraynya misalnya int arr [5] = {1,2,3,4,5}. Array dimulai dari 0 arr [0]= {1}, dan seterusnya dengan elemen terakhir diinisialisasikan ke 0 atau nilai acak.
2.  Selain itu juga bisa dikosongkan panjang arraynya lalu diikuti nilai di dalamnya misalnya int arr2 [] = {5,6,7,8}.
3.  Size dari array sendiri adalah byte dari nilai didalam array dikali banyaknya misalnya dalam arr2 karena int merupakan 4 byte maka size dr arraynya adala 4x4 = 16.
4.  Maka pada int arrLen dapat diketahui adalah 16/4 = 4.
5.  Kemudian pada multidimensional array[3][4] atau matrix 3 x 4 didefinisikan nilai-nilai di dalamnya lalu dicetak nilai terakhir dari array tersebut sebesar 20.
6.  Selanjutnya niali terakhir tadi diubah menjadi 10, dan pada pencetakan setelahnya akan mencetak nilai 10.

# Char
```
#include <stdio.h>

int main(){

    //char charArray[5] ={'a','r','u','n','d'};
    //char charArray[6] ={'a','r','u','n','d'}; //secret '\0'
    //char charArray[6]= "arund";
    printf("%s\n",charArray); //more like printing the address
    printf("%c\n",charArray[0]);
    printf("%c\n",charArray[5]); 

    // char stringHello [] = "Hello"; // 'H'(1) 'e'(2) 'l'(3) 'l'(4) 'o'(5) '\0'(6)

    printf ("%d\n",sizeof(charArray));
    printf("%c",charArray);
    printf("%s\n",charArray);

    char stringArray[][6] = {"Arund","Taib","Anton"};
    printf("%s",stringArray[2]);

}
```
1. char charArray[5] ={'a','r','u','n','d'};: Mendeklarasikan karakter charArray dengan panjang 5 elemen.
2. char charArray[6] ={'a','r','u','n','d'};: Mendeklarasikan array karakter charArray dengan panjang 6 elemen. Karakter keenam adalah karakter null terminator '\0' sebagai penanda akhir.
3. char string[6]= "arund" merupakan string yang 6 elemen yang akan diinisialisasikan arund ke dalamnya termasuk dengan null terminator '\0'.
Sehingga nantinya akan tersimpan sebagai 'a', 'r', 'u', 'n', 'd', '\0' (Perlu diingat kembali array dimulai dari 0).
4. printf("%s\n",charArray) akan mencetak array sebagai string.
5. printf("%c\n",charArray[0]) mencetak karakter pertama dari array dan printf("%c\n",charArray[5])nantinya akan mencetak karakter keenam dari array, yang merupakan '\0'.
6. char stringHello [] = "Hello" nantinya mendeklarasikan string stringHello tanpa menentukan panjangnya secara eksplisit yang didalamnya akan memuat null terminator '\0'.
7. printf ("%d\n",sizeof(stringHello)) akan mencetak size dari char stringHello , yaitu 6 x 1 byte = 6.
8. printf("%c",stringHello) mencetak karakter pertama dari stringHello, dan printf("%s\n",stringHello) akan mencetak seluruh string stringHello.
9. char stringArray[][6] = {"Arund","Taib","Anton"}; Mendeklarasikan array karakter dua dimensi stringArray dengan panjang kolom 6 serta menginisialisasi 3 string.
10. printf("%s",stringArray[2]); Mencetak string dari baris ketiga stringArray, yaitu "Anton".
11. Berikut ini adalah contoh dari Array dan Char.
```
#include <stdio.h>

int main() {
    char string[] = "Aku07";
    printf("%s dan ", string);

    printf("%c", string[0]);
    printf("%c", string[1]);
    printf("%c", string[2]);
    printf("%c", string[3]);
    printf("%c", string[4]);

    return 0;
}
```
12. Nantinya program akan mencetak Aku07 dan Aku07.

# Operator
```
#include <stdio.h>

/*  
Arithmetic Operator :
    + (addition) 2 + 3 = 5
    - , *, / 
    % (modulus) = to calculate the remainder of a divided value 
        ex : 5 % 2 =  1
             2 % 4 =  2
*/

int main(){
    /*
    //modulus
    int a = 5, b = 2, c = 4 ;
    printf("5 %% 2 equals to = %d",a%b); printf("\n2 %% 4 equals to = %d",b%c);
    //*/

    ///*
    //increment and decrement = a++,++a,i--,--i
    //++a means increment first then use the value,  a++ means use the value then increment
    int a = 1;
    a++;
    printf("%d\n",a);

    int b  =  1;
    printf("%d\n",b++);
    printf("%d\n",b);

    int c = 1;
    printf("%d\n",++c);
}
```
1. Operator aritmatika dasar dalam C meliputi penambahan (+), pengurangan (-), perkalian (*), pembagian (/), dan sisa pembagian atau modulus (%).
2. i++ berarti i ditambah 1, begitu pulla jika i-- maka i dikurang 1.
3. a++ menambahkan 1 ke a setelah digunakan sehingga nanti a menjadi 2.
4. Nilai b akan dicetak dahulu sebelum ditambah 1 (sehingga output adalah 1), lalu b menjadi 2. Baru pada printf setelahnya nilai b adalah 2. (printf("%d\n",b++))
5. Sedangkan Nilai c ditambah 1 sebelum digunakan (output adalah 2).(printf("%d\n",++c);)

# For
```
#include <stdio.h>
/*

for (initialize expression (1); test expression(2); update expression(4))
{
    //
    // body of for loop (3)
    //
}

while (test expression)
{
   // body consisting of multiple statements
}

do {
 
    // body of do-while loop    
    
} while (condition);
*/
int main(){
    int a = 10;
    ///*
    // int i = 0;
    // for(; i<10; i++,printf("%d ",i)){
    //     ;
    // }
    //*/

   // /*
    https://www.youtube.com/watch?v=0BkoXZBbhfU
    int arr[5] = {10,2,5,11,3};
    int tmp;
    for (int i = 0; i < 5 - 1; i++) {     
        // Last i elements are already in place, so the loop will only num n(5) - i - 1 times
        for (int j = 0; j < 5 - i - 1; j++) {
            if (arr[j] > arr[j + 1]){
                tmp = arr[j+1];
                arr[j+1] = arr[j];
                arr[j] = tmp;
            }
        }
    }
    for(int i =0;i<5;i++){
        printf("%d ",arr[i]);
    }
    
    a=10;
    while(a<=10){
        printf("%d",a);
        a++;
    }

    do{
        printf("%d",a);
        a++;
    }while(a<10);
}
```
1. For(initialization; condition; increment){} adalah pengulangan jika kita tahu akan berapa kali yang biasanya condition akan berhubungan dengan increment dan dimulainya pengulangan digunakan initialization.
2. While(condition){} adalah pengulangan yang ketika condition masih terpenuhi akan terus berulang.
3. Do{}While(condition) adalah pengulangan yang akan melakukan loop terlebih dahulu baru dicek kondisinya.
4. Pada kode for yang pertama akan mencetak nilai int i=0 yang dilakukan increment i++ dengan i<10, sehingga nanti akan dicetak 0-9.
5. For kedua merupakan bubble sort terdapat dua pengulangan, dimana pengulangan akan melakukan perbandingan. Jika nilai elemen saat ini lebih besar dari elemen setelahnya maka nilai ditukar posisinya. Ketika pengulangan kedua ini sudah berakhir maka akan dilakukan pengulangan pertama yang akan melakukan pengulangan kedua kembali (Membandingkan dan Menukar).
6. Kemudian for ketiga akan mencetak hasil dari array yang telah diurutkan dengan bubble sort.
7. Loop while(a<10) memeriksa apakah a kurang dari 10. Karena a dimulai dengan nilai 10, loop ini tidak akan dijalankan sama sekali.
8. Sedangkan pada do{...}While(a<10) akan dicetak 10 terlebih dahulu, baru memeriksa kondisi apakah a kurang dari 10. Karenanya a tidak kurang dari 10 maka loop tidak dijalankan lagi.

# If-Else
1. Pada if dan else if digunakan operator pembanding sama dengan (==), tidak sama dengan (!=), kurang dari dan lebih dari sama dengan (<=,>), operator not (!), operator and (&&) dan operator atau (||)
2.
```
// if(a < c ){
//     printf("a is smaller than c\n");
// } else {
//     printf("a is bigger than c\n");
// }






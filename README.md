# UAS-Dasprog
# Ujian Akhir Semester 
<br>Mata Kuliah 	: Dasar Pemrograman
<br> Nama		: Nizzami Ramdhan Arraudy
<br>NIM		        : 1227050106
<br>Jurusan		:[Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 

## Deskripsi Umum
Array adalah sebuah variabel yang punya kemampuan untuk menyimpan lebih dari 1 nilai yang memiliki tipe yang sama. Atau dalam kata lain array adalah sekumpulan data dengan tipe data yang sama. 
Sedangkan array dua dimensi adalah sebutan untuk array yang penomoran index-nya menggunakan 2 buah angka. Analogi yang sering dipakai seperti titik koordinat dalam diagram kartesius.

Diagram kartesius merupakan diagram yang biasa kita pakai untuk membuat grafik. Disini terdapat sumbu X dan sumbu Y. Sebuah titik dalam diagram kartesius ini harus disebut secara berpasangan, seperti (2,3) atau (-3, 1).
Analogi lain adalah matriks. Dalam matematika, matriks terdiri dari kolom dan baris. Kembali, untuk menentukan nilai dari sebuah matriks, kita harus sebut secara berpasangan seperti baris 1 kolom 1, atau baris 2 kolom 3, dst. 
Konsep seperti inilah yang menjadi dasar dari array 2 dimensi.

Untuk membuat array 2 dimensi di dalam bahasa C++, caranya tulis 2 kali tanda kurung siku setelah nama variabel, seperti contoh berikut:

int arr[2][2];

Baris diatas akan membuat array 2 dimensi dengan nama variabel: arr. Variabel arr ini total berisi 4 element (2 x 2). Atau jika diibaratkan sebagai matriks, disini kita membuat matriks 2 x 2.

Untuk mengakses setiap element array, penulisan index juga harus ditulis 2 kali, seperti contoh berikut:

arr[0][0] = 20;
arr[0][1] = 58;
arr[1][0] = 22;
arr[1][1] = 98;

## Source Code
```
#include <iostream>
#include <conio.h>
using namespace std;

int main() {
    cout << "Nama : Nizzami Ramdhan Arraudy" <<endl;
    cout << "NIM  : 1227050106 \n" <<endl;

    //SOAL NOMOR SATU
    cout << "=========================================\n";
    cout << "= Baris Jadi Kolom dan Kolom Jadi Baris =\n";
    cout << "=========================================\n";

    int i, j, x, y;
    int arr[10][10];

    cout << "Masukkan Banyak Baris : "; cin >> x;
    cout << "Masukkan Banyak Kolom : "; cin >> y;
    for (i = 1; i <= x; i++) {
        for (j = 1; j <= y; j++) {
            cout << "Baris ke " << i << " Kolom ke " << j << " = "; cin >> arr[i][j];
        }
    }

    cout << endl;

    cout << "Nilai Input : " <<endl;
    for (i = 1; i <= x; i++) {
        for (j = 1; j <= x; j++) {
            cout << " [ " << arr[i][j] << " ] ";
        }
        cout << endl;
    }

    cout << endl;

    cout << "Hasil Matriks : " <<endl;
    for (i = 1; i <= x; i++) {
        for (j = 1; j <= x; j++) {
            cout << " [ " << arr[j][i] << " ] " ;
        }
        cout << endl;
    }

    cout <<endl;

    //SOAL NOMOR DUA
    int baris, kolom, res;

    cout << "============================================\n";
    cout << "= Bilangan Yang Dapat Habis Dibagi 3, 5, 7 =\n";
    cout << "============================================\n";

    //input
    cout << "Masukkan Banyak Baris : "; cin >> baris;
    cout << "Masukkan Banyak Kolom : "; cin >> kolom;

    int bakol[baris][kolom];

	// input
	for (i = 1; i <= baris; i++) {
		for (j = 1; j <= kolom; j++) {
			cout << "Baris ke " << i << " Kolom ke " << j << " = ";
			cin >> bakol[i][j];
		}
	}

	cout << endl;

    //proses
  	for (i = 1; i <= baris; i++) {
		for (j = 1; j <= kolom; j++) {
			if (bakol[i][j] % 3 == 0 && bakol[i][j] % 5 == 0 && bakol[i][j] % 7 == 0) {
				cout << "Bilangan yang habis dibagi 3, 5, 7: " << bakol[i][j] << endl;
			}
		}
	}


    getch();
}
```
## Output

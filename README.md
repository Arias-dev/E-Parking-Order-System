# E-Parking-Order-System
ini merupakan project sistem parkir pada c++

#include <iostream>
#include <string.h>
#include <string>
#include <conio.h>
#include <windows.h>
#include <stdlib.h>

using namespace std;

void setcolor(unsigned short color)//buat ngubah warna teks dan background command
{
HANDLE hCon = GetStdHandle(STD_OUTPUT_HANDLE);

SetConsoleTextAttribute(hCon,color);//buat ngeset color
}

struct pengendara
{
    int choise;
    int lahan;
    char no_kendaraan[15];


};

pengendara kendaraan;


struct lahan
{
    string status_lahan [16] = {};
};

lahan lmotor;
lahan lmobil;
lahan ltruk;



void defLahan(){ //Deklarasi awal untuk mengosongkan semua lahan
if(kendaraan.choise==1)
{
    for(int i = 1; i<=29; i++){
        lmotor.status_lahan[i] = "Kosong";
    }
}

else if(kendaraan.choise==2)
{
    for(int i = 1; i<=29; i++){
        lmobil.status_lahan[i] = "Kosong";
    }
}

else if(kendaraan.choise==3)
{
    for(int i = 1; i<=29; i++){
        ltruk.status_lahan[i] = "Kosong";
    }
}



}

void SLkosong(){ // Kodingan buat liat lahan kosong

if(kendaraan.choise==1)
{
    cout << "Lahan yang tersedia adalah: ";
    for (int i=1; i<=29; i++){
        if(lmotor.status_lahan[i] == "Kosong"){
        cout << i << ", ";
        }
    }
    cout << endl;
}

else if(kendaraan.choise==2)
{
    cout << "Lahan yang tersedia adalah: ";
    for (int i=1; i<=29; i++){
        if(lmobil.status_lahan[i] == "Kosong"){
        cout << i << ", ";
        }
    }
    cout << endl;
}

else if(kendaraan.choise==3)
{
    cout << "Lahan yang tersedia adalah: ";
    for (int i=1; i<=29; i++){
        if(ltruk.status_lahan[i] == "Kosong"){
        cout << i << ", ";
        }
    }
    cout << endl;
}



}

void SLisi(){ // Kodingan buat liat lahan terisi

    cout << "Lahan yang terisi adalah: ";
if (kendaraan.choise==1)
 {
    for (int i=1; i<=29; i++){
        if(lmotor.status_lahan[i] == "Isi"){
        cout << i << ", ";
        }
    }
    cout << endl;
 }
else if (kendaraan.choise==2)
 {
     for (int i=1; i<=29; i++){
        if(lmobil.status_lahan[i] == "Isi"){
        cout << i << ", ";
        }
    }
    cout << endl;

 }
else if (kendaraan.choise==3)
 {
     for (int i=1; i<=29; i++){
        if(ltruk.status_lahan[i] == "Isi"){
        cout << i << ", ";
        }
    }
    cout << endl;
 }
}

void isiKosong(){ // Kodingan buat mengisi lahan kosong
if (kendaraan.choise==1)
{
    cout << "Lahan yang tersedia adalah: ";
    for (int i=1; i<=29; i++){
        if(lmotor.status_lahan[i] == "Kosong"){
        cout << i << ", ";
        }
    }
    int pil;
    cout << endl << "Masukkan pilihan anda: "; cin >> pil;

    if(lmotor.status_lahan[pil] == "Kosong"){
        lmotor.status_lahan[pil] = "Isi";
        cout << "Berhasil" << endl;
    } else {
        cout << "Maaf, lahan sudah terisi" << endl;
    }
}

else if (kendaraan.choise==2)
{
    cout << "Lahan yang tersedia adalah: ";
    for (int i=1; i<=29; i++){
        if(lmobil.status_lahan[i] == "Kosong"){
        cout << i << ", ";
        }
    }
    int pil;
    cout << endl << "Masukkan pilihan anda: "; cin >> pil;

    if(lmobil.status_lahan[pil] == "Kosong"){
        lmobil.status_lahan[pil] = "Isi";
        cout << "Berhasil" << endl;
    } else {
        cout << "Maaf, lahan sudah terisi" << endl;
    }
}


else if (kendaraan.choise==3)
{
    cout << "Lahan yang tersedia adalah: ";
    for (int i=1; i<=29; i++){
        if(ltruk.status_lahan[i] == "Kosong"){
        cout << i << ", ";
        }
    }
    int pil;
    cout << endl << "Masukkan pilihan anda: "; cin >> pil;

    if(ltruk.status_lahan[pil] == "Kosong"){
        ltruk.status_lahan[pil] = "Isi";
        cout << "Berhasil" << endl;
    } else {
        cout << "Maaf, lahan sudah terisi" << endl;
    }
}




}

void kosongIsi(){ // Kodingan buat menosongkan lahan terisi
if (kendaraan.choise==1)
{
    cout << "Lahan yang terisi adalah: ";
    for (int i=1; i<=29; i++){
        if(lmotor.status_lahan[i] == "Isi"){
        cout << i << ", ";
        }
    }
    int pil;
    cout << "Masukkan pilihan anda: "; cin >> pil;

    if(lmotor.status_lahan[pil] == "Isi"){
        lmotor.status_lahan[pil] = "Kosong";
        cout << "Berhasil" << endl;
    } else {
        cout << "Maaf, lahan sudah kosong" << endl;
    }
}

else if (kendaraan.choise==2)
{
    cout << "Lahan yang terisi adalah: ";
    for (int i=1; i<=29; i++){
        if(lmobil.status_lahan[i] == "Isi"){
        cout << i << ", ";
        }
    }
    int pil;
    cout << "Masukkan pilihan anda: "; cin >> pil;

    if(lmobil.status_lahan[pil] == "Isi"){
        lmobil.status_lahan[pil] = "Kosong";
        cout << "Berhasil" << endl;
    } else {
        cout << "Maaf, lahan sudah kosong" << endl;
    }
}

else if (kendaraan.choise==3)
{
    cout << "Lahan yang terisi adalah: ";
    for (int i=1; i<=29; i++){
        if(ltruk.status_lahan[i] == "Isi"){
        cout << i << ", ";
        }
    }
    int pil;
    cout << "Masukkan pilihan anda: "; cin >> pil;

    if(ltruk.status_lahan[pil] == "Isi"){
        ltruk.status_lahan[pil] = "Kosong";
        cout << "Berhasil" << endl;
    } else {
        cout << "Maaf, lahan sudah kosong" << endl;
    }
}




}



void mainMenu(){
    int pil;
cout<<"==============================="<<endl;
cout<<"            MAIN MENU          "<<endl;
cout<<"==============================="<<endl;
cout<< "1. Lihat lahan kosong         "<<endl;
cout<< "2. Lihat lahan terisi         "<<endl;
cout<< "3. Pilih lahan                "<<endl;
cout<< "4. Kosongkan lahan            "<<endl;
cout<< "5. Keluar Aplikasi            "<<endl;
cout<<"==============================="<<endl<<endl;
    cout << "Pilih operasi: "; cin >> pil;
    system("cls");

    switch(pil){
        case 1: SLkosong(); break;system("cls");
        case 2: SLisi(); break;system("cls");
        case 3: isiKosong(); break;system("cls");
        case 4: kosongIsi(); break;system("cls");
        case 5: cout<<"TERIMA KASIH"<<endl;exit(5); break;system("cls");

    }
    mainMenu();
}


void jenis_kendaraan()
{
    cout<<"=========================================="<<endl;
    cout<<" 1. MOTOR / 2. MOBIL / 3. TRUK ATAU BUS   "<<endl;
    cout<<"=========================================="<<endl;
}



int main()
{

    noken:
    setcolor(02);
    cout<<"MASUKAN NOMOR KENDARAAN  : "; cin.getline(kendaraan.no_kendaraan,15);
    if(kendaraan.no_kendaraan==NULL)
    {
      cout<<"MASUKAN ULANG NO KENDARAAN ANDA"<<endl;
      goto noken;
    }
    jenis:
    setcolor(04);
    jenis_kendaraan();
    setcolor(06);
    cout<<"MASUKAN JENIS KENDARAAN  : "; cin>>kendaraan.choise;
    system("cls");
         if (kendaraan.choise==1)
    {
      cout<<"JENIS KENDARAAN : MOTOR "<<endl<<endl;

      cout<<"|=======================|"<<endl;
      cout<<"|         BLOK A        |"<<endl;
      cout<<"|=======================|"<<endl;
      cout<<"|=======================|"<<endl;
      cout<<"| 1  2  3  4  5  6  7   |"<<endl;
      cout<<"| 8  9  10 11 12 13 14  |"<<endl;
      cout<<"| 15 16 17 18 19 20 21  |"<<endl;
      cout<<"| 22 23 24 25 26 27 28  |"<<endl;
      cout<<"|=======================|"<<endl<<endl;

    }
   else if (kendaraan.choise==2)
    {
      cout<<"JENIS KENDARAAN : MOBIL "<<endl<<endl;

      cout<<"|=======================|"<<endl;
      cout<<"|         BLOK B        |"<<endl;
      cout<<"|=======================|"<<endl;
      cout<<"|=======================|"<<endl;
      cout<<"| 1  2  3  4  5  6  7   |"<<endl;
      cout<<"| 8  9  10 11 12 13 14  |"<<endl;
      cout<<"| 15 16 17 18 19 20 21  |"<<endl;
      cout<<"| 22 23 24 25 26 27 28  |"<<endl;
      cout<<"|=======================|"<<endl<<endl;


    }
   else if (kendaraan.choise==3)
    {
      cout<<"JENIS KENDARAAN : TRUK ATAU BUS "<<endl<<endl;

      cout<<"|=======================|"<<endl;
      cout<<"|         BLOK C        |"<<endl;
      cout<<"|=======================|"<<endl;
      cout<<"|=======================|"<<endl;
      cout<<"| 1  2  3  4  5  6  7   |"<<endl;
      cout<<"| 8  9  10 11 12 13 14  |"<<endl;
      cout<<"| 15 16 17 18 19 20 21  |"<<endl;
      cout<<"| 22 23 24 25 26 27 28  |"<<endl;
      cout<<"|=======================|"<<endl<<endl;


    }
   else
    {
       cout<<"ANDA SALAH MEMASUKAN PILIHAN "<<endl;
       goto jenis;

    }
    setcolor(01);
    defLahan();
    setcolor(03);
    mainMenu();




}


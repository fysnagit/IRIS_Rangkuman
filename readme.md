OBJECT ORIENTED PROGRAMING (OOP)

Secara garis besar OOP merupakan paradigma dalam membuat program yang dimana program itu diklasifikasikan berdasarkan objek
OOP ini diciptakan agar mempermudah dalam pembuatan kode
Dalam C++ OOP dapat dibuat dengan menggunakan class.

	Abstrak Class
	Dalam Class OOP terdapat property dan method. 
	1.) Property ini berisi variabel variabel yang dibutuhkan untuk pembuatan class.
	2.) Method berisi fungsi-fungsi yang digunakan untuk pembuatan class
 
	Didalam Class ini terdapat beberapa pembagian yaitu
	1.) Private
	    Bagian private ini fungsi maupun variabel hanya dapat diakses di dalam class.
	2.) Protected
	    Protected ini mirip dengan private namun keistimewaan dari protected dapat digunakan untuk inherit
	3.) Public
	    Pada bagian publik ini property maupun method dapat diakses di luar class. dengan cara membuat objek dari class tersebut
	
	Contructor
	Dalam pembuatan suatu objek terkadang diperlukan pengaturan awal. Constructor ini berfungsi sebagai penerima pengaturan awal lewat parameter
	
	Inherit
	Inherit ini salah satu konsep yang sering digunakan dalam pembuatan class karena sangat efisien
	Secara garis besar konsep dari inherit ini adalah mewarisi isi dari suatu class ke class yang lain.

	Polymorfisme
	Polimorfisme merupakan kemampuan objekobjek yang berbeda kelas namun terkait dalam pewarisan untuk merespon secara berbeda terhadap suatu pesan yang sama.

Contoh Kode OOP dalam C++
#include<iostream>
using namespace std;

class Segitiga{
  public:
  int alas,tinggi;
  
};


class SegitigaSamaSisi:public Segitiga{
  public:

  SegitigaSamaSisi(int alasnya,int tingginya){
    this->alas = alasnya;
    this->tinggi=tingginya;
  }

  float cariluas(){
    return this->alas*this->tinggi*0.5;
  }
  float carikeliling(){
    return this->alas*3;
  }
};

class SegitigaSembarang:public Segitiga{
  private:
  int sisi;
  public:

  SegitigaSembarang(int alasnya,int tingginya,int sisinya = 69){
    this->alas  = alasnya;
    this->tinggi =tingginya;
    this->sisi = sisinya;
  }

  float cariluas(){
    return this->alas*this->tinggi*0.5;
  }

  float carikeliling(){
    return this->sisi*4;
  }
};

int main()
{
  SegitigaSamaSisi sgtSisi(3,4);
  SegitigaSembarang sgtSembarang(5,5);

  cout<<"SEGITIGA SAMA SISI"<<endl;
  cout<<sgtSisi.carikeliling()<<endl;
  cout<<sgtSisi.cariluas()<<endl;

  cout<<"SEGITIGA SEMBARANG"<<endl;
  cout<<sgtSembarang.carikeliling()<<endl;
  cout<<sgtSembarang.cariluas()<<endl;

  
  return 0;
}


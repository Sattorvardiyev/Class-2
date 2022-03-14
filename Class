//.Eshik va deraza class larini yarating
//va ularni bog’lovchi funksiyalar yarating
#include<iostream>
using namespace std;

namespace d_fazo { //Yangi nomlar fazosi
  class Eshik {
  protected:
    int olchami, ishlab_chiqarilgan_yili;
    string materiali;

  public:
    Eshik() {}
    Eshik(int olchami, int yil, string materiali) {
      this->olchami = olchami;
      this->ishlab_chiqarilgan_yili = yil;
      this->materiali =materiali;
    }
    static void qidirish(Eshik* massiv, int n, string mat) {
        //qidirish materiali bo'yicha
      for (int i = 0; i <n; i++) {
        if (massiv[i].materiali ==mat) massiv[i].print();
      }
    }
    static void saralash(Eshik* massiv, int n) {
        //saralash o'lcham bo'yicha
      for (int i = 0; i <n; i++) {
        for (int j = i + 1; j <n; j++) {
          if (massiv[i].olchami >massiv[j].olchami)
            swap(massiv[i], massiv[j]);
        }
      }
    }
    void ozgartirish(int olchami, int yil, string materiali) {
        //o'zgartirish metodi
      this->olchami = olchami;
      this->ishlab_chiqarilgan_yili = yil;
      this->materiali =materiali;
    }
    void print() {
      cout <<"\nOlchami: "<<olchami;
      cout  <<"\nIshlab chiqarilgan yili: "<< ishlab_chiqarilgan_yili;
        cout<<"\nMateriali : "<< materiali << endl;
    }
  };
  class Deraza :public Eshik {
  public:
    Deraza(){}
    Deraza(int olchami, int yil, string materiali) {
      this->olchami = olchami;
      this->ishlab_chiqarilgan_yili = yil;
      this->materiali =materiali;
    }
  };
}

int main() {
  using namespace d_fazo;
  // Yangi hosil qilingan nomlar fazosidan foydalanish
  int n, m;
  cout <<"Nechta Eshik haqida ma'lumot kiritmoqchisiz?"<<endl<<"n = "; cin >> n;
  Eshik* eshiklar;
  eshiklar = new Eshik[n];
  if (n) cout <<"\nEshiklar haqida ma'lumotlarni kiritish:"<<endl;
  for (int i = 0; i < n; i++) {
    int olchami, yili;
    string materiali;
    cout <<"Eshikning olchami: "; cin >> olchami;
    cout <<"Eshikni ishlab chiqarilgan yili: "; cin >> yili;
    cout <<"Eshikning materiali: "; cin >> materiali;
    eshiklar[i] =Eshik(olchami, yili, materiali);
  }
  cout <<"\nEshiklarni saralash, olcham bo'yicha:\n";
  eshiklar[0].saralash(eshiklar, n);
  //Ekranga chiqarish:
  for (int i = 0; i < n; i++) {
    eshiklar[i].print();
  }
  cout <<"\nQidirish: \nMaterialni kiriting: ";
  string man; cin >> man;
  eshiklar[0].qidirish(eshiklar, n, man);
cout <<"Nechta deraza haqida ma'lumot kiritmoqchisiz?\nn = "; cin >> m;
  Deraza* derazalar;
  derazalar = new Deraza[m];
  if (m) cout <<"\nDerazalar haqida ma'lumotlarni kiritish:\n\n";
  for (int i = 0; i < m; i++) {
    int olchami, yili;
    string material;
    cout <<"Derazaning olchami: "; cin >> olchami;
    cout <<"Derazaning  ishlab chiqarilgan yili: "; cin >> yili;
    cout <<"Derazaning materiali: "; cin >> material;
    derazalar[i] =Deraza(olchami, yili, material);
  }
  cout <<"\nDErazani saralash olcham boyicha:\n";
  derazalar[0].saralash(derazalar, m);
  //Ekranga chiqarish:
  for (int i = 0; i < m; i++) {
    derazalar[i].print();
  }
  cout <<"\nQidirish: Materialni kiriting: ";
cin >> man;
  derazalar[0].qidirish(derazalar, m, man);

}

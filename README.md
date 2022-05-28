# static-sinif-ve-uyeler
Static Sınıf ve Üyeler   



```

using System;

namespace staticClass
{
    class MainClass
    {
        public static void Main(string[] args)
        {
            Console.WriteLine("Çalısan sayisi: {0} ", Calisan.CalisanSayisi);
            Calisan calisan = new Calisan("Ali", "Demir", "HR");
            Console.WriteLine("Çalışan Sayısı: {0}", Calisan.CalisanSayisi);
        }


        class Calisan
        {
            private static int calisanSayisi;

            public static int CalisanSayisi { get => calisanSayisi; }

            private string Isim;
            private string Soyisim;
            private string Departman;

            static Calisan()
            {
                calisanSayisi = 0;
            }

            public Calisan(string Isim, string Soyisim, string departman)
            {
                this.Isim = Isim;
                this.Soyisim = Soyisim;
                this.Departman = departman;
                calisanSayisi++;
            }
                
        }
    }
}



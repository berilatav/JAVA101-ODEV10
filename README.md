Sınıf Geçme Durumu Hesaplama

Eğer girilen ders notları 0 veya 100 arasında değil ise ortalamaya katılmasın.Geçme notu 55 olarak al.

import java.util.Scanner;

public class Odev10 {
    public static void main(String[] args) {

        int mat,fizik,turkce,kimya,muzik ;
        double ortalama ;

        Scanner input = new Scanner(System.in);

        System.out.println("Matematik notunuzu giriniz: ");
        mat = input.nextInt();

        System.out.println("Fizik notunuzu giriniz: ");
        fizik = input.nextInt();

        System.out.println("Türkçe notunuzu giriniz: ");
        turkce = input.nextInt();

        System.out.println("Kimya notunuzu giriniz: ");
        kimya = input.nextInt();

        System.out.println("Müzik notunuzu giriniz: ");
        muzik = input.nextInt();

        if(mat < 0 || mat > 100){
            ortalama = (fizik + turkce + kimya + muzik) / 4 ;
        }
        if(fizik < 0 || fizik > 100){
            ortalama = (mat + turkce + kimya + muzik) / 4 ;
        }
        if (turkce < 0 || turkce > 100){
            ortalama = (mat + fizik + kimya + muzik) / 4 ;
        }
        if (kimya < 0 || kimya > 100){
            ortalama = (mat + fizik + turkce + muzik) / 4 ;
        }
        if (muzik < 0 || muzik > 100){
            ortalama = (mat + fizik + turkce + kimya ) / 4 ;
        }
        else {
            ortalama = (mat + fizik + turkce + kimya + muzik) / 5 ;
        }
        System.out.println("Ortalamanız : " + ortalama );

        if (ortalama > 55){
            System.out.println("Sınıfı geçtiniz.Tebrikler ! ");
        }
        else {
            System.out.println("Sınıfta kaldınız. ");
        }




    }
}

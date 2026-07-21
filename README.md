# Terminal Tabanli Mini Stok ve Satis Sistemi

Bu projede amac, Python kullanarak Linux terminali uzerinden calisan basit bir stok ve satis sistemi gelistirmektir.

Projeyi yaparken herhangi bir IDE kullanilmayacak. Kod yazma, dosya olusturma, klasor yonetimi ve programi calistirma islemleri terminal uzerinden yapilacak.

## Proje Amaci

Bu odevde ogrencinin asagidaki konulari pratik etmesi beklenir:

- Linux terminal kullanimi
- Python ile kullanicidan veri alma
- Dosya okuma ve dosyaya yazma
- Listeleme, arama ve guncelleme islemleri
- Basit stok ve satis mantigi
- Hata kontrolu
- Programi terminalden manuel calistirma

## Baslangic

Once terminalden proje klasoru olustur:

```bash
mkdir stok_sistemi
cd stok_sistemi
touch main.py
```

Program asagidaki komutla calistirilmalidir:

```bash
python3 main.py
```

## Proje Kurallari

1. Kod sadece terminal uzerinden yazilacak.
2. Program `python3 main.py` komutuyla calisacak.
3. Veriler dosyada tutulacak.
4. Program kapaninca veriler silinmeyecek.
5. Hatali girislerde program cokmeyecek.

## Kullanilacak Dosyalar

Projede en az iki veri dosyasi kullanilmalidir:

```text
urunler.txt
satislar.txt
```

### urunler.txt

Urun bilgileri bu dosyada tutulacak.

Ornek veri formati:

```text
elma,20,30,50,meyve
armut,15,25,40,meyve
ekmek,8,12,100,gida
```

Alanlar sirasiyla:

```text
urun_adi,alis_fiyati,satis_fiyati,stok_adedi,kategori
```

### satislar.txt

Yapilan satislar bu dosyada tutulacak.

Ornek veri formati:

```text
elma,3,90,30
ekmek,5,60,20
```

Alanlar sirasiyla:

```text
urun_adi,satilan_adet,toplam_satis,toplam_kar
```

## Program Menusu

Program calistiginda kullaniciya asagidaki gibi bir menu gosterilmelidir:

```text
1 - Urun ekle
2 - Urunleri listele
3 - Urun ara
4 - Satis yap
5 - Stok raporu
6 - Cikis
```

Kullanici secim yaptikca ilgili islem calismalidir. Islem bittikten sonra program tekrar menuye donmelidir.

## Gorevler

### 1. Urun Ekleme

Kullanicidan asagidaki bilgiler alinmalidir:

```text
Urun adi:
Alis fiyati:
Satis fiyati:
Stok adedi:
Kategori:
```

Girilen bilgiler `urunler.txt` dosyasina kaydedilmelidir.

Ornek:

```text
Urun adi: elma
Alis fiyati: 20
Satis fiyati: 30
Stok adedi: 50
Kategori: meyve
```

Dosyaya yazilacak hali:

```text
elma,20,30,50,meyve
```

### 2. Urunleri Listeleme

`urunler.txt` dosyasindaki tum urunler ekrana yazdirilmalidir.

Ornek cikti:

```text
Urun: elma
Alis fiyati: 20 TL
Satis fiyati: 30 TL
Stok: 50
Kategori: meyve
--------------------
Urun: armut
Alis fiyati: 15 TL
Satis fiyati: 25 TL
Stok: 40
Kategori: meyve
--------------------
```

### 3. Urun Arama

Kullanici urun adi girerek arama yapabilmelidir.

Ornek:

```text
Aranacak urun: elma
```

Bulunursa:

```text
Urun: elma
Alis fiyati: 20 TL
Satis fiyati: 30 TL
Stok: 50
Kategori: meyve
```

Bulunamazsa:

```text
Urun bulunamadi.
```

### 4. Satis Yapma

Kullanici satilacak urun adini ve adet bilgisini girmelidir.

Ornek:

```text
Satilacak urun: elma
Adet: 3
```

Program sunlari yapmalidir:

- Urunun var olup olmadigini kontrol etmeli
- Stok miktarinin yeterli olup olmadigini kontrol etmeli
- Stoktan satilan adedi dusmeli
- Satis bilgisini `satislar.txt` dosyasina kaydetmeli
- Toplam satis tutarini hesaplamali
- Toplam kar miktarini hesaplamali

Ornek hesap:

```text
Alis fiyati: 20 TL
Satis fiyati: 30 TL
Satilan adet: 3

Toplam satis: 90 TL
Toplam kar: 30 TL
```

Ornek cikti:

```text
elma urununden 3 adet satildi.
Toplam satis: 90 TL
Toplam kar: 30 TL
Kalan stok: 47
```

### 5. Stok Raporu

Program stok ve satis bilgilerine gore basit bir rapor olusturmalidir.

Raporda en az asagidaki bilgiler bulunmalidir:

- Toplam satis tutari
- Toplam kar
- Stokta az kalan urunler

Stok adedi 5 veya daha az olan urunler "az kalan urun" olarak kabul edilebilir.

Ornek cikti:

```text
Toplam satis: 450 TL
Toplam kar: 120 TL

Stokta az kalan urunler:
- ekmek: 4 adet kaldi
- sut: 2 adet kaldi
```

## Hata Kontrolu

Program asagidaki durumlarda cokmemelidir:

- Kullanici menuye gecersiz secim girerse
- Urun bulunamazsa
- Satis icin yeterli stok yoksa
- Fiyat veya adet alanina sayi yerine metin girilirse
- Veri dosyasi henuz olusmamissa

Ornek hata mesajlari:

```text
Gecersiz secim yaptiniz.
Urun bulunamadi.
Yeterli stok yok.
Lutfen sayisal bir deger girin.
```

## Teslim Beklentisi

Proje tamamlandiginda asagidaki dosyalar bulunmalidir:

```text
stok_sistemi/
  main.py
  urunler.txt
  satislar.txt
```

Ogrenci programi terminalden calistirip urun ekleme, listeleme, arama, satis yapma ve rapor alma islemlerini gosterebilmelidir.

## Ekstra Gelistirme Fikirleri

Bu kisim zorunlu degildir. Projeyi bitiren ogrenci isterse asagidaki ozellikleri ekleyebilir:

- Urun silme
- Urun guncelleme
- Kategoriye gore listeleme
- En cok satilan urunu gosterme
- Gunluk satis raporu


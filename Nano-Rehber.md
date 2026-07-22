# Nano Kullanim Rehberi

Bu rehber, Linux terminalinde `nano` ile dosya olusturmayi, duzenlemeyi, kaydetmeyi ve cikmayi yeni baslayan biri icin basit sekilde anlatir.

## Nano Nedir?

`nano`, terminal uzerinden kullanilan basit bir metin editorudur.

Python dosyasi, not dosyasi veya ayar dosyasi yazmak icin kullanilabilir.

Ornek:

```bash
nano main.py
```

Bu komut `main.py` dosyasini nano ile acar. Dosya yoksa yeni dosya olusturur.

## Nano Ile Dosya Acma

Terminalde asagidaki komutu yaz:

```bash
nano dosya_adi
```

Ornek:

```bash
nano main.py
```

Eger `main.py` varsa acilir. Yoksa bos bir dosya olarak acilir.

## Nano Ekrani

Nano acildiginda ekranda yazmaya baslayabilirsin.

En altta bazi kisayollar gorunur:

```text
^G Help      ^O Write Out      ^W Where Is      ^K Cut
^X Exit      ^R Read File      ^\ Replace       ^U Paste
```

Buradaki `^` isareti `Ctrl` tusu anlamina gelir.

Yani:

```text
^X = Ctrl + X
^O = Ctrl + O
^W = Ctrl + W
```

## Yazi Yazma

Nano acildiktan sonra direkt yazmaya baslayabilirsin.

Ornek olarak `main.py` icine sunu yaz:

```python
print("Merhaba dunya")
```

## Dosyayi Kaydetme

Dosyayi kaydetmek icin:

```text
Ctrl + O
```

Tuslarina bas.

Nano sana dosya adini sorar:

```text
File Name to Write: main.py
```

Dosya adi dogruysa:

```text
Enter
```

tusuna bas.

Dosya kaydedilir.

## Nano'dan Cikma

Nano'dan cikmak icin:

```text
Ctrl + X
```

tuslarina bas.

Eger dosyada degisiklik yaptiysan nano sana kaydetmek isteyip istemedigini sorar.

```text
Save modified buffer?
Y Yes
N No
```

Kaydetmek istiyorsan:

```text
Y
```

Kaydetmeden cikmak istiyorsan:

```text
N
```

## En Cok Kullanilan Kisayollar

| Kisayol | Anlami |
| --- | --- |
| `Ctrl + O` | Dosyayi kaydet |
| `Enter` | Kaydetme ismini onayla |
| `Ctrl + X` | Nano'dan cik |
| `Ctrl + W` | Dosya icinde arama yap |
| `Ctrl + K` | Satiri kes |
| `Ctrl + U` | Kesilen satiri yapistir |
| `Ctrl + C` | Imlecin bulundugu satir ve sutunu goster |
| `Ctrl + G` | Yardim ekranini ac |

## Arama Yapma

Dosya icinde bir kelime aramak icin:

```text
Ctrl + W
```

tuslarina bas.

Aranacak kelimeyi yaz:

```text
urun
```

Sonra:

```text
Enter
```

tusuna bas.

Nano kelimeyi dosya icinde bulursa imleci oraya goturur.

## Satir Kesme ve Yapistirma

Bulundugun satiri kesmek icin:

```text
Ctrl + K
```

Kesilen satiri yapistirmak icin:

```text
Ctrl + U
```

Bu ozellik kod satirlarini tasirken kullanislidir.

## Dosya Kaydetmeden Cikmak

Eger yanlis bir sey yazdiysan ve kaydetmeden cikmak istiyorsan:

```text
Ctrl + X
```

Sonra nano sorarsa:

```text
Save modified buffer?
```

Burada:

```text
N
```

tusuna bas.

Bu sekilde degisiklikler kaydedilmeden cikilir.

## Python Dosyasi Yazma Ornegi

Terminalde dosya olustur:

```bash
nano main.py
```

Icine sunu yaz:

```python
isim = input("Adinizi girin: ")
print("Merhaba", isim)
```

Kaydet:

```text
Ctrl + O
Enter
```

Cik:

```text
Ctrl + X
```

Programi calistir:

```bash
python3 main.py
```

Ornek calisma:

```text
Adinizi girin: Ali
Merhaba Ali
```

## Basit Calisma Alistirmasi

Asagidaki adimlari terminalde uygula:

1. Yeni bir klasor olustur:

```bash
mkdir nano_deneme
```

2. Klasore gir:

```bash
cd nano_deneme
```

3. Python dosyasi olustur:

```bash
nano selam.py
```

4. Dosyanin icine su kodu yaz:

```python
print("Nano ile ilk Python dosyam")
```

5. Dosyayi kaydet:

```text
Ctrl + O
Enter
```

6. Nano'dan cik:

```text
Ctrl + X
```

7. Programi calistir:

```bash
python3 selam.py
```

Beklenen cikti:

```text
Nano ile ilk Python dosyam
```

## Sik Yapilan Hatalar

### Ctrl + O yaptim ama kaydetmedi

`Ctrl + O` yaptiktan sonra `Enter` tusuna basman gerekir.

### Ctrl + X yaptim, soru sordu

Dosyada degisiklik yapmissindir. Kaydetmek istiyorsan `Y`, kaydetmeden cikmak istiyorsan `N` tusuna bas.

### Dosya adini yanlis yazdim

Nano'dan cik. Sonra terminalde dogru dosya adiyla tekrar ac:

```bash
nano dogru_dosya_adi.py
```

### Kod calismiyor

Dosyayi kaydettiginden emin ol:

```text
Ctrl + O
Enter
```

Sonra tekrar calistir:

```bash
python3 main.py
```

## Kisa Ozet

Nano kullanirken en onemli uc sey:

```text
Ctrl + O  -> Kaydet
Enter     -> Kaydetmeyi onayla
Ctrl + X  -> Cik
```

Bunlari biliyorsan nano ile temel dosya yazma ve duzenleme islemlerini yapabilirsin.

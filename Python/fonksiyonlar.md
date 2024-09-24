# Python'da Fonksiyonlar: Baştan Sona Detaylı Bir Rehber

## 1. Fonksiyon Nedir?

Bir fonksiyon, belirli bir görevi yerine getiren ve gerektiğinde tekrar kullanılabilen kod bloklarıdır. Fonksiyonlar sayesinde kodlarımızı daha düzenli, okunabilir ve tekrar kullanılabilir hale getirebiliriz.

## 2. Neden Fonksiyon Kullanırız?

- **Kod Tekrarını Önlemek:** Aynı işlemi birden fazla yerde yapmanız gerekiyorsa, bu işlemi bir fonksiyon içine alarak kod tekrarını önleyebilirsiniz.
- **Kod Düzenini Sağlamak:** Kodunuzu mantıksal parçalara ayırarak daha düzenli ve anlaşılır hale getirebilirsiniz.
- **Bakımı Kolaylaştırmak:** Fonksiyonlar sayesinde kodunuzun belirli bölümlerini kolayca güncelleyebilir veya değiştirebilirsiniz.

## 3. Python'da Fonksiyon Tanımlama

### 3.1. Temel Sözdizimi

```python
def fonksiyon_adi(parametreler):
    # Fonksiyonun yaptığı işler
    return sonuç
```
- **def** anahtar kelimesi ile fonksiyon tanımlanır.
- **fonksiyon_adi** fonksiyonun adıdır ve küçük harflerle yazılması tercih edilir.
- **parametreler** fonksiyona dışarıdan gönderilen verilerdir (isteğe bağlıdır).
- **return** fonksiyonun çağrıldığı yere geri döndürdüğü değeri belirtir (isteğe bağlıdır).

### 3.2. Örnek: Parametresiz ve Dönüş Değeri Olmayan Fonksiyon

```python
def merhaba_de():
    print("Merhaba!")
```
### 3.3. Örnek: Parametre Alan ve Değer Döndüren Fonksiyon

```python
def toplama(a, b):
    toplam = a + b
    return toplam
```

**Kullanımı:**
```python
sonuc = toplama(5, 3)
print(sonuc)  # Çıktı: 8
```

## 4. Fonksiyon Parametreleri ve Argümanlar

- **Parametreler:** Fonksiyon tanımlanırken parantez içinde belirtilen değişkenlerdir.
- **Argümanlar:** Fonksiyon çağrılırken parametrelere karşılık gelen değerlerdir.

### 4.1. Varsayılan Parametreler

Fonksiyon parametrelerine varsayılan değerler atayabilirsiniz.

```python
def selamla(isim="Misafir"):
    print(f"Merhaba, {isim}!")
```
**Kullanımı:**
```python
selamla("Ahmet")  # Çıktı: Merhaba, Ahmet!
selamla()         # Çıktı: Merhaba, Misafir!
```
### 4.2. Anahtar Kelime Argümanları

Anahtar kelime argümanları, fonksiyon çağrılırken parametrelerin sırasını belirtmek zorunda kalmadan, parametre isimlerine karşılık gelen argümanları belirtmenize olanak tanır. Bu, kodun daha okunabilir olmasını sağlar ve parametrelerin sırası önemli olmadığında kullanışlıdır.

```python
def bilgiler(isim, yas, sehir):
    print(f"İsim: {isim}, Yaş: {yas}, Şehir: {sehir}")
```
**Kullanımı:**
```python
bilgiler(yas=25, sehir="İstanbul", isim="Ayşe")
```
## 5. *args ve **kwargs ile Esnek Parametreler

Python'da fonksiyonlara esnek sayıda argüman geçirmek için iki özel sözdizimi kullanılır: `*args` ve `**kwargs`. Bu yapıların kullanılması, fonksiyonların değişken sayıda parametre alabilmesini sağlar.

### 5.1. *args (Arbitrary Arguments)

`*args`, bir fonksiyona belirsiz sayıda pozisyonel argüman geçirmemizi sağlar. Fonksiyonun içinde `*args` bir **tuple** olarak davranır ve gönderilen tüm argümanlar bu tuple'da toplanır.

```python
def toplam(*sayilar):
    toplam = 0
    for sayi in sayilar:
        toplam += sayi
    return toplam
```
**Kullanımı:**
```python
print(toplam(1, 2, 3))         # Çıktı: 6
print(toplam(4, 5, 6, 7, 8))   # Çıktı: 30
```

Bu örnekte, `toplam` fonksiyonu değişken sayıda argüman alabilir. Her bir sayı, `*sayilar` parametresi sayesinde bir tuple içinde toplanır.
### 5.2. **kwargs (Keyword Arguments)

`**kwargs`, bir fonksiyona değişken sayıda **anahtar kelime argümanı** geçmenizi sağlar. Bu argümanlar, fonksiyon içinde bir **dictionary (sözlük)** olarak tutulur ve anahtar-değer çiftleri şeklinde işlenir.

Fonksiyona anahtar kelime argümanları gönderdiğinizde, Python bu argümanları bir sözlük içinde toplar. Bu sayede, değişken sayıda anahtar kelime argümanı gönderebilir ve bu argümanları esnek bir şekilde işleyebilirsiniz.

#### Örnek:

```python
def bilgiler(**kwargs):
    for anahtar, deger in kwargs.items():
        print(f"{anahtar}: {deger}")
```
**Kullanımı:**
```python
bilgiler(isim="Mehmet", yas=30, sehir="Ankara")
```

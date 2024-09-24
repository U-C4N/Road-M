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
## 6. return İfadesi ve Fonksiyonun Dönüş Değeri

`return` ifadesi, bir fonksiyonun çalışması tamamlandığında bir **değer döndürmesini** sağlar. Fonksiyonun çağrıldığı noktada bu döndürülen değer kullanılabilir. Eğer bir fonksiyon içerisinde `return` ifadesi kullanılmazsa, fonksiyon **varsayılan olarak** `None` döndürür.

### 6.1. return Kullanımı

Bir fonksiyonun sonucunu döndürmek için `return` ifadesi kullanılır. Döndürülen değer, fonksiyonun çağrıldığı yere geri gönderilir.

#### Örnek:

```python
def kare(sayi):
    return sayi ** 2
```
**Kullanımı:**
```python
sonuc = kare(4)
print(sonuc)  # Çıktı: 16
```
### 6.2. `return` İfadesi ve Fonksiyonun Dönüş Değeri

Python'da bir fonksiyon, `return` ifadesi ile bir değer döndürebilir. Fonksiyonun görevi bittiğinde, `return` ifadesiyle belirtilen değer çağrıldığı yere geri gönderilir. Eğer bir fonksiyon `return` ifadesi kullanmazsa, Python otomatik olarak `None` değeri döndürür.

#### `return` İfadesinin Kullanımı:

```python
def kare(sayi):
    return sayi ** 2
```
**Kullanımı:**
```python
sonuc = kare(5)
print(sonuc)  # Çıktı: 25
```
Fonksiyon `kare(5)` ifadesiyle çağrıldığında, 5'in karesi hesaplanır ve bu değer `sonuc` değişkenine atanır.

### `return` İfadesi Olmadan:
Eğer `return` ifadesi kullanılmazsa, fonksiyon sonuç döndürmez ve varsayılan olarak `None` değeri döner.


# 7. Değişkenlerin Kapsamı (Scope)

- **Yerel Değişkenler (Local Variables):** Fonksiyon içinde tanımlanan ve sadece o fonksiyon içinde erişilebilen değişkenlerdir.
- **Global Değişkenler:** Fonksiyon dışında tanımlanan ve programın her yerinden erişilebilen değişkenlerdir.

```python
x = 10  # Global değişken

def fonksiyon():
    x = 5  # Yerel değişken
    print(x)  # Çıktı: 5

fonksiyon()
print(x)  # Çıktı: 10
```

### 7.1. global Anahtar Kelimesi

Fonksiyon içinde global bir değişkeni değiştirmek için kullanılır.

```python
x = 10

def degistir():
    global x
    x = 5

degistir()
print(x)  # Çıktı: 5
```

# 8. Lambda Fonksiyonları (Anonim Fonksiyonlar)

- Tek satırlık, isimsiz fonksiyonlardır.
- **lambda** anahtar kelimesi ile tanımlanır.

```python
kare = lambda x: x ** 2
print(kare(5))  # Çıktı: 25
```

# 9. Rekürsif Fonksiyonlar

- Kendini çağıran fonksiyonlardır.
- Özellikle matematiksel hesaplamalarda kullanılır (faktöriyel, Fibonacci serisi vb.).

```python
def faktoriyel(n):
    if n == 1:
        return 1
    else:
        return n * faktoriyel(n - 1)

print(faktoriyel(5))  # Çıktı: 120
```

# 10. Docstring (Fonksiyonları Belgelendirme)

- Fonksiyonların ne yaptığını açıklamak için kullanılır.
- Üç tırnak işareti arasında yazılır.

```python
def toplama(a, b):
    """Bu fonksiyon iki sayının toplamını döndürür."""
    return a + b

print(toplama.__doc__)  # Çıktı: Bu fonksiyon iki sayının toplamını döndürür.
```

# 11. Fonksiyonları Parametre Olarak Kullanmak

Fonksiyonlar da birer nesnedir ve başka fonksiyonlara parametre olarak geçirilebilirler.

```python
def uygulama(fonksiyon, deger):
    return fonksiyon(deger)

def kare(x):
    return x ** 2

print(uygulama(kare, 5))  # Çıktı: 25
```

# 12. Yerleşik Fonksiyonlar ve Kullanıcı Tanımlı Fonksiyonlar

- **Yerleşik Fonksiyonlar:** Python'un kendi içinde hazır olarak gelen fonksiyonlardır (print(), len(), type() vb.).
- **Kullanıcı Tanımlı Fonksiyonlar:** Kendi ihtiyaçlarımıza göre tanımladığımız fonksiyonlardır.

# 13. Örnek Uygulama: Basit Bir Hesap Makinesi

```python
def toplama(a, b):
    return a + b

def cikarma(a, b):
    return a - b

def carpma(a, b):
    return a * b

def bolme(a, b):
    if b == 0:
        return "Hata: Bölme işleminde payda sıfır olamaz."
    return a / b

print("İşlem Seçiniz:")
print("1. Toplama")
print("2. Çıkarma")
print("3. Çarpma")
print("4. Bölme")

secim = input("Seçiminiz (1/2/3/4): ")
sayi1 = float(input("Birinci sayıyı girin: "))
sayi2 = float(input("İkinci sayıyı girin: "))

if secim == '1':
    print("Sonuç:", toplama(sayi1, sayi2))
elif secim == '2':
    print("Sonuç:", cikarma(sayi1, sayi2))
elif secim == '3':
    print("Sonuç:", carpma(sayi1, sayi2))
elif secim == '4':
    print("Sonuç:", bolme(sayi1, sayi2))
else:
    print("Geçersiz seçim.")
```

# 14. Özet ve Sonuç

- Fonksiyonlar kodumuzu daha düzenli ve yönetilebilir hale getirir.
- Parametreler ve dönüş değerleri ile fonksiyonlar esnek ve güçlü yapılar sunar.
- *args ve **kwargs ile fonksiyonlarınızı daha genel hale getirebilirsiniz.
- Lambda fonksiyonları ile hızlı ve kısa fonksiyonlar tanımlayabilirsiniz.
- Fonksiyonları iyi anlamak, Python'da etkili programlama yapmanın temel adımlarından biridir.

# 15. Ek Kaynaklar

- **Python Resmi Belgeleri:** [https://docs.python.org/tr/3/tutorial/index.html](https://docs.python.org/tr/3/tutorial/index.html)
- **Online Python Dersleri ve Eğitimleri**

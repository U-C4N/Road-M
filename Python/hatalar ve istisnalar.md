# Python'da Hatalar ve İstisnalar: Baştan İleri Seviyeye Kadar Detaylı Bir Anlatım

Python programlamaya yeni başlayan biri olarak, hatalar ve istisnaların nasıl çalıştığını anlamak, kodunuzun güvenilirliğini ve dayanıklılığını artırmak için kritik öneme sahiptir. Bu rehberde, hatalar ve istisnaların temellerinden başlayarak ileri seviye konulara kadar detaylı bir şekilde ele alacağız.

## İçindekiler

1. [Hata ve İstisnaların Tanımı](#hata-ve-istisnaların-tanımı)
2. [Sözdizimi Hataları ve İstisnalar](#sözdizimi-hataları-ve-istisnalar)
3. [Python'daki Yaygın İstisnalar](#pythondaki-yaygın-istisnalar)
4. [İstisna Yakalama: `try` ve `except`](#istisna-yakalama-try-ve-except)
5. [Özel İstisnaların Yakalanması](#özel-istisnaların-yakalanması)
6. [Birden Fazla `except` Bloğu Kullanımı](#birden-fazla-except-bloğu-kullanımı)
7. [`else` ve `finally` Blokları](#else-ve-finally-blokları)
8. [İstisnaların Yükseltilmesi: `raise`](#istisnaların-yükseltilmesi-raise)
9. [Özel İstisnalar Oluşturma](#özel-istisnalar-oluşturma)
10. [İstisna Hiyerarşisi](#istisna-hiyerarşisi)
11. [İstisna Zincirleme](#istisna-zincirleme)
12. [En İyi Uygulamalar](#en-iyi-uygulamalar)
13. [Gelişmiş Konular](#gelişmiş-konular)
14. [Sonuç](#sonuç)

---

## Hata ve İstisnaların Tanımı

**Hata (Error)**: Programın çalışmasını engelleyen sorunlardır. Hatalar genellikle sözdizimi (syntax) hataları veya mantıksal hatalar olabilir.

**İstisna (Exception)**: Programın normal akışını bozan olaylardır. İstisnalar, programın beklenmeyen durumlarla karşılaştığında verdiği tepkilerdir.

## Sözdizimi Hataları ve İstisnalar

### Sözdizimi Hataları

Sözdizimi hataları, Python kodunun dilin kurallarına uymadığında ortaya çıkar. Örneğin:

```python
# Eksik parantez
print("Merhaba Dünya"
```
Bu kod çalıştırıldığında `SyntaxError` alırsınız.

### İstisnalar
Sözdizimi hataları düzeltildikten sonra, kod çalışırken ortaya çıkan hatalara istisna denir. Örneğin:

```python
# Tanımsız bir değişken kullanımı
print(x)
```

Bu kod `NameError` istisnası fırlatır çünkü `x` tanımlanmamıştır.


## Python'daki Yaygın İstisnalar

- **`NameError`**: Tanımsız bir değişken kullanıldığında.
- **`TypeError`**: Yanlış türde bir değer kullanıldığında.
- **`IndexError`**: Listede olmayan bir indekse erişildiğinde.
- **`KeyError`**: Sözlükte olmayan bir anahtara erişildiğinde.
- **`ValueError`**: Bir fonksiyona geçersiz bir değer verildiğinde.
- **`ZeroDivisionError`**: Bir sayıyı sıfıra bölmeye çalışıldığında.
- **`AttributeError`**: Bir nesnenin olmayan bir özelliğine erişildiğinde.

### Örnekler

```python
# ZeroDivisionError
print(10 / 0)
```

```python
# IndexError
liste = [1, 2, 3]
print(liste[5])
```

## İstisna Yakalama: `try` ve `except`

İstisnaları yakalamak ve yönetmek için `try` ve `except` bloklarını kullanırız.

### Temel Kullanım

```python
try:
    # Hata olabilecek kod buraya yazılır
    sayi = int(input("Bir sayı girin: "))
    sonuc = 10 / sayi
    print("Sonuç:", sonuc)
except ZeroDivisionError:
    # İstisna durumunda çalışacak kod
    print("Sıfıra bölme hatası!")
```

Bu kodda, kullanıcı sıfır girerse `ZeroDivisionError` yakalanır ve program çökmez.

## Özel İstisnaların Yakalanması

Birden fazla istisna türünü yakalamak için farklı `except` blokları kullanabilirsiniz.

```python
try:
    sayi = int(input("Bir sayı girin: "))
    sonuc = 10 / sayi
    print("Sonuç:", sonuc)
except ZeroDivisionError:
    print("Sıfıra bölme hatası!")
except ValueError:
    print("Geçersiz bir sayı girdiniz!")
```

## Birden Fazla `except` Bloğu Kullanımı

Bir `try` bloğunda birden fazla `except` bloğu kullanarak farklı istisnaları ayrı ayrı ele alabilirsiniz.

```python
try:
    # Kodunuz
except TypeError:
    # TypeError ele alındığında çalışacak kod
except ValueError:
    # ValueError ele alındığında çalışacak kod
```

## `else` ve `finally` Blokları

### `else` Bloğu

`try` bloğunda hata oluşmazsa `else` bloğu çalışır.

```python
try:
    sayi = int(input("Bir sayı girin: "))
except ValueError:
    print("Geçersiz giriş!")
else:
    print("Girdiğiniz sayı:", sayi)
```

### `finally` Bloğu

Hata oluşsa da oluşmasa da her zaman çalışır.

```python
try:
    dosya = open("dosya.txt", "r")
    # Dosya işlemleri
except FileNotFoundError:
    print("Dosya bulunamadı!")
finally:
    dosya.close()
```

## İstisnaların Yükseltilmesi: `raise`

Kendi istisnalarınızı fırlatmak için `raise` ifadesini kullanabilirsiniz.

```python
def pozitif_sayi(sayi):
    if sayi <= 0:
        raise ValueError("Sayı pozitif olmalıdır!")
    return sayi

try:
    pozitif_sayi(-5)
except ValueError as e:
    print(e)
```

## Özel İstisnalar Oluşturma

Kendi istisna sınıflarınızı oluşturabilirsiniz.

```python
class ÖzelleştirilmişHata(Exception):
    pass

def kontrol_et(sayi):
    if sayi > 100:
        raise ÖzelleştirilmişHata("Sayı 100'den büyük olamaz!")

try:
    kontrol_et(150)
except ÖzelleştirilmişHata as e:
    print(e)
```

## İstisna Hiyerarşisi

Python'daki tüm istisnalar bir hiyerarşi içerisindedir.

- `BaseException`
  - `Exception`
    - `ArithmeticError`
      - `ZeroDivisionError`
    - `LookupError`
      - `IndexError`
      - `KeyError`
    - vb.

Bu hiyerarşiyi bilmek, istisnaları daha etkin bir şekilde yakalamanıza yardımcı olur.

## İstisna Zincirleme

Bir istisnayı başka bir istisnadan kaynaklandığını belirtmek için kullanılır.

```python
try:
    # Kodunuz
except SomeException as e:
    raise AnotherException("Mesaj") from e
```

## En İyi Uygulamalar

- **Spesifik İstisnaları Yakalayın**: Genel `Exception` sınıfını yakalamak yerine spesifik istisnaları yakalayın.
- **Minimal Kod Kullanın**: `try` bloğunda sadece hata oluşturabilecek kodları bulundurun.
- **Kaynakları Temizleyin**: `finally` bloğunu veya `with` ifadesini kullanarak kaynakları temizleyin.
- **Bilgilendirici Hata Mesajları**: Kullanıcıya veya geliştiriciye yardımcı olacak mesajlar verin.

## Gelişmiş Konular

### Bağlam Yöneticileri ve `with` İfadesi

Kaynak yönetimini otomatikleştirmek için kullanılır.

```python
with open("dosya.txt", "r") as dosya:
    içerik = dosya.read()
```

### Doğrulamalar

`assert` ifadesi ile koşulların doğru olup olmadığını kontrol edebilirsiniz.

```python
assert x > 0, "x pozitif olmalıdır"
```

### Çoklu İş Parçacığında İstisna Yönetimi

Çoklu iş parçacığı kullanırken istisnaları düzgün bir şekilde yönetmek önemlidir. Her iş parçacığındaki istisnaları ayrı ayrı ele almalısınız.

## Sonuç

Hatalar ve istisnalar, Python programlamada kaçınılmazdır. Ancak bunları doğru bir şekilde yöneterek programlarınızın güvenilirliğini artırabilirsiniz. Bu rehberde temel kavramlardan başlayarak ileri seviye konulara kadar detaylı bir inceleme yaptık. Pratik yaparak ve gerçek dünya projelerinde bu bilgileri uygulayarak uzmanlaşabilirsiniz.


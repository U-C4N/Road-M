# Python Öğrenme Haritası (Sıfırdan Orta Seviyeye)

---

## 1. Programlamaya ve Python'a Giriş

### Programlamanın Temelleri
- **Algoritma ve Akış Diyagramları**
  - Algoritma nedir? Nasıl yazılır?
  - Akış diyagramı sembolleri ve kullanımı.
  - Örnek bir algoritmanın akış diyagramına dönüştürülmesi.
- **Programlama Dilleri ve Paradigmaları**
  - Farklı programlama dilleri ve kullanım alanları.
  - Yapısal, nesne yönelimli ve fonksiyonel programlama kavramları.
  - Python'un çok paradigmalı yapısı ve avantajları.

### Python'un Temelleri
- **Python Nedir?**
  - Python'un tarihçesi ve geliştiricisi Guido van Rossum.
  - Python 2 ve Python 3 arasındaki farklar.
  - Python'un popüler olma sebepleri ve kullanım alanları.
- **Geliştirme Ortamının Kurulumu**
  - Python'ın farklı işletim sistemlerine (Windows, macOS, Linux) kurulumu.
  - Anaconda ve Miniconda gibi dağıtımların kullanımı.
  - Sanal ortamların önemi ve `venv`, `virtualenv` kullanımı.
- **İlk Kodun Çalıştırılması**
  - Komut satırından Python çalıştırma (`python` ve `python3` komutları).
  - Basit bir "Hello, World!" programının farklı şekillerde yazılması.
  - Jupyter Notebook ve IPython kullanımı.

---

## 2. Temel Sözdizimi ve Veri Tipleri

### Değişkenler ve Veri Tipleri
- **Değişken Tanımlama Kuralları**
  - İsimlendirme konvansiyonları (snake_case, camelCase).
  - Anahtar kelimeler ve kaçınması gereken isimler.
- **Veri Tipleri**
  - **Sayısal Tipler**
    - **Tam Sayılar (`int`)**
    - **Ondalıklı Sayılar (`float`)**
    - **Karmaşık Sayılar (`complex`)**
  - **Metin Tipleri (`str`)**
    - String Tanımlama, Kaçış Karakterleri ve Raw Stringler.
  - **Mantıksal Tipler (`bool`)**
    - `True` ve `False` Değerleri
  - **Tip Dönüşümleri**
    - `int()`, `float()`, `str()`, `bool()` ve `type()`, `isinstance()` fonksiyonları.

### Operatörler
- **Aritmetik Operatörler**
  - Toplama (`+`), çıkarma (`-`), çarpma (`*`), bölme (`/`), mod alma (`%`), tam sayı bölmesi (`//`), üs alma (`**`).
- **Karşılaştırma Operatörleri**
  - Eşitlik (`==`), eşit değildir (`!=`), büyüklük ve küçüklük (`>`, `<`), küçük veya eşit (`<=`), büyük veya eşit (`>=`).
- **Mantıksal Operatörler**
  - `and`, `or`, `not`
- **Atama Operatörleri**
  - `=`, `+=`, `-=`, `*=`, `/=`, vb.
- **Bit Düzeyi Operatörleri**
  - `&`, `|`, `^`, `~`, `<<`, `>>`.

### Girdi ve Çıktı İşlemleri
- **`print()` Fonksiyonu**
  - Biçimlendirme: `format()`, f-string kullanımı.
- **`input()` Fonksiyonu**
  - Kullanıcıdan veri alma ve tip dönüşümleri.

---

## 3. Kontrol Akışı

### Koşullu İfadeler
- **`if`, `elif`, `else` Yapıları**
  - İç içe koşullar, `in`, `is`, `not in`, `is not`.

### Döngüler
- **`for` Döngüsü**
  - `range()`, `enumerate()`, `zip()` fonksiyonları.
- **`while` Döngüsü**
  - Koşula bağlı döngüler.
- **Döngü Kontrol İfadeleri**
  - `break`, `continue`, `pass`.

---

## 4. Veri Yapıları

### Listeler
- **Liste Oluşturma ve Erişim**
  - İndeksleme ve dilimleme.
- **Liste Metodları**
  - `append()`, `insert()`, `remove()`, `pop()`, `clear()`, `sort()`, `reverse()`.

### Demetler (Tuples)
- **Demetlerin Özellikleri**
  - Değişmezlik.
- **Demet Metodları**
  - `count()`, `index()`.

### Sözlükler (Dictionaries)
- **Anahtar-Değer İlişkisi**
  - Anahtar kullanarak değer erişimi.
- **Sözlük Metodları**
  - `keys()`, `values()`, `items()`, `get()`, `pop()`, `setdefault()`.

### Kümeler (Sets)
- **Küme Oluşturma**
  - `set()` ve `frozenset()`.
- **Küme Operasyonları**
  - Birleşim, kesişim, fark, simetrik fark.
- **Küme Metodları**
  - `add()`, `remove()`, `discard()`, `update()`.

---

## 5. String İşlemleri

### String Oluşturma ve Temel İşlemler
- **İndeksleme ve Dilimleme**
- **String Birleştirme ve Tekrarlama**
  - `+`, `*` operatörleri.

### String Metodları
- **Büyük/Küçük Harf Dönüşümleri**
  - `upper()`, `lower()`, `title()`, `capitalize()`, `swapcase()`.
- **Arama ve Değiştirme**
  - `find()`, `index()`, `replace()`.
- **Bölme ve Birleştirme**
  - `split()`, `join()`, `splitlines()`.
- **Kontrol Metodları**
  - `startswith()`, `endswith()`, `isalpha()`, `isdigit()`, `isalnum()`.
- **Boşluk Silme**
  - `strip()`, `lstrip()`, `rstrip()`.

---

## 6. Fonksiyonlar

### Fonksiyon Tanımlama ve Çağırma
- `def` anahtar kelimesi.
- Parametreler ve geri dönüş değerleri.

### Parametre Türleri
- **Varsayılan Parametreler**
- **Esnek Parametreler**: `*args`, `**kwargs`.

### Lambda Fonksiyonları
- **Anonim Fonksiyonlar**
  - `lambda` ifadesi.

### Rekürsif Fonksiyonlar
- **Kendi Kendini Çağıran Fonksiyonlar**

### Yüksek Seviyeli Fonksiyonlar
- **`map()`, `filter()`, `reduce()`**

---

## 7. Modüller ve Paketler

### Modüllerin İçe Aktarılması
- **`import` ve `from ... import ...`**
- **Standart Kütüphaneler**
  - `math`, `random`, `datetime`, `os`, `sys`.

### Kendi Modüllerini Oluşturma
- Modüllerin modüler hale getirilmesi.

### Paketler
- Paket Yapısı ve `__init__.py`.

---

## 8. Dosya İşlemleri

### Dosya Açma ve Kapama
- **`open()` Fonksiyonu**
  - Dosya modları: `'r'`, `'w'`, `'a'`, `'b'`.

### Dosya ve Dizin İşlemleri
- **`os` ve `shutil` Modülleri**

### JSON ve CSV İşlemleri
- **`json` Modülü**
  - `json.load()`, `json.dump()`.
- **`csv` Modülü**
  - `csv.reader()`, `csv.writer()`.

---

## 9. Hata ve İstisna Yönetimi

### İstisnaların Yakalanması
- **`try`, `except`, `else`, `finally`**

### Özel İstisnalar Oluşturma
- **`raise` İfadesi**

### Hata Ayıklama Teknikleri
- **`pdb` Modülü**
- **`logging` Modülü**

---

## 10. Nesne Yönelimli Programlama (OOP)

### Sınıflar ve Nesneler
- **Sınıf Yapısı ve Tanımlama**
- **Nesne Oluşturma**

### Nitelikler ve Metodlar
- **`self` Parametresi**
- **Sınıf Nitelikleri**

### Özel Metodlar (Magic Methods)
- **`__init__()`, `__str__()`, `__repr__()`**

### Kalıtım ve Polimorfizm
- **`super()` Fonksiyonu**
- **Metotların Yeniden Tanımlanması**

### Kapsülleme ve Veri Gizleme
- **Erişim Belirleyicileri**
  - `_protected`, `__private`.

### Getter ve Setter Metodları
- **`@property` Dekoratörü**

---

## 11. İleri Seviye Konular

### İteratörler ve Generatorlar
- **`__iter__()`, `__next__()`**
- **`yield` İfadesi**

### Dekoratörler
- **Fonksiyon ve Sınıf Dekoratörleri**

### Context Manager'lar
- **`with` İfadesi**
  - `__enter__()`, `__exit__()`.

---

## 12. Popüler Kütüphanelerle Çalışma

### Veri Analizi ve Görselleştirme
- **`numpy`, `pandas`**
- **`matplotlib`, `seaborn`**

### Web Geliştirme
- **`Flask`, `Django`**

### Web Scraping
- **`requests`, `BeautifulSoup`, `Selenium`**

---

## 13. Versiyon Kontrolü ve İş Birliği

### Git ve GitHub Kullanımı
- **Temel Git Komutları**
- **Dallanma ve Birleştirme**
- **GitHub ile Proje Paylaşımı**

---

## 14. Proje Geliştirme ve Uygulamalar

### Küçük Ölçekli Projeler
- **Hesap Makinesi Uygulaması**
- **Not Defteri (To-Do List)**
- **Basit Oyunlar**
  - "Adam Asmaca", "Taş Kağıt Makas".

### Orta Ölçekli Projeler
- **Blog veya Portföy Web Sitesi**
- **Veri Analizi Projeleri**

---

## 15. Kod Kalitesi ve En İyi Uygulamalar

### PEP 8 ve Kod Stili
- **Kod Standartlarına Uyum**
- **`flake8`, `pylint` ile Kod Analizi**

### Dokümantasyon
- **Docstrings ve Yorumlar**
- **`Sphinx` ile Otomatik Dokümantasyon**

### Test Etme ve Hata Ayıklama
- **Birim Testleri**
  - `unittest`, `pytest`.

---

## 16. İleriye Dönük Adımlar

### Asenkron Programlama
- **`asyncio` Kütüphanesi**

### Tip Kontrolü
- **`typing` Modülü**

### Dağıtık Sistemler ve Mikroservisler
- **Docker ve Kubernetes**

### Sürekli Öğrenme ve Kaynaklar
- **Topluluklar ve Etkinlikler**
  - Python Türkiye, Stack Overflow, GitHub.

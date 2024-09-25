
# Python Map, Filter ve Reduce Fonksiyonları Açıklaması

Bu repository, Python'daki `map()`, `filter()` ve `reduce()` fonksiyonlarını yeni başlayanlar için anlaşılır bir şekilde açıklamaktadır.

## Giriş

Python'da **`map()`**, **`filter()`** ve **`reduce()`** fonksiyonları, listeler ve diğer iterable (yinelenebilir) veri yapıları üzerinde işlem yapmamızı sağlayan güçlü araçlardır. Bu fonksiyonlar, fonksiyonel programlamadan esinlenmiştir ve veri koleksiyonlarını daha verimli bir şekilde işlemek için kullanılır.

Bu README'de, hiç bilmeyen birine göre bu fonksiyonları adım adım açıklayacağız.

---

## Temel Kavramlar

- **Fonksiyon**: Belirli bir görevi yerine getiren kod parçalarıdır. Örneğin, bir sayıyı ikiyle çarpan bir fonksiyon yazabiliriz.
- **Liste**: Birden fazla öğeyi bir arada tutan veri yapısıdır. Örneğin, `[1, 2, 3, 4, 5]` bir listedir.
- **İterasyon**: Bir koleksiyonun öğeleri üzerinde sırayla işlem yapma sürecidir.

---

## map() Fonksiyonu

### Tanım

**`map()`**, bir fonksiyonu bir listenin her öğesine uygular ve sonuçları yeni bir listede toplar.

### Nasıl Çalışır?

1. **Bir Fonksiyon Tanımlayın**: Örneğin, bir sayıyı ikiyle çarpan bir fonksiyon.
2. **Bir Liste Oluşturun**: İşlem yapmak istediğiniz sayıları içeren bir liste.
3. **`map()` Fonksiyonunu Kullanın**: Fonksiyon ve listeyi `map()`'e verin.
4. **Sonucu Alın**: Yeni oluşan listeyi alın.

### Örnek

#### Adım 1: Fonksiyon Tanımlama

```python
def ikiyle_carp(x):
    return x * 2
```

Bu fonksiyon, verilen sayıyı ikiyle çarpar.

#### Adım 2: Liste Oluşturma

```python
sayilar = [1, 2, 3, 4, 5]
```

#### Adım 3: `map()` Kullanma

```python
sonuc = map(ikiyle_carp, sayilar)
```

#### Adım 4: Sonucu Görüntüleme

```python
print(list(sonuc))  # Çıktı: [2, 4, 6, 8, 10]
```

---

## filter() Fonksiyonu

### Tanım

**`filter()`**, bir koşula göre bir listedeki öğeleri filtreler. Koşulu sağlayan öğeler yeni bir liste oluşturur.

### Nasıl Çalışır?

1. **Bir Koşul Fonksiyonu Tanımlayın**: Örneğin, bir sayının çift olup olmadığını kontrol eden fonksiyon.
2. **Bir Liste Oluşturun**: İşlem yapmak istediğiniz sayıları içeren bir liste.
3. **`filter()` Fonksiyonunu Kullanın**: Fonksiyon ve listeyi `filter()`'a verin.
4. **Sonucu Alın**: Koşulu sağlayan öğelerden oluşan yeni listeyi alın.

### Örnek

#### Adım 1: Fonksiyon Tanımlama

```python
def cift_mi(x):
    return x % 2 == 0
```

Bu fonksiyon, sayı çiftse `True`, değilse `False` döndürür.

#### Adım 2: Liste Oluşturma

```python
sayilar = [1, 2, 3, 4, 5, 6]
```

#### Adım 3: `filter()` Kullanma

```python
sonuc = filter(cift_mi, sayilar)
```

#### Adım 4: Sonucu Görüntüleme

```python
print(list(sonuc))  # Çıktı: [2, 4, 6]
```

---

## reduce() Fonksiyonu

### Tanım

**`reduce()`**, bir listenin öğelerini birleştirerek tek bir değer üretir. Bu fonksiyonu kullanmak için `functools` modülünü import etmemiz gerekir.

### Nasıl Çalışır?

1. **İki Argüman Alan Bir Fonksiyon Tanımlayın**: Örneğin, iki sayıyı toplayan bir fonksiyon.
2. **Bir Liste Oluşturun**: İşlem yapmak istediğiniz sayıları içeren bir liste.
3. **`reduce()` Fonksiyonunu Kullanın**: Fonksiyon ve listeyi `reduce()`'a verin.
4. **Sonucu Alın**: Tek bir değer elde edin.

### Örnek

#### Adım 1: Fonksiyon Tanımlama

```python
def topla(x, y):
    return x + y
```

#### Adım 2: Liste Oluşturma

```python
sayilar = [1, 2, 3, 4, 5]
```

#### Adım 3: `reduce()` Kullanma

```python
from functools import reduce
sonuc = reduce(topla, sayilar)
```

#### Adım 4: Sonucu Görüntüleme

```python
print(sonuc)  # Çıktı: 15
```

---

## Özet ve İpuçları

- **`map()`**: Dönüştürme işlemleri için kullanılır. Her öğeye aynı işlemi uygular.
- **`filter()`**: Seçme işlemleri için kullanılır. Belirli bir koşulu sağlayan öğeleri seçer.
- **`reduce()`**: İndirgeme işlemleri için kullanılır. Bir listeyi tek bir değere dönüştürür.

Bu fonksiyonları anlamak, başlangıçta zor gelebilir, ancak örneklerle çalışarak ve pratik yaparak kavramları pekiştirebilirsiniz. 
Eğer takıldığınız noktalar varsa, sorularınızı sormaktan çekinmeyin!


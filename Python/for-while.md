# Python `for` ve `while` Döngüleri

Python'da **döngüler (loops)**, belirli bir kod bloğunu birden fazla kez çalıştırmak için kullanılır. İki ana döngü tipi vardır: **`for` döngüsü** ve **`while` döngüsü**. Şimdi bu döngüleri detaylı bir şekilde inceleyelim, kıyaslayalım ve hangi projelerde kullanıldıklarına bakalım.

---

## **`for` Döngüsü**

### **Tanım:**

`for` döngüsü, belirli bir dizinin (liste, demet, sözlük, string vb.) elemanları üzerinde iterasyon yapmak için kullanılır. Döngü, her bir eleman için kod bloğunu çalıştırır.

### **Kullanım Şekli:**

```python
for eleman in koleksiyon:
    # İşlem yapılacak kod bloğu
```
### **Örnekler:**

**1. Liste Elemanlarını Yazdırma**

```python
meyveler = ["elma", "armut", "muz"]
for meyve in meyveler:
    print(meyve)
```
**Çıktı**

```python
elma
armut
muz
```

**2. range() Fonksiyonu ile**
```python
for i in range(5):
    print(i)
```
**Çıktı**

```python
0
1
2
3
4
```

## **`while` Döngüsü**

### **Tanım:**

`while` döngüsü, belirli bir koşul **`True`** olduğu sürece kod bloğunu tekrarlar. Koşul **`False`** olduğunda döngü sona erer.

### **Örnekler:**

**1. Sayaç ile Döngü**

```python
sayi = 0
while sayi < 5:
    print(sayi)
    sayi += 1
```
**Çıktı**
```python
0
1
2
3
4
```


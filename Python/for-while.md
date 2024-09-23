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

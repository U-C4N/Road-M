
# Döngülerde `break`, `continue` ve `pass` Kullanımı

Döngüler, programlamada belirli bir işlemi birden fazla kez tekrarlamak için kullanılır. Python'da en yaygın kullanılan döngüler `for` ve `while` döngüleridir. Bu döngüler içinde akışı kontrol etmek için `break`, `continue` ve `pass` gibi özel ifadeler kullanılır. Bu rehberde, bu ifadelerin ne işe yaradığını ve nasıl kullanıldığını basit örneklerle anlatacağız.

## İçindekiler

1. [For ve While Döngüleri](#for-ve-while-döngüleri)
2. [`break` İfadesi](#break-ifadsi)
   - [For Döngüsünde `break`](#for-döngüsünde-break)
   - [While Döngüsünde `break`](#while-döngüsünde-break)
3. [`continue` İfadesi](#continue-ifadsi)
   - [For Döngüsünde `continue`](#for-döngüsünde-continue)
   - [While Döngüsünde `continue`](#while-döngüsünde-continue)
4. [`pass` İfadesi](#pass-ifadsi)
   - [For Döngüsünde `pass`](#for-döngüsünde-pass)
   - [While Döngüsünde `pass`](#while-döngüsünde-pass)
5. [Sonuç](#sonuç)

---

## For ve While Döngüleri

- **For Döngüsü**: Belirli bir koleksiyonun (liste, dizi, string vb.) elemanları üzerinde gezinmek için kullanılır.

  ```python
  for eleman in koleksiyon:
      # Yapılacak işlemler
  ```

- **While Döngüsü**: Belirli bir koşul doğru olduğu sürece çalışır.

  ```python
  while koşul:
      # Yapılacak işlemler
  ```

---

## `break` İfadesi

`break` ifadesi, bir döngüyü anında sonlandırmak için kullanılır. Döngü içindeki belirli bir koşul gerçekleştiğinde döngüden çıkmak istiyorsanız `break` ifadesini kullanabilirsiniz.

### For Döngüsünde `break`

**Örnek**: 1'den 10'a kadar sayıları yazdırın, ancak sayı 5 olduğunda döngüyü sonlandırın.

```python
for i in range(1, 11):
    if i == 5:
        break
    print(i)
```

**Çıktı:**

```
1
2
3
4
```

**Açıklama**: `i` değeri 5'e eşit olduğunda `break` ifadesi çalışır ve döngü sonlanır.

### While Döngüsünde `break`

**Örnek**: Sayacı 1'den başlayarak artırın, ancak sayı 5 olduğunda döngüyü sonlandırın.

```python
i = 1
while i <= 10:
    if i == 5:
        break
    print(i)
    i += 1
```

**Çıktı:**

```
1
2
3
4
```

**Açıklama**: `i` değeri 5'e ulaştığında `break` ifadesi çalışır ve döngü sonlanır.

---

## `continue` İfadesi

`continue` ifadesi, döngünün o anki yinelemesini atlayıp bir sonraki yinelemeye geçmek için kullanılır. Döngüden çıkmak yerine, belirli bir koşul altında işlemleri atlamak istediğinizde kullanılır.

### For Döngüsünde `continue`

**Örnek**: 1'den 5'e kadar sayıları yazdırın, ancak sayı 3 olduğunda yazdırmayı atlayın.

```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```

**Çıktı:**

```
1
2
4
5
```

**Açıklama**: `i` değeri 3 olduğunda `continue` ifadesi çalışır ve `print(i)` satırı atlanır.

### While Döngüsünde `continue`

**Örnek**: 1'den 5'e kadar sayıları yazdırın, ancak sayı 3 olduğunda yazdırmayı atlayın.

```python
i = 1
while i <= 5:
    if i == 3:
        i += 1
        continue
    print(i)
    i += 1
```

**Çıktı:**

```
1
2
4
5
```

**Açıklama**: `i` değeri 3 olduğunda `continue` ifadesi çalışır, `print(i)` atlanır ve döngü bir sonraki yinelemeye geçer.

---

## `pass` İfadesi

`pass` ifadesi, hiçbir işlem yapmadan döngünün çalışmasına devam etmesini sağlar. Genellikle bir kod bloğunun boş geçici olarak bırakılması gerektiğinde kullanılır.

### For Döngüsünde `pass`

**Örnek**: Bir liste içinde negatif sayıları bulun, negatif sayı yoksa hiçbir işlem yapmayın.

```python
sayılar = [1, 2, -3, 4, -5]

for sayı in sayılar:
    if sayı < 0:
        pass  # Şimdilik işlem yapmıyoruz
    else:
        print(sayı)
```

**Çıktı:**

```
1
2
4
```

**Açıklama**: Negatif sayılar için `pass` ifadesi çalışır ve döngüde hiçbir işlem yapmadan devam eder.

### While Döngüsünde `pass`

**Örnek**: Sayaç 5'e eşit olana kadar artırın, ancak 3 olduğunda hiçbir işlem yapmayın.

```python
i = 1
while i <= 5:
    if i == 3:
        pass  # İşlem yok
    else:
        print(i)
    i += 1
```

**Çıktı:**

```
1
2
4
5
```

**Açıklama**: `i` değeri 3 olduğunda `pass` ifadesi çalışır ve `print(i)` atlanır.

---

## Sonuç

- **`break`**: Döngüyü anında sonlandırır.
- **`continue`**: Döngünün o anki yinelemesini atlar, bir sonraki yinelemeye geçer.
- **`pass`**: Hiçbir işlem yapmaz, döngünün çalışmasına aynen devam eder.

Bu ifadeler, döngülerde akışı kontrol etmek ve kodunuzu daha esnek hale getirmek için kullanışlıdır. Özellikle karmaşık koşullar ve işlemler içeren döngülerde, bu ifadeleri kullanarak kodunuzu daha okunabilir ve yönetilebilir hale getirebilirsiniz.

---

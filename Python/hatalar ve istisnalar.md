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
print("Merhaba Dünya")
```
Bu kod çalıştırıldığında `SyntaxError` alırsınız.

### İstisnalar
Sözdizimi hataları düzeltildikten sonra, kod çalışırken ortaya çıkan hatalara istisna denir. Örneğin:

```python
# Tanımsız bir değişken kullanımı
print(x)
```

Bu kod `NameError` istisnası fırlatır çünkü `x` tanımlanmamıştır.


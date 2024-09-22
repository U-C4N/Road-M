**Çözüm:**

Verilen problemde, gerçel sayı **α** için her pozitif tam sayı **n** için aşağıdaki şart sağlanmaktadır:

S(n) = ⌊α⌋ + ⌊2α⌋ + ⌊3α⌋ + ... + ⌊nα⌋

Ve bu toplam **n** sayısının bir katı olmalıdır, yani:

S(n) ≡ 0 (mod n)

Burada ⌊x⌋, x'den küçük veya ona eşit en büyük tam sayıyı ifade etmektedir.

**Amacımız:** Bu şartı sağlayan tüm **α** gerçel sayılarını bulmaktır.

---

### 1. α bir tam sayı ise

Eğer **α** bir tam sayıysa, yani **α ∈ Z**, her **k** pozitif tam sayısı için:

⌊kα⌋ = kα

Çünkü **α** tam sayı olduğundan, çarpım da tam sayı olur ve tam kısmı kendisine eşittir.

Toplam:

S(n) = Σ(k=1, n) kα = α * Σ(k=1, n) k = α * (n(n+1)) / 2

**S(n)**'nin **n**'ye bölümünden kalanı inceleyelim:

S(n) mod n = (α * (n(n+1)) / 2) mod n = α * ((n+1) / 2) * n mod n

Burada α * ((n+1) / 2) bir tam sayıysa, **S(n)**, **n**'nin tam katı olacaktır.

**Durumları inceleyelim:**

- **a)** **α** çift tam sayı ise, yani **α = 2k**, k ∈ Z:

  S(n) = 2k * (n(n+1)) / 2 = k * n * (n+1)

  Burada **S(n)**, k * n * (n+1) şeklindedir ve **n**'nin tam katıdır.

- **b)** **α** tek tam sayı ise, yani **α = 2k+1**, k ∈ Z:

  S(n) = (2k+1) * (n(n+1)) / 2

  **n** çift bir sayı olduğunda, (n+1)/2 kesirli bir sayı

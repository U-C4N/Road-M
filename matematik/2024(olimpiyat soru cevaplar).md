1. Soru çözümü :

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

  **n** çift bir sayı olduğunda, (n+1)/2 kesirli bir sayı olur ve **S(n)** tam sayı olmayabilir.

  Örneğin, **n = 2** için:

  S(2) = (2k+1) * (2 * 3) / 2 = (2k+1) * 3 = 3(2k+1)

  **S(2)**, **2**'nin tam katı mıdır?

  S(2) mod 2 = 3(2k+1) mod 2 = (2k+1) mod 2

  Çünkü **2k+1** tek sayıdır, (2k+1) mod 2 = 1 olur. Yani **S(2)**, **2**'nin katı değildir.

  Dolayısıyla, **α** tek tam sayı olduğunda, şart her **n** için sağlanmaz.

**Sonuç:** **α** tam sayı ise, şartın sağlanması için **α**'nın **çift tam sayı** olması gerekir.

---

### 2. α tam sayı değilse

Eğer **α** tam sayı değilse, yani **α ∉ Z**, o zaman **α**'yı tam kısmı ve kesirli kısmı olarak yazabiliriz:

α = m + θ, burada m ∈ Z ve 0 < θ < 1

Her **k** pozitif tam sayısı için:

⌊kα⌋ = ⌊k(m + θ)⌋ = km + ⌊kθ⌋

Toplamı yazalım:

S(n) = Σ(k=1, n) (km + ⌊kθ⌋) = m * Σ(k=1, n) k + Σ(k=1, n) ⌊kθ⌋

İlk terim:

m * Σ(k=1, n) k = m * (n(n+1)) / 2

İkinci terim olan Σ(k=1, n) ⌊kθ⌋ ifadesi ise genellikle **n**'nin katı değildir.

**Karşı Örnek:**

- 0 < θ < 1 ve **nθ** tam sayı değilse, ⌊kθ⌋ değerleri düzensiz artar.
- Örneğin, **n = 2**, **θ = 0.6** için:

  ⌊1 * 0.6⌋ = 0 ve ⌊2 * 0.6⌋ = ⌊1.2⌋ = 1

  Toplam:

  S(2) = m * (2 * 3) / 2 + (0 + 1) = 3m + 1

  **S(2)**'nin **2**'ye bölümünden kalan:

  S(2) mod 2 = (3m + 1) mod 2

  **3m**'in **2**'ye bölümünden kalan **m**'in tek veya çift olmasına bağlıdır, ancak **1** eklediğimiz için sonuç genellikle **0** olmaz.

Dolayısıyla, **α** tam sayı değilse, **S(n)** genellikle **n**'nin tam katı olmaz ve verilen şart sağlanmaz.

---

### Sonuç:

Verilen şartı sağlayan **α** gerçel sayıları yalnızca **çift tam sayılardır**.

**Cevap:**

**α**, **çift tam sayı** ise, verilen şart sağlanır. Bu nedenle, şartı sağlayan tüm **α** gerçel sayıları **çift tam sayılardır**.

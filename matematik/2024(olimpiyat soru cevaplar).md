**Çözüm:**

Verilen problemde, gerçel sayı **α** için her pozitif tam sayı **n** için aşağıdaki şart sağlanmaktadır:

\[
S(n) = \left\lfloor \alpha \right\rfloor + \left\lfloor 2\alpha \right\rfloor + \left\lfloor 3\alpha \right\rfloor + \dotsb + \left\lfloor n\alpha \right\rfloor
\]

Ve bu toplam **n** sayısının bir katı olmalıdır, yani:

\[
S(n) \equiv 0 \pmod n
\]

Burada \(\left\lfloor x \right\rfloor\), \(x\)'den küçük veya ona eşit en büyük tam sayıyı ifade etmektedir.

**Amacımız:** Bu şartı sağlayan tüm **α** gerçel sayılarını bulmaktır.

---

**1. α bir tam sayı ise**

Eğer **α** bir tam sayıysa, yani **α ∈ \mathbb{Z}**, her **k** pozitif tam sayısı için:

\[
\left\lfloor k\alpha \right\rfloor = k\alpha
\]

Çünkü **α** tam sayı olduğundan, çarpım da tam sayı olur ve tam kısmı kendisine eşittir.

Toplam:

\[
S(n) = \sum_{k=1}^{n} k\alpha = \alpha \sum_{k=1}^{n} k = \alpha \cdot \frac{n(n+1)}{2}
\]

**S(n)**'nin **n**'ye bölümünden kalanı inceleyelim:

\[
S(n) \mod n = \left( \alpha \cdot \frac{n(n+1)}{2} \right) \mod n = \left( \alpha \cdot \frac{n+1}{2} \cdot n \right) \mod n = \left( \alpha \cdot \frac{n+1}{2} \cdot n \mod n \right)
\]

Burada \(\alpha \cdot \frac{n+1}{2}\) bir tam sayıysa, **S(n)**, **n**'nin tam katı olacaktır.

**Durumları inceleyelim:**

- **a)** **α** çift tam sayı ise, yani **α = 2k**, \(k \in \mathbb{Z}\):

  \[
  S(n) = 2k \cdot \frac{n(n+1)}{2} = k n (n+1)
  \]

  Burada **S(n)**, **k n (n+1)** şeklindedir ve **n**'nin tam katıdır.

- **b)** **α** tek tam sayı ise, yani **α = 2k+1**, \(k \in \mathbb{Z}\):

  \[
  S(n) = (2k+1) \cdot \frac{n(n+1)}{2}
  \]

  **n** çift bir sayı olduğunda, \(\frac{n+1}{2}\) kesirli bir sayı olur ve **S(n)** tam sayı olmayabilir.

  Örneğin, **n = 2** için:

  \[
  S(2) = (2k+1) \cdot \frac{2 \cdot 3}{2} = (2k+1) \cdot 3 = 3(2k+1)
  \]

  **S(2)**, **2**'nin tam katı mıdır?

  \[
  S(2) \mod 2 = 3(2k+1) \mod 2 = (2k+1) \mod 2
  \]

  Çünkü **2k+1** tek sayıdır, **(2k+1) \mod 2 = 1** olur. Yani **S(2)**, **2**'nin katı değildir.

  Dolayısıyla, **α** tek tam sayı olduğunda, şart her **n** için sağlanmaz.

**Sonuç:** **α** tam sayı ise, şartın sağlanması için **α**'nın **çift tam sayı** olması gerekir.

---

**2. α tam sayı değilse**

Eğer **α** tam sayı değilse, yani **α  \mathbb{Z}**, o zaman **α**'yı tam kısmı ve kesirli kısmı olarak yazabiliriz:

\[
\alpha = m + \theta \quad \text{burada} \quad m \in \mathbb{Z}, \quad 0 < \theta < 1
\]

Her **k** pozitif tam sayısı için:

\[
\left\lfloor k\alpha \right\rfloor = \left\lfloor k(m + \theta) \right\rfloor = km + \left\lfloor k\theta \right\rfloor
\]

Toplamı yazalım:

\[
S(n) = \sum_{k=1}^{n} \left( km + \left\lfloor k\theta \right\rfloor \right) = m \sum_{k=1}^{n} k + \sum_{k=1}^{n} \left\lfloor k\theta \right\rfloor
\]

İlk terim:

\[
m \sum_{k=1}^{n} k = m \cdot \frac{n(n+1)}{2}
\]

İkinci terim olan \(\sum_{k=1}^{n} \left\lfloor k\theta \right\rfloor\) ifadesi ise genellikle **n**'nin katı değildir.

**Karşı Örnek:**

- **0 < \theta < 1** ve **n\theta** tam sayı değilse, \(\left\lfloor k\theta \right\rfloor\) değerleri düzensiz artar.
- Örneğin, **n = 2**, **\theta = 0.6** için:

  \[
  \left\lfloor 1 \cdot 0.6 \right\rfloor = 0 \quad \text{ve} \quad \left\lfloor 2 \cdot 0.6 \right\rfloor = \left\lfloor 1.2 \right\rfloor = 1
  \]

  Toplam:

  \[
  S(2) = m \cdot \frac{2 \cdot 3}{2} + (0 + 1) = 3m + 1
  \]

  **S(2)**'nin **2**'ye bölümünden kalan:

  \[
  S(2) \mod 2 = (3m + 1) \mod 2
  \]

  **3m**'in **2**'ye bölümünden kalan **m**'in tek veya çift olmasına bağlıdır, ancak **1** eklediğimiz için sonuç genellikle **0** olmaz.

Dolayısıyla, **α** tam sayı değilse, **S(n)** genellikle **n**'nin tam katı olmaz ve verilen şart sağlanmaz.

---

**Sonuç:**

Verilen şartı sağlayan **α** gerçel sayıları yalnızca **çift tam sayılardır**.

**Cevap:**

**α**, **çift tam sayı** ise, verilen şart sağlanır. Bu nedenle, şartı sağlayan tüm **α** gerçel sayıları **çift tam sayılardır**.


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

### 1. α bir tam sayı ise

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

Burada \(\alpha \cdot \frac{

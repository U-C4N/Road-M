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


2. Soru çözümü ;

**Çözüm:**

Verilen koşulu sağlayan tek pozitif tam sayı ikilisi (a, b) = (1, 1)'dir.

**Açıklama:**

Öncelikle (a, b) = (1, 1) ikilisini inceleyelim:

Her **n** için:

ebob(1n + 1, 1n + 1) = ebob(2, 2) = 2

Görüldüğü gibi ebob değeri her zaman 2 olup sabittir. Dolayısıyla (1, 1) ikilisi verilen koşulu sağlar.

**Diğer pozitif tam sayı ikilileri için genelleme yapalım:**

**Anahtar Sayı Tanımı:**  
M = ab + 1 alın.

**Aralarında Asallık:**  
ebob(a, M) = 1  
ebob(b, M) = 1

Çünkü M = ab + 1 ifadesi, a ve b ile ortak bölen içermez.

**Euler Teoremi Uygulaması:**  
Euler'in Totient fonksiyonu φ(M) olsun.  
n değerini φ(M)'nin büyük bir katı olacak şekilde seçelim (n ≥ N).

Bu durumda:  
a^n ≡ 1 (mod M) ve b^n ≡ 1 (mod M)

**Modüler Denklem İncelemesi:**

a^n + b ≡ 1 + b (mod M)  
b^n + a ≡ 1 + a (mod M)

Bu ifadelerin ebob'ının M'yi bölmesi gerekir. Yani:  
ebob(1 + b, 1 + a) ≡ 0 (mod M)

Buradan:  
a + 1 ≡ 0 (mod M) ve b + 1 ≡ 0 (mod M)

Yani:  
a ≡ -1 (mod M) ve b ≡ -1 (mod M)

**Toplamın İncelenmesi:**

a + b ≡ -1 + (-1) = -2 (mod M)

Bu ifadeden -2 ≡ 0 (mod M) elde edilir. Yani M sayısı 2'yi bölmelidir.

**M'nin Değerinin Belirlenmesi:**

M = ab + 1 ve M pozitif bir tam sayı olduğuna göre, M = 2 olmalıdır.

Bu durumda:  
ab + 1 = 2 ⟹ ab = 1

a ve b pozitif tam sayılar olduğundan, sadece a = b = 1 mümkündür.

**Sonuç:**

Verilen koşulu sağlayan tek pozitif tam sayı ikilisi (a, b) = (1, 1)'dir.

**Cevap:**  
(a, b) = (1, 1)



3. Soru Çözümü ;


**Çözüm:**

Verilen problemde, pozitif tam sayılardan oluşan sonsuz bir (a_n) dizisi ve N pozitif tam sayısı verilmiştir.  
n > N için, a_n terimi, a_(n-1) teriminin a_1, a_2, …, a_(n-1) arasında kaç kere geçtiğine eşittir.

**Amacımız:**  
(a_1, a_3, a_5, …) veya (a_2, a_4, a_6, …) dizilerinden en az birinin bir yerden sonra periyodik olduğunu ispatlamaktır.

### İspata Başlayalım:

**Başlangıç Değerlerinin Sınırlandırılması:**

Öncelikle, ilk N terim a_1, a_2, …, a_N verilmiştir. Bu terimlerin maksimum değerini M = max{a_1, a_2, …, a_N} olarak tanımlayalım.

**Dizinin Gelişiminin Analizi:**

n > N için, her bir a_n terimi a_(n-1) teriminin a_1'den a_(n-1)'e kadar kaç kez tekrar ettiğine eşittir. Yani, a_n terimi, a_(n-1) teriminin önceki terimler arasında kaç defa göründüğünün sayısıdır.

**Terimlerin Değerlerinin Yükselmesi:**

Bir terimin değeri, o terimin önceki tekrarıyla ilgilidir. Eğer bir terim sık sık tekrar ederse, sayısı artar. Ancak, her a_n terimi en fazla n-1 olabilir çünkü a_(n-1), a_1'den a_(n-1)'e kadar en fazla n-1 kere görünebilir.

**Sınırlı Durumların Tespiti ve Durum Makinesi Oluşturma:**

Dizinin gelecekteki davranışını incelemek için, dizinin durumlarını takip edebileceğimiz bir yöntem geliştirelim. Bunun için, her terimin ve onun tekrar sayısının belirlediği bir durum tanımlayalım.  
n > N için, durumu S_n = (a_(n-1), a_n) olarak tanımlayalım. Burada:  
- a_(n-1) terimi, bir önceki terimdir.  
- a_n terimi ise, a_(n-1) teriminin önceki terimler arasında kaç kez göründüğüdür.

**Durum Sayısının Sonluluğu:**

Şimdi, bu durumların sayısının sonlu olduğunu göstereceğiz. Öncelikle, a_(n-1) terimi pozitif bir tam sayıdır. a_n terimi ise, a_(n-1) teriminin tekrar sayısıdır. Tekrar sayısı, n arttıkça artabilir, ancak her adımda birer birer artar. Bu yüzden, durumlar (a_(n-1), a_n) çiftleri olarak düşünülürse, bu çiftlerin sayısı, terimlerin alabileceği değerlerden dolayı sınırlıdır.

**Pigeonhole Prensibi'nin Uygulanması:**

Durumların sonlu olması ve dizinin sonsuz olması nedeniyle, Pigeonhole Prensibi'ne göre, aynı durumlar sonsuz defa tekrar etmek zorundadır. Yani, dizide herhangi bir (a_(n-1), a_n) durumu, farklı n değerleri için tekrar tekrar meydana gelecektir.

**Periyodikliğin Tespiti:**

Aynı durumlar tekrar ettiğinde, dizinin ilerleyişi aynı şekilde devam eder. Bu nedenle, durumların tekrarından dolayı, dizinin terimleri periyodik bir döngüye girer.

**Tek ve Çift İndisli Dizilerin İncelenmesi:**

Diziyi tek ve çift indisli terimlere ayırdık:  
- **Tek İndisli Terimler:** (a_1, a_3, a_5, …)  
- **Çift İndisli Terimler:** (a_2, a_4, a_6, …)

Yukarıdaki argümanımızı bu alt diziler için uygularsak, en az birinin bir yerden sonra periyodik olmak zorunda olduğunu görürüz. Çünkü durumların sonlu sayıda olması ve Pigeonhole Prensibi nedeniyle, ya tek indisli terimler ya da çift indisli terimler periyodik bir döngüye girecektir.

**Sonuç:**

Bu nedenle, verilen koşullar altında (a_1, a_3, a_5, …) veya (a_2, a_4, a_6, …) dizilerinden en az birinin bir yerden sonra periyodik olduğunu ispatlamış oluyoruz.


# Bilangan Berpangkat dan Bentuk Akar

## 1. Notasi Dasar

> [!definisi] Bilangan real  
> Bilangan real adalah bilangan yang dapat diletakkan pada garis bilangan. Himpunan bilangan real ditulis $\mathbb{R}$.

> [!definisi] Bilangan bulat  
> Bilangan bulat adalah bilangan tanpa bagian pecahan:  
> $$  
> \mathbb{Z}={\ldots,-3,-2,-1,0,1,2,3,\ldots}  
> $$

> [!definisi] Bilangan asli  
> Dalam catatan ini, bilangan asli berarti bilangan bulat positif:  
> $$  
> \mathbb{N}^+={1,2,3,\ldots}  
> $$

> [!definisi] Bilangan rasional  
> Bilangan rasional adalah bilangan yang dapat ditulis sebagai pecahan dua bilangan bulat:  
> $$  
> \frac{p}{q}  
> $$  
> dengan $p,q\in\mathbb{Z}$ dan $q\neq 0$.

> [!definisi] Bilangan irasional  
> Bilangan irasional adalah bilangan real yang tidak dapat ditulis sebagai $\frac{p}{q}$ dengan $p,q\in\mathbb{Z}$ dan $q\neq 0$.

Contoh bilangan rasional:  
$$  
2,\quad -5,\quad \frac{3}{4},\quad 0{,}125  
$$

Contoh bilangan irasional:  
$$  
\sqrt{2},\quad \sqrt{3},\quad \pi  
$$

Alasan $\sqrt{2}$ disebut irasional adalah tidak ada bilangan bulat $p$ dan $q\neq 0$ yang memenuhi $\sqrt{2}=\frac{p}{q}$.

---

## 2. Pengertian Bilangan Berpangkat

> [!definisi] Bilangan berpangkat  
> Bilangan berpangkat adalah bentuk perkalian berulang dari suatu bilangan yang sama.

Jika $a$ adalah bilangan real dan $n$ adalah bilangan bulat positif, maka:

$$  
a^n=\underbrace{a\times a\times a\times \cdots \times a}_{n\text{ faktor}}  
$$

Pada bentuk $a^n$:

- $a$ disebut **basis** atau **bilangan pokok**.
    
- $n$ disebut **eksponen** atau **pangkat**.
    
- $a^n$ dibaca “$a$ pangkat $n$”.
    

Contoh notasi:

$$  
2^5=2\times 2\times 2\times 2\times 2  
$$

$$  
(-3)^4=(-3)\times(-3)\times(-3)\times(-3)  
$$

Alasan definisi ini dipakai adalah karena pangkat positif menyatakan jumlah pengulangan perkalian dengan faktor yang sama.

---

## 3. Pangkat Satu

> [!definisi] Pangkat satu  
> Untuk setiap bilangan real $a$:  
> $$  
> a^1=a  
> $$

Alasannya, $a^1$ berarti ada tepat satu faktor, yaitu $a$ sendiri.

Contoh:

$$  
7^1=7  
$$

$$  
(-4)^1=-4  
$$

---

## 4. Pangkat Nol

> [!definisi] Pangkat nol  
> Untuk setiap bilangan real $a$ dengan $a\neq 0$:  
> $$  
> a^0=1  
> $$

Syarat $a\neq 0$ diperlukan karena $0^0$ tidak didefinisikan dalam aritmetika biasa.

Alasan $a^0=1$ berasal dari aturan pembagian pangkat dengan basis sama.

Untuk $a\neq 0$:

$$  
\frac{a^m}{a^m}=1  
$$

Di sisi lain, aturan pengurangan pangkat memberi:

$$  
\frac{a^m}{a^m}=a^{m-m}=a^0  
$$

Karena keduanya mewakili nilai yang sama, maka:

$$  
a^0=1  
$$

Contoh:

$$  
5^0=1  
$$

$$  
(-9)^0=1  
$$

$$  
\left(\frac{2}{3}\right)^0=1  
$$

Bentuk $0^0$ tidak didefinisikan karena jika mengikuti pola $a^0=1$, maka $0^0$ seolah-olah bernilai $1$, tetapi jika mengikuti pola $0^n=0$ untuk $n>0$, maka $0^0$ seolah-olah bernilai $0$. Dua pola menghasilkan tuntutan berbeda, sehingga bentuk itu tidak diberi nilai tunggal dalam konteks ini. Manusia menemukan cara membuat nol ribut bahkan ketika tidak melakukan apa-apa.

---

## 5. Pangkat Bilangan Bulat Positif

Jika $n\in\mathbb{N}^+$, maka $a^n$ berarti perkalian $a$ sebanyak $n$ faktor.

Beberapa sifat dasar:

$$  
0^n=0,\quad n\in\mathbb{N}^+  
$$

Alasannya, perkalian yang memuat faktor $0$ menghasilkan $0$.

$$  
1^n=1  
$$

Alasannya, perkalian berulang dari $1$ tetap menghasilkan $1$.

$$  
(-1)^n=  
\begin{cases}  
1, & n \text{ genap}\  
-1, & n \text{ ganjil}  
\end{cases}  
$$

Alasannya, pasangan faktor $(-1)(-1)$ menghasilkan $1$. Jika jumlah faktor $-1$ genap, semua faktor dapat dipasangkan. Jika ganjil, tersisa satu faktor $-1$.

---

## 6. Pangkat Genap dan Pangkat Ganjil

> [!definisi] Pangkat genap  
> Pangkat genap adalah pangkat dengan eksponen berupa bilangan genap, misalnya $2,4,6,8,\ldots$.

> [!definisi] Pangkat ganjil  
> Pangkat ganjil adalah pangkat dengan eksponen berupa bilangan ganjil, misalnya $1,3,5,7,\ldots$.

Jika $a$ bilangan real, maka:

$$  
a^{2k}\geq 0  
$$

untuk setiap bilangan bulat positif $k$.

Alasannya, pangkat genap dapat dipandang sebagai hasil perkalian pasangan:

$$  
a^{2k}=(a^k)^2  
$$

Kuadrat dari bilangan real selalu tidak negatif.

Untuk pangkat ganjil:

$$  
a^{2k+1}=a\cdot a^{2k}  
$$

Karena $a^{2k}\geq 0$, tanda $a^{2k+1}$ mengikuti tanda $a$.

Contoh:

$$  
(-2)^4=16  
$$

$$  
(-2)^5=-32  
$$

---

## 7. Perbedaan $-a^n$ dan $(-a)^n$

Tanda kurung menentukan bagian mana yang dipangkatkan.

$$  
-a^n=-(a^n)  
$$

Artinya, pangkat dikerjakan pada $a$ terlebih dahulu, kemudian hasilnya diberi tanda negatif.

Sedangkan:

$$  
(-a)^n  
$$

berarti bilangan $-a$ seluruhnya dipangkatkan.

Contoh:

$$  
-3^2=-(3^2)=-9  
$$

$$  
(-3)^2=9  
$$

Perbedaan ini muncul karena dalam urutan operasi, perpangkatan memiliki prioritas lebih tinggi daripada tanda negatif di depan bilangan, kecuali tanda negatif itu masuk ke dalam tanda kurung. Ya, tanda kurung menyelamatkan peradaban dari kekacauan notasi.

---

## 8. Aturan Perkalian Pangkat dengan Basis Sama

> [!definisi] Basis sama  
> Dua bentuk berpangkat memiliki basis sama jika bilangan pokoknya sama, misalnya $a^m$ dan $a^n$.

Untuk $m,n\in\mathbb{N}^+$:

$$  
a^m\cdot a^n=a^{m+n}  
$$

Alasannya, $a^m$ memuat $m$ faktor $a$, sedangkan $a^n$ memuat $n$ faktor $a$. Jika dikalikan, jumlah faktor $a$ menjadi $m+n$.

Ilustrasi:

$$  
a^3\cdot a^4=(a\cdot a\cdot a)(a\cdot a\cdot a\cdot a)=a^7  
$$

Maka:

$$  
a^3\cdot a^4=a^{3+4}=a^7  
$$

---

## 9. Aturan Pembagian Pangkat dengan Basis Sama

Untuk $a\neq 0$ dan $m,n$ bilangan bulat:

$$  
\frac{a^m}{a^n}=a^{m-n}  
$$

Syarat $a\neq 0$ diperlukan karena pembagian dengan nol tidak didefinisikan.

Alasan aturan ini berasal dari pembatalan faktor yang sama pada pembilang dan penyebut.

Jika $m>n$:

# $$  
\frac{a^m}{a^n}

# \frac{\underbrace{a\cdot a\cdots a}_{m\text{ faktor}}}  
{\underbrace{a\cdot a\cdots a}_{n\text{ faktor}}}

a^{m-n}  
$$

Contoh notasi:

$$  
\frac{x^7}{x^3}=x^4,\quad x\neq 0  
$$

Jika $m=n$, maka:

$$  
\frac{a^m}{a^m}=a^0=1  
$$

Jika $m<n$, hasilnya berkaitan dengan pangkat negatif.

---

## 10. Pangkat Negatif

> [!definisi] Pangkat negatif  
> Untuk $a\neq 0$ dan $n\in\mathbb{N}^+$:  
> $$  
> a^{-n}=\frac{1}{a^n}  
> $$

Syarat $a\neq 0$ diperlukan karena bentuk $\frac{1}{a^n}$ tidak terdefinisi jika $a=0$.

Alasan definisi ini dipilih adalah agar aturan pembagian pangkat tetap berlaku untuk kasus $m<n$.

Misalnya:

$$  
\frac{a^2}{a^5}=a^{2-5}=a^{-3}  
$$

Namun secara pembatalan faktor:

# $$  
\frac{a^2}{a^5}

# \frac{a\cdot a}{a\cdot a\cdot a\cdot a\cdot a}

\frac{1}{a^3}  
$$

Maka:

$$  
a^{-3}=\frac{1}{a^3}  
$$

Contoh:

$$  
2^{-4}=\frac{1}{2^4}=\frac{1}{16}  
$$

# $$  
\left(\frac{3}{5}\right)^{-2}

# \left(\frac{5}{3}\right)^2

\frac{25}{9}  
$$

Secara umum:

# $$  
\left(\frac{a}{b}\right)^{-n}

\left(\frac{b}{a}\right)^n  
$$

dengan $a\neq 0$ dan $b\neq 0$.

Alasannya:

# $$  
\left(\frac{a}{b}\right)^{-n}

# \frac{1}{\left(\frac{a}{b}\right)^n}

# \frac{1}{\frac{a^n}{b^n}}

# \frac{b^n}{a^n}

\left(\frac{b}{a}\right)^n  
$$

---

## 11. Aturan Pangkat dari Pangkat

Untuk bilangan real $a$ dan bilangan bulat positif $m,n$:

$$  
(a^m)^n=a^{mn}  
$$

Alasannya, $(a^m)^n$ berarti $a^m$ dikalikan sebanyak $n$ kali:

# $$  
(a^m)^n=  
\underbrace{a^m\cdot a^m\cdot \ldots \cdot a^m}_{n\text{ faktor}}

# a^{m+m+\cdots+m}

a^{mn}  
$$

Contoh notasi:

$$  
(x^3)^4=x^{12}  
$$

Untuk pangkat bilangan bulat secara umum, aturan ini berlaku jika bentuk yang muncul terdefinisi. Jika pangkat negatif terlibat, basis yang menerima pangkat negatif tidak boleh bernilai nol.

---

## 12. Aturan Pangkat dari Perkalian

Untuk bilangan real $a,b$ dan bilangan bulat positif $n$:

$$  
(ab)^n=a^n b^n  
$$

Alasannya:

$$  
(ab)^n=  
\underbrace{(ab)(ab)\cdots(ab)}_{n\text{ faktor}}  
$$

Karena perkalian bilangan real bersifat komutatif dan asosiatif, faktor-faktor $a$ dapat dikelompokkan dengan $a$, dan faktor-faktor $b$ dapat dikelompokkan dengan $b$:

$$  
(ab)^n=a^n b^n  
$$

Contoh:

$$  
(2x)^3=2^3x^3=8x^3  
$$

Untuk pangkat negatif, syarat tambahan diperlukan:

$$  
(ab)^{-n}=a^{-n}b^{-n}  
$$

berlaku jika $a\neq 0$ dan $b\neq 0$.

---

## 13. Aturan Pangkat dari Pembagian

Untuk $b\neq 0$ dan $n\in\mathbb{N}^+$:

$$  
\left(\frac{a}{b}\right)^n=\frac{a^n}{b^n}  
$$

Alasannya:

# $$  
\left(\frac{a}{b}\right)^n

# \underbrace{\frac{a}{b}\cdot\frac{a}{b}\cdots\frac{a}{b}}_{n\text{ faktor}}

\frac{a^n}{b^n}  
$$

Untuk pangkat negatif:

# $$  
\left(\frac{a}{b}\right)^{-n}

\left(\frac{b}{a}\right)^n  
$$

dengan $a\neq 0$ dan $b\neq 0$.

---

## 14. Pangkat Bilangan Bulat

> [!definisi] Pangkat bilangan bulat  
> Pangkat bilangan bulat adalah pangkat dengan eksponen anggota $\mathbb{Z}$, yaitu bilangan bulat positif, nol, atau negatif.

Untuk $a\neq 0$ dan $m,n\in\mathbb{Z}$, berlaku:

$$  
a^m\cdot a^n=a^{m+n}  
$$

$$  
\frac{a^m}{a^n}=a^{m-n}  
$$

$$  
(a^m)^n=a^{mn}  
$$

Syarat $a\neq 0$ diperlukan karena pangkat negatif dan pembagian dengan basis nol tidak didefinisikan.

Jika eksponen hanya bilangan bulat positif, basis $a=0$ masih dapat digunakan. Namun jika eksponen nol atau negatif muncul, $a=0$ perlu diperiksa secara khusus. Inilah bagian tempat notasi matematika menolak dimanfaatkan secara asal-asalan, sebuah kejadian yang terlalu jarang di dunia manusia.

---

## 15. Tabel Syarat Dasar Perpangkatan Real

|Bentuk|Syarat|Nilai / Keterangan|
|---|--:|---|
|$a^n$, $n\in\mathbb{N}^+$|$a\in\mathbb{R}$|Terdefinisi|
|$a^0$|$a\neq 0$|$1$|
|$a^{-n}$|$a\neq 0$|$\frac{1}{a^n}$|
|$0^n$, $n\in\mathbb{N}^+$|Terdefinisi|$0$|
|$0^0$|Tidak didefinisikan|Tidak punya nilai tunggal|
|$0^{-n}$|Tidak didefinisikan|Karena memuat $\frac{1}{0^n}$|

---

## 16. Akar Bilangan

> [!definisi] Akar ke-$n$  
> Jika $n\in\mathbb{N}^+$ dan $x,y\in\mathbb{R}$, maka $y$ disebut akar ke-$n$ dari $x$ jika:  
> $$  
> y^n=x  
> $$

Misalnya, $3$ adalah akar kuadrat dari $9$ karena:

$$  
3^2=9  
$$

Bilangan $-3$ juga akar kuadrat dari $9$ karena:

$$  
(-3)^2=9  
$$

Jadi, frasa “akar kuadrat dari $9$” dapat mengarah pada dua bilangan, yaitu $3$ dan $-3$, jika tidak dijelaskan maksudnya.

Untuk menghilangkan ambiguitas, digunakan konsep **akar utama**.

---

## 17. Akar Utama

> [!definisi] Akar utama  
> Akar utama adalah nilai akar yang dipilih sebagai nilai standar dari simbol akar $\sqrt[n]{x}$.

Untuk $n$ genap:

$$  
\sqrt[n]{x}  
$$

didefinisikan sebagai bilangan real **tidak negatif** yang jika dipangkatkan $n$ menghasilkan $x$.

Karena pangkat genap bilangan real selalu tidak negatif, maka:

$$  
\sqrt[n]{x}  
$$

untuk $n$ genap hanya terdefinisi dalam bilangan real jika:

$$  
x\geq 0  
$$

Contoh:

$$  
\sqrt{9}=3  
$$

bukan $-3$, karena simbol $\sqrt{9}$ menyatakan akar utama.

Untuk $n$ ganjil:

$$  
\sqrt[n]{x}  
$$

terdefinisi untuk semua bilangan real $x$.

Contoh:

$$  
\sqrt[3]{8}=2  
$$

$$  
\sqrt[3]{-8}=-2  
$$

Alasannya, pangkat ganjil mempertahankan tanda bilangan: bilangan positif berpangkat ganjil menghasilkan positif, bilangan negatif berpangkat ganjil menghasilkan negatif.

---

## 18. Notasi Bentuk Akar

> [!definisi] Bentuk akar  
> Bentuk akar adalah bentuk matematika yang memuat simbol akar, misalnya:  
> $$  
> \sqrt{2},\quad \sqrt{5},\quad \sqrt[3]{7},\quad 2\sqrt{3}  
> $$

Pada bentuk:

$$  
\sqrt[n]{a}  
$$

bagian-bagiannya adalah:

- $n$ disebut **indeks akar**.
    
- $a$ disebut **radikan**, yaitu bilangan atau ekspresi di dalam tanda akar.
    
- Simbol $\sqrt{\phantom{x}}$ disebut **tanda akar** atau **radikal**.
    

Jika indeks akar tidak ditulis, indeksnya dianggap $2$.

$$  
\sqrt{a}=\sqrt[2]{a}  
$$

Jadi:

$$  
\sqrt{16}=\sqrt[2]{16}  
$$

---

## 19. Akar Kuadrat

> [!definisi] Akar kuadrat  
> Akar kuadrat dari $a$ adalah bilangan yang kuadratnya sama dengan $a$.

Simbol akar kuadrat utama:

$$  
\sqrt{a}  
$$

Untuk bilangan real, $\sqrt{a}$ terdefinisi jika:

$$  
a\geq 0  
$$

dan nilainya selalu:

$$  
\sqrt{a}\geq 0  
$$

Contoh:

$$  
\sqrt{25}=5  
$$

$$  
\sqrt{0}=0  
$$

Bentuk $\sqrt{-25}$ tidak mempunyai nilai real karena tidak ada bilangan real yang kuadratnya negatif.

---

## 20. Akar Pangkat Tiga

> [!definisi] Akar pangkat tiga  
> Akar pangkat tiga dari $a$ adalah bilangan yang jika dipangkatkan tiga menghasilkan $a$.

Simbolnya:

$$  
\sqrt[3]{a}  
$$

Untuk semua $a\in\mathbb{R}$, bentuk $\sqrt[3]{a}$ terdefinisi.

Contoh:

$$  
\sqrt[3]{27}=3  
$$

$$  
\sqrt[3]{-27}=-3  
$$

Alasannya, fungsi pangkat tiga dapat menghasilkan bilangan positif, nol, atau negatif sesuai tanda basisnya.

---

## 21. Hubungan Pangkat dan Akar

Akar merupakan kebalikan dari pangkat dalam batas tertentu.

Jika $a\geq 0$, maka:

$$  
(\sqrt{a})^2=a  
$$

dan

$$  
\sqrt{a^2}=|a|  
$$

> [!definisi] Nilai mutlak  
> Nilai mutlak $|a|$ adalah jarak $a$ dari nol pada garis bilangan:  
> $$  
> |a|=  
> \begin{cases}  
> a, & a\geq 0\  
> -a, & a<0  
> \end{cases}  
> $$

Mengapa $\sqrt{a^2}=|a|$, bukan selalu $a$?

Karena $\sqrt{a^2}$ adalah akar kuadrat utama, sehingga nilainya harus tidak negatif. Jika $a<0$, maka $a$ negatif, tetapi $|a|$ positif.

Contoh:

$$  
\sqrt{(-5)^2}=\sqrt{25}=5=|-5|  
$$

Bukan:

$$  
\sqrt{(-5)^2}=-5  
$$

Untuk akar pangkat ganjil:

$$  
\sqrt[3]{a^3}=a  
$$

untuk semua $a\in\mathbb{R}$.

Alasannya, akar pangkat ganjil dapat bernilai negatif, sehingga tidak perlu dipaksa menjadi nilai tidak negatif.

---

## 22. Pangkat Pecahan

> [!definisi] Pangkat pecahan  
> Pangkat pecahan adalah pangkat dengan eksponen berbentuk pecahan, misalnya:  
> $$  
> a^{\frac{1}{2}},\quad a^{\frac{2}{3}},\quad a^{-\frac{3}{4}}  
> $$

Untuk $a\geq 0$ dan $n\in\mathbb{N}^+$:

$$  
a^{\frac{1}{n}}=\sqrt[n]{a}  
$$

Untuk $a\geq 0$, $m\in\mathbb{Z}$, dan $n\in\mathbb{N}^+$:

$$  
a^{\frac{m}{n}}=\sqrt[n]{a^m}  
$$

Jika $m>0$, bentuk ini juga dapat ditulis:

$$  
a^{\frac{m}{n}}=(\sqrt[n]{a})^m  
$$

Alasan definisi ini dipakai adalah agar aturan pangkat dari pangkat tetap berlaku:

$$  
\left(a^{\frac{1}{n}}\right)^n=a^{\frac{1}{n}\cdot n}=a  
$$

Jadi $a^{\frac{1}{n}}$ harus berarti bilangan yang jika dipangkatkan $n$ menghasilkan $a$, yaitu $\sqrt[n]{a}$.

Contoh notasi:

$$  
16^{\frac{1}{2}}=\sqrt{16}=4  
$$

$$  
27^{\frac{1}{3}}=\sqrt[3]{27}=3  
$$

$$  
81^{\frac{3}{4}}=(\sqrt[4]{81})^3=3^3=27  
$$

---

## 23. Pangkat Rasional

> [!definisi] Pangkat rasional  
> Pangkat rasional adalah pangkat dengan eksponen berupa bilangan rasional, yaitu bilangan yang dapat ditulis sebagai $\frac{m}{n}$ dengan $m,n\in\mathbb{Z}$ dan $n\neq 0$.

Dalam pembahasan bilangan real, definisi yang paling aman untuk semua aturan pangkat adalah:

$$  
a^r  
$$

dengan $a>0$ dan $r\in\mathbb{Q}$.

Jika $a>0$, $m\in\mathbb{Z}$, dan $n\in\mathbb{N}^+$, maka:

$$  
a^{\frac{m}{n}}=\sqrt[n]{a^m}  
$$

Karena $a>0$, semua akar yang muncul bernilai real dan positif.

Untuk $a=0$, bentuk $0^r$ hanya terdefinisi jika $r>0$.

Contoh:

$$  
0^{\frac{1}{2}}=0  
$$

Tetapi:

$$  
0^{-\frac{1}{2}}  
$$

tidak didefinisikan karena sama dengan:

$$  
\frac{1}{0^{\frac{1}{2}}}=\frac{1}{0}  
$$

Untuk $a<0$, pangkat rasional harus ditangani hati-hati. Bentuk seperti:

$$  
(-8)^{\frac{1}{3}}  
$$

dapat bernilai real karena:

$$  
\sqrt[3]{-8}=-2  
$$

Namun aturan pangkat rasional pada basis negatif tidak selalu bebas digunakan karena pecahan eksponen dapat ditulis dalam bentuk berbeda.

Misalnya:

$$  
\frac{1}{3}=\frac{2}{6}  
$$

Tetapi bentuk:

$$  
(-8)^{\frac{1}{3}}  
$$

berhubungan dengan akar pangkat tiga, sedangkan:

$$  
(-8)^{\frac{2}{6}}  
$$

dapat menimbulkan akar pangkat enam jika ditafsirkan langsung sebagai $\sqrt[6]{(-8)^2}$.

Karena akar pangkat enam adalah akar genap, bentuknya mengikuti aturan berbeda. Itulah sebabnya dalam aljabar real, aturan pangkat rasional paling bersih diberlakukan untuk basis positif.

---

## 24. Aturan Pangkat Rasional

Untuk $a>0$, $b>0$, dan $r,s\in\mathbb{Q}$, berlaku:

$$  
a^r\cdot a^s=a^{r+s}  
$$

$$  
\frac{a^r}{a^s}=a^{r-s}  
$$

$$  
(a^r)^s=a^{rs}  
$$

$$  
(ab)^r=a^r b^r  
$$

$$  
\left(\frac{a}{b}\right)^r=\frac{a^r}{b^r}  
$$

Syarat $a>0$ dan $b>0$ membuat semua bentuk akar yang terkait dengan pangkat rasional terdefinisi sebagai bilangan real positif. Dengan begitu, perubahan bentuk eksponen tidak menyebabkan pertentangan tanda atau masalah akar genap dari bilangan negatif.

---

## 25. Bentuk Akar Sederhana

> [!definisi] Bentuk akar sederhana  
> Bentuk akar sederhana adalah bentuk akar yang radikannya tidak lagi memuat faktor pangkat sempurna yang dapat dikeluarkan dari tanda akar.

> [!definisi] Kuadrat sempurna  
> Kuadrat sempurna adalah bilangan yang merupakan hasil kuadrat bilangan bulat.  
> Contoh:  
> $$  
> 1,4,9,16,25,36,49,\ldots  
> $$

> [!definisi] Pangkat-$n$ sempurna  
> Pangkat-$n$ sempurna adalah bilangan yang dapat ditulis sebagai $k^n$ untuk suatu bilangan bulat $k$.

Contoh pangkat tiga sempurna:

$$  
1,8,27,64,125,\ldots  
$$

Bentuk:

$$  
\sqrt{12}  
$$

belum sederhana karena:

$$  
12=4\cdot 3  
$$

dan $4$ adalah kuadrat sempurna.

Maka:

$$  
\sqrt{12}=\sqrt{4\cdot 3}=2\sqrt{3}  
$$

Alasan $2$ dapat keluar dari akar adalah:

$$  
\sqrt{4}=2  
$$

Bentuk:

$$  
\sqrt[3]{54}  
$$

belum sederhana karena:

$$  
54=27\cdot 2  
$$

dan $27$ adalah pangkat tiga sempurna.

Maka:

$$  
\sqrt[3]{54}=\sqrt[3]{27\cdot 2}=3\sqrt[3]{2}  
$$

---

## 26. Sifat Perkalian Bentuk Akar

Untuk $a\geq 0$ dan $b\geq 0$:

$$  
\sqrt{a}\cdot\sqrt{b}=\sqrt{ab}  
$$

Alasannya, kedua ruas bernilai tidak negatif, dan kuadrat keduanya sama:

$$  
(\sqrt{a}\cdot\sqrt{b})^2=(\sqrt{a})^2(\sqrt{b})^2=ab  
$$

Karena akar utama dari $ab$ adalah bilangan tidak negatif yang kuadratnya $ab$, maka:

$$  
\sqrt{a}\cdot\sqrt{b}=\sqrt{ab}  
$$

Contoh:

$$  
\sqrt{2}\cdot\sqrt{8}=\sqrt{16}=4  
$$

Untuk akar indeks $n$:

Jika $n$ genap, $a\geq 0$ dan $b\geq 0$:

$$  
\sqrt[n]{a}\cdot\sqrt[n]{b}=\sqrt[n]{ab}  
$$

Jika $n$ ganjil, aturan ini berlaku untuk semua $a,b\in\mathbb{R}$:

$$  
\sqrt[n]{a}\cdot\sqrt[n]{b}=\sqrt[n]{ab}  
$$

Alasannya, akar ganjil terdefinisi untuk semua bilangan real.

---

## 27. Sifat Pembagian Bentuk Akar

Untuk $a\geq 0$ dan $b>0$:

$$  
\frac{\sqrt{a}}{\sqrt{b}}=\sqrt{\frac{a}{b}}  
$$

Syarat $b>0$ diperlukan karena penyebut tidak boleh nol dan $\sqrt{b}$ harus terdefinisi.

Alasannya, kedua ruas bernilai tidak negatif, dan kuadrat keduanya sama:

# $$  
\left(\frac{\sqrt{a}}{\sqrt{b}}\right)^2

\frac{a}{b}  
$$

Maka bentuk itu sama dengan akar utama dari $\frac{a}{b}$.

Untuk akar indeks $n$:

Jika $n$ genap, $a\geq 0$ dan $b>0$:

$$  
\frac{\sqrt[n]{a}}{\sqrt[n]{b}}=\sqrt[n]{\frac{a}{b}}  
$$

Jika $n$ ganjil, aturan ini berlaku untuk $b\neq 0$:

$$  
\frac{\sqrt[n]{a}}{\sqrt[n]{b}}=\sqrt[n]{\frac{a}{b}}  
$$

---

## 28. Penjumlahan dan Pengurangan Bentuk Akar

Bentuk akar hanya dapat dijumlahkan atau dikurangkan secara langsung jika memiliki bagian akar yang sama.

> [!definisi] Suku sejenis pada bentuk akar  
> Dua suku bentuk akar disebut sejenis jika memiliki bagian akar yang sama persis setelah disederhanakan.

Contoh suku sejenis:

$$  
2\sqrt{3},\quad 5\sqrt{3},\quad -\sqrt{3}  
$$

Ketiganya sejenis karena sama-sama memiliki bagian akar $\sqrt{3}$.

Aturannya:

$$  
a\sqrt{c}+b\sqrt{c}=(a+b)\sqrt{c}  
$$

Alasannya, $\sqrt{c}$ menjadi faktor yang sama:

$$  
a\sqrt{c}+b\sqrt{c}=(a+b)\sqrt{c}  
$$

Contoh:

$$  
3\sqrt{5}+7\sqrt{5}=10\sqrt{5}  
$$

Bentuk:

$$  
\sqrt{2}+\sqrt{3}  
$$

tidak dapat digabung menjadi:

$$  
\sqrt{5}  
$$

karena:

$$  
(\sqrt{2}+\sqrt{3})^2=5+2\sqrt{6}  
$$

sedangkan:

$$  
(\sqrt{5})^2=5  
$$

Kedua bentuk tidak sama.

Kadang dua bentuk akar tampak tidak sejenis sebelum disederhanakan.

Contoh:

$$  
\sqrt{12}+2\sqrt{3}  
$$

Karena:

$$  
\sqrt{12}=2\sqrt{3}  
$$

maka:

$$  
\sqrt{12}+2\sqrt{3}=4\sqrt{3}  
$$

---

## 29. Menyederhanakan Akar dengan Faktorisasi Prima

> [!definisi] Faktorisasi prima  
> Faktorisasi prima adalah penulisan bilangan sebagai hasil kali bilangan-bilangan prima.

Contoh:

$$  
72=2^3\cdot 3^2  
$$

Untuk akar kuadrat, setiap pasangan faktor yang sama dapat dikeluarkan dari akar.

$$  
\sqrt{p^2}=p  
$$

untuk $p\geq 0$.

Secara umum:

$$  
\sqrt{p^{2k}}=p^k  
$$

dan

$$  
\sqrt{p^{2k+1}}=p^k\sqrt{p}  
$$

untuk bilangan prima positif $p$.

Contoh bentuk:

# $$  
\sqrt{72}

# \sqrt{2^3\cdot 3^2}

# \sqrt{2^2\cdot 3^2\cdot 2}

# 2\cdot 3\sqrt{2}

6\sqrt{2}  
$$

Untuk akar pangkat tiga, setiap tiga faktor yang sama dapat dikeluarkan dari akar.

$$  
\sqrt[3]{p^3}=p  
$$

Secara umum:

$$  
\sqrt[3]{p^{3k}}=p^k  
$$

dan

$$  
\sqrt[3]{p^{3k+r}}=p^k\sqrt[3]{p^r}  
$$

dengan $r=1$ atau $r=2$.

Contoh bentuk:

# $$  
\sqrt[3]{108}

# \sqrt[3]{2^2\cdot 3^3}

3\sqrt[3]{4}  
$$

Untuk akar indeks $n$:

$$  
\sqrt[n]{p^{nq+r}}=p^q\sqrt[n]{p^r}  
$$

dengan $0\leq r<n$.

Alasannya, $p^{nq+r}=p^{nq}\cdot p^r=(p^q)^n\cdot p^r$, sehingga bagian $(p^q)^n$ dapat keluar dari akar sebagai $p^q$.

---

## 30. Bentuk Akar dengan Variabel

Jika variabel muncul di dalam akar, tanda nilai mutlak perlu diperhatikan untuk akar genap.

Untuk setiap $x\in\mathbb{R}$:

$$  
\sqrt{x^2}=|x|  
$$

bukan selalu $x$.

Secara umum, untuk akar genap:

$$  
\sqrt[2n]{x^{2n}}=|x|  
$$

Alasannya, akar genap utama harus bernilai tidak negatif.

Untuk akar ganjil:

$$  
\sqrt[2n+1]{x^{2n+1}}=x  
$$

Alasannya, akar ganjil boleh bernilai negatif, sehingga tanda asli $x$ tetap dipertahankan.

Contoh:

$$  
\sqrt{x^4}=x^2  
$$

Karena $x^2\geq 0$ untuk semua $x\in\mathbb{R}$.

Namun:

$$  
\sqrt{x^6}=|x^3|  
$$

Karena:

$$  
x^6=(x^3)^2  
$$

dan akar kuadrat utama dari $(x^3)^2$ adalah $|x^3|$.

Jika diketahui $x\geq 0$, maka $|x|=x$.

Jika diketahui $x<0$, maka $|x|=-x$.

---

## 31. Mengubah Bentuk Akar ke Bentuk Pangkat

Bentuk akar dapat ditulis sebagai pangkat pecahan.

$$  
\sqrt[n]{a}=a^{\frac{1}{n}}  
$$

Untuk $a\geq 0$ dan $m\in\mathbb{Z}$:

$$  
\sqrt[n]{a^m}=a^{\frac{m}{n}}  
$$

Contoh:

$$  
\sqrt{x}=x^{\frac{1}{2}}  
$$

$$  
\sqrt[3]{x^2}=x^{\frac{2}{3}}  
$$

$$  
\frac{1}{\sqrt{x}}=x^{-\frac{1}{2}}  
$$

dengan $x>0$.

Syarat $x>0$ pada bentuk terakhir diperlukan karena penyebut $\sqrt{x}$ tidak boleh nol.

---

## 32. Mengubah Bentuk Pangkat ke Bentuk Akar

Bentuk pangkat pecahan dapat ditulis sebagai bentuk akar.

$$  
a^{\frac{m}{n}}=\sqrt[n]{a^m}  
$$

Untuk $a\geq 0$, bentuk itu juga dapat ditulis:

$$  
a^{\frac{m}{n}}=(\sqrt[n]{a})^m  
$$

Contoh:

$$  
x^{\frac{3}{2}}=\sqrt{x^3}=(\sqrt{x})^3  
$$

dengan $x\geq 0$.

$$  
x^{-\frac{2}{3}}=\frac{1}{x^{\frac{2}{3}}}=\frac{1}{\sqrt[3]{x^2}}  
$$

dengan $x\neq 0$.

Syarat $x\neq 0$ diperlukan karena pangkat negatif menghasilkan bentuk kebalikan.

---

## 33. Merasionalkan Penyebut

> [!definisi] Merasionalkan penyebut  
> Merasionalkan penyebut adalah mengubah pecahan yang penyebutnya memuat bentuk akar menjadi pecahan ekuivalen dengan penyebut rasional.

> [!definisi] Pecahan ekuivalen  
> Dua pecahan disebut ekuivalen jika nilainya sama.

Merasionalkan penyebut tidak mengubah nilai pecahan, karena pembilang dan penyebut dikalikan dengan bentuk yang sama dan tidak bernilai nol.

### 33.1 Penyebut Berupa Akar Kuadrat Tunggal

Untuk $a>0$:

$$  
\frac{1}{\sqrt{a}}=\frac{\sqrt{a}}{a}  
$$

Alasannya:

# $$  
\frac{1}{\sqrt{a}}\cdot \frac{\sqrt{a}}{\sqrt{a}}

\frac{\sqrt{a}}{a}  
$$

karena:

$$  
\sqrt{a}\cdot\sqrt{a}=a  
$$

Contoh:

# $$  
\frac{5}{\sqrt{3}}

\frac{5\sqrt{3}}{3}  
$$

### 33.2 Penyebut Berupa $b\sqrt{a}$

Untuk $a>0$ dan $b\neq 0$:

# $$  
\frac{c}{b\sqrt{a}}

\frac{c\sqrt{a}}{ba}  
$$

Alasannya, penyebut dikalikan dengan $\sqrt{a}$:

$$  
b\sqrt{a}\cdot\sqrt{a}=ba  
$$

### 33.3 Penyebut Berupa Akar Pangkat $n$

Untuk $a>0$:

# $$  
\frac{1}{\sqrt[n]{a^k}}

\frac{\sqrt[n]{a^{n-k}}}{a}  
$$

dengan $1\leq k<n$.

Alasannya:

# $$  
\sqrt[n]{a^k}\cdot \sqrt[n]{a^{n-k}}

# \sqrt[n]{a^n}

a  
$$

Contoh:

# $$  
\frac{1}{\sqrt[3]{2}}

# \frac{\sqrt[3]{2^2}}{2}

\frac{\sqrt[3]{4}}{2}  
$$

### 33.4 Penyebut Berbentuk Dua Suku dengan Akar

> [!definisi] Sekawan  
> Bentuk sekawan adalah pasangan dua suku yang hanya berbeda tanda di antara kedua sukunya.

Contoh pasangan sekawan:

$$  
a+\sqrt{b}  
\quad \text{dan} \quad  
a-\sqrt{b}  
$$

$$  
\sqrt{a}+\sqrt{b}  
\quad \text{dan} \quad  
\sqrt{a}-\sqrt{b}  
$$

Dasar merasionalkan dengan sekawan adalah identitas selisih kuadrat:

$$  
(x+y)(x-y)=x^2-y^2  
$$

Jika penyebutnya $\sqrt{a}+\sqrt{b}$, maka:

# $$  
\frac{1}{\sqrt{a}+\sqrt{b}}

\frac{\sqrt{a}-\sqrt{b}}{(\sqrt{a}+\sqrt{b})(\sqrt{a}-\sqrt{b})}  
$$

Penyebutnya menjadi:

$$  
(\sqrt{a})^2-(\sqrt{b})^2=a-b  
$$

Maka:

# $$  
\frac{1}{\sqrt{a}+\sqrt{b}}

\frac{\sqrt{a}-\sqrt{b}}{a-b}  
$$

dengan $a\geq 0$, $b\geq 0$, dan $a\neq b$.

Syarat $a\neq b$ diperlukan karena penyebut akhir $a-b$ tidak boleh nol.

---

## 34. Bentuk Sekawan dan Identitas Selisih Kuadrat

Identitas:

$$  
(x+y)(x-y)=x^2-y^2  
$$

berlaku karena:

$$  
(x+y)(x-y)=x^2-xy+xy-y^2=x^2-y^2  
$$

Suku $-xy$ dan $xy$ saling meniadakan.

Dalam bentuk akar:

$$  
(\sqrt{a}+\sqrt{b})(\sqrt{a}-\sqrt{b})=a-b  
$$

karena:

$$  
(\sqrt{a})^2=a  
$$

dan:

$$  
(\sqrt{b})^2=b  
$$

Contoh bentuk:

$$  
(3+\sqrt{5})(3-\sqrt{5})=9-5=4  
$$

Sekawan membuat penyebut yang semula memuat akar berubah menjadi bentuk tanpa akar karena hasil perkalian memakai selisih kuadrat.

---

## 35. Operasi Campuran Pangkat dan Akar

Bentuk pangkat dan akar sering muncul dalam ekspresi yang sama. Urutan konsepnya:

1. Akar dapat ditulis sebagai pangkat pecahan.
    
2. Pangkat negatif dapat ditulis sebagai kebalikan.
    
3. Aturan pangkat hanya digunakan jika syarat basisnya terpenuhi.
    

Contoh bentuk identitas:

# $$  
\sqrt{x}\cdot x^{\frac{3}{2}}

# x^{\frac{1}{2}}\cdot x^{\frac{3}{2}}

x^2  
$$

dengan $x\geq 0$.

Alasannya:

$$  
\frac{1}{2}+\frac{3}{2}=2  
$$

Contoh lain:

$$  
\frac{x^{\frac{5}{3}}}{x^{\frac{2}{3}}}=x  
$$

dengan $x>0$.

Alasannya:

$$  
\frac{5}{3}-\frac{2}{3}=1  
$$

Syarat $x>0$ membuat pangkat rasional terdefinisi tanpa ambiguitas.

---

## 36. Bilangan Berpangkat dengan Basis Pecahan

Jika basis berupa pecahan:

$$  
\left(\frac{a}{b}\right)^n=\frac{a^n}{b^n}  
$$

dengan $b\neq 0$.

Contoh:

$$  
\left(\frac{2}{3}\right)^4=\frac{2^4}{3^4}=\frac{16}{81}  
$$

Jika pangkatnya negatif:

$$  
\left(\frac{a}{b}\right)^{-n}=\left(\frac{b}{a}\right)^n  
$$

dengan $a\neq 0$ dan $b\neq 0$.

Contoh:

# $$  
\left(\frac{2}{5}\right)^{-3}

# \left(\frac{5}{2}\right)^3

\frac{125}{8}  
$$

Alasannya, pangkat negatif berarti kebalikan.

---

## 37. Bilangan Berpangkat dengan Basis Desimal

Desimal berhingga dapat diubah menjadi pecahan, lalu dipangkatkan.

Contoh:

$$  
0{,}2=\frac{1}{5}  
$$

Maka:

$$  
(0{,}2)^3=\left(\frac{1}{5}\right)^3=\frac{1}{125}=0{,}008  
$$

Alasannya, desimal berhingga selalu dapat ditulis sebagai pecahan dengan penyebut berupa pangkat $10$.

Contoh:

$$  
0{,}125=\frac{125}{1000}=\frac{1}{8}  
$$

Sehingga:

# $$  
(0{,}125)^{\frac{2}{3}}

# \left(\frac{1}{8}\right)^{\frac{2}{3}}

# \left(\sqrt[3]{\frac{1}{8}}\right)^2

# \left(\frac{1}{2}\right)^2

\frac{1}{4}  
$$

---

## 38. Pangkat Sepuluh

> [!definisi] Pangkat sepuluh  
> Pangkat sepuluh adalah bentuk $10^n$ dengan $n$ bilangan bulat.

Untuk $n\in\mathbb{N}^+$:

$$  
10^n=1\underbrace{00\ldots0}_{n\text{ nol}}  
$$

Contoh:

$$  
10^1=10  
$$

$$  
10^2=100  
$$

$$  
10^3=1000  
$$

Untuk pangkat negatif:

$$  
10^{-n}=\frac{1}{10^n}  
$$

Contoh:

$$  
10^{-1}=0{,}1  
$$

$$  
10^{-2}=0{,}01  
$$

$$  
10^{-3}=0{,}001  
$$

Alasannya, membagi dengan $10^n$ menggeser nilai tempat desimal sebanyak $n$ posisi ke kanan pada penyebut, atau setara dengan menggeser koma desimal ke kiri pada nilai bilangan.

---

## 39. Notasi Ilmiah

> [!definisi] Notasi ilmiah  
> Notasi ilmiah adalah bentuk penulisan bilangan:  
> $$  
> a\times 10^n  
> $$  
> dengan:  
> $$  
> 1\leq |a|<10  
> $$  
> dan $n\in\mathbb{Z}$.

Bilangan $a$ disebut koefisien, sedangkan $10^n$ menunjukkan skala berdasarkan pangkat sepuluh.

Contoh:

$$  
3500=3{,}5\times 10^3  
$$

$$  
0{,}0042=4{,}2\times 10^{-3}  
$$

Alasan syarat $1\leq |a|<10$ digunakan adalah agar representasi notasi ilmiah menjadi tunggal.

Misalnya, bilangan $3500$ dapat ditulis sebagai:

$$  
35\times 10^2  
$$

atau:

$$  
0{,}35\times 10^4  
$$

Namun hanya:

$$  
3{,}5\times 10^3  
$$

yang memenuhi $1\leq |a|<10$.

---

## 40. Operasi dalam Notasi Ilmiah

Untuk perkalian:

# $$  
(a\times 10^m)(b\times 10^n)

(ab)\times 10^{m+n}  
$$

Alasannya:

$$  
10^m\cdot 10^n=10^{m+n}  
$$

Untuk pembagian:

# $$  
\frac{a\times 10^m}{b\times 10^n}

\frac{a}{b}\times 10^{m-n}  
$$

dengan $b\neq 0$.

Alasannya:

$$  
\frac{10^m}{10^n}=10^{m-n}  
$$

Jika koefisien hasil tidak memenuhi $1\leq |a|<10$, koefisien diubah kembali dengan menyesuaikan pangkat sepuluh.

Contoh bentuk:

$$  
(3\times 10^4)(4\times 10^5)=12\times 10^9=1{,}2\times 10^{10}  
$$

Perubahan dari $12\times 10^9$ ke $1{,}2\times 10^{10}$ terjadi karena:

$$  
12=1{,}2\times 10  
$$

sehingga:

$$  
12\times 10^9=(1{,}2\times 10)\times 10^9=1{,}2\times 10^{10}  
$$

---

## 41. Bentuk Akar sebagai Bilangan Irasional

Tidak semua bentuk akar bernilai irasional.

Contoh bentuk akar yang rasional:

$$  
\sqrt{4}=2  
$$

$$  
\sqrt{9}=3  
$$

$$  
\sqrt[3]{8}=2  
$$

Bentuk akar seperti ini menghasilkan bilangan rasional karena radikannya merupakan pangkat sempurna.

Bentuk akar seperti:

$$  
\sqrt{2},\quad \sqrt{3},\quad \sqrt{5}  
$$

merupakan bilangan irasional.

Untuk akar kuadrat bilangan bulat positif $n$, berlaku:

$$  
\sqrt{n}  
$$

rasional jika dan hanya jika $n$ adalah kuadrat sempurna.

Alasannya, jika $\sqrt{n}=r$ rasional dan $n$ bilangan bulat, maka struktur faktor prima $n$ harus memiliki pangkat genap untuk setiap faktor primanya. Itulah ciri bilangan kuadrat sempurna.

Contoh:

$$  
36=2^2\cdot 3^2  
$$

Semua pangkat faktor primanya genap, sehingga:

$$  
\sqrt{36}=6  
$$

Sedangkan:

$$  
12=2^2\cdot 3  
$$

Faktor $3$ berpangkat ganjil, sehingga:

$$  
\sqrt{12}=2\sqrt{3}  
$$

dan masih memuat akar irasional.

---

## 42. Penyederhanaan Bentuk Akar Kuadrat Bilangan Bulat

Jika $a$ bilangan bulat positif, maka penyederhanaan $\sqrt{a}$ bergantung pada pemisahan faktor kuadrat sempurna terbesar.

Jika:

$$  
a=k^2b  
$$

dengan $k\in\mathbb{N}^+$ dan $b$ tidak memuat faktor kuadrat sempurna selain $1$, maka:

$$  
\sqrt{a}=k\sqrt{b}  
$$

Alasannya:

$$  
\sqrt{k^2b}=\sqrt{k^2}\sqrt{b}=k\sqrt{b}  
$$

Contoh bentuk:

# $$  
\sqrt{180}

# \sqrt{36\cdot 5}

6\sqrt{5}  
$$

Di sini $36$ adalah faktor kuadrat sempurna terbesar dari $180$.

---

## 43. Penyederhanaan Bentuk Akar Pangkat Tiga

Jika:

$$  
a=k^3b  
$$

maka:

$$  
\sqrt[3]{a}=k\sqrt[3]{b}  
$$

Alasannya:

$$  
\sqrt[3]{k^3b}=\sqrt[3]{k^3}\sqrt[3]{b}=k\sqrt[3]{b}  
$$

Contoh bentuk:

# $$  
\sqrt[3]{250}

# \sqrt[3]{125\cdot 2}

5\sqrt[3]{2}  
$$

Untuk akar pangkat tiga, radikan boleh negatif.

Contoh:

# $$  
\sqrt[3]{-250}

# \sqrt[3]{-125\cdot 2}

-5\sqrt[3]{2}  
$$

Alasannya:

$$  
(-5)^3=-125  
$$

---

## 44. Hubungan $\sqrt[n]{a^n}$ dengan Tanda Basis

Untuk $n$ genap:

$$  
\sqrt[n]{a^n}=|a|  
$$

untuk semua $a\in\mathbb{R}$.

Alasannya, $a^n$ sama dengan $(-a)^n$ jika $n$ genap, sehingga akar utama tidak dapat mempertahankan tanda negatif. Akar utama selalu memilih nilai tidak negatif.

Untuk $n$ ganjil:

$$  
\sqrt[n]{a^n}=a  
$$

untuk semua $a\in\mathbb{R}$.

Alasannya, fungsi pangkat ganjil mempertahankan tanda basis.

Contoh:

$$  
\sqrt[4]{(-2)^4}=2  
$$

bukan $-2$.

Tetapi:

$$  
\sqrt[3]{(-2)^3}=-2  
$$

---

## 45. Menyamakan Indeks Akar

> [!definisi] Indeks akar sejenis  
> Bentuk akar memiliki indeks sejenis jika indeks akarnya sama.

Contoh:

$$  
\sqrt[3]{2}  
\quad \text{dan} \quad  
\sqrt[3]{5}  
$$

memiliki indeks sama, yaitu $3$.

Untuk mengalikan atau membagi akar dengan indeks berbeda, bentuk akar dapat diubah menjadi pangkat pecahan terlebih dahulu.

Contoh bentuk:

# $$  
\sqrt{a}\cdot\sqrt[3]{a}

# a^{\frac{1}{2}}\cdot a^{\frac{1}{3}}

# a^{\frac{5}{6}}

\sqrt[6]{a^5}  
$$

dengan $a\geq 0$.

Alasan penyebut $2$ dan $3$ berubah menjadi $6$ adalah karena:

$$  
\frac{1}{2}+\frac{1}{3}=\frac{3}{6}+\frac{2}{6}=\frac{5}{6}  
$$

---

## 46. Membandingkan Bilangan Berpangkat

> [!definisi] Membandingkan bilangan  
> Membandingkan bilangan berarti menentukan hubungan $<$, $>$, atau $=$ antara dua bilangan.

Jika $a>1$ dan $m>n$, maka:

$$  
a^m>a^n  
$$

Alasannya, mengalikan lagi dengan faktor $a>1$ memperbesar nilai.

Jika $0<a<1$ dan $m>n$, maka:

$$  
a^m<a^n  
$$

Alasannya, mengalikan dengan bilangan positif kurang dari $1$ memperkecil nilai.

Contoh:

$$  
2^5>2^3  
$$

karena basis $2>1$.

Namun:

$$  
\left(\frac{1}{2}\right)^5<\left(\frac{1}{2}\right)^3  
$$

karena basis $\frac{1}{2}$ berada di antara $0$ dan $1$.

Jika basis negatif, pola tanda ikut bergantung pada genap atau ganjilnya eksponen.

Contoh:

$$  
(-2)^4=16  
$$

$$  
(-2)^5=-32  
$$

Jadi membandingkan pangkat dengan basis negatif tidak cukup hanya melihat besar eksponen.

---

## 47. Membandingkan Bentuk Akar

Untuk $a,b\geq 0$:

$$  
\sqrt{a}<\sqrt{b}  
$$

jika dan hanya jika:

$$  
a<b  
$$

Alasannya, fungsi akar kuadrat utama meningkat pada bilangan tidak negatif. Artinya, radikan lebih besar menghasilkan akar utama lebih besar.

Contoh:

$$  
\sqrt{7}<\sqrt{10}  
$$

karena:

$$  
7<10  
$$

Untuk akar pangkat $n$ dengan $n$ genap:

$$  
\sqrt[n]{a}<\sqrt[n]{b}  
$$

jika dan hanya jika:

$$  
a<b  
$$

dengan $a,b\geq 0$.

Untuk akar pangkat ganjil:

$$  
\sqrt[n]{a}<\sqrt[n]{b}  
$$

jika dan hanya jika:

$$  
a<b  
$$

untuk semua $a,b\in\mathbb{R}$.

Alasannya, fungsi pangkat ganjil dan akar ganjil mempertahankan urutan bilangan real.

---

## 48. Persamaan Bentuk Pangkat

> [!definisi] Persamaan bentuk pangkat  
> Persamaan bentuk pangkat adalah persamaan yang memuat variabel pada basis, eksponen, atau keduanya dalam bentuk berpangkat.

Jika $a>0$ dan $a\neq 1$, maka:

$$  
a^x=a^y  
$$

berarti:

$$  
x=y  
$$

Alasannya, untuk $a>0$ dan $a\neq 1$, setiap eksponen menghasilkan satu nilai pangkat yang berbeda. Dengan kata lain, fungsi $a^x$ bersifat satu-ke-satu.

Untuk pangkat bilangan bulat:

Jika $n$ ganjil:

$$  
x^n=y^n  
$$

berarti:

$$  
x=y  
$$

Alasannya, pangkat ganjil mempertahankan tanda dan urutan.

Jika $n$ genap:

$$  
x^n=y^n  
$$

berarti:

$$  
|x|=|y|  
$$

atau:

$$  
x=y \quad \text{atau} \quad x=-y  
$$

Alasannya, pangkat genap menghilangkan perbedaan tanda.

Contoh:

$$  
x^2=9  
$$

berhubungan dengan:

$$  
x=3 \quad \text{atau} \quad x=-3  
$$

karena:

$$  
3^2=9  
$$

dan:

$$  
(-3)^2=9  
$$

---

## 49. Persamaan Bentuk Akar

> [!definisi] Persamaan bentuk akar  
> Persamaan bentuk akar adalah persamaan yang memuat variabel di dalam tanda akar.

Bentuk akar genap menuntut radikan tidak negatif.

Contoh syarat bentuk:

$$  
\sqrt{x-2}  
$$

terdefinisi dalam bilangan real jika:

$$  
x-2\geq 0  
$$

sehingga:

$$  
x\geq 2  
$$

Untuk bentuk:

$$  
\frac{1}{\sqrt{x-2}}  
$$

syaratnya lebih ketat:

$$  
x-2>0  
$$

sehingga:

$$  
x>2  
$$

Alasannya, selain radikan harus tidak negatif, penyebut juga tidak boleh nol.

Jika kedua ruas persamaan dikuadratkan, kesetaraan baru perlu tetap berada pada syarat awal. Alasannya, operasi kuadrat dapat membuat dua bilangan berbeda tanda menjadi sama kuadratnya.

Contoh struktur:

$$  
a=b  
\Rightarrow  
a^2=b^2  
$$

Tetapi kebalikannya tidak selalu benar:

$$  
a^2=b^2  
\not\Rightarrow  
a=b  
$$

karena bisa saja:

$$  
a=-b  
$$

Itulah sebabnya syarat domain dan sifat akar utama menjadi bagian dari materi, bukan aksesori dekoratif seperti grafik tiga dimensi yang tidak diminta siapa pun.

---

## 50. Domain Bentuk Pangkat dan Akar

> [!definisi] Domain  
> Domain adalah himpunan semua nilai yang membuat suatu bentuk matematika terdefinisi.

Untuk bentuk pangkat:

$$  
x^{-n}  
$$

syaratnya:

$$  
x\neq 0  
$$

karena:

$$  
x^{-n}=\frac{1}{x^n}  
$$

Untuk bentuk akar genap:

$$  
\sqrt[2n]{A}  
$$

syaratnya:

$$  
A\geq 0  
$$

karena akar genap dari bilangan negatif tidak bernilai real.

Untuk bentuk akar ganjil:

$$  
\sqrt[2n+1]{A}  
$$

tidak ada syarat tanda pada $A$ dalam bilangan real.

Untuk bentuk pecahan:

$$  
\frac{A}{B}  
$$

syaratnya:

$$  
B\neq 0  
$$

Jika suatu bentuk memuat beberapa syarat, semua syarat harus dipenuhi sekaligus.

Contoh bentuk:

$$  
\frac{\sqrt{x+1}}{x-3}  
$$

Syarat dari akar:

$$  
x+1\geq 0  
$$

Syarat dari penyebut:

$$  
x-3\neq 0  
$$

Maka domainnya:

$$  
x\geq -1,\quad x\neq 3  
$$

---

## 51. Bentuk Akar Bertingkat

> [!definisi] Akar bertingkat  
> Akar bertingkat adalah bentuk akar yang di dalam radikannya masih terdapat bentuk akar lain.

Contoh:

$$  
\sqrt{5+2\sqrt{6}}  
$$

Beberapa akar bertingkat dapat disederhanakan menjadi jumlah atau selisih akar.

Dasarnya adalah identitas:

$$  
(\sqrt{m}+\sqrt{n})^2=m+n+2\sqrt{mn}  
$$

Maka:

$$  
\sqrt{m+n+2\sqrt{mn}}=\sqrt{m}+\sqrt{n}  
$$

dengan $m,n\geq 0$.

Alasannya, ruas kanan bernilai tidak negatif dan kuadratnya sama dengan radikan ruas kiri.

Contoh bentuk:

# $$  
\sqrt{5+2\sqrt{6}}

\sqrt{3}+\sqrt{2}  
$$

karena:

# $$  
(\sqrt{3}+\sqrt{2})^2

# 3+2+2\sqrt{6}

5+2\sqrt{6}  
$$

Untuk bentuk selisih:

$$  
(\sqrt{m}-\sqrt{n})^2=m+n-2\sqrt{mn}  
$$

Jika $\sqrt{m}\geq \sqrt{n}$, maka:

$$  
\sqrt{m+n-2\sqrt{mn}}=\sqrt{m}-\sqrt{n}  
$$

Syarat $\sqrt{m}\geq \sqrt{n}$ diperlukan karena akar utama harus bernilai tidak negatif.

---

## 52. Identitas Penting yang Berkaitan dengan Pangkat dan Akar

### 52.1 Kuadrat Jumlah

$$  
(a+b)^2=a^2+2ab+b^2  
$$

Alasannya:

$$  
(a+b)^2=(a+b)(a+b)  
$$

$$  
=a^2+ab+ab+b^2  
$$

$$  
=a^2+2ab+b^2  
$$

Identitas ini sering muncul ketika bentuk akar dijumlahkan lalu dikuadratkan.

### 52.2 Kuadrat Selisih

$$  
(a-b)^2=a^2-2ab+b^2  
$$

Alasannya:

$$  
(a-b)^2=(a-b)(a-b)  
$$

$$  
=a^2-ab-ab+b^2  
$$

$$  
=a^2-2ab+b^2  
$$

### 52.3 Selisih Kuadrat

$$  
a^2-b^2=(a-b)(a+b)  
$$

Alasannya:

$$  
(a-b)(a+b)=a^2+ab-ab-b^2=a^2-b^2  
$$

Identitas ini menjadi dasar bentuk sekawan dalam merasionalkan penyebut.

### 52.4 Jumlah Kubus

$$  
a^3+b^3=(a+b)(a^2-ab+b^2)  
$$

Alasannya:

# $$  
(a+b)(a^2-ab+b^2)

# a^3-a^2b+ab^2+a^2b-ab^2+b^3

a^3+b^3  
$$

### 52.5 Selisih Kubus

$$  
a^3-b^3=(a-b)(a^2+ab+b^2)  
$$

Alasannya:

# $$  
(a-b)(a^2+ab+b^2)

# a^3+a^2b+ab^2-a^2b-ab^2-b^3

a^3-b^3  
$$

Identitas kubus berkaitan dengan akar pangkat tiga dan penyederhanaan bentuk yang melibatkan pangkat tiga.

---

## 53. Bentuk Akar dalam Pecahan Aljabar

Jika bentuk akar muncul bersama variabel, syarat domain harus tetap diperhatikan.

Contoh bentuk:

$$  
\frac{\sqrt{x}}{\sqrt{x}+1}  
$$

Syarat:

$$  
x\geq 0  
$$

Penyebut:

$$  
\sqrt{x}+1  
$$

selalu lebih dari atau sama dengan $1$ karena $\sqrt{x}\geq 0$, sehingga tidak pernah nol.

Contoh bentuk lain:

$$  
\frac{1}{\sqrt{x}-2}  
$$

Syarat akar:

$$  
x\geq 0  
$$

Syarat penyebut:

$$  
\sqrt{x}-2\neq 0  
$$

Maka:

$$  
\sqrt{x}\neq 2  
$$

sehingga:

$$  
x\neq 4  
$$

Domainnya:

$$  
x\geq 0,\quad x\neq 4  
$$

---

## 54. Rasionalisasi Pecahan Aljabar Berakar

Contoh bentuk umum:

$$  
\frac{1}{\sqrt{x}+a}  
$$

Sekawannya:

$$  
\sqrt{x}-a  
$$

Maka:

# $$  
\frac{1}{\sqrt{x}+a}  
\cdot  
\frac{\sqrt{x}-a}{\sqrt{x}-a}

\frac{\sqrt{x}-a}{x-a^2}  
$$

Syarat:

$$  
x\geq 0  
$$

dan:

$$  
\sqrt{x}+a\neq 0  
$$

Penyebut akhir $x-a^2$ dapat bernilai nol saat $x=a^2$, sehingga nilai itu harus sesuai dengan syarat penyebut awal.

Alasannya, rasionalisasi tidak boleh memperkenalkan pembagian dengan nol.

---

## 55. Pangkat dan Akar pada Bilangan Negatif

Untuk bilangan negatif, pangkat bilangan bulat selalu terdefinisi.

Contoh:

$$  
(-a)^n  
$$

terdefinisi untuk semua $a\in\mathbb{R}$ dan $n\in\mathbb{N}^+$.

Jika $n$ genap:

$$  
(-a)^n=a^n  
$$

Alasannya, jumlah faktor negatif genap menghasilkan positif.

Jika $n$ ganjil:

$$  
(-a)^n=-a^n  
$$

Alasannya, jumlah faktor negatif ganjil menyisakan tanda negatif.

Untuk akar:

- Akar genap dari bilangan negatif tidak terdefinisi dalam bilangan real.
    
- Akar ganjil dari bilangan negatif terdefinisi dalam bilangan real.
    

Contoh:

$$  
\sqrt{-4}  
$$

tidak bernilai real.

Tetapi:

$$  
\sqrt[3]{-8}=-2  
$$

---

## 56. Ketunggalan Akar Utama

> [!definisi] Tunggal  
> Suatu nilai disebut tunggal jika hanya ada satu nilai yang dipilih atau memenuhi definisi tertentu.

Untuk $a\geq 0$, nilai $\sqrt{a}$ tunggal.

Walaupun persamaan:

$$  
x^2=a  
$$

dapat memiliki dua solusi, yaitu:

$$  
x=\sqrt{a}  
$$

dan:

$$  
x=-\sqrt{a}  
$$

simbol:

$$  
\sqrt{a}  
$$

sendiri hanya menyatakan akar utama yang tidak negatif.

Contoh:

$$  
x^2=25  
$$

memiliki dua nilai $x$:

$$  
x=5\quad \text{atau}\quad x=-5  
$$

Tetapi:

$$  
\sqrt{25}=5  
$$

bukan $\pm 5$.

Alasan perbedaan ini adalah bahwa $\sqrt{25}$ adalah ekspresi akar utama, sedangkan $x^2=25$ adalah persamaan yang mencari semua nilai $x$ yang memenuhi.

---

## 57. Bentuk $\pm\sqrt{a}$

Simbol:

$$  
\pm\sqrt{a}  
$$

berarti dua nilai:

$$  
\sqrt{a}  
$$

dan:

$$  
-\sqrt{a}  
$$

Simbol ini biasanya muncul ketika menyatakan semua bilangan yang kuadratnya sama dengan $a$.

Jika $a>0$, maka:

$$  
x^2=a  
$$

memiliki penyelesaian:

$$  
x=\pm\sqrt{a}  
$$

Jika $a=0$, maka:

$$  
x^2=0  
$$

hanya memiliki:

$$  
x=0  
$$

Walaupun dapat ditulis $x=\pm\sqrt{0}$, kedua tandanya menghasilkan nilai yang sama, yaitu $0$.

---

## 58. Bentuk Akar dan Nilai Mutlak pada Penyederhanaan

Jika tidak ada informasi tanda variabel, akar genap dari kuadrat harus memakai nilai mutlak.

$$  
\sqrt{x^2}=|x|  
$$

$$  
\sqrt{(x-3)^2}=|x-3|  
$$

Alasannya, $x-3$ dapat bernilai positif, nol, atau negatif, tetapi akar kuadrat utama harus tidak negatif.

Jika diketahui:

$$  
x\geq 3  
$$

maka:

$$  
|x-3|=x-3  
$$

Jika diketahui:

$$  
x<3  
$$

maka:

$$  
|x-3|=3-x  
$$

Bentuk nilai mutlak menyimpan informasi tanda yang belum diketahui.

---

## 59. Bentuk Akar yang Senilai tetapi Berbeda Bentuk

Dua bentuk akar dapat terlihat berbeda tetapi memiliki nilai sama.

Contoh:

$$  
\sqrt{8}=2\sqrt{2}  
$$

Alasannya:

$$  
\sqrt{8}=\sqrt{4\cdot 2}=\sqrt{4}\sqrt{2}=2\sqrt{2}  
$$

Contoh lain:

$$  
\sqrt{50}=5\sqrt{2}  
$$

karena:

$$  
50=25\cdot 2  
$$

dan:

$$  
\sqrt{25}=5  
$$

Bentuk sederhana biasanya dipilih karena radikan dibuat sekecil mungkin tanpa faktor kuadrat sempurna yang masih tersisa.

---

## 60. Bentuk Akar dan Perkalian Suku Dua

Jika bentuk akar berada dalam suku dua, perkalian mengikuti sifat distributif.

> [!definisi] Sifat distributif  
> Sifat distributif menyatakan bahwa:  
> $$  
> a(b+c)=ab+ac  
> $$

Contoh bentuk:

# $$  
\sqrt{2}(3+\sqrt{5})

3\sqrt{2}+\sqrt{10}  
$$

Alasannya:

$$  
\sqrt{2}\cdot 3=3\sqrt{2}  
$$

dan:

$$  
\sqrt{2}\cdot\sqrt{5}=\sqrt{10}  
$$

Contoh bentuk lain:

$$  
(\sqrt{3}+2)(\sqrt{3}-5)  
$$

Dengan sifat distributif:

$$  
(\sqrt{3})(\sqrt{3})+(\sqrt{3})(-5)+2(\sqrt{3})+2(-5)  
$$

Hasilnya:

# $$  
3-5\sqrt{3}+2\sqrt{3}-10

-7-3\sqrt{3}  
$$

---

## 61. Bentuk Akar dalam Identitas Kuadrat

Bentuk akar sering muncul dalam identitas kuadrat.

Jika:

$$  
a=\sqrt{m}  
$$

dan:

$$  
b=\sqrt{n}  
$$

maka:

# $$  
(\sqrt{m}+\sqrt{n})^2

m+2\sqrt{mn}+n  
$$

Alasannya:

$$  
(a+b)^2=a^2+2ab+b^2  
$$

dengan:

$$  
a^2=m,\quad b^2=n,\quad ab=\sqrt{mn}  
$$

Contoh bentuk:

# $$  
(\sqrt{2}+\sqrt{3})^2

# 2+2\sqrt{6}+3

5+2\sqrt{6}  
$$

Untuk selisih:

# $$  
(\sqrt{m}-\sqrt{n})^2

m-2\sqrt{mn}+n  
$$

Contoh:

# $$  
(\sqrt{5}-\sqrt{2})^2

# 5-2\sqrt{10}+2

7-2\sqrt{10}  
$$

---

## 62. Bentuk Akar dan Urutan Operasi

Urutan operasi dalam ekspresi berpangkat dan berakar:

1. Tanda kurung.
    
2. Pangkat dan akar.
    
3. Perkalian dan pembagian.
    
4. Penjumlahan dan pengurangan.
    

Akar diperlakukan seperti pangkat pecahan, sehingga berada pada tingkat operasi pangkat.

Contoh perbedaan:

$$  
\sqrt{a+b}  
$$

tidak sama dengan:

$$  
\sqrt{a}+\sqrt{b}  
$$

secara umum.

Alasannya:

$$  
(\sqrt{a}+\sqrt{b})^2=a+b+2\sqrt{ab}  
$$

sedangkan:

$$  
(\sqrt{a+b})^2=a+b  
$$

Keduanya hanya sama dalam keadaan khusus, misalnya ketika $ab=0$ dan $a,b\geq 0$.

Begitu pula:

$$  
(a+b)^2  
$$

tidak sama dengan:

$$  
a^2+b^2  
$$

secara umum, karena:

$$  
(a+b)^2=a^2+2ab+b^2  
$$

---

## 63. Bentuk Pangkat dengan Eksponen Nol pada Ekspresi

Jika $A$ adalah suatu ekspresi, maka:

$$  
A^0=1  
$$

dengan syarat:

$$  
A\neq 0  
$$

Contoh:

$$  
(x-2)^0=1  
$$

dengan syarat:

$$  
x-2\neq 0  
$$

yaitu:

$$  
x\neq 2  
$$

Alasannya, jika $x=2$, maka bentuk menjadi:

$$  
0^0  
$$

yang tidak didefinisikan.

---

## 64. Bentuk Pangkat Negatif pada Ekspresi

Jika $A$ adalah ekspresi dan $n\in\mathbb{N}^+$, maka:

$$  
A^{-n}=\frac{1}{A^n}  
$$

dengan syarat:

$$  
A\neq 0  
$$

Contoh:

$$  
(x+1)^{-2}=\frac{1}{(x+1)^2}  
$$

dengan syarat:

$$  
x+1\neq 0  
$$

yaitu:

$$  
x\neq -1  
$$

Alasannya, pangkat negatif menghasilkan kebalikan, sehingga basis tidak boleh nol.

---

## 65. Bentuk Pangkat Pecahan pada Ekspresi

Jika:

$$  
A^{\frac{1}{2}}  
$$

maka:

$$  
A^{\frac{1}{2}}=\sqrt{A}  
$$

Syarat realnya:

$$  
A\geq 0  
$$

Jika:

$$  
A^{-\frac{1}{2}}  
$$

maka:

$$  
A^{-\frac{1}{2}}=\frac{1}{\sqrt{A}}  
$$

Syarat realnya:

$$  
A>0  
$$

Alasannya, $A$ harus membuat akar kuadrat terdefinisi dan penyebut tidak boleh nol.

Contoh:

$$  
(x-4)^{\frac{1}{2}}=\sqrt{x-4}  
$$

dengan syarat:

$$  
x\geq 4  
$$

Sedangkan:

$$  
(x-4)^{-\frac{1}{2}}=\frac{1}{\sqrt{x-4}}  
$$

dengan syarat:

$$  
x>4  
$$

---

## 66. Akar sebagai Invers Pangkat

> [!definisi] Fungsi invers  
> Fungsi invers adalah fungsi yang membalikkan hubungan input dan output dari fungsi asal.

Untuk $x\geq 0$, fungsi:

$$  
f(x)=x^2  
$$

memiliki invers:

$$  
f^{-1}(x)=\sqrt{x}  
$$

Pembatasan $x\geq 0$ diperlukan karena fungsi $x^2$ pada seluruh bilangan real tidak satu-ke-satu.

Contoh:

$$  
2^2=4  
$$

dan:

$$  
(-2)^2=4  
$$

Dua input berbeda menghasilkan output sama, sehingga tidak dapat langsung dibalik menjadi satu nilai.

Dengan membatasi domain ke $x\geq 0$, setiap output memiliki satu input, sehingga inversnya adalah akar utama.

Untuk pangkat ganjil:

$$  
f(x)=x^3  
$$

memiliki invers:

$$  
f^{-1}(x)=\sqrt[3]{x}  
$$

pada seluruh bilangan real karena fungsi pangkat tiga satu-ke-satu.

---

## 67. Eksponen Rasional dan Penyederhanaan Aljabar

Untuk $a>0$, bentuk berpangkat rasional dapat disederhanakan memakai aturan eksponen.

Contoh bentuk:

$$  
a^{\frac{2}{3}}a^{\frac{5}{3}}=a^{\frac{7}{3}}  
$$

Alasannya:

$$  
\frac{2}{3}+\frac{5}{3}=\frac{7}{3}  
$$

Bentuk:

$$  
a^{\frac{7}{3}}  
$$

dapat ditulis:

$$  
a^2\sqrt[3]{a}  
$$

karena:

$$  
\frac{7}{3}=2+\frac{1}{3}  
$$

Sehingga:

$$  
a^{\frac{7}{3}}=a^2a^{\frac{1}{3}}=a^2\sqrt[3]{a}  
$$

Contoh lain:

$$  
\frac{x^{\frac{5}{2}}}{x^{\frac{1}{2}}}=x^2  
$$

dengan $x>0$.

Alasannya:

$$  
\frac{5}{2}-\frac{1}{2}=2  
$$

---

## 68. Eksponen Rasional Negatif

Jika $a>0$ dan $r\in\mathbb{Q}$, maka:

$$  
a^{-r}=\frac{1}{a^r}  
$$

Contoh:

$$  
x^{-\frac{3}{2}}=\frac{1}{x^{\frac{3}{2}}}  
$$

dan:

$$  
x^{\frac{3}{2}}=x\sqrt{x}  
$$

Maka:

$$  
x^{-\frac{3}{2}}=\frac{1}{x\sqrt{x}}  
$$

dengan $x>0$.

Alasannya:

$$  
x^{\frac{3}{2}}=x^{1+\frac{1}{2}}=x\cdot x^{\frac{1}{2}}=x\sqrt{x}  
$$

Bentuk penyebut dapat dirasionalkan:

# $$  
\frac{1}{x\sqrt{x}}

\frac{\sqrt{x}}{x^2}  
$$

karena:

$$  
x\sqrt{x}\cdot\sqrt{x}=x^2  
$$

---

## 69. Pangkat Nol pada Pangkat Rasional

Untuk $a>0$:

$$  
a^0=1  
$$

Jika suatu ekspresi berpangkat rasional menghasilkan eksponen total nol, hasilnya $1$ selama basisnya tidak nol.

Contoh:

$$  
x^{\frac{2}{3}}x^{-\frac{2}{3}}=x^0=1  
$$

dengan $x>0$.

Syarat $x>0$ menjaga pangkat rasional tetap terdefinisi tanpa ambiguitas.

---

## 70. Relasi Antara Pangkat dan Faktorisasi

Jika:

$$  
a^m=a^n  
$$

dengan $a>0$ dan $a\neq 1$, maka:

$$  
m=n  
$$

Alasannya, pangkat dengan basis positif selain $1$ menghasilkan nilai berbeda untuk eksponen berbeda.

Namun jika $a=1$:

$$  
1^m=1^n  
$$

untuk semua $m,n$.

Jika $a=0$, bentuk $0^m$ perlu memperhatikan apakah eksponen positif, nol, atau negatif.

Jika $a=-1$, nilai bergantung pada genap atau ganjilnya eksponen.

Contoh:

$$  
(-1)^2=1  
$$

$$  
(-1)^4=1  
$$

Eksponen berbeda dapat menghasilkan nilai sama karena pola tanda berulang.

---

## 71. Bentuk Pangkat dalam Faktorisasi Aljabar

Pangkat digunakan untuk menulis faktor berulang secara ringkas.

Contoh:

$$  
x^2-9  
$$

dapat ditulis:

$$  
x^2-3^2  
$$

Karena ini selisih kuadrat:

$$  
x^2-9=(x-3)(x+3)  
$$

Contoh:

$$  
x^3-8  
$$

dapat ditulis:

$$  
x^3-2^3  
$$

Karena ini selisih kubus:

$$  
x^3-8=(x-2)(x^2+2x+4)  
$$

Alasannya mengikuti identitas:

$$  
a^3-b^3=(a-b)(a^2+ab+b^2)  
$$

Bentuk akar dapat muncul setelah faktorisasi jika suatu persamaan atau ekspresi melibatkan akar dari faktor tersebut.

---

## 72. Koefisien pada Bentuk Akar

> [!definisi] Koefisien bentuk akar  
> Koefisien bentuk akar adalah faktor di luar tanda akar.

Pada bentuk:

$$  
5\sqrt{3}  
$$

koefisiennya adalah $5$, dan bagian akarnya adalah $\sqrt{3}$.

Pada bentuk:

$$  
-\frac{2}{3}\sqrt{7}  
$$

koefisiennya adalah:

$$  
-\frac{2}{3}  
$$

Jika koefisien tidak ditulis, koefisiennya dianggap $1$.

$$  
\sqrt{5}=1\sqrt{5}  
$$

Jika tanda negatif berada di depan akar:

$$  
-\sqrt{5}=-1\sqrt{5}  
$$

Koefisien memungkinkan bentuk akar sejenis dijumlahkan seperti bentuk aljabar biasa.

---

## 73. Bentuk Akar Sejenis dan Tidak Sejenis

Bentuk akar sejenis harus memiliki:

1. Indeks akar yang sama.
    
2. Radikan yang sama setelah disederhanakan.
    

Contoh sejenis:

$$  
3\sqrt{2},\quad -7\sqrt{2},\quad \frac{1}{2}\sqrt{2}  
$$

Contoh tidak sejenis:

$$  
\sqrt{2}  
\quad \text{dan} \quad  
\sqrt{3}  
$$

karena radikannya berbeda.

Contoh lain:

$$  
\sqrt{2}  
\quad \text{dan} \quad  
\sqrt[3]{2}  
$$

tidak sejenis karena indeks akarnya berbeda.

Bentuk:

$$  
\sqrt{8}  
$$

dan:

$$  
\sqrt{2}  
$$

menjadi sejenis setelah penyederhanaan karena:

$$  
\sqrt{8}=2\sqrt{2}  
$$

---

## 74. Perkalian Bentuk Akar Berkoefisien

Jika $a,b$ adalah koefisien dan bentuk akar terdefinisi, maka:

$$  
(a\sqrt{m})(b\sqrt{n})=ab\sqrt{mn}  
$$

dengan $m,n\geq 0$.

Alasannya:

# $$  
(a\sqrt{m})(b\sqrt{n})

# ab(\sqrt{m}\sqrt{n})

ab\sqrt{mn}  
$$

Contoh:

$$  
(3\sqrt{2})(5\sqrt{7})=15\sqrt{14}  
$$

Jika radikan hasil masih dapat disederhanakan, bentuknya dapat diubah lagi.

Contoh:

# $$  
(2\sqrt{6})(3\sqrt{12})

# 6\sqrt{72}

# 6\cdot 6\sqrt{2}

36\sqrt{2}  
$$

---

## 75. Pembagian Bentuk Akar Berkoefisien

Jika $b\neq 0$, $n>0$, dan bentuk akar terdefinisi:

# $$  
\frac{a\sqrt{m}}{b\sqrt{n}}

\frac{a}{b}\sqrt{\frac{m}{n}}  
$$

dengan $m\geq 0$ dan $n>0$.

Contoh:

# $$  
\frac{6\sqrt{10}}{3\sqrt{2}}

2\sqrt{5}  
$$

Alasannya:

$$  
\frac{\sqrt{10}}{\sqrt{2}}=\sqrt{\frac{10}{2}}=\sqrt{5}  
$$

Jika penyebut masih memuat akar, bentuk dapat dirasionalkan.

Contoh:

# $$  
\frac{2}{3\sqrt{5}}

\frac{2\sqrt{5}}{15}  
$$

karena penyebut dikalikan dengan $\sqrt{5}$.

---

## 76. Bentuk Akar dan Eksponen dalam Satu Radikan

Jika radikan mengandung pangkat, sebagian faktor dapat keluar dari akar.

Untuk akar kuadrat:

# $$  
\sqrt{x^5}

# \sqrt{x^4\cdot x}

\sqrt{(x^2)^2\cdot x}  
$$

Jika $x\geq 0$:

$$  
\sqrt{x^5}=x^2\sqrt{x}  
$$

Jika tidak ada informasi $x\geq 0$, syarat real untuk $\sqrt{x^5}$ adalah:

$$  
x^5\geq 0  
$$

yang berarti:

$$  
x\geq 0  
$$

Jadi dalam kasus ini tetap:

$$  
\sqrt{x^5}=x^2\sqrt{x}  
$$

Untuk bentuk:

$$  
\sqrt{x^6}  
$$

hasilnya:

$$  
|x^3|  
$$

karena:

$$  
x^6=(x^3)^2  
$$

dan:

$$  
\sqrt{(x^3)^2}=|x^3|  
$$

---

## 77. Bentuk Akar Pecahan

Untuk $a\geq 0$ dan $b>0$:

$$  
\sqrt{\frac{a}{b}}=\frac{\sqrt{a}}{\sqrt{b}}  
$$

Jika penyebut memuat akar, bentuk dapat dirasionalkan.

Contoh:

# $$  
\sqrt{\frac{3}{5}}

# \frac{\sqrt{3}}{\sqrt{5}}

\frac{\sqrt{15}}{5}  
$$

Alasannya:

# $$  
\frac{\sqrt{3}}{\sqrt{5}}\cdot\frac{\sqrt{5}}{\sqrt{5}}

\frac{\sqrt{15}}{5}  
$$

Untuk akar pangkat $n$:

Jika $n$ genap:

$$  
\sqrt[n]{\frac{a}{b}}=\frac{\sqrt[n]{a}}{\sqrt[n]{b}}  
$$

dengan $a\geq 0$ dan $b>0$.

Jika $n$ ganjil:

$$  
\sqrt[n]{\frac{a}{b}}=\frac{\sqrt[n]{a}}{\sqrt[n]{b}}  
$$

dengan $b\neq 0$.

---

## 78. Bilangan Berpangkat dan Skala Nilai

Jika $|a|>1$, nilai $|a|^n$ membesar ketika $n$ bertambah.

Jika $0<|a|<1$, nilai $|a|^n$ mengecil ketika $n$ bertambah.

Alasannya:

- Mengalikan dengan bilangan yang nilai mutlaknya lebih dari $1$ memperbesar nilai mutlak.
    
- Mengalikan dengan bilangan yang nilai mutlaknya kurang dari $1$ memperkecil nilai mutlak.
    

Contoh:

$$  
3^1<3^2<3^3  
$$

karena:

$$  
3<9<27  
$$

Tetapi:

$$  
\left(\frac{1}{3}\right)^1>  
\left(\frac{1}{3}\right)^2>  
\left(\frac{1}{3}\right)^3  
$$

karena:

$$  
\frac{1}{3}>\frac{1}{9}>\frac{1}{27}  
$$

---

## 79. Bentuk Pangkat dengan Eksponen Genap dan Ganjil pada Pertidaksamaan

Jika $n$ ganjil, maka:

$$  
a<b \Rightarrow a^n<b^n  
$$

untuk semua $a,b\in\mathbb{R}$.

Alasannya, fungsi pangkat ganjil meningkat pada seluruh bilangan real.

Jika $n$ genap, pernyataan:

$$  
a<b \Rightarrow a^n<b^n  
$$

tidak selalu benar pada seluruh bilangan real.

Contoh:

$$  
-3<2  
$$

tetapi:

$$  
(-3)^2=9>4=2^2  
$$

Untuk pangkat genap, nilai mutlak lebih menentukan:

$$  
a^2<b^2  
$$

jika dan hanya jika:

$$  
|a|<|b|  
$$

Alasannya, kuadrat mengubah bilangan menjadi ukuran jaraknya dari nol dalam bentuk positif.

---

## 80. Bentuk Eksponen dan Akar dalam Himpunan Real

Dalam catatan ini, pembahasan dilakukan pada bilangan real.

Konsekuensinya:

$$  
\sqrt{-1}  
$$

tidak mempunyai nilai real.

$$  
\sqrt[4]{-16}  
$$

tidak mempunyai nilai real.

Namun:

$$  
\sqrt[3]{-1}=-1  
$$

dan:

$$  
\sqrt[5]{-32}=-2  
$$

mempunyai nilai real.

Alasannya, akar berindeks ganjil dapat menerima radikan negatif, sedangkan akar berindeks genap tidak dapat menerima radikan negatif dalam bilangan real.

---

## 81. Bentuk Pangkat yang Tidak Terdefinisi

Beberapa bentuk tidak terdefinisi dalam aritmetika real dasar:

$$  
\frac{1}{0}  
$$

tidak terdefinisi karena tidak ada bilangan real yang jika dikalikan $0$ menghasilkan $1$.

$$  
0^0  
$$

tidak didefinisikan karena pola pangkat nol dan pola pangkat basis nol memberi tuntutan yang tidak konsisten.

$$  
0^{-n}  
$$

tidak terdefinisi karena:

$$  
0^{-n}=\frac{1}{0^n}=\frac{1}{0}  
$$

$$  
\sqrt[2n]{a}  
$$

tidak bernilai real jika:

$$  
a<0  
$$

Alasannya, pangkat genap bilangan real tidak pernah negatif.

---

## 82. Bentuk Pangkat dan Akar yang Ekuivalen

Beberapa bentuk ekuivalen penting:

$$  
\sqrt{a}=a^{\frac{1}{2}}  
$$

$$  
\sqrt[3]{a}=a^{\frac{1}{3}}  
$$

$$  
\sqrt[n]{a^m}=a^{\frac{m}{n}}  
$$

untuk $a\geq 0$ dalam konteks akar genap.

$$  
a^{-n}=\frac{1}{a^n}  
$$

$$  
\frac{1}{a^{-n}}=a^n  
$$

$$  
\left(\frac{a}{b}\right)^{-n}=\left(\frac{b}{a}\right)^n  
$$

dengan $a\neq 0$ dan $b\neq 0$.

Setiap kesetaraan di atas membutuhkan syarat karena operasi pangkat, akar, dan pembagian tidak selalu terdefinisi untuk semua bilangan real.

---

## 83. Struktur Umum Penyederhanaan Bentuk Akar

Penyederhanaan bentuk akar bertujuan mengubah bentuk menjadi ekuivalen dengan bagian akar yang lebih sederhana.

Untuk akar kuadrat:

$$  
\sqrt{a}  
$$

dicari bentuk:

$$  
k\sqrt{b}  
$$

dengan $k$ rasional dan $b$ tidak memuat faktor kuadrat sempurna selain $1$.

Untuk akar pangkat tiga:

$$  
\sqrt[3]{a}  
$$

dicari bentuk:

$$  
k\sqrt[3]{b}  
$$

dengan $b$ tidak memuat faktor pangkat tiga sempurna selain $1$.

Untuk akar indeks $n$:

$$  
\sqrt[n]{a}  
$$

dicari bentuk:

$$  
k\sqrt[n]{b}  
$$

dengan $b$ tidak memuat faktor pangkat-$n$ sempurna selain $1$.

Alasannya, faktor pangkat-$n$ sempurna dapat keluar dari akar sebagai bilangan biasa.

---

## 84. Hubungan Bentuk Akar dengan Perkalian Faktor

Jika:

$$  
a=b\cdot c  
$$

maka untuk akar kuadrat dengan $b,c\geq 0$:

$$  
\sqrt{a}=\sqrt{bc}=\sqrt{b}\sqrt{c}  
$$

Namun pemecahan seperti ini memerlukan syarat radikan tidak negatif.

Untuk bilangan negatif, bentuk:

$$  
\sqrt{(-4)(-9)}  
$$

bernilai:

$$  
\sqrt{36}=6  
$$

Tetapi:

$$  
\sqrt{-4}\sqrt{-9}  
$$

tidak bernilai real.

Jadi aturan:

$$  
\sqrt{bc}=\sqrt{b}\sqrt{c}  
$$

tidak dapat digunakan sembarangan jika $b$ atau $c$ negatif dalam bilangan real. Matematika, secara mengejutkan, tidak menghargai keberanian tanpa syarat domain.

---

## 85. Hubungan Bentuk Akar dengan Pembagian Faktor

Jika $a\geq 0$ dan $b>0$, maka:

$$  
\sqrt{\frac{a}{b}}=\frac{\sqrt{a}}{\sqrt{b}}  
$$

Syarat $b>0$ memastikan:

1. Pecahan $\frac{a}{b}$ terdefinisi.
    
2. Akar $\sqrt{b}$ terdefinisi.
    
3. Penyebut $\sqrt{b}$ tidak nol.
    

Jika $b=0$, bentuk pecahan tidak terdefinisi.

Jika $b<0$, akar $\sqrt{b}$ tidak bernilai real.

---

## 86. Akar dari Hasil Kali Kuadrat

Jika $a,b\in\mathbb{R}$, maka:

$$  
\sqrt{a^2b^2}=|ab|  
$$

Alasannya:

$$  
a^2b^2=(ab)^2  
$$

dan:

$$  
\sqrt{(ab)^2}=|ab|  
$$

Jika diketahui $ab\geq 0$, maka:

$$  
|ab|=ab  
$$

Jika diketahui $ab<0$, maka:

$$  
|ab|=-ab  
$$

Untuk bentuk:

$$  
\sqrt{a^2b}  
$$

penyederhanaannya:

$$  
|a|\sqrt{b}  
$$

dengan syarat:

$$  
b\geq 0  
$$

Alasannya:

$$  
\sqrt{a^2b}=\sqrt{a^2}\sqrt{b}=|a|\sqrt{b}  
$$

---

## 87. Akar dari Pecahan Kuadrat

Untuk $b\neq 0$:

# $$  
\sqrt{\frac{a^2}{b^2}}

\left|\frac{a}{b}\right|  
$$

Alasannya:

$$  
\frac{a^2}{b^2}=\left(\frac{a}{b}\right)^2  
$$

dan akar kuadrat utama dari kuadrat suatu bilangan adalah nilai mutlak bilangan tersebut.

Jika diketahui:

$$  
\frac{a}{b}\geq 0  
$$

maka:

$$  
\sqrt{\frac{a^2}{b^2}}=\frac{a}{b}  
$$

Jika diketahui:

$$  
\frac{a}{b}<0  
$$

maka:

$$  
\sqrt{\frac{a^2}{b^2}}=-\frac{a}{b}  
$$

---

## 88. Bentuk Akar dan Pangkat Sempurna

Jika $a$ adalah pangkat sempurna ke-$n$, maka akar ke-$n$ dari $a$ adalah bilangan rasional atau bulat tertentu.

Contoh:

$$  
64=8^2  
$$

maka:

$$  
\sqrt{64}=8  
$$

$$  
64=4^3  
$$

maka:

$$  
\sqrt[3]{64}=4  
$$

$$  
64=2^6  
$$

maka:

$$  
\sqrt[6]{64}=2  
$$

Satu bilangan dapat menjadi pangkat sempurna untuk beberapa indeks berbeda. Alasannya, eksponen pada faktorisasi prima dapat memiliki beberapa pembagi.

Contoh:

$$  
64=2^6  
$$

Eksponen $6$ habis dibagi $2$, $3$, dan $6$, sehingga $64$ merupakan kuadrat sempurna, pangkat tiga sempurna, dan pangkat enam sempurna.

---

## 89. Bentuk Akar Tidak Sederhana karena Faktor Tersembunyi

Suatu radikan dapat tampak tidak memiliki faktor pangkat sempurna jika tidak difaktorkan.

Contoh:

$$  
\sqrt{98}  
$$

Karena:

$$  
98=49\cdot 2  
$$

dan $49$ adalah kuadrat sempurna, maka:

$$  
\sqrt{98}=7\sqrt{2}  
$$

Contoh akar pangkat tiga:

$$  
\sqrt[3]{192}  
$$

Karena:

$$  
192=64\cdot 3  
$$

dan $64$ adalah pangkat tiga sempurna, maka:

$$  
\sqrt[3]{192}=4\sqrt[3]{3}  
$$

Alasan faktorisasi penting adalah karena faktor pangkat sempurna dapat keluar dari tanda akar.

---

## 90. Pangkat sebagai Perkalian Berulang Tidak Berlaku untuk Semua Eksponen

Definisi awal:

$$  
a^n=\underbrace{a\cdot a\cdots a}_{n\text{ faktor}}  
$$

hanya berlaku langsung untuk $n\in\mathbb{N}^+$.

Untuk pangkat nol, negatif, dan pecahan, maknanya diperluas dengan definisi yang menjaga konsistensi aturan pangkat.

Pangkat nol:

$$  
a^0=1  
$$

untuk $a\neq 0$.

Pangkat negatif:

$$  
a^{-n}=\frac{1}{a^n}  
$$

untuk $a\neq 0$.

Pangkat pecahan:

$$  
a^{\frac{1}{n}}=\sqrt[n]{a}  
$$

dengan syarat sesuai indeks akar.

Alasannya, tidak masuk akal mengatakan “mengalikan $a$ sebanyak setengah kali” secara langsung dalam aritmetika dasar. Eksponen pecahan diberi makna melalui akar, bukan melalui jumlah faktor literal. Di titik ini bahasa sehari-hari memang menyerah, seperti biasanya.

---

## 91. Konsistensi Aturan Eksponen

Definisi pangkat nol, negatif, dan pecahan dipilih agar aturan berikut tetap konsisten:

$$  
a^m\cdot a^n=a^{m+n}  
$$

$$  
\frac{a^m}{a^n}=a^{m-n}  
$$

$$  
(a^m)^n=a^{mn}  
$$

Untuk pangkat nol:

$$  
a^m\cdot a^0=a^{m+0}=a^m  
$$

Agar benar, $a^0$ harus menjadi identitas perkalian, yaitu $1$.

Untuk pangkat negatif:

$$  
a^n\cdot a^{-n}=a^{n-n}=a^0=1  
$$

Agar benar:

$$  
a^{-n}=\frac{1}{a^n}  
$$

Untuk pangkat pecahan:

$$  
\left(a^{\frac{1}{n}}\right)^n=a^1=a  
$$

Agar benar, $a^{\frac{1}{n}}$ harus berarti akar ke-$n$ dari $a$.

---

## 92. Hubungan Bentuk Pangkat dengan Bentuk Standar Aljabar

Bentuk berpangkat membuat ekspresi aljabar lebih ringkas.

$$  
x\cdot x\cdot x\cdot x=x^4  
$$

$$  
(2x)(2x)(2x)=8x^3  
$$

Alasannya:

$$  
(2x)^3=2^3x^3=8x^3  
$$

Bentuk akar membuat pangkat pecahan lebih eksplisit.

$$  
x^{\frac{1}{2}}=\sqrt{x}  
$$

$$  
x^{\frac{3}{2}}=x\sqrt{x}  
$$

karena:

$$  
x^{\frac{3}{2}}=x^{1+\frac{1}{2}}=x\cdot x^{\frac{1}{2}}  
$$

dengan $x\geq 0$.

---

## 93. Perubahan Bentuk Tanpa Mengubah Nilai

Dalam aljabar, bentuk dapat diubah selama nilainya tetap sama dan syaratnya tidak berubah secara keliru.

Contoh perubahan sah:

$$  
\sqrt{20}=2\sqrt{5}  
$$

karena:

$$  
20=4\cdot 5  
$$

dan:

$$  
\sqrt{4}=2  
$$

Contoh perubahan sah:

$$  
x^{-2}=\frac{1}{x^2}  
$$

dengan $x\neq 0$.

Contoh perubahan yang tidak sah secara umum:

$$  
\sqrt{x^2}=x  
$$

karena yang benar adalah:

$$  
\sqrt{x^2}=|x|  
$$

Pernyataan $\sqrt{x^2}=x$ hanya sah jika diketahui $x\geq 0$.

Alasan utamanya adalah akar kuadrat utama selalu tidak negatif.

---

## 94. Struktur Lengkap Syarat pada Bentuk Gabungan

Jika suatu bentuk memuat pangkat negatif, akar genap, dan pecahan, syaratnya digabung.

Contoh bentuk:

$$  
\frac{x^{-2}}{\sqrt{x-1}}  
$$

Syarat dari $x^{-2}$:

$$  
x\neq 0  
$$

Syarat dari penyebut $\sqrt{x-1}$:

$$  
x-1>0  
$$

sehingga:

$$  
x>1  
$$

Jika $x>1$, otomatis $x\neq 0$.

Jadi domainnya:

$$  
x>1  
$$

Contoh bentuk lain:

$$  
\sqrt{\frac{x+2}{x-3}}  
$$

Syarat akar kuadrat:

$$  
\frac{x+2}{x-3}\geq 0  
$$

Syarat pecahan:

$$  
x-3\neq 0  
$$

yaitu:

$$  
x\neq 3  
$$

Bentuk ini menunjukkan bahwa syarat radikan tidak selalu sekadar “bagian dalam akar lebih dari nol”; jika bagian dalam berupa pecahan, seluruh pecahan sebagai radikan yang harus tidak negatif.

---

## 95. Hubungan Akar dan Kuadrat dalam Persamaan

Jika:

$$  
\sqrt{A}=B  
$$

maka harus berlaku:

$$  
B\geq 0  
$$

dan:

$$  
A=B^2  
$$

Syarat $B\geq 0$ diperlukan karena akar utama selalu tidak negatif.

Contoh struktur:

$$  
\sqrt{x}=x-2  
$$

Syarat dari akar:

$$  
x\geq 0  
$$

Syarat dari ruas kanan sebagai nilai akar:

$$  
x-2\geq 0  
$$

sehingga:

$$  
x\geq 2  
$$

Kemudian hubungan kuadrat:

$$  
x=(x-2)^2  
$$

Syarat nilai tetap bagian dari persamaan, bukan hiasan pinggir halaman.

---

## 96. Hubungan Akar Ganjil dan Pangkat Ganjil dalam Persamaan

Jika:

$$  
\sqrt[3]{A}=B  
$$

maka:

$$  
A=B^3  
$$

Tidak diperlukan syarat $B\geq 0$ karena akar pangkat tiga dapat bernilai negatif.

Contoh struktur:

$$  
\sqrt[3]{x-1}=2  
$$

setara dengan:

$$  
x-1=8  
$$

Alasannya:

$$  
2^3=8  
$$

Jika:

$$  
\sqrt[3]{A}=B  
$$

maka mengkubikkan kedua ruas tidak menimbulkan masalah tanda seperti pada akar kuadrat, karena fungsi pangkat tiga satu-ke-satu pada seluruh bilangan real.

---

## 97. Bentuk Pangkat, Akar, dan Nilai Absolut dalam Satu Identitas

Identitas penting:

$$  
\sqrt{x^2}=|x|  
$$

$$  
(\sqrt{x})^2=x,\quad x\geq 0  
$$

Kedua bentuk ini berbeda arah.

Pada:

$$  
(\sqrt{x})^2=x  
$$

akar dilakukan lebih dahulu. Karena $\sqrt{x}$ sudah tidak negatif, kuadratnya kembali menjadi $x$.

Pada:

$$  
\sqrt{x^2}=|x|  
$$

kuadrat dilakukan lebih dahulu. Informasi tanda $x$ hilang saat dikuadratkan, lalu akar utama mengambil nilai tidak negatif.

Contoh:

$$  
(\sqrt{9})^2=3^2=9  
$$

Tetapi:

$$  
\sqrt{(-9)^2}=\sqrt{81}=9  
$$

bukan $-9$.

---

## 98. Bentuk Umum Eksponen dengan Basis Positif

Untuk $a>0$, eksponen dapat diperluas dari bilangan bulat ke bilangan rasional dengan konsisten.

Jika:

$$  
r=\frac{m}{n}  
$$

dengan $m\in\mathbb{Z}$ dan $n\in\mathbb{N}^+$, maka:

$$  
a^r=a^{\frac{m}{n}}=\sqrt[n]{a^m}  
$$

Karena $a>0$, maka:

$$  
a^m>0  
$$

untuk semua $m\in\mathbb{Z}$, selama $a^m$ terdefinisi.

Jika $m<0$:

$$  
a^m=\frac{1}{a^{-m}}  
$$

tetap positif karena $a^{-m}>0$.

Alasan basis positif menjadi pilihan utama adalah karena akar genap dan akar ganjil tidak menimbulkan konflik tanda.

---

## 99. Bentuk Umum Eksponen dengan Basis Nol

Untuk basis nol:

$$  
0^n=0  
$$

jika $n\in\mathbb{N}^+$.

Untuk eksponen rasional positif:

$$  
0^{\frac{m}{n}}=0  
$$

jika $m>0$ dan bentuk akar yang muncul terdefinisi.

Contoh:

$$  
0^{\frac{3}{2}}=0  
$$

karena:

$$  
\sqrt{0^3}=0  
$$

Untuk eksponen nol:

$$  
0^0  
$$

tidak didefinisikan.

Untuk eksponen negatif:

$$  
0^{-r}  
$$

tidak didefinisikan karena menghasilkan pembagian dengan nol.

---

## 100. Bentuk Umum Eksponen dengan Basis Negatif

Untuk basis negatif dan eksponen bilangan bulat, bentuk selalu terdefinisi.

Contoh:

$$  
(-5)^3=-125  
$$

$$  
(-5)^4=625  
$$

Untuk eksponen rasional, bentuk dapat terdefinisi atau tidak dalam bilangan real tergantung penyebut eksponen setelah disederhanakan.

Jika penyebut eksponen dalam bentuk paling sederhana adalah ganjil, bentuk dapat bernilai real.

Contoh:

$$  
(-8)^{\frac{1}{3}}=-2  
$$

Jika penyebut eksponen dalam bentuk paling sederhana adalah genap, bentuk tidak bernilai real.

Contoh:

$$  
(-8)^{\frac{1}{2}}  
$$

tidak bernilai real.

Namun aturan umum eksponen seperti:

$$  
(a^r)^s=a^{rs}  
$$

tidak boleh digunakan sembarangan untuk basis negatif dan eksponen rasional.

Alasannya, perubahan bentuk pecahan eksponen dapat mengubah jenis akar yang muncul, terutama antara akar ganjil dan akar genap.

---

## 101. Batasan Operasi Akar terhadap Penjumlahan

Secara umum:

$$  
\sqrt{a+b}\neq \sqrt{a}+\sqrt{b}  
$$

Alasannya, jika keduanya sama, maka setelah dikuadratkan akan diperoleh:

$$  
a+b=a+b+2\sqrt{ab}  
$$

yang mengharuskan:

$$  
2\sqrt{ab}=0  
$$

atau:

$$  
ab=0  
$$

Jadi kesetaraan itu hanya terjadi pada keadaan khusus, bukan aturan umum.

Demikian pula:

$$  
\sqrt{a-b}\neq \sqrt{a}-\sqrt{b}  
$$

secara umum.

Contoh pembeda:

$$  
\sqrt{9-4}=\sqrt{5}  
$$

sedangkan:

$$  
\sqrt{9}-\sqrt{4}=3-2=1  
$$

dan:

$$  
\sqrt{5}\neq 1  
$$

---

## 102. Batasan Operasi Pangkat terhadap Penjumlahan

Secara umum:

$$  
(a+b)^n\neq a^n+b^n  
$$

untuk $n>1$.

Untuk $n=2$:

$$  
(a+b)^2=a^2+2ab+b^2  
$$

Suku tengah $2ab$ muncul karena setiap suku pada faktor pertama dikalikan dengan setiap suku pada faktor kedua.

Untuk $n=3$:

$$  
(a+b)^3=a^3+3a^2b+3ab^2+b^3  
$$

Alasannya, perkalian:

$$  
(a+b)(a+b)(a+b)  
$$

menghasilkan semua kombinasi faktor $a$ dan $b$, bukan hanya $a^3$ dan $b^3$.

---

## 103. Bentuk Akar dalam Penyebut dan Standar Penulisan

Dalam banyak konvensi aljabar sekolah, bentuk akhir pecahan tidak dibiarkan memiliki akar di penyebut.

Contoh:

$$  
\frac{2}{\sqrt{5}}  
$$

ditulis sebagai:

$$  
\frac{2\sqrt{5}}{5}  
$$

Kedua bentuk bernilai sama karena:

# $$  
\frac{2}{\sqrt{5}}\cdot\frac{\sqrt{5}}{\sqrt{5}}

\frac{2\sqrt{5}}{5}  
$$

Alasan bentuk kedua dipilih adalah penyebutnya rasional, sehingga struktur pecahan lebih standar dalam manipulasi aljabar.

---

## 104. Bentuk Akar sebagai Faktor

Bentuk akar dapat diperlakukan sebagai faktor aljabar.

Jika:

$$  
A=3\sqrt{2}  
$$

dan:

$$  
B=5\sqrt{2}  
$$

maka:

$$  
A+B=8\sqrt{2}  
$$

karena $\sqrt{2}$ faktor bersama.

Jika:

$$  
A=3\sqrt{2}  
$$

dan:

$$  
C=5\sqrt{3}  
$$

maka:

$$  
A+C  
$$

tidak dapat digabung menjadi satu suku akar sederhana karena faktor akarnya berbeda.

Bentuk itu tetap:

$$  
3\sqrt{2}+5\sqrt{3}  
$$

Kecuali ada penyederhanaan tersembunyi pada salah satu radikan, bentuk akar berbeda tidak digabungkan.

---

## 105. Bentuk Akar dan Pangkat dalam Suku Banyak

> [!definisi] Suku banyak  
> Suku banyak adalah ekspresi aljabar yang tersusun dari penjumlahan suku-suku berpangkat bilangan bulat tak negatif.

Contoh:

$$  
x^2+3x+2  
$$

Bentuk seperti:

$$  
x^{\frac{1}{2}}+x+1  
$$

bukan suku banyak dalam variabel $x$ karena memuat pangkat pecahan.

Bentuk seperti:

$$  
x^{-1}+2  
$$

juga bukan suku banyak karena memuat pangkat negatif.

Alasannya, definisi suku banyak menuntut eksponen variabel berupa bilangan bulat tak negatif.

Namun bentuk-bentuk tersebut tetap merupakan ekspresi aljabar, hanya bukan suku banyak.

---

## 106. Akar dan Eksponen dalam Penyebut Variabel

Bentuk:

$$  
\frac{1}{x^n}  
$$

dapat ditulis:

$$  
x^{-n}  
$$

dengan $x\neq 0$.

Bentuk:

$$  
\frac{1}{\sqrt{x}}  
$$

dapat ditulis:

$$  
x^{-\frac{1}{2}}  
$$

dengan $x>0$.

Bentuk:

$$  
\frac{1}{\sqrt[3]{x}}  
$$

dapat ditulis:

$$  
x^{-\frac{1}{3}}  
$$

dengan $x\neq 0$.

Untuk akar pangkat tiga, $x$ boleh negatif, tetapi tidak boleh nol karena berada di penyebut.

---

## 107. Bentuk Pangkat sebagai Notasi Kompak

Pangkat bukan operasi baru yang terpisah dari perkalian; untuk eksponen bulat positif, pangkat adalah notasi kompak untuk perkalian berulang.

$$  
a^5=a\cdot a\cdot a\cdot a\cdot a  
$$

Akar bukan operasi asing yang berdiri sendiri; akar adalah operasi yang mencari basis dari suatu pangkat.

$$  
\sqrt[n]{a}=b  
$$

berarti:

$$  
b^n=a  
$$

Pangkat pecahan menyatukan dua gagasan itu:

$$  
a^{\frac{m}{n}}  
$$

berarti pangkat $m$ dan akar ke-$n$, dengan syarat real yang sesuai.

---

## 108. Daftar Identitas Inti dengan Syarat

Untuk $a,b>0$ dan $r,s\in\mathbb{Q}$:

$$  
a^r a^s=a^{r+s}  
$$

$$  
\frac{a^r}{a^s}=a^{r-s}  
$$

$$  
(a^r)^s=a^{rs}  
$$

$$  
(ab)^r=a^r b^r  
$$

$$  
\left(\frac{a}{b}\right)^r=\frac{a^r}{b^r}  
$$

Untuk $a,b\geq 0$:

$$  
\sqrt{a}\sqrt{b}=\sqrt{ab}  
$$

$$  
\frac{\sqrt{a}}{\sqrt{b}}=\sqrt{\frac{a}{b}},\quad b>0  
$$

Untuk $a\in\mathbb{R}$:

$$  
\sqrt{a^2}=|a|  
$$

Untuk $a\in\mathbb{R}$:

$$  
\sqrt[3]{a^3}=a  
$$

Untuk $a\neq 0$ dan $n\in\mathbb{N}^+$:

$$  
a^{-n}=\frac{1}{a^n}  
$$

Untuk $a\neq 0$:

$$  
a^0=1  
$$

Setiap syarat ditulis karena tanpa syarat tersebut, beberapa bentuk dapat menjadi tidak terdefinisi atau berubah makna. Matematika memang cerewet, tetapi setidaknya cerewetnya konsisten.
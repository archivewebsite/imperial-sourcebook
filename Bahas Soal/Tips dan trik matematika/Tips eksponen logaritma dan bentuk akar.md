# Tips eksponen logaritma dan bentuk akar

> Pakai untuk menyederhanakan pangkat, akar, logaritma, notasi ilmiah, dan persamaan eksponensial.

## Hukum eksponen

$$
a^m a^n=a^{m+n}
$$

$$
\frac{a^m}{a^n}=a^{m-n}
$$

$$
(a^m)^n=a^{mn}
$$

$$
a^{-n}=\frac{1}{a^n}
$$

$$
a^{m/n}=\sqrt[n]{a^m}
$$

Syarat: perhatikan basis nol, basis negatif, dan akar genap.

## Samakan basis

Untuk persamaan:

$$
a^{f(x)}=a^{g(x)}
$$

jika $a>0$ dan $a\ne 1$, maka:

$$
f(x)=g(x)
$$

Jika basis belum sama, ubah ke basis prima atau basis yang sama.

## Logaritma sebagai eksponen

Definisi:

$$
\log_a b=c \iff a^c=b
$$

dengan $a>0$, $a\ne 1$, dan $b>0$.

## Hukum logaritma

$$
\log_a(xy)=\log_a x+\log_a y
$$

$$
\log_a\left(\frac{x}{y}\right)=\log_a x-\log_a y
$$

$$
\log_a(x^n)=n\log_a x
$$

$$
\log_a b=\frac{\log_c b}{\log_c a}
$$

Jebakan penting: tidak ada aturan untuk $\log(x+y)$ menjadi $\log x+\log y$.

## Rantai logaritma

Jika basis dan argumen menyambung:

$$
\log_a b\cdot \log_b c=\log_a c
$$

Contoh:

$$
\log_2 3\cdot \log_3 8=\log_2 8=3
$$

## Bentuk akar

Keluarkan faktor kuadrat sempurna:

$$
\sqrt{a^2b}=a\sqrt b
$$

Contoh:

$$
\sqrt{72}=\sqrt{36\cdot 2}=6\sqrt2
$$

## Rasionalisasi

Satu akar:

$$
\frac{1}{\sqrt a}=\frac{\sqrt a}{a}
$$

Dua suku:

$$
\frac{1}{a+\sqrt b}=\frac{a-\sqrt b}{a^2-b}
$$

$$
\frac{1}{\sqrt a+\sqrt b}=\frac{\sqrt a-\sqrt b}{a-b}
$$

## Akar dalam akar

Untuk:

$$
\sqrt{a+2\sqrt b}
$$

cari $x,y$ sehingga:

$$
x+y=a,\quad xy=b
$$

Maka:

$$
\sqrt{a+2\sqrt b}=\sqrt x+\sqrt y
$$

Contoh:

$$
\sqrt{7+2\sqrt{12}}=2+\sqrt3
$$

karena $4+3=7$ dan $4\cdot 3=12$.

## Notasi ilmiah

Gunakan:

$$
(a\times 10^m)(b\times 10^n)=ab\times 10^{m+n}
$$

Pastikan angka depan berada pada interval $1\le a<10$.

## Jebakan umum

- Cek domain log setelah menyelesaikan persamaan.
- Akar kuadrat utama selalu tidak negatif.
- Saat menguadratkan dua sisi, cek ulang solusi ke persamaan awal.
- Jangan mencampur aturan pangkat untuk penjumlahan: $(a+b)^2\ne a^2+b^2$.

## Terkait

- [[Tips aljabar dan faktorisasi]]
- [[Tips persamaan pertidaksamaan dan fungsi]]
- [[Tips bilangan dan teori bilangan]]

## Sumber rujukan

- [OpenStax Algebra and Trigonometry 2e - Logarithmic Properties](https://openstax.org/books/algebra-and-trigonometry-2e/pages/6-5-logarithmic-properties)
- [OpenStax Algebra and Trigonometry 2e - Key Equations, Chapter 6](https://openstax.org/books/algebra-and-trigonometry-2e/pages/6-key-equations)


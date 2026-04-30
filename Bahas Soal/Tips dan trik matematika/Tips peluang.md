# Tips peluang

> Pakai untuk kejadian acak, peluang bersyarat, minimal satu kejadian, pengambilan objek, binomial, dan ekspektasi.

## Rumus dasar

Jika semua hasil sama mungkin:

$$
P(A)=\frac{\text{banyak hasil menguntungkan}}{\text{banyak seluruh hasil}}
$$

## Komplemen

Gunakan komplemen untuk soal "minimal satu", "setidaknya", atau "tidak semuanya".

$$
P(A)=1-P(A^c)
$$

Contoh:

Peluang minimal satu angka $6$ dalam $4$ lemparan dadu:

$$
1-\left(\frac{5}{6}\right)^4
$$

## Aturan penjumlahan

Untuk dua kejadian:

$$
P(A\cup B)=P(A)+P(B)-P(A\cap B)
$$

Jika saling lepas:

$$
P(A\cup B)=P(A)+P(B)
$$

## Aturan perkalian

Secara umum:

$$
P(A\cap B)=P(A)P(B|A)
$$

Jika independen:

$$
P(A\cap B)=P(A)P(B)
$$

## Peluang bersyarat

$$
P(A|B)=\frac{P(A\cap B)}{P(B)}
$$

Syarat: $P(B)>0$.

## Bayes

$$
P(A|B)=\frac{P(B|A)P(A)}{P(B)}
$$

Pakai jika soal memberi peluang gejala dengan syarat penyebab, tetapi yang ditanya penyebab dengan syarat gejala.

## Dengan atau tanpa pengembalian

| Situasi | Dampak |
|---|---|
| dengan pengembalian | peluang tiap pengambilan tetap |
| tanpa pengembalian | penyebut dan pembilang berubah |

Untuk tanpa pengembalian, sering lebih aman menggambar pohon singkat.

## Distribusi binomial

Jika ada $n$ percobaan independen, peluang sukses $p$, dan ditanya tepat $k$ sukses:

$$
P(X=k)=\binom{n}{k}p^k(1-p)^{n-k}
$$

Mean:

$$
E[X]=np
$$

Variansi:

$$
\operatorname{Var}(X)=np(1-p)
$$

## Ekspektasi linear

Ekspektasi bisa dijumlahkan walau kejadian tidak independen:

$$
E[X+Y]=E[X]+E[Y]
$$

Trik: definisikan variabel indikator untuk menghitung "banyaknya objek yang memenuhi syarat".

## Jebakan umum

- Independen tidak sama dengan saling lepas.
- "Minimal satu" biasanya lebih cepat dengan komplemen.
- Dalam peluang bersyarat, ruang sampel berubah.
- Untuk pengambilan tanpa pengembalian, jangan pakai peluang tetap.

## Terkait

- [[Tips kombinatorika]]
- [[Tips statistika]]
- [[Tips bilangan dan teori bilangan]]

## Sumber rujukan

- [OpenStax Precalculus 2e - Key Equations, Chapter 11](https://openstax.org/books/precalculus-2e/pages/11-key-equations)
- [OpenStax Introductory Statistics 2e - Mathematical Phrases, Symbols, and Formulas](https://openstax.org/books/introductory-statistics-2e/pages/f-mathematical-phrases-symbols-and-formulas)


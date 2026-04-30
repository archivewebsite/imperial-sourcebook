# Tips kombinatorika

> Pakai untuk soal "berapa banyak cara", susunan, pilihan, urutan, pembagian objek, dan koefisien binomial.

## Prinsip penjumlahan dan perkalian

- Jika pilihan saling eksklusif, jumlahkan.
- Jika proses bertahap dan setiap tahap harus terjadi, kalikan.

Contoh:

Jika ada $3$ pilihan baju dan $4$ pilihan celana, jumlah pasangan:

$$
3\cdot 4=12
$$

## Permutasi vs kombinasi

Tanya dulu: urutan penting atau tidak?

| Situasi | Rumus |
|---|---|
| urutan penting | $P(n,r)=\frac{n!}{(n-r)!}$ |
| urutan tidak penting | $\binom{n}{r}=\frac{n!}{r!(n-r)!}$ |

## Komplemen dalam menghitung

Jika menghitung langsung rumit, hitung total dikurangi kasus buruk.

Contoh:

"Minimal satu" sering lebih cepat sebagai:

$$
\text{total} - \text{tidak ada sama sekali}
$$

## Inklusi-eksklusi

Untuk dua himpunan:

$$
|A\cup B|=|A|+|B|-|A\cap B|
$$

Untuk tiga himpunan:

$$
|A\cup B\cup C|=|A|+|B|+|C|-|A\cap B|-|A\cap C|-|B\cap C|+|A\cap B\cap C|
$$

## Permutasi dengan unsur sama

Jika total $n$ objek dan ada pengulangan $a,b,c,\ldots$:

$$
\frac{n!}{a!b!c!\cdots}
$$

Contoh jumlah susunan "MAMA":

$$
\frac{4!}{2!2!}=6
$$

## Permutasi melingkar

Untuk $n$ objek berbeda di lingkaran:

$$
(n-1)!
$$

Jika kalung bisa dibalik dan semua objek berbeda:

$$
\frac{(n-1)!}{2}
$$

## Stars and bars

Jumlah solusi bilangan bulat tak negatif:

$$
x_1+x_2+\cdots+x_k=n
$$

adalah:

$$
\binom{n+k-1}{k-1}
$$

Jika setiap $x_i\ge 1$:

$$
\binom{n-1}{k-1}
$$

## Identitas kombinasi

$$
\binom{n}{r}=\binom{n}{n-r}
$$

$$
\binom{n}{r}+\binom{n}{r-1}=\binom{n+1}{r}
$$

$$
\sum_{r=0}^{n}\binom{n}{r}=2^n
$$

Hockey stick:

$$
\binom{r}{r}+\binom{r+1}{r}+\cdots+\binom{n}{r}=\binom{n+1}{r+1}
$$

## Koefisien binomial

Koefisien $x^r$ dalam:

$$
(1+x)^n
$$

adalah:

$$
\binom{n}{r}
$$

Untuk:

$$
(a+b)^n
$$

suku umum:

$$
\binom{n}{r}a^{n-r}b^r
$$

## Derangement

Banyak permutasi tanpa objek kembali ke posisi asal:

$$
!n=n!\left(1-\frac{1}{1!}+\frac{1}{2!}-\cdots+\frac{(-1)^n}{n!}\right)
$$

Perkiraan:

$$
!n\approx \frac{n!}{e}
$$

## Catalan

Bilangan Catalan:

$$
C_n=\frac{1}{n+1}\binom{2n}{n}
$$

Muncul pada susunan kurung valid, jalur kisi yang tidak melewati diagonal, dan beberapa bentuk pohon biner.

## Jebakan umum

- Jangan membagi dengan $r!$ jika urutan memang penting.
- Jika ada batas maksimal tiap kotak, stars and bars biasa belum cukup.
- Permutasi melingkar berbeda dari permutasi baris karena rotasi dianggap sama.
- Hati-hati overcount: satu objek yang sama jangan dihitung berkali-kali karena label palsu.

## Terkait

- [[Tips peluang]]
- [[Tips bilangan dan teori bilangan]]
- [[Tips barisan deret dan pola]]

## Sumber rujukan

- [OpenStax Precalculus 2e - Key Equations, Chapter 11](https://openstax.org/books/precalculus-2e/pages/11-key-equations)

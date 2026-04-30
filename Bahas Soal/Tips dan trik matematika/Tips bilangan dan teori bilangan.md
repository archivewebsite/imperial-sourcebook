# Tips bilangan dan teori bilangan

> Pakai untuk faktor, kelipatan, sisa bagi, digit terakhir, bilangan prima, banyak pembagi, dan pola bilangan bulat.

## FPB dan KPK

Rumus paling sering:

$$
\gcd(a,b)\cdot \operatorname{lcm}(a,b)=ab
$$

Pakai jika dua dari tiga informasi diketahui.

## Algoritma Euclid

Untuk mencari FPB cepat:

$$
\gcd(a,b)=\gcd(b, a \bmod b)
$$

Contoh:

$$
\gcd(252,105)=\gcd(105,42)=\gcd(42,21)=21
$$

## Aturan habis dibagi

| Pembagi | Aturan cepat |
|---|---|
| $2$ | digit terakhir genap |
| $3$ | jumlah digit habis dibagi $3$ |
| $4$ | dua digit terakhir habis dibagi $4$ |
| $5$ | digit terakhir $0$ atau $5$ |
| $6$ | habis dibagi $2$ dan $3$ |
| $8$ | tiga digit terakhir habis dibagi $8$ |
| $9$ | jumlah digit habis dibagi $9$ |
| $11$ | selisih jumlah digit selang-seling habis dibagi $11$ |
| $25$ | dua digit terakhir $00$, $25$, $50$, atau $75$ |

## Faktorisasi prima

Jika:

$$
n=p_1^{a_1}p_2^{a_2}\cdots p_k^{a_k}
$$

maka banyak pembagi positif:

$$
d(n)=(a_1+1)(a_2+1)\cdots(a_k+1)
$$

Contoh:

$$
60=2^2\cdot 3\cdot 5 \Rightarrow d(60)=3\cdot 2\cdot 2=12
$$

## Jumlah pembagi

Untuk $n=p^a q^b \cdots$:

$$
\sigma(n)=\frac{p^{a+1}-1}{p-1}\cdot \frac{q^{b+1}-1}{q-1}\cdots
$$

Pakai jika soal menanyakan jumlah semua faktor, bukan banyaknya faktor.

## Sisa bagi dan modular

Aturan operasi:

$$
(a+b)\bmod n = ((a\bmod n)+(b\bmod n))\bmod n
$$

$$
ab\bmod n = ((a\bmod n)(b\bmod n))\bmod n
$$

Gunakan untuk digit terakhir, pola kalender, dan pangkat besar.

## Digit terakhir pangkat

Siklus umum:

| Basis akhir | Siklus digit akhir |
|---|---|
| $2$ | $2,4,8,6$ |
| $3$ | $3,9,7,1$ |
| $4$ | $4,6$ |
| $7$ | $7,9,3,1$ |
| $8$ | $8,4,2,6$ |
| $9$ | $9,1$ |
| $0,1,5,6$ | tetap |

Contoh:

$$
7^{2026}: 2026 \bmod 4 = 2 \Rightarrow \text{digit akhir }9
$$

## Banyak nol di akhir faktorial

Jumlah nol di akhir $n!$ ditentukan oleh faktor $5$:

$$
v_5(n!)=\left\lfloor \frac{n}{5}\right\rfloor+\left\lfloor \frac{n}{25}\right\rfloor+\left\lfloor \frac{n}{125}\right\rfloor+\cdots
$$

Contoh:

$$
100! \text{ punya }20+4=24\text{ nol}
$$

## Fermat kecil

Jika $p$ prima dan $\gcd(a,p)=1$:

$$
a^{p-1}\equiv 1 \pmod p
$$

Pakai untuk memangkas pangkat besar modulo bilangan prima.

## Jebakan umum

- Jangan pakai aturan Fermat jika modulus bukan prima.
- Digit terakhir hanya memberi informasi modulo $10$, bukan nilai penuh.
- Untuk FPB/KPK lebih dari dua bilangan, kerjakan bertahap.
- Jumlah pembagi dan banyak pembagi adalah dua pertanyaan berbeda.

## Terkait

- [[Tips aritmetika cepat dan pecahan]]
- [[Tips kombinatorika]]
- [[Tips peluang]]

## Sumber rujukan

- [Wolfram MathWorld - Number Theory](https://mathworld.wolfram.com/NumberTheory.html)
- [OpenStax Precalculus 2e - Key Equations, Chapter 11](https://openstax.org/books/precalculus-2e/pages/11-key-equations)


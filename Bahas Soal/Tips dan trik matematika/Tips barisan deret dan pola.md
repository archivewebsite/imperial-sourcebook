# Tips barisan deret dan pola

> Pakai untuk soal suku ke-n, jumlah deret, pola gambar, beda bertingkat, dan rekursi sederhana.

## Barisan aritmetika

Suku ke-$n$:

$$
U_n=a+(n-1)d
$$

Jumlah $n$ suku:

$$
S_n=\frac{n}{2}(a+U_n)=\frac{n}{2}(2a+(n-1)d)
$$

Trik: jika diketahui suku pertama dan terakhir, gunakan rata-rata kali banyak suku.

## Barisan geometri

Suku ke-$n$:

$$
U_n=ar^{n-1}
$$

Jumlah $n$ suku:

$$
S_n=a\frac{r^n-1}{r-1},\quad r\ne 1
$$

Deret geometri tak hingga:

$$
S_\infty=\frac{a}{1-r},\quad |r|<1
$$

## Beda bertingkat

Jika beda pertama konstan, bentuknya linear.

Jika beda kedua konstan, bentuknya kuadrat:

$$
U_n=An^2+Bn+C
$$

Cara cepat:

1. Buat tabel $n$ dan $U_n$.
2. Hitung beda pertama.
3. Hitung beda kedua.
4. Jika beda kedua $=2A$, langsung dapat $A$.
5. Substitusi dua nilai awal untuk $B,C$.

## Deret penting

$$
1+2+\cdots+n=\frac{n(n+1)}{2}
$$

$$
1^2+2^2+\cdots+n^2=\frac{n(n+1)(2n+1)}{6}
$$

$$
1^3+2^3+\cdots+n^3=\left(\frac{n(n+1)}{2}\right)^2
$$

$$
1+3+5+\cdots+(2n-1)=n^2
$$

## Telescoping

Pecah pecahan agar banyak suku saling hapus:

$$
\frac{1}{n(n+1)}=\frac{1}{n}-\frac{1}{n+1}
$$

$$
\frac{1}{n(n+2)}=\frac{1}{2}\left(\frac{1}{n}-\frac{1}{n+2}\right)
$$

Contoh:

$$
\sum_{n=1}^{N}\frac{1}{n(n+1)}=1-\frac{1}{N+1}
$$

## Pola gambar

Untuk pola gambar, catat:

- jumlah baru yang ditambahkan setiap tahap
- apakah pertambahan konstan
- apakah ada bentuk persegi, segitiga, atau kisi
- apakah tahap ke-$0$ lebih alami daripada tahap ke-$1$

## Rekursi sederhana

Jika:

$$
U_n=U_{n-1}+d
$$

maka aritmetika. Jika:

$$
U_n=rU_{n-1}
$$

maka geometri.

## Jebakan umum

- Jangan pakai rumus geometri jika rasio tidak konstan.
- Cek apakah $n$ dimulai dari $0$ atau $1$.
- Untuk deret tak hingga, wajib $|r|<1$.
- Pada pola gambar, gambar tahap awal kadang hanya ilustrasi, bukan definisi penuh.

## Terkait

- [[Tips aljabar dan faktorisasi]]
- [[Tips kombinatorika]]
- [[Tips kalkulus dasar]]

## Sumber rujukan

- [OpenStax Precalculus 2e - Key Equations, Chapter 11](https://openstax.org/books/precalculus-2e/pages/11-key-equations)


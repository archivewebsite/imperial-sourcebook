# Tips kalkulus dasar

> Pakai untuk limit, turunan, integral dasar, optimasi, laju perubahan, luas daerah, dan volume putar tingkat awal.

## Limit

Mulai dari substitusi langsung. Jika muncul bentuk tak tentu seperti $0/0$, coba:

1. faktorkan
2. rasionalkan
3. samakan penyebut
4. gunakan limit khusus
5. gunakan L'Hopital jika sudah memenuhi bentuk $0/0$ atau $\infty/\infty$

Limit khusus:

$$
\lim_{x\to 0}\frac{\sin x}{x}=1
$$

$$
\lim_{x\to 0}\frac{1-\cos x}{x^2}=\frac{1}{2}
$$

$$
\lim_{x\to 0}\frac{e^x-1}{x}=1
$$

## Turunan dasar

$$
\frac{d}{dx}x^n=nx^{n-1}
$$

$$
\frac{d}{dx}\sin x=\cos x
$$

$$
\frac{d}{dx}\cos x=-\sin x
$$

$$
\frac{d}{dx}e^x=e^x
$$

$$
\frac{d}{dx}\ln x=\frac{1}{x}
$$

## Aturan turunan

Jumlah:

$$
(f+g)'=f'+g'
$$

Produk:

$$
(fg)'=f'g+fg'
$$

Hasil bagi:

$$
\left(\frac{f}{g}\right)'=\frac{f'g-fg'}{g^2}
$$

Rantai:

$$
(f(g(x)))'=f'(g(x))g'(x)
$$

## Optimasi

Langkah cepat:

1. Tulis fungsi objektif.
2. Ubah menjadi satu variabel.
3. Turunkan.
4. Cari titik kritis.
5. Cek ujung interval jika domain tertutup.

Tanda turunan:

- $f'(x)>0$: naik.
- $f'(x)<0$: turun.
- $f'(x)=0$: kandidat maksimum/minimum lokal.

## Integral dasar

$$
\int x^n\,dx=\frac{x^{n+1}}{n+1}+C,\quad n\ne -1
$$

$$
\int \frac{1}{x}\,dx=\ln|x|+C
$$

$$
\int e^x\,dx=e^x+C
$$

$$
\int \sin x\,dx=-\cos x+C
$$

$$
\int \cos x\,dx=\sin x+C
$$

## Substitusi integral

Jika ada fungsi dalam dan turunannya:

$$
\int f(g(x))g'(x)\,dx
$$

pakai $u=g(x)$.

Contoh pola:

$$
\int 2x(x^2+1)^5\,dx
$$

ambil $u=x^2+1$.

## Simetri integral

Jika $f$ ganjil:

$$
\int_{-a}^{a}f(x)\,dx=0
$$

Jika $f$ genap:

$$
\int_{-a}^{a}f(x)\,dx=2\int_0^a f(x)\,dx
$$

## Luas dan volume

Luas antara dua kurva:

$$
L=\int_a^b(\text{atas}-\text{bawah})\,dx
$$

Volume cakram terhadap sumbu $x$:

$$
V=\pi\int_a^b [f(x)]^2\,dx
$$

Kulit silinder terhadap sumbu $y$:

$$
V=2\pi\int_a^b x f(x)\,dx
$$

## Jebakan umum

- Limit trigonometri khusus memakai radian.
- L'Hopital hanya untuk bentuk tak tentu tertentu.
- Integral tak tentu butuh konstanta $C$.
- Untuk luas, pakai nilai positif "atas minus bawah", bukan sekadar integral satu fungsi.
- Titik kritis tidak otomatis maksimum atau minimum; cek tanda atau nilai.

## Terkait

- [[Tips persamaan pertidaksamaan dan fungsi]]
- [[Tips trigonometri]]
- [[Tips barisan deret dan pola]]

## Sumber rujukan

- [OpenStax Calculus Volume 1 - Key Equations, Chapter 2](https://openstax.org/books/calculus-volume-1/pages/2-key-equations)
- [OpenStax Calculus Volume 1 - Key Equations, Chapter 3](https://openstax.org/books/calculus-volume-1/pages/3-key-equations)
- [OpenStax Calculus Volume 1 - Key Equations, Chapter 5](https://openstax.org/books/calculus-volume-1/pages/5-key-equations)
- [Paul's Online Math Notes - Calculus Cheat Sheets](https://tutorial.math.lamar.edu/cheat_table.aspx)

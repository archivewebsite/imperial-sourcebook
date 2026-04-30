# Tips geometri koordinat

> Pakai untuk titik, garis, gradien, jarak, lingkaran, parabola, dan luas poligon di bidang koordinat.

## Jarak dan titik tengah

Jarak dua titik:

$$
d=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2}
$$

Titik tengah:

$$
M=\left(\frac{x_1+x_2}{2},\frac{y_1+y_2}{2}\right)
$$

## Gradien

$$
m=\frac{y_2-y_1}{x_2-x_1}
$$

Hubungan garis:

- Sejajar: $m_1=m_2$.
- Tegak lurus: $m_1m_2=-1$.
- Garis vertikal: gradien tidak terdefinisi.

## Persamaan garis

Titik-gradien:

$$
y-y_1=m(x-x_1)
$$

Gradien-intersep:

$$
y=mx+c
$$

Bentuk umum:

$$
Ax+By+C=0
$$

## Jarak titik ke garis

Untuk titik $(x_0,y_0)$ dan garis $Ax+By+C=0$:

$$
d=\frac{|Ax_0+By_0+C|}{\sqrt{A^2+B^2}}
$$

## Luas segitiga dari koordinat

Untuk titik $(x_1,y_1)$, $(x_2,y_2)$, $(x_3,y_3)$:

$$
L=\frac{1}{2}|x_1(y_2-y_3)+x_2(y_3-y_1)+x_3(y_1-y_2)|
$$

## Shoelace

Untuk poligon:

$$
L=\frac{1}{2}\left|\sum x_i y_{i+1}-\sum y_i x_{i+1}\right|
$$

Ulangi titik pertama di akhir daftar agar pasangan terakhir tertutup.

## Pick's theorem

Untuk poligon pada kisi bilangan bulat:

$$
L=I+\frac{B}{2}-1
$$

dengan:

- $I$: banyak titik kisi di dalam poligon.
- $B$: banyak titik kisi pada batas poligon.

Pakai saat semua titik sudut berada pada koordinat bilangan bulat dan soal meminta luas.

## Lingkaran

Bentuk pusat-radius:

$$
(x-a)^2+(y-b)^2=r^2
$$

Bentuk umum:

$$
x^2+y^2+Dx+Ey+F=0
$$

Pusat:

$$
\left(-\frac{D}{2},-\frac{E}{2}\right)
$$

Radius:

$$
r=\sqrt{\frac{D^2+E^2}{4}-F}
$$

## Parabola cepat

Untuk:

$$
y=ax^2+bx+c
$$

sumbu:

$$
x=-\frac{b}{2a}
$$

Titik potong $y$ adalah $(0,c)$.

## Jebakan umum

- Rumus jarak titik ke garis perlu bentuk umum $Ax+By+C=0$.
- Gradien garis vertikal tidak boleh dipakai dalam rumus $y=mx+c$.
- Pada shoelace, urutan titik harus mengitari poligon, bukan acak.
- Untuk lingkaran, koefisien $x^2$ dan $y^2$ harus sama sebelum memakai bentuk umum.

## Terkait

- [[Tips geometri bidang]]
- [[Tips persamaan pertidaksamaan dan fungsi]]
- [[Tips trigonometri]]

## Sumber rujukan

- [OpenStax Precalculus 2e - Key Equations, Chapter 2](https://openstax.org/books/precalculus-2e/pages/2-key-equations)
- [OpenStax Precalculus 2e - Key Equations, Chapter 10](https://openstax.org/books/precalculus-2e/pages/10-key-equations)

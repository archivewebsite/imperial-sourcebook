# Tips aljabar dan faktorisasi

> Pakai saat ekspresi bisa disederhanakan, difaktorkan, atau diubah bentuk sebelum menyelesaikan persamaan.

## Urutan berpikir

1. Cari faktor persekutuan.
2. Cari pola identitas.
3. Jika kuadrat, cek apakah faktorisasi cepat mungkin.
4. Jika simetris, ubah ke jumlah dan hasil kali.
5. Jika tidak rapi, pakai rumus umum atau substitusi.

## Identitas wajib

$$
(a+b)^2=a^2+2ab+b^2
$$

$$
(a-b)^2=a^2-2ab+b^2
$$

$$
a^2-b^2=(a+b)(a-b)
$$

$$
a^3+b^3=(a+b)(a^2-ab+b^2)
$$

$$
a^3-b^3=(a-b)(a^2+ab+b^2)
$$

## Selisih kuadrat sebagai jalan hitung

Jika bentuknya dua angka dekat:

$$
87\cdot 93=(90-3)(90+3)=90^2-3^2=8091
$$

## Kuadrat sempurna

Kenali:

$$
x^2+2ax+a^2=(x+a)^2
$$

$$
x^2-2ax+a^2=(x-a)^2
$$

Trik cepat: suku tengah harus dua kali hasil kali akar suku pertama dan akar suku terakhir.

## Faktorisasi kuadrat monik

Untuk:

$$
x^2+bx+c
$$

cari $m,n$ sehingga:

$$
m+n=b,\quad mn=c
$$

Maka:

$$
x^2+bx+c=(x+m)(x+n)
$$

## Faktorisasi kuadrat nonmonik

Untuk $ax^2+bx+c$:

1. Hitung $ac$.
2. Cari $m,n$ dengan $mn=ac$ dan $m+n=b$.
3. Pecah $bx$ menjadi $mx+nx$.
4. Faktorkan dengan pengelompokan.

## Melengkapkan kuadrat

Untuk bentuk:

$$
x^2+bx
$$

gunakan:

$$
x^2+bx=\left(x+\frac{b}{2}\right)^2-\left(\frac{b}{2}\right)^2
$$

Pakai untuk titik puncak parabola, nilai minimum, dan rumus kuadrat.

## Vieta untuk kuadrat

Jika akar $x_1,x_2$ dari:

$$
ax^2+bx+c=0
$$

maka:

$$
x_1+x_2=-\frac{b}{a},\quad x_1x_2=\frac{c}{a}
$$

Turunan cepat:

$$
x_1^2+x_2^2=(x_1+x_2)^2-2x_1x_2
$$

$$
\frac{1}{x_1}+\frac{1}{x_2}=\frac{x_1+x_2}{x_1x_2}
$$

## Diskriminan

Untuk:

$$
ax^2+bx+c=0
$$

diskriminan:

$$
D=b^2-4ac
$$

- $D>0$: dua akar real berbeda.
- $D=0$: akar kembar.
- $D<0$: tidak ada akar real.
- $D$ kuadrat sempurna: akar rasional lebih mungkin.

## SFFT

Jika ada pola $xy+ax+by$, tambahkan dan kurangi $ab$:

$$
xy+ax+by+ab=(x+b)(y+a)
$$

Contoh:

$$
xy+5x+3y=7
$$

Tambah $15$:

$$
(x+3)(y+5)=22
$$

## Teorema faktor dan sisa

Jika $f(a)=0$, maka $(x-a)$ adalah faktor dari $f(x)$.

Sisa pembagian $f(x)$ oleh $(x-a)$ adalah:

$$
f(a)
$$

Untuk pembagi $(ax-b)$, sisa adalah:

$$
f\left(\frac{b}{a}\right)
$$

## Uji akar rasional

Jika akar rasional dari:

$$
a_nx^n+\cdots+a_1x+a_0=0
$$

adalah $\frac{p}{q}$ dalam bentuk sederhana, maka:

$$
p\mid a_0,\quad q\mid a_n
$$

Pakai untuk menyaring kandidat akar sebelum membagi polinom.

## Vieta untuk pangkat tiga

Jika akar $\alpha,\beta,\gamma$ dari:

$$
x^3+px^2+qx+r=0
$$

maka:

$$
\alpha+\beta+\gamma=-p
$$

$$
\alpha\beta+\beta\gamma+\gamma\alpha=q
$$

$$
\alpha\beta\gamma=-r
$$

## Ekspresi simetris

Jika diketahui:

$$
x+y=s,\quad xy=p
$$

maka:

$$
x^2+y^2=s^2-2p
$$

$$
x^3+y^3=s^3-3sp
$$

Gunakan saat soal hanya memberi jumlah dan hasil kali akar.

## AM-GM

Untuk bilangan positif:

$$
\frac{a_1+a_2+\cdots+a_n}{n}\ge \sqrt[n]{a_1a_2\cdots a_n}
$$

Sama dengan terjadi saat semua $a_i$ sama.

Pola cepat:

$$
x+\frac{1}{x}\ge 2,\quad x>0
$$

## Cauchy bentuk Engel

Untuk penyebut positif:

$$
\frac{a^2}{x}+\frac{b^2}{y}+\frac{c^2}{z}\ge \frac{(a+b+c)^2}{x+y+z}
$$

Pakai untuk pertidaksamaan pecahan yang punya jumlah penyebut.

## Jebakan umum

- Jangan membagi dengan ekspresi yang mungkin nol tanpa mencatat kasus nol.
- Rumus Vieta butuh bentuk standar sama dengan nol.
- Kuadrat sempurna harus cocok tanda dan suku tengah.
- Dalam pertidaksamaan, mengalikan dengan bilangan negatif membalik tanda.
- AM-GM dan Cauchy bentuk ini perlu syarat positif pada bagian tertentu.

## Terkait

- [[Tips persamaan pertidaksamaan dan fungsi]]
- [[Tips eksponen logaritma dan bentuk akar]]
- [[Tips soal cerita dan strategi ujian]]

## Sumber rujukan

- [OpenStax Algebra and Trigonometry 2e - Quadratic Equations](https://openstax.org/books/algebra-and-trigonometry-2e/pages/2-5-quadratic-equations)

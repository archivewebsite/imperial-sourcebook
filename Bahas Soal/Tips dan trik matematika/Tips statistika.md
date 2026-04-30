# Tips statistika

> Pakai untuk mean, median, modus, kuartil, variansi, simpangan baku, data berkelompok, grafik data, dan interpretasi ringkas.

## Mean cepat dengan asumsi

Pilih angka acuan $A$ dekat pusat data:

$$
\bar{x}=A+\frac{\sum(x_i-A)}{n}
$$

Contoh data $48,52,47,53,50$, pilih $A=50$:

$$
\bar{x}=50+\frac{-2+2-3+3+0}{5}=50
$$

## Mean gabungan

Jika dua kelompok punya banyak data $n_1,n_2$ dan mean $m_1,m_2$:

$$
m=\frac{n_1m_1+n_2m_2}{n_1+n_2}
$$

Jebakan: mean gabungan bukan rata-rata dari dua mean jika ukuran kelompok berbeda.

## Median

- Urutkan data dulu.
- Jika $n$ ganjil, median adalah data ke-$(n+1)/2$.
- Jika $n$ genap, median adalah rata-rata data ke-$n/2$ dan ke-$(n/2+1)$.

## Modus

Modus adalah nilai yang paling sering muncul. Data bisa punya:

- tidak ada modus
- satu modus
- lebih dari satu modus

## Jangkauan dan IQR

Jangkauan:

$$
R=x_{\max}-x_{\min}
$$

IQR:

$$
IQR=Q_3-Q_1
$$

IQR lebih tahan terhadap pencilan daripada jangkauan.

## Variansi cepat

Untuk populasi:

$$
\sigma^2=E[X^2]-(E[X])^2
$$

Untuk data:

$$
\sigma^2=\frac{\sum x_i^2}{n}-\bar{x}^2
$$

Simpangan baku:

$$
\sigma=\sqrt{\sigma^2}
$$

## Transformasi data

Jika semua data ditambah $c$:

- mean naik $c$
- median naik $c$
- simpangan baku tetap

Jika semua data dikali $k$:

- mean dikali $k$
- median dikali $k$
- simpangan baku dikali $|k|$
- variansi dikali $k^2$

## Data berkelompok

Median:

$$
Me=L+\frac{\frac{n}{2}-F}{f}\cdot p
$$

Modus:

$$
Mo=L+\frac{d_1}{d_1+d_2}\cdot p
$$

Keterangan:

- $L$: tepi bawah kelas.
- $F$: frekuensi kumulatif sebelum kelas.
- $f$: frekuensi kelas.
- $p$: panjang kelas.
- $d_1$: selisih frekuensi kelas modus dengan kelas sebelumnya.
- $d_2$: selisih frekuensi kelas modus dengan kelas sesudahnya.

## Membaca grafik

- Cek satuan sumbu.
- Cek apakah sumbu mulai dari nol.
- Untuk diagram lingkaran, ubah persen ke bagian total.
- Untuk histogram, perhatikan lebar kelas jika tidak sama.

## Jebakan umum

- Mean sensitif terhadap pencilan.
- Median perlu data terurut.
- Persentase pada grafik harus punya basis total yang jelas.
- Data berkelompok memberi pendekatan, bukan nilai eksak semua data mentah.

## Terkait

- [[Tips peluang]]
- [[Tips persen rasio dan proporsi]]
- [[Tips soal cerita dan strategi ujian]]

## Sumber rujukan

- [OpenStax Introductory Statistics 2e - Mathematical Phrases, Symbols, and Formulas](https://openstax.org/books/introductory-statistics-2e/pages/f-mathematical-phrases-symbols-and-formulas)


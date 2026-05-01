# Tips aritmetika cepat dan pecahan

> Pakai saat soal menuntut hitungan cepat, estimasi, operasi pecahan, atau pengecekan angka sebelum memakai aljabar.

## Prinsip utama

- Pecah angka ke bentuk dekat $10$, $100$, $1000$, atau pecahan yang mudah.
- Kompensasi perubahan: jika satu bagian dinaikkan, bagian lain harus dikoreksi.
- Pilih operasi yang mengurangi beban memori: bagi dulu jika hasilnya tetap bulat.
- Setelah selesai, cek digit terakhir, orde besar, atau sisa mod $9$.

## Perkalian cepat

### Kali 5, 25, 50, 125

| Operasi | Cara cepat |
|---|---|
| $\times 5$ | bagi $2$, lalu kali $10$ |
| $\times 25$ | bagi $4$, lalu kali $100$ |
| $\times 50$ | bagi $2$, lalu kali $100$ |
| $\times 125$ | bagi $8$, lalu kali $1000$ |

Contoh:

$$
48 \times 125 = 6 \times 1000 = 6000
$$

### Kali 9, 99, 999

Gunakan komplemen:

$$
n \times 99 = 100n - n
$$

Contoh:

$$
86 \times 99 = 8600 - 86 = 8514
$$

### Kali 11 untuk dua digit

Untuk $ab \times 11$, sisipkan $a+b$ di tengah. Jika $a+b \ge 10$, simpan satu ke digit depan.

$$
72 \times 11 = 7(9)2 = 792
$$

$$
78 \times 11 = 7(15)8 = 858
$$

### Dekat 100

Untuk $(100-a)(100-b)$:

$$
(100-a)(100-b)=10000-100(a+b)+ab
$$

Contoh:

$$
96 \times 97 = 10000 - 700 + 12 = 9312
$$

### Selisih kuadrat

Jika dua faktor mengapit angka tengah yang mudah:

$$
(m-d)(m+d)=m^2-d^2
$$

Contoh:

$$
47 \times 53 = 50^2-3^2 = 2491
$$

### Kuadrat berakhiran 5

Jika bilangan berbentuk $10a+5$:

$$
(10a+5)^2 = a(a+1)\,|\,25
$$

Contoh:

$$
85^2 = 8 \cdot 9\,|\,25 = 7225
$$

## Pecahan cepat

### Bandingkan pecahan dengan silang

Untuk penyebut positif:

$$
\frac{a}{b} > \frac{c}{d} \iff ad > bc
$$

Contoh:

$$
\frac{7}{9} \text{ vs } \frac{5}{7}: 49 > 45
$$

Jadi $\frac{7}{9}$ lebih besar.

### Pecahan patokan yang wajib cepat

| Pecahan | Desimal | Persen |
|---|---:|---:|
| $1/2$ | $0.5$ | $50\%$ |
| $1/3$ | $0.333...$ | $33.33\%$ |
| $1/4$ | $0.25$ | $25\%$ |
| $1/5$ | $0.2$ | $20\%$ |
| $1/8$ | $0.125$ | $12.5\%$ |
| $1/16$ | $0.0625$ | $6.25\%$ |
| $1/20$ | $0.05$ | $5\%$ |
| $1/25$ | $0.04$ | $4\%$ |

### Pecahan campuran ke pecahan biasa

Jangan kalikan semua jika hanya perlu membandingkan. Untuk $a\frac{b}{c}$, lihat bagian utuh dulu. Jika bagian utuh sama, bandingkan pecahannya.

## Cek cepat

- Digit terakhir hasil perkalian harus cocok dengan hasil kali digit terakhir faktor.
- Hasil perkalian dua angka dekat $100$ harus dekat $10000$.
- Untuk penjumlahan banyak angka, kelompokkan ke pasangan $10$, $100$, atau $1000$.
- Untuk cek aritmetika, jumlah digit hasil harus sama sisa mod $9$ dengan operasi asal.

## Konstanta pendekatan

| Konstanta | Pendekatan |
|---|---:|
| $\pi$ | $3.14$ atau $22/7$ |
| $e$ | $2.718$ |
| $\sqrt2$ | $1.414$ |
| $\sqrt3$ | $1.732$ |
| $\sqrt5$ | $2.236$ |
| $\ln 2$ | $0.693$ |
| $\log_{10}2$ | $0.301$ |
| $\log_{10}3$ | $0.477$ |

Gunakan untuk membuang opsi yang terlalu jauh sebelum menghitung persis.

## Jebakan umum

- Soal meminta pembuktian, bukan hasil numerik.
- Bilangan tidak dekat patokan dan trik justru menambah langkah.
- Pecahan punya penyebut negatif; normalkan tanda dulu.
- Pada pembulatan kompensasi, hasil perkiraan tetap harus dicek dengan batas atas dan batas bawah jika opsi berdekatan.
- Trik digit terakhir hanya memeriksa satu digit; hasil yang digit akhirnya benar masih bisa salah.

## Terkait

- [[Tips persen rasio dan proporsi]]
- [[Tips bilangan dan teori bilangan]]
- [[Trik dan Tips Matematika|Trik pembagian persen dan desimal]]

## Sumber rujukan

- [Khan Academy - Distributive property review](https://www.khanacademy.org/math/arithmetic-home/multiply-divide/properties-of-multiplication/a/distributive-property-review)
- [Khan Academy - Converting between percents, fractions, and decimals](https://www.khanacademy.org/math/cc-sixth-grade-math/x0267d782%3Acc-6th-rates-and-percentages/x0267d782%3Aequivalent-representations-of-percent-problems/a/converting-between-percents-fractions-decimals)

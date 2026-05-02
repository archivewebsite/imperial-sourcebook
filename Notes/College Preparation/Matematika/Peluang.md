---
title: Peluang
mata_pelajaran: Matematika
tanggal: 29 Agustus 2025
materi: Peluang
tags:
  - matematika
  - peluang
  - aturan-pencacahan
  - faktorial
  - kombinasi
  - permutasi
  - teori-peluang
  - kejadian-majemuk
---

# Peluang

## A. Aturan Pencacahan

Jika suatu kejadian dapat terjadi dalam `m` cara, kemudian diikuti oleh kejadian lain yang dapat terjadi dalam `n` cara, maka:

### 1. Aturan Perkalian

> Kata kunci: **dan**

Jika kedua kejadian tersebut **dapat terjadi secara bersamaan**, maka:

$$
\text{Banyak cara} = m \cdot n
$$

---

### 2. Aturan Penjumlahan

> Kata kunci: **atau**

Jika kedua kejadian tersebut **tidak dapat terjadi secara bersamaan**, maka:

$$
\text{Banyak cara} = m+n
$$

---

## B. Faktorial

Faktorial ditulis sebagai:

$$
n! = n(n-1)(n-2)\cdots 3 \cdot 2 \cdot 1
$$

Bentuk lain:

$$
n! = n(n-1)!
$$

$$
n! = n(n-1)(n-2)!
$$

### Contoh

$$
3! = 3 \cdot 2 \cdot 1 = 6
$$

$$
4! = 4 \cdot 3 \cdot 2 \cdot 1 = 24
$$

$$
5! = 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 120
$$

$$
5! = 5 \cdot 4!
$$

$$
5! = 5 \cdot 4 \cdot 3!
$$

$$
5! = 20 \cdot 6 = 120
$$

$$
\frac{5!}{3!}
=
\frac{5 \cdot 4 \cdot 3!}{3!}
=
20
$$

$$
1! = 1
$$

$$
0! = 1
$$

### Pembuktian $0! = 1$

$$
1! = 1 \cdot 0!
$$

$$
1! = 0!
$$

$$
0! = 1
$$

---

## C. Kombinasi

Notasi:

$$
{}^nC_r = C(n,r)
$$

Kombinasi `r` unsur dari `n` unsur, ditulis ${}^nC_r$, adalah banyak cara **mengelompokkan** `r` unsur yang diambil dari `n` unsur yang tersedia **tanpa memperhatikan urutan atau susunan**.

Rumus:

$$
{}^nC_r = \frac{n!}{r!(n-r)!}
$$

---

## D. Permutasi

Notasi:

$$
{}^nP_r = P(n,r)
$$

Permutasi `r` unsur dari `n` unsur, ditulis ${}^nP_r$, adalah banyak cara **menyusun** `r` unsur yang diambil dari `n` unsur yang tersedia **dengan memperhatikan urutan atau susunan**.

Rumus:

$$
{}^nP_r = \frac{n!}{(n-r)!}
$$

---

# Perbedaan Kombinasi dengan Permutasi

Dari 4 huruf:

$$
a,b,c,d
$$

akan diambil 3 huruf.

## Kombinasi

Kombinasi tidak memperhatikan urutan.

| Kombinasi |
|---|
| abc |
| abd |
| acd |
| bcd |

## Permutasi

Permutasi memperhatikan urutan.

| Kombinasi Dasar | Susunan Permutasi |
|---|---|
| abc | abc, acb, bac, bca, cab, cba |
| abd | abd, adb, bad, bda, dab, dba |
| acd | acd, adc, cad, cda, dac, dca |
| bcd | bcd, bdc, cbd, cdb, dbc, dcb |

---

# Jenis-Jenis Permutasi

## 1. Permutasi Siklis

Banyak susunan `n` unsur yang disusun secara melingkar adalah:

$$
(n-1)!
$$

---

## 2. Permutasi Beberapa Unsur yang Sama

Banyak susunan `n` unsur yang di antaranya terdapat:

- $n_1$ unsur sejenis I
- $n_2$ unsur sejenis II
- $n_3$ unsur sejenis III

adalah:

$$
{}^nP_{n_1,n_2,n_3}
=
\frac{n!}{n_1! \cdot n_2! \cdot n_3!}
$$

---

# Contoh Soal Aturan Pencacahan, Kombinasi, dan Permutasi

## Contoh 1

Andi mempunyai:

- 4 jaket
- 3 sweater
- 5 celana jeans

Tentukan:

### a. Banyak cara Andi memakai atasan

Atasan dapat berupa jaket atau sweater.

$$
4+3=7
$$

Jadi:

$$
7 \text{ cara}
$$

### b. Banyak cara Andi berpakaian

Atasan ada 7 pilihan dan celana jeans ada 5 pilihan.

$$
7 \cdot 5 = 35
$$

Jadi:

$$
35 \text{ cara}
$$

---

## Contoh 2

Banyak bilangan yang terdiri dari 4 angka berbeda yang dapat disusun dari angka:

$$
0,1,2,3,4,5
$$

jika nilainya lebih dari 3000 adalah ....

Karena bilangan harus lebih dari 3000, angka ribuan dapat dipilih dari:

$$
3,4,5
$$

Susunan banyak pilihan:

| Posisi | Banyak Pilihan |
|---|---:|
| Ribuan | 3 |
| Ratusan | 5 |
| Puluhan | 4 |
| Satuan | 3 |

Maka:

$$
3 \cdot 5 \cdot 4 \cdot 3 = 180
$$

Jadi:

$$
180 \text{ bilangan}
$$

---

## Contoh 3

Banyak bilangan ratusan yang terdiri dari 3 angka berbeda yang dapat disusun dari angka:

$$
1,2,3,4,5
$$

jika harus bernilai genap adalah ....

Agar bernilai genap, angka satuan harus:

$$
2 \text{ atau } 4
$$

Pada papan ditulis:

$$
3 \cdot 4 \cdot 2 = 24
$$

Jadi:

$$
24 \text{ bilangan}
$$

> [!note]
> Secara logika pencacahan, pilihan dapat dipahami sebagai: satuan 2 pilihan, lalu dua posisi lain diisi dari sisa angka. Hasil akhirnya tetap $24$.

---

## Contoh 4

Banyak bilangan ratusan dengan angka-angka berlainan yang nilainya antara 300 dan 600 yang dapat disusun dari angka:

$$
2,3,4,5,6,7
$$

jika harus bernilai ganjil adalah ....

Bilangan harus berada antara 300 dan 600, sehingga angka ratusan yang mungkin:

$$
3,4,5
$$

Bilangan harus ganjil, sehingga angka satuan yang mungkin:

$$
3,5,7
$$

### Kasus 1: Ratusan 3 atau 5

Pada papan ditulis:

$$
2 \cdot 4 \cdot 2 = 16
$$

### Kasus 2: Ratusan 4

Pada papan ditulis:

$$
1 \cdot 4 \cdot 3 = 12
$$

Total:

$$
16+12=28
$$

Jadi:

$$
28 \text{ bilangan}
$$

---

## Contoh 5

Dalam sebuah ruangan terdapat 10 orang. Jika mereka saling bersalaman, maka banyak salaman yang terjadi adalah ....

Karena salaman:

$$
a \to b
$$

sama dengan:

$$
b \to a
$$

maka digunakan **kombinasi**.

$$
{}^{10}C_2
=
\frac{10!}{2!(10-2)!}
$$

$$
=
\frac{10!}{2! \cdot 8!}
$$

$$
=
\frac{10 \cdot 9 \cdot 8!}{2 \cdot 1 \cdot 8!}
$$

$$
=
45
$$

Jadi:

$$
45 \text{ cara}
$$

---

## Contoh 6

Dari 8 orang perwakilan kelas, akan dipilih 3 orang pengurus OSIS yang terdiri dari:

- ketua
- sekretaris
- bendahara

Banyak cara memilih adalah ....

Karena jabatan berbeda, maka digunakan **permutasi**.

$$
{}^8P_3
=
\frac{8!}{(8-3)!}
$$

$$
=
\frac{8!}{5!}
$$

$$
=
\frac{8 \cdot 7 \cdot 6 \cdot 5!}{5!}
$$

$$
=
336
$$

Jadi:

$$
336 \text{ cara}
$$

---

# E. Teori Peluang

## 1. Peluang Teoritis

Rumus:

$$
P(A) = \frac{n(A)}{n(S)}
$$

Keterangan:

| Simbol | Keterangan |
|---|---|
| $P(A)$ | Peluang kejadian A |
| $n(A)$ | Banyak kejadian A |
| $n(S)$ | Banyak anggota ruang sampel |

### Banyak Anggota Ruang Sampel

| Percobaan | Banyak Anggota Ruang Sampel |
|---|---:|
| Dadu | $n(S)=6^n$ |
| Koin | $n(S)=2^n$ |
| Kartu bridge | $n(S)=52$ |

Keterangan:

$$
n = \text{banyak objek}
$$

---

## 2. Kisaran Nilai Peluang

Nilai peluang berada pada interval:

$$
0 \leq P(A) \leq 1
$$

Keterangan:

| Nilai | Arti |
|---|---|
| $P(A)=0$ | Mustahil terjadi |
| $P(A)=1$ | Pasti terjadi |

---

## 3. Peluang Komplemen

Rumus:

$$
P(A^c)=1-P(A)
$$

Keterangan:

$$
P(A^c)=\text{peluang tidak terjadinya kejadian A}
$$

---

## 4. Peluang Empiris

Peluang empiris adalah peluang berdasarkan suatu percobaan.

Rumus:

$$
P(A)=\frac{f(A)}{n}
$$

Keterangan:

| Simbol | Keterangan |
|---|---|
| $f(A)$ | Frekuensi kejadian A terjadi |
| $n$ | Banyak percobaan |

---

## 5. Frekuensi Harapan

Rumus:

$$
F_H = P(A) \cdot n
$$

Keterangan:

$$
F_H = \text{frekuensi harapan}
$$

---

# F. Peluang Kejadian Majemuk

Jika ada 2 kejadian atau lebih sekaligus terjadi.

---

## 1. Kejadian Tidak Saling Lepas

Rumus:

$$
P(A \cup B)
=
P(A)+P(B)-P(A \cap B)
$$

Keterangan:

| Simbol | Keterangan |
|---|---|
| $P(A \cup B)$ | Peluang kejadian A atau B |
| $P(A \cap B)$ | Peluang kejadian A dan B |

---

## 2. Kejadian Saling Lepas

Rumus:

$$
P(A \cap B)=0
$$

$$
P(A \cup B)=P(A)+P(B)
$$

---

## 3. Kejadian Saling Bebas

Rumus:

$$
P(A \cap B)=P(A) \cdot P(B)
$$

---

## 4. Kejadian Bersyarat

Rumus:

$$
P(A|B)
=
\frac{P(A \cap B)}{P(B)}
$$

Keterangan:

$$
P(A|B)
=
\text{peluang kejadian A dengan syarat B telah terjadi}
$$

---

## 5. Kejadian Binomial

Jika ada suatu kejadian yang hanya memiliki 2 kemungkinan, yaitu:

- berhasil
- gagal

dan dilakukan sebanyak `n` kali, maka peluang berhasil sebanyak `r` kali adalah:

$$
P(X=r)
=
{}^nC_r \cdot p^r \cdot (1-p)^{n-r}
$$

Keterangan:

| Simbol | Keterangan |
|---|---|
| $p$ | Peluang berhasil |
| $1-p$ | Peluang gagal |
| $n$ | Banyak percobaan |
| $r$ | Banyak keberhasilan |

---

# Contoh Soal Peluang Kejadian Majemuk

## Contoh 1

Sebuah dadu bermata 6 dilempar. Peluang mendapat mata dadu genap atau faktor dari 6 adalah ....

Ruang sampel:

$$
S=\{1,2,3,4,5,6\}
$$

$$
n(S)=6
$$

Misalkan:

$$
A=\text{kejadian muncul mata dadu genap}
$$

$$
A=\{2,4,6\}
$$

$$
n(A)=3
$$

Misalkan:

$$
B=\text{kejadian muncul faktor dari 6}
$$

$$
B=\{1,2,3,6\}
$$

$$
n(B)=4
$$

Irisan:

$$
A \cap B=\{2,6\}
$$

$$
n(A \cap B)=2
$$

Maka:

$$
P(A \cup B)
=
P(A)+P(B)-P(A \cap B)
$$

$$
=
\frac{3}{6}
+
\frac{4}{6}
-
\frac{2}{6}
$$

$$
=
\frac{5}{6}
$$

Jawaban:

$$
\frac{5}{6}
$$

---

## Contoh 2

Dua dadu dilempar sekaligus. Peluang muncul jumlah kedua dadu 4 atau 9 adalah ....

Ruang sampel:

$$
n(S)=6^2=36
$$

Misalkan:

$$
A=\text{kejadian jumlah kedua dadu 4}
$$

$$
A=\{(1,3),(2,2),(3,1)\}
$$

$$
n(A)=3
$$

Misalkan:

$$
B=\text{kejadian jumlah kedua dadu 9}
$$

$$
B=\{(3,6),(4,5),(5,4),(6,3)\}
$$

$$
n(B)=4
$$

Karena kejadian jumlah 4 dan jumlah 9 saling lepas, maka:

$$
P(A \cup B)=P(A)+P(B)
$$

$$
=
\frac{3}{36}
+
\frac{4}{36}
$$

$$
=
\frac{7}{36}
$$

Jawaban:

$$
\frac{7}{36}
$$

---

## Contoh 3

Pada pelemparan 1 dadu dan 1 koin, peluang muncul angka pada koin dan faktor dari 6 pada dadu adalah ....

Untuk koin:

$$
S=\{A,G\}
$$

$$
n(S)=2
$$

$$
P(A)=\frac{1}{2}
$$

Untuk dadu:

$$
S=\{1,2,3,4,5,6\}
$$

$$
n(S)=6
$$

Misalkan:

$$
B=\text{kejadian muncul faktor dari 6}
$$

$$
B=\{1,2,3,6\}
$$

$$
n(B)=4
$$

$$
P(B)=\frac{4}{6}
$$

Karena kejadian pada koin dan dadu saling bebas:

$$
P(A \cap B)=P(A) \cdot P(B)
$$

$$
=
\frac{1}{2}
\cdot
\frac{4}{6}
$$

$$
=
\frac{4}{12}
$$

Jawaban pada papan:

$$
\frac{4}{12}
$$

> [!note]
> Bentuk sederhana dari $\frac{4}{12}$ adalah $\frac{1}{3}$, tetapi papan menuliskan $\frac{4}{12}$.
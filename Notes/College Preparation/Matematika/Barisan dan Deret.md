## Barisan Aritmatika

Barisan aritmatika adalah barisan bilangan yang memiliki **selisih tetap** antar suku berurutan.

### Rumus beda

$$ b = U_n - U_{n-1} $$

Keterangan variabel:

- $b$ = beda atau selisih tetap
- $U_n$ = suku ke-$n$
- $U_{n-1}$ = suku sebelum suku ke-$n$

### Rumus suku ke-$n$

$$ U_n = a + (n-1)b $$

Keterangan variabel:

- $U_n$ = suku ke-$n$
- $a$ = suku pertama
- $n$ = nomor suku
- $b$ = beda

### Rumus suku tengah

Jika jumlah suku ganjil, maka: $$ U_t = \frac{a + U_n}{2} $$

Keterangan variabel:

- $U_t$ = suku tengah
- $a$ = suku pertama
- $U_n$ = suku terakhir

### Menentukan beda dari dua suku

Jika diketahui $U_p$ dan $U_q$, maka: $$ b = \frac{U_q - U_p}{q - p} $$

Keterangan variabel:

- $b$ = beda
- $U_p$ = suku ke-$p$
- $U_q$ = suku ke-$q$
- $p, q$ = nomor suku

### Menentukan suku pertama

$$ a = U_n - (n-1)b $$

Keterangan variabel:

- $a$ = suku pertama
- $U_n$ = suku ke-$n$
- $n$ = nomor suku
- $b$ = beda

---

## Deret Aritmatika

Deret aritmatika adalah **jumlah suku-suku** pada barisan aritmatika.

### Bentuk umum

$$ S_n = a + (a+b) + (a+2b) + \cdots + U_n $$

Keterangan variabel:

- $S_n$ = jumlah $n$ suku pertama
- $a$ = suku pertama
- $b$ = beda
- $U_n$ = suku ke-$n$

### Rumus jumlah $n$ suku pertama

$$ S_n = \frac{n}{2}(a + U_n) $$

Keterangan variabel:

- $S_n$ = jumlah $n$ suku pertama
- $n$ = banyak suku
- $a$ = suku pertama
- $U_n$ = suku ke-$n$

### Rumus lain jumlah $n$ suku pertama

$$ S_n = \frac{n}{2}(2a + (n-1)b) $$

Keterangan variabel:

- $S_n$ = jumlah $n$ suku pertama
- $n$ = banyak suku
- $a$ = suku pertama
- $b$ = beda

### Hubungan suku dan jumlah

$$ U_n = S_n - S_{n-1} $$

Keterangan variabel:

- $U_n$ = suku ke-$n$
- $S_n$ = jumlah $n$ suku pertama
- $S_{n-1}$ = jumlah $(n-1)$ suku pertama

---

## Barisan Geometri

Barisan geometri adalah barisan bilangan yang memiliki **rasio tetap** antar suku berurutan.

### Rumus rasio

$$ r = \frac{U_n}{U_{n-1}} $$

Keterangan variabel:

- $r$ = rasio
- $U_n$ = suku ke-$n$
- $U_{n-1}$ = suku sebelum suku ke-$n$

### Rumus suku ke-$n$

$$ U_n = a \cdot r^{n-1} $$

Keterangan variabel:

- $U_n$ = suku ke-$n$
- $a$ = suku pertama
- $r$ = rasio
- $n$ = nomor suku

### Menentukan rasio dari dua suku

Jika diketahui $U_p$ dan $U_q$, maka: $$ r = \left(\frac{U_q}{U_p}\right)^{\frac{1}{q-p}} $$

Keterangan variabel:

- $r$ = rasio
- $U_p$ = suku ke-$p$
- $U_q$ = suku ke-$q$
- $p, q$ = nomor suku

### Menentukan suku pertama

$$ a = \frac{U_n}{r^{n-1}} $$

Keterangan variabel:

- $a$ = suku pertama
- $U_n$ = suku ke-$n$
- $r$ = rasio
- $n$ = nomor suku

### Sifat tiga suku berurutan

Jika $x$, $y$, dan $z$ adalah tiga suku berurutan dalam barisan geometri, maka: $$ y^2 = xz $$

Keterangan variabel:

- $x$ = suku pertama
- $y$ = suku kedua
- $z$ = suku ketiga

---

## Deret Geometri

Deret geometri adalah **jumlah suku-suku** pada barisan geometri.

### Bentuk umum

$$ S_n = a + ar + ar^2 + ar^3 + \cdots + ar^{n-1} $$

Keterangan variabel:

- $S_n$ = jumlah $n$ suku pertama
- $a$ = suku pertama
- $r$ = rasio
- $n$ = banyak suku

### Rumus jumlah $n$ suku pertama jika $r \ne 1$

$$ S_n = \frac{a(r^n - 1)}{r - 1} $$

Atau dapat ditulis juga: $$ S_n = \frac{a(1 - r^n)}{1 - r} $$

Keterangan variabel:

- $S_n$ = jumlah $n$ suku pertama
- $a$ = suku pertama
- $r$ = rasio
- $n$ = banyak suku

### Kasus khusus jika $r = 1$

$$ S_n = na $$

Keterangan variabel:

- $S_n$ = jumlah $n$ suku pertama
- $n$ = banyak suku
- $a$ = suku pertama

### Hubungan suku dan jumlah

$$ U_n = S_n - S_{n-1} $$

Keterangan variabel:

- $U_n$ = suku ke-$n$
- $S_n$ = jumlah $n$ suku pertama
- $S_{n-1}$ = jumlah $(n-1)$ suku pertama

---

## Deret Geometri Tak Hingga

Deret geometri tak hingga memiliki jumlah jika memenuhi syarat konvergen.

### Syarat konvergen

$$ |r| < 1 $$

Keterangan variabel:

- $r$ = rasio
- $|r|$ = nilai mutlak rasio

### Rumus jumlah tak hingga

$$ S_{\infty} = \frac{a}{1-r} $$

Keterangan variabel:

- $S_{\infty}$ = jumlah deret geometri tak hingga
- $a$ = suku pertama
- $r$ = rasio, dengan syarat $|r| < 1$

---

## Rumus Terkait Lainnya

### Sisipan bilangan pada barisan aritmatika

Jika disisipkan $k$ bilangan antara $p$ dan $q$, maka: $$ b = \frac{q-p}{k+1} $$

Keterangan variabel:

- $b$ = beda
- $p$ = bilangan awal
- $q$ = bilangan akhir
- $k$ = banyak bilangan yang disisipkan

### Sisipan bilangan pada barisan geometri

Jika disisipkan $k$ bilangan antara $p$ dan $q$, maka: $$ r = \left(\frac{q}{p}\right)^{\frac{1}{k+1}} $$

Keterangan variabel:

- $r$ = rasio
- $p$ = bilangan awal
- $q$ = bilangan akhir
- $k$ = banyak bilangan yang disisipkan

### Rata-rata aritmatika dua bilangan

$$ A = \frac{x+y}{2} $$

Keterangan variabel:

- $A$ = rata-rata aritmatika
- $x, y$ = dua bilangan

### Rata-rata geometri dua bilangan

$$ G = \sqrt{xy} $$

Keterangan variabel:

- $G$ = rata-rata geometri
- $x, y$ = dua bilangan

---

## Ringkasan Cepat

### Barisan Aritmatika

$$ U_n = a + (n-1)b $$

### Deret Aritmatika

$$ S_n = \frac{n}{2}(a + U_n) $$

$$ S_n = \frac{n}{2}(2a + (n-1)b) $$

### Barisan Geometri

$$ U_n = a \cdot r^{n-1} $$

### Deret Geometri

$$ S_n = \frac{a(r^n - 1)}{r - 1}, \quad r \ne 1 $$

### Deret Geometri Tak Hingga

$$ S_{\infty} = \frac{a}{1-r}, \quad |r| < 1 $$

---

## Simbol yang Digunakan

- $a$ = suku pertama
- $b$ = beda pada barisan aritmatika
- $r$ = rasio pada barisan geometri
- $U_n$ = suku ke-$n$
- $S_n$ = jumlah $n$ suku pertama
- $S_{\infty}$ = jumlah tak hingga
- $n$ = nomor suku atau banyak suku
- $p, q$ = posisi atau nilai tertentu dalam barisan
- $x, y, z$ = variabel bilangan atau suku
- $k$ = banyak bilangan yang disisipkan
- $U_t$ = suku tengah
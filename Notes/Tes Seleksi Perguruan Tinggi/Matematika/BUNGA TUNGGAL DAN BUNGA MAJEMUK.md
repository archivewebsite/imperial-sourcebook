## BAGIAN 1 — BUNGA TUNGGAL

### Pengertian

Bunga tunggal adalah bunga yang besarnya selalu dihitung berdasarkan **modal awal** dan **tidak berubah** dari periode ke periode. Bunga tidak ditambahkan ke pokok untuk periode berikutnya.

---

### Rumus Bunga Tunggal

**Rumus dasar:**

$$I = p \times M_0$$

**Rumus bunga dalam jangka waktu tertentu:**

| Satuan Waktu | Rumus |
|:---|:---|
| $t$ tahun | $I = p \times M_0 \times t$ |
| $b$ bulan | $I = p \times M_0 \times \dfrac{b}{12}$ |
| $h$ hari (dasar 360) | $I = p \times M_0 \times \dfrac{h}{360}$ |
| $h$ hari (dasar 365) | $I = p \times M_0 \times \dfrac{h}{365}$ |
| $h$ hari (dasar 366) | $I = p \times M_0 \times \dfrac{h}{366}$ |

> Penggunaan 360, 365, atau 366 tergantung pada ketentuan soal. Umumnya dalam soal SNBT digunakan 360.

**Rumus total tabungan setelah dikenai bunga:**

$$M_n = M_0 (1 + t \cdot p)$$

$$M_n = M_0 \left(1 + \frac{b}{12} \cdot p\right)$$

$$M_n = M_0 \left(1 + \frac{h}{360} \cdot p\right)$$

---

### Keterangan Variabel

| Simbol | Keterangan |
|:---:|:---|
| $I$ | Besar bunga |
| $p$ | Suku bunga dalam desimal (% dibagi 100) |
| $M_0$ | Jumlah tabungan / modal awal |
| $M_n$ | Jumlah tabungan pada waktu ke-$n$ |
| $t$ | Jumlah tahun |
| $b$ | Jumlah bulan |
| $h$ | Jumlah hari |

---

### Contoh Soal — Bunga Tunggal

**Contoh 1**

Sutris memiliki tabungan sebesar Rp100.000,00, lalu tabungannya dikenai bunga sebesar 10%. Berapakah besar bunganya?

Diketahui: $p = 10\% = 0{,}1$; $M_0 = \text{Rp}100.000$

$$I = p \times M_0 = \frac{10}{100} \times 100.000 = \text{Rp}10.000$$

---

**Contoh 2**

Lolly menabung di bank sebesar Rp45.000.000. Bunga dari bank 10% per tahun. Setelah 4 tahun menabung, berapa total bunga yang didapatkan Lolly?

Diketahui: $M_0 = \text{Rp}45.000.000$; $p = 0{,}1$; $t = 4$

$$I = p \times M_0 \times t = \frac{10}{100} \times 45.000.000 \times 4 = \text{Rp}18.000.000$$

---

**Contoh 3**

Budi memiliki tabungan sebesar Rp10.000.000. Bank memberinya bunga 5% per tahun. Setelah 5 tahun, berapakah jumlah tabungan Budi?

Diketahui: $M_0 = \text{Rp}10.000.000$; $p = 0{,}05$; $t = 5$

$$M_n = M_0(1 + t \cdot p) = 10.000.000\left(1 + 5 \cdot \frac{5}{100}\right) = 10.000.000 \times 1{,}25 = \text{Rp}12.500.000$$

---

## BAGIAN 2 — BUNGA MAJEMUK

### Pengertian

Bunga majemuk adalah bunga yang besarnya **tidak sama setiap periode** karena bunga pada setiap periode ditambahkan ke pokok dan ikut dikenai bunga pada periode berikutnya. Bunga dihitung atas modal awal ditambah bunga yang telah terakumulasi.

Perbedaan kunci:
- Bunga tunggal: bunga selalu dihitung dari **modal awal**
- Bunga majemuk: bunga dihitung dari **modal awal + bunga yang sudah terkumpul**

---

### Rumus Bunga Majemuk

**Nilai akhir (future value):**

$$Na = Nt \cdot (1 + i)^n$$

**Besar bunga pada periode ke-$n$:**

$$i(n) = \left[(1+i)^n - (1+i)^{n-1}\right] \cdot Nt$$

**Rumus untuk berbagai frekuensi pembungaan:**

| Frekuensi | Rumus |
|:---|:---|
| Tahunan (1x/tahun) | $Na = Nt(1+i)^n$ |
| Semesteran (2x/tahun) | $Na = Nt\left(1+\dfrac{i}{2}\right)^{2n}$ |
| Kuartalan (4x/tahun) | $Na = Nt\left(1+\dfrac{i}{4}\right)^{4n}$ |
| Bulanan (12x/tahun) | $Na = Nt\left(1+\dfrac{i}{12}\right)^{12n}$ |

---

### Keterangan Variabel

| Simbol | Keterangan |
|:---:|:---|
| $Na$ | Nilai akhir (modal akhir) |
| $Nt$ | Nilai tunai (modal awal / present value) |
| $i$ | Suku bunga per periode dalam desimal |
| $n$ | Jangka waktu (jumlah periode) |

---

### Contoh Soal — Bunga Majemuk

**Contoh 1**

Dedy berinvestasi modal senilai Rp50.000.000 dengan bunga majemuk 5% per tahun. Berapakah modal di akhir tahun ketiga?

Diketahui: $Nt = \text{Rp}50.000.000$; $i = 0{,}05$; $n = 3$

$$Na = Nt \cdot (1+i)^n = 50.000.000 \cdot (1{,}05)^3 = 50.000.000 \times 1{,}158 = \text{Rp}57.900.000$$

---

**Contoh 2**

Elvi mendepositokan uang di bank sebesar Rp20.000.000 selama 10 tahun dengan suku bunga majemuk 7% per tahun. Berapakah besar bunga yang akan Elvi peroleh pada tahun ke-10?

Diketahui: $Nt = \text{Rp}20.000.000$; $i = 0{,}07$; $n = 10$

$$i(10) = \left[(1{,}07)^{10} - (1{,}07)^{9}\right] \times 20.000.000 = [1{,}967 - 1{,}838] \times 20.000.000 = \text{Rp}2.580.000$$

---

## BAGIAN 3 — PERBANDINGAN BUNGA TUNGGAL DAN BUNGA MAJEMUK

| Aspek | Bunga Tunggal | Bunga Majemuk |
|:---|:---|:---|
| Dasar perhitungan | Modal awal saja | Modal awal + bunga terakumulasi |
| Pola pertumbuhan | Linear | Eksponensial |
| Rumus utama | $I = p \times M_0 \times t$ | $Na = Nt(1+i)^n$ |
| Besar bunga tiap periode | Tetap | Bertambah setiap periode |
| Keuntungan jangka panjang | Lebih kecil | Lebih besar |

---

## BAGIAN 4 — TOPIK PENDUKUNG

### Nilai Sekarang / Present Value

Dari rumus bunga majemuk, dapat diturunkan rumus untuk mencari modal awal:

$$Nt = \frac{Na}{(1+i)^n}$$

Digunakan untuk menghitung berapa uang yang perlu diinvestasikan sekarang agar bernilai $Na$ di masa depan.

---

### Anuitas

Anuitas adalah pembayaran atau penerimaan dalam jumlah **tetap** yang dilakukan secara **berkala** dalam jangka waktu tertentu.

**Anuitas akhir** — pembayaran dilakukan di akhir setiap periode:

$$S = A \cdot \frac{(1+i)^n - 1}{i}$$

$$P = A \cdot \frac{1-(1+i)^{-n}}{i}$$

**Anuitas awal** — pembayaran dilakukan di awal setiap periode:

$$S_{\text{awal}} = S \cdot (1+i)$$

$$P_{\text{awal}} = P \cdot (1+i)$$

| Simbol | Keterangan |
|:---:|:---|
| $A$ | Besar angsuran per periode |
| $i$ | Suku bunga per periode |
| $n$ | Jumlah periode |
| $S$ | Nilai akhir anuitas |
| $P$ | Nilai sekarang anuitas |

---

## BAGIAN 5 — LATIHAN SOAL

### Tingkat Dasar

**Soal 1**

Rina menyimpan uang di bank sebesar Rp5.000.000 dengan bunga tunggal 8% per tahun. Berapa besar bunga yang diperoleh setelah 3 tahun?

<details>
<summary>Pembahasan</summary>

Diketahui: $M_0 = 5.000.000$; $p = 0{,}08$; $t = 3$

$$I = p \times M_0 \times t = 0{,}08 \times 5.000.000 \times 3 = \textbf{Rp1.200.000}$$
</details>

---

**Soal 2**

Seorang pedagang meminjam uang sebesar Rp2.000.000 dengan bunga tunggal 1,5% per bulan. Berapa total utang yang harus dibayar setelah 8 bulan?

<details>
<summary>Pembahasan</summary>

Diketahui: $M_0 = 2.000.000$; $p = 0{,}015$ per bulan; $b = 8$

$$M_n = M_0(1 + b \cdot p) = 2.000.000(1 + 8 \times 0{,}015) = 2.000.000 \times 1{,}12 = \textbf{Rp2.240.000}$$
</details>

---

**Soal 3**

Seseorang menyimpan Rp6.000.000 di bank dengan bunga tunggal. Setelah 4 tahun, uangnya menjadi Rp7.440.000. Berapakah suku bunga per tahun?

<details>
<summary>Pembahasan</summary>

$$7.440.000 = 6.000.000(1 + 4p) \implies 1{,}24 = 1 + 4p \implies p = 0{,}06 = \textbf{6\% per tahun}$$
</details>

---

### Tingkat Menengah

**Soal 4**

Dani menginvestasikan Rp15.000.000 dengan bunga majemuk 10% per tahun. Berapa nilai investasinya setelah 3 tahun? Gunakan $(1{,}1)^3 = 1{,}331$.

<details>
<summary>Pembahasan</summary>

$$Na = 15.000.000 \times (1{,}1)^3 = 15.000.000 \times 1{,}331 = \textbf{Rp19.965.000}$$
</details>

---

**Soal 5**

Sebuah bank menawarkan dua pilihan: (A) bunga tunggal 12% per tahun, dan (B) bunga majemuk 10% per tahun. Jika Ani menyimpan Rp10.000.000 selama 4 tahun, manakah pilihan yang lebih menguntungkan? Gunakan $(1{,}1)^4 = 1{,}4641$.

<details>
<summary>Pembahasan</summary>

Pilihan A (bunga tunggal):

$$M_n = 10.000.000(1 + 4 \times 0{,}12) = 10.000.000 \times 1{,}48 = \text{Rp}14.800.000$$

Pilihan B (bunga majemuk):

$$Na = 10.000.000 \times (1{,}1)^4 = 10.000.000 \times 1{,}4641 = \text{Rp}14.641.000$$

**Kesimpulan:** Pilihan A lebih menguntungkan karena Rp14.800.000 > Rp14.641.000.
</details>

---

**Soal 6**

Seseorang ingin memiliki uang sebesar Rp33.100.000 setelah 3 tahun. Jika bunga majemuk yang ditawarkan bank adalah 10% per tahun, berapakah uang yang harus ditabung sekarang? Gunakan $(1{,}1)^3 = 1{,}331$.

<details>
<summary>Pembahasan</summary>

$$Nt = \frac{Na}{(1+i)^n} = \frac{33.100.000}{1{,}331} \approx \textbf{Rp24.869.271}$$
</details>

---

**Soal 7**

Seorang nasabah menyimpan Rp8.000.000 di bank dengan bunga majemuk 6% per tahun. Berapa besar bunga yang diperoleh pada tahun ke-2 saja? Gunakan $(1{,}06)^2 = 1{,}1236$ dan $(1{,}06)^1 = 1{,}06$.

<details>
<summary>Pembahasan</summary>

$$i(2) = \left[(1{,}06)^2 - (1{,}06)^1\right] \times 8.000.000 = (1{,}1236 - 1{,}06) \times 8.000.000 = 0{,}0636 \times 8.000.000 = \textbf{Rp508.800}$$
</details>

---

### Tingkat Tinggi (SNBT/SBMPTN)

**Soal 8**

Seorang investor menanamkan modal Rp20.000.000 dengan bunga majemuk 15% per tahun. Setelah berapa tahun modal investor akan lebih dari dua kali lipat modal awal? Gunakan $\log 1{,}15 = 0{,}0607$ dan $\log 2 = 0{,}3010$.

<details>
<summary>Pembahasan</summary>

$$Na > 2 \times Nt \implies (1{,}15)^n > 2$$

$$n \cdot \log 1{,}15 > \log 2 \implies n > \frac{0{,}3010}{0{,}0607} \approx 4{,}96$$

Jadi, setelah minimal **5 tahun**, modal menjadi lebih dari dua kali lipat.
</details>

---

**Soal 9**

Setiap akhir tahun, Banu menyetor Rp3.000.000 ke rekening tabungan berbunga majemuk 8% per tahun selama 5 tahun. Berapa total nilai tabungannya pada akhir tahun ke-5? Gunakan $(1{,}08)^5 = 1{,}469$.

<details>
<summary>Pembahasan</summary>

Ini adalah soal anuitas akhir.

$$S = A \cdot \frac{(1+i)^n - 1}{i} = 3.000.000 \times \frac{1{,}469 - 1}{0{,}08} = 3.000.000 \times 5{,}8625 = \textbf{Rp17.587.500}$$
</details>

---

**Soal 10**

Pak Andi meminjam uang di bank sebesar Rp50.000.000 dengan bunga majemuk 12% per tahun dan akan dicicil selama 5 tahun. Berapa besar cicilan per tahun yang harus dibayar? Gunakan $(1{,}12)^5 = 1{,}7623$.

<details>
<summary>Pembahasan</summary>

$$50.000.000 = A \times \frac{1 - (1{,}12)^{-5}}{0{,}12} = A \times \frac{1 - \dfrac{1}{1{,}7623}}{0{,}12} = A \times \frac{0{,}4325}{0{,}12} = A \times 3{,}6042$$

$$A = \frac{50.000.000}{3{,}6042} \approx \textbf{Rp13.873.000}$$
</details>

---

**Soal 11**

Tika menabung Rp10.000.000 dengan bunga tunggal selama 3 tahun dan mendapat bunga Rp3.600.000. Dika menginvestasikan jumlah yang sama dengan bunga majemuk 10% per tahun selama 3 tahun. Gunakan $(1{,}1)^3 = 1{,}331$.

(a) Berapakah suku bunga tabungan Tika per tahun?

(b) Berapakah nilai akhir investasi Dika?

(c) Siapakah yang mendapatkan keuntungan lebih besar?

<details>
<summary>Pembahasan</summary>

**(a)**

$$3.600.000 = p \times 10.000.000 \times 3 \implies p = \frac{3.600.000}{30.000.000} = 0{,}12 = \textbf{12\% per tahun}$$

**(b)**

$$Na = 10.000.000 \times (1{,}1)^3 = 10.000.000 \times 1{,}331 = \text{Rp}13.310.000$$

Keuntungan Dika $= 13.310.000 - 10.000.000 = \text{Rp}3.310.000$

**(c)**

- Keuntungan Tika = Rp3.600.000
- Keuntungan Dika = Rp3.310.000

**Tika mendapatkan keuntungan lebih besar** selisih Rp290.000.
</details>

---

## RINGKASAN RUMUS

**Bunga Tunggal**

| Tujuan | Rumus |
|:---|:---|
| Bunga (tanpa waktu) | $I = p \times M_0$ |
| Bunga selama $t$ tahun | $I = p \times M_0 \times t$ |
| Bunga selama $b$ bulan | $I = p \times M_0 \times \dfrac{b}{12}$ |
| Bunga selama $h$ hari | $I = p \times M_0 \times \dfrac{h}{360}$ |
| Total tabungan | $M_n = M_0(1 + t \cdot p)$ |

**Bunga Majemuk**

| Tujuan | Rumus |
|:---|:---|
| Nilai akhir | $Na = Nt(1+i)^n$ |
| Nilai sekarang | $Nt = \dfrac{Na}{(1+i)^n}$ |
| Bunga pada periode ke-$n$ | $i(n) = [(1+i)^n - (1+i)^{n-1}] \times Nt$ |
| Mencari $n$ | $n = \dfrac{\log(Na/Nt)}{\log(1+i)}$ |

**Anuitas**

| Tujuan | Rumus |
|:---|:---|
| Nilai akhir anuitas | $S = A \cdot \dfrac{(1+i)^n - 1}{i}$ |
| Nilai sekarang anuitas | $P = A \cdot \dfrac{1-(1+i)^{-n}}{i}$ |

---

## TIPS UNTUK UJIAN

1. Pastikan satuan bunga dan waktu konsisten — bunga per tahun harus dipasangkan dengan waktu dalam tahun.
2. Konversi persen ke desimal sebelum menghitung: $10\% = 0{,}10$.
3. Bedakan dengan teliti apakah soal menanyakan **besar bunga** saja atau **total tabungan**.
4. Untuk mencari $n$ pada bunga majemuk, gunakan logaritma.
5. Bunga majemuk tumbuh secara eksponensial — untuk jangka panjang, nilainya jauh melampaui bunga tunggal meskipun persentasenya lebih kecil.
6. Pada soal anuitas, perhatikan apakah pembayaran dilakukan di **awal** atau **akhir** periode.

---

*Catatan dibuat berdasarkan materi dari @privatalfaiz*
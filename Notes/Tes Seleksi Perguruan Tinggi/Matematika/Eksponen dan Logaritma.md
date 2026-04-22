**Sumber:** Cerdas Matematika  
**Struktur:** Selaras dengan bab “Eksponen dan Logaritma” pada file referensi.

## 1. Eksponen

### A. Pengertian Eksponen
Eksponen adalah bentuk perpangkatan yang menyatakan perkalian berulang.

**Bentuk umum:**  
$$a^n = a \times a \times a \times \dots \times a$$ (sebanyak \(n\) faktor)

**Keterangan:**  
- \(a\) = bilangan pokok / basis  
- \(n\) = eksponen / pangkat  

**Contoh:**  
- \(2^4 = 2 \times 2 \times 2 \times 2 = 16\)  
- \(5^3 = 5 \times 5 \times 5 = 125\)

### B. Sifat-Sifat Eksponen
Untuk nilai yang memenuhi syarat operasinya, sifat-sifat penting eksponen adalah:

1. \(a^m \times a^n = a^{m+n}\)  
2. \(a^m / a^n = a^{m-n}\), dengan \(a \neq 0\)  
3. \(a^n \times b^n = (ab)^n\)  
4. \(a^n / b^n = (a/b)^n\), dengan \(b \neq 0\)  
5. \((a^m)^n = a^{mn}\)  
6. \((ab)^n = a^n b^n\)  
7. \(a^0 = 1\), dengan \(a \neq 0\)  
8. \(a^{-n} = 1 / a^n\)  
9. \(a^{m/n} = \sqrt[n]{a^m}\)

**Catatan penting:**  
- Sifat nomor 3 dan 6 pada dasarnya ekuivalen (hanya urutan penulisan berbeda).  
- **Hati-hati:** \(a^m + a^n\) **tidak** dapat disederhanakan menjadi \(a^{m+n}\).

### C. Fungsi Eksponen
Bentuk umum fungsi eksponen:  
$$y = a^{f(x)}$$  
(variabel berada pada pangkat).

**Bentuk yang sering digunakan:**  
- \(y = a^x\)  
- \(y = k \cdot a^x\), dengan \(k \neq 0\)

**Syarat umum:**  
- \(a > 0\)  
- \(a \neq 1\)

**Gagasan penting:**  
- Jika \(a > 1\): fungsi menunjukkan **pertumbuhan eksponensial**.  
- Jika \(0 < a < 1\): fungsi menunjukkan **peluruhan eksponensial**.

### D. Persamaan Eksponen
Bentuk-bentuk utama:

1. Jika \(a^{f(x)} = a^n\), maka \(f(x) = n\).  
2. Jika \(a^{f(x)} = a^{g(x)}\), maka \(f(x) = g(x)\).  
3. Jika \(f(x)^{g(x)} = f(x)^{h(x)}\), maka \(g(x) = h(x)\) (dengan syarat basis valid).  
4. Jika \(f(x)^{g(x)} = h(x)^{g(x)}\), maka \(f(x) = h(x)\) (dengan syarat pangkat sama).  
5. Jika basis belum sama, ubah bentuk atau gunakan logaritma.

**Tips penyelesaian:**  
- Samakan bilangan pokok bila memungkinkan.  
- Sederhanakan dengan sifat eksponen.  
- Jika perlu, ubah ke bentuk logaritma.

**Catatan akurasi:**  
Pola \(f(x)^{g(x)} = 1\) tidak selalu berarti \(f(x) = 1\); bisa juga \(g(x) = 0\) atau kasus khusus lain. Harus dicek domain dan syarat.

### E. Pertidaksamaan Eksponen
**Aturan utama:**

- **Jika \(a > 1\):**  
  \(a^{f(x)} > a^{g(x)}\) \(\implies\) \(f(x) > g(x)\)  
  \(a^{f(x)} < a^{g(x)}\) \(\implies\) \(f(x) < g(x)\)

- **Jika \(0 < a < 1\):**  
  \(a^{f(x)} > a^{g(x)}\) \(\implies\) \(f(x) < g(x)\)  
  \(a^{f(x)} < a^{g(x)}\) \(\implies\) \(f(x) > g(x)\)

**Inti:**  
- Basis \(> 1\) → tanda pertidaksamaan **tetap**.  
- Basis \(0 < a < 1\) → tanda pertidaksamaan **berbalik**.

## 2. Logaritma

### A. Pengertian Logaritma
Logaritma adalah invers (kebalikan) dari eksponen.

**Hubungan dasar:**  
$$\log_a b = c \quad \Leftrightarrow \quad a^c = b$$

**Keterangan:**  
- \(a\) = basis logaritma  
- \(b\) = numerus  
- \(c\) = hasil logaritma  

**Syarat:**  
- \(a > 0\), \(a \neq 1\)  
- \(b > 0\)

**Contoh:**  
- \(\log_2 8 = 3\) karena \(2^3 = 8\)  
- \(\log_3 81 = 4\) karena \(3^4 = 81\)

### B. Logaritma Umum
Jika basis adalah 10, basis tidak ditulis:  
$$\log x \quad \text{artinya} \quad \log_{10} x$$

### C. Sifat-Sifat Logaritma

1. \(\log_a a = 1\)  
2. \(\log_a 1 = 0\)  
3. \(a^{\log_a b} = b\)  
4. \(\log_a (a^c) = c\)  
5. \(\log_a (bc) = \log_a b + \log_a c\)  
6. \(\log_a (b/c) = \log_a b - \log_a c\)  
7. \(\log_a (b^n) = n \log_a b\)  
8. \((\log_a b)(\log_b c) = \log_a c\)  
9. \(\log_a b = \frac{\log_c b}{\log_c a}\) (rumus perubahan basis)  
10. \(\log_a b = \frac{1}{\log_b a}\)  
11. \(\log_{a^n} (b^n) = \log_a b\)  
12. \(\log_{a^n} (b^m) = \frac{m}{n} \log_a b\)

**Catatan penting:**  
- Rumus perubahan basis (no. 9) sangat berguna saat kalkulator hanya punya \(\log\) atau \(\ln\).

### D. Fungsi Logaritma
Bentuk umum:  
$$y = \log_a x$$

**Catatan penting:**  
- **Domain:** \(x > 0\) (tidak ada logaritma bilangan negatif dalam bilangan real).  
- \(\log_a 1 = 0\), sehingga grafik selalu melalui titik \((1, 0)\).  
- Merupakan fungsi invers dari fungsi eksponen.

### E. Persamaan Logaritma

1. Jika \(\log_a f(x) = \log_a p\), maka \(f(x) = p\).  
2. Jika \(\log_a f(x) = \log_a g(x)\), maka \(f(x) = g(x)\).  
3. Jika \(\log_{f(x)} a = \log_{g(x)} a\), maka \(f(x) = g(x)\).  
4. Jika \(\log_{f(x)} g(x) = p\), maka \(g(x) = f(x)^p\).  
5. Jika \(\log_{f(x)} g(x) = \log_{h(x)} g(x)\), maka \(f(x) = h(x)\).  
6. Jika \(\log_{f(x)} g(x) = \log_{f(x)} h(x)\), maka \(g(x) = h(x)\).

**Syarat yang harus dicek:**  
- Basis \(a > 0\), \(a \neq 1\)  
- Numerus > 0

### F. Pertidaksamaan Logaritma
**Sebelum menyelesaikan, cek syarat domain:**  
- \(f(x) > 0\), \(g(x) > 0\)  
- Basis \(a > 0\), \(a \neq 1\)

**Aturan utama:**

- **Jika \(a > 1\):**  
  \(\log_a f(x) > \log_a g(x)\) \(\implies\) \(f(x) > g(x)\)  
  \(\log_a f(x) < \log_a g(x)\) \(\implies\) \(f(x) < g(x)\)

- **Jika \(0 < a < 1\):**  
  \(\log_a f(x) > \log_a g(x)\) \(\implies\) \(f(x) < g(x)\)  
  \(\log_a f(x) < \log_a g(x)\) \(\implies\) \(f(x) > g(x)\)

**Inti:** Sama seperti pertidaksamaan eksponen (basis > 1 → tanda tetap; basis 0 < a < 1 → tanda berbalik).

## 3. Hubungan Eksponen dan Logaritma
Hubungan paling penting:  
$$\log_a b = c \quad \Leftrightarrow \quad a^c = b$$

**Makna:**  
- Eksponen menjawab: “Basis dipangkatkan berapa supaya hasilnya \(b\)?”  
- Logaritma menjawab: “Berapa pangkat dari basis \(a\) agar menjadi \(b\)?”

**Contoh:**  
- \(2^5 = 32\) \(\iff\) \(\log_2 32 = 5\)  
- \(10^3 = 1000\) \(\iff\) \(\log 1000 = 3\)

## 4. Langkah Cepat Menyelesaikan Soal

### A. Untuk Eksponen
1. Sederhanakan dengan sifat eksponen.  
2. Samakan basis jika memungkinkan.  
3. Bandingkan pangkatnya.  
4. Jika tidak bisa, ubah ke bentuk logaritma.

### B. Untuk Logaritma
1. Cek syarat domain terlebih dahulu.  
2. Gunakan sifat logaritma untuk menyederhanakan.  
3. Jika bentuk \(\log_a f(x) = \log_a g(x)\), samakan numerusnya.  
4. Jika perlu, ubah ke bentuk eksponen.
# Sistem Koordinat Kartesius

## Konsep Dasar

Sistem koordinat Kartesius adalah sistem yang digunakan untuk menentukan posisi setiap titik dalam suatu bidang datar menggunakan sepasang bilangan yang disebut **koordinat**. Sistem ini dinamai sesuai nama filsuf dan matematikawan Prancis, René Descartes (1596–1650), yang mempopulerkannya dalam karyanya _La Géométrie_.

Bidang tempat sistem ini bekerja disebut **bidang Kartesius** atau **bidang koordinat**. Bidang ini dibentuk oleh dua garis lurus yang saling tegak lurus (membentuk sudut 90°) dan saling berpotongan di satu titik.

## Sumbu Koordinat

Dua garis yang membentuk bidang Kartesius disebut **sumbu koordinat**.

- **Sumbu $x$** (sumbu absis): garis horizontal. Nilai di sebelah kanan titik pusat bernilai positif; nilai di sebelah kiri bernilai negatif.
- **Sumbu $y$** (sumbu ordinat): garis vertikal. Nilai di atas titik pusat bernilai positif; nilai di bawah bernilai negatif.

Titik perpotongan antara sumbu $x$ dan sumbu $y$ disebut **titik asal** atau **titik pusat**, yang ditulis sebagai $O(0, 0)$.

## Koordinat Titik

Setiap titik dalam bidang Kartesius dinyatakan dengan pasangan berurutan $(x, y)$, di mana:

- $x$ disebut **absis**, yaitu jarak horizontal titik tersebut dari sumbu $y$.
- $y$ disebut **ordinat**, yaitu jarak vertikal titik tersebut dari sumbu $x$.

Urutan penulisan selalu absis terlebih dahulu, baru ordinat: $(x, y)$, bukan $(y, x)$.

> **Contoh:** Titik $A(3, 5)$ berarti titik $A$ terletak 3 satuan ke kanan dari sumbu $y$ dan 5 satuan ke atas dari sumbu $x$.

> **Contoh:** Titik $B(-2, -4)$ berarti titik $B$ terletak 2 satuan ke kiri dari sumbu $y$ dan 4 satuan ke bawah dari sumbu $x$.

## Kuadran

Sumbu $x$ dan sumbu $y$ membagi bidang Kartesius menjadi empat daerah yang disebut **kuadran**. Penomoran kuadran dimulai dari kanan atas dan berputar berlawanan arah jarum jam.

|Kuadran|Tanda Absis ($x$)|Tanda Ordinat ($y$)|
|---|---|---|
|Kuadran I|positif ($+$)|positif ($+$)|
|Kuadran II|negatif ($-$)|positif ($+$)|
|Kuadran III|negatif ($-$)|negatif ($-$)|
|Kuadran IV|positif ($+$)|negatif ($-$)|

Titik yang terletak tepat pada sumbu $x$ atau sumbu $y$ tidak termasuk dalam kuadran mana pun.

> **Contoh:** $P(-3, 7)$ berada di Kuadran II karena $x < 0$ dan $y > 0$.

> **Contoh:** $Q(5, -1)$ berada di Kuadran IV karena $x > 0$ dan $y < 0$.

## Jarak antara Dua Titik

Jarak antara dua titik $A(x_1, y_1)$ dan $B(x_2, y_2)$ dihitung menggunakan rumus yang diturunkan dari Teorema Pythagoras:

$$d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$

Jarak bersifat selalu positif atau nol (nol hanya jika kedua titik sama).

> **Contoh:** Jarak antara $A(1, 2)$ dan $B(4, 6)$: $$d = \sqrt{(4-1)^2 + (6-2)^2} = \sqrt{9 + 16} = \sqrt{25} = 5$$

## Titik Tengah Dua Titik

Titik tengah (midpoint) dari segmen garis yang menghubungkan $A(x_1, y_1)$ dan $B(x_2, y_2)$ adalah titik $M$ dengan koordinat:

$$M = \left(\frac{x_1 + x_2}{2},; \frac{y_1 + y_2}{2}\right)$$

Rumus ini berarti koordinat titik tengah adalah rata-rata dari masing-masing koordinat kedua titik ujung.

> **Contoh:** Titik tengah dari $A(2, 4)$ dan $B(8, 10)$: $$M = \left(\frac{2+8}{2}, \frac{4+10}{2}\right) = (5, 7)$$

## Refleksi Titik terhadap Sumbu

Jika sebuah titik $P(x, y)$ dicerminkan, hasilnya adalah titik bayangan $P'$ dengan koordinat yang berubah mengikuti aturan tertentu.

- **Refleksi terhadap sumbu $x$**: $P(x, y) \to P'(x, -y)$. Ordinat berubah tanda; absis tetap.
- **Refleksi terhadap sumbu $y$**: $P(x, y) \to P'(-x, y)$. Absis berubah tanda; ordinat tetap.
- **Refleksi terhadap titik asal $O$**: $P(x, y) \to P'(-x, -y)$. Keduanya berubah tanda.
- **Refleksi terhadap garis $y = x$**: $P(x, y) \to P'(y, x)$. Absis dan ordinat ditukar.
- **Refleksi terhadap garis $y = -x$**: $P(x, y) \to P'(-y, -x)$. Absis dan ordinat ditukar, lalu keduanya berubah tanda.

> **Contoh:** Bayangan dari $A(3, -5)$ terhadap sumbu $y$ adalah $A'(-3, -5)$.

## Translasi Titik

**Translasi** adalah perpindahan setiap titik dalam bidang dengan jarak dan arah yang sama. Jika titik $P(x, y)$ ditranslasikan dengan vektor $T(a, b)$, maka titik bayangannya adalah:

$$P' = (x + a,; y + b)$$

Nilai $a$ menunjukkan perpindahan horizontal (positif = ke kanan, negatif = ke kiri) dan $b$ menunjukkan perpindahan vertikal (positif = ke atas, negatif = ke bawah).

> **Contoh:** Titik $A(2, 3)$ ditranslasi dengan vektor $(4, -1)$: $$A' = (2+4,; 3+(-1)) = (6, 2)$$

## Rotasi Titik

**Rotasi** adalah perputaran titik sebesar sudut tertentu terhadap suatu titik pusat. Untuk rotasi terhadap titik asal $O(0,0)$:

- **Rotasi 90° berlawanan arah jarum jam**: $P(x, y) \to P'(-y, x)$
- **Rotasi 90° searah jarum jam**: $P(x, y) \to P'(y, -x)$
- **Rotasi 180°**: $P(x, y) \to P'(-x, -y)$

> **Contoh:** Titik $B(3, 2)$ dirotasi 90° berlawanan arah jarum jam terhadap $O$: $$B' = (-2, 3)$$

## Dilatasi Titik

**Dilatasi** adalah transformasi yang memperbesar atau memperkecil jarak titik dari pusat dilatasi dengan faktor skala $k$. Untuk dilatasi terhadap titik asal $O(0,0)$ dengan faktor $k$:

$$P(x, y) \to P'(kx, ky)$$

- Jika $k > 1$: titik menjauh dari pusat (diperbesar).
- Jika $0 < k < 1$: titik mendekat ke pusat (diperkecil).
- Jika $k < 0$: titik berpindah ke sisi berlawanan dari pusat.

> **Contoh:** Titik $C(4, -2)$ didilatasi dengan faktor $k = 3$ terhadap $O$: $$C' = (12, -6)$$

## Gradien Garis dalam Koordinat Kartesius

**Gradien** (kemiringan) suatu garis adalah ukuran seberapa curam garis tersebut, dinyatakan sebagai rasio perubahan vertikal terhadap perubahan horizontal. Untuk dua titik $A(x_1, y_1)$ dan $B(x_2, y_2)$ yang dilalui garis:

$$m = \frac{y_2 - y_1}{x_2 - x_1}, \quad x_1 \neq x_2$$

- Garis dengan $m > 0$ miring ke kanan atas.
- Garis dengan $m < 0$ miring ke kanan bawah.
- Garis dengan $m = 0$ adalah horizontal.
- Garis vertikal tidak memiliki gradien (tidak terdefinisi) karena penyebutnya nol.

Dua garis sejajar memiliki gradien yang sama. Dua garis saling tegak lurus memenuhi syarat $m_1 \times m_2 = -1$.

## Persamaan Garis Lurus

Persamaan garis lurus dalam bidang Kartesius dapat ditulis dalam beberapa bentuk.

**Bentuk gradien-intersep** (paling umum): $$y = mx + c$$ di mana $m$ adalah gradien dan $c$ adalah titik potong garis dengan sumbu $y$ (intersep $y$).

**Bentuk dua titik**: Jika garis melalui $A(x_1, y_1)$ dan $B(x_2, y_2)$: $$\frac{y - y_1}{y_2 - y_1} = \frac{x - x_1}{x_2 - x_1}$$

**Bentuk titik-gradien**: Jika garis melalui $A(x_1, y_1)$ dengan gradien $m$: $$y - y_1 = m(x - x_1)$$

> **Contoh:** Garis melalui $A(1, 2)$ dan $B(3, 8)$. Gradiennya: $m = \frac{8-2}{3-1} = 3$. Persamaannya: $y - 2 = 3(x - 1) \Rightarrow y = 3x - 1$.

---

# Dasar-Dasar Geometri

## Unsur Dasar Geometri

### Titik

**Titik** adalah unsur paling mendasar dalam geometri. Titik tidak memiliki ukuran—tidak ada panjang, lebar, atau tinggi. Titik hanya menunjukkan **posisi**. Dalam gambar, titik diwakili oleh sebuah noktah kecil dan diberi nama dengan huruf kapital, seperti titik $A$, titik $B$, titik $P$.

### Garis

**Garis** adalah kumpulan tak terhingga titik-titik yang tersusun lurus dan memanjang tanpa batas di kedua ujungnya. Garis tidak memiliki tebal dan tidak memiliki ujung. Garis dinamai menggunakan dua titik yang dilaluinya, misalnya garis $AB$, atau dengan satu huruf kecil, misalnya garis $\ell$.

**Sinar** adalah bagian garis yang memiliki satu titik ujung (titik pangkal) dan memanjang tanpa batas ke satu arah. Sinar $AB$ dimulai dari titik $A$ dan melewati $B$ tanpa batas.

**Ruas garis** (segmen garis) adalah bagian garis yang memiliki dua titik ujung. Ruas garis $AB$ dimulai dari $A$ dan berakhir di $B$; panjangnya terbatas dan dapat diukur.

### Bidang

**Bidang** adalah permukaan datar yang memanjang tanpa batas ke segala arah. Bidang tidak memiliki ketebalan. Sebuah bidang dapat ditentukan oleh tiga titik yang tidak segaris, atau oleh satu garis dan satu titik di luar garis tersebut.

### Hubungan antara Titik, Garis, dan Bidang

- Dua titik berbeda selalu menentukan tepat satu garis.
- Dua garis dalam satu bidang dapat sejajar (tidak berpotongan) atau berpotongan di tepat satu titik.
- Tiga titik yang tidak segaris selalu menentukan tepat satu bidang.
- Dua bidang dapat sejajar atau berpotongan membentuk satu garis.

## Sudut

### Definisi Sudut

**Sudut** terbentuk dari dua sinar yang berasal dari titik yang sama. Titik persekutuan kedua sinar disebut **titik sudut** (_vertex_). Kedua sinar tersebut disebut **kaki sudut**.

Besar sudut diukur dalam derajat (°) atau radian (rad). Hubungan antara keduanya: $180° = \pi$ radian.

### Jenis-Jenis Sudut

- **Sudut lancip** (_acute angle_): besar sudutnya di antara 0° dan 90°, tidak termasuk 0° maupun 90°.
- **Sudut siku-siku** (_right angle_): besar sudutnya tepat 90°. Ditandai dengan lambang kotak kecil di titik sudutnya.
- **Sudut tumpul** (_obtuse angle_): besar sudutnya di antara 90° dan 180°, tidak termasuk 90° maupun 180°.
- **Sudut lurus** (_straight angle_): besar sudutnya tepat 180°. Kedua kakinya membentuk garis lurus.
- **Sudut refleks** (_reflex angle_): besar sudutnya di antara 180° dan 360°.
- **Sudut penuh** (_full angle_): besar sudutnya tepat 360°.

### Hubungan antara Sudut

**Sudut saling berpelurus** (_supplementary angles_): dua sudut yang jumlahnya 180°. Jika $\angle A$ dan $\angle B$ saling berpelurus, maka $\angle A + \angle B = 180°$.

**Sudut saling berpenyiku** (_complementary angles_): dua sudut yang jumlahnya 90°. Jika $\angle A$ dan $\angle B$ saling berpenyiku, maka $\angle A + \angle B = 90°$.

**Sudut bertolak belakang** (_vertically opposite angles_): dua sudut yang terbentuk ketika dua garis berpotongan, terletak di sisi yang berlawanan dari titik potong. Sudut bertolak belakang selalu sama besar.

**Sudut berdampingan** (_adjacent angles_): dua sudut yang memiliki satu titik sudut yang sama, satu kaki yang sama, dan tidak saling tumpang tindih.

## Garis Sejajar dan Garis Transversal

Dua garis disebut **sejajar** jika keduanya terletak dalam satu bidang dan tidak pernah berpotongan meski diperpanjang tanpa batas. Ditulis: $\ell_1 \parallel \ell_2$.

Sebuah **garis transversal** adalah garis yang memotong dua atau lebih garis lain di titik-titik yang berbeda.

Ketika satu garis transversal memotong dua garis sejajar, terbentuk pasangan sudut dengan hubungan khusus:

- **Sudut sehadap** (_corresponding angles_): terletak di posisi yang sama relatif terhadap masing-masing titik potong. Sudut sehadap sama besar.
- **Sudut dalam berseberangan** (_alternate interior angles_): terletak di antara dua garis sejajar, di sisi yang berlawanan dari transversal. Sudut dalam berseberangan sama besar.
- **Sudut luar berseberangan** (_alternate exterior angles_): terletak di luar dua garis sejajar, di sisi yang berlawanan dari transversal. Sudut luar berseberangan sama besar.
- **Sudut dalam sepihak** (_co-interior angles_ atau _same-side interior angles_): terletak di antara dua garis sejajar, di sisi yang sama dari transversal. Jumlah sudut dalam sepihak adalah 180°.

## Bangun Datar

### Segitiga

**Segitiga** adalah bangun datar yang dibatasi oleh tiga ruas garis yang saling berhubungan di tiga titik sudut. Jumlah semua sudut dalam segitiga selalu 180°.

#### Jenis Segitiga Berdasarkan Panjang Sisi

- **Segitiga sama sisi**: ketiga sisinya sama panjang. Ketiga sudutnya juga sama besar, yaitu 60° masing-masing.
- **Segitiga sama kaki**: dua sisinya sama panjang. Dua sudut di dasar (sudut alas) sama besar.
- **Segitiga sembarang**: ketiga sisinya berbeda panjang. Ketiga sudutnya juga berbeda besar.

#### Jenis Segitiga Berdasarkan Besar Sudut

- **Segitiga lancip**: ketiga sudutnya lancip (kurang dari 90°).
- **Segitiga siku-siku**: salah satu sudutnya tepat 90°. Sisi di hadapan sudut siku-siku disebut **hipotenusa** dan merupakan sisi terpanjang.
- **Segitiga tumpul**: salah satu sudutnya tumpul (lebih dari 90°).

#### Rumus Segitiga

Jika $a$, $b$, $c$ adalah panjang sisi dan $t$ adalah tinggi (jarak tegak lurus dari satu titik sudut ke sisi yang berseberangan):

$$\text{Keliling} = a + b + c$$ $$\text{Luas} = \frac{1}{2} \times \text{alas} \times \text{tinggi}$$

Untuk segitiga dengan sisi $a$, $b$, $c$ yang diketahui semua panjangnya, luas dapat dihitung dengan **Rumus Heron**: $$s = \frac{a + b + c}{2} \quad \text{(setengah keliling)}$$ $$\text{Luas} = \sqrt{s(s-a)(s-b)(s-c)}$$

> **Contoh:** Segitiga dengan alas 8 cm dan tinggi 5 cm: Luas $= \frac{1}{2} \times 8 \times 5 = 20$ cm².

### Persegi

**Persegi** adalah bangun datar segi empat dengan keempat sisinya sama panjang dan keempat sudutnya siku-siku (90°). Persegi memiliki dua diagonal yang sama panjang, saling tegak lurus, dan saling membagi dua sama panjang.

$$\text{Keliling} = 4s$$ $$\text{Luas} = s^2$$ $$\text{Diagonal} = s\sqrt{2}$$

di mana $s$ adalah panjang sisi.

### Persegi Panjang

**Persegi Panjang** adalah segi empat dengan keempat sudutnya siku-siku. Sisi-sisi yang berhadapan sama panjang dan sejajar. Persegi panjang memiliki dua diagonal yang sama panjang dan saling membagi dua sama panjang, tetapi diagonalnya tidak harus saling tegak lurus.

$$\text{Keliling} = 2(p + l)$$ $$\text{Luas} = p \times l$$ $$\text{Diagonal} = \sqrt{p^2 + l^2}$$

di mana $p$ adalah panjang dan $l$ adalah lebar.

### Jajar Genjang

**Jajar genjang** (_parallelogram_) adalah segi empat dengan dua pasang sisi yang sejajar dan sama panjang. Sudut-sudut yang berhadapan sama besar; sudut-sudut yang berdampingan berjumlah 180°. Diagonal jajar genjang saling membagi dua sama panjang, tetapi tidak harus sama panjang satu sama lain dan tidak harus tegak lurus.

$$\text{Keliling} = 2(a + b)$$ $$\text{Luas} = a \times t$$

di mana $a$ adalah panjang alas dan $t$ adalah tinggi (jarak tegak lurus antara dua sisi sejajar).

### Belah Ketupat

**Belah ketupat** (_rhombus_) adalah segi empat dengan keempat sisinya sama panjang. Belah ketupat adalah jajar genjang khusus. Diagonalnya saling tegak lurus dan saling membagi dua sama panjang, tetapi umumnya tidak sama panjang satu sama lain.

$$\text{Keliling} = 4s$$ $$\text{Luas} = \frac{d_1 \times d_2}{2}$$

di mana $d_1$ dan $d_2$ adalah panjang kedua diagonal.

### Trapesium

**Trapesium** adalah segi empat dengan tepat satu pasang sisi yang sejajar. Sisi yang sejajar disebut **alas** (alas bawah dan alas atas). Sisi yang tidak sejajar disebut **kaki trapesium**.

- **Trapesium sama kaki**: kedua kakinya sama panjang. Sudut-sudut di setiap alas sama besar. Diagonalnya sama panjang.
- **Trapesium siku-siku**: salah satu kakinya tegak lurus terhadap kedua alas.
- **Trapesium sembarang**: keempat sisinya berbeda panjang.

$$\text{Keliling} = a + b + c + d$$ $$\text{Luas} = \frac{(a_1 + a_2)}{2} \times t$$

di mana $a_1$ dan $a_2$ adalah panjang kedua alas, dan $t$ adalah tinggi trapesium (jarak tegak lurus antara kedua alas).

### Layang-Layang

**Layang-layang** (_kite_) adalah segi empat dengan dua pasang sisi yang sama panjang, masing-masing pasang berdampingan (bukan berhadapan). Diagonalnya saling tegak lurus; salah satu diagonal membagi dua sama panjang diagonal yang lain.

$$\text{Keliling} = 2(a + b)$$ $$\text{Luas} = \frac{d_1 \times d_2}{2}$$

di mana $a$ dan $b$ adalah panjang sisi-sisi yang berbeda, dan $d_1$, $d_2$ adalah panjang kedua diagonal.

### Lingkaran

**Lingkaran** adalah himpunan semua titik dalam sebuah bidang yang berjarak sama dari satu titik tetap. Titik tetap tersebut disebut **pusat lingkaran** dan jarak tersebut disebut **jari-jari** ($r$).

Beberapa unsur penting lingkaran:

- **Jari-jari** ($r$): ruas garis dari pusat ke tepi lingkaran.
- **Diameter** ($d = 2r$): ruas garis yang menghubungkan dua titik pada lingkaran dan melewati pusatnya. Diameter adalah tali busur terpanjang.
- **Tali busur** (_chord_): ruas garis yang menghubungkan dua titik pada lingkaran, tidak harus melewati pusat.
- **Busur** (_arc_): bagian dari keliling lingkaran.
- **Juring** (_sector_): daerah di antara dua jari-jari dan busur yang diapit.
- **Tembereng** (_segment_): daerah di antara tali busur dan busur yang diapit.
- **Apotema**: jarak tegak lurus dari pusat ke suatu tali busur.

$$\text{Keliling} = 2\pi r = \pi d$$ $$\text{Luas} = \pi r^2$$

Untuk **busur** dengan sudut pusat $\theta$ (dalam derajat): $$\text{Panjang busur} = \frac{\theta}{360°} \times 2\pi r$$

Untuk **juring** dengan sudut pusat $\theta$: $$\text{Luas juring} = \frac{\theta}{360°} \times \pi r^2$$

### Segi-$n$ Beraturan

**Segi-$n$ beraturan** adalah bangun datar dengan $n$ sisi sama panjang dan $n$ sudut sama besar.

Besar setiap sudut dalam segi-$n$ beraturan: $$\text{Sudut dalam} = \frac{(n-2) \times 180°}{n}$$

Jumlah seluruh sudut dalam segi-$n$: $$\text{Jumlah sudut dalam} = (n-2) \times 180°$$

> **Contoh:** Segi enam beraturan: jumlah sudut dalam $= (6-2) \times 180° = 720°$. Setiap sudut $= 720° \div 6 = 120°$.

## Teorema Pythagoras

Untuk segitiga siku-siku dengan kaki-kaki $a$ dan $b$, serta hipotenusa $c$ (sisi terpanjang, di hadapan sudut siku-siku):

$$a^2 + b^2 = c^2$$

Teorema ini berlaku hanya untuk segitiga siku-siku. Konversnya juga benar: jika $a^2 + b^2 = c^2$, maka segitiga tersebut pasti siku-siku.

**Tripel Pythagoras** adalah himpunan tiga bilangan bulat positif $(a, b, c)$ yang memenuhi $a^2 + b^2 = c^2$. Contoh yang umum:

- $(3, 4, 5)$: $9 + 16 = 25$ ✓
- $(5, 12, 13)$: $25 + 144 = 169$ ✓
- $(8, 15, 17)$: $64 + 225 = 289$ ✓

Kelipatan dari tripel Pythagoras juga merupakan tripel Pythagoras. Misalnya, $(6, 8, 10)$ adalah kelipatan 2 dari $(3, 4, 5)$.

> **Contoh:** Sebuah tangga sepanjang 13 m bersandar pada tembok. Kaki tangga berjarak 5 m dari tembok. Tinggi ujung tangga: $c^2 = a^2 + b^2 \Rightarrow 13^2 = 5^2 + t^2 \Rightarrow t^2 = 169 - 25 = 144 \Rightarrow t = 12$ m.

## Kongruensi

Dua bangun datar dikatakan **kongruen** jika keduanya memiliki bentuk dan ukuran yang tepat sama—satu dapat diletakkan tepat di atas yang lain melalui translasi, rotasi, dan/atau refleksi.

Notasi: $\triangle ABC \cong \triangle DEF$ berarti segitiga $ABC$ kongruen dengan segitiga $DEF$.

### Syarat Kongruensi Segitiga

Ada empat kondisi yang masing-masing cukup untuk membuktikan dua segitiga kongruen:

- **Sisi-Sisi-Sisi (SSS)**: ketiga pasang sisi yang bersesuaian sama panjang.
- **Sisi-Sudut-Sisi (SAS)**: dua pasang sisi yang bersesuaian sama panjang, dan sudut yang diapit keduanya sama besar.
- **Sudut-Sisi-Sudut (ASA)**: dua pasang sudut yang bersesuaian sama besar, dan sisi yang diapit keduanya sama panjang.
- **Sudut-Sudut-Sisi (AAS)**: dua pasang sudut yang bersesuaian sama besar, dan satu pasang sisi yang tidak diapit (tetapi bersesuaian) sama panjang.

Catatan: **Sudut-Sudut-Sudut (AAA)** tidak menjamin kongruensi, hanya menjamin kesebangunan.

## Kesebangunan

Dua bangun datar dikatakan **sebangun** (_similar_) jika keduanya memiliki bentuk yang sama tetapi tidak harus ukuran yang sama. Sudut-sudut yang bersesuaian sama besar, dan sisi-sisi yang bersesuaian memiliki **rasio yang sama** (disebut **faktor skala**).

Notasi: $\triangle ABC \sim \triangle DEF$.

Jika faktor skala antara dua bangun sebangun adalah $k$, maka:

- Rasio sisi-sisi yang bersesuaian $= k$
- Rasio keliling $= k$
- Rasio luas $= k^2$

### Syarat Kesebangunan Segitiga

- **AA (Sudut-Sudut)**: dua pasang sudut yang bersesuaian sama besar. Karena jumlah sudut segitiga selalu 180°, cukup dua pasang sudut untuk membuktikan kesebangunan.
- **SSS (Sisi-Sisi-Sisi)**: ketiga pasang sisi yang bersesuaian memiliki rasio yang sama.
- **SAS (Sisi-Sudut-Sisi)**: dua pasang sisi yang bersesuaian memiliki rasio yang sama, dan sudut yang diapit keduanya sama besar.

> **Contoh:** $\triangle ABC \sim \triangle PQR$ dengan $AB = 4$, $BC = 6$, $AC = 8$, dan $PQ = 6$. Faktor skala $= \frac{PQ}{AB} = \frac{6}{4} = 1{,}5$. Maka $QR = 6 \times 1{,}5 = 9$ dan $PR = 8 \times 1{,}5 = 12$.

## Bangun Ruang

### Kubus

**Kubus** adalah bangun ruang yang dibatasi oleh enam sisi berbentuk persegi yang sama ukurannya. Kubus memiliki 8 titik sudut, 12 rusuk yang sama panjang, dan 6 sisi.

$$\text{Volume} = s^3$$ $$\text{Luas permukaan} = 6s^2$$ $$\text{Diagonal ruang} = s\sqrt{3}$$ $$\text{Diagonal sisi} = s\sqrt{2}$$

di mana $s$ adalah panjang rusuk.

### Balok

**Balok** (_rectangular prism_) adalah bangun ruang yang dibatasi oleh enam sisi berbentuk persegi panjang. Sisi-sisi yang berhadapan sama bentuk dan ukurannya.

$$\text{Volume} = p \times l \times t$$ $$\text{Luas permukaan} = 2(pl + pt + lt)$$ $$\text{Diagonal ruang} = \sqrt{p^2 + l^2 + t^2}$$

di mana $p$ = panjang, $l$ = lebar, $t$ = tinggi.

### Prisma

**Prisma** adalah bangun ruang yang memiliki dua alas berbentuk segi banyak yang sama dan sejajar, dihubungkan oleh sisi-sisi tegak berbentuk persegi panjang. Prisma dinamai berdasarkan bentuk alasnya (prisma segitiga, prisma segi empat, prisma segi lima, dan seterusnya).

$$\text{Volume} = \text{Luas alas} \times \text{tinggi}$$ $$\text{Luas permukaan} = 2 \times \text{Luas alas} + \text{Keliling alas} \times \text{tinggi}$$

### Limas

**Limas** (_pyramid_) adalah bangun ruang yang memiliki satu alas berbentuk segi banyak dan sisi-sisi tegak berbentuk segitiga yang bertemu di satu titik puncak. Limas dinamai berdasarkan bentuk alasnya (limas segitiga, limas segi empat, dan seterusnya).

$$\text{Volume} = \frac{1}{3} \times \text{Luas alas} \times \text{tinggi}$$ $$\text{Luas permukaan} = \text{Luas alas} + \text{Jumlah luas seluruh sisi tegak}$$

### Tabung

**Tabung** (_cylinder_) adalah bangun ruang yang memiliki dua alas berbentuk lingkaran yang sama dan sejajar, dihubungkan oleh sisi lengkung.

$$\text{Volume} = \pi r^2 t$$ $$\text{Luas permukaan} = 2\pi r^2 + 2\pi r t = 2\pi r(r + t)$$ $$\text{Luas selimut} = 2\pi r t$$

di mana $r$ = jari-jari alas dan $t$ = tinggi.

### Kerucut

**Kerucut** (_cone_) adalah bangun ruang yang memiliki satu alas berbentuk lingkaran dan sisi lengkung yang mengerucut ke satu titik puncak. Jarak dari titik puncak ke tepi alas disebut **garis pelukis** atau **slant height** ($s$).

$$s = \sqrt{r^2 + t^2}$$ $$\text{Volume} = \frac{1}{3}\pi r^2 t$$ $$\text{Luas permukaan} = \pi r^2 + \pi r s = \pi r(r + s)$$ $$\text{Luas selimut} = \pi r s$$

### Bola

**Bola** (_sphere_) adalah bangun ruang yang merupakan himpunan semua titik dalam ruang yang berjarak sama dari satu titik pusat.

$$\text{Volume} = \frac{4}{3}\pi r^3$$ $$\text{Luas permukaan} = 4\pi r^2$$

## Hubungan antara Volume Bangun Ruang

Ada dua hubungan penting yang sering dimanfaatkan:

1. Volume limas sama dengan sepertiga volume prisma dengan alas dan tinggi yang sama: $V_\text{limas} = \frac{1}{3} V_\text{prisma}$.
2. Volume kerucut sama dengan sepertiga volume tabung dengan alas dan tinggi yang sama: $V_\text{kerucut} = \frac{1}{3} V_\text{tabung}$.

## Transformasi Geometri

**Transformasi geometri** adalah perpindahan atau perubahan posisi, ukuran, atau bentuk suatu bangun berdasarkan aturan tertentu. Ada empat jenis transformasi utama.

### Translasi

Setiap titik pada bangun dipindahkan dengan jarak dan arah yang sama. Bentuk dan ukuran bangun tidak berubah.

### Refleksi

Setiap titik pada bangun dicerminkan terhadap suatu sumbu atau garis tertentu. Jarak setiap titik dari garis cermin dipertahankan. Bentuk dan ukuran bangun tidak berubah, tetapi orientasinya terbalik. Sumbu refleksi dapat berupa sumbu $x$, sumbu $y$, garis $y = x$, garis $y = -x$, atau garis lainnya.

### Rotasi

Setiap titik pada bangun diputar sebesar sudut tertentu terhadap suatu titik pusat. Bentuk dan ukuran bangun tidak berubah. Rotasi memerlukan tiga informasi: titik pusat, besar sudut, dan arah perputaran (searah atau berlawanan jarum jam).

### Dilatasi

Setiap titik pada bangun diperbesar atau diperkecil dari suatu titik pusat dengan faktor skala $k$. Jika $|k| > 1$, bangun diperbesar; jika $0 < |k| < 1$, bangun diperkecil. Dilatasi mengubah ukuran tetapi mempertahankan bentuk (sudut-sudut tetap sama). Oleh karena itu, hasil dilatasi selalu sebangun dengan bangun asal.

|Transformasi|Bentuk|Ukuran|Orientasi|
|---|---|---|---|
|Translasi|Tetap|Tetap|Tetap|
|Refleksi|Tetap|Tetap|Terbalik|
|Rotasi|Tetap|Tetap|Berubah|
|Dilatasi|Tetap|Berubah|Tergantung tanda $k$|

## Sifat-Sifat Diagonal pada Segi Empat

Sifat diagonal berbeda-beda pada tiap jenis segi empat, dan perbedaan ini sering menjadi dasar pembuktian atau identifikasi bangun.

- **Persegi**: diagonal sama panjang, saling tegak lurus, dan saling membagi dua sama panjang.
- **Persegi panjang**: diagonal sama panjang dan saling membagi dua sama panjang, tetapi tidak tegak lurus.
- **Jajar genjang**: diagonal saling membagi dua sama panjang, tetapi tidak sama panjang dan tidak tegak lurus.
- **Belah ketupat**: diagonal saling tegak lurus dan saling membagi dua sama panjang, tetapi tidak sama panjang.
- **Trapesium sama kaki**: diagonal sama panjang.
- **Layang-layang**: diagonal saling tegak lurus; salah satu diagonal membagi dua sama panjang diagonal yang lain, tetapi tidak sebaliknya.

## Garis-Garis Istimewa pada Segitiga

### Garis Tinggi

**Garis tinggi** adalah ruas garis dari sebuah titik sudut yang tegak lurus terhadap sisi di hadapannya (atau perpanjangan sisi tersebut). Ketiga garis tinggi suatu segitiga berpotongan di satu titik yang disebut **ortosentrum**.

### Garis Bagi

**Garis bagi** adalah ruas garis dari sebuah titik sudut yang membagi sudut tersebut menjadi dua sudut sama besar. Ketiga garis bagi suatu segitiga berpotongan di satu titik yang disebut **insentrum**, yang merupakan pusat lingkaran dalam segitiga (lingkaran yang menyinggung ketiga sisi dari dalam).

### Garis Berat

**Garis berat** adalah ruas garis dari sebuah titik sudut ke titik tengah sisi di hadapannya. Ketiga garis berat suatu segitiga berpotongan di satu titik yang disebut **titik berat** (_centroid_). Titik berat membagi setiap garis berat dengan rasio $2 : 1$ dari titik sudut ke sisi.

### Sumbu Simetri Sisi

**Sumbu simetri sisi** (garis sumbu) adalah garis yang tegak lurus terhadap sisi dan melewati titik tengahnya. Ketiga sumbu simetri sisi suatu segitiga berpotongan di satu titik yang disebut **sirkumsentrum**, yang merupakan pusat lingkaran luar segitiga (lingkaran yang melewati ketiga titik sudut).

## Luas Bangun Datar: Rangkuman Rumus

|Bangun|Rumus Luas|
|---|---|
|Segitiga|$\dfrac{1}{2} \times a \times t$|
|Persegi|$s^2$|
|Persegi panjang|$p \times l$|
|Jajar genjang|$a \times t$|
|Trapesium|$\dfrac{(a_1 + a_2)}{2} \times t$|
|Belah ketupat|$\dfrac{d_1 \times d_2}{2}$|
|Layang-layang|$\dfrac{d_1 \times d_2}{2}$|
|Lingkaran|$\pi r^2$|
|Segi-$n$ beraturan|$\dfrac{n \times s^2}{4\tan(180°/n)}$|
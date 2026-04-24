# Notasi standar yang berlaku di seluruh rumus ini

- **Sisi:** $a, b, c$ (Sisi $a$ berhadapan dengan sudut $A$, sisi $b$ berhadapan dengan sudut $B$, dst.)
- **Sudut:** $A, B, C$
- **Luas:** $L$
- **Keliling:** $K$
- **Setengah Keliling (Semi-perimeter):** $s$

## 1. Sifat Dasar & Keliling

- **Jumlah Sudut Dalam:**

$$A + B + C = 180^\circ$$

- **Keliling:**

$$K = a + b + c$$

- **Setengah Keliling:**

$$s = \frac{a + b + c}{2}$$

## 2. Macam-macam Rumus Luas ($L$)

Gunakan rumus yang sesuai dengan data yang Anda miliki di soal.

- **Jika diketahui alas dan tinggi ($t_a$ ditarik menuju alas $a$):**

$$L = \frac{1}{2} \cdot a \cdot t_a$$

- **Rumus Heron (Diketahui panjang ketiga sisi $a, b, c$):**

$$L = \sqrt{s(s-a)(s-b)(s-c)}$$

- **Trigonometri (Diketahui 2 sisi dan 1 sudut apit):**

$$L = \frac{1}{2}ab \sin C$$

$$L = \frac{1}{2}ac \sin B$$

$$L = \frac{1}{2}bc \sin A$$

- **Berdasarkan Jari-jari Lingkaran Dalam ($r$):**

$$L = s \cdot r$$

- **Berdasarkan Jari-jari Lingkaran Luar ($R$):**

$$L = \frac{abc}{4R}$$

- **Rumus Tali Sepatu / Shoelace (Jika diketahui titik koordinat kartesius $(x_1,y_1), (x_2,y_2), (x_3,y_3)$):**

$$L = \frac{1}{2} |x_1(y_2 - y_3) + x_2(y_3 - y_1) + x_3(y_1 - y_2)|$$

## 3. Aturan Trigonometri Segitiga Sembarang

Berlaku untuk semua jenis segitiga untuk mencari panjang sisi atau besar sudut yang hilang.

- **Aturan Sinus** (Gunakan jika diketahui pasangan sisi & sudut yang berhadapan):

$$\frac{a}{\sin A} = \frac{b}{\sin B} = \frac{c}{\sin C} = 2R$$

- **Aturan Cosinus** (Gunakan jika diketahui 3 sisi, atau 2 sisi dan 1 sudut apit):

  **Mencari panjang sisi:**

$$a^2 = b^2 + c^2 - 2bc \cos A$$

$$b^2 = a^2 + c^2 - 2ac \cos B$$

$$c^2 = a^2 + b^2 - 2ab \cos C$$

  **Mencari besar sudut:**

$$\cos A = \frac{b^2 + c^2 - a^2}{2bc}$$

- **Aturan Tangen:**

$$\frac{a-b}{a+b} = \frac{\tan(\frac{A-B}{2})}{\tan(\frac{A+B}{2})}$$

## 4. Garis-garis Istimewa dalam Segitiga

Rumus untuk mencari panjang garis yang ditarik dari titik sudut.

- **Panjang Garis Tinggi ($t_a$ = garis tegak lurus ke sisi $a$):**

$$t_a = \frac{2L}{a} = c \sin B = b \sin C$$

- **Panjang Garis Berat / Teorema Apollonius ($m_c$ = membagi sisi $c$ menjadi 2 sama panjang):**

$$m_c = \frac{1}{2} \sqrt{2a^2 + 2b^2 - c^2}$$

- **Panjang Garis Bagi Dalam ($d_c$ = membagi sudut $C$ menjadi 2 sama besar):**

$$d_c = \frac{2ab \cos(C/2)}{a+b}$$

(Catatan: Bisa juga dengan $d_c = \sqrt{ab - xy}$, di mana $x$ dan $y$ adalah segmen sisi $c$ yang terpotong oleh garis bagi tersebut).

## 5. Jari-jari Lingkaran pada Segitiga

- **Jari-jari Lingkaran Dalam ($r$):** Menyinggung ketiga sisi segitiga di bagian dalam.

$$r = \frac{L}{s} = \sqrt{\frac{(s-a)(s-b)(s-c)}{s}}$$

- **Jari-jari Lingkaran Luar ($R$):** Melewati ketiga titik sudut segitiga.

$$R = \frac{abc}{4L} = \frac{a}{2 \sin A}$$

- **Jari-jari Lingkaran Singgung Luar ($r_a$):** Menyinggung sisi $a$ bagian luar dan perpanjangan dua sisi lainnya.

$$r_a = \frac{L}{s-a}$$

## 6. Rumus Segitiga Khusus

Turunan rumus dari bentuk umum di atas yang disederhanakan karena memiliki sifat khusus.

### A. Segitiga Siku-Siku (Misal sudut siku-siku di $C$)

- **Teorema Pythagoras:**

$$c^2 = a^2 + b^2$$

- **Luas:**

$$L = \frac{1}{2} \cdot a \cdot b$$

- **Tinggi ke hipotenusa ($t_c$):**

$$t_c = \frac{a \cdot b}{c}$$

### B. Segitiga Sama Sisi (Ketiga sisi sama panjang: $a = b = c$)

- **Tinggi ($t$):**

$$t = \frac{1}{2}a\sqrt{3}$$

- **Luas ($L$):**

$$L = \frac{1}{4}a^2\sqrt{3}$$

- **Jari-jari Dalam ($r$):**

$$r = \frac{1}{6}a\sqrt{3}$$

- **Jari-jari Luar ($R$):**

$$R = \frac{1}{3}a\sqrt{3}$$
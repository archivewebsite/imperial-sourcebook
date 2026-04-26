# Persamaan Garis

## 1. Sistem Koordinat Kartesius

Sistem koordinat Kartesius adalah sistem untuk menentukan posisi titik pada bidang menggunakan dua garis bilangan yang saling tegak lurus.

Dua garis bilangan tersebut adalah:

- sumbu horizontal, disebut sumbu-$x$;
- sumbu vertikal, disebut sumbu-$y$.

Titik pada bidang Kartesius dinyatakan sebagai pasangan berurutan:

$$
(x,y)
$$

dengan:

- $x$ menyatakan posisi titik terhadap sumbu-$y$;
- $y$ menyatakan posisi titik terhadap sumbu-$x$.

Alasan pasangan ditulis berurutan adalah karena posisi horizontal dan vertikal memiliki peran berbeda. Pasangan $(x,y)$ tidak dapat ditukar menjadi $(y,x)$ tanpa mengubah posisi titik, kecuali dalam keadaan khusus tertentu.

---

## 2. Titik

Titik adalah objek geometri yang menyatakan suatu posisi tanpa ukuran panjang, luas, atau volume.

Dalam bidang Kartesius, titik ditentukan oleh koordinatnya.

Jika suatu titik diberi nama $P$, maka koordinatnya dapat ditulis:

$$
P(x_P,y_P)
$$

dengan:

- $x_P$ adalah koordinat horizontal titik $P$;
- $y_P$ adalah koordinat vertikal titik $P$.

Subskrip pada $x_P$ dan $y_P$ digunakan untuk menunjukkan bahwa koordinat tersebut milik titik $P$. Ini menghilangkan ambiguitas ketika beberapa titik dibahas sekaligus.

---

## 3. Garis Lurus

Garis lurus adalah himpunan titik-titik pada bidang yang memiliki arah tetap.

Pada bidang Kartesius, garis lurus dapat dinyatakan dengan persamaan. Persamaan tersebut menentukan semua titik yang berada pada garis.

Jika suatu titik $(x,y)$ berada pada garis, maka koordinatnya memenuhi persamaan garis tersebut. Jika tidak memenuhi, maka titik itu tidak berada pada garis.

Alasannya, persamaan garis berfungsi sebagai syarat keanggotaan: titik termasuk pada garis hanya jika koordinatnya membuat persamaan bernilai benar.

---

## 4. Persamaan Garis

Persamaan garis adalah persamaan yang memuat variabel koordinat titik, biasanya $x$ dan $y$, sehingga semua pasangan $(x,y)$ yang memenuhi persamaan tersebut membentuk suatu garis lurus.

Variabel $x$ dan $y$ dalam persamaan garis menyatakan koordinat titik umum pada garis, bukan satu titik tertentu.

Sebuah persamaan disebut persamaan garis lurus apabila himpunan penyelesaiannya pada bidang Kartesius membentuk garis lurus.

---

## 5. Gradien

Gradien adalah ukuran kemiringan garis terhadap arah horizontal.

Gradien menyatakan perbandingan antara perubahan koordinat vertikal dan perubahan koordinat horizontal.

Secara umum, gradien ditulis:

$$
m=\frac{\Delta y}{\Delta x}
$$

dengan:

- $m$ adalah gradien;
- $\Delta y$ adalah perubahan nilai $y$;
- $\Delta x$ adalah perubahan nilai $x$.

Simbol $\Delta$ dibaca sebagai “perubahan”.

Alasan gradien ditulis sebagai perbandingan $\frac{\Delta y}{\Delta x}$ adalah karena kemiringan garis ditentukan oleh seberapa besar perubahan vertikal terjadi untuk setiap perubahan horizontal.

Gradien hanya terdefinisi jika $\Delta x \ne 0$. Jika $\Delta x=0$, pembagian oleh nol terjadi, dan pembagian oleh nol tidak didefinisikan dalam aritmetika biasa.

---

## 6. Gradien dari Dua Titik

Jika sebuah garis melalui dua titik berbeda $P(x_P,y_P)$ dan $Q(x_Q,y_Q)$, maka gradien garis tersebut adalah:

$$
m=\frac{y_Q-y_P}{x_Q-x_P}
$$

dengan syarat:

$$
x_Q \ne x_P
$$

Alasan syarat tersebut diperlukan adalah karena penyebut $x_Q-x_P$ tidak boleh bernilai nol.

Dua titik harus berbeda agar dapat menentukan arah garis. Jika dua titik sama, tidak ada perubahan posisi, sehingga arah garis tidak dapat ditentukan dari pasangan titik tersebut saja.

---

## 7. Garis Horizontal

Garis horizontal adalah garis yang sejajar dengan sumbu-$x$.

Pada garis horizontal, semua titik memiliki nilai $y$ yang sama. Oleh karena itu bentuk persamaannya adalah:

$$
y=k
$$

dengan $k$ adalah konstanta.

Gradien garis horizontal adalah:

$$
m=0
$$

Alasannya, pada garis horizontal tidak terjadi perubahan vertikal, sehingga $\Delta y=0$. Karena gradien adalah $\frac{\Delta y}{\Delta x}$, maka gradiennya bernilai nol selama $\Delta x \ne 0$.

---

## 8. Garis Vertikal

Garis vertikal adalah garis yang sejajar dengan sumbu-$y$.

Pada garis vertikal, semua titik memiliki nilai $x$ yang sama. Oleh karena itu bentuk persamaannya adalah:

$$
x=h
$$

dengan $h$ adalah konstanta.

Gradien garis vertikal tidak terdefinisi.

Alasannya, pada garis vertikal tidak terjadi perubahan horizontal, sehingga $\Delta x=0$. Karena gradien menggunakan pembagian oleh $\Delta x$, maka gradien tidak dapat dihitung.

---

## 9. Bentuk Umum Persamaan Garis

Bentuk umum persamaan garis adalah:

$$
Ax+By+C=0
$$

dengan:

- $A$, $B$, dan $C$ adalah konstanta;
- $x$ dan $y$ adalah variabel koordinat titik umum pada garis;
- $A$ dan $B$ tidak boleh keduanya bernilai nol.

Syarat tersebut ditulis:

$$
(A,B)\ne(0,0)
$$

Alasan $A$ dan $B$ tidak boleh keduanya nol adalah karena jika keduanya nol, persamaan tidak lagi memuat variabel $x$ atau $y$, sehingga tidak menentukan garis pada bidang.

Bentuk umum dapat mewakili garis miring, garis horizontal, dan garis vertikal. Ini terjadi karena hubungan antara $x$ dan $y$ dapat disesuaikan oleh konstanta $A$, $B$, dan $C$.

---

## 10. Bentuk Eksplisit Persamaan Garis

Bentuk eksplisit persamaan garis adalah bentuk yang menyatakan $y$ secara langsung sebagai fungsi dari $x$:

$$
y=mx+c
$$

dengan:

- $m$ adalah gradien;
- $c$ adalah titik potong garis dengan sumbu-$y$;
- $x$ adalah koordinat horizontal titik umum pada garis;
- $y$ adalah koordinat vertikal titik umum pada garis.

Bentuk ini hanya dapat digunakan untuk garis yang bukan vertikal.

Alasannya, pada garis vertikal, satu nilai $x$ berpasangan dengan banyak nilai $y$, sehingga $y$ tidak dapat dinyatakan sebagai satu nilai tunggal yang bergantung pada $x$.

---

## 11. Titik Potong dengan Sumbu-$y$

Titik potong dengan sumbu-$y$ adalah titik tempat garis memotong sumbu-$y$.

Setiap titik pada sumbu-$y$ memiliki koordinat horizontal:

$$
x=0
$$

Maka, untuk persamaan:

$$
y=mx+c
$$

ketika titik berada pada sumbu-$y$, berlaku:

$$
y=c
$$

Jadi titik potong dengan sumbu-$y$ adalah:

$$
(0,c)
$$

Alasannya, substitusi $x=0$ ke dalam bentuk $y=mx+c$ menghilangkan suku $mx$, sehingga nilai $y$ yang tersisa adalah $c$.

---

## 12. Bentuk Titik-Gradien

Bentuk titik-gradien menyatakan persamaan garis berdasarkan satu titik pada garis dan gradien garis.

Jika garis memiliki gradien $m$ dan melalui titik $P(x_P,y_P)$, maka persamaannya adalah:

$$
y-y_P=m(x-x_P)
$$

Makna setiap bagian:

- $(x,y)$ adalah titik umum pada garis;
- $(x_P,y_P)$ adalah titik tetap yang diketahui berada pada garis;
- $m$ adalah gradien garis.

Alasan bentuk ini benar adalah karena gradien antara titik umum $(x,y)$ dan titik tetap $P(x_P,y_P)$ harus sama dengan gradien garis. Hubungan tersebut berasal dari definisi gradien sebagai perbandingan perubahan vertikal terhadap perubahan horizontal.

---

## 13. Bentuk Dua Titik

Bentuk dua titik digunakan untuk menyatakan persamaan garis melalui dua titik berbeda.

Jika garis melalui titik $P(x_P,y_P)$ dan $Q(x_Q,y_Q)$, serta $x_Q\ne x_P$, maka persamaannya dapat ditulis:

$$
y-y_P=\frac{y_Q-y_P}{x_Q-x_P}(x-x_P)
$$

Bentuk ini berasal dari bentuk titik-gradien, dengan gradien:

$$
m=\frac{y_Q-y_P}{x_Q-x_P}
$$

Alasan bentuk ini memerlukan $x_Q\ne x_P$ adalah karena gradien dalam bentuk tersebut memiliki penyebut $x_Q-x_P$. Jika penyebut bernilai nol, bentuk tersebut tidak terdefinisi.

Untuk garis vertikal yang melalui dua titik dengan koordinat horizontal sama, persamaannya berbentuk:

$$
x=x_P
$$

Alasannya, semua titik pada garis vertikal memiliki koordinat horizontal yang sama.

---

## 14. Bentuk Intersep

Bentuk intersep adalah bentuk persamaan garis yang menggunakan titik potong garis terhadap sumbu-$x$ dan sumbu-$y$.

Bentuknya adalah:

$$
\frac{x}{a}+\frac{y}{b}=1
$$

dengan:

- $a$ adalah nilai koordinat $x$ saat garis memotong sumbu-$x$;
- $b$ adalah nilai koordinat $y$ saat garis memotong sumbu-$y$;
- $a\ne0$ dan $b\ne0$.

Titik potong dengan sumbu-$x$ adalah:

$$
(a,0)
$$

Titik potong dengan sumbu-$y$ adalah:

$$
(0,b)
$$

Alasan $a$ dan $b$ tidak boleh nol adalah karena keduanya menjadi penyebut dalam persamaan. Pembagian oleh nol tidak didefinisikan.

Bentuk ini tidak mencakup garis yang melalui titik asal sebagai satu-satunya titik potong terhadap kedua sumbu, karena bentuk tersebut membutuhkan dua intersep tak nol.

---

## 15. Hubungan Bentuk Umum dan Bentuk Eksplisit

Bentuk umum:

$$
Ax+By+C=0
$$

dapat diubah menjadi bentuk eksplisit jika:

$$
B\ne0
$$

Dengan memindahkan suku selain $By$ ke ruas lain:

$$
By=-Ax-C
$$

Lalu membagi kedua ruas dengan $B$:

$$
y=-\frac{A}{B}x-\frac{C}{B}
$$

Maka gradiennya adalah:

$$
m=-\frac{A}{B}
$$

dan titik potong dengan sumbu-$y$ adalah:

$$
c=-\frac{C}{B}
$$

Alasan syarat $B\ne0$ diperlukan adalah karena perubahan ke bentuk eksplisit memerlukan pembagian oleh $B$.

---

## 16. Garis Sejajar

Dua garis sejajar adalah dua garis pada bidang yang memiliki arah sama dan tidak berpotongan.

Untuk dua garis tidak vertikal, jika gradiennya masing-masing $m_1$ dan $m_2$, maka garis-garis tersebut sejajar jika:

$$
m_1=m_2
$$

Alasannya, gradien menyatakan arah kemiringan garis. Jika dua garis memiliki gradien yang sama, keduanya memiliki arah yang sama.

Untuk garis vertikal, semua garis vertikal saling sejajar karena semuanya memiliki arah yang sama, yaitu sejajar dengan sumbu-$y$.

---

## 17. Garis Berpotongan

Dua garis berpotongan adalah dua garis yang memiliki tepat satu titik persekutuan.

Untuk dua garis tidak vertikal, jika gradiennya berbeda, maka garis-garis tersebut berpotongan:

$$
m_1\ne m_2
$$

Alasannya, gradien berbeda menunjukkan arah kemiringan berbeda. Dua garis lurus dengan arah berbeda pada bidang akan bertemu pada satu titik, kecuali dalam kasus representasi yang tidak membentuk garis valid.

---

## 18. Garis Tegak Lurus

Dua garis tegak lurus adalah dua garis yang berpotongan membentuk sudut siku-siku.

Untuk dua garis tidak vertikal dan tidak horizontal, dengan gradien $m_1$ dan $m_2$, syarat tegak lurus adalah:

$$
m_1m_2=-1
$$

atau setara dengan:

$$
m_2=-\frac{1}{m_1}
$$

Alasan hubungan ini muncul adalah karena dua arah garis yang membentuk sudut siku-siku memiliki kemiringan yang saling berbalik tanda dan saling resiprokal.

Garis horizontal tegak lurus dengan garis vertikal.

Alasannya, garis horizontal sejajar dengan sumbu-$x$, sedangkan garis vertikal sejajar dengan sumbu-$y$. Kedua sumbu tersebut saling tegak lurus dalam sistem koordinat Kartesius.

---

## 19. Kedudukan Titik terhadap Garis

Kedudukan titik terhadap garis menyatakan apakah suatu titik berada pada garis atau tidak.

Misalkan garis dinyatakan oleh:

$$
Ax+By+C=0
$$

dan titik dinyatakan oleh:

$$
P(x_P,y_P)
$$

Titik $P$ berada pada garis jika:

$$
Ax_P+By_P+C=0
$$

Titik $P$ tidak berada pada garis jika:

$$
Ax_P+By_P+C\ne0
$$

Alasannya, persamaan garis adalah syarat yang harus dipenuhi oleh semua titik pada garis. Jika koordinat titik membuat ruas kiri bernilai nol, maka titik memenuhi syarat tersebut.

---

## 20. Titik Potong Dua Garis

Titik potong dua garis adalah titik yang terletak pada kedua garis sekaligus.

Jika dua garis dinyatakan sebagai:

$$
A_1x+B_1y+C_1=0
$$

dan

$$
A_2x+B_2y+C_2=0
$$

maka titik potongnya adalah pasangan $(x,y)$ yang memenuhi kedua persamaan tersebut secara bersamaan.

Secara aljabar, titik potong diperoleh dari sistem persamaan linear:

$$
\begin{cases}
A_1x+B_1y+C_1=0\\
A_2x+B_2y+C_2=0
\end{cases}
$$

Alasannya, titik potong harus menjadi anggota garis pertama dan garis kedua sekaligus. Karena setiap garis dinyatakan oleh persamaan, koordinat titik potong harus memenuhi kedua persamaan tersebut.

---

## 21. Kesetaraan Persamaan Garis

Dua persamaan garis disebut setara jika keduanya menyatakan himpunan titik yang sama.

Persamaan:

$$
Ax+By+C=0
$$

setara dengan:

$$
\lambda A x+\lambda B y+\lambda C=0
$$

dengan syarat:

$$
\lambda\ne0
$$

Alasan $\lambda$ tidak boleh nol adalah karena jika seluruh koefisien dikalikan nol, persamaan kehilangan variabel dan tidak lagi menyatakan garis yang sama.

Kesetaraan ini berarti satu garis dapat memiliki lebih dari satu bentuk persamaan. Perbedaan bentuk aljabar tidak selalu berarti perbedaan garis.

---

## 22. Koefisien dalam Persamaan Garis

Koefisien adalah konstanta yang mengalikan variabel dalam suatu persamaan.

Pada persamaan:

$$
Ax+By+C=0
$$

koefisien $x$ adalah $A$, koefisien $y$ adalah $B$, dan konstanta bebas adalah $C$.

Konstanta bebas adalah suku yang tidak memuat variabel.

Alasan koefisien penting adalah karena nilai koefisien menentukan arah dan posisi garis pada bidang Kartesius.

---

## 23. Garis sebagai Himpunan Penyelesaian

Persamaan garis dapat dipandang sebagai himpunan penyelesaian.

Untuk persamaan:

$$
Ax+By+C=0
$$

himpunan penyelesaiannya adalah:

$$
\{(x,y)\mid Ax+By+C=0\}
$$

Notasi tersebut berarti kumpulan semua pasangan $(x,y)$ yang memenuhi persamaan.

Alasan sudut pandang ini penting adalah karena garis bukan hanya gambar, tetapi juga himpunan titik yang memenuhi syarat aljabar tertentu.

---

## 24. Peran Variabel dan Konstanta

Dalam persamaan garis, variabel dan konstanta memiliki peran berbeda.

Variabel adalah simbol yang nilainya dapat berubah, seperti $x$ dan $y$.

Konstanta adalah simbol yang nilainya tetap dalam satu persamaan, seperti $A$, $B$, $C$, $m$, dan $c$.

Alasan pembedaan ini diperlukan adalah karena variabel menentukan titik-titik yang mungkin berada pada garis, sedangkan konstanta menentukan garis tertentu yang sedang dibahas.

---

## 25. Kemiringan dan Arah Garis

Kemiringan garis ditentukan oleh gradien.

Jika gradien bernilai positif, maka ketika $x$ bertambah, $y$ juga bertambah.

Jika gradien bernilai negatif, maka ketika $x$ bertambah, $y$ berkurang.

Jika gradien nol, garis horizontal.

Jika gradien tidak terdefinisi, garis vertikal.

Alasannya, gradien membandingkan perubahan $y$ terhadap perubahan $x$. Tanda dan keberadaan nilai gradien menunjukkan arah perubahan vertikal ketika terjadi perubahan horizontal.
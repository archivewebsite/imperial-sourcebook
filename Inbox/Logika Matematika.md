> [!abstract] Ringkasan  
> Logika matematika mempelajari cara menentukan kebenaran suatu pernyataan, membentuk pernyataan majemuk, menegasikan pernyataan, memakai kuantor, serta menarik kesimpulan yang valid dari beberapa premis.

## Konsep Dasar

Logika matematika digunakan untuk menilai apakah suatu pernyataan benar atau salah secara sistematis. Dalam matematika, logika penting karena menjadi dasar pembuktian, penalaran, dan penyusunan argumen.

Objek utama dalam logika adalah **proposisi**, yaitu kalimat yang memiliki nilai kebenaran.

## Proposisi

**Proposisi** adalah kalimat deklaratif yang dapat ditentukan bernilai **benar** atau **salah**, tetapi tidak keduanya sekaligus.

Contoh proposisi:

- Bandung adalah ibu kota Jawa Barat.  
    Nilai kebenaran: benar.
    
- 7 adalah faktor dari 10.  
    Nilai kebenaran: salah.
    
- $5 + 6 = 11$.  
    Nilai kebenaran: benar.
    
- 2 adalah bilangan prima.  
    Nilai kebenaran: benar.
    

Bukan proposisi:

- Semoga selamat sampai tujuan.  
    Kalimat harapan.
    
- Dilarang merokok.  
    Kalimat perintah atau larangan.
    
- Bunda sedang apa?  
    Kalimat tanya.
    
- $x - 8 < 7$.  
    Kalimat terbuka karena masih bergantung pada nilai $x$.
    

> [!warning] Koreksi penting  
> Kalimat seperti $x - 8 < 7$, $x$ faktor dari 7, dan $y + 4 = 6$ **bukan proposisi**, melainkan **kalimat terbuka**, karena nilai kebenarannya belum dapat ditentukan sebelum variabelnya diberi nilai.

## Kalimat Terbuka

**Kalimat terbuka** adalah kalimat yang memuat variabel sehingga nilai kebenarannya belum dapat ditentukan.

Contoh:

- $4x + 2 = 18$
    

Jika $x = 4$, maka:

$$
4(4) + 2 = 18  
$$

Pernyataan bernilai benar.

Jika $x = 5$, maka:

$$
4(5) + 2 = 22  
$$

Pernyataan bernilai salah.

Jadi, $4x + 2 = 18$ adalah kalimat terbuka karena nilai kebenarannya bergantung pada nilai $x$.

## Nilai Kebenaran

Nilai kebenaran suatu proposisi biasanya ditulis sebagai:

|Simbol|Arti|
|---|---|
|B|Benar|
|S|Salah|
|T|True|
|F|False|

Dalam catatan ini digunakan simbol **B** dan **S**.

## Operator Logika

Operator logika digunakan untuk membentuk pernyataan majemuk.

|Operator|Simbol|Dibaca|Bentuk|
|---|--:|---|---|
|Negasi|$\neg p$ atau $\sim p$|tidak $p$|ingkaran|
|Konjungsi|$p \land q$|$p$ dan $q$|dan|
|Disjungsi inklusif|$p \lor q$|$p$ atau $q$|atau|
|Disjungsi eksklusif|$p \oplus q$|$p$ atau $q$, tetapi tidak keduanya|xor|
|Implikasi|$p \to q$|jika $p$, maka $q$|sebab-akibat logis|
|Biimplikasi|$p \leftrightarrow q$|$p$ jika dan hanya jika $q$|ekuivalensi dua arah|

> [!note] Catatan simbol  
> Dalam logika matematika, kata "atau" biasanya berarti **atau inklusif**, yaitu tetap benar jika kedua pernyataan sama-sama benar. Untuk "atau tetapi tidak keduanya", gunakan **disjungsi eksklusif** atau $p \oplus q$. Ya, satu kata "atau" saja bisa bikin repot. Bahasa manusia, luar biasa.

## Negasi

Negasi dari proposisi $p$ ditulis $\neg p$.

Jika $p$ benar, maka $\neg p$ salah.  
Jika $p$ salah, maka $\neg p$ benar.

| P   | $\neg p$ |
| --- | -------- |
| B   | S        |
| S   | B        |

Contoh:

- $p$: $5 + 4 = 9$  
    $\neg p$: $5 + 4 \ne 9$
    
- $p$: Neneng memakai baju putih  
    $\neg p$: Neneng tidak memakai baju putih
    
- $p$: $2 + 5 > 9$  
    $\neg p$: $2 + 5 \le 9$
    

## Konjungsi

Konjungsi adalah pernyataan majemuk yang menggunakan kata hubung **dan**.

Bentuk:

$$
p \land q  
$$

Konjungsi bernilai benar hanya jika **kedua proposisi benar**.

|$p$|$q$|$p \land q$|
|---|---|---|
|B|B|B|
|B|S|S|
|S|B|S|
|S|S|S|

Contoh:

- $p$: $5 + 8 = 13$
    
- $q$: 2 adalah bilangan prima
    

Maka:

$$
p \land q  
$$

berarti "$5 + 8 = 13$ dan 2 adalah bilangan prima".

Karena keduanya benar, maka $p \land q$ bernilai benar.

## Disjungsi

Disjungsi adalah pernyataan majemuk yang menggunakan kata hubung **atau**.

### Disjungsi Inklusif

Bentuk:

$$
p \lor q  
$$

Disjungsi inklusif bernilai benar jika **minimal salah satu** dari $p$ atau $q$ benar.

|$p$|$q$|$p \lor q$|
|---|---|---|
|B|B|B|
|B|S|B|
|S|B|B|
|S|S|S|

Contoh:

- $p$: $3 + 5 = 8$
    
- $q$: Metro terletak di Palembang
    

Nilai kebenaran:

- $p$: benar
    
- $q$: salah
    

Maka:

$$
p \lor q  
$$

bernilai benar.

### Disjungsi Eksklusif

Bentuk:

$$
p \oplus q  
$$

Disjungsi eksklusif bernilai benar jika **tepat satu** dari $p$ atau $q$ benar.

|$p$|$q$|$p \oplus q$|
|---|---|---|
|B|B|S|
|B|S|B|
|S|B|B|
|S|S|S|

## Implikasi

Implikasi adalah pernyataan majemuk berbentuk:

$$
p \to q  
$$

Dibaca:

- Jika $p$, maka $q$.
    
- $p$ mengakibatkan $q$.
    
- $p$ adalah syarat cukup bagi $q$.
    
- $q$ adalah syarat perlu bagi $p$.
    

Dalam implikasi:

- $p$ disebut **anteseden**, **hipotesis**, atau **sebab**.
    
- $q$ disebut **konsekuen**, **konklusi**, atau **akibat**.
    

|$p$|$q$|$p \to q$|
|---|---|---|
|B|B|B|
|B|S|S|
|S|B|B|
|S|S|B|

Implikasi hanya salah ketika $p$ benar tetapi $q$ salah.

Contoh:

- $p$: 7 adalah bilangan prima.
    
- $q$: 7 habis dibagi 2.
    

Maka:

$$
p \to q  
$$

berbunyi:

"Jika 7 adalah bilangan prima, maka 7 habis dibagi 2."

Karena $p$ benar dan $q$ salah, maka implikasi tersebut bernilai salah.

## Biimplikasi

Biimplikasi adalah pernyataan majemuk berbentuk:

$$
p \leftrightarrow q  
$$

Dibaca:

- $p$ jika dan hanya jika $q$.
    
- $p$ ekuivalen dengan $q$.
    

Biimplikasi bernilai benar jika $p$ dan $q$ memiliki nilai kebenaran yang sama.

|$p$|$q$|$p \leftrightarrow q$|
|---|---|---|
|B|B|B|
|B|S|S|
|S|B|S|
|S|S|B|

Contoh:

- $p$: 10 adalah bilangan genap.
    
- $q$: 10 habis dibagi 2.
    

Keduanya benar, maka:

$$
p \leftrightarrow q  
$$

bernilai benar.

## Tabel Kebenaran Utama

|$p$|$q$|$\neg p$|$p \land q$|$p \lor q$|$p \oplus q$|$p \to q$|$p \leftrightarrow q$|
|---|---|---|---|---|---|---|---|
|B|B|S|B|B|S|B|B|
|B|S|S|S|B|B|S|S|
|S|B|B|S|B|B|B|S|
|S|S|B|S|S|S|B|B|

## Ingkaran Pernyataan Majemuk

Negasi pernyataan majemuk tidak boleh asal menambahkan kata "tidak". Ada aturannya. Mengejutkan sekali, matematika tidak menerima improvisasi bebas.

### Ingkaran Konjungsi

$$
\neg(p \land q) \equiv \neg p \lor \neg q  
$$

Contoh:

- $p$: Rudi sedang makan.
    
- $q$: Rudi sedang mendengarkan lagu.
    

Pernyataan:

$$
p \land q  
$$

"Rudi sedang makan dan mendengarkan lagu."

Negasinya:

$$
\neg p \lor \neg q  
$$

"Rudi tidak sedang makan atau Rudi tidak sedang mendengarkan lagu."

### Ingkaran Disjungsi

$$
\neg(p \lor q) \equiv \neg p \land \neg q  
$$

Contoh:

"Mahasiswa membawa pulpen atau pensil."

Negasinya:

"Mahasiswa tidak membawa pulpen dan tidak membawa pensil."

### Ingkaran Implikasi

$$
\neg(p \to q) \equiv p \land \neg q  
$$

Contoh:

Pernyataan:

"Jika saya belajar, maka saya lulus."

Negasinya:

"Saya belajar dan saya tidak lulus."

### Ingkaran Biimplikasi

$$
\neg(p \leftrightarrow q) \equiv (p \land \neg q) \lor (\neg p \land q)  
$$

Artinya, $p$ dan $q$ memiliki nilai kebenaran yang berbeda.

## Konvers, Invers, dan Kontraposisi

Dari implikasi:

$$
p \to q  
$$

dapat dibentuk tiga pernyataan baru.

|Bentuk|Rumus|Nama|
|---|---|---|
|Implikasi awal|$p \to q$|implikasi|
|Konvers|$q \to p$|konvers|
|Invers|$\neg p \to \neg q$|invers|
|Kontraposisi|$\neg q \to \neg p$|kontraposisi|

Hubungan penting:

$$
p \to q \equiv \neg q \to \neg p  
$$

Implikasi ekuivalen dengan kontraposisinya.

$$
q \to p \equiv \neg p \to \neg q  
$$

Konvers ekuivalen dengan inversnya.

Contoh:

Pernyataan awal:

"Jika harga BBM naik, maka harga beras naik."

- Konvers: Jika harga beras naik, maka harga BBM naik.
    
- Invers: Jika harga BBM tidak naik, maka harga beras tidak naik.
    
- Kontraposisi: Jika harga beras tidak naik, maka harga BBM tidak naik.
    

## Kuantor

Kuantor digunakan untuk mengubah kalimat terbuka menjadi pernyataan.

### Kuantor Universal

Kuantor universal ditulis:

$$
\forall  
$$

Dibaca:

- untuk semua
    
- setiap
    
- semua
    

Bentuk umum:

$$
(\forall x \in S), P(x)  
$$

Artinya:

"Untuk semua $x$ dalam semesta $S$, berlaku $P(x)$."

Contoh:

$$
(\forall x \in \mathbb{R}), x^2 \ge 0  
$$

Artinya:

"Untuk setiap bilangan real $x$, berlaku $x^2 \ge 0$."

Pernyataan ini benar.

> [!warning] Koreksi penting  
> Untuk membuktikan pernyataan universal benar, **tidak cukup memberi satu contoh**. Harus ditunjukkan bahwa pernyataan berlaku untuk semua anggota semesta. Satu contoh hanya cukup untuk membuktikan pernyataan eksistensial.

### Kuantor Eksistensial

Kuantor eksistensial ditulis:

$$
\exists  
$$

Dibaca:

- ada
    
- terdapat
    
- paling sedikit satu
    

Bentuk umum:

$$
(\exists x \in S), P(x)  
$$

Artinya:

"Ada paling sedikit satu $x$ dalam semesta $S$ sehingga $P(x)$ benar."

Contoh:

$$
(\exists x \in \mathbb{Z}), x^2 = x  
$$

Pernyataan ini benar karena $x = 0$ dan $x = 1$ memenuhi persamaan tersebut.

## Ingkaran Pernyataan Berkuantor

### Ingkaran Kuantor Universal

$$
\neg(\forall x), P(x) \equiv (\exists x), \neg P(x)  
$$

Artinya:

"Tidak benar bahwa semua $x$ memenuhi $P(x)$" sama dengan "Ada $x$ yang tidak memenuhi $P(x)$."

Contoh:

Pernyataan:

"Semua siswa telah pulang."

Negasi:

"Ada siswa yang belum pulang."

### Ingkaran Kuantor Eksistensial

$$
\neg(\exists x), P(x) \equiv (\forall x), \neg P(x)  
$$

Artinya:

"Tidak ada $x$ yang memenuhi $P(x)$" sama dengan "Semua $x$ tidak memenuhi $P(x)$."

Contoh:

Pernyataan:

$$
(\exists x \in \mathbb{Z}), x^2 = 9  
$$

Negasinya:

$$
(\forall x \in \mathbb{Z}), x^2 \ne 9  
$$

> [!warning] Koreksi penting  
> Negasi dari $(\exists x \in \mathbb{Z}), x^2 = 9$ bukan $(\exists x \in \mathbb{Z}), x^2 \ne 9$, melainkan $(\forall x \in \mathbb{Z}), x^2 \ne 9$.  
> Dalam catatan mentah juga muncul kalimat "tidak sama dengan 25", padahal pernyataan awalnya $x^2 = 9$. Itu harus diganti menjadi "tidak sama dengan 9".

## Tautologi, Kontradiksi, dan Kontingensi

### Tautologi

Tautologi adalah pernyataan majemuk yang selalu bernilai benar untuk semua kemungkinan nilai kebenaran komponennya.

Contoh:

$$
p \lor \neg p  
$$

|$p$|$\neg p$|$p \lor \neg p$|
|---|---|---|
|B|S|B|
|S|B|B|

Karena selalu benar, maka $p \lor \neg p$ adalah tautologi.

### Kontradiksi

Kontradiksi adalah pernyataan majemuk yang selalu bernilai salah.

Contoh:

$$
p \land \neg p  
$$

|$p$|$\neg p$|$p \land \neg p$|
|---|---|---|
|B|S|S|
|S|B|S|

Karena selalu salah, maka $p \land \neg p$ adalah kontradiksi.

### Kontingensi

Kontingensi adalah pernyataan majemuk yang kadang bernilai benar dan kadang bernilai salah.

Contoh:

$$
p \to q  
$$

|$p$|$q$|$p \to q$|
|---|---|---|
|B|B|B|
|B|S|S|
|S|B|B|
|S|S|B|

Karena ada nilai benar dan ada nilai salah, maka $p \to q$ adalah kontingensi.

## Ekuivalensi Logis

Dua pernyataan disebut ekuivalen secara logis jika keduanya memiliki nilai kebenaran yang sama untuk semua kemungkinan.

Ditulis:

$$
p \equiv q  
$$

## Hukum-Hukum Logika

### Hukum Identitas

$$
p \lor S \equiv p  
$$

$$
p \land B \equiv p  
$$

### Hukum Dominasi

$$
p \lor B \equiv B  
$$

$$
p \land S \equiv S  
$$

### Hukum Negasi

$$
p \lor \neg p \equiv B  
$$

$$
p \land \neg p \equiv S  
$$

### Hukum Idempoten

$$
p \lor p \equiv p  
$$

$$
p \land p \equiv p  
$$

### Hukum Negasi Ganda

$$
\neg(\neg p) \equiv p  
$$

### Hukum Komutatif

$$
p \lor q \equiv q \lor p  
$$

$$
p \land q \equiv q \land p  
$$

### Hukum Asosiatif

$$
p \lor (q \lor r) \equiv (p \lor q) \lor r  
$$

$$
p \land (q \land r) \equiv (p \land q) \land r  
$$

### Hukum Distributif

$$
p \lor (q \land r) \equiv (p \lor q) \land (p \lor r)  
$$

$$
p \land (q \lor r) \equiv (p \land q) \lor (p \land r)  
$$

### Hukum De Morgan

$$
\neg(p \land q) \equiv \neg p \lor \neg q  
$$

$$
\neg(p \lor q) \equiv \neg p \land \neg q  
$$

### Hukum Implikasi

$$
p \to q \equiv \neg p \lor q  
$$

### Hukum Biimplikasi

$$
p \leftrightarrow q \equiv (p \to q) \land (q \to p)  
$$

$$
p \leftrightarrow q \equiv (p \land q) \lor (\neg p \land \neg q)  
$$

## Inferensi Logika

Inferensi logika adalah proses menarik kesimpulan dari premis-premis.

Sebuah argumen dikatakan **valid** jika bentuk implikasi berikut adalah tautologi:

$$
(p_1 \land p_2 \land \cdots \land p_n) \to q  
$$

dengan:

- $p_1, p_2, \ldots, p_n$ sebagai premis.
    
- $q$ sebagai kesimpulan.
    

## Silogisme Hipotetis

Bentuk umum:

$$
p \to q  
$$

$$
q \to r  
$$

$$
\therefore p \to r  
$$

Contoh:

- Jika saya rajin belajar, maka saya mendapat nilai bagus.
    
- Jika saya mendapat nilai bagus, maka saya mendapat hadiah.
    
- Jadi, jika saya rajin belajar, maka saya mendapat hadiah.
    

## Modus Ponens

Bentuk umum:

$$
p \to q  
$$

$$
p  
$$

$$
\therefore q  
$$

Contoh:

- Jika saya makan, maka saya kenyang.
    
- Saya makan.
    
- Jadi, saya kenyang.
    

Modus ponens adalah bentuk argumen valid.

## Modus Tollens

Bentuk umum:

$$
p \to q  
$$

$$
\neg q  
$$

$$
\therefore \neg p  
$$

Contoh:

- Jika saya makan, maka saya kenyang.
    
- Saya tidak kenyang.
    
- Jadi, saya tidak makan.
    

> [!warning] Koreksi penting  
> Bentuk "Jika saya makan maka saya kenyang. Saya tidak makan. Jadi saya tidak kenyang" **tidak valid**. Itu disebut kesalahan **denying the antecedent**. Dari tidak makan, belum tentu tidak kenyang, karena bisa saja kenyang karena minum susu, makan sebelumnya, atau karena semesta memang hobi membuat kasus tepi.

## Simplifikasi

Bentuk umum:

$$
p \land q  
$$

$$
\therefore p  
$$

atau:

$$
p \land q  
$$

$$
\therefore q  
$$

Contoh:

- Rudi memiliki mobil dan motor.
    
- Jadi, Rudi memiliki mobil.
    

Atau:

- Rudi memiliki mobil dan motor.
    
- Jadi, Rudi memiliki motor.
    

## Konjungsi

Bentuk umum:

$$
p  
$$

$$
q  
$$

$$
\therefore p \land q  
$$

Contoh:

- 2 adalah bilangan prima.
    
- 4 adalah bilangan genap.
    
- Jadi, 2 adalah bilangan prima dan 4 adalah bilangan genap.
    

## Penambahan

Bentuk umum:

$$
p  
$$

$$
\therefore p \lor q  
$$

Contoh:

- Saya belajar.
    
- Jadi, saya belajar atau saya tidur.
    

Secara logika bentuk ini valid, meskipun secara bahasa terdengar seperti alasan manusia yang sedang menghindari tanggung jawab.

## Kesalahan Inferensi yang Sering Terjadi

### Affirming the Consequent

Bentuk keliru:

$$
p \to q  
$$

$$
q  
$$

$$
\therefore p  
$$

Contoh:

- Jika hujan, maka jalan basah.
    
- Jalan basah.
    
- Jadi, hujan.
    

Kesimpulan tidak valid, karena jalan bisa basah karena disiram, banjir, atau tetangga sedang mencuci kendaraan dengan ambisi berlebihan.

### Denying the Antecedent

Bentuk keliru:

$$
p \to q  
$$

$$
\neg p  
$$

$$
\therefore \neg q  
$$

Contoh:

- Jika saya makan, maka saya kenyang.
    
- Saya tidak makan.
    
- Jadi, saya tidak kenyang.
    

Kesimpulan tidak valid.

## Contoh Klasifikasi Kalimat

|Kalimat|Jenis|Nilai Kebenaran|
|---|---|---|
|Jawa Barat terletak di Pulau Sumatra|proposisi|salah|
|$3 + 7 \le 4 + 5$|proposisi|salah|
|Semoga lekas sembuh|bukan proposisi|tidak ada|
|$x > 10$|kalimat terbuka|bergantung pada $x$|
|3 adalah faktor dari 15|proposisi|benar|
|Mari kita belajar|bukan proposisi|tidak ada|

## Contoh Negasi

|Pernyataan|Negasi|
|---|---|
|10 adalah bilangan bulat positif|10 bukan bilangan bulat positif|
|$10 + 6 \le 15$|$10 + 6 > 15$|
|Semua guru memakai baju putih|Ada guru yang tidak memakai baju putih|
|Ada burung yang tidak bisa terbang|Semua burung bisa terbang|
|Semua siswa lulus ujian|Ada siswa yang tidak lulus ujian|

## Catatan Koreksi dari Versi Mentah

> [!warning] Bagian yang perlu diperbaiki  
> Beberapa bagian catatan mentah perlu dikoreksi agar tidak menyesatkan ketika dipakai belajar.

- Kalimat $x - 8 < 7$, $x$ faktor dari 7, dan $y + 4 = 6$ harus diklasifikasikan sebagai **kalimat terbuka**, bukan proposisi.
    
- Negasi dari $p \land q$ adalah $\neg p \lor \neg q$, bukan $\neg(p \lor q)$.
    
- Negasi dari $p \lor q$ adalah $\neg p \land \neg q$, bukan $\neg(p \land q)$.
    
- Negasi dari $(\exists x)P(x)$ adalah $(\forall x)\neg P(x)$, bukan tetap memakai $\exists$.
    
- Untuk membuktikan pernyataan universal, satu contoh tidak cukup.
    
- Modus tollens harus berbentuk $p \to q$, $\neg q$, maka $\neg p$. Bukan $p \to q$, $\neg p$, maka $\neg q$.
    
- Pada implikasi $p \to q$, $p$ adalah **syarat cukup** bagi $q$, sedangkan $q$ adalah **syarat perlu** bagi $p$.
    
- Gunakan simbol $p \oplus q$ untuk disjungsi eksklusif agar tidak tertukar dengan disjungsi inklusif $p \lor q$.
    

## Latihan Singkat

> [!question] Latihan  
> Tentukan jenis kalimat berikut: proposisi, kalimat terbuka, atau bukan proposisi.

- Gunung Bromo terletak di Jawa Tengah.
    
- Nabi Muhammad adalah utusan Allah.
    
- Pergi saja kamu dari sini.
    
- $6 + x > 9$.
    
- 35 habis dibagi 2.
    
- Semoga kamu berhasil.
    

> [!question] Latihan  
> Tentukan negasi dari pernyataan berikut.

- Semua mahasiswa hadir.
    
- Ada siswa yang tidak mengumpulkan tugas.
    
- Jika saya belajar, maka saya lulus.
    
- $p \land q$.
    
- $p \to q$.
    

> [!question] Latihan  
> Tentukan konvers, invers, dan kontraposisi dari pernyataan berikut.

"Jika saya lapar, maka saya makan."

## Jawaban Ringkas

### Klasifikasi Kalimat

|Kalimat|Jenis|
|---|---|
|Gunung Bromo terletak di Jawa Tengah|proposisi|
|Nabi Muhammad adalah utusan Allah|proposisi|
|Pergi saja kamu dari sini|bukan proposisi|
|$6 + x > 9$|kalimat terbuka|
|35 habis dibagi 2|proposisi|
|Semoga kamu berhasil|bukan proposisi|

### Negasi

|Pernyataan|Negasi|
|---|---|
|Semua mahasiswa hadir|Ada mahasiswa yang tidak hadir|
|Ada siswa yang tidak mengumpulkan tugas|Semua siswa mengumpulkan tugas|
|Jika saya belajar, maka saya lulus|Saya belajar dan saya tidak lulus|
|$p \land q$|$\neg p \lor \neg q$|
|$p \to q$|$p \land \neg q$|

### Konvers, Invers, dan Kontraposisi

Pernyataan awal:

$$
p \to q  
$$

"Jika saya lapar, maka saya makan."

|Bentuk|Pernyataan|
|---|---|
|Konvers|Jika saya makan, maka saya lapar|
|Invers|Jika saya tidak lapar, maka saya tidak makan|
|Kontraposisi|Jika saya tidak makan, maka saya tidak lapar|

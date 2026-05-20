![Image](https://pbs.twimg.com/media/HCxVWWSbgAAxRS2?format=jpg&name=large)

Artikel ini dibuat dari permasalahan matematika dari :

[https://x.com/yourmathsphere/status/2029668140028940325?s=20](https://x.com/yourmathsphere/status/2029668140028940325?s=20)

Bayangkan ada sepasang manusia, sebut saja namanya Naya dan Audi, Mereka mencintai satu sama lain. Si Naya, laki-laki puber ini mau ketemu dengan pacarnya... Dan berdasarkan ilustrasi di gambar :

![Image](https://pbs.twimg.com/media/HCxWPmZbgAAnKkM?format=png&name=large)

Gambar 1.1 : Terdapat 2 cara Audi dan Naya bisa bertemu.

Setidaknya Naya bisa bertemu dengan Audi dengan 2 cara, Yakni (Kanan, Atas) atau (Atas, Kanan)

Simpel, cukup dengan 2 cara saja.

Tapi, ini bukan permasalahan utama... Bagaimana jika jarak Naya dan Audi sangat jauh? Bagaimana jika jaraknya butuh melewati beberapa rumah, berapa cara ?

![Image](https://pbs.twimg.com/media/HCxX0D4aUAAZYna?format=png&name=large)

Gambar 1.2 : Naya dan Audi memiliki beberapa jarak kota yang sangat jauh

Aturan permainannya sederhana, gerakannya hanya ke-kanan atau ke-atas.

Jika semua jalan K1 semua di-blokir, kira-kira ada berapa cara Mas Naya ini bisa sampai ke Kak Audi?

[#Cara](https://x.com/search?q=%23Cara&src=hashtag_click) **1 : Menggunakan Teori Kombinatorika**

**Kombinatorika** ini dibagi menjadi 2 tipe : > **Permutasi** merupakan pengambilan cara dengan memerhatikan urutan **> Kombinasi** merupakan tanpa memerhatikan pengambilan urutan.

Kasus ini termasuk **tipe Permutasi**, kasus ini termasuk tipe permutasi dari himpunan n unsur yang memuat p, q, dan r unsur yang sama.

**Rumusnya sebagai berikut :**

$$
P(k1,k2,…,kt)=n!k1!k2!…kt!P_{(k_1,k_2,\dots,k_t)} = \dfrac{n!}{k_1! k_2! \dots k_t!}
$$

Keterangan : n = Jumlah semua elemen yang ada k1 = Jumlah elemen yang sama pada kelompok ke-1 k2 = Jumlah elemen yang sama pada kelompok ke-2 kt = Jumlah elemen yang sama pada kelompok ke-t

![Image](https://pbs.twimg.com/media/HCxptFpbwAAnvFU?format=png&name=large)

Gambar 2.1 Konsep semua kemungkinan cara Naya menuju ke tempat Audi

Semua cara membutuhkan 6 Langkah, dan terbagi menjadi 3 ke-kanan dan 3ke-kiri. Misal : H3 (Kanan) K3 (Kanan) H4 (Atas) B4 (Kanan) M4 (Atas) K2 (Atas) M2

Kita akan menyebutnya sebagai => P(KKKNNN), melambangkan 3 Kanan dan 3 Atas, dan kita bisa menyelesaikan dengan rumus sebagai berikut :

$$
P(KKKNNN)=(3+3)!3!3!=6!3!3!=6×5×4×3!3!×6=5×4=20P(KKKNNN) = \dfrac{(3+3)!}{3! 3!} \\ = \dfrac{6!}{3! 3!} \\ = \dfrac{6 \times 5 \times 4 \times 3!}{3! \times 6} \\ = 5 \times 4 \\ = 20
$$

Ini adalah semua cara, tapi bagaimana dengan kasus yang melewati Kota K1? Karena menuju K1 Itu memiliki 2 cara, yakni lewat H1(KNN - 1 Kanan, 2 Naik) dan M3(KKN - 2 Kanan, 1 Naik)

**Dengan rumus yang sama :**

$$
P(H1→K1)×P(M3→K1)=3!1!2!×3!2!1!=61×2×62×1=3×3=9P(H1 \to K1) \times P(M3 \to K1) = \dfrac{3!}{1! 2!} \times \dfrac{3!}{2! 1!} \\ = \dfrac{6}{1 \times 2} \times \dfrac{6}{2 \times 1} \\ = 3 \times 3 \\ = 9
$$

Karena akses K1 diblokir, maka artinya opsi perjalanan dikurangi, sehingga :

**20 - 9 = 11 Cara**

**Menggunakan Teori Kombinatorika(Permutasi)**, Cara Naya menuju ke tempat Audi sebanyak 11 Cara

[#Cara](https://x.com/search?q=%23Cara&src=hashtag_click) **2 : Menggunakan Konsep Segitiga Pascal**

Sebelum menentukan caranya, kalian harus mengetahui apa itu konsep **Segitiga Pascal**

**Sebenarnya** konsep ini memang di ambil dari kombinatorika, tapi konsep yang saya ambil adalah **cara alternatif bagaimana menentukan total dari jalan yang bisa ditempuh** :

![Image](https://pbs.twimg.com/media/HCxz3TKaIAARp5l?format=png&name=large)

Gambar 3.1 : Segitiga Pascal dan jumlah rute dam bagaimana bilangan tersebut memiliki pola.

Kalau dilihat pada gambar, misal pada baris ke-2 urutan ke-2, terdapat bilangan 2, dan terdapat 2 panah yang berasal dari 1. Hal ini menunjukkan bahwa untuk mendapatkan 2, diperlukan 1 + 1 cara.

Konsep ini juga pernah saya praktekkan pada [#TriviaSahur](https://x.com/search?q=%23TriviaSahur&src=hashtag_click) pada : [https://x.com/yourmathsphere/status/2027863022879052108?s=20](https://x.com/yourmathsphere/status/2027863022879052108?s=20)

> Bagaimana hubungan konsep segitiga pascal dan masalah kasus menemukan jalan?

Lihat gambar ini :

![Image](https://pbs.twimg.com/media/HCx1EigakAAvVFs?format=png&name=large)

Gambar 3.2 Konsep Segitiga Pascal yang diadaptasi untuk kasus perjalanan Naya menuju Audi

Contoh, untuk rute H3 ke M3, DIbutuhkan 2 cara : H3 => K3(Kanan) => M3(Atas) H3 => B3(Kanan) => M3(Atas)

Kemudian, kita tingkatkan kesulitannya, dengan menuju ke B4. Dengan cara yang sama : H3 => K3(Kanan) => M3(Atas) => B4 H3 => B3(Kanan) => M3(Atas) => B4 H3 => K3(Kanan) => H4(Kanan) => B4

Bisa diperhatikan bahwa cara menuju B4 lewat M3 tetap membutuhkan 2 cara, sedangkan alternatifnya lewat H4 dengan 1 cara, hasilnya dijumlah, yaitu **2 + 1 cara = 3 cara**

**Jadi, Konsep Segitiga Pascal bisa diaplikasikan ke permasalahan ini.**

**Bagaimana hasil final dari konsep ini? Ini dia gambarannya :**

![Image](https://pbs.twimg.com/media/HCx3RSubgAAVYru?format=png&name=large)

Gambar 3.3 : Hasilnya juga 11 Cara

**Menurut konsep segitiga pascal, total cara Naya menuju ke tempat Audi adalah 11 Cara.**

Bagaimana? Konsepnya menarik bukan? Cara ini tidak menghitung perkalian, tetapi melakukan penjumlahan. Cara ini memang cenderung lebih lama, tetapi memakai konsep yang lebih sederhana.

Terima kasih karena sudah meluangkan waktu untuk membaca artikel ini. Semoga bermanfaat :D
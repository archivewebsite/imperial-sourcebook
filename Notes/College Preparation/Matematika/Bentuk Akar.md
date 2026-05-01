---
title: Bentuk Akar
mata_pelajaran: Matematika
tanggal: 30 April 2026
materi: Bentuk Akar
tags:
  - matematika
  - aljabar
  - bentuk-akar
  - bilangan-real
  - eksponen
aliases:
  - Radikal
  - Akar
  - Surd
---

# Bentuk Akar

## Konvensi Notasi

Dalam catatan ini, huruf seperti \(A\), \(B\), \(C\), \(D\), \(P\), \(Q\), \(R\), dan \(S\) menyatakan objek matematika umum. Objek tersebut dapat berupa bilangan, bentuk aljabar, atau ekspresi lain, bergantung pada syarat yang ditulis bersama rumusnya.

Simbol \(\mathbb{R}\) menyatakan himpunan [[Bilangan Real]], yaitu himpunan bilangan yang dapat ditempatkan pada garis bilangan real.

Simbol \(\mathbb{Q}\) menyatakan himpunan [[Bilangan Rasional]], yaitu bilangan yang dapat ditulis sebagai hasil bagi dua bilangan bulat dengan penyebut tidak sama dengan nol.

Simbol \(\mathbb{Z}\) menyatakan himpunan [[Bilangan Bulat]].

Simbol \(\mathbb{N}\) menyatakan himpunan [[Bilangan Asli]], yaitu bilangan yang digunakan untuk menghitung banyaknya objek.

Simbol \(>\), \(\ge\), \(<\), dan \(\le\) masing-masing menyatakan relasi lebih dari, lebih dari atau sama dengan, kurang dari, dan kurang dari atau sama dengan.

Simbol \(\in\) berarti “anggota dari”.

Simbol \(\notin\) berarti “bukan anggota dari”.

Simbol \(\neq\) berarti “tidak sama dengan”.

Simbol \(\iff\) berarti “jika dan hanya jika”.

Simbol \(:=\) berarti “didefinisikan sebagai”.

---

## Bilangan Real

> [!definisi]
> [[Bilangan Real]] adalah bilangan yang dapat direpresentasikan sebagai titik pada garis bilangan.

Bilangan real mencakup bilangan rasional dan bilangan irasional.

> [!definisi]
> [[Bilangan Rasional]] adalah bilangan yang dapat dinyatakan dalam bentuk hasil bagi dua bilangan bulat dengan penyebut tidak nol.

> [!definisi]
> [[Bilangan Irasional]] adalah bilangan real yang tidak dapat dinyatakan sebagai hasil bagi dua bilangan bulat dengan penyebut tidak nol.

> [!alasan]
> Bentuk akar sering menghasilkan bilangan irasional, sehingga perbedaan antara bilangan rasional dan irasional perlu didefinisikan sebelum membahas penyederhanaan akar.

---

## Operasi Perpangkatan

> [!definisi]
> Perpangkatan adalah operasi yang menyatakan pengulangan perkalian suatu bilangan atau ekspresi terhadap dirinya sendiri.

Bentuk umum perpangkatan ditulis sebagai

\[
A^n
\]

dengan:
- \(A\) disebut **basis**.
- \(n\) disebut **eksponen** atau **pangkat**.

Jika \(n\) adalah bilangan bulat positif, maka \(A^n\) berarti hasil perkalian \(A\) sebanyak \(n\) faktor yang sama.

> [!alasan]
> Akar didefinisikan sebagai operasi kebalikan dari perpangkatan tertentu. Karena itu, perpangkatan harus dipahami sebelum akar.

---

## Pangkat Genap dan Pangkat Ganjil

> [!definisi]
> Pangkat genap adalah perpangkatan dengan eksponen bilangan genap.

> [!definisi]
> Pangkat ganjil adalah perpangkatan dengan eksponen bilangan ganjil.

Dalam bilangan real:

\[
A^{\text{genap}} \ge 0
\]

untuk setiap \(A \in \mathbb{R}\).

> [!alasan]
> Hasil pangkat genap tidak negatif karena faktor negatif berpasangan menghasilkan nilai positif, sedangkan faktor positif tetap menghasilkan nilai positif, dan nol tetap nol.

Untuk pangkat ganjil, tanda hasil mengikuti tanda basis.

> [!alasan]
> Pada pangkat ganjil, faktor negatif tidak semuanya berpasangan, sehingga satu faktor negatif tersisa dan membuat hasilnya negatif.

---

## Akar

> [!definisi]
> Akar adalah operasi yang mencari suatu bilangan atau ekspresi yang jika dipangkatkan dengan indeks tertentu menghasilkan bilangan atau ekspresi semula.

Bentuk umum akar adalah

\[
\sqrt[n]{A}
\]

dengan:
- \(n\) disebut **indeks akar**.
- \(A\) disebut **radikan**.
- \(\sqrt{\phantom{A}}\) disebut **tanda akar** atau **radikal**.
- \(\sqrt[n]{A}\) disebut **bentuk radikal**.

> [!definisi]
> Indeks akar adalah bilangan yang menunjukkan pangkat yang menjadi pasangan kebalikan dari operasi akar.

> [!definisi]
> Radikan adalah ekspresi yang berada di bawah tanda akar.

> [!definisi]
> Tanda akar adalah simbol yang menyatakan operasi akar.

Secara konseptual,

\[
\sqrt[n]{A}=B
\]

berarti

\[
B^n=A
\]

dengan syarat domain yang sesuai.

> [!alasan]
> Definisi ini menunjukkan bahwa akar bukan operasi yang berdiri sendiri tanpa hubungan dengan pangkat; akar ditentukan oleh pangkat yang menjadi kebalikannya.

---

## Akar Kuadrat

> [!definisi]
> Akar kuadrat adalah akar dengan indeks dua.

Akar kuadrat ditulis

\[
\sqrt{A}
\]

dan secara formal berarti

\[
\sqrt{A}=\sqrt[2]{A}
\]

Dalam penulisan standar, indeks dua tidak ditulis.

> [!alasan]
> Indeks dua dihilangkan karena akar kuadrat adalah bentuk akar yang paling umum digunakan, sehingga notasi disederhanakan secara konvensional.

Dalam bilangan real, \(\sqrt{A}\) terdefinisi jika

\[
A \ge 0
\]

> [!alasan]
> Tidak ada bilangan real yang kuadratnya negatif. Karena akar kuadrat mencari bilangan real yang kuadratnya sama dengan radikan, radikan akar kuadrat harus tidak negatif.

---

## Akar Pangkat \(n\)

> [!definisi]
> Akar pangkat \(n\) adalah akar dengan indeks \(n\), yaitu operasi yang mencari suatu nilai yang jika dipangkatkan \(n\) menghasilkan radikan.

Bentuknya adalah

\[
\sqrt[n]{A}
\]

dengan \(n \in \mathbb{N}\) dan \(n>1\).

Syarat realnya bergantung pada paritas indeks.

Jika \(n\) genap, maka

\[
\sqrt[n]{A}
\]

terdefinisi dalam \(\mathbb{R}\) hanya jika

\[
A \ge 0
\]

Jika \(n\) ganjil, maka

\[
\sqrt[n]{A}
\]

terdefinisi dalam \(\mathbb{R}\) untuk setiap

\[
A \in \mathbb{R}
\]

> [!alasan]
> Pangkat genap tidak dapat menghasilkan bilangan negatif dalam bilangan real, sedangkan pangkat ganjil dapat menghasilkan bilangan positif, nol, atau negatif sesuai tanda basis.

---

## Nilai Utama Akar

> [!definisi]
> Nilai utama akar adalah nilai yang dipilih sebagai hasil standar dari operasi akar.

Untuk akar berindeks genap, nilai utama dalam bilangan real adalah nilai tidak negatif.

\[
\sqrt[n]{A} \ge 0
\]

jika \(n\) genap dan \(A \ge 0\).

> [!alasan]
> Jika \(n\) genap dan \(A>0\), ada dua bilangan real yang pangkat \(n\)-nya menghasilkan \(A\), yaitu satu positif dan satu negatif. Agar operasi akar menjadi fungsi bernilai tunggal, dipilih nilai utama yang tidak negatif.

Untuk akar berindeks ganjil, nilai utama memiliki tanda yang sama dengan radikan.

> [!alasan]
> Pangkat ganjil mempertahankan tanda basis, sehingga akar ganjil dari radikan negatif bernilai negatif, akar ganjil dari radikan positif bernilai positif, dan akar ganjil dari nol bernilai nol.

---

## Bentuk Akar

> [!definisi]
> Bentuk akar adalah bentuk matematika yang memuat operasi akar terhadap suatu radikan.

Bentuk akar dapat berupa:
- akar dari bilangan,
- akar dari ekspresi aljabar,
- kombinasi akar dengan operasi aljabar,
- akar bertingkat,
- akar yang dinyatakan sebagai eksponen pecahan.

> [!definisi]
> Bentuk akar sederhana adalah bentuk akar yang radikannya tidak lagi memuat faktor yang dapat dikeluarkan dari tanda akar sesuai indeksnya.

> [!alasan]
> Penyederhanaan bentuk akar bertujuan memisahkan bagian radikan yang merupakan pangkat sempurna terhadap indeks akar, karena bagian tersebut dapat ditulis di luar tanda akar.

---

## Pangkat Sempurna terhadap Indeks Akar

> [!definisi]
> Pangkat sempurna terhadap indeks \(n\) adalah ekspresi yang dapat ditulis sebagai pangkat \(n\) dari ekspresi lain.

Jika

\[
A=B^n
\]

maka \(A\) adalah pangkat sempurna terhadap indeks \(n\).

Dalam konteks akar,

\[
\sqrt[n]{B^n}
\]

berhubungan langsung dengan \(B\), tetapi hasil pastinya bergantung pada paritas \(n\).

Jika \(n\) ganjil, maka

\[
\sqrt[n]{B^n}=B
\]

Jika \(n\) genap, maka

\[
\sqrt[n]{B^n}=|B|
\]

> [!alasan]
> Untuk indeks ganjil, pangkat \(n\) mempertahankan tanda basis. Untuk indeks genap, pangkat \(n\) menghapus tanda basis, sehingga akar utama harus bernilai tidak negatif; nilai tidak negatif dari \(B\) ditulis sebagai \(|B|\).

---

## Nilai Mutlak

> [!definisi]
> Nilai mutlak dari suatu bilangan real adalah jarak bilangan tersebut dari nol pada garis bilangan.

Nilai mutlak ditulis

\[
|A|
\]

dan selalu memenuhi

\[
|A| \ge 0
\]

Nilai mutlak diperlukan dalam akar berindeks genap karena akar utama harus tidak negatif.

Hubungan pentingnya adalah

\[
\sqrt{A^2}=|A|
\]

dan secara umum, untuk \(n\) genap,

\[
\sqrt[n]{A^n}=|A|
\]

> [!alasan]
> Akar berindeks genap menghasilkan nilai utama yang tidak negatif, sedangkan \(A\) sendiri dapat bernilai negatif, nol, atau positif. Nilai mutlak menjamin hasilnya selalu tidak negatif.

---

## Radikan

> [!definisi]
> Radikan adalah ekspresi yang dikenai operasi akar.

Pada bentuk

\[
\sqrt[n]{A}
\]

radikannya adalah \(A\).

Radikan dapat berupa:
- bilangan real,
- ekspresi aljabar,
- hasil operasi penjumlahan,
- hasil operasi pengurangan,
- hasil operasi perkalian,
- hasil operasi pembagian,
- bentuk berpangkat,
- bentuk akar lain.

Syarat radikan bergantung pada indeks akar.

Jika indeks genap, radikan harus memenuhi

\[
A \ge 0
\]

Jika indeks ganjil, radikan boleh berupa sembarang bilangan real.

> [!alasan]
> Pembatasan ini berasal dari sifat pangkat genap dan pangkat ganjil pada bilangan real.

---

## Indeks Akar

> [!definisi]
> Indeks akar adalah bilangan yang menentukan jenis akar dan menentukan pangkat kebalikannya.

Pada

\[
\sqrt[n]{A}
\]

indeksnya adalah \(n\).

Indeks akar harus memenuhi

\[
n \in \mathbb{N}, \quad n>1
\]

> [!alasan]
> Indeks satu tidak membentuk operasi akar yang bermakna baru karena \(\sqrt[1]{A}=A\). Indeks nol tidak digunakan karena pangkat nol tidak dapat dibalik secara unik.

Indeks akar memengaruhi:
- syarat radikan,
- tanda hasil akar,
- aturan penyederhanaan,
- hubungan akar dengan eksponen pecahan,
- bentuk domain fungsi akar.

---

## Radikal

> [!definisi]
> Radikal adalah tanda atau struktur notasi yang menyatakan operasi akar.

Bentuk radikal mencakup tanda akar, indeks akar, dan radikan.

\[
\sqrt[n]{A}
\]

merupakan satu bentuk radikal lengkap.

> [!alasan]
> Dalam aljabar, istilah “radikal” sering digunakan bukan hanya untuk simbol akar, tetapi juga untuk keseluruhan bentuk yang memuat akar.

---

## Bentuk Akar dan Bilangan Irasional

Tidak semua bentuk akar bernilai irasional.

> [!definisi]
> Akar eksak adalah akar yang hasilnya dapat dinyatakan tanpa tanda akar karena radikannya merupakan pangkat sempurna terhadap indeks akar.

> [!definisi]
> Akar tidak eksak adalah akar yang tidak dapat dinyatakan sebagai bentuk tanpa tanda akar dalam sistem bilangan yang sedang digunakan.

Dalam bilangan rasional, bentuk akar sering menjadi irasional ketika radikan bukan pangkat sempurna yang sesuai dengan indeksnya.

> [!alasan]
> Jika suatu radikan bukan pangkat sempurna terhadap indeks akar, maka tidak ada bilangan rasional yang dipangkatkan sesuai indeks tersebut menghasilkan radikan. Akibatnya, nilai akar tidak dapat ditulis sebagai hasil bagi dua bilangan bulat.

---

## Bentuk Akar sebagai Eksponen Pecahan

> [!definisi]
> Eksponen pecahan adalah eksponen yang berbentuk hasil bagi dua bilangan bulat.

Akar dapat ditulis sebagai eksponen pecahan.

\[
\sqrt[n]{A}=A^{\frac{1}{n}}
\]

dengan syarat bahwa ruas kiri dan ruas kanan terdefinisi dalam sistem bilangan yang sama.

Lebih umum,

\[
\sqrt[n]{A^m}=A^{\frac{m}{n}}
\]

dan

\[
\left(\sqrt[n]{A}\right)^m=A^{\frac{m}{n}}
\]

dengan syarat domain yang sesuai.

> [!alasan]
> Pangkat \(\frac{1}{n}\) didefinisikan sebagai operasi kebalikan dari pangkat \(n\), sehingga notasi eksponen pecahan menyatukan operasi akar dan perpangkatan dalam satu sistem.

---

## Urutan Operasi pada Bentuk Akar

> [!definisi]
> Urutan operasi adalah aturan yang menentukan operasi mana yang dikerjakan lebih dahulu dalam suatu ekspresi.

Dalam bentuk akar, operasi yang berada di dalam radikan dianggap sebagai bagian dari radikan.

Pada bentuk

\[
\sqrt[n]{A+B}
\]

radikannya adalah seluruh ekspresi \(A+B\), bukan hanya \(A\) atau \(B\).

Pada bentuk

\[
\sqrt[n]{AB}
\]

radikannya adalah seluruh ekspresi \(AB\).

> [!alasan]
> Garis akar berfungsi seperti tanda pengelompokan. Semua ekspresi di bawah garis akar menjadi satu kesatuan radikan.

---

## Domain Bentuk Akar

> [!definisi]
> Domain adalah himpunan semua nilai masukan yang membuat suatu ekspresi terdefinisi.

Untuk bentuk akar berindeks genap,

\[
\sqrt[n]{A}
\]

dengan \(n\) genap, domain ditentukan oleh syarat

\[
A \ge 0
\]

Untuk bentuk akar berindeks ganjil,

\[
\sqrt[n]{A}
\]

dengan \(n\) ganjil, domain mencakup semua nilai yang membuat \(A\) sendiri terdefinisi.

> [!alasan]
> Akar genap memerlukan radikan tidak negatif dalam bilangan real. Akar ganjil tidak memiliki pembatasan tanda radikan, tetapi tetap mengikuti syarat agar radikan sebagai ekspresi bermakna.

---

## Kodomain dan Nilai Akar

> [!definisi]
> Kodomain adalah himpunan tujuan nilai keluaran suatu fungsi atau operasi.

> [!definisi]
> Range adalah himpunan nilai keluaran yang benar-benar dihasilkan.

Untuk akar genap utama,

\[
\sqrt[n]{A} \ge 0
\]

sehingga nilai keluarannya tidak negatif.

Untuk akar ganjil,

\[
\sqrt[n]{A}
\]

dapat bernilai negatif, nol, atau positif.

> [!alasan]
> Perbedaan ini berasal dari sifat pangkat genap yang tidak dapat menghasilkan bilangan negatif, sedangkan pangkat ganjil dapat menghasilkan semua tanda bilangan real.

---

## Kesetaraan Bentuk Akar

> [!definisi]
> Dua bentuk akar disebut setara jika keduanya memiliki nilai yang sama untuk semua nilai yang berada dalam domain bersama keduanya.

Kesetaraan bentuk akar harus memperhatikan:
- indeks akar,
- radikan,
- domain,
- nilai utama,
- tanda ekspresi,
- syarat pembagi tidak nol bila ada pecahan.

> [!alasan]
> Bentuk yang tampak serupa dapat memiliki domain berbeda. Dalam aljabar, kesetaraan tidak cukup dilihat dari kemiripan simbol, tetapi harus dilihat dari nilai dan syarat keberlakuannya.

---

## Operasi Penjumlahan Bentuk Akar

> [!definisi]
> Penjumlahan bentuk akar adalah operasi menjumlahkan dua atau lebih ekspresi yang memuat akar.

Bentuk akar hanya dapat digabungkan langsung jika memiliki bagian akar yang sejenis.

> [!definisi]
> Akar sejenis adalah bentuk akar yang memiliki indeks akar sama dan radikan sama setelah disederhanakan.

Jika dua bentuk akar sejenis, maka koefisiennya dapat dijumlahkan.

\[
P\sqrt[n]{A}+Q\sqrt[n]{A}=(P+Q)\sqrt[n]{A}
\]

> [!alasan]
> Bagian \(\sqrt[n]{A}\) berperan sebagai faktor yang sama. Berdasarkan sifat distributif, faktor yang sama dapat dikeluarkan dari penjumlahan koefisien.

Jika akar tidak sejenis, penjumlahan tidak dapat digabungkan menjadi satu akar sederhana.

\[
\sqrt[n]{A}+\sqrt[n]{B}\neq \sqrt[n]{A+B}
\]

secara umum.

> [!alasan]
> Akar adalah operasi kebalikan dari pangkat, bukan operasi linear terhadap penjumlahan. Pangkat dari jumlah tidak sama dengan jumlah pangkat masing-masing bagian, sehingga akar dari jumlah tidak sama dengan jumlah akar secara umum.

---

## Operasi Pengurangan Bentuk Akar

> [!definisi]
> Pengurangan bentuk akar adalah operasi mengurangkan satu bentuk akar dari bentuk akar lain.

Jika akar sejenis, maka koefisiennya dapat dikurangkan.

\[
P\sqrt[n]{A}-Q\sqrt[n]{A}=(P-Q)\sqrt[n]{A}
\]

> [!alasan]
> Pengurangan dapat dipandang sebagai penjumlahan dengan lawan bilangan. Karena bagian akarnya sama, sifat distributif tetap berlaku.

Jika akar tidak sejenis, pengurangan tidak dapat digabungkan langsung.

\[
\sqrt[n]{A}-\sqrt[n]{B}\neq \sqrt[n]{A-B}
\]

secara umum.

> [!alasan]
> Operasi akar tidak menyebar terhadap pengurangan karena pangkat tidak menyebar terhadap pengurangan.

---

## Operasi Perkalian Bentuk Akar

> [!definisi]
> Perkalian bentuk akar adalah operasi mengalikan dua atau lebih bentuk yang memuat akar.

Untuk indeks yang sama dan syarat domain yang sesuai,

\[
\sqrt[n]{A}\cdot \sqrt[n]{B}=\sqrt[n]{AB}
\]

Untuk akar berindeks genap dalam bilangan real, syarat yang umum digunakan adalah

\[
A \ge 0,\quad B \ge 0
\]

Untuk akar berindeks ganjil, syarat tanda radikan tidak diperlukan.

> [!alasan]
> Jika \(\sqrt[n]{A}\) dan \(\sqrt[n]{B}\) masing-masing dipangkatkan \(n\), hasilnya adalah \(A\) dan \(B\). Perkalian keduanya ketika dipangkatkan \(n\) menghasilkan \(AB\), sehingga bentuk tersebut sesuai dengan definisi akar. Pada indeks genap, syarat tidak negatif diperlukan agar akar realnya terdefinisi dan nilai utama tetap konsisten.

---

## Operasi Pembagian Bentuk Akar

> [!definisi]
> Pembagian bentuk akar adalah operasi membagi satu bentuk akar dengan bentuk akar lain.

Untuk indeks yang sama dan syarat domain yang sesuai,

\[
\frac{\sqrt[n]{A}}{\sqrt[n]{B}}=\sqrt[n]{\frac{A}{B}}
\]

dengan

\[
B \neq 0
\]

Untuk akar berindeks genap dalam bilangan real, syarat umum adalah

\[
A \ge 0,\quad B>0
\]

> [!alasan]
> Penyebut tidak boleh nol karena pembagian dengan nol tidak terdefinisi. Untuk akar genap, \(B>0\) menjamin \(\sqrt[n]{B}\) terdefinisi dan tidak bernilai nol.

---

## Perpangkatan Bentuk Akar

> [!definisi]
> Perpangkatan bentuk akar adalah operasi memangkatkan suatu bentuk akar.

Jika bentuk akar dipangkatkan sesuai indeksnya, maka

\[
\left(\sqrt[n]{A}\right)^n=A
\]

untuk semua \(A\) dalam domain akar tersebut.

> [!alasan]
> Akar pangkat \(n\) didefinisikan sebagai kebalikan dari pangkat \(n\), sehingga memangkatkan akar dengan indeks yang sama mengembalikan radikannya.

Untuk urutan sebaliknya,

\[
\sqrt[n]{A^n}
\]

hasilnya bergantung pada paritas \(n\).

Jika \(n\) ganjil,

\[
\sqrt[n]{A^n}=A
\]

Jika \(n\) genap,

\[
\sqrt[n]{A^n}=|A|
\]

> [!alasan]
> Pada indeks genap, akar utama tidak boleh negatif, sedangkan \(A\) dapat bernilai negatif. Karena itu diperlukan nilai mutlak.

---

## Penyederhanaan Bentuk Akar

> [!definisi]
> Penyederhanaan bentuk akar adalah proses menulis bentuk akar ke bentuk setara yang lebih sederhana dengan mengeluarkan faktor pangkat sempurna dari radikan.

Jika radikan dapat ditulis sebagai

\[
A=B^nC
\]

maka

\[
\sqrt[n]{A}=\sqrt[n]{B^nC}
\]

Untuk \(n\) ganjil,

\[
\sqrt[n]{B^nC}=B\sqrt[n]{C}
\]

Untuk \(n\) genap,

\[
\sqrt[n]{B^nC}=|B|\sqrt[n]{C}
\]

dengan syarat akar realnya terdefinisi.

> [!alasan]
> Faktor \(B^n\) dapat dikeluarkan dari akar karena akar pangkat \(n\) dari \(B^n\) adalah \(B\) untuk indeks ganjil dan \(|B|\) untuk indeks genap.

---

## Bentuk Akar Paling Sederhana

> [!definisi]
> Bentuk akar paling sederhana adalah bentuk akar yang memenuhi semua kondisi penyederhanaan sesuai sistem yang digunakan.

Dalam konteks aljabar real, bentuk akar biasanya dianggap paling sederhana jika:
- radikan tidak memuat faktor pangkat sempurna yang dapat dikeluarkan,
- tidak ada akar di penyebut jika konvensi rasionalisasi digunakan,
- indeks akar tidak dapat diturunkan,
- radikan tidak memuat pecahan yang masih dapat dipisahkan,
- akar sejenis sudah digabungkan,
- faktor di luar akar dan di dalam akar sudah ditempatkan sesuai aturan nilai utama.

> [!alasan]
> Kondisi-kondisi tersebut membuat bentuk akar lebih mudah dibandingkan karena bagian yang dapat disederhanakan sudah dipindahkan ke luar akar atau digabungkan.

---

## Faktor dalam Radikan

> [!definisi]
> Faktor adalah bagian dari suatu hasil perkalian.

Jika radikan berupa hasil perkalian,

\[
AB
\]

maka \(A\) dan \(B\) adalah faktor dari radikan tersebut.

Jika salah satu faktor merupakan pangkat sempurna terhadap indeks akar, faktor tersebut dapat dikeluarkan dari akar.

\[
\sqrt[n]{A^nB}
\]

dapat disederhanakan menjadi bentuk yang memuat \(\sqrt[n]{B}\), dengan memperhatikan paritas \(n\).

> [!alasan]
> Operasi akar terhadap perkalian dapat dipisahkan ketika syarat domain terpenuhi, sehingga faktor pangkat sempurna dapat dipindahkan ke luar tanda akar.

---

## Koefisien Bentuk Akar

> [!definisi]
> Koefisien bentuk akar adalah faktor yang berada di luar tanda akar dan mengalikan bentuk akar tersebut.

Pada bentuk

\[
P\sqrt[n]{A}
\]

koefisiennya adalah \(P\).

Koefisien dapat berasal dari:
- faktor yang sejak awal berada di luar akar,
- faktor pangkat sempurna yang dikeluarkan dari radikan,
- hasil operasi penjumlahan atau pengurangan akar sejenis.

> [!alasan]
> Menempatkan faktor pangkat sempurna sebagai koefisien membuat radikan tersisa lebih sederhana.

---

## Akar Sejenis

> [!definisi]
> Akar sejenis adalah bentuk akar yang memiliki indeks akar sama dan radikan sama setelah semua bentuk disederhanakan.

Bentuk umum akar sejenis adalah

\[
P\sqrt[n]{A}
\]

dan

\[
Q\sqrt[n]{A}
\]

Akar sejenis dapat digabungkan melalui penjumlahan atau pengurangan koefisien.

\[
P\sqrt[n]{A}\pm Q\sqrt[n]{A}=(P\pm Q)\sqrt[n]{A}
\]

> [!alasan]
> Karena bagian akar sama, kedua bentuk tersebut berbeda hanya pada faktor pengalinya. Sifat distributif memungkinkan penggabungan faktor pengali.

---

## Akar Tidak Sejenis

> [!definisi]
> Akar tidak sejenis adalah bentuk akar yang indeks atau radikannya berbeda setelah penyederhanaan.

Bentuk akar tidak sejenis tidak dapat digabungkan melalui penjumlahan atau pengurangan langsung.

\[
P\sqrt[n]{A}+Q\sqrt[m]{B}
\]

tidak dapat digabungkan sebagai satu suku akar jika bagian akarnya tidak sama.

> [!alasan]
> Penjumlahan suku aljabar hanya dapat digabungkan bila bagian nonkoefisiennya sama. Jika indeks atau radikan berbeda, faktor akarnya bukan faktor yang sama.

---

## Menyamakan Indeks Akar

> [!definisi]
> Menyamakan indeks akar adalah proses menulis beberapa bentuk akar dengan indeks yang sama menggunakan hubungan antara akar dan eksponen pecahan.

Karena

\[
\sqrt[n]{A}=A^{\frac{1}{n}}
\]

maka akar dengan indeks berbeda dapat dianalisis melalui eksponen pecahan.

Jika indeks akar berbeda, struktur umumnya dapat dibandingkan dengan mencari penyebut eksponen pecahan yang sama.

> [!alasan]
> Eksponen pecahan mengubah operasi akar menjadi operasi eksponen, sehingga aturan penyamaan penyebut pada pecahan dapat digunakan untuk melihat hubungan antarindeks.

---

## Akar Bertingkat

> [!definisi]
> Akar bertingkat adalah bentuk akar yang radikannya masih memuat bentuk akar lain.

Bentuk umumnya dapat ditulis sebagai

\[
\sqrt[m]{\sqrt[n]{A}}
\]

Dengan notasi eksponen pecahan,

\[
\sqrt[m]{\sqrt[n]{A}}
=
\left(A^{\frac{1}{n}}\right)^{\frac{1}{m}}
\]

Jika syarat domain terpenuhi, maka

\[
\left(A^{\frac{1}{n}}\right)^{\frac{1}{m}}
=
A^{\frac{1}{mn}}
\]

sehingga

\[
\sqrt[m]{\sqrt[n]{A}}=\sqrt[mn]{A}
\]

dengan syarat keberlakuan yang sesuai.

> [!alasan]
> Pangkat dari pangkat dikalikan eksponennya. Karena akar dapat ditulis sebagai eksponen pecahan, akar bertingkat dapat digabungkan melalui perkalian indeks.

---

## Akar dari Hasil Kali

> [!definisi]
> Akar dari hasil kali adalah bentuk akar dengan radikan berupa hasil perkalian.

Bentuk umumnya adalah

\[
\sqrt[n]{AB}
\]

Dengan syarat yang sesuai,

\[
\sqrt[n]{AB}=\sqrt[n]{A}\sqrt[n]{B}
\]

Untuk indeks genap dalam bilangan real, pemisahan ini aman ketika

\[
A \ge 0,\quad B \ge 0
\]

Untuk indeks ganjil, pemisahan dapat dilakukan untuk semua radikan real.

> [!alasan]
> Pada indeks genap, akar utama harus tidak negatif. Jika tanda radikan tidak dikontrol, pemisahan dapat mengubah domain atau nilai. Pada indeks ganjil, akar mempertahankan tanda sehingga pemisahan lebih luas berlaku.

---

## Akar dari Hasil Bagi

> [!definisi]
> Akar dari hasil bagi adalah bentuk akar dengan radikan berupa pecahan atau pembagian.

Bentuk umumnya adalah

\[
\sqrt[n]{\frac{A}{B}}
\]

dengan

\[
B\neq 0
\]

Dengan syarat yang sesuai,

\[
\sqrt[n]{\frac{A}{B}}=
\frac{\sqrt[n]{A}}{\sqrt[n]{B}}
\]

Untuk indeks genap dalam bilangan real, syarat umum adalah

\[
A\ge 0,\quad B>0
\]

> [!alasan]
> Penyebut harus tidak nol agar pecahan terdefinisi. Untuk akar genap, penyebut positif memastikan akar penyebut terdefinisi dan tidak nol.

---

## Akar dari Pangkat

> [!definisi]
> Akar dari pangkat adalah bentuk akar yang radikannya berupa ekspresi berpangkat.

Bentuk umumnya adalah

\[
\sqrt[n]{A^m}
\]

Dengan notasi eksponen pecahan,

\[
\sqrt[n]{A^m}=A^{\frac{m}{n}}
\]

dengan syarat domain yang sesuai.

Jika \(m\) dapat ditulis sebagai kelipatan indeks \(n\), yaitu

\[
m=nq+r
\]

dengan \(q\) dan \(r\) bilangan bulat serta \(r\) sisa pembagian, maka bagian \(A^{nq}\) dapat berhubungan dengan faktor di luar akar.

Secara struktural,

\[
\sqrt[n]{A^{nq+r}}
=
\sqrt[n]{(A^q)^nA^r}
\]

Untuk indeks ganjil,

\[
\sqrt[n]{(A^q)^nA^r}=A^q\sqrt[n]{A^r}
\]

Untuk indeks genap,

\[
\sqrt[n]{(A^q)^nA^r}=|A^q|\sqrt[n]{A^r}
\]

> [!alasan]
> Pemisahan ini mengikuti pembagian eksponen menjadi bagian yang habis dibagi indeks dan bagian sisa. Bagian yang habis dibagi indeks dapat keluar dari akar.

---

## Hubungan Akar dan Faktorisasi

> [!definisi]
> Faktorisasi adalah proses menulis suatu ekspresi sebagai hasil perkalian beberapa faktor.

Dalam bentuk akar, faktorisasi digunakan untuk menemukan bagian radikan yang merupakan pangkat sempurna terhadap indeks akar.

Jika

\[
A=BC
\]

dan \(B\) merupakan pangkat sempurna terhadap indeks \(n\), maka \(B\) dapat dikeluarkan dari akar.

> [!alasan]
> Akar berinteraksi langsung dengan perkalian. Karena itu, faktor yang berbentuk pangkat sempurna dapat dipisahkan dari faktor lain.

---

## Radikan yang Berupa Jumlah

> [!definisi]
> Radikan berupa jumlah adalah bentuk akar yang radikannya adalah hasil penjumlahan dua atau lebih ekspresi.

Bentuk umumnya adalah

\[
\sqrt[n]{A+B}
\]

Secara umum,

\[
\sqrt[n]{A+B}\neq \sqrt[n]{A}+\sqrt[n]{B}
\]

> [!alasan]
> Operasi akar tidak bersifat distributif terhadap penjumlahan. Jika akar dari jumlah disamakan dengan jumlah akar, maka setelah dipangkatkan kembali akan muncul suku campuran yang tidak terdapat pada radikan awal.

---

## Radikan yang Berupa Selisih

> [!definisi]
> Radikan berupa selisih adalah bentuk akar yang radikannya adalah hasil pengurangan dua ekspresi.

Bentuk umumnya adalah

\[
\sqrt[n]{A-B}
\]

Secara umum,

\[
\sqrt[n]{A-B}\neq \sqrt[n]{A}-\sqrt[n]{B}
\]

> [!alasan]
> Operasi akar tidak bersifat distributif terhadap pengurangan. Pangkat dari selisih tidak sama dengan selisih pangkat masing-masing bagian.

---

## Radikan yang Berupa Perkalian

> [!definisi]
> Radikan berupa perkalian adalah bentuk akar yang radikannya merupakan hasil kali beberapa faktor.

Bentuk umumnya adalah

\[
\sqrt[n]{ABC}
\]

Jika syarat domain terpenuhi, bentuk ini dapat dipisahkan menjadi

\[
\sqrt[n]{A}\sqrt[n]{B}\sqrt[n]{C}
\]

atau sebaliknya digabungkan menjadi satu akar.

> [!alasan]
> Pangkat \(n\) dari hasil kali sama dengan hasil kali pangkat \(n\) masing-masing faktor, sehingga operasi kebalikannya, yaitu akar, sesuai dengan struktur perkalian.

---

## Radikan yang Berupa Pecahan

> [!definisi]
> Radikan berupa pecahan adalah bentuk akar yang radikannya mengandung pembagian.

Bentuk umumnya adalah

\[
\sqrt[n]{\frac{A}{B}}
\]

dengan

\[
B\neq 0
\]

Jika syarat domain terpenuhi,

\[
\sqrt[n]{\frac{A}{B}}=
\frac{\sqrt[n]{A}}{\sqrt[n]{B}}
\]

> [!alasan]
> Hubungan ini berasal dari sifat pangkat terhadap pembagian: pangkat dari hasil bagi sama dengan hasil bagi pangkat, selama penyebut tidak nol.

---

## Rasionalisasi

> [!definisi]
> Rasionalisasi adalah proses mengubah bentuk pecahan yang memuat akar pada penyebut menjadi bentuk setara yang penyebutnya tidak memuat akar.

> [!definisi]
> Penyebut adalah bagian bawah dari suatu pecahan.

> [!definisi]
> Pembilang adalah bagian atas dari suatu pecahan.

Bentuk umum pecahan dengan akar di penyebut adalah

\[
\frac{P}{\sqrt[n]{A}}
\]

Rasionalisasi dilakukan dengan mengalikan pembilang dan penyebut oleh bentuk yang membuat penyebut menjadi pangkat sempurna terhadap indeks akar.

> [!alasan]
> Mengalikan pembilang dan penyebut dengan bentuk yang sama dan tidak nol tidak mengubah nilai pecahan, karena operasi tersebut sama dengan mengalikan pecahan dengan satu.

---

## Rasionalisasi Penyebut Akar Kuadrat Tunggal

Untuk penyebut berbentuk akar kuadrat tunggal,

\[
\frac{P}{\sqrt{A}}
\]

bentuk rasionalisasi menggunakan faktor

\[
\sqrt{A}
\]

sehingga penyebut menjadi

\[
\sqrt{A}\cdot \sqrt{A}=A
\]

dengan syarat

\[
A>0
\]

> [!alasan]
> Akar kuadrat dikalikan dirinya sendiri menghasilkan radikan, sehingga penyebut tidak lagi memuat tanda akar. Syarat \(A>0\) memastikan penyebut awal dan faktor pengali tidak nol.

---

## Rasionalisasi Penyebut Akar Pangkat \(n\)

Untuk penyebut

\[
\sqrt[n]{A^k}
\]

rasionalisasi bertujuan membentuk pangkat penuh \(n\) pada radikan penyebut.

Jika penyebut mengandung

\[
\sqrt[n]{A^k}
\]

maka faktor yang dibutuhkan secara struktural adalah

\[
\sqrt[n]{A^{n-k}}
\]

agar

\[
\sqrt[n]{A^k}\cdot \sqrt[n]{A^{n-k}}
=
\sqrt[n]{A^n}
\]

yang dapat disederhanakan sesuai paritas indeks.

> [!alasan]
> Pangkat pada radikan penyebut harus melengkapi kelipatan indeks akar supaya akar dapat dihilangkan dari penyebut.

---

## Konjugat

> [!definisi]
> Konjugat adalah pasangan bentuk binomial yang memiliki dua suku sama tetapi tanda operasi di antara sukunya berlawanan.

Untuk bentuk

\[
A+\sqrt{B}
\]

konjugatnya adalah

\[
A-\sqrt{B}
\]

Untuk bentuk

\[
A-\sqrt{B}
\]

konjugatnya adalah

\[
A+\sqrt{B}
\]

Konjugat digunakan dalam rasionalisasi penyebut yang berbentuk penjumlahan atau pengurangan yang memuat akar.

> [!alasan]
> Perkalian bentuk berkonjugat menghasilkan selisih kuadrat, yaitu struktur yang dapat menghilangkan akar kuadrat dari penyebut.

---

## Selisih Kuadrat

> [!definisi]
> Selisih kuadrat adalah bentuk aljabar yang merupakan selisih dari dua kuadrat.

Identitasnya adalah

\[
(A+B)(A-B)=A^2-B^2
\]

Dalam rasionalisasi,

\[
(A+\sqrt{B})(A-\sqrt{B})=A^2-B
\]

dengan syarat bentuk-bentuk tersebut terdefinisi.

> [!alasan]
> Suku silang saling meniadakan karena memiliki besar yang sama dan tanda berlawanan, sehingga akar yang semula muncul pada suku silang hilang.

---

## Penyebut Binomial Berakar

> [!definisi]
> Penyebut binomial berakar adalah penyebut pecahan yang terdiri atas dua suku dan setidaknya salah satu sukunya memuat akar.

Bentuk umumnya dapat berupa

\[
A+\sqrt{B}
\]

atau

\[
A-\sqrt{B}
\]

Rasionalisasi dilakukan dengan mengalikan pembilang dan penyebut oleh konjugat penyebut.

\[
\frac{P}{A+\sqrt{B}}
\cdot
\frac{A-\sqrt{B}}{A-\sqrt{B}}
\]

atau

\[
\frac{P}{A-\sqrt{B}}
\cdot
\frac{A+\sqrt{B}}{A+\sqrt{B}}
\]

> [!alasan]
> Konjugat mengubah penyebut menjadi selisih kuadrat, sehingga akar kuadrat pada penyebut dapat hilang.

---

## Bentuk Akar dalam Pecahan Aljabar

> [!definisi]
> Pecahan aljabar adalah pecahan yang pembilang atau penyebutnya memuat ekspresi aljabar.

Dalam pecahan aljabar yang memuat akar, syarat utama adalah:
- penyebut tidak boleh nol,
- setiap akar genap harus memiliki radikan tidak negatif,
- setiap operasi yang muncul harus terdefinisi.

> [!alasan]
> Pecahan dan akar memiliki syarat keberlakuan sendiri. Semua syarat tersebut harus dipenuhi bersamaan agar ekspresi bermakna dalam bilangan real.

---

## Penyederhanaan Akar dalam Pecahan

Jika radikan berbentuk pecahan,

\[
\sqrt[n]{\frac{A}{B}}
\]

maka bentuk ini dapat ditulis sebagai

\[
\frac{\sqrt[n]{A}}{\sqrt[n]{B}}
\]

dengan syarat sesuai.

Sebaliknya,

\[
\frac{\sqrt[n]{A}}{\sqrt[n]{B}}
\]

dapat digabungkan menjadi

\[
\sqrt[n]{\frac{A}{B}}
\]

dengan syarat penyebut tidak nol dan akar terdefinisi.

> [!alasan]
> Kedua arah perubahan mengikuti sifat akar terhadap pembagian. Namun syarat domain harus dijaga agar bentuk baru tidak memperluas atau mempersempit makna secara tidak sah.

---

## Denesting Akar

> [!definisi]
> Denesting akar adalah proses mengubah akar bertingkat atau akar dari bentuk majemuk menjadi bentuk yang lebih sederhana tanpa akar bertingkat.

Bentuk yang dapat didenesting biasanya memiliki struktur radikan yang dapat dihubungkan dengan kuadrat dari penjumlahan atau pengurangan bentuk akar.

Secara struktural,

\[
(A+B)^2=A^2+2AB+B^2
\]

dan

\[
(A-B)^2=A^2-2AB+B^2
\]

Jika suatu radikan cocok dengan struktur kuadrat tersebut, akar kuadratnya dapat ditulis sebagai bentuk penjumlahan atau pengurangan.

> [!alasan]
> Akar kuadrat membalik operasi kuadrat. Jika radikan dapat dikenali sebagai kuadrat suatu bentuk, akar kuadratnya dapat dikembalikan ke bentuk tersebut, dengan memperhatikan nilai utama.

---

## Akar dan Identitas Aljabar

> [!definisi]
> Identitas aljabar adalah persamaan yang benar untuk semua nilai yang memenuhi syarat ekspresinya.

Identitas yang sering berkaitan dengan bentuk akar meliputi:

\[
(A+B)^2=A^2+2AB+B^2
\]

\[
(A-B)^2=A^2-2AB+B^2
\]

\[
(A+B)(A-B)=A^2-B^2
\]

\[
(A+B)^3=A^3+3A^2B+3AB^2+B^3
\]

\[
(A-B)^3=A^3-3A^2B+3AB^2-B^3
\]

> [!alasan]
> Identitas aljabar membantu mengenali radikan yang merupakan pangkat sempurna atau bentuk yang dapat dirasionalisasi.

---

## Bentuk Akar dan Persamaan

> [!definisi]
> Persamaan adalah pernyataan matematika yang menyatakan kesamaan dua ekspresi.

> [!definisi]
> Persamaan berakar adalah persamaan yang memuat variabel di dalam radikan.

Dalam persamaan berakar, syarat domain harus ditentukan sebelum manipulasi aljabar.

Jika ada bentuk

\[
\sqrt[n]{A}
\]

dengan \(n\) genap, maka syaratnya adalah

\[
A\ge 0
\]

Jika kedua ruas persamaan dipangkatkan, hasil yang diperoleh harus tetap diperiksa terhadap syarat awal.

> [!alasan]
> Pemangkatan dapat menghasilkan persamaan baru yang memiliki solusi tambahan karena operasi pangkat, terutama pangkat genap, tidak selalu satu-ke-satu pada seluruh bilangan real.

---

## Operasi Satu-ke-Satu

> [!definisi]
> Operasi satu-ke-satu adalah operasi yang tidak menghasilkan nilai keluaran sama dari dua masukan berbeda dalam domain yang sedang dibahas.

Pangkat ganjil pada bilangan real bersifat satu-ke-satu.

> [!alasan]
> Jika dua bilangan real berbeda dipangkatkan dengan pangkat ganjil yang sama, urutan nilainya tetap berbeda.

Pangkat genap tidak satu-ke-satu pada seluruh bilangan real.

> [!alasan]
> Dua bilangan real yang berlawanan tanda memiliki hasil pangkat genap yang sama. Karena itu, akar genap memerlukan pilihan nilai utama agar menjadi fungsi.

---

## Solusi Tambahan dalam Persamaan Berakar

> [!definisi]
> Solusi tambahan adalah nilai yang muncul dari proses manipulasi aljabar tetapi tidak memenuhi persamaan awal.

Solusi tambahan dapat muncul ketika persamaan berakar dipangkatkan.

> [!alasan]
> Pemangkatan dapat menghilangkan informasi tanda. Akibatnya, nilai yang memenuhi persamaan hasil pemangkatan belum tentu memenuhi persamaan sebelum dipangkatkan.

---

## Bentuk Akar dan Pertidaksamaan

> [!definisi]
> Pertidaksamaan adalah pernyataan matematika yang membandingkan dua ekspresi menggunakan relasi urutan seperti \(<\), \(\le\), \(>\), atau \(\ge\).

> [!definisi]
> Pertidaksamaan berakar adalah pertidaksamaan yang memuat bentuk akar.

Dalam pertidaksamaan berakar, domain akar harus ditentukan terlebih dahulu.

Untuk akar genap,

\[
\sqrt[n]{A}
\]

memerlukan

\[
A\ge 0
\]

Jika kedua ruas pertidaksamaan dipangkatkan dengan pangkat genap, tanda pertidaksamaan tidak cukup ditentukan tanpa mengetahui tanda ruas-ruasnya.

> [!alasan]
> Pangkat genap tidak mempertahankan urutan pada seluruh bilangan real. Namun pada bilangan tidak negatif, pangkat genap bersifat meningkat, sehingga pemangkatan lebih aman bila kedua ruas tidak negatif.

---

## Fungsi Akar

> [!definisi]
> Fungsi adalah aturan yang memasangkan setiap masukan dalam domain dengan tepat satu keluaran.

> [!definisi]
> Fungsi akar adalah fungsi yang memuat operasi akar terhadap masukan atau ekspresi yang bergantung pada masukan.

Bentuk umum fungsi akar adalah

\[
f(X)=\sqrt[n]{A(X)}
\]

dengan \(A(X)\) menyatakan ekspresi yang bergantung pada masukan \(X\).

Jika \(n\) genap, domain fungsi harus memenuhi

\[
A(X)\ge 0
\]

Jika \(n\) ganjil, domain fungsi mengikuti domain \(A(X)\).

> [!alasan]
> Fungsi akar harus menghasilkan nilai real tunggal untuk setiap masukan dalam domainnya. Akar genap membutuhkan radikan tidak negatif agar nilai realnya ada.

---

## Grafik Fungsi Akar

> [!definisi]
> Grafik fungsi adalah himpunan titik yang menyatakan pasangan masukan dan keluaran fungsi.

Fungsi akar dasar berindeks genap memiliki keluaran tidak negatif.

\[
f(X)=\sqrt[n]{X}
\]

dengan \(n\) genap memiliki syarat

\[
X\ge 0
\]

dan keluaran

\[
f(X)\ge 0
\]

Fungsi akar dasar berindeks ganjil terdefinisi untuk seluruh bilangan real.

\[
f(X)=\sqrt[n]{X}
\]

dengan \(n\) ganjil memiliki domain

\[
\mathbb{R}
\]

dan range

\[
\mathbb{R}
\]

> [!alasan]
> Sifat domain dan range grafik fungsi akar mengikuti sifat akar genap dan akar ganjil pada bilangan real.

---

## Transformasi Bentuk Fungsi Akar

> [!definisi]
> Transformasi fungsi adalah perubahan bentuk fungsi yang memengaruhi letak atau bentuk grafiknya.

Bentuk umum transformasi fungsi akar dapat ditulis sebagai

\[
f(X)=P\sqrt[n]{A(X)-H}+K
\]

dengan:
- \(P\) memengaruhi skala vertikal dan pencerminan terhadap sumbu horizontal jika tandanya berubah,
- \(H\) memengaruhi pergeseran horizontal,
- \(K\) memengaruhi pergeseran vertikal,
- \(A(X)-H\) menentukan syarat domain untuk indeks genap.

> [!alasan]
> Perubahan di luar akar memengaruhi keluaran, sedangkan perubahan di dalam akar memengaruhi masukan yang membuat radikan memenuhi syarat.

---

## Akar dan Komposisi Fungsi

> [!definisi]
> Komposisi fungsi adalah pembentukan fungsi baru dengan memasukkan hasil suatu fungsi ke fungsi lain.

Jika bentuk akar ditulis sebagai

\[
\sqrt[n]{A(X)}
\]

maka dapat dipandang sebagai komposisi antara fungsi luar

\[
R(U)=\sqrt[n]{U}
\]

dan fungsi dalam

\[
U=A(X)
\]

Domainnya ditentukan oleh syarat fungsi dalam dan syarat fungsi luar.

> [!alasan]
> Nilai \(A(X)\) harus terlebih dahulu terdefinisi, lalu nilai tersebut harus memenuhi syarat agar akar \(\sqrt[n]{U}\) terdefinisi.

---

## Akar dan Nilai Absolut dalam Fungsi

Dalam fungsi akar, bentuk

\[
\sqrt{A(X)^2}
\]

tidak sama dengan

\[
A(X)
\]

secara umum.

Yang benar adalah

\[
\sqrt{A(X)^2}=|A(X)|
\]

> [!alasan]
> Akar kuadrat utama selalu tidak negatif. Jika \(A(X)\) bernilai negatif untuk sebagian domain, maka hasil akar kuadrat dari kuadratnya tetap tidak negatif, sehingga harus ditulis sebagai nilai mutlak.

---

## Bentuk Akar dalam Bilangan Kompleks

> [!definisi]
> Bilangan kompleks adalah bilangan yang dapat ditulis dalam bentuk penjumlahan bagian real dan bagian imajiner.

> [!definisi]
> Unit imajiner adalah bilangan yang kuadratnya sama dengan negatif satu, biasanya ditulis sebagai \(i\).

Dalam bilangan real, akar genap dari radikan negatif tidak terdefinisi. Dalam bilangan kompleks, bentuk tersebut dapat didefinisikan menggunakan unit imajiner.

> [!alasan]
> Sistem bilangan kompleks memperluas bilangan real dengan menambahkan bilangan yang kuadratnya negatif, sehingga akar kuadrat dari bilangan negatif dapat diberi makna.

Namun, dalam pembahasan bentuk akar real, akar genap dari radikan negatif tetap dianggap tidak terdefinisi.

> [!alasan]
> Setiap sistem bilangan memiliki aturan domain sendiri. Pernyataan dalam bilangan kompleks tidak otomatis berlaku dalam pembahasan bilangan real.

---

## Akar dan Persamaan Polinomial

> [!definisi]
> Polinomial adalah ekspresi aljabar yang tersusun dari penjumlahan suku-suku berpangkat bilangan bulat tak negatif.

Bentuk akar sering muncul sebagai hasil penyelesaian persamaan polinomial tertentu.

Jika suatu persamaan dapat diubah menjadi bentuk

\[
U^n=A
\]

maka nilai \(U\) berkaitan dengan

\[
\sqrt[n]{A}
\]

dengan memperhatikan jumlah kemungkinan nilai dan pilihan nilai utama.

> [!alasan]
> Akar adalah operasi kebalikan dari perpangkatan. Oleh karena itu, persamaan yang memuat pangkat dapat menghasilkan penyelesaian dalam bentuk akar.

---

## Akar dan Persamaan Kuadrat

> [!definisi]
> Persamaan kuadrat adalah persamaan polinomial berderajat dua.

Penyelesaian persamaan kuadrat sering memuat akar kuadrat karena proses penyelesaiannya melibatkan pembalikan operasi kuadrat.

Bentuk akar yang muncul pada persamaan kuadrat biasanya berasal dari diskriminan.

> [!definisi]
> Diskriminan adalah ekspresi yang menentukan sifat akar-akar suatu persamaan kuadrat.

Jika diskriminan berada di bawah akar kuadrat, maka syarat realnya adalah diskriminan tidak negatif.

> [!alasan]
> Akar kuadrat real hanya terdefinisi untuk radikan tidak negatif, sehingga diskriminan menentukan apakah penyelesaian real dapat diperoleh.

---

## Bentuk Akar dan Ketaksamaan Nilai

Untuk radikan tidak negatif, akar berindeks genap utama mempertahankan urutan.

Jika

\[
A\le B
\]

dan

\[
0\le A,\quad 0\le B
\]

maka

\[
\sqrt[n]{A}\le \sqrt[n]{B}
\]

untuk \(n\) genap.

Untuk \(n\) ganjil, fungsi akar juga mempertahankan urutan pada seluruh bilangan real.

> [!alasan]
> Fungsi akar utama merupakan fungsi meningkat pada domain realnya. Jika radikan lebih besar, nilai akar yang sesuai juga tidak lebih kecil.

---

## Monotonitas Fungsi Akar

> [!definisi]
> Monoton meningkat adalah sifat fungsi yang mempertahankan urutan masukan: masukan yang lebih besar menghasilkan keluaran yang lebih besar atau sama.

Fungsi

\[
R(X)=\sqrt[n]{X}
\]

bersifat meningkat pada domain realnya.

Untuk indeks genap, domainnya adalah

\[
X\ge 0
\]

Untuk indeks ganjil, domainnya adalah

\[
X\in\mathbb{R}
\]

> [!alasan]
> Akar adalah kebalikan dari perpangkatan pada interval yang sesuai, dan perpangkatan tersebut meningkat pada domain yang dipilih untuk nilai utama.

---

## Bentuk Akar dan Ketertutupan Operasi

> [!definisi]
> Ketertutupan operasi berarti hasil suatu operasi terhadap anggota himpunan tertentu tetap berada dalam himpunan tersebut.

Bilangan rasional tertutup terhadap penjumlahan, pengurangan, perkalian, dan pembagian oleh bilangan bukan nol.

Namun, bilangan rasional tidak tertutup terhadap operasi akar.

> [!alasan]
> Akar dari bilangan rasional tertentu dapat menghasilkan bilangan irasional ketika radikannya bukan pangkat sempurna terhadap indeks akar.

Bilangan real tertutup terhadap akar ganjil, tetapi tidak tertutup terhadap akar genap dari radikan negatif.

> [!alasan]
> Akar ganjil dari bilangan real selalu real, sedangkan akar genap dari bilangan real negatif tidak real.

---

## Bentuk Akar dan Penyebut Nol

Penyebut nol membuat pecahan tidak terdefinisi.

Jika bentuk akar berada pada penyebut,

\[
\frac{P}{\sqrt[n]{A}}
\]

maka harus dipenuhi

\[
\sqrt[n]{A}\neq 0
\]

Untuk akar apa pun yang terdefinisi,

\[
\sqrt[n]{A}=0 \iff A=0
\]

sehingga syarat penyebut tidak nol menjadi

\[
A\neq 0
\]

dengan syarat domain akar tetap dipenuhi.

> [!alasan]
> Akar dari nol adalah nol karena nol dipangkatkan indeks apa pun yang valid tetap menghasilkan nol. Jika penyebut bernilai nol, pembagian tidak bermakna.

---

## Bentuk Akar dan Tanda Ekspresi

Tanda bentuk akar bergantung pada:
- indeks akar,
- tanda radikan,
- koefisien di luar akar.

Untuk akar genap utama,

\[
\sqrt[n]{A}\ge 0
\]

Untuk akar ganjil,

\[
\sqrt[n]{A}
\]

memiliki tanda yang sama dengan \(A\).

Jika ada koefisien \(P\), tanda bentuk

\[
P\sqrt[n]{A}
\]

ditentukan oleh tanda \(P\) dan tanda akar.

> [!alasan]
> Koefisien mengalikan nilai akar. Dalam perkalian, tanda hasil ditentukan oleh tanda faktor-faktornya.

---

## Bentuk Akar dan Persamaan Identik

> [!definisi]
> Persamaan identik adalah persamaan yang benar untuk semua nilai dalam domainnya.

Pernyataan

\[
\left(\sqrt[n]{A}\right)^n=A
\]

adalah identitas pada domain akar tersebut.

Pernyataan

\[
\sqrt[n]{A^n}=A
\]

adalah identitas untuk indeks ganjil, tetapi untuk indeks genap perlu diganti menjadi

\[
\sqrt[n]{A^n}=|A|
\]

> [!alasan]
> Urutan operasi memengaruhi hasil. Akar lalu pangkat mengembalikan radikan, sedangkan pangkat lalu akar harus mengikuti nilai utama akar.

---

## Reduksi Indeks Akar

> [!definisi]
> Reduksi indeks akar adalah proses menurunkan indeks akar dengan memanfaatkan faktor persekutuan pada indeks dan pangkat radikan.

Jika bentuk akar ditulis sebagai eksponen pecahan,

\[
\sqrt[n]{A^m}=A^{\frac{m}{n}}
\]

maka pecahan \(\frac{m}{n}\) dapat disederhanakan jika pembilang dan penyebut memiliki faktor persekutuan.

Namun, pada bilangan real, reduksi indeks harus memperhatikan tanda dan domain.

> [!alasan]
> Penyederhanaan eksponen pecahan dapat mengubah syarat domain jika tidak memperhatikan paritas indeks. Indeks genap dan ganjil memiliki aturan domain yang berbeda.

---

## Akar dengan Radikan Berpangkat Genap

Jika radikan berbentuk pangkat genap,

\[
A^{2k}
\]

maka akar kuadratnya berkaitan dengan nilai mutlak.

\[
\sqrt{A^{2k}}=|A^k|
\]

> [!alasan]
> Ekspresi \(A^{2k}\) dapat ditulis sebagai \((A^k)^2\). Akar kuadrat dari kuadrat suatu ekspresi adalah nilai mutlak ekspresi tersebut.

---

## Akar dengan Radikan Berpangkat Ganjil

Jika indeks akar ganjil dan radikan berbentuk pangkat yang sesuai, maka nilai mutlak tidak diperlukan.

\[
\sqrt[2k+1]{A^{2k+1}}=A
\]

> [!alasan]
> Pangkat ganjil mempertahankan tanda, sehingga akar ganjil dapat mengembalikan basis tanpa harus mengambil nilai mutlak.

---

## Bentuk Akar Campuran

> [!definisi]
> Bentuk akar campuran adalah bentuk akar yang terdiri atas koefisien di luar akar dan radikan yang tidak sepenuhnya keluar dari akar.

Bentuk umumnya adalah

\[
P\sqrt[n]{A}
\]

dengan \(P\) sebagai koefisien dan \(\sqrt[n]{A}\) sebagai bagian radikal.

Bentuk akar campuran biasanya muncul setelah sebagian faktor radikan dikeluarkan dari akar.

> [!alasan]
> Jika radikan memiliki faktor pangkat sempurna dan faktor bukan pangkat sempurna, hanya faktor pangkat sempurna yang dapat keluar dari akar, sedangkan faktor lainnya tetap berada dalam radikan.

---

## Bentuk Akar Murni

> [!definisi]
> Bentuk akar murni adalah bentuk akar yang tidak memiliki koefisien eksplisit selain satu di luar tanda akar.

Bentuk umumnya adalah

\[
\sqrt[n]{A}
\]

Bentuk akar murni dapat berubah menjadi bentuk akar campuran setelah penyederhanaan jika radikannya memiliki faktor pangkat sempurna.

> [!alasan]
> Penyederhanaan mengeluarkan faktor pangkat sempurna dari radikan, sehingga faktor tersebut menjadi koefisien di luar akar.

---

## Bentuk Akar Majemuk

> [!definisi]
> Bentuk akar majemuk adalah bentuk yang memuat lebih dari satu suku akar atau memuat operasi gabungan antara akar dan ekspresi lain.

Bentuk majemuk dapat memuat:
- jumlah akar,
- selisih akar,
- hasil kali akar,
- hasil bagi akar,
- akar bertingkat,
- akar dalam pecahan,
- akar dalam persamaan,
- akar dalam fungsi.

> [!alasan]
> Suatu bentuk disebut majemuk karena struktur aljabarnya tidak hanya terdiri atas satu operasi akar sederhana.

---

## Ketunggalan Nilai Akar Utama

Akar utama memberikan satu nilai untuk setiap radikan yang memenuhi domain.

Untuk akar genap,

\[
\sqrt[n]{A}
\]

tidak menyatakan dua nilai, melainkan satu nilai utama yang tidak negatif.

> [!alasan]
> Fungsi harus memasangkan setiap masukan dengan tepat satu keluaran. Jika akar genap dianggap menghasilkan dua nilai sekaligus, maka notasi akar tidak menjadi fungsi.

Penyelesaian persamaan

\[
U^n=A
\]

dengan \(n\) genap dapat memiliki lebih dari satu nilai \(U\), tetapi notasi

\[
\sqrt[n]{A}
\]

tetap menyatakan nilai utama.

> [!alasan]
> Persamaan mencari semua nilai yang memenuhi relasi, sedangkan simbol akar utama adalah operasi bernilai tunggal.

---

## Bentuk Akar dan Tanda Plus-Minus

> [!definisi]
> Simbol \(\pm\) menyatakan dua kemungkinan tanda, yaitu positif dan negatif.

Simbol \(\pm\sqrt{A}\) berbeda makna dari \(\sqrt{A}\).

\[
\sqrt{A}
\]

menyatakan akar utama tidak negatif.

\[
\pm\sqrt{A}
\]

menyatakan dua nilai yang berlawanan tanda jika \(A>0\), dan satu nilai jika \(A=0\).

> [!alasan]
> Akar utama adalah satu nilai, sedangkan simbol \(\pm\) ditambahkan ketika suatu persamaan pangkat genap memiliki dua kemungkinan nilai.

---

## Bentuk Akar dan Keterdefinisian

> [!definisi]
> Suatu ekspresi disebut terdefinisi jika semua operasi di dalamnya memiliki makna dalam sistem bilangan yang digunakan.

Bentuk akar real terdefinisi jika:
- setiap akar genap memiliki radikan tidak negatif,
- setiap penyebut tidak nol,
- setiap operasi di dalam radikan terdefinisi,
- setiap ekspresi pangkat dan akar mengikuti syarat domainnya.

> [!alasan]
> Satu bagian ekspresi yang tidak terdefinisi membuat seluruh ekspresi tidak terdefinisi karena nilai keseluruhan tidak dapat ditentukan secara konsisten.

---

## Bentuk Akar dan Penyederhanaan Domain

Saat bentuk akar disederhanakan, domain awal harus dipertahankan.

Jika bentuk awal memiliki syarat tertentu, bentuk hasil penyederhanaan tidak boleh digunakan di luar syarat tersebut.

> [!alasan]
> Transformasi aljabar yang sah hanya menjamin kesetaraan pada domain tempat kedua bentuk terdefinisi. Mengabaikan domain dapat menghasilkan pernyataan yang berlaku pada daerah yang tidak termasuk bentuk awal.

---

## Akar dan Invers Pangkat

> [!definisi]
> Invers operasi adalah operasi yang membalik efek operasi lain pada domain tertentu.

Akar pangkat \(n\) adalah invers dari pangkat \(n\) pada domain yang sesuai.

Untuk indeks ganjil, pangkat \(n\) memiliki invers pada seluruh bilangan real.

Untuk indeks genap, pangkat \(n\) memiliki invers sebagai fungsi hanya jika domain basis dibatasi pada bilangan tidak negatif atau tidak positif.

Dalam notasi akar utama, pembatasan yang digunakan adalah keluaran tidak negatif.

> [!alasan]
> Pangkat genap tidak satu-ke-satu pada seluruh bilangan real. Agar memiliki invers fungsi, domain atau hasilnya harus dibatasi sehingga setiap nilai keluaran berasal dari satu masukan utama.

---

## Struktur Aljabar Bentuk Akar

Bentuk akar dapat dipandang sebagai bagian dari struktur aljabar yang melibatkan:
- operasi penjumlahan,
- operasi pengurangan,
- operasi perkalian,
- operasi pembagian,
- operasi perpangkatan,
- operasi akar,
- syarat domain.

Setiap perubahan bentuk harus menghormati struktur tersebut.

> [!alasan]
> Akar tidak mengikuti semua sifat operasi dasar. Akar berperilaku baik terhadap perkalian dan pembagian dalam syarat tertentu, tetapi tidak terhadap penjumlahan dan pengurangan secara umum.

---

## Relasi antara Akar dan Logika Implikasi

Ketika menulis

\[
\sqrt[n]{A}=B
\]

maka pernyataan ini mengandung dua informasi:

\[
B^n=A
\]

dan \(B\) adalah nilai utama sesuai indeks akar.

Untuk indeks genap, informasi nilai utama berarti

\[
B\ge 0
\]

Untuk indeks ganjil, tanda \(B\) mengikuti tanda \(A\).

> [!alasan]
> Tanpa syarat nilai utama, persamaan \(B^n=A\) pada indeks genap dapat memiliki lebih dari satu nilai \(B\). Notasi akar memilih salah satunya.

---

## Akar dalam Bentuk Eksponen Negatif

> [!definisi]
> Eksponen negatif menyatakan kebalikan dari bentuk berpangkat positif.

Untuk ekspresi yang tidak nol,

\[
A^{-r}=\frac{1}{A^r}
\]

Jika akar dinyatakan sebagai eksponen pecahan negatif,

\[
A^{-\frac{m}{n}}
\]

maka

\[
A^{-\frac{m}{n}}=\frac{1}{A^{\frac{m}{n}}}
\]

dengan

\[
A^{\frac{m}{n}}=\sqrt[n]{A^m}
\]

sesuai syarat domain.

> [!alasan]
> Eksponen negatif menunjukkan kebalikan, sehingga bentuk akar dengan eksponen pecahan negatif memuat pembagian dan harus memenuhi syarat penyebut tidak nol.

---

## Akar dan Eksponen Nol

> [!definisi]
> Eksponen nol adalah eksponen yang menghasilkan satu untuk basis tidak nol.

Untuk \(A\neq 0\),

\[
A^0=1
\]

Dalam konteks akar dan eksponen pecahan, basis nol harus diperiksa ketika eksponen negatif atau pembagian muncul.

> [!alasan]
> Nol tidak boleh menjadi penyebut. Karena eksponen negatif membentuk kebalikan, basis nol tidak diperbolehkan pada bentuk berpangkat negatif.

---

## Akar dan Bilangan Nol

Akar dari nol adalah nol untuk setiap indeks valid.

\[
\sqrt[n]{0}=0
\]

dengan

\[
n\in\mathbb{N},\quad n>1
\]

> [!alasan]
> Nol dipangkatkan dengan indeks valid apa pun tetap menghasilkan nol, sehingga akar pangkat \(n\) dari nol adalah nol.

---

## Akar dan Bilangan Satu

Akar dari satu adalah satu untuk setiap indeks valid.

\[
\sqrt[n]{1}=1
\]

dengan

\[
n\in\mathbb{N},\quad n>1
\]

> [!alasan]
> Satu dipangkatkan dengan indeks valid apa pun tetap menghasilkan satu, dan akar utama memilih nilai yang sesuai.

---

## Akar dan Tanda Negatif

Untuk indeks genap,

\[
\sqrt[n]{-A}
\]

dalam bilangan real terdefinisi hanya jika

\[
-A\ge 0
\]

Untuk indeks ganjil,

\[
\sqrt[n]{-A}=-\sqrt[n]{A}
\]

dengan syarat ekspresi yang terlibat terdefinisi.

> [!alasan]
> Pangkat ganjil mempertahankan tanda, sehingga akar ganjil dapat mengeluarkan tanda negatif dari radikan. Pangkat genap tidak dapat menghasilkan radikan negatif dalam bilangan real.

---

## Akar dan Operasi Kebalikan

Operasi akar dan pangkat saling membalik dalam dua bentuk berbeda:

\[
\left(\sqrt[n]{A}\right)^n=A
\]

dan

\[
\sqrt[n]{A^n}
\]

Bentuk pertama selalu mengembalikan radikan pada domain akar.

Bentuk kedua mengembalikan basis hanya untuk indeks ganjil, sedangkan untuk indeks genap menghasilkan nilai mutlak.

> [!alasan]
> Pada bentuk pertama, akar utama dipilih terlebih dahulu lalu dipangkatkan kembali. Pada bentuk kedua, basis dipangkatkan terlebih dahulu sehingga informasi tanda dapat hilang jika indeksnya genap.

---

## Penyederhanaan Bentuk Akar dengan Banyak Faktor

Jika radikan terdiri atas beberapa faktor,

\[
A_1A_2A_3\cdots A_k
\]

maka setiap faktor diperiksa apakah merupakan pangkat sempurna terhadap indeks akar.

Jika beberapa faktor dapat digabung menjadi pangkat sempurna, gabungan faktor tersebut dapat dikeluarkan dari akar.

> [!alasan]
> Yang penting bukan apakah setiap faktor sendiri-sendiri merupakan pangkat sempurna, melainkan apakah hasil kali sebagian faktor dapat membentuk pangkat sempurna terhadap indeks akar.

---

## Bentuk Akar dan Representasi Setara

Satu nilai dapat memiliki banyak representasi bentuk akar.

Representasi dapat berbeda karena:
- faktor dapat berada di dalam atau di luar akar,
- indeks dapat diubah melalui eksponen pecahan,
- penyebut dapat dirasionalisasi,
- akar sejenis dapat digabungkan atau dipisahkan,
- bentuk berpangkat dapat ditulis sebagai akar.

> [!alasan]
> Representasi aljabar tidak selalu unik. Kesetaraan ditentukan oleh nilai dan domain, bukan oleh tampilan simbol semata.

---

## Bentuk Akar dalam Ekspresi Bertingkat Operasi

Dalam ekspresi yang memuat akar, pangkat, pecahan, dan operasi dasar, keterdefinisian harus diperiksa dari bagian terdalam ke bagian terluar.

Jika suatu radikan memuat pecahan, penyebut dalam radikan harus tidak nol.

Jika akar luar berindeks genap, seluruh radikan luar harus tidak negatif.

> [!alasan]
> Ekspresi matematika dibangun secara bertingkat. Bagian dalam harus memiliki nilai terlebih dahulu sebelum bagian luar dapat dievaluasi.

---

## Keterkaitan Akar dengan Orde Operasi

Akar memiliki prioritas seperti pangkat dalam struktur operasi, tetapi radikan ditentukan oleh panjang garis akar atau tanda pengelompokan.

Ekspresi di bawah tanda akar diperlakukan sebagai satu kesatuan.

> [!alasan]
> Tanpa pengelompokan yang jelas, makna ekspresi dapat berubah. Garis akar berfungsi sebagai penanda batas radikan.

---

## Bentuk Akar dan Parameter

> [!definisi]
> Parameter adalah simbol yang dianggap tetap selama suatu analisis, tetapi nilainya dapat memengaruhi bentuk atau domain ekspresi.

Jika radikan memuat parameter, syarat domain dapat bergantung pada parameter tersebut.

Untuk akar genap,

\[
\sqrt[n]{A}
\]

mensyaratkan

\[
A\ge 0
\]

Jika \(A\) memuat parameter, maka parameter harus membuat syarat tersebut terpenuhi.

> [!alasan]
> Domain akar genap ditentukan oleh tanda radikan. Jika tanda radikan bergantung pada parameter, maka keterdefinisian akar juga bergantung pada parameter.

---

## Bentuk Akar dan Substitusi

> [!definisi]
> Substitusi adalah proses mengganti suatu ekspresi dengan simbol lain atau mengganti simbol dengan ekspresi lain.

Dalam bentuk akar, substitusi dapat digunakan untuk menyederhanakan struktur ekspresi.

Jika

\[
U=A
\]

maka

\[
\sqrt[n]{A}
\]

dapat ditulis sebagai

\[
\sqrt[n]{U}
\]

selama hubungan \(U=A\) dan syarat domain tetap dipertahankan.

> [!alasan]
> Substitusi tidak mengubah nilai jika ekspresi pengganti setara dengan ekspresi awal pada domain yang sama.

---

## Bentuk Akar dan Homogenitas Operasi Perkalian

Bentuk akar memiliki sifat homogen terhadap perkalian dalam syarat tertentu.

\[
\sqrt[n]{AB}=\sqrt[n]{A}\sqrt[n]{B}
\]

> [!alasan]
> Sifat ini muncul karena perpangkatan mendistribusi terhadap perkalian: \((AB)^n=A^nB^n\). Karena akar adalah invers pangkat, struktur perkalian dapat dipertahankan.

Namun bentuk akar tidak homogen terhadap penjumlahan.

\[
\sqrt[n]{A+B}\neq \sqrt[n]{A}+\sqrt[n]{B}
\]

secara umum.

> [!alasan]
> Pangkat tidak mendistribusi terhadap penjumlahan, sehingga inversnya juga tidak dapat diperlakukan sebagai operasi yang mendistribusi terhadap penjumlahan.

---

## Bentuk Akar dan Simetri Tanda

Untuk indeks genap,

\[
A^n=(-A)^n
\]

sehingga akar utama tidak dapat membedakan tanda asal sebelum dipangkatkan.

Akibatnya,

\[
\sqrt[n]{A^n}=|A|
\]

Untuk indeks ganjil,

\[
(-A)^n=-A^n
\]

sehingga tanda tetap terbaca oleh akar.

Akibatnya,

\[
\sqrt[n]{A^n}=A
\]

> [!alasan]
> Pangkat genap memiliki simetri terhadap perubahan tanda, sedangkan pangkat ganjil tidak memiliki simetri tersebut.

---

## Bentuk Akar dalam Notasi Interval

> [!definisi]
> Notasi interval adalah cara menulis himpunan bilangan real yang memenuhi batas tertentu.

Untuk akar genap dasar,

\[
\sqrt[n]{X}
\]

domainnya adalah

\[
[0,\infty)
\]

dan range-nya juga

\[
[0,\infty)
\]

Untuk akar ganjil dasar,

\[
\sqrt[n]{X}
\]

domain dan range-nya adalah

\[
(-\infty,\infty)
\]

> [!alasan]
> Akar genap hanya menerima radikan tidak negatif dan menghasilkan nilai tidak negatif. Akar ganjil menerima semua bilangan real dan menghasilkan semua bilangan real.

---

## Bentuk Akar dan Keterurutan Pangkat

Jika

\[
0\le A\le B
\]

maka untuk indeks valid \(n\),

\[
\sqrt[n]{A}\le \sqrt[n]{B}
\]

dalam domain akar utama.

> [!alasan]
> Pada domain tidak negatif, pangkat \(n\) dan akar pangkat \(n\) mempertahankan urutan karena keduanya meningkat.

---

## Bentuk Akar dan Pembandingan Nilai

Pembandingan dua bentuk akar dapat dilakukan dengan memperhatikan indeks, domain, dan monotonitas.

Jika dua akar memiliki indeks sama dan radikan berada pada domain yang sesuai, maka pembandingan nilai akar sejalan dengan pembandingan radikan.

\[
\sqrt[n]{A}\le \sqrt[n]{B}
\iff
A\le B
\]

pada domain tempat fungsi akar meningkat.

> [!alasan]
> Fungsi akar meningkat pada domain realnya, sehingga urutan radikan dipertahankan oleh operasi akar.

---

## Bentuk Akar dan Kuadrat Kedua Ruas

Jika kedua ruas tidak negatif, maka

\[
A=B
\iff
A^2=B^2
\]

Namun jika tanda ruas tidak diketahui, pemangkatan kuadrat hanya memberi implikasi satu arah.

\[
A=B \Rightarrow A^2=B^2
\]

tetapi

\[
A^2=B^2 \not\Rightarrow A=B
\]

secara umum.

> [!alasan]
> Kuadrat menghilangkan tanda. Dua nilai yang berlawanan tanda dapat memiliki kuadrat sama.

Dalam bentuk akar, hal ini penting karena akar kuadrat utama selalu tidak negatif.

---

## Bentuk Akar dan Ketaksamaan Setelah Pemangkatan

Untuk ruas tidak negatif,

\[
A\le B
\iff
A^n\le B^n
\]

dengan \(n\) bilangan bulat positif.

> [!alasan]
> Pada bilangan tidak negatif, fungsi pangkat positif meningkat, sehingga urutan dipertahankan.

Jika ruas dapat bernilai negatif dan \(n\) genap, kesetaraan urutan tidak berlaku secara umum.

> [!alasan]
> Pangkat genap mengubah nilai negatif menjadi tidak negatif dan dapat membalik perbandingan berdasarkan besar nilai mutlak.

---

## Bentuk Akar dan Penyederhanaan Simbolik

> [!definisi]
> Penyederhanaan simbolik adalah proses mengubah ekspresi menjadi bentuk setara menggunakan aturan aljabar tanpa menetapkan nilai khusus pada simbol.

Pada bentuk akar, penyederhanaan simbolik harus mempertimbangkan:
- apakah indeks genap atau ganjil,
- apakah radikan memenuhi syarat domain,
- apakah faktor yang dikeluarkan memerlukan nilai mutlak,
- apakah penyebut tetap tidak nol,
- apakah transformasi mempertahankan domain.

> [!alasan]
> Simbol dapat mewakili nilai dengan tanda berbeda. Karena itu, penyederhanaan yang benar untuk semua nilai memerlukan syarat eksplisit.

---

## Bentuk Akar dan Notasi Radikal Bersarang

> [!definisi]
> Radikal bersarang adalah bentuk radikal yang berada di dalam radikal lain.

Bentuknya dapat ditulis sebagai

\[
\sqrt[m]{A+\sqrt[n]{B}}
\]

atau bentuk lain yang memuat akar di dalam radikan.

Radikal bersarang tidak selalu dapat disederhanakan menjadi bentuk tanpa akar bersarang.

> [!alasan]
> Penyederhanaan hanya mungkin jika struktur radikan cocok dengan bentuk pangkat sempurna atau identitas aljabar tertentu. Tanpa struktur tersebut, akar bersarang tetap menjadi bentuk paling tepat.

---

## Bentuk Akar dan Pangkat Rasional

> [!definisi]
> Pangkat rasional adalah pangkat yang eksponennya berupa bilangan rasional.

Bentuk

\[
A^{\frac{m}{n}}
\]

dihubungkan dengan akar melalui

\[
A^{\frac{m}{n}}=\sqrt[n]{A^m}
\]

atau

\[
A^{\frac{m}{n}}=\left(\sqrt[n]{A}\right)^m
\]

dengan syarat bahwa bentuk tersebut terdefinisi dan interpretasinya konsisten.

> [!alasan]
> Bilangan rasional sebagai eksponen dapat dipahami sebagai gabungan operasi pangkat bilangan bulat dan akar.

---

## Bentuk Akar dan Pangkat Irasional

> [!definisi]
> Pangkat irasional adalah pangkat yang eksponennya berupa bilangan irasional.

Pangkat irasional tidak sama dengan bentuk akar biasa, karena bentuk akar berkaitan langsung dengan eksponen rasional berpenyebut indeks akar.

> [!alasan]
> Akar pangkat \(n\) sesuai dengan eksponen \(\frac{1}{n}\), yaitu bilangan rasional. Eksponen irasional memerlukan definisi melalui konsep limit atau eksponensial yang lebih luas.

---

## Bentuk Akar dan Kesamaan Formal

> [!definisi]
> Kesamaan formal adalah kesamaan yang diperoleh dari aturan simbolik dengan syarat tertentu.

Rumus bentuk akar seperti

\[
\sqrt[n]{AB}=\sqrt[n]{A}\sqrt[n]{B}
\]

merupakan kesamaan formal yang memerlukan syarat domain.

> [!alasan]
> Tanpa syarat domain, kedua ruas dapat memiliki makna berbeda atau salah satu ruas tidak terdefinisi dalam bilangan real.

---

## Bentuk Akar dan Validitas Transformasi

> [!definisi]
> Transformasi aljabar valid adalah perubahan bentuk yang mempertahankan nilai pada domain yang sedang dibahas.

Transformasi bentuk akar valid jika:
- kedua bentuk terdefinisi,
- domain tidak berubah tanpa dicatat,
- nilai utama akar tetap dipertahankan,
- operasi pembagian tidak memperkenalkan penyebut nol,
- pemangkatan tidak menghasilkan solusi tambahan tanpa pemeriksaan.

> [!alasan]
> Bentuk akar sensitif terhadap domain dan tanda. Transformasi yang mengabaikan keduanya dapat menghasilkan bentuk yang tidak setara.

---

## Bentuk Akar dan Pembatasan Sistem Bilangan

Pembahasan bentuk akar dapat berbeda antara sistem bilangan:
- dalam \(\mathbb{Q}\), banyak akar tidak tertutup,
- dalam \(\mathbb{R}\), akar genap dari radikan negatif tidak terdefinisi,
- dalam bilangan kompleks, akar radikan negatif dapat didefinisikan.

> [!alasan]
> Operasi yang sama dapat memiliki keterdefinisian berbeda bergantung pada himpunan bilangan yang digunakan.

---

## Bentuk Akar dan Penyederhanaan dengan Asumsi

> [!definisi]
> Asumsi adalah syarat tambahan yang diterima sebagai dasar suatu pembahasan.

Jika diasumsikan

\[
A\ge 0
\]

maka

\[
\sqrt{A^2}=A
\]

Jika tidak ada asumsi tersebut, bentuk yang benar adalah

\[
\sqrt{A^2}=|A|
\]

> [!alasan]
> Asumsi tanda menentukan apakah nilai mutlak dapat dihilangkan. Tanpa asumsi, nilai mutlak diperlukan agar pernyataan benar untuk semua nilai real.

---

## Hierarki Pemahaman Bentuk Akar

Bentuk akar tersusun dari beberapa lapisan konsep:
- bilangan real sebagai sistem nilai,
- perpangkatan sebagai operasi dasar,
- akar sebagai invers pangkat,
- indeks sebagai penentu jenis akar,
- radikan sebagai objek yang diakarkan,
- domain sebagai syarat keterdefinisian,
- nilai utama sebagai pilihan hasil tunggal,
- penyederhanaan sebagai perubahan bentuk setara,
- rasionalisasi sebagai penghilangan akar dari penyebut,
- eksponen pecahan sebagai notasi alternatif,
- fungsi akar sebagai bentuk relasi masukan-keluaran.

> [!alasan]
> Setiap lapisan diperlukan karena bentuk akar tidak hanya persoalan simbol, tetapi juga menyangkut nilai, domain, operasi, dan kesetaraan.

---

## Peta Konsep Internal

- [[Bilangan Real]]
  - [[Bilangan Rasional]]
  - [[Bilangan Irasional]]
- [[Perpangkatan]]
  - [[Eksponen]]
  - [[Pangkat Genap]]
  - [[Pangkat Ganjil]]
- [[Akar]]
  - [[Indeks Akar]]
  - [[Radikan]]
  - [[Radikal]]
  - [[Nilai Utama Akar]]
- [[Bentuk Akar]]
  - [[Akar Sejenis]]
  - [[Penyederhanaan Bentuk Akar]]
  - [[Rasionalisasi]]
  - [[Konjugat]]
  - [[Eksponen Pecahan]]
- [[Fungsi Akar]]
  - [[Domain]]
  - [[Range]]
  - [[Monotonitas]]
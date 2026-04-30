# Tips logika matematika dan himpunan

> Pakai untuk proposisi, implikasi, negasi, kuantor, himpunan, diagram Venn, dan argumen matematika.

## Implikasi

Implikasi:

$$
p\Rightarrow q
$$

setara dengan kontraposisi:

$$
\neg q\Rightarrow \neg p
$$

Jangan tertukar dengan konvers:

$$
q\Rightarrow p
$$

Konvers tidak otomatis benar.

## Bentuk setara

$$
p\Rightarrow q \equiv \neg p\lor q
$$

$$
\neg(p\land q)\equiv \neg p\lor \neg q
$$

$$
\neg(p\lor q)\equiv \neg p\land \neg q
$$

$$
\neg(p\Rightarrow q)\equiv p\land \neg q
$$

## Kuantor

Negasi kuantor:

$$
\neg(\forall x\,P(x))\equiv \exists x\,\neg P(x)
$$

$$
\neg(\exists x\,P(x))\equiv \forall x\,\neg P(x)
$$

Trik: "semua benar" disangkal oleh "ada satu yang salah".

## Tabel kebenaran cepat

- $p\land q$ benar hanya jika keduanya benar.
- $p\lor q$ salah hanya jika keduanya salah.
- $p\Rightarrow q$ salah hanya saat $p$ benar dan $q$ salah.
- $p\Leftrightarrow q$ benar jika nilai kebenaran sama.

## Himpunan

Operasi dasar:

$$
A\cup B
$$

berarti anggota A atau B.

$$
A\cap B
$$

berarti anggota A dan B.

Selisih:

$$
A-B
$$

berarti anggota A yang bukan anggota B.

## Diagram Venn

Untuk dua himpunan:

$$
n(A\cup B)=n(A)+n(B)-n(A\cap B)
$$

Untuk tiga himpunan, isi dari tengah terlebih dahulu agar tidak menghitung ganda.

## Pembuktian cepat

| Target | Cara umum |
|---|---|
| "Jika p maka q" | bukti langsung atau kontraposisi |
| "Tidak mungkin" | kontradiksi |
| "Ada" | berikan contoh |
| "Untuk semua" | ambil elemen umum, bukan contoh khusus |
| kesamaan himpunan | buktikan dua arah inklusi |

## Jebakan umum

- "Jika" tidak sama dengan "jika dan hanya jika".
- Satu contoh tidak membuktikan klaim "untuk semua".
- Satu counterexample cukup untuk membantah klaim universal.
- Pada Venn tiga himpunan, angka pada irisan dua himpunan sering masih termasuk irisan tiga; kurangi bagian tengah dulu.

## Terkait

- [[Tips kombinatorika]]
- [[Tips peluang]]
- [[Tips soal cerita dan strategi ujian]]

## Sumber rujukan

- [OpenStax Precalculus 2e - Key Equations, Chapter 11](https://openstax.org/books/precalculus-2e/pages/11-key-equations)


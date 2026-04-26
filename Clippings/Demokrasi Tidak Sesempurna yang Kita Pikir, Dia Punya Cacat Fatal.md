---
title: "Demokrasi Tidak Sesempurna yang Kita Pikir, Dia Punya Cacat Fatal"
source: "https://medium.com/berbagi-berdampak/demokrasi-tidak-sesempurna-yang-kita-pikir-dia-punya-cacat-fatal-f5eb031611f1"
author:
  - "[[Yopi Makdori]]"
published: 2026-04-05
created: 2026-04-27
description: "MEMBEDAH MITOS DALAM DEMOKRASI Demokrasi Tidak Sesempurna yang Kita Pikir, Dia Punya Cacat Fatal Mengambil Logika ‘Gagal Booting' pada Laptop untuk Pilpres 2019 dan 2024; Konsekuensi Salah …"
tags:
  - "clippings"
---
## [Berbagi & Berdampak](https://medium.com/berbagi-berdampak?source=post_page---publication_nav-8f182c62f384-f5eb031611f1---------------------------------------)

[![Berbagi & Berdampak](https://miro.medium.com/v2/resize:fill:76:76/1*FkaWa3Je1HsBmyJulfe3Dg.jpeg)](https://medium.com/berbagi-berdampak?source=post_page---post_publication_sidebar-8f182c62f384-f5eb031611f1---------------------------------------)

Hidup terlalu singkat untuk dimiliki sendirian. Kami mengajak berbagi untuk memberikan dampak bersama. Tautan mendaftar sebagai penulis: [http://bit.ly/form-berbagi-berdampak](http://bit.ly/form-berbagi-berdampak)

## MEMBEDAH MITOS DALAM DEMOKRASI

## Mengambil Logika ‘Gagal Booting' pada Laptop untuk Pilpres 2019 dan 2024; Konsekuensi Salah Diagnosa?

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*-PKMgg9qCl2DXXsT)

Photo by Arnaud Jaegers on Unsplash

H-2 lebaran hingga malam takbiran saya dipusingkan dengan laptop lama yang berkali-kali gagal *booting* (proses memuat sistem operasi atau OS). Di satu sisi saya senang karena mesin laptop kembali hidup, setelah sebelumnya divonis teknisi (teman yang ahli soal *beginian)* mengalami *chipset* terbakar.

==Sebuah konsekuensi akibat== ==*overheat*== ==karena dipakai belajar desain dan edit video (aplikasi yang membutuhkan tenaga jumbo). Padahal laptop tipe bisnis yang ditenagai prosesor seri hemat daya jelas bukan untuk== ==*gaming*== ==apalagi aktivitas desain.==

Ketika laptop tipe ini dipaksa mengerjakan aktivitas berat, maka konsekuensinya bisa dipastikan laptop bakal terasa panas. Dan ujungnya tiba-tiba mati sendiri akibat *overheat*.

Selepas itu, saya coba menyalakan kembali, tapi mesin sama sekali tidak merespons. Dan terpaksa berakhir di tangan teknisi, sampai dia memvonis laptop saya mengalami *dead chip*.

Saya pasrah dan membiarkan laptop itu berbulan-bulan tak tersentuh. Hingga di momen pulang kampung, saya teringat untuk meng- *upgrade* laptop baru menggunakan RAM dan SSD dari laptop lama. Namun sebelum itu, saya iseng menekan tombol *power* pada laptop lama.

Dan betapa senangnya ketika mendengar mesin laptop itu menyala. Artinya vonis *dead chip* itu keliru sebab mesin kembali memberi sinyal tanda-tanda kehidupan. Jika vonis itu benar, maka mesin sama sekali tidak akan merespons seruan untuk bangun.

Kalau laptop tidak mengalami gangguan, lantas kenapa ia berulang kali gagal memuat OS dan tertahan di Recovery System (WinRE)? Diutak-atik sekian lama akhirnya penyakitnya ketemu. Ternyata susunan *booting* dalam BIOS (penghubung antara mesin dengan OS) alias *booting order* kembali ke pengaturan awal atau *default*.

Sebagai informasi, secara *default* OS pada laptop saya ditanam di perangkat *hard disk drive* (HDD). Kemudian saya *upgarde* dan memindah OS ke *solid state drive* (SSD) supaya kinerjanya lebih *was wis wus*.

Maka jika sistem berjalan normal *sequence* *booting-* nya seperti ini, Windows Boot Manager (untuk menentukan sistem mana yang akan dimuat), SSD (OS dalam SSD dimuat). Tapi dalam kasus saya, urutannya justru HDD dulu baru SSD padahal OS di HDD sudah *corrupt*.

Sehingga berbagai cara dilakukan, OS tetap menolak untuk dimuat karena sudah rusak. Oke karena sudah ketemu biang keroknya, saya mencoba mengubah urutan *booting* lewat BIOS. Tujuannya supaya SSD di posisi atas sebelum HDD karena OS yang tertanam di SSD belum ada masalah. Kalau saya kukuh membiarkan *booting order* apa adanya, maka sampai kapan pun OS tidak akan pernah bisa dimuat.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*_wuFVKQr0BwMgFFwBSdNSA.png)

Booting Order/Ist.

Ketika *booting order* telah saya ubah pada BIOS, maka secara teori mestinya semua akan normal. Tapi anehnya setelah *restart,* urutan itu kembali ke *default,* yaitu HDD di atas baru SSD.

Saya masih berasumsi ini hanya kesalahan biasa dan berpikir mengubahnya berkali-kali lewat BIOS, tapi hasilnya tetap sama. *Sequence* tetap memprioritaskan HDD sebagai *booting* awal alih-alih SSD.

Dari situ saya curiga pasti ada masalah lain, dan benar saja yang membuat pengaturan BIOS selalu kembali ke *default* adalah karena baterai CMOS (ini bukan baterai laptop), baterai yang menyuplai daya *chip* CMOS untuk menyimpan pengaturan BIOS, mengalami kerusakan.

Karena sudah diketahui masalahnya, maka pilihannya hanya ada dua;

> Pertama, saya mengganti baterai CMOS dulu; atau
> 
> kedua menghapus *file booting* untuk OS di HDD.

**Karena cara pertama lebih teknis, saya memilih cara kedua untuk mengeliminasi HDD dalam *booting order*. Kali ini bukan lewat BIOS, melainkan lewat *Command Prompt* (CMD) di Recovery System.**

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*mMSwqEtYf8zfXOJmrnq4hg.png)

Disk Checking di CMD/Ist.

**Baru setelah itu, OS bisa kembali dimuat karena menghilangkan HDD dalam *booting order*. Sehingga sistem langsung memuat OS yang terinstal dalam SSD.**

## Logika Demokrasi

==Dari proses== ==*ngutak-ngatik*== ==laptop ini saya terpikir soal asumsi yang keliru menghasilkan kesimpulan yang salah.==

> Bayangkan orang dijejali dogma bahwa demokrasi akan menghasilkan pemimpin yang baik, yang bakal memberikan kesejahteraan bagi rakyat.

Dogma ini disebar oleh para pendeta sekuler, yang seringnya diemban para intelektual. Tapi tidak semua intelektual mengamini dogma ini.

Saya melihat di lapangan, selama bertahun-tahun kita berdemokrasi tapi mimpi soal kesejahteraan serta pemerataan kekayaan dan kesempatan, justru jauh panggang dari api. Mestinya rakyat bisa memilih pemimpin dan kebijakan yang baik sehingga pada gilirannya akan menghadirkan kesejahteraan, t **api praktiknya tidak begitu.**

Jika berkaca pada insiden kerusakan laptop yang saya alami, maka kita harus berpikir;

“Mengapa laptop terus menerus mengalami gagal *booting*?”

> **Kegagalan *booting* dalam konteks demokrasi adalah kandasnya demokrasi dalam menghadirkan kesejahteraan dan pemerataan ekonomi bagi semua orang.**

Pemerataan ini tidak perlu dimaknai setiap orang mempunya harta yang sama, cukup mengecilkan ketimpangan. Jangan sampai dari 100 warga negara, separuhnya memperebutkan hanya 2,5 potong roti, sementara 10 orang terkaya justru memiliki 60 potong roti!

Sistem yang baik mestinya bekerja seperti peladen dalam sistem jaringan. Ia memastikan semua perangkat mendapatkan jaringan yang proporsional.

Dalam konteks ini, ia melakukan redistribusi kekayaan supaya tidak ada seorang pun yang tertinggal. Karena ketertinggalan ini memiliki efek yang maha dahsyat.

Misalnya begini, seorang anak yang terlahir dari keluarga miskin, berpeluang menjadi miskin lagi ketika dewasa. Seringnya bukan karena dia tak tertolong (malas atau bodoh), melainkan karena sistem memaksanya untuk tetap miskin lewat penyempitan kesempatan dan “membatasi” *resource* (saya sengaja memakai diksi aktif ketimbang pasif karena kemiskinan itu bukan sesuatu yang turun dari langit, ia hasil aktif buah desain sistem).

## Dogma

Maka mestinya, kita harus memahami demokrasi bukan seperti dogma agama yang ketika imam berkata A, kita percaya itu A.

> Apa pun yang tidak bisa didebat, disanggah atau digugat, itu adalah dogma dan siapa pun yang menganggap demokrasi demikian, dia tidak sedang berpolitik. Melainkan sedang beragama.

Sehingga jika demokrasi terus menerus mengalami kegagalan *booting*, *sequence* apa yang keliru atau ada masalah lain?

**Mayoritas opini publik yang dibimbing *influncer* (tokoh pemengaruh) *bilang* kalau yang membuat demokrasi gagal merealisasi janji kesejahteraan bagi sebagian besar orang, adalah ketidakdewasaan kita dalam berpolitik.**

Bagi mereka dewasa dalam berdemokrasi atau berpolitik adalah ketika masyarakat memilih pemimpin berdasarkan kalkulasi rasional, dengan melihat rekam jejak calon pemimpin.

Mereka percaya pada “mitos” bahwa ketika masyarakat berada dalam level dewasa dalam berdemokrasi, maka akan menghasilkan pemimpin yang kompeten.

> Ada asumsi yang tak terucap bahwa prasyarat membuat masyarakat dewasa dalam berdemokrasi adalah lewat pendidikan.

**Konsep soal kedewasaan dalam berdemokrasi sebetulnya secara tidak langsung mencomot logika John Stuart Mill, salah satu dedengkot filsuf liberal klasik, soal “masyarakat terbelakang.” Lewat buku “** [**On Liberty**](https://mega.nz/file/ulRHDIjB#KZNyyUDMEr3bT7H3l-KkgFZjL9Tw9beZqJcM4Vi1IA4) **” dia secara eksplisit merumuskan hierarki masyarakat dalam berdemokrasi.**

*Cuman* bedanya, dalam buku itu Mill mengizinkan untuk membatasi kebebasan pada masyarakat yang belum dewasa (*nonage*) atau menurut dia masyarakat terbelakang. Sehingga menurut Mill, kebebasan itu eksklusif untuk “ras Eropa,” ras yang bagi dia sudah dewasa berpolitik.

Sementara, intelektual di Indonesia memang mengakui ada masyarakat yang belum dewasa secara politik yang membuat demokrasi gagal “memuat” pemerataan kesejahteraan.

Namun sebagian besar tidak menyarankan untuk membatasi kebebasan mereka, tapi lebih ke menawarkan ramuan dengan mencerdaskan mereka, salah satunya lewat pendidikan.

Tapi apakah ramuan ini valid?

> Maksud saya apakah jika semua rakyat cerdas, demokrasi bakal menghasilkan pemimpin dan kebijakan yang baik, yang mampu menyejahterakan rakyat?

Tapi sebelum itu, pernah terpikirkan dari mana dasar mitos yang bilang kalau demokrasi pada akhirnya akan selalu menghasilkan keputusan yang baik?

## Konsep The Miracle of Aggregation

**Jadi selama bertahun-tahun, keyakinan itu ditopang oleh sebuah konsep statistik yang disebut *the miracle of aggregation*, atau keajaiban agregasi.** Asumsinya seperti ini, mayoritas pemilih itu buta huruf secara politik dan ekonomi.

Mereka sama sekali tidak tahu apa yang mereka pilih, dan pada dasarnya mereka hanya melempar koin atau menebak secara acak saat berada di bilik suara (ini terjadi di semua negara).

Jika asumsi itu benar, maka secara logika demokrasi seakan berjalan menuju bencana. Sebab mana mungkin “orang-orang yang *ngasal* ” dalam memilih bisa mendapatkan kebijakan yang baik?

**Namun ada cerita klasik tentang ini dari James Surowiecki, mengenai pameran sapi di desa**. Ceritanya begini, misalnya saya membawa seekor sapi yang sangat besar ke tengah pameran, lalu saya meminta seratus “orang awam” yang lewat untuk menebak berapa berat sapi tersebut.

Kalau saya tanya satu persatu, tebakan mereka mungkin akan sangat kacau. Namun, hasil rata-ratanya sering kali luar biasa akurat, menyamai atau bahkan mengalahkan tebakan seorang peternak sapi profesional. Itulah esensi dari konsep keajaiban agregasi.

Mengapa bisa begitu akurat? Karena kesalahan yang acak akan saling meniadakan. Orang yang menebak terlalu berat akan diimbangi oleh orang yang menebak terlalu ringan.

## Konteks Pemilu

Sekarang saya tarik konsep ini ke dalam pemilu, misalnya 99 persen pemilih sama sekali tidak tahu apa-apa dan memilih secara acak antara kandidat A dan kandidat B.

Suara mereka akan terpecah secara sempurna, 49,5 persen untuk A dan 49,5 persen untuk B. Sisa 1 persen pemilih nantinya yang menentukan hasil.

Kelompok 1 persen ini yang secara teori adalah pemilih yang benar-benar meluangkan waktu untuk membaca program kerja, paham ekonomi, dan rasional. Karena sisa 99 persen suaranya impas (49,5 vs. 49,5), maka 1 persen orang pintar inilah yang memecah kebuntuan.

Sehingga teorinya kelompok 1 persen tadi bakal memilih kandidat yang kompeten, karena mereka telah membaca program kerja, paham ekonomi, dan rasional. Jika dilihat melalui lensa ini, demokrasi terlihat sangat elegan.

Sistem ini seolah memiliki mekanisme pertahanan otomatis yang memastikan kebijakan yang baik akan menang, meskipun mayoritas warganya sama sekali tidak peduli dengan politik.

### Kelemahan Teori

**Teori keajaiban agregasi ini mempunyai satu kelemahan fatal.**

> **Bagaimana kalau tebakan para pemilih itu tidak acak? Bagaimana kalau mayoritas orang melakukan kesalahan sistematis?**

Misalnya begini;

Di sebuah ruang ujian pilihan ganda, pesertanya sama sekali tidak belajar dan tidak tahu jawaban yang benar. Kalau mereka murni menebak secara acak antara A, B, C, atau D, maka jawaban pasti akan terdistribusi merata.

Tapi bagaimana jika secara psikologis, seluruh peserta di ruangan itu merasa bahwa “huruf C terlihat paling menarik” atau ya paling menenangkan, lalu mereka semua serempak menjawab C? Kesalahan mereka tidak lagi saling meniadakan (tidak terdelusi), mereka melakukan kesalahan yang searah secara serempak.

## Rational Irrationality

**Ekonom Bryan Caplan lewat “** [**The Myth of the Rational Voter**](https://mega.nz/file/cUYF2RzC#go8pD10nbb9sO38RZQHQZupL8Zyj8SkPYLAWV-lisOo) **” memberikan penjelasan mengapa orang memilih jawaban yang salah secara berjamaah.** Ekonom George Mason University itu mencetuskan *rational irrationality*, atau irasionalitas rasional.

Saya tidak akan menjelaskan secara *textbook*, kita langsung meloncat ke contoh;

Misalnya begini saya sedang berbelanja di pasar atau supermarket. Lantas tiba-tiba saya memiliki keyakinan irasional bahwa meminum susu yang sudah basi dan berbau busuk itu sebenarnya baik untuk pencernaan.

Saya membeli susu basi itu, meminumnya, dan dalam hitungan jam saya dilarikan ke rumah sakit. Dalam contoh itu saya menanggung biaya penuh secara langsung dari kebodohan saya sendiri. Pasar memberikan hukuman yang sangat cepat bagi keyakinan yang salah.

Namun, mari kita pindah ke bilik suara. Secara matematis, peluang suara satu individu, suara saya, untuk mengubah hasil akhir dari sebuah pemilihan umum berskala nasional, itu hampir nol.

Karena peluang suara saya menjadi penentu hasil pemilu itu nyaris nol, maka biaya pribadi yang harus saya tanggung akibat memiliki keyakinan politik atau ekonomi yang salah, itu juga nyaris nol.

**Caplan memberikan sebuah ilustrasi dengan Robinson Crusoe (tokoh dalam novel karya Daniel Defoe dengan judul sama) tentang hal ini. Misalnya ada sebuah pulau yang dihuni oleh seribu orang kloningan Robinson Crusoe.**

Mereka harus mengadakan pemungutan suara untuk memutuskan apakah penduduk asli pulau itu, yang kita sebut saja Friday, diizinkan untuk bercocok tanam. Para Crusoe ini memiliki keyakinan yang sama sekali tidak berdasar secara ilmiah, semacam dogma emosional, bahwa Friday tidak bisa bertani. Padahal mungkin Friday adalah petani yang jauh lebih hebat.

Maka secara teori jika para Crusoe melarang Friday bertani, produksi makanan di pulau itu akan merosot tajam. Asumsinya kerugian ekonomi per kapita untuk setiap Crusoe akibat larangan itu adalah $1.000 (sekitar Rp16,9 juta). Tetapi, probabilitas suara satu Crusoe menjadi penentu dalam pemilu pulau itu hanyalah, katakanlah, 0,1 persen.

Kalau kerugian totalnya $1.000, tapi peluang suaranya menjadi penentu cuma 0,1 persen, berarti harga probabilitas dari “memegang keyakinan yang salah” itu hanyalah $1 (sekitar Rp16,9 ribu).

Dengan membayar harga probabilitas sebesar $1 saja, seorang Crusoe bisa masuk ke bilik suara, memuaskan egonya, merasa superior secara emosional, dan mengekspresikan biasnya tanpa rasa takut. Setelah itu dia mendapatkan kepuasan emosional secara gratis dan murah.

Tetapi ujung-ujungnya, karena semua orang berpikir dengan cara yang sama, kebijakan itu lolos, dan seluruh pulau harus menanggung kerugian ekonomi $1.000.

> Karena bias ini sangat murah secara psikologis, maka pemilih memborongnya.

==Supaya lebih membumi dan kontekstual, asumsikan begini 56 persen penduduk di suatu negara serempak memilih sepasang presiden dan wakilnya, bukan gara-gara kompetensi atau kinerjanya, tapi hanya karena misalnya kandidat itu “menggemaskan.”==

Massa akan dengan enteng mencoblos pasangan calon presiden bukan berdasarkan rasionalitas, melainkan seperti memainkan permainan iseng-iseng berhadiah karena konsekuensinya sering kali kabur.

Termasuk, ketika ada celetukan di masyarakat yang bilang;

“Siapa pun presidennya hidup kami *gini-gini* saja.”

> Celetukan ini yang membuat mereka tidak pernah memikirkan secara dalam soal politik yang bersih dari bias.

Karena mereka tidak menakuti apa pun atas konsekuensi dari pilihan politik itu, apalagi jika konsekuensinya ditanggung bareng-bareng.

Kalau kita pernah mendengar, ada juga celetukan berbunyi begini, “lebih baik salah *rame-rame*, daripada benar sendirian.” Orang takut benar, karena benar konsekuensinya “sendirian” dan sendiri itu “kesepian.”

**Lewat buku itu, Caplan benar-benar meruntuhkan “dongeng” utama dalam demokrasi, dongeng soal keajaiban agregasi.**

Berkaca dari pembacaan tadi, kita harus sungguh-sungguh bertanya;

> **“Apakah benar suara rakyat itu benar-benar “Suara Tuhan”?**

### Rakyat Paham Mana yang “Baik” Buat Mereka?

**Kalau tadi mengasumsikan rakyat gagal paham soal apa yang “baik” buat mereka, *folk theory* tentang demokrasi justru berasumsi rakyat mempunyai kekuatan penuh, punya keinginan kebijakan yang jelas.** Sehingga kita tinggal datang ke kotak suara untuk memilih pemimpin yang “akan melaksanakan” keinginan itu.

**Ini yang dalam Ilmu Politik disebut model spasial, sebuah model klasik dalam studi ini.**

*Biar tidak kayak lagi kuliah saya jelaskan begini*,

Anggap ada sebuah garis lurus yang mewakili spektrum politik, dari kiri ke kanan.

Teori ini berasumsi bahwa sebagian besar pemilih berkumpul di tengah garis tersebut, mereka inilah yang dikenal sebagai pemilih moderat.

Logikanya, jika partai politik ingin memenangkan pemilu, mereka harus bergerak ke tengah untuk merebut suara mayoritas itu.

Medan rebutan ini berisi “aspirasi populer” yang diidam-idamkan rakyat. Sehingga politisi yang ingin merebut hati rakyat, akan menawarkan janji-janji untuk mengeksekusi aspirasi tersebut.

> Model ini masuk akal, tapi hanya jika politik mempunyai satu dimensi saja, misalnya sekadar mengurus soal pajak.

Begitu kita memasukkan banyak isu sekaligus, seperti ekonomi, sosial, lingkungan, hingga kebijakan luar negeri; model itu langsung hancur.

Kehancuran model ini bukan sekadar spekulatif, tetapi ada bukti matematisnya. **Matematikawan Kenneth Arrow membuktikan lewat** [***Impossibility Theorem***](https://plato.stanford.edu/entries/arrows-theorem/) **\-nya bahwa ketika ada lebih dari dua pilihan dalam isu yang multidimensi, kehendak mayoritas yang koheren pada dasarnya tidak ada.**

Misalnya ada tiga kelompok pemilih yang harus memilih tiga kebijakan, kita sebut A, B, dan C. Kelompok pertama lebih suka A daripada B, B daripada C. Kelompok kedua suka B daripada C, C daripada A.

Kelompok ketiga suka C daripada A, A daripada B. Jika diadu satu per satu dalam pemungutan suara, A mengalahkan B, B mengalahkan C, tapi C mengalahkan A. Persis seperti batu-gunting-kertas yang tidak mempunyai pemenang absolut.

> Artinya, apa yang akhirnya diloloskan sebagai “kehendak rakyat” sebenarnya hanya ilusi. Hasil akhirnya sangat bergantung pada siapa yang menyusun agenda atau urutan pemungutan suara.

Gagasan bahwa ada satu kebijakan tunggal yang paling memuaskan mayoritas rakyat, secara matematis, berdasarkan teorema ini sering kali tidak nyata.

## Framing Effect

Oke, berarti secara model matematis rakyat itu sebetulnya tidak paham mana yang baik buat mereka, **karena semuanya bergantung siapa yang menyusun agenda untuk dilempar ke tengah publik.**

Tapi memang untuk isu yang dekat dengan kehidupan sehari-hari, seperti anggaran kemiskinan atau layanan kesehatan, orang pasti mempunyai pendirian yang kuat.

Artinya, mereka bakal menginginkan agenda-agenda populer (agenda bulat). Meskipun demikian, ternyata tetap tidak sekuat yang kita bayangkan.

**Dalam “** [**Democracy for Realists**](https://mega.nz/file/sRgBkDwA#rCmDZFKIjjCzjNp3czWIWnLMXXC1m5vjSNpix7rwbm8) **” karya Christopher H. Achen dan Larry Bartels menyajikan contoh nyata tentang *framing effect*.**

Di Amerika Serikat, peneliti melakukan survei opini berskala besar.

Ketika warga ditanya apakah pemerintah menghabiskan terlalu sedikit anggaran untuk bantuan bagi orang miskin?

> Sekitar 63 hingga 65 persen orang Amerika mendukung peningkatan anggaran tersebut.

Pada kelompok survei yang lain, peneliti menanyakan kebijakan yang sama persis (jumlah anggarannya sama, sasarannya sama) tetapi hanya mengubah satu frasa;

“Bantuan bagi orang miskin” diganti dengan “kesejahteraan atau *welfare”*.

Hasilnya?

> Dukungan anjlok ke angka 20 hingga 25 persen. Hanya karena satu kata diganti.

==Jika mengubah satu kata benda dalam kuesioner bisa menghapus dukungan dari puluhan juta orang, kita harus jujur bertanya; “== ==**Seberapa nyata dan seberapa rasional sebenarnya preferensi kebijakan pemilih itu?”**==

Jika pendirian publik serapuh itu, maka klaim bahwa rakyat mempunyai kehendak yang jelas dan konsisten adalah dongeng yang sangat indah tapi tidak berdasar.

Ini perlu sangat saya tekankan, Amerika itu bukan negara *kaleng-kaleng*. Sebanyak 50,7% warga usia produktif di sana memiliki gelar universitas. **Sehingga temuan Achen dan Bartels adalah bantahan keras terhadap asumsi yang bilang “Kalau di masyarakat terdidik, demokrasi bakal berjalan dengan baik.”**

**Masih tidak percaya? Ada penelitian Gabriel Lenz tentang pemilu Presiden AS tahun 2000 antara George W. Bush dan Al Gore, mengungkap fenomena psikologis yang juga meruntuhkan dongeng soal demokrasi.**

Saat itu, salah satu perdebatan terpanas adalah soal privatisasi jaminan sosial.

Logika dongengnya begini, saya mendukung privatisasi, saya dengar Bush mendukung privatisasi, maka saya pilih Bush.

Tapi setelah mewawancarai pemilih yang sama berkali-kali selama masa kampanye, Lenz menemukan yang terjadi justru sebaliknya. Seseorang yang sejak awal sudah menyukai Bush (entah karena gaya bicaranya yang santai, karena partainya, atau karena citranya) kemudian mendengar bahwa Bush mendukung privatisasi jaminan sosial.

==Alih-alih mengevaluasi posisi itu secara kritis, pemilih ini secara psikologis mengubah pandangannya sendiri tentang jaminan sosial agar sesuai dengan opini kandidat idolanya.==

Maka ini bukan evaluasi, ini rasionalisasi. Pemilih bertindak lebih mirip “pendukung fanatik klub sepak bola” alias hooligan.

> Anda tidak mendukung sebuah klub karena strategi formasi mereka sejalan dengan filosofi sepak bola Anda. Anda mendukungnya karena kota asal Anda, atau karena sejarah keluarga.

Lalu Anda akan membenarkan “strategi seburuk apa pun” (dalam konteks politik kebijakan) yang dipakai pelatih klub tersebut, asal menang.

Makanya coba perhatikan, kaum yang “katanya terdidik,” ketika Pilpres 2014 dan Pilpres 2019 fanatik dengan kandidat presiden Joko Widodo atau Prabowo Subianto. Kedua pendukung seolah-oleh mempunyai jalan kebijakan berbeda.

Pendukung Jokowi “menyerang” tanpa ampun gagasan Prabowo, pun pendukung Prabowo sebaliknya. Namun ketika di Pilpres 2024 tiba, dan keduanya sudah saling merangkul. Kebijakan-kebijakan yang semula saling mereka lawan, kini banyak didukung mati-matian.

Pendukung Jokowi misalnya, ketika Jokowi mengisyaratkan dukungan kuat terhadap pencalonan Prabowo di Pilpres 2024, tidak sedikit dari mereka ikut begitu saja. Padahal Prabowo di 2014 dan 2019 saat mereka lawan mati-matian adalah Prabowo yang sama, tidak ada pergeseran ideologi atau gagasan. Begitu juga sebaliknya terhadap pendukung Prabowo yang pernah menyerang Jokowi gila-gilaan.

**Sehingga temuan dari Lenz ini menguatkan argumen bahwa pola hooligan (mereka yang fanatik terhadap politisi) dalam politik, itu bukan eksklusif di negara dengan tingkat pendidikan rendah.** Justru orang-orang terdidik juga tidak kalah fanatik terhadap politisi ketimbang mereka yang tidak terdidik.

> Artinya omongan yang bilang “demokrasi bakal sempurna” kalau semua masyarakat terdidik itu tidak lebih dari omong kosong.

Anggap misalnya mitos soal “masyarakat yang cerdas” bakal menghasilkan pemimpin dan kebijakan yang baik itu benar.

> Pertanyaan saya, bagaimana menghasilkan masyarakat yang cerdas kalau yang terpilih selalu pemimpin yang tidak mau mengutamakan pendidikan?

Bagaimana supaya orang kompeten dengan rekam jejak baik dan menjamin akan memprioritaskan pendidikan sehingga masyarakat bisa cerdas, itu bisa terpilih dalam pemilu?

Ya, masyarakat harus cerdas dan apa ganjalan membuat masyarakat cerdas?

> **Balik lagi tadi ke awal, terus saja berputar-putar seperti itu tanpa ada titik akhir.**

Saya sudah membongkar semua asumsi-asumsi keliru atau mitos yang dipercaya banyak kalangan (bahkan kalangan yang katanya terdidik) soal demokrasi. Seperti upaya saya mencari kegagalan dalam *booting* laptop, kegagalan *booting* dalam demokrasi ternyata bukan karena salah menempatkan *booting order* atau baterai CMOS yang habis (dalam konteks ini masyarakat yang tidak terdidik).

> ==Tapi lebih dalam lagi, demokrasi memang “didesain” untuk tidak pernah menghasilkan kebijakan yang baik, terutama bagi kaum mayoritas terbawah dalam ekonomi.==

Ketimpangan di negara demokrasi tidak ubahnya dengan ketimpangan ekonomi yang terjadi di negara-negara yang tidak menerapkan demokrasi.

Lalu, apa solusinya?

==Adakah sistem lain yang lebih baik? Tulis keresahanmu di kolom komentar.==[Last published 12 hours ago](https://medium.com/berbagi-berdampak/influencer-c3a4dcf8582f?source=post_page---post_publication_info--f5eb031611f1---------------------------------------)

Hidup terlalu singkat untuk dimiliki sendirian. Kami mengajak berbagi untuk memberikan dampak bersama. Tautan mendaftar sebagai penulis: [http://bit.ly/form-berbagi-berdampak](http://bit.ly/form-berbagi-berdampak)

## Responses (10)

Raja Premium 88[putrimelati\_123](https://medium.com/@putrimelati0873?source=post_page---post_responses--f5eb031611f1----0-----------------------------------)

[

Apr 5

](https://medium.com/@putrimelati0873/aku-juga-pernah-menulis-bahwa-demokrasi-ternyata-bukan-sistem-terbaik-sebelum-pilpres-kemaren-0f5d0459fbc2?source=post_page---post_responses--f5eb031611f1----0-----------------------------------)

==Adakah sistem lain yang lebih baik? Tulis keresahanmu di kolom komentar.==

```c
Aku juga pernah menulis bahwa demokrasi ternyata bukan sistem terbaik sebelum pilpres kemaren. 

Menurutku sistem terbaik ya seperti zaman Rasulullah jadi khalifah.
```

3

==Alih-alih mengevaluasi posisi itu secara kritis, pemilih ini secara psikologis mengubah pandangannya sendiri tentang jaminan sosial agar sesuai dengan opini kandidat idolanya.==

```c
Saya pernah menonton video yg menjelaskan tentang ini di channel YouTube Veritasium, dan kesimpulan yang saya tarik bahwa orang pintar sekalipun akan jadi "bodoh" begitu sudah membahas politik..
```

2

==Supaya lebih membumi dan kontekstual, asumsikan begini 56 persen penduduk di suatu negara serempak memilih sepasang presiden dan wakilnya, bukan gara-gara kompetensi atau kinerjanya, ta...==

```c
Ada satu influencer wanita terkenal dengan "otak kosongnya" yang sekaligus menjadi nilai jualnya, ngomong bahwa dia memilih salah satu kandidat capres dan cawapres karena menurut dia mereka itu gemoy..

Bayangkan berapa banyak orang yang terpengaruh gara-gara ucapannya di media sosial itu...

Anyway, tulisan ini bagus sekali!
```

1
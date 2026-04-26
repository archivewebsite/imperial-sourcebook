# Catatan Git: Perintah Esensial

---

## Daftar Isi
1. [Perintah dari Daftar Anda](#1-perintah-dari-daftar-anda)
2. [Perintah Penting yang Perlu Anda Tahu](#2-perintah-penting-yang-perlu-anda-tahu)
3. [Alur Kerja Lengkap: Dari Nol ke GitHub](#3-alur-kerja-lengkap-dari-nol-ke-github)

---

## 1. Perintah dari Daftar Anda

---

### `git add .`

**Fungsi:** Memasukkan *semua* perubahan di direktori kerja saat ini ke dalam *staging area* — area penampungan sebelum perubahan dikunci sebagai commit.

Tanda titik (`.`) berarti "semua file yang berubah di direktori ini dan subfolder-nya." Jika ingin menambahkan satu file saja, ganti titik dengan nama file.

**Contoh nyata:**

Anda baru mengubah tiga file: `index.html`, `style.css`, dan `app.js`.

```bash
git add .
# Ketiga file masuk ke staging area sekaligus

git add index.html
# Hanya index.html yang masuk staging area
```

**Peringatan:** `git add .` tidak memilah — semua file yang berubah ikut masuk, termasuk file yang tidak ingin Anda commit. Gunakan `.gitignore` untuk mengecualikan file tertentu (misalnya file `.env` berisi password).

---

### `git commit -m "Commit pertama saya"`

**Fungsi:** Mengunci snapshot semua file yang ada di staging area menjadi satu titik sejarah permanen di repositori lokal. Flag `-m` diikuti pesan yang mendeskripsikan isi perubahan.

Commit bersifat lokal — belum ada yang dikirim ke server sampai Anda menjalankan `git push`.

**Contoh nyata:**

```bash
git commit -m "Tambah halaman login dan validasi form"
# Pesan spesifik: orang lain (atau Anda di masa depan) langsung tahu isi commit ini

git commit -m "Fix bug"
# Pesan buruk: tidak memberi informasi apa pun tentang bug mana yang diperbaiki
```

**Konvensi pesan commit yang baik:**
- Gunakan kalimat imperatif: "Tambah fitur X", bukan "Menambahkan fitur X"
- Maksimal 72 karakter untuk baris pertama
- Jika perubahan kompleks, tambahkan deskripsi detail di baris kedua setelah baris kosong

---

### `git branch -M main`

**Fungsi:** Mengganti nama branch *aktif saat ini* menjadi `main`. Flag `-M` (huruf besar) memaksa penggantian nama meski nama `main` sudah ada di repositori.

GitHub menggunakan `main` sebagai nama branch default sejak 2020. Repositori lama mungkin masih menggunakan nama `master`.

**Contoh nyata:**

```bash
# Anda baru saja git init, branch default bernama "master"
git branch -M main
# Branch aktif sekarang bernama "main"

git branch
# Output: * main
```

Perintah ini hanya relevan dijalankan sekali saat setup awal repositori baru.

---

### `git remote add origin <URL>`

**Fungsi:** Menghubungkan repositori lokal Anda ke repositori di server (misalnya GitHub) dengan memberi nama alias `origin` pada URL tersebut.

`origin` adalah konvensi nama — secara teknis bisa diganti nama lain, tapi seluruh ekosistem Git menggunakan `origin` sebagai standar untuk remote utama.

**Contoh nyata:**

```bash
git remote add origin https://github.com/username/nama-proyek.git

# Verifikasi koneksi berhasil:
git remote -v
# Output:
# origin  https://github.com/username/nama-proyek.git (fetch)
# origin  https://github.com/username/nama-proyek.git (push)
```

Jika salah mengetik URL, perbaiki dengan:
```bash
git remote set-url origin https://github.com/username/url-yang-benar.git
```

---

### `git push -u origin main`

**Fungsi:** Mengirim commit dari branch `main` lokal ke remote `origin`, sekaligus menetapkan `origin/main` sebagai *upstream* default untuk branch ini.

Flag `-u` (atau `--set-upstream`) hanya perlu digunakan sekali. Setelah itu, cukup ketik `git push` tanpa argumen tambahan.

**Contoh nyata:**

```bash
# Pertama kali push ke GitHub:
git push -u origin main
# Output: Branch 'main' set up to track remote branch 'main' from 'origin'.

# Push berikutnya (sudah ada upstream):
git push
# Tidak perlu tulis "origin main" lagi
```

---

### `git push -f origin main`

**Fungsi:** Memaksa (*force*) server untuk menerima push Anda, bahkan jika push tersebut akan menimpa commit yang sudah ada di remote. Ini menghapus permanen history yang ada di server dan menggantinya dengan history lokal Anda.

**Kapan digunakan:** Setelah `git rebase` atau `git commit --amend` yang mengubah history commit yang sudah pernah di-push.

**Contoh nyata:**

```bash
# Anda sudah push commit A → B → C ke GitHub
# Lalu Anda amend commit C secara lokal, history lokal jadi A → B → C'
# git push biasa akan ditolak karena history berbeda

git push -f origin main
# Paksa GitHub menerima A → B → C' dan hapus C yang lama
```

**Peringatan keras:** Jangan jalankan `git push -f` di branch yang digunakan bersama tim. Commit orang lain yang sudah di-push akan terhapus dari remote dan menyebabkan konflik besar. Alternatif lebih aman untuk kolaborasi: `git push --force-with-lease` (dijelaskan di bagian bawah).

---

### `git rebase --abort`

**Fungsi:** Membatalkan proses `git rebase` yang sedang berjalan dan mengembalikan branch ke kondisi sebelum rebase dimulai.

**Kapan digunakan:** Saat rebase memunculkan konflik yang terlalu rumit untuk diselesaikan saat ini, atau Anda menyadari strategi rebase Anda salah.

**Contoh nyata:**

```bash
# Anda menjalankan rebase dan muncul konflik di tengah jalan:
git rebase main
# CONFLICT (content): Merge conflict in src/app.js
# error: could not apply a1b2c3d... Tambah fitur login

# Opsi 1: Selesaikan konflik, lanjutkan rebase
# (edit file, git add ., git rebase --continue)

# Opsi 2: Batalkan seluruh rebase, kembali ke kondisi semula
git rebase --abort
# HEAD is now at a1b2c3d Commit terakhir sebelum rebase
```

Setelah `--abort`, semua perubahan yang terjadi selama proses rebase dibatalkan. Branch kembali persis seperti sebelum rebase dimulai.

---

## 2. Perintah Penting yang Perlu Anda Tahu

---

### `git status`

**Fungsi:** Menampilkan kondisi repositori saat ini: file mana yang berubah, file mana yang sudah di-staging, dan file mana yang belum di-track Git.

Ini perintah paling sering digunakan — jalankan sebelum `git add` dan sebelum `git commit` untuk memastikan Anda tidak commit file yang salah.

**Contoh nyata:**

```bash
git status
# Output:
# On branch main
# Changes to be committed:
#   (use "git restore --staged <file>..." to unstage)
#         modified:   index.html        ← sudah di-staging
#
# Changes not staged for commit:
#   modified:   style.css             ← belum di-staging
#
# Untracked files:
#   secret.env                        ← belum pernah di-track sama sekali
```

---

### `git log --oneline`

**Fungsi:** Menampilkan history commit dalam format ringkas — satu baris per commit, berisi hash pendek dan pesan commit.

**Contoh nyata:**

```bash
git log --oneline
# Output:
# f3a9b2c Tambah validasi email di form registrasi
# d1e8a7f Perbaiki bug crash saat user logout
# 9c4b1e2 Setup project awal
```

Untuk melihat history dalam bentuk grafik branch:
```bash
git log --oneline --graph --all
```

---

### `git diff`

**Fungsi:** Menampilkan perubahan baris per baris antara kondisi file saat ini dengan kondisi di commit terakhir (atau antara dua commit).

**Contoh nyata:**

```bash
git diff
# Tampilkan semua perubahan yang belum di-staging

git diff --staged
# Tampilkan perubahan yang sudah di-staging (akan masuk commit berikutnya)

git diff HEAD~1 HEAD
# Bandingkan commit terakhir dengan commit sebelumnya
```

---

### `git stash`

**Fungsi:** Menyimpan sementara perubahan yang belum di-commit ke tumpukan tersembunyi (*stash*), sehingga direktori kerja kembali bersih. Berguna saat Anda perlu berpindah branch tapi tidak mau commit perubahan yang belum selesai.

**Contoh nyata:**

```bash
# Anda sedang mengerjakan fitur baru, tiba-tiba ada bug urgent di branch main
git stash
# Perubahan Anda tersimpan, working directory bersih

git checkout main
# Perbaiki bug, commit, push

git checkout feature-branch
git stash pop
# Perubahan yang tadi disimpan kembali muncul
```

---

### `git restore` dan `git restore --staged`

**Fungsi:** `git restore <file>` membuang perubahan pada file dan mengembalikannya ke kondisi commit terakhir. `git restore --staged <file>` mengeluarkan file dari staging area tanpa membuang perubahannya.

**Contoh nyata:**

```bash
# Anda mengacaukan style.css dan ingin memulai ulang:
git restore style.css
# style.css kembali ke kondisi commit terakhir — perubahan hilang permanen

# Anda tidak sengaja git add file yang salah:
git restore --staged secret.env
# secret.env keluar dari staging area, perubahannya masih ada di file
```

---

### `git branch` dan `git checkout -b`

**Fungsi:** `git branch` menampilkan daftar branch. `git checkout -b <nama>` membuat branch baru sekaligus berpindah ke branch tersebut.

**Contoh nyata:**

```bash
git branch
# Output:
# * main          ← tanda * = branch aktif saat ini
#   fitur-login

git checkout -b fitur-registrasi
# Branch baru "fitur-registrasi" dibuat dari kondisi main saat ini
# Anda otomatis berpindah ke branch tersebut

# Cara modern (Git 2.23+):
git switch -c fitur-registrasi
```

---

### `git merge`

**Fungsi:** Menggabungkan perubahan dari satu branch ke branch aktif.

**Contoh nyata:**

```bash
# Anda sudah selesai mengerjakan fitur-login dan ingin gabungkan ke main:
git checkout main
git merge fitur-login
# Semua commit dari fitur-login masuk ke main

# Hapus branch yang sudah tidak diperlukan:
git branch -d fitur-login
```

---

### `git pull`

**Fungsi:** Mengambil perubahan terbaru dari remote dan langsung menggabungkannya ke branch lokal. Ekuivalen dengan `git fetch` + `git merge`.

**Contoh nyata:**

```bash
# Rekan tim Anda baru push perubahan ke main di GitHub:
git pull origin main
# Perubahan mereka masuk ke branch main lokal Anda

# Jika ingin pull dengan rebase (history lebih bersih):
git pull --rebase origin main
```

---

### `git push --force-with-lease`

**Fungsi:** Versi aman dari `git push -f`. Memaksa push hanya jika tidak ada commit baru di remote yang belum Anda fetch — sehingga tidak menimpa pekerjaan orang lain secara tidak sengaja.

**Contoh nyata:**

```bash
# Lebih aman dari git push -f saat bekerja di tim:
git push --force-with-lease origin fitur-login

# Jika ada orang lain yang push ke branch yang sama setelah Anda fetch terakhir,
# perintah ini akan ditolak — bukan menimpa commit mereka diam-diam
```

---

### `git reset`

**Fungsi:** Memindahkan HEAD (penunjuk commit aktif) ke commit tertentu. Ada tiga mode:
- `--soft`: Batalkan commit, perubahan tetap ada di staging area
- `--mixed` (default): Batalkan commit, perubahan kembali ke working directory
- `--hard`: Batalkan commit, perubahan dihapus permanen

**Contoh nyata:**

```bash
# Anda commit terlalu cepat, ingin batalkan commit terakhir:
git reset --soft HEAD~1
# Commit dibatalkan, file tetap di staging area → tinggal edit dan commit ulang

git reset --mixed HEAD~1
# Commit dibatalkan, file kembali ke working directory → perlu git add ulang

git reset --hard HEAD~1
# Commit dibatalkan, semua perubahan di commit itu hilang permanen
```

---

### `.gitignore`

**Fungsi:** File konfigurasi (bukan perintah) yang memberi tahu Git daftar file atau folder yang harus diabaikan — tidak di-track, tidak masuk staging, tidak ikut commit.

**Contoh nyata:**

Buat file bernama `.gitignore` di root proyek:

```
# File environment berisi API key dan password
.env
.env.local

# Folder dependencies Node.js (bisa di-install ulang kapan saja)
node_modules/

# File build hasil kompilasi
dist/
build/

# File sistem operasi
.DS_Store        # macOS
Thumbs.db        # Windows
```

Setelah `.gitignore` dibuat, file-file tersebut tidak akan muncul di `git status` dan tidak bisa di-`git add` secara tidak sengaja.

---

## 3. Alur Kerja Lengkap: Dari Nol ke GitHub

Berikut urutan perintah yang benar untuk memulai proyek baru dan menghubungkannya ke GitHub:

```bash
# 1. Buat folder proyek dan masuk ke dalamnya
mkdir proyek-saya && cd proyek-saya

# 2. Inisialisasi repositori Git
git init

# 3. Buat file pertama
echo "# Proyek Saya" > README.md

# 4. Buat .gitignore
echo "node_modules/" > .gitignore

# 5. Masukkan file ke staging area
git add .

# 6. Buat commit pertama
git commit -m "Inisialisasi proyek"

# 7. Rename branch ke main
git branch -M main

# 8. Hubungkan ke repositori GitHub (buat dulu di github.com)
git remote add origin https://github.com/username/proyek-saya.git

# 9. Push ke GitHub (pertama kali, gunakan -u)
git push -u origin main

# --- Alur kerja harian setelahnya ---

# 10. Buat branch baru untuk fitur
git checkout -b fitur-baru

# 11. Kerjakan perubahan, lalu:
git add .
git commit -m "Tambah fitur baru"

# 12. Push branch ke GitHub
git push origin fitur-baru

# 13. Setelah fitur selesai, gabungkan ke main
git checkout main
git merge fitur-baru
git push

# 14. Hapus branch yang sudah tidak diperlukan
git branch -d fitur-baru
git push origin --delete fitur-baru
```

---

*Catatan dibuat: Maret 2026*

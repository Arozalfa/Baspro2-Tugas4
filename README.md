﻿# Baspro2-Tugas4

### Penjelasan Kode: Perkalian Matriks \( 5 \times 5 \)

Kode ini bertujuan menghitung hasil perkalian dua matriks berukuran \( 5 \times 5 \): \( A \) dan \( B \). Berikut adalah penjelasan langkah-langkahnya:

---

#### **1. Matriks Input**
- **Matriks \( A \)**: 
  Sebuah matriks berukuran \( 5 \times 5 \) dengan elemen bernilai berturut-turut dari 1 hingga 25, diatur dalam baris dan kolom. Contohnya:
  \[
  A =
  \begin{bmatrix}
  1 & 2 & 3 & 4 & 5 \\
  6 & 7 & 8 & 9 & 10 \\
  11 & 12 & 13 & 14 & 15 \\
  16 & 17 & 18 & 19 & 20 \\
  21 & 22 & 23 & 24 & 25
  \end{bmatrix}
  \]

- **Matriks \( B \)**:
  Matriks \( B \) memiliki elemen-elemen acak yang digunakan sebagai operand kedua dalam perkalian matriks:
  \[
  B =
  \begin{bmatrix}
  1 & 0 & 4 & 0 & 1 \\
  0 & 3 & 0 & 3 & 4 \\
  0 & 1 & 5 & 0 & 2 \\
  1 & 2 & 0 & 2 & 0 \\
  1 & 0 & 1 & 7 & 1
  \end{bmatrix}
  \]

---

#### **2. Inisialisasi Matriks Hasil**
Sebuah matriks kosong, \( hasil \), dibuat untuk menyimpan elemen-elemen hasil dari operasi perkalian.

---

#### **3. Logika Perkalian Matriks**
Proses perkalian matriks dilakukan menggunakan **loop bertingkat**:
1. **Loop luar pertama** (`for i in range(5)`):  
   Iterasi ini mewakili baris \( i \) dari matriks \( A \). Setiap iterasi menghasilkan satu baris dalam matriks hasil.

2. **Loop tengah kedua** (`for j in range(5)`):  
   Iterasi ini mewakili kolom \( j \) dari matriks \( B \). Setiap iterasi menghasilkan satu elemen dari baris \( i \) dan kolom \( j \) dalam matriks hasil.

3. **Loop terdalam ketiga** (`for k in range(5)`):  
   - Digunakan untuk menghitung elemen \( hasil[i][j] \).
   - Elemen \( hasil[i][j] \) dihitung sebagai jumlah dari produk elemen baris \( i \) dari \( A \) dengan elemen kolom \( j \) dari \( B \).  
     Secara matematis:
     \[
     hasil[i][j] = \sum_{k=0}^{4} A[i][k] \times B[k][j]
     \]

---

#### **4. Menyimpan Elemen ke Matriks Hasil**
Setelah elemen \( hasil[i][j] \) dihitung, nilai ini dimasukkan ke dalam list `baris`. Setelah semua kolom \( j \) selesai, list `baris` ditambahkan ke matriks `hasil`.

---

#### **5. Menampilkan Matriks Hasil**
Setelah selesai, matriks `hasil` dicetak elemen-elemennya baris demi baris. Hasil ini adalah matriks yang merepresentasikan \( A \times B \).

---

#### **Hasil dari Kode**
Mari kita jalankan kode ini untuk menghitung matriks hasil.

### Hasil Perkalian Matriks \( A \times B \)

Matriks hasil adalah:

\[
\text{Hasil} =
\begin{bmatrix}
10 & 17 & 24 & 49 & 20 \\
25 & 47 & 74 & 109 & 60 \\
40 & 77 & 124 & 169 & 100 \\
55 & 107 & 174 & 229 & 140 \\
70 & 137 & 224 & 289 & 180
\end{bmatrix}
\]

---

### Penjelasan
- **Setiap elemen dalam hasil** dihitung sebagai jumlah perkalian elemen baris dari matriks \( A \) dengan elemen kolom dari matriks \( B \).
- Contoh:
  - Elemen di baris 1 kolom 1 (\( 10 \)):
    \[
    10 = (1 \times 1) + (2 \times 0) + (3 \times 0) + (4 \times 1) + (5 \times 1)
    \]
  - Elemen di baris 3 kolom 4 (\( 169 \)):
    \[
    169 = (11 \times 0) + (12 \times 3) + (13 \times 0) + (14 \times 2) + (15 \times 7)
    \]

Kode berhasil menghitung matriks hasil perkalian \( A \) dan \( B \).

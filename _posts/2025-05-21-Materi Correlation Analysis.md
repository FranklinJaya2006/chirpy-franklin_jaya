---
title: "Materi Correlation Analysis"
date: 2025-04-16 10:00:00 +0700
categories: [Pearson, Spearman, Korelasi]
tags: ["Statistik dan Probabilitas", "Distribusi Data", "R"]
---

# Correlation Analysis

---

## Apa itu Korelasi?
Korelasi mengukur **kekuatan** dan **arah hubungan linier** antara dua variabel numerik.

---

## Daftar Isi
- [Jenis Korelasi](#jenis-korelasi)
  - [Korelasi Pearson](#1-korelasi-pearson)
    - [Deskripsi](#deskripsi)
    - [Syarat Penggunaan](#syarat-penggunaan)
    - [Interpretasi Nilai Korelasi](#interpretasi-nilai-korelasi)
    - [Contoh Kasus Pearson](#contoh-kasus-pearson)
  - [Korelasi Spearman](#2-korelasi-spearman)
    - [Deskripsi](#deskripsi-1)
    - [Karakteristik](#karakteristik)
    - [Langkah Perhitungan di Excel](#langkah-perhitungan-di-excel)
    - [Contoh Kasus Spearman](#contoh-kasus-spearman)
- [Kesimpulan](#kesimpulan)

---

## Jenis Korelasi

### 1. Korelasi Pearson

#### Deskripsi
- Digunakan untuk data numerik (interval/rasio) dengan **hubungan linier**.
- Mengukur kekuatan dan arah hubungan linier antar dua variabel.
- Sensitif terhadap **outlier**.
- Paling umum digunakan dalam analisis statistik.

#### Syarat Penggunaan
- Data dalam skala **interval atau rasio**.
- Hubungan antar variabel **linier**.
- Tidak banyak **outlier**.
- (Idealnya) data terdistribusi **normal**.

#### Interpretasi Nilai Korelasi
Berlaku untuk **Pearson** maupun **Spearman**:

- **r > 0**: Hubungan positif (semakin besar X, semakin besar Y).
- **r < 0**: Hubungan negatif (semakin besar X, semakin kecil Y).
- **r ≈ 0**: Tidak ada hubungan linier.

| Nilai r / ρ       | Interpretasi Umum             |
|-------------------|-------------------------------|
| 0.00 – 0.19       | Sangat lemah / tidak ada      |
| 0.20 – 0.39       | Lemah                         |
| 0.40 – 0.59       | Cukup                         |
| 0.60 – 0.79       | Kuat                          |
| 0.80 – 1.00       | Sangat kuat                   |

#### Contoh Kasus Pearson
Misalkan dua variabel skor dan jumlah jam belajar menghasilkan korelasi `r = 0.82`.  
Interpretasinya: **hubungan linier positif yang sangat kuat**.

---

### 2. Korelasi Spearman

#### Deskripsi
- Digunakan untuk **data ordinal** atau hubungan **non-linier tapi monotonic**.
- Tidak memerlukan distribusi normal.
- Berdasarkan **peringkat (ranking)** dari nilai-nilai.
- Cocok digunakan jika data **tidak memenuhi asumsi Pearson**.

#### Karakteristik
- Tidak sensitif terhadap bentuk distribusi data.
- Tidak terpengaruh secara signifikan oleh **outlier**.

#### Langkah Perhitungan di Excel

- **Spearman:**  
  1. Ranking dulu data X dan Y dengan `=RANK.AVG(...)`.  
  2. Setelah itu langsung hitung korelasi dengan:  
     ```excel
     =CORREL(rankX_range, rankY_range)
     ```

- **Pearson:**  
  Langsung gunakan fungsi:  
  ```excel
  =CORREL(X_range, Y_range)

#### Contoh Kasus Spearman

| Math | English |
|------|---------|
| 70   | 60      |
| 70   | 65      |
| 80   | 70      |
| 85   | 75      |
| 90   | 80      |

1. **Ranking Math** → [1.5, 1.5, 3, 4, 5]  
2. **Ranking English** → [1, 2, 3, 4, 5]  
3. Hitung korelasi:  
   ```excel
   =CORREL(rankMath, rankEnglish)


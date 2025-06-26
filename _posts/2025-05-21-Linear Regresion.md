---
title: "Lecture 9 - Linear Regression"
date: 2025-06-26
categories: [Statistik, Regresi, R]
tags: ["Linear Regression", "Probabilistik", "R", "Statistik"]
---

# 📘 Linear Regression

## 📑 Daftar Isi

1. [Tujuan Pembelajaran](#tujuan-pembelajaran)
2. [Apa Itu Regresi?](#apa-itu-regresi)
3. [Pengantar Regresi](#pengantar-regresi)
4. [Terminologi dalam Regresi](#terminologi-dalam-regresi)
5. [Alasan Menggunakan Regresi Linear](#alasan-menggunakan-regresi-linear)
6. [Model Probabilistik Linear](#model-probabilistik-linear)
7. [Interpretasi Grafis](#interpretasi-grafis)
8. [Contoh Kasus Linear Regression](#contoh-kasus-linear-regression)
9. [Estimasi Parameter Model](#estimasi-parameter-model)
10. [Prediksi dan Residual](#prediksi-dan-residual)
11. [Multiple Linear Regression](#multiple-linear-regression)
12. [Variabel Independen Kategorik](#variabel-independen-kategorik)
13. [Uji Hipotesis (Omnibus Test)](#uji-hipotesis-omnibus-test)
14. [Formulasi ANOVA untuk Omnibus Test](#formulasi-anova-untuk-omnibus-test)
15. [F-Test untuk Subset Variabel](#f-test-untuk-subset-variabel)
16. [Uji Hipotesis Koefisien Individual](#uji-hipotesis-koefisien-individual)
17. [Pemeriksaan Asumsi Model](#pemeriksaan-asumsi-model)
18. [Fixed Effects vs Random Effects](#fixed-effects-vs-random-effects)

---

## Tujuan Pembelajaran

- Memahami dasar regresi linear dari sudut pandang probabilistik.
- Mengestimasi parameter dan melakukan uji hipotesis dalam model linear.
- Mengimplementasikan regresi linear di R.

---

## Apa Itu Regresi?

- **Regresi** adalah teknik statistik yang digunakan untuk memodelkan dan menganalisis hubungan antara satu variabel dependen (**Y**) dan satu atau lebih variabel independen (**X**).
- Tujuannya adalah untuk:
  - Menjelaskan bagaimana **Y dipengaruhi oleh X**
  - Melakukan **prediksi** nilai Y berdasarkan nilai X
  - Melakukan **estimasi parameter**
  - Melakukan **pengujian hipotesis**
  - Memodelkan hubungan **kausalitas**

> 🔍 Intinya: Jika kamu tahu nilai X, maka kamu bisa memperkirakan nilai Y berdasarkan model regresi yang terbentuk.

---

## Pengantar Regresi

- Regresi digunakan untuk menganalisis dan memodelkan data numerik.
- Memanfaatkan hubungan antara dua atau lebih variabel untuk membuat prediksi atau estimasi.
- Aplikasi: prediksi, estimasi, uji hipotesis, dan pemodelan kausal.

---

## Terminologi dalam Regresi

- **Y**: Variabel Dependen / Outcome / Respon.
- **X**: Variabel Independen / Prediktor / Penjelas.

---

## Alasan Menggunakan Regresi Linear

- Misal kita ingin memodelkan Y berdasarkan X1, X2, X3.
- Data tidak cukup untuk memodelkan f(X1, X2, X3) secara bebas.
- Maka kita batasi bentuk f menjadi linear:  
  `Y = β0 + β1X1 + β2X2 + β3X3`

---

## Model Probabilistik Linear

- Hubungan Y dan X tidak deterministik, ada error acak `ε ~ N(0, σ²)`
- Model:  
  `Y = β0 + β1X + ε`
- Maka:
  - `E(Y | X=x*) = β0 + β1x*`
  - `Var(Y | X=x*) = σ²`

---

## Interpretasi Grafis

- Untuk X tertentu (misalnya tinggi), μ_Y|X adalah rata-rata Y (misalnya berat).
- Tiap titik Y menyebar secara normal di sekitar garis regresi.

---

## Contoh Kasus Linear Regression

Diberikan model:
```
y = 7.5 + 0.5x, σ = 3

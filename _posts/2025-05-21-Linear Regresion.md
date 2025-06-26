---
title: "Lecture 9 - Linear Regression"
date: 2025-06-26
categories: [Statistik, Regresi, R]
tags: ["Linear Regression", "Probabilistik", "R", "Statistik"]
---

# 📘 Lecture 9: Linear Regression

## 📑 Daftar Isi

1. [Tujuan Pembelajaran](#tujuan-pembelajaran)
2. [Pengantar Regresi](#pengantar-regresi)
3. [Terminologi dalam Regresi](#terminologi-dalam-regresi)
4. [Mengapa Regresi Linear?](#mengapa-regresi-linear)
5. [Model Probabilistik Linear](#model-probabilistik-linear)
6. [Interpretasi Grafis](#interpretasi-grafis)
7. [Contoh Model Regresi](#contoh-model-regresi)
8. [Estimasi Parameter Model](#estimasi-parameter-model)
9. [Prediksi dan Residual](#prediksi-dan-residual)
10. [Multiple Linear Regression](#multiple-linear-regression)
11. [Variabel Independen Kategorik](#variabel-independen-kategorik)
12. [Uji Hipotesis - Omnibus Test](#uji-hipotesis---omnibus-test)
13. [Formulasi ANOVA untuk Omnibus Test](#formulasi-anova-untuk-omnibus-test)
14. [F-Test untuk Subset Variabel](#f-test-untuk-subset-variabel)
15. [Uji Koefisien Individual](#uji-koefisien-individual)
16. [Pemeriksaan Asumsi Model](#pemeriksaan-asumsi-model)
17. [Fixed vs Random Effects](#fixed-vs-random-effects)

---

## 🎯 Tujuan Pembelajaran

- Memahami konsep regresi linear dari perspektif probabilistik.
- Melakukan estimasi parameter dan uji hipotesis pada model linear.
- Mengimplementasikan regresi linear menggunakan R.

---

## 📊 Pengantar Regresi

- Digunakan untuk memodelkan dan menganalisis data numerik.
- Memanfaatkan hubungan antara dua atau lebih variabel.
- Aplikasi: prediksi, estimasi, pengujian hipotesis, dan pemodelan kausal.

---

## 🧠 Terminologi dalam Regresi

- **Y**: Variabel dependen / outcome / respon.
- **X**: Variabel independen / prediktor / penjelas.

---

## ❓ Mengapa Regresi Linear?

- Misal kita ingin memodelkan Y berdasarkan X1, X2, X3:  
  `Y = f(X1, X2, X3)`  
- Karena keterbatasan data, f biasanya diaproksimasi menjadi bentuk linear:  
  `Y = β₀ + β₁X₁ + β₂X₂ + β₃X₃`

---

## 📐 Model Probabilistik Linear

Model dasar:
Y = β₀ + β₁X + ε, dengan ε ~ N(0, σ²)

Implikasi:
- E(Y | X=x*) = β₀ + β₁x*
- Var(Y | X=x*) = σ²

---

## 📉 Interpretasi Grafis

- Untuk x tertentu (mis. tinggi badan), rata-rata Y (mis. berat) berada di garis regresi.
- Y menyebar secara normal di sekitar garis regresi.

---

## 🧮 Contoh Model Regresi

Model: `Y = 7.5 + 0.5x`, dengan σ = 3

- Jika x = 20, maka E(Y | x=20) = 17.5
- P(Y > 22 | x=20) = P(Z > (22 - 17.5)/3) = P(Z > 1.5) ≈ 0.067

---

## 🧾 Estimasi Parameter Model

- Menggunakan metode **least squares**:
β̂₀ = ȳ - β̂₁x̄
SSE = Σ(yi - ŷi)²
σ̂² = SSE / (n - 2)


---

## 🧩 Prediksi dan Residual

- Nilai prediksi:  
ŷᵢ = β̂₀ + β̂₁xᵢ  
- Residual:  
eᵢ = yᵢ - ŷᵢ  
- Digunakan untuk menghitung SSE dan r²:
r² = 1 - SSE/SST


---

## 🔢 Multiple Linear Regression

Model:
Y = β₀ + β₁X₁ + β₂X₂ + ... + βₙXₙ + ε

- βᵢ: efek parsial dari Xᵢ terhadap Y (dengan variabel lain konstan).

---

## 🧮 Variabel Independen Kategorik

- Representasi dengan **dummy variable**
- Jika ada 3 level (AA, AG, GG), maka butuh 2 dummy:
x₁ = 1 jika AA, 0 lain
x₂ = 1 jika AG, 0 lain


---

## 🧪 Uji Hipotesis - Omnibus Test

- Tujuan: cek apakah ada X yang signifikan
- Hipotesis:
H₀: β₁ = β₂ = ... = βk = 0
Hₐ: Minimal satu βᵢ ≠ 0

- Statistik F:
F = [R² / k] / [(1 - R²) / (n - k - 1)]


---

## 📊 Formulasi ANOVA untuk Omnibus Test

| Sumber | df     | SS                         | MS     | F       |
|--------|--------|----------------------------|--------|---------|
| Regresi| k      | SSR = Σ(ŷᵢ - ȳ)²           | SSR/k  | MSR/MSE |
| Error  | n - 2  | SSE = Σ(yᵢ - ŷᵢ)²          | SSE/n−2|         |
| Total  | n - 1  | SST = Σ(yᵢ - ȳ)²           |        |         |

---

## 🧪 F-Test untuk Subset Variabel

- Bandingkan dua model:
- Full: semua prediktor
- Reduced: subset dari prediktor
- Statistik F:
F = [(SSER - SSEF) / (k - l)] / [SSEF / (n - (k + 1))]


---

## 🧪 Uji Koefisien Individual

- Gunakan **uji t**:
H₀: β̂ᵢ = 0
t = β̂ᵢ / se(β̂ᵢ)
CI: β̂ᵢ ± tₐ/2 × se(β̂ᵢ)


---

## 🔍 Pemeriksaan Asumsi Model

- Cek:
- Outlier
- Normalitas residual
- Homoskedastisitas
- Independensi residual
- Gunakan plot:
- y vs xᵢ
- QQ-plot residual
- residual vs fitted
- residual vs xᵢ

---

## 🧭 Fixed vs Random Effects

- **Fixed Effects**: level variabel dipilih secara khusus.
- **Random Effects**: level variabel merupakan sampel acak dari populasi besar.

---


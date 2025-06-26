---
title: "Materi Uji Hipotesis Koefisien Regresi Linier Sederhana Menggunakan P-value"
date: 2025-04-16 10:00:00 +0700
categories: [derajat bebas, p-value, hipotesis, variansi dan galat]
tags: ["Statistik dan Probabilitas", "Distribusi Data", "R"]
---

# Uji Hipotesis Koefisien Regresi Linier Sederhana Menggunakan P-value  

---

## Daftar Isi
1. [Data Observasi](#1-data-observasi)  
2. [Langkah-Langkah Uji Hipotesis](#2-langkah-langkah-uji-hipotesis)  
   - [a. Hipotesis](#a-hipotesis)  
   - [b. Estimasi Model Regresi](#b-estimasi-model-regresi)  
   - [c. Galat dan Variansi Galat](#c-galat-dan-variansi-galat)  
   - [d. Standard Error dan Statistik Uji](#d-standard-error-dan-statistik-uji)  
   - [e. Derajat Bebas](#e-derajat-bebas)  
   - [f. P-value](#f-p-value)  
   - [g. Keputusan](#g-keputusan)  
3. [Kesimpulan](#3-kesimpulan)

---

## 1. Data Observasi

Variabel:  
- X = Jam Belajar  
- Y = Nilai Ujian  

| No | X | Y  |
|----|---|----|
| 1  | 1 | 50 |
| 2  | 2 | 55 |
| 3  | 3 | 53 |
| 4  | 4 | 70 |
| 5  | 5 | 68 |

---

## 2. Langkah-Langkah Uji Hipotesis

### a. Hipotesis
- **H₀** : β₁ = 0 → *tidak ada pengaruh signifikan*  
- **H₁** : β₁ ≠ 0 → *ada pengaruh signifikan*

---

### b. Estimasi Model Regresi

- Rata-rata X (X̄) = 3  
- Rata-rata Y (Ȳ) = 59.2  

Perhitungan koefisien:
- β̂₁ = Σ(Xi − X̄)(Yi − Ȳ) / Σ(Xi − X̄)² = 51 / 10 = **5.1**  
- β̂₀ = Ȳ − β̂₁·X̄ = 59.2 − (5.1 × 3) = **43.9**

**Model Regresi:**  
**Ŷ = 43.9 + 5.1X**

---

### c. Galat dan Variansi Galat

Perhitungan prediksi dan galat:

| No | Xi | Yi | Ŷi   | ei    |
|----|----|----|------|-------|
| 1  | 1  | 50 | 49.0 | 1.0   |
| 2  | 2  | 55 | 54.1 | 0.9   |
| 3  | 3  | 53 | 59.2 | -6.2  |
| 4  | 4  | 70 | 64.3 | 5.7   |
| 5  | 5  | 68 | 69.4 | -1.4  |

- Jumlah kuadrat galat: Σei² = 74.70  
- Variansi galat: σ̂² = 74.70 / (5 − 2) = **24.9**

---

### d. Standard Error dan Statistik Uji

- SE(β̂₁) = √σ̂² / Σ(Xi − X̄)² = √24.9 / 10 ≈ **1.58**  
- Statistik uji: t = β̂₁ / SE(β̂₁) = 5.1 / 1.58 ≈ **3.23**

---

### e. Derajat Bebas

- df = n − 2 = 5 − 2 = **3**

---

### f. P-value

- p-value dua sisi untuk t = 3.23 dan df = 3  
- Berdasarkan distribusi t:  
  **p-value ≈ 2 × 0.0247 = 0.0494**

---

### g. Keputusan

Dengan tingkat signifikansi α = 0.05:

- p-value = 0.0494 < α  
- ⇒ **Tolak H₀**

---

## 3. Kesimpulan

Terdapat **bukti yang cukup** untuk menyimpulkan bahwa **koefisien regresi β₁ ≠ 0**.  
Artinya, **jam belajar (X)** berpengaruh **signifikan** terhadap **nilai ujian (Y)**.

---



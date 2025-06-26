---
title: "Materi Pengujian Pengantar Hipotesis"
date: 2025-04-16 10:00:00 +0700
categories: [Hipotesis, Sample, Populasi]
tags: ["Statitik dan Probabilitas", "Distribusi Data", "R"]
---

# Pengantar Pengujian Hipotesis

## Daftar Isi
- [Populasi vs Sampel](#populasi-vs-sampel)
  - [Populasi](#populasi)
  - [Sampel](#sampel)
  - [Alasan Menggunakan Sampel](#alasan-menggunakan-sampel)
- [Kapan kita dapat dikatakan menggunakan sampel atau populasi?](#kapan-kita-dapat-dikatakan-menggunakan-sampel-atau-populasi)
  - [Populasi](#populasi-1)
  - [Sampel](#sampel-1)
- [Beberapa Istilah Penting](#beberapa-istilah-penting)
- [Beberapa terms yang perlu kita ketahui](#beberapa-terms-yang-perlu-kita-ketahui)
- [Apa Itu Hipotesis?](#apa-itu-hipotesis)
- [Langkah-langkah Pengujian Hipotesis](#langkah-langkah-pengujian-hipotesis)
- [Contoh Soal](#contoh-soal)
  - [1. Tentukan Hipotesis](#1-tentukan-hipotesis)
  - [2. Ambil Data Sampel](#2-ambil-data-sampel)
  - [3. Hitung Statistik Sampel](#3-hitung-statistik-sampel)
  - [4. Hitung p-value](#4-hitung-p-value)
  - [5. Bandingkan dengan 0.05](#5-bandingkan-dengan-005)
  - [Kesimpulan](#kesimpulan)

---

## Populasi vs Sampel

### Populasi
- Kumpulan seluruh elemen yang menjadi objek kajian.
- Bisa berupa orang, objek, kejadian, atau data.

### Sampel
- Bagian dari populasi yang digunakan untuk mewakili populasi.
- Diambil secara acak atau berdasarkan kriteria tertentu.

### Alasan Menggunakan Sampel
- Mengamati seluruh populasi membutuhkan waktu, biaya, dan tenaga besar.
- Sampel memungkinkan analisis yang efisien dan cukup akurat.

## Kapan kita dapat dikatakan menggunakan sampel atau populasi?

### Populasi
- Jika kita mengambil secara keseluruhan, contoh jika saya blg kami mewawancarai seluruh mahasiswa UC Makassar.

### Sampel 
- Jika kita hanya mengambil perwakilan dari populasi, misal saya mewawancarai 50 orang mahasiswa UC Makassar.

## Beberapa Istilah Penting

- **Statistik Inferensial**: Statistik yang digunakan untuk membuat kesimpulan tentang populasi berdasarkan data sampel.
- **Central Limit Theorem**: Teorema yang menyatakan distribusi rata-rata sampel akan mendekati distribusi normal, meskipun populasi tidak normal, jika ukuran sampel cukup besar.
- **Uji Hipotesis**: Cara menguji klaim atau dugaan tentang populasi berdasarkan data sampel.

## Beberapa terms yang perlu kita ketahui

| Aspek             | Populasi                    | Sampel                    |
|-------------------|-----------------------------|---------------------------|
| Ukuran            | Seluruh elemen              | Sebagian elemen           |
| Nilai rata-rata   | Parameter (μ)               | Statistik (x̄)             |
| Simpangan baku    | Simpangan baku populasi (σ) | Simpangan baku sampel (s) |
| Sumber Data       | Keseluruhan data            | Diambil dari populasi     |

## Apa Itu Hipotesis?

- **Hipotesis Nol (H₀)**: Dugaan awal, menyatakan "tidak ada perbedaan" atau "tidak ada pengaruh".  
  - Contoh: μ = 75
- **Hipotesis Alternatif (H₁)**: Dugaan tandingan, menyatakan "ada perbedaan" atau "ada pengaruh".  
  - Contoh: μ ≠ 75

## Langkah-langkah Pengujian Hipotesis

1. Tentukan H₀ dan H₁  
2. Ambil data sampel  
3. Hitung statistik uji (contoh: t-statistik)  
4. Hitung p-value  
5. Bandingkan dengan tingkat signifikansi (α), biasanya 0.05  
6. Ambil kesimpulan

## Contoh Soal

### Studi Kasus: Menguji Klaim Rata-rata Nilai = 75
Seorang dosen mengklaim bahwa rata-rata nilai ujian mahasiswa adalah 75. Kita ingin menguji klaim ini berdasarkan sampel acak 10 mahasiswa.

### 1. Tentukan Hipotesis
- H₀: μ = 75 (klaim dosen)  
- H₁: μ ≠ 75

### 2. Ambil Data Sampel
- 10 mahasiswa diambil secara acak dari 60 mahasiswa  
- Contoh data:  
  `[67.9, 84.6, 70.8, 76.2, 65.2, 77.6, 74.7, 73.2, 76.3, 70.2]`

### 3. Hitung Statistik Sampel
- Rata-rata (x̄): 74.04  
- Simpangan baku (s): 8.24  
- Jumlah sampel (n): 10

### 4. Hitung p-value
- Nilai t = -0.37, df = 9  
- p-value ≈ 0.72  
- Cara menghitung bisa melalui kalkulator statistik atau Excel:  
  `=T.DIST.2T(ABS(t), df)`

### 5. Bandingkan dengan 0.05
- Karena p-value > 0.05 → Gagal menolak H₀

## Kesimpulan
Berdasarkan data sampel, tidak cukup bukti untuk menolak klaim bahwa rata-rata nilai ujian = 75.  
Rata-rata 74.04 masih wajar jika klaim 75 itu benar.

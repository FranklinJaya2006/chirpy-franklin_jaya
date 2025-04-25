---
title: "Week 1 Statistik Deskriptif"
date: 2025-02-27 10:00:00 +0700
categories: [Mean, Median, Mode, Standar Deviasi, Statistik Deskriptif, Kuartil]
tags: ["Statitik dan Probabilitas", "Statistik", "R"]
---

#### Statistik Deskriptif adalah cabang dari statistik yang berfungsi untuk mengorganisir sekumpulan data sehingga data yang kita dapatkan dapat lebih mudah dipahami, seringkali statistik deskriptif membantu dalam bidang bidang data science dan machine learning, serta statistik deskriptif dapat menjadi acuan dalam membantu penelitian mengamnil keputusan berbasis data.

### Pada statistika deskriptif terdapat 2 pengukuran utama yang biasa digunakan untuk menganalisa data, yang pertama ada Ukuran pemusatan atau *Measures of Central Tendency*, ini adalah jenis ukuran yang digunakan untuk mengetahui nilai yang mewakili atau menjadi pusat dari sekumpulan data.

## Jenis jenis ukuran pemusatan Statistik Deskriptif: 
1. **Mean:**
> Hasil rata-rata dari sekumpulan data. Kita dapat menghitung mean dengan cara menjumlahkan seluruh data yang ada, lalu membaginya dengan jumlah data tersebut.

<img src="/assets/Mean.png" alt="Mean">

2. **Median:**
> Median adalah nilai tengah dari sekumpulan data yang telah diurutkan dari yang terkecil ke terbesar. Jika jumlah data ganjil, median adalah nilai tengah. Jika jumlah data genap, median adalah rata-rata dari dua nilai tengah.

<img src="/assets/Median.png" alt="">

3. **Modus:**
> Jumlah data yang paling sering muncul. Untuk mengetahui mana yang menjadi modus dari sejumlah data, kita dapat menghitung frekuensi kemunculan setiap nilai, lalu mengambil nilai yang muncul paling banyak.

<img src="/assets/Mode.png" alt=""/>

### Selain itu, pada statistika deskriptif terdapat ukuran penyebaran yang disebut *Measures of Dispersion*. Ini adalah cara untuk mengukur seberapa besar variasi atau sebaran data dalam suatu kumpulan data. Ini berfungsi untuk membantu kita memahami apakah data yang kita kumpulkan cenderung berkumpul di sekitar nilai tertentu (misalnya rata-rata) atau tersebar jauh dari nilai tersebut.

## Jenis jenis ukuran penyebaran Statistik Deskriptif: 
1. **Variansi:**
> Cara untuk menggambarkan bagaimana sebuah data dapat menyebar jauh dari hasil mean.

    Variansi terbagi atas 2 jenis, yaitu:
    - **Variansi Populasi (σ):**

    Berikut ini rumus menghitung variansi populasi:
    <img src="/assets/populasi.png"/>

    **Keterangan:**
    - \( x_i \): Nilai data ke-i  
    - \( μ \): Rata-rata populasi  
    - \( ∑ \): Simbol penjumlahan (menjumlahkan semua nilai dari i=1 sampai N)
    - \( N \): Jumlah total data dalam populasi  
    - \(Variansi Populasi (σ²)\): menggunakan pembagi N, karena memperhitungkan seluruh data

    - **Variansi Sampel (s):**  

    Berikut ini rumus menghitung variansi sampel:
    <img src="/assets/sample.png"/>

    **Keterangan:**
    - \( x_i \): Nilai data ke-i  
    - \( x̄ \): Rata-rata sampel
     - \( ∑ \): Simbol penjumlahan (menjumlahkan semua nilai dari i=1 sampai N)
    - \( n \): Jumlah total data dalam sampel  
    - \(Variansi Sampel (s²)\) menggunakan pembagi n − 1, agar hasilnya tidak bias 

2. **Standar deviasi:**
> Cara untuk menggambarkan seberapa besar sebaran atau variasi data terhadap nilai rata-ratanya (mean).

    Standar Deviasi terbagi atas 2 jenis, yaitu:
    - **Standar Deviasi Populasi (σ):**

    Berikut ini rumus menghitung standar deviasi populasi:
    <img src="/assets/stdevp.png"/>

    **Keterangan:**
    - \( x_i \): Nilai data ke-i  
    - \( μ \): Rata-rata populasi  
    - \( ∑ \): Simbol penjumlahan (menjumlahkan semua nilai dari i=1 sampai N)
    - \( N \): Jumlah total data dalam populasi  
    - \(Variansi Populasi (σ²)\): menggunakan pembagi N, karena memperhitungkan seluruh data

    - **Standar Deviasi Sampel (s):**  

    Berikut ini rumus menghitung standar deviasi sampel:
    <img src="/assets/stdevs.png"/>

    **Keterangan:**
    - \( x_i \): Nilai data ke-i  
    - \( x̄ \): Rata-rata sampel
     - \( ∑ \): Simbol penjumlahan (menjumlahkan semua nilai dari i=1 sampai N)
    - \( n \): Jumlah total data dalam sampel  
    - \(Variansi Sampel (s²)\) menggunakan pembagi n − 1, agar hasilnya tidak bias 

## Tugas Instalasi
##### Mahasiswa diminta melakukan instalasi R untuk memudahkan proses mengerjakan tugas minggu depan

## Kesimpulan
##### Statistik deskriptif merupakan alat untuk mengorganisir data secara ringkas dan informatif. Dengan menggunakan ukuran pemusatan seperti mean, median, dan modus, kita dapat mengetahui nilai yang mewakili kumpulan data. Sementara itu, dengan ukuran penyebaran seperti variansi dan standar deviasi, kita dapat memahami seberapa besar persebaran data terhadap nilai pusatnya.
##### Kombinasi antara ukuran pemusatan dan penyebaran membantu dalam menganalisis karakteristik data secara menyeluruh, sehingga sangat berguna dalam pengambilan keputusan berbasis data di berbagai bidang seperti data science dan machine learning, dan masih banyak lago.
# Latihan Studi Kasus: Prediksi Probabilitas Banjir Menggunakan Algoritma Regresi

### Platform : Dicoding

### Kelas : Belajar Machine Learning untuk Pemula

### Modul : Supervised Learning - Regresi

### Dataset : [Kaggle-Flood Prediction Dataset](https://www.kaggle.com/competitions/playground-series-s4e5/data)

## Data Loading

Langkah pertama yang perlu dilakukan adalah memuat data. Penting untuk mengimpor library pandas agar bisa membaca file data. Dapat dilihat pada output kode di bawah bahwa data yang dimiliki memiliki 1.117.957 baris dengan 22 kolom.

![1](https://github.com/user-attachments/assets/f342795a-5753-4398-9867-c75f1014ce13)

## Data Cleaning dan Transformation

Langkah kedua adalah melihat informasi dasar tentang dataset, seperti jumlah baris, kolom, tipe data, dan jumlah nilai yang hilang. Pertama-tama, periksa tipe data dari masing-masing fitur yang ada di dataset. Tujuan dari pemeriksaan tipe data ini adalah untuk memastikan seluruh tipe data yang ada sudah sesuai dan tidak ada kekeliruan (contoh: data numerik terdeteksi str (string)).

![2](https://github.com/user-attachments/assets/45aed034-869e-4d9e-9248-bc18834995cf)

Selanjutnya, perlu dilakukan analisis statistik deskriptif dari dataset yang digunakan. Tujuan analisis statistik deskriptif dalam proses data cleaning pada machine learning adalah untuk memahami karakteristik dasar dari data yang sedang diproses. Dengan melakukan analisis statistik deskriptif, akan memastikan bahwa data yang digunakan untuk melatih model machine learning adalah data yang representatif, berkualitas tinggi, dan bebas dari masalah yang dapat memengaruhi hasil akhir.

![3](https://github.com/user-attachments/assets/47eab36b-b685-46d0-9cd6-5afa16954439)

Terakhir, perlu dilakukan pemeriksaan terhadap data yang hilang (missing value). Tujuannya untuk mencegah kesalahan ketika melakukan analisis, mencegah error pada model, dan meningkatkan performa model. Dengan melakukan pemeriksaan missing value, dapat memastikan bahwa proses analisis data dan pelatihan model machine learning berjalan dengan baik, sehingga hasil yang diperoleh lebih valid dan akurat.

![4](https://github.com/user-attachments/assets/94b02328-98ab-4802-8a41-de107ff17c60)



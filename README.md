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

Tahap berikutnya, yaitu menangani outliers. Outliers merupakan salah satu blocker dalam membangun model machine learning yang optimal. Hal ini bisa disebabkan oleh berbagai hal seperti kesalahan pengisian data, error yang terjadi ketika pengumpulan data, dan lain sebagainya. Salah satu cara mengatasi outliers adalah dengan menggunakan metode IQR (Interquartile Range) adalah salah satu pendekatan yang efektif. IQR adalah rentang antara kuartil pertama (Q1) dan kuartil ketiga (Q3) dalam data. Nilai yang terletak di luar batas IQR dianggap sebagai outlier.

![5](https://github.com/user-attachments/assets/befe54cc-a13b-44b2-9584-e4bcebe08899)

Berdasarkan visualisasi data di atas, dapat disimpulkan bahwa nilai yang berada di bawah batas minimum atau di atas batas maksimum dianggap sebagai outlier. Ada dua pilihan yang biasa dilakukan untuk mengatasi permasalahan ini, yaitu dapat memilih untuk menghapus outlier atau Menggantinya dengan nilai yang lebih moderat (seperti batas terdekat), atau menerapkan transformasi.

Ketika melakukan analisis deskriptif di awal ada beberapa hal yang menarik seperti distribusi data yang berbeda, standar deviasi yang masih besar, hingga rentang data yang berbeda-beda. Untuk mengatasi permasalahan tersebut, akan dilakukan standardisasi pada data agar dapat mengoptimalkan proses pelatihannya. Berikut adalah perbedaan sebelum dan sesudah dilakukan standarisasi.

![6](https://github.com/user-attachments/assets/a00d40ec-226b-4951-9369-ad87cc4373f0)

![7](https://github.com/user-attachments/assets/db6264f9-d176-4b33-829b-80b09d3c0f1d)

Standardisasi penting untuk memastikan bahwa semua fitur dalam dataset memiliki skala yang sama sehingga mempermudah model untuk belajar dengan lebih baik dan memberikan hasil yang lebih akurat serta stabil.

## Exploratory dan Explanatory Data Analysis

Tahap berikutnya, yaitu exploratory dan explanatory data. Pada tahap ini dilakukan dengan menggali informasi sedalam-dalamnya sehingga dapat memperoleh insight yang bermanfaat. Dimulai dengan melihat karakteristik data.

![8](https://github.com/user-attachments/assets/7d83a054-18e9-4b87-bba8-6c09c72ec0d4)

![9](https://github.com/user-attachments/assets/44cb95f9-1f72-487b-a45b-86b9e00ffc3c)

Standardisasi yang dilakukan dapat membantu mengurangi efek bias atau skewness dari data yang tidak merata distribusinya. Dengan menempatkan fitur-fitur dalam skala yang sama, model machine learning lebih mudah untuk menemukan pola yang relevan seperti gambar di atas. Selain itu, ketika variabel-variabel berada pada skala yang berbeda secara signifikan, model machine learning mungkin menjadi tidak stabil dan memberikan hasil yang buruk. Standardisasi mengurangi risiko ini dengan membuat semua variabel berada dalam rentang yang konsisten.

## Data Splitting

Data splitting adalah langkah penting dalam workflow machine learning untuk memastikan bahwa model yang dibangun dapat digeneralisasikan dengan baik pada data yang belum pernah dilihat. Ini dapat menghindari bias evaluasi dan mengoptimalkan model dengan benar, dan memberikan estimasi kinerja yang lebih akurat. 

![10](https://github.com/user-attachments/assets/9bf8fe02-d16e-4564-9cbb-7943bf7d8233)

Dari gambar diatas bisa dilihat bahwa dari jumlah data yang digunakan dapat dibagi menjadi dua subset yang berbeda dengan proporsi yang sudah ditentukan. Pada kasus ini akan menggunakan 676.708 data latih dan 169.178 data testing. Dengan begitu data splitting memungkinkan untuk mengevaluasi kinerja model secara objektif. Dengan memisahkan data pelatihan dan pengujian, bisa dilihat seberapa baik model bekerja pada data yang belum pernah dilihat yang menyimulasikan kondisi dunia nyata. Ini membantu menghindari overfitting sehingga model dapat bekerja dengan sangat baik pada data pelatihan tetapi buruk pada data baru. 

Selain itu, dengan membagi data menjadi bagian-bagian yang lebih kecil seperti set pelatihan dan set validasi memungkinkan untuk menyetel hyperparameter model. Set validasi membantu dalam mengoptimalkan model tanpa memengaruhi data pengujian, yang sebaiknya hanya digunakan sekali untuk evaluasi akhir.


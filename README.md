# Klasifikasi Tingkat Risiko Penyakit Jantung menggunakan Algoritma Decision Tree C4.5 dan K-Nearest Neighbor Berdasarkan Data Rekam Medis

Proyek *data mining* ini bertujuan untuk melakukan klasifikasi tingkat risiko penyakit jantung pada pasien menggunakan pendekatan *supervised learning*. Proyek ini membandingkan dua algoritma dengan karakteristik berbeda: **Decision Tree C4.5** (berbasis pohon keputusan/informasi) dan **K-Nearest Neighbor** (berbasis metrik jarak), dengan fokus utama pada performa akurasi serta tingkat interpretabilitas model dalam domain klinis.

## 👥 Kontributor
* **Pancar Wahyu Setiabi** (pancar.setiabi@mhs.unsoed.ac.id)
* **Satria Megantara Wildan Irchamy** (satria.irchamy@mhs.unsoed.ac.id)

---

## 📌 Fitur Utama Proyek
* **Eksplorasi Data (EDA):** Visualisasi otomatis untuk sebaran frekuensi kolom, matriks korelasi fitur medis menggunakan *heatmap* Seaborn, serta *scatter plot matrix*.
* **Pra-pemrosesan Data:** Penanganan data duplikat, pembagian data (*stratified split*) rasio 70:30, serta standardisasi fitur numerik menggunakan *Z-Score Standardization*.
* **Komparasi Algoritma:** Implementasi terkalibrasi untuk Decision Tree C4.5 (`criterion='entropy'`) dan KNN ($K=5$, `metric='euclidean'`).
* **Evaluasi Komprehensif:** Menyajikan visualisasi matriks perbandingan akurasi akhir dalam bentuk grafik batang interaktif.

---

## 📊 Dataset Informasii
Dataset yang digunakan dalam penelitian ini adalah **Heart Disease Dataset** yang bersumber dari UCI Machine Learning Repository.
* **Jumlah Sampel:** 303 rekam medis pasien (setelah pembersihan duplikasi).
* **Fitur Medis (13 Atribut):** Usia (`age`), Jenis Kelamin (`sex`), Tipe Nyeri Dada (`cp`), Tekanan Darah (`trestbps`), Kolesterol (`chol`), Gula Darah (`fbs`), ECG (`restecg`), Detak Jantung Maksimum (`thalach`), Angina (`exang`), Oldpeak (`oldpeak`), Slope (`slope`), CA (`ca`), dan Thal (`thal`).
* **Target Variabel:** Status indikasi penyakit jantung (`target`: 0 = Sehat, 1 = Sakit).

---

## 🛠️ Struktur Direktori Repositori
```text
├── datasets/
│   └── heart_new.csv                 # Dataset rekam medis klinis (303 sampel)
├── notebooks/
│   └── heart_disease_mining.ipynb    # Jupyter Notebook utama (Code & Dokumentasi)
├── reports/
│   └── Paper_Data_Mining.docx        # Naskah publikasi ilmiah / Laporan akhir
└── README.md                         # Dokumentasi utama repositori

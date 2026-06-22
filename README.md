# Klasifikasi Tingkat Risiko Penyakit Jantung menggunakan Algoritma Decision Tree C4.5 dan K-Nearest Neighbor Berdasarkan Data Rekam Medis

Proyek *data mining* ini bertujuan untuk melakukan klasifikasi tingkat risiko penyakit jantung pada pasien menggunakan pendekatan *supervised learning*. Eksperimen ini melakukan studi komparatif terkalibrasi antara dua algoritma dengan arsitektur berbeda: **Decision Tree C4.5** (berbasis teori informasi) dan **K-Nearest Neighbor (KNN)** (berbasis metrik jarak). Proyek ini berfokus pada optimasi *hyperparameter*, stabilitas pengujian melalui validasi silang, serta tingkat interpretabilitas model di dalam domain informatika medis.

## 👥 Kontributor
* **Pancar Wahyu Setiabi** (pancar.setiabi@mhs.unsoed.ac.id)
* **Satria Megantara Wildan Irchamy** (satria.irchamy@mhs.unsoed.ac.id)

*Informatics Department, Universitas Jenderal Soedirman, Indonesia*

---

## 📌 Fitur Utama Proyek
* **Eksplorasi Data (EDA) Modern:** Visualisasi sebaran frekuensi kolom rekam medis, pembuatan matriks korelasi inter-fitur menggunakan *heatmap* Seaborn, serta pemetaan sebaran data pasien via *scatter plot matrix*.
* **Pra-pemrosesan Data Klinis:** Pembagian data terstratifikasi (*Stratified Random Sampling*) dengan rasio 70:30 untuk menjaga keseimbangan distribusi kelas, serta standardisasi fitur numerik menggunakan **Z-Score Normalization (StandardScaler)**.
* **Optimasi Hyperparameter (Grid Search):** Pencarian parameter terbaik secara otomatis menggunakan `GridSearchCV` pada data latih:
  * **C4.5:** Batasan kedalaman pohon (`max_depth`) dan batas minimal pembagian sampel (`min_samples_split`).
  * **KNN:** Analisis sensitivitas rentang nilai tetangga terdekat $K = \{3, 5, 7, 9, 11\}$ dengan metrik jarak *Euclidean*.
* **Validasi Silang (5-Fold Cross-Validation):** Evaluasi performa model di setiap lipatan (*fold*) data latih untuk mengukur kestabilan variansi model melalui nilai Standar Deviasi (Std).
* **Evaluasi Multi-Metrik:** Pengujian akhir model menggunakan parameter diagnostik lengkap meliputi *Accuracy, Precision, Recall (Sensitivity), Specificity*, dan *F1-Score*.

---

## 📊 Informasi Dataset
Dataset yang digunakan adalah **Heart Disease Dataset** asli dari UCI Machine Learning Repository (dikemas dalam berkas `heart.csv`).
* **Jumlah Sampel:** 303 rekam medis pasien (Kondisi kelas seimbang: 160 sehat, 143 terindikasi sakit).
* **Fitur Medis (13 Atribut):** Usia (`age`), Jenis Kelamin (`sex`), Tipe Nyeri Dada (`cp`), Tekanan Darah (`trestbps`), Kolesterol (`chol`), Gula Darah (`fbs`), ECG (`restecg`), Detak Jantung Maksimum (`thalach`), Angina (`exang`), Oldpeak (`oldpeak`), Slope (`slope`), CA (`ca`), dan Thal (`thal`).
* **Target Variabel:** Status indikasi penyakit jantung (`target`: 0 = Absent/Sehat, 1 = Present/Sakit).

---

## 🛠️ Struktur Direktori Repositori
```text
├── datasets/
│   └── heart.csv                 # Dataset rekam medis klinis asli (303 sampel)
├── notebooks/
│   └── c45_vs_knn_heart.ipynb        # Jupyter Notebook utama (Code, Grid Search & CV)
├── reports/
│   └── Jurnal_Decision Tree_KNN.docx # Naskah publikasi ilmiah / Laporan akhir formal
└── README.md                         # Dokumentasi utama repositori

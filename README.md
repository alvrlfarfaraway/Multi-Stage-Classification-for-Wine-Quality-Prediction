# Multi-Stage-Classification-for-Wine-Quality-Prediction

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Framework](https://img.shields.io/badge/Framework-Scikit--Learn%20%7C%20XGBoost-green.svg)
![Task](https://img.shields.io/badge/Task-Multiclass%20Classification-red.svg)

## 📌 Project Overview
Proyek ini mengimplementasikan alur kerja *machine learning* tingkat lanjut untuk mengklasifikasikan kualitas anggur berdasarkan fitur fisikokimia. Dengan menggabungkan teknik **Power Transformation** untuk normalisasi distribusi, **SMOTE** untuk penanganan ketidakseimbangan kelas, dan model **Ensemble (Voting Classifier)**, sistem ini dirancang untuk memberikan prediksi yang stabil dan akurat sesuai standar kompetisi data sains.

## 🛠️ Machine Learning Pipeline

### 1. Load Data & Initial EDA
Tahap awal melibatkan pemuatan dataset dan prosedur *Exploratory Data Analysis* (EDA) diagnostik. Fokus utama adalah identifikasi integritas data melalui pemeriksaan *missing values*, analisis statistik kemiringan distribusi (*skewness*), dan pemetaan interaksi antar fitur menggunakan matriks korelasi.

### 2. Integrated Data Preprocessing & Feature Engineering
Tahap ini merupakan fase krusial untuk mentransformasi data mentah menjadi representasi optimal. Alur kerja mencakup:
* **Manajemen Outlier:** Menggunakan metode *IQR Clipping* untuk memitigasi distorsi dari nilai ekstrem.
* **Data Splitting (The Golden Rule):** Isolasi data uji untuk mencegah kebocoran informasi (*data leakage*).
* **Normalisasi & Power Transformation:** Penerapan *Yeo-Johnson* dan *Standard Scaling* untuk menyelaraskan rentang variabel.
* **Handling Class Imbalance:** Implementasi *SMOTE* secara eksklusif pada set pelatihan untuk menciptakan *decision boundary* yang representatif.

### 3. Hybrid Ensemble Modeling
Arsitektur prediktif menggunakan pendekatan *Hybrid Ensemble* (Voting Classifier) yang mengintegrasikan *Random Forest* dan *XGBoost*. Evaluasi dilakukan menggunakan *Confusion Matrix* dan *Classification Report* untuk mengukur akurasi, presisi, dan *recall* secara komprehensif.

### 4. Stability & Feature Importance Analysis
Validasi reliabilitas model dilakukan melalui mekanisme *5-Fold Cross-Validation*. Selain itu, dilakukan ekstraksi skor *Feature Importance* untuk memberikan transparansi terhadap variabel kimiawi yang paling dominan dalam menentukan kualitas anggur.

### 5. Final Prediction & Serialization
Fase akhir melibatkan inferensi model pada data pengujian final. Hasil prediksi diserialisasi ke dalam format CSV sesuai spesifikasi teknis (kolom `Id` dan `quality`).

## 📁 Repository Structure
* `wine quality prediction.ipynb`: Notebook utama berisi seluruh alur analisis dan pemodelan.
* `data_training.csv`: Dataset untuk melatih model.
* `data_testing.csv`: Dataset untuk pengujian final.
* `hasil_prediksi_final.csv`: Hasil prediksi akhir.

---
**Author: Alverrell Gustivierda Zidna Fann**

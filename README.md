# Kelompok_3_Tugas03_Classification

# Analisis Dataset Diabetes Prediction Menggunakan Algoritma Supervised Learning

## Kelompok 3
**Anggota Kelompok:**
- Meutia Aini (2208107010005)
- Akhsania Maisa Rahmah (2208107010017)
- Fadli Ahmad Yazid (2208107010032)
- Muhammad Mahathir (2208107010056)
- Muhammad Aufa Zaikra (2208107010070)

## Deskripsi
Proyek ini berisi implementasi dan analisis berbagai algoritma supervised learning untuk memprediksi diabetes berdasarkan faktor kesehatan dan demografis. Melalui notebook ini, Anda dapat mempelajari proses lengkap data science dari eksplorasi data awal hingga evaluasi model machine learning.

## Dataset
Dataset diabetes prediction yang digunakan tersedia dalam repository ini (`diabetes_prediction_dataset.csv`). Dataset ini berisi data dari 100.000 pasien dengan berbagai karakteristik:
- Total data: 100.000 records (96.146 setelah penghapusan duplikat)
- Distribusi kelas: 91.2% tidak diabetes, 8.8% diabetes (imbalanced)
- Jumlah fitur: 8 (tidak termasuk target)
- Target: Status diabetes (0: Tidak diabetes, 1: Diabetes)

### Fitur-fitur dalam Dataset:
- **gender**: Jenis kelamin (Male, Female, Other)
- **age**: Usia dalam tahun
- **hypertension**: 0 = tidak hipertensi, 1 = hipertensi
- **heart_disease**: 0 = tidak ada penyakit jantung, 1 = ada penyakit jantung
- **smoking_history**: Riwayat merokok (never, former, current, etc.)
- **bmi**: Body Mass Index
- **HbA1c_level**: Kadar HbA1c dalam darah
- **blood_glucose_level**: Kadar glukosa darah

## Metodologi
Proyek ini menggunakan pendekatan data science end-to-end:

1. **Data Understanding**: Eksplorasi data untuk memahami karakteristik dan distribusi
2. **Data Preprocessing**:
   - Penanganan missing values
   - Penghapusan duplikat
   - Deteksi dan penanganan outlier
   - Encoding fitur kategorikal
   - Normalisasi fitur numerik
   - Penanganan ketidakseimbangan kelas (SMOTE)
3. **Model Building**: Implementasi beberapa algoritma supervised learning:
   - Logistic Regression
   - K-Nearest Neighbors
   - Naïve Bayes
   - Decision Tree
4. **Model Evaluation**: Evaluasi performa model menggunakan:
   - Accuracy, Precision, Recall, F1-Score
   - Confusion Matrix
   - ROC Curve dan AUC
   - Cross-Validation
5. **Hyperparameter Tuning**: Optimasi model terbaik menggunakan Grid Search

## Hasil Utama

### Performa Model
| Model                | Accuracy | Precision | Recall  | F1 Score | AUC     |
|----------------------|----------|-----------|---------|----------|---------|
| Logistic Regression  | 0.9581   | 0.8584    | 0.6291  | 0.7261   | 0.9591  |
| K-Nearest Neighbor   | 0.9602*  | 0.9314    | 0.5920  | 0.7239   | 0.9007  |
| Naïve Bayes          | 0.9049   | 0.4762    | 0.7795  | 0.5912   | 0.9373  |
| Decision Tree        | 0.9497   | 0.7051    | 0.7388  | 0.7216   | 0.8551  |

*Setelah tuning hyperparameter

### Fitur Penting
- Kadar HbA1c dalam darah
- Kadar glukosa darah
- Usia
- BMI

### Hyperparameter Optimal untuk K-Nearest Neighbor:
- metric: 'manhattan'
- n_neighbors: 9
- weights: 'uniform'

## Requirements
Untuk menjalankan notebook ini, Anda memerlukan library Python berikut:

```python
# Instalasi library yang diperlukan
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
```

Library utama yang digunakan dalam proyek ini:
- **pandas & numpy**: Untuk manipulasi dan analisis data
- **matplotlib & seaborn**: Untuk visualisasi data
- **scikit-learn**: Untuk implementasi algoritma machine learning dan evaluasi model
- **imbalanced-learn**: Untuk menangani ketidakseimbangan kelas dengan SMOTE

## Struktur Proyek
```
/
├── Notebook_Tugas03.ipynb             # Notebook utama dengan analisis lengkap
├── diabetes_prediction_dataset.csv    # Dataset diabetes
└── README.md                          # Dokumentasi proyek
```

## Kelompok XYZ
**Anggota Kelompok:**
1. Nama Mahasiswa 1 (NPM)
2. Nama Mahasiswa 2 (NPM)
3. Nama Mahasiswa 3 (NPM)
4. Nama Mahasiswa 4 (NPM)

## Cara Menggunakan

### Opsi 1: Menggunakan GitHub
1. Clone repositori ini ke komputer lokal Anda:
   ```
   git clone https://github.com/FadliAhmadYazid/Kelompok_3_Tugas03_Classification.git
   ```
2. Pastikan semua requirements telah diinstal (lihat bagian Requirements di atas)
3. Buka Jupyter Notebook:
   ```
   jupyter notebook
   ```
4. Buka file `Notebook_Tugas03.ipynb`
5. Jalankan sel kode secara berurutan dari atas ke bawah untuk mereproduksi analisis

### Opsi 2: Menggunakan Google Colab
1. Download repositori ini atau fork ke akun GitHub Anda
2. Upload file `Notebook_Tugas03.ipynb` ke Google Colab
3. Upload juga file dataset `diabetes_prediction_dataset.csv` ke direktori konten di Google Colab
4. Pastikan path ke dataset sudah benar di notebook
5. Jalankan sel-sel kode secara berurutan

### Urutan Eksekusi yang Direkomendasikan:
1. Import Library: Jalankan sel-sel untuk mengimpor semua library yang diperlukan
2. Load Dataset: Baca dan tampilkan data awal
3. Pemahaman Dataset: Eksplorasi awal dan visualisasi data
4. Pra-pemrosesan: Bersihkan data, tangani missing values dan outlier, lakukan encoding
5. Implementasi Model: Buat dan latih model machine learning
6. Evaluasi Model: Analisis performa model dan bandingkan hasilnya
7. Tuning Hyperparameter: Optimalkan model terbaik
8. Analisis Hasil: Interpretasi temuan dan kesimpulan

Notebook ini berisi penjelasan detail untuk setiap langkah sehingga mudah diikuti dan dimodifikasi sesuai kebutuhan.

# 🧠 Pengenalan Wajah dengan Ekstraksi LDA dan Klasifikasi K-Nearest Neighbor

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-0082C9?style=for-the-badge&logo=python&logoColor=white)

---

## 📘 Deskripsi Singkat  
Penelitian ini mengembangkan **sistem pengenalan wajah berbasis citra digital** menggunakan kombinasi metode:
- **PCA (Principal Component Analysis)**  
- **LDA (Linear Discriminant Analysis)**  
- **KNN (K-Nearest Neighbor)**  

Metode ini digunakan untuk:
1. Meningkatkan akurasi dalam identifikasi wajah.
2. Membedakan antara wajah dan non-wajah.
3. Mengoptimalkan waktu komputasi dalam proses klasifikasi.

---

## 🎯 Tujuan
- Mengimplementasikan metode ekstraksi fitur **PCA** dan **LDA** untuk pengenalan wajah.  
- Menggunakan algoritma **KNN** sebagai metode klasifikasi berbasis jarak.  
- Mengukur akurasi dan performa sistem terhadap dua jenis dataset (wajah dan non-wajah).

---

## 🧩 Metodologi Penelitian

### 🔹 Tahapan Sistem
1. **Akuisisi Citra** – Mengambil dataset wajah dan non-wajah dari Kaggle.  
2. **Preprocessing** – Mengubah citra menjadi grayscale dan melakukan normalisasi.  
3. **Ekstraksi Fitur** –  
   - **PCA** digunakan untuk reduksi dimensi.  
   - **LDA** digunakan untuk pemisahan antar kelas.  
4. **Klasifikasi** – Menggunakan algoritma **KNN** berdasarkan jarak **Euclidean Distance**.  
5. **Evaluasi** – Menghitung tingkat akurasi dengan *confusion matrix*.

---

## 🧠 Dataset
| Jenis Dataset | Sumber | Jumlah Data | Deskripsi |
|----------------|---------|--------------|------------|
| Wajah (Face) | [Kaggle – ORL Database](https://www.kaggle.com/datasets/tavarez/the-orl-database-for-training-and-testing) | 400 citra (40 kelas × 10 gambar) | Digunakan untuk pengenalan wajah |
| Wajah & Non-Wajah | [Kaggle – ATT Database of Faces](https://www.kaggle.com/datasets/kasikrit/att-database-of-faces) | 800 citra (400 wajah, 400 non-wajah) | Digunakan untuk klasifikasi wajah/non-wajah |

---

## 🧮 Arsitektur Sistem  
Diagram alur utama sistem meliputi:
Input Citra → Preprocessing → PCA → LDA → KNN → Output Klasifikasi


---

## ⚙️ Implementasi
### Bahasa & Library
- Python  
- NumPy  
- OpenCV  
- scikit-learn  
- Matplotlib  

### Langkah Utama Implementasi
1. **PCA (Eigenface)**  
   - Mengubah citra menjadi vektor  
   - Menghitung nilai eigen dan eigenvector  
   - Menghasilkan *projection matrix*  

2. **LDA (Linear Discriminant Analysis)**  
   - Menghitung matriks sebaran antar kelas (Sb) dan dalam kelas (Sw)  
   - Menentukan proyeksi terbaik antar kelas  

3. **KNN (K-Nearest Neighbor)**  
   - Menghitung jarak Euclidean antara citra uji dan citra latih  
   - Menentukan kelas berdasarkan *k* tetangga terdekat  

---

## 📊 Hasil dan Analisis
| Kasus | Metode | Akurasi |
|--------|---------|----------|
| Pengenalan wajah | PCA + LDA + KNN | **95%** |
| Deteksi wajah vs non-wajah | LDA + KNN | **77.75%** |

- Kombinasi **PCA + LDA + KNN** memberikan hasil paling optimal dalam pengenalan wajah.  
- LDA dan KNN efektif dalam klasifikasi sederhana wajah dan non-wajah dengan waktu komputasi cepat.

---

## 📈 Visualisasi
- **Confusion Matrix** digunakan untuk mengevaluasi hasil klasifikasi.  
- **Plotting hasil LDA** menunjukkan pemisahan antar kelas yang jelas.  
- **Proyeksi PCA** menampilkan distribusi fitur pada ruang berdimensi rendah.

---

## 🧩 Kesimpulan  
- Metode kombinasi **PCA + LDA + KNN** berhasil meningkatkan akurasi pengenalan wajah hingga **95%**.  
- Implementasi **LDA + KNN** mampu membedakan wajah dan non-wajah dengan akurasi **77.75%**.  
- Sistem ini memiliki potensi untuk dikembangkan lebih lanjut sebagai dasar sistem absensi atau keamanan berbasis pengenalan wajah.  

## 📅 Tahun
**2023 – Universitas Trunojoyo Madura**


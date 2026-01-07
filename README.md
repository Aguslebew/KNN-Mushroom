# KNN-Mushroom
Proyek ini bertujuan untuk mengklasifikasikan jamur apakah **dapat dimakan** atau **beracun** menggunakan algoritma **K-Nearest Neighbors (KNN)** dengan bahasa pemrograman **Python** dan library **scikit-learn**.

Dataset yang digunakan adalah *Mushroom Dataset* yang berisi karakteristik fisik jamur dalam bentuk data kategorikal.

---

##  Struktur Proyek

```
├── mushrooms.csv        # Dataset jamur
├── knn_mushroom.ipynb   # File Jupyter Notebook
└── README.md            # Dokumentasi proyek
```

---

## Dataset

- Sumber: Mushroom Dataset (UCI Machine Learning Repository)
- Jumlah fitur: 22 fitur
- Label / kelas:
  - `e` : Edible (Dapat dimakan)
  - `p` : Poisonous (Beracun)

Semua fitur bersifat **kategorikal**, sehingga perlu dilakukan **encoding** sebelum digunakan dalam model machine learning.

---

##  Library yang Digunakan

Pastikan library berikut sudah terpasang:

```bash
pip install pandas scikit-learn
```

Library utama:
- `pandas`
- `scikit-learn`

---

##  Alur Program

1. **Load Dataset**  
   Membaca file `mushrooms.csv` menggunakan pandas.

2. **Encoding Data**  
   Semua kolom (fitur dan label) dikonversi dari data kategorikal menjadi numerik menggunakan `LabelEncoder`.

3. **Pemisahan Data**  
   - Fitur (X)
   - Label (y)

4. **Split Data**  
   Dataset dibagi menjadi:
   - 80% data training
   - 20% data testing

5. **Training Model**  
   Model KNN dilatih dengan parameter:
   - `n_neighbors = 5`

6. **Evaluasi Model**  
   Menggunakan:
   - Accuracy Score
   - Confusion Matrix
   - Classification Report

7. **Prediksi Data Baru**  
   Model digunakan untuk memprediksi satu data jamur baru berdasarkan ciri-ciri yang diberikan.

---

##  Evaluasi Model

Output evaluasi yang ditampilkan:
- **Akurasi model**
- **Confusion Matrix**
- **Precision, Recall, dan F1-Score**

Hasil ini menunjukkan seberapa baik model KNN dalam membedakan jamur beracun dan yang dapat dimakan.

---

##  Contoh Prediksi Jamur Baru

Contoh data jamur baru dimasukkan secara manual dalam bentuk `DataFrame`, kemudian:
1. Di-encode menggunakan encoder yang sama
2. Diprediksi menggunakan model KNN

Output akhir:
-  *Jamur termasuk BERACUN* **atau**
-  *Jamur termasuk DAPAT DIMAKAN*

---

##  Kesimpulan

- Algoritma **KNN** sangat cocok untuk dataset ini karena pola data yang jelas
- Encoding data kategorikal sangat penting sebelum training model
- Model mampu memprediksi kelas jamur dengan akurasi tinggi

---

## 🚀 Pengembangan Selanjutnya

Beberapa pengembangan yang bisa dilakukan:
- Mencari nilai `k` terbaik dengan **cross-validation**
- Membandingkan KNN dengan algoritma lain (Decision Tree, Naive Bayes)
- Membuat aplikasi berbasis GUI atau Web

---

## 👤 Penulis

Dibuat sebagai proyek pembelajaran Machine Learning menggunakan Python dan scikit-learn.

✨ Selamat belajar dan bereksperimen dengan Machine Learning!


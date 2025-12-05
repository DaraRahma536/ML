**==============================================**   
**DETEKSI TAHUN TERBIT LAGU DENGAN MODEL MACHINE LEARNING**   
**==============================================**   

*Nama: Dara Rahma Safitri*   
*NIM: 1103220169*   
*Kelas: TK-46-02*   

Tujuan Repository
   -
   Proyek ini menggunakan model Machine Learning yang berfokus pada analisis regresi untuk memprediksi tahun rilis lagu berdasarkan berbagai fitur audio. Proyek ini mengimplementasikan beberapa model regresi, mengevaluasi performanya, dan membandingkan hasil menggunakan metriks regresi standar.
   
Penjelasan Singkat
   - 
   Proyek ini menggunakan dataset berisi sekitar 515.000 sampel dengan 90 fitur audio untuk memprediksi tahun rilis lagu (variabel target). Pada proyek ini dilakukan penyeleksian fitur berdasarkan korelasi target dan pelatihan model dengan menggunakan beberapa algoritma regresi (Linear, Ridge, Lasso, Random Forest, Gradient Boosting).
 
Deskripsi Model dan Hasil Metriks
   -
   - **Model**   
     - Linear Regression (mencari garis lurus terbaik yang memodelkan hubungan linear)
     - Ridge Regression (Linear Regression dengan penalti L2 untuk mencegah overfitting. Menggunakan nilai alpha 1.0)
     - Lasso Regression (Linear Regression dengan penalti L1 yang bisa menghasilkan koefisien tepat nol. Menggunakan nilai alpha 0.01)
     - Random Forest Regressor (menggabungkan banyak decision tree untuk prediksi lebih akurat dan stabil. Jumlah tree yang digunakan adalah 100 dengan random state 42)
     - Gradient Boosting Regressor (metode sequential dimana setiap model baru memperbaiki error model sebelumnya. jumlah n sebanyak 100 dengan random state sebesar 42)
     
   - **Hasil Matriks**   
     Matriks evaluasi yang digunakan yaitu RMSE (Root Mean Squared Error), MAE (Mean Absolute Error), dan R² (Koefisien Determinasi).
     |Model|RMSE|MAE|R²|
     |-----|----|---|--|
     |Linear Regression|10.04|7.37|0.155|
     |Ridge Regression|10.04|7.37|0.155|
     |Lasso Regression|10.04|7.37|0.155|
     |Random Forest|9.49|6.88|0.246|
     |Gradient Boosting|9.63|6.94|0.224|   

     Dari 5 model diatas, model terbaik yang didapat adalah **Random Forest Regressor** yang memiliki nilai RMSE terendah dan R² tertinggi pada data validasi, sehingga menjadikannya model dengan performa terbaik.
     
Navigasi Notebooks
   -
   - **Struktur Repository**   
     ├── UTS2_ML_Dara_NoTuning.ipynb &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Notebook utama (baseline tanpa tuning)   

   - **Navigasi Notebook**
     - Instalasi Modul (polars, gdown, sklearn, dll)   
     - Download dataset training dan testing   
     - Load Dataset   
     - Preprocessing Data (mengisi nilai null, deteksi outlier menggunakan IQR, scaling fitur, pembagian data train, validasi, dan test 70/15/15, seleksi fitur dan pemilihan fitur)   
     - Model Training dan Evaluasi (train dengan 5 model regresi dan evaluasim menggunakan RMSE, MAE, dan R²)   
     - Evaluasi Pada Data Uji (Pengujian model terbaik pada data uji serta menampilkan visualisasi hasil prediksi dan aktual)



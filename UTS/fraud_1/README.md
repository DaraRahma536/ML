**===============================================**   
**DETEKSI PENIPUAN TRANSAKSI DENGAN MODEL MACHINE LEARNING**   
**===============================================**   

*Nama: Dara Rahma Safitri*   
*NIM: 1103220169*   
*Kelas: TK-46-02*   

Tujuan Repository
   -
   Proyek ini menggunakan model Machine Learning untuk mendeteksi penipuan (fraud) dalam transaksi keuangan. Tujuan utamanya adalah membangun model klasifikasi yang dapat mengidentifikasi transaksi penipuan secara akurat menggunakan data transaksi dunia nyata.
   
Penjelasan Singkat
   - 
   Proyek ini mengimplementasikan pipeline end-to-end dengan model Machine Learning lengkap untuk mendeteksi penipuan. Proyek ini menggunakan sumber data berupa **train_transaction.csv** dan **test_transaction.csv**.Skala data yang digunakan sekitar 590.000 sampel training dengan 393 fitur dan 506.000 sampel testing. Dalam pemrosesan data menggunakan polars agar lebih ringan dan cepat, sedangkan untuk modeling menggunakan LightGBM.
 
Deskripsi Model dan Hasil Metriks
   -
   - **Model**   
     LightGBM (Light Gradient Boosting Machine) Classifier merupakan framework gradient boosting yang dirancang khusus untuk kecepatan tinggi dan efisiensi memori. Ini adalah algoritma ensemble yang menggunakan decision trees dan termasuk dalam keluarga GBM. Model ini digunakan karena proyek ini menggunakan Google Colab dengan resource CPU (tidak menggunakan GPU karena compute units habis) agar ringan dan tidak terjadi crashed. Untuk mengisi data null, numerik diisi dengan median, sedangkan str diisi dengan missing. Split data sebesar 80% training dan 20% validation.
     
   - **Hasil Matriks**   
     Primary Matriks menggunakan AUC-ROC (Area Under the Receiver Operating Characteristic Curve). Model dilatih dengan parameter default LightBGM dengan output berupa probabilitas penipuan (fraud) untuk setiap transaksi di data testing.
     
Navigasi Notebooks
   -
   - **Struktur Repository**   
     ├── UTS1_ML_Dara(NoTuning).ipynb &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Notebook utama (baseline tanpa tuning)   
├── midterm_folder/ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # Folder data (dari Google Drive)   
│   ├── train_transaction.csv &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # Data training   
│   └── test_transaction.csv &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # Data testing   
├── train_clean.csv &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; # Data training setelah preprocessing   
└── submission_done.csv &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Hasil prediksi final

   - **Navigasi Notebook**
     - Instalasi Modul (polars, lightBGM)
     - Download dataset training dan testing
     - Load Dataset   
     - Preprocessing Data (Split numerik dan karakter, mengisi null, label encoding, save clean data)
     - Train dengan LightBGM dengan parameter default
     - Prediksi data testing dan hasil disimpan di file submission_done.csv


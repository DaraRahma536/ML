**==============================================**   
**DETEKSI TAHUN TERBIT LAGU DENGAN MODEL MACHINE LEARNING**   
**==============================================**   

*Nama: Dara Rahma Safitri*   
*NIM: 1103220169*   
*Kelas: TK-46-02*   

Tujuan Repository
   -
   Proyek ini berfokus untuk melakukan eksperimen pengimplementasian pipeline Machine Learning end-to-end yang berfokus pada clustering. Tujuan utamanya adalah Membersihkan dan melakukan preprocessing data pelanggan, melakukan rekayasa fitur, menerapkan metode unsupervised learning, seperti K-Means, Hierarchical Clustering, dll.
   
Penjelasan Singkat
   - 
   Proyek ini merupakan pipeline analisis data regresi yang mencakup preprocessing dataset, seperti train-test dan standarisasi, pemodelan clustering, evaluasi dan analisis cluster. Proyek ini membantu memahami bagaimana segmentasi pelanggan dapat digunakan untuk strategi bisnis, promosi, dan pengelolaan resiko kredit. 
 
Deskripsi Model dan Hasil Metriks
   -
   - **Model**   
     - K-Means Clustering (model utama karena efisien dan cocok untuk dataset numerik)
     - Hierarchical Clustering (visualisasi struktur cluster melalui dendrogram)
     - DBSCAN (cocok untuk mendeteksi cluster dengan bentuk tidak teratur dan menangani outliers)
     - Gaussian Mixture Model (berbasis probability density function dan campuran dari beberapa distribusi Gaussian)
     
   - **Hasil Matriks**   
     Proyek ini menggunakan beberapa matriks dan metode validasi cluster, seperti Elbow Method (menentukan jumlah kluster optimal dengan melihat inertia), Silhouette Score (mengukur seberapa baik anggota cluster terpisah dan mengelompokkan dengan benar), dan Cluster Visualization (PCA atau scatter plot untuk menilai struktur cluster secara visual). Hasil evaluasi ini digunakan untuk menentukan jumlah cluster terbaik dan menafsirkan pola perilaku pelanggan.
     Cluster yang digunakan adalah sebanyak 3 buah (cluster 0, cluster 1, dan cluster 3). Cluster 0 merepresentasikan High Spender dengan Limit Tinggi, cluster 1 merepresentasikan Cash Advance Users / High Risk Borrowers, dan cluster 2 merepresentasikan Low Usage / Passive Users.
     
Navigasi Notebooks
   -
   - **Struktur Repository**   
     ├── UTS2_ML_Dara_NoTuning.ipynb &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Notebook utama (baseline tanpa tuning)
     │── cluster_distribution.png   
     │── cluster_heatmap.png   
     │── cluster_profiles_20251202_215637.csv   
     │── clustering_evaluation_20251202_215637.csv   
     │── customer_clusters_20251202_21567.csv   
     │── elbow_method.png   
     │── outliers_before.png   
     │── parallel_coordinates.png   
     │── pca_2d_clusters.png   
     │── pca_explained_variance.png   
     │── silhouette_scores.png   

   - **Navigasi Notebook**
     - install modul dan import libraries (gdown, pandas, matplotlib, seaborn, sklearn, dll)
     - Load Dataset
     - Exploratory Data Analysis (EDA) (statistik ringkas, korelasi fitur, distribusi data, dan deteksi outlier)
     - Preprocessing Data (mengisi missing values, scaling, penanganan outlier)
     - Modeling Clustering (menjalankan K-Means dan mencari jumlah cluster optimal)
     - Evaluasi Cluster (Sillhoutte analysis dan visualisasi hasil cluster)





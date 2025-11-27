# 🛒 Customer Segmentation & Product Recommendation  
### Using RFM Analysis + K-Means Clustering

Proyek ini melakukan segmentasi pelanggan berdasarkan perilaku pembelian menggunakan **RFM (Recency, Frequency, Monetary)** dan algoritma **K-Means**.  
Selain segmentasi, proyek juga menghasilkan **sistem rekomendasi produk** berdasarkan cluster pelanggan.

Repositori ini berisi seluruh proses analisis, notebook, screenshot hasil, serta dokumentasi untuk mereplikasi proyek.

---

## 🚀 Fitur Utama

✔ Data Cleaning & Pre-processing  
✔ Perhitungan Fitur **RFM**  
✔ Feature Engineering tambahan:  
   - Product Diversity  
   - Cancel Rate  
   - Seasonal Trends  
   - Geographic Features  
✔ Outlier Detection menggunakan **Isolation Forest**  
✔ PCA untuk dimensionality reduction  
✔ Clustering menggunakan **K-Means (k = 4)**  
✔ Evaluasi cluster  
✔ Visualisasi lengkap  
✔ Sistem rekomendasi produk top-3 per cluster  
✔ Dokumentasi untuk replikasi

---

## 📊 Dataset

Dataset yang digunakan berasal dari:  
**Online Retail Dataset — UCI Machine Learning Repository**

Link dataset:  
(https://www.kaggle.com/datasets/carrie1/ecommerce-data)

---

# ⚙️ Instalasi & Menjalankan Proyek

## 1️⃣ Clone Repository
```bash
git clone https://github.com/rivanapr/A25-CS262-Capstone-Project.git
cd A25-CS262-Capstone-Project
```
## 2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```
## 3️⃣ Tambahkan Dataset

#🔍 Alur Analisis
## 1. Load & Inspect Data
- Cek missing values
- Cek deskripsi data
- Cek statistik awal

## 2. Data Cleaning
- Menghapus missing values
- Menghapus transaksi Cancel
- Menghapus duplikasi
- Menghapus StockCode anomali
- Menghapus harga UnitPrice = 0
- Standardisasi Description

## 3. Feature Engineering
✦ RFM:
- Recency → Days_Since_Last_Purchase
- Frequency → Total_Transactions
- Monetary → Total_Spend
✦ Tambahan:
- Product diversity
- Average days between purchase
- Favorite shopping hour/day
- Country features
- Cancellation rate
- Seasonality & trend

## 4. Outlier Detection
Menggunakan:
- Isolation Forest
- Outlier kemudian dihapus.

## 5. Feature Scaling
Menggunakan StandardScaler pada variabel numerik.

## 6. Dimensionality Reduction
PCA dengan:
- 6 komponen optimal
- Visualisasi cumulative explained variance

## 7. Clustering
Metode Penentuan Jumlah Cluster:
- Elbow Method → 4 cluster optimal
- Silhouette Score
- Davies-Bouldin Index
- Calinski-Harabasz Index
- Final model: K-Means (k = 4)

# 📈 Hasil & Insight Segmentasi
## 📌 Cluster 0 — Loyal Customers
- Frequency tinggi
- Monetary tinggi
- Recency rendah
- Cocok untuk: loyalty program, VIP reward
## 📌 Cluster 1 — Big Spenders
- Pengeluaran besar
- Tidak selalu frekuensi tinggi
- Cocok untuk: upselling premium
## 📌 Cluster 2 — At-Risk Customers
- Recency tinggi (lama tidak transaksi)
- Cocok: win-back campaign, diskon besar

# 🛒 Sistem Rekomendasi Produk
Setiap pelanggan mendapatkan 3 rekomendasi produk berdasarkan:
- Top products di cluster pelanggan
- Produk yang belum pernah dibeli

# 📦 Requirements
```bash
pandas
numpy
scikit-learn
matplotlib
seaborn
plotly
yellowbrick
tabulate
```

# 🔄 Cara Replikasi (Singkat)
- Clone repo
- Install dependencies
- Download dataset
- Jalankan notebook
- Semua hasil akan keluar otomatis

# 👥 Kontributor
- Rivan Aprilian
- Zaimatul Ummah
- Jonathan Pratama

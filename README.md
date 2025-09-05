# 🛒 Market Basket Analysis  

Proyek ini melakukan analisis keranjang belanja (*Market Basket Analysis*) menggunakan algoritma **Apriori** pada dataset ritel online. Market Basket Analysis adalah teknik data mining yang menganalisis pola pembelian pelanggan untuk mengidentifikasi hubungan antara produk yang sering dibeli bersama. Analisis ini berguna untuk strategi penempatan produk, promosi bundling, dan rekomendasi produk.  

---

## 🎯 Tujuan  
- Mengidentifikasi pola asosiasi dan hubungan antara produk yang sering dibeli bersama.  
- Menghasilkan *insight* untuk strategi pemasaran, penataan produk, dan rekomendasi pelanggan.  
- Menjadi portfolio yang menunjukkan kemampuan dalam menganalisis data serta menghasilkan actionable insights.  

---

## 📁 Struktur Proyek  
```
Market-Basket-Analysis/
├── Online Retail - MBA.ipynb      # Jupyter notebook dengan analisis lengkap
├── MBA (Dashboard).pbit           # Dashboard Power BI
├── Model View.jpg                 # Skema model data
├── Project Process.jpg            # Preview dashboard
├── Toolley.png                    # Ikon dalam dashboard
├── Product Association.csv        # Hasil analisis asosiasi produk
└── README.md
```
---

## 📋 Dataset  
Dataset bersumber dari Kaggle: *Retail Sales Dataset*  
Data ini merepresentasikan penjualan toko online dengan total **461.773 baris** dan **7 kolom** utama.  

- Periode Data: Januari – Desember 2010  
- Ukuran Data: 461.773 baris, 7 kolom  
- Karakteristik Data: berisi transaksi penjualan mencakup informasi pesanan, produk, jumlah, harga, dan pelanggan.  
- Struktur Kolom:  
  - Data Transaksi Penjualan → `order_id`, `order_date`  
  - Informasi Produk → `product_code`, `product_name`, `quantity`, `price`  
  - Informasi Pelanggan → `customer_id`  

---

## 📈 Metrik Analisis  
Analisis asosiasi produk dilakukan menggunakan algoritma Apriori dengan metrik utama:  

- **Support** → Seberapa sering itemset muncul dalam seluruh transaksi.  
- **Confidence** → Probabilitas item Y dibeli jika item X dibeli.  
- **Lift** → Penguatan hubungan antara item X dan Y dibandingkan acak.   

ℹ️ Karena keragaman produk yang sangat tinggi, analisis hanya menampilkan asosiasi produk dengan **support > 10%** dan **confidence ≥ 70%** untuk memastikan relevansi aturan. 

---

## 🖥️ Dashboard Preview  
Berikut adalah tampilan dashboard interaktif yang dibuat dengan Power BI.  

![Preview](https://drive.google.com/uc?export=view&id=12zUr5Ol4VAq97ux7M-cegCjPxg6hAThV) 

Dashboard interaktif ini memungkinkan pengguna untuk memantau performa keseluruhan, menganalisis kekuatan aturan asosiasi, mengidentifikasi aturan terbaik berdasarkan skor tertinggi, menelusuri detail setiap aturan, serta mendapatkan wawasan untuk strategi penempatan produk, bundling, dan promosi yang efektif.

---

## 🔧 Teknologi dan Tools  
Analisis dilakukan menggunakan Python dengan dukungan library utama:  

- Bahasa Pemrograman: `Python`  
- Analisis Data: `Pandas`, `NumPy`  
- Market Basket Analysis: `MLxtend` (Apriori algorithm, Association Rules)  
- Visualisasi Data: `Matplotlib`, `Seaborn`  
- Visualisasi Interaktif: `Power BI`   
- Lingkungan Pengembangan: `Jupyter Notebook`  

---

## 🔍 Insight Utama  
- Asosiasi Produk menunjukkan confidence yang sangat tinggi (rata-rata 80%) dan lift score (rata-rata 35.72, maksimal 67.22), mengindikasikan hubungan produk yang sangat signifikan.  
- Produk alat taman anak dan dekorasi rumah menunjukkan asosiasi terkuat, dengan aturan seperti garden fork biru → pink (confidence 85%, lift 66.7).  
- Pelanggan secara konsisten membeli set produk bertema (warna serasi, produk spesifik ruangan, atau varian produk yang sama dalam variasi berbeda).  
- Lift score yang sangat tinggi (banyak di atas 40) mengungkap kandidat sempurna untuk bundling produk dan penempatan strategis.  

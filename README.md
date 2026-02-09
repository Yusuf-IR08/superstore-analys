# 📊 Superstore Sales Analysis & Forecasting
## 📌 Project Overview
Project ini bertujuan untuk menganalisis performa penjualan dataset Superstore melalui proses Exploratory Data Analysis (EDA), visualisasi dashboard, serta forecasting penjualan menggunakan metode Holt-Winters (Triple Exponential Smoothing).
Analisis difokuskan pada:
- Tren penjualan dan profit
- Performa kategori, segmen, dan wilayah
- Efisiensi pengiriman (Lead Time)
- Prediksi penjualan di periode mendatang

## 🗂 Dataset
Dataset: Sample Superstore
Sumber: Dataset publik (sering digunakan untuk pembelajaran data analytics)
Kolom utama:
- Order Date
- Ship Date
- Sales
- Profit
- Quantity
- Category, Sub-Category
- Segment
- Region, State
- Ship Mode

## 🎯 Objectives
- Memahami pola penjualan dan profit dari waktu ke waktu
- Mengidentifikasi kategori, segmen, dan wilayah dengan performa terbaik
- Menganalisis lead time pengiriman dan hubungannya dengan profit
- Membangun model forecasting untuk memprediksi total penjualan bulanan

## 🔍 Exploratory Data Analysis (EDA)
- Tahapan EDA meliputi:
- Pengecekan struktur data dan missing values
- Analisis distribusi Sales dan Profit
- Analisis tren penjualan tahunan dan bulanan
- Analisis performa berdasarkan:
- Category & Sub-Category
- Segment
- Region & State
- Ship Mode
- Analisis Order Date vs Ship Date untuk menghitung Lead Time

EDA digunakan sebagai dasar pengambilan keputusan visualisasi dan pemilihan metode forecasting.

## 📊 Dashboard

Dashboard dibuat untuk menyajikan hasil EDA secara ringkas dan interaktif.

### Page 1 — Sales & Profit Overview
- Total Sales, Profit, Profit Ratio, Quantity
- Tren Sales & Profit (Time Series)
- Sales & Profit by Category
- Sales by Segment
- Sales by State (Geo Map)
- Product by Sales

### Page 2 — Shipping & Operational Analysis
- Average Lead Time, Max Lead Time, Quantity
- Trend Lead Time over Time
- Count by Ship Mode
- Lead Time by Ship Mode
- Lead Time by Region
- Profit by Ship Mode

Dashboard dirancang untuk menjawab pertanyaan apa yang terjadi dan mengapa hal tersebut terjadi.

## 🔮 Forecasting

Forecasting dilakukan untuk Total Sales Bulanan menggunakan metode Holt-Winters.
Alur Forecasting:
1. Agregasi data menjadi penjualan bulanan
2. Train–test split berbasis waktu
   * Train: 2014–2016
   * Test: 2017
3. Penerapan Holt-Winters (Additive Trend & Seasonality)
4. Evaluasi model menggunakan:
   * MAPE
5. Hasil Evaluasi:
   * MAPE ≈ 22%

Model mampu menangkap tren dan pola musiman, namun masih memiliki deviasi pada periode dengan fluktuasi tinggi
Model dinilai cukup layak (acceptable) sebagai baseline forecasting

## 🛠 Tools & Libraries
- Python
- Pandas
- NumPy
- Matplotlib / Seaborn
- Scikit-learn
- Statsmodels
- Looker Studio (Dashboard)

## 📌 Key Insights
- Penjualan menunjukkan tren meningkat dari tahun ke tahun dengan puncak di akhir tahun
- Kategori Technology memiliki kontribusi sales dan profit yang tinggi
- Standard Class merupakan ship mode paling sering digunakan namun memiliki lead time lebih lama
- Pengiriman lebih cepat tidak selalu menghasilkan profit lebih tinggi
- Holt-Winters mampu memodelkan pola musiman penjualan bulanan dengan cukup baik

## 🚀 Future Improvements
- Membandingkan Holt-Winters dengan SARIMA
- Forecasting per Category atau Region
- Menggunakan rolling forecast evaluation
- Menambahkan confidence interval pada hasil forecasting

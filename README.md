# Data Mining Tugas 1

Exploratory Data Analysis (EDA) pada dataset Netflix Customer Churn untuk memahami karakteristik pelanggan, pola yang berkaitan dengan churn (berhenti berlangganan), dan wawasan awal yang bisa ditindaklanjuti.

- Author: Abyan Bismar Alfayed  
- NRP: 5025221026  
- Repo: https://github.com/abyanba/data-mining-1  
- Kaggle Notebook: https://www.kaggle.com/code/abyanba/data-mining-tugas-1  
- Dataset: https://www.kaggle.com/datasets/abdulwadood11220/netflix-customer-churn-dataset

## Tujuan
- Memeriksa kualitas data (missing values, tipe data, statistik ringkas)
- Melihat distribusi target churn dan keseimbangannya
- Mengeksplorasi distribusi fitur numerik dan kategorikal
- Menganalisis hubungan fitur dengan churn (bivariat)
- Melihat segmentasi churn lintas kategori (multivariat)

## Dataset & Fitur

Fitur target:
- `churned`: 1 = pelanggan churn (berhenti), 0 = pelanggan aktif

Fitur identitas:
- `customer_id`: ID unik pelanggan

Fitur numerik:
- `age`, `monthly_fee`, `watch_hours`, `last_login_days`,
  `avg_watch_time_per_day`, `number_of_profiles`

Fitur kategorikal:
- `gender`, `subscription_type`, `region`, `device`,
  `payment_method`, `favorite_genre`

Sumber data: Kaggle — “Netflix Customer Churn Dataset”. Harap ikuti lisensi/ketentuan di halaman dataset tersebut.

## Ringkasan Alur Analisis (sesuai notebook)
1) Import paket: pandas, numpy, matplotlib, seaborn, warnings  
2) Info & statistik dataset: `head`, shape/size, `describe`, `info`, `isna`, `nunique`  
3) Distribusi target (`churned`): barplot + pie chart  
4) Distribusi fitur numerik: histogram/boxplot + heatmap korelasi  
5) Distribusi fitur kategorikal: countplot per kategori  
6) Bivariat (churn vs kategori): countplot dengan hue `churned`  
7) Bivariat (churn vs numerik): KDE/countplot per fitur + ringkasan mean/median/max/std per kelas churn  
8) Multivariat (segmentasi): faceted countplot (region/gender × kategori lain)

Catatan: Notebook menunjukkan distribusi target yang seimbang dan dataset yang bersih berdasarkan pemeriksaan awal. Detail temuan spesifik (misal faktor paling berpengaruh) bergantung interpretasi dari visual/angka dalam sel.

## Cara Menjalankan

### 1) Kaggle
- Jalankan notebook di Kaggle. Path data di notebook diset ke:
  `/kaggle/input/netflix-customer-churn-dataset/netflix_customer_churn.csv`
- Pastikan Anda menambahkan dataset yang benar ke sesi Kaggle Anda.

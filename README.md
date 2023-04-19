# **Marketing Campaign Analysis : Project Overview**
- Membangun model machine learning yang mampu memprediksi apakah seorang customer akan merespon campaign selanjutnya atau tidak.
- Dataset ini diperoleh dari [Marketing Campaign | Kaggle](https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign)
- Membersihkan data dari missing value dengan cara drop() kolom Income.
- Engineered features untuk mengoptimalkan proses pembelajaran model.
- *Handle Imbalanced Class* dengan 3 metode sampling berbeda kemudian memasangkan model untuk setiap metode sampling dengan menggunakan 7 algoritma berbeda, lalu pilih metode terbaik dan top 3 algoritma untuk selanjutnya dilakukan hyperparameter tuning.
- Validasi model dengan data test

### Problem:
PT. NolBir bergerak dibidang retail menjual berbagai produk seperti wine, buah-buahan, daging ikan, makanan manis, dan juga emas. Untuk melakukan pembelian customer dapat langsung ke store melalui website maupun catalog.
Perusahaan ini telah melakukan marketing campaign untuk meningkatkan penjualan sebanyak 5 kali. Namun tingkat respon customer terhadap campaign yang telah dilakukan terlalu rendah.

### Purpose:
Membuat marketing campaign yang tepat sasaran (response rate dan profit tinggi).

# Analysis Data
1. Distribution of Response is Imbalanced
![Distribution of Response](https://user-images.githubusercontent.com/104814864/232986117-7bd15510-cde3-41f5-8b6c-1c9c89c72d8a.png)

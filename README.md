# **Marketing Campaign Analysis : Project Overview**
- Membangun model machine learning yang mampu memprediksi apakah seorang customer akan merespon campaign selanjutnya atau tidak.
- Dataset ini diperoleh dari [Marketing Campaign | Kaggle](https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign)
- Membersihkan data dari missing value dengan cara drop() kolom Income.
- Engineered features untuk mengoptimalkan proses pembelajaran model.
- *Handle Imbalanced Class* dengan 3 metode sampling berbeda kemudian memasangkan model untuk setiap metode sampling dengan menggunakan 7 algoritma berbeda, lalu pilih metode terbaik dan top 3 algoritma untuk selanjutnya dilakukan hyperparameter tuning.
- Validasi model dengan data test

## Problem:
PT. NolBir bergerak dibidang retail menjual berbagai produk seperti wine, buah-buahan, daging ikan, makanan manis, dan juga emas. Untuk melakukan pembelian customer dapat langsung ke store melalui website maupun catalog.
Perusahaan ini telah melakukan marketing campaign untuk meningkatkan penjualan sebanyak 5 kali. Namun tingkat respon customer terhadap campaign yang telah dilakukan terlalu rendah.

## Purpose:
Membuat marketing campaign yang tepat sasaran (response rate dan profit tinggi).

# Analysis Data
1. Distribusi Response Imbalanced
![Distribution of Response](https://user-images.githubusercontent.com/104814864/232986117-7bd15510-cde3-41f5-8b6c-1c9c89c72d8a.png)
2. Kebanyakan customer yang merespon campaign berusia 38 - 53 tahun
![Amount of Customers who Responded Campaign Based On Age](https://user-images.githubusercontent.com/104814864/232989189-ca1716e4-cf25-4aea-800c-545289760e9f.png)
3. Customer yang tidak memiliki dependents cenderung merespon campaign
![Amount of Dependents](https://user-images.githubusercontent.com/104814864/232989648-2545606d-d460-481f-906b-cdc332c82170.png)
4. Customer yang baru-baru ini melakukan pembelian, kemungkinan meresponse campaign
![Distribution of Recency to Response](https://user-images.githubusercontent.com/104814864/232990053-c34884e0-0728-45c3-9461-0301d0fedcd4.png)

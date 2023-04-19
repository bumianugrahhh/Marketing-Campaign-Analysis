# **Marketing Campaign Analysis : Project Overview**
- Membangun classification model machine learning yang mampu memprediksi apakah seorang customer akan merespon campaign selanjutnya atau tidak.
- Dataset ini diperoleh dari [Marketing Campaign | Kaggle](https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign)
- Membersihkan data dari missing value dengan cara drop() kolom Income.
- Engineered features untuk mengoptimalkan proses pembelajaran model.
- *Handle Imbalanced Class* dengan 3 metode sampling berbeda kemudian memasangkan model untuk setiap metode sampling dengan menggunakan 5 algoritma berbeda, lalu pilih metode terbaik dan top 3 algoritma untuk selanjutnya dilakukan hyperparameter tuning. 
- Validasi model dengan data test.
- Model yang dipilih adalah *Random Forest*

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

# ML Modeling
Sebelum melatih model, dilakukan Split Data Train dan Data Test (test size 30%). Melatih model dengan 5 algoritma berbeda dan mengevaluasinya dengan **ROC AUC**. Alasan mengurangi False Positive dan False Negative agar campaign yang dilakukan tepat sasaran, yang mana Revenue Lossnya kecil dan Cost yang digunakan juga optimal sehingga menghasilkan Profit yang tinggi. Model dilatih dengan :
- Logistic Reggresion
- Decision Tree
- Random Forest
- XGBoost
- AdaBoost

# Model Evaluation
Model di evaluasi dengan **ROC AUC** kemudian memilih Top 3 ROC AUC tertinggi. Karena masih cenderung overfitting maka akan dilakukan hyperparameter tuning selanjutnya.
Model | Train ROC AUC | Test ROC AUC
----- | ------------- | ------------
Random Forest Classifier | 0.999968 | 0.883274
XGBOost Classifier | 0.999974 | 0.861372
AdaBoost Classifier | 0.938959 | 0.884735

Setelah dilakukan hyperparameter tuning didaptkan bahwa **Random Forest** memiliki performa model terbaik.
Model | Train ROC AUC | Test ROC AUC
----- | ------------- | ------------
Random Forest Classifier | 0.9684294270299644 | 0.8929469026548671

# Business Insight and Recommendation
1. **Recency** rendah : customer yang barumelakukan pembelian. <br>
Menargetkan campaign kepada customer yang **akhir-akhir ini melakukan pembelian**.
2. Banyak yang berasal dari kategori **usia 38-53 tahun**. <br>
**Menargetkan campaign kepada customer yang berusia sekitar 38-53 tahun** karena customer tersebut terlihat memiliki karakteristik lebih bersedia untuk menerima suatu campaign.
3. Banyak customer yang **baru beberapa kali melakukan pembelian** (number of purchases rendah), baik melalui store/ website/ catalog/ dengan diskon. <br> Menargetkan campaign kepada customer yang **baru beberapa kali melakukan pembelian** karena customer baru mungkin belum pernah menerima campaign sebelumnya, sehingga pada campaign terakhir terdapat beberapa customer baru yang tertarik untuk mencoba/menerima campaign.

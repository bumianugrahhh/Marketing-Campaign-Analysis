# **Marketing Campaign Analysis : Project Overview**
- Membangun model machine learning yang mampu memprediksi apakah seorang customer akan merespon campaign selanjutnya atau tidak.
- Dataset ini diperoleh dari https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign
- Membersihkan data dari missing value dengan cara drop() kolom Income karena hanya terdapat 24 baris missing value atau sebanyak 1.07% dari keseluruhan data.
- Engineered features untuk mengoptimalkan proses pembelajaran model.
- *Handle Imbalanced Class* dengan 3 metode berbeda dan kemudian memilih 1 metode terbaik.
- Melatih model dengan 7 algoritma berbeda kemudian pilih top 3 untuk selanjutnya dilakukan hyperparameter tuning
- Validasi model dengan data test

### Business Understanding:
PT. NolBir bergerak dibidang retail menjual berbagai produk seperti wine, buah-buahan, daging ikan, makanan manis, dan juga emas. Untuk melakukan pembelian customer dapat langsung ke store melalui website maupun catalog.
Perusahaan ini telah melakukan marketing campaign untuk meningkatkan penjualan sebanyak 5 kali. Namun tingkat respon customer terhadap campaign yang telah dilakukan terlalu rendah.


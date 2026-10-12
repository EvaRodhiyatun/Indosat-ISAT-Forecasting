# Indosat-ISAT-Forecasting
Proyek ini membangun model MLP (Multilayer Perceptron) untuk mempelajari pola historis harga penutupan saham Indosat Ooredoo Hutchison Tbk (ISAT) dan memprediksi harganya 30 hari ke depan.
## Konteks
Harga saham bersifat dinamis dan dipengaruhi banyak faktor, baik internal perusahaan maupun eksternal (kondisi ekonomi, kebijakan pemerintah, sentimen pasar). Fluktuasi yang tinggi menciptakan ketidakpastian besar bagi investor.

ISAT adalah salah satu perusahaan telekomunikasi besar di Indonesia yang sahamnya aktif diperdagangkan di Bursa Efek Indonesia. Pergerakan harganya mencerminkan kinerja perusahaan dan ekspektasi pasar. Karena itu, metode berbasis kecerdasan buatan, khususnya Jaringan Saraf Tiruan Multilayer Perceptron (MLP), dimanfaatkan untuk mempelajari pola historis harga dan menghasilkan prediksi sebagai bahan pertimbangan keputusan investasi.
## Problem Statement
Harga saham ISAT berfluktuasi sehingga sulit diprediksi dengan pendekatan konvensional. Ketidakpastian ini menyulitkan investor menentukan waktu yang tepat untuk membeli, menahan, atau menjual saham. Prediksi yang kurang akurat meningkatkan risiko kerugian dan menurunkan efektivitas strategi investasi.

Diperlukan model machine learning yang mampu mempelajari pola dan hubungan non-linier pada data deret waktu (harga penutupan dan informasi waktu) untuk memperkirakan harga ISAT pada periode mendatang.
## Tujuan
1. Membangun dan melatih model MLP Regressor dari data historis yang dinormalisasi dan disiapkan dengan metode sliding window.
2. Menyediakan prediksi harga ISAT untuk 30 hari ke depan sebagai panduan investasi jangka pendek.
3. Mengidentifikasi tren yang paling mungkin terjadi pada periode tersebut (naik, turun, atau sideways).
## Dataset
Dataset terdiri dari 1201 baris dan 2 kolom yaitu, kolom Tanggal dan kolom Terakhir (harga penutupan). Dataset yang digunakan dari periode 13 November 2020 - 13 November 2025.
## Hasil
### Evaluasi Model MLP
| Metrik | Nilai |
|---|---|
| MSE | 0,0053 |
| RMSE | 0,0727 |
| MAE | 0,0514 |
| MAPE | 2,63% |
### Prediksi 30 hari ke depan
Prediksi dilakukan secara iteratif: jendela 5 harga terakhir dipakai sebagai input, hasil prediksi ditambahkan ke jendela, lalu data tertua dibuang, dan seterusnya.

| Tanggal | Prediksi |
|---|---|
| 14 Nov 2025 | 2,137 |
| 24 Nov 2025 | 2,189 |
| 3 Des 2025 | 2,252 |
| 13 Des 2025 | 2,342 |

Harga diprediksi naik bertahap dan konsisten sepanjang 30 hari.
## Kesimpulan

- Model MLP berhasil dibangun dan mampu mempelajari pola harga ISAT periode 2020–2025.
- Performa pada data testing baik, dengan MAPE 2,63% (di bawah 10%), sehingga rata-rata kesalahan prediksi relatif kecil.
- Prediksi 30 hari ke depan menunjukkan **tren naik** dari 2,137 menjadi 2,342.
- Model dapat menjadi alat bantu keputusan investasi jangka pendek, tetapi hasilnya tetap perlu dipertimbangkan bersama analisis pasar yang lebih luas.

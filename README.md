# Analisa Performa Optimizer LSTM untuk Prediksi Iradiasi Matahari
Repository ini berisi kode, data, dan sumber daya untuk penelitian tugas akhir berjudul "Analisa Performa Optimizer Algoritma Pembelajaran Mesin dalam Prediksi Iradiasi Matahari Berdasarkan Luas Penerangan (Lux) di Atap Gedung Jakarta Selatan". Penelitian ini bertujuan untuk menganalisis dan membandingkan secara sistematis performa dari tiga optimizer populer—SGD, RMSProp, dan Adam—dalam melatih model Long Short-Term Memory (LSTM) untuk prediksi deret waktu.
## Visualisasi Hasil Utama
Grafik di bawah ini menunjukkan perbandingan antara nilai iradiasi matahari aktual dengan hasil prediksi dari empat model terbaik. Temuan kunci dari penelitian ini adalah meskipun model dengan optimizer SGD (garis oranye) memiliki metrik error kuantitatif terendah, prediksinya cenderung datar (underfitting). Sebaliknya, model dengan optimizer Adam (garis ungu) menunjukkan kemampuan kualitatif yang jauh lebih superior dalam menangkap fluktuasi dinamis data, menjadikannya model terbaik secara fungsional.
## 📂 Struktur Repository
Berikut adalah gambaran umum mengenai struktur folder dalam repository ini:
/notebooks: Berisi Notebook Jupyter (.ipynb) utama yang mencakup seluruh alur kerja penelitian, mulai dari pra-pemrosesan data, pelatihan model, hingga evaluasi.
/data: Berisi dataset yang digunakan.
/data/raw: Dataset asli hasil pengukuran lux harian.
/data/processed: Dataset yang telah dibersihkan, dikonversi, dan dinormalisasi, siap untuk digunakan dalam pelatihan model.
/results: Berisi semua output yang dihasilkan dari notebook.
/results/plots: Semua gambar dan grafik visualisasi yang dihasilkan.
/results/models: File model LSTM yang telah dilatih (.h5).
/docs: Berisi dokumen pendukung seperti laporan tugas akhir, makalah ilmiah, dan presentasi seminar dalam format PDF.
## 📊 Sumber Data
Dataset yang digunakan adalah data deret waktu univariat hasil pengukuran intensitas cahaya (lux) harian.
Lokasi: Atap sebuah gedung di Jakarta Selatan.
Periode: 1 Maret 2023 – 29 Februari 2024 (1 tahun).
Frekuensi: Harian.
Catatan: Dataset mentah dapat ditemukan di folder /data/raw.
## 🔬 Ringkasam Hasil Penelitian
Performa Pelatihan: Optimizer Adam dengan learning rate rendah (0.001) menunjukkan kemampuan belajar paling superior pada data latih, mampu menurunkan loss secara signifikan.
Evaluasi Akhir: Terdapat perbedaan signifikan antara evaluasi kuantitatif dan kualitatif.
Kuantitatif: Model dengan optimizer SGD secara tak terduga menghasilkan nilai MAE dan RMSE terendah pada data uji.
Kualitatif: Visualisasi menunjukkan bahwa prediksi SGD cenderung datar dan mengalami underfitting. Model dengan optimizer Adam terbukti jauh lebih baik dalam menangkap dinamika dan volatilitas data aktual.
Model Terbaik: Berdasarkan sintesis kedua evaluasi tersebut, model dari Percobaan 12 (Optimizer Adam, η=0.001, β₁=0.5, β₂=0.85) dipilih sebagai model terbaik karena menawarkan keseimbangan antara metrik yang kompetitif dan kemampuan generalisasi kualitatif yang superior.

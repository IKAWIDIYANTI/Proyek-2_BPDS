# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

# Business Understanding

Perusahaan edutech ini beroperasi dalam lanskap pendidikan tinggi, yang saat ini menghadapi tantangan serius terkait retensi mahasiswa. 
Fenomena dropout tidak hanya berdampak negatif pada performa akademik individu, tetapi juga pada reputasi institusi dan keberlanjutan finansial. 
Dengan menganalisis data historis mahasiswa, perusahaan ini berupaya menciptakan solusi berbasis teknologi untuk memprediksi risiko dropout dan mengidentifikasi faktor-faktor kuncinya. 
Tujuan utama dari inisiatif ini adalah memungkinkan intervensi dini yang tepat, sehingga institusi pendidikan dapat mempertahankan lebih banyak mahasiswa dan meningkatkan tingkat kelulusan secara keseluruhan.

# Problem Statement

1. Tingginya tingkat dropout mahasiswa mencapai 30% yang menyebabkan kerugian finansial dan reputasi institusi
2. Ketidakmampuan mengidentifikasi mahasiswa berisiko sejak dini menyebabkan intervensi terlambat
3. Kurangnya pemahaman faktor dominan penyebab dropout menyulitkan pengambilan kebijakan
4. Adanya indikasi ketimpangan sosial ekonomi mempengaruhi kelulusan mahasiswa

# Tujuan (Goals)

1. Mengidentifikasi pola dan faktor kunci penyebab dropout.
2. Membangun dashboard interaktif untuk memantau performa mahasiswa secara real-time.
3. Mengembangkan model prediksi dropout dengan akurasi tinggi untuk intervensi dini.
4. Merekomendasikan strategi retensi mahasiswa berbasis data.

# Metrik Evaluasi Machine Learning

Karena target (Status) mungkin tidak seimbang:
1. F1-Score: Mengukur keseimbangan antara precision dan recall.
2. ROC-AUC: Mengevaluasi kemampuan model membedakan kelas dropout vs graduate.
3. Recall: Meminimalkan false negative (mahasiswa berisiko dropout tapi tidak terdeteksi).

# Cakupan Proyek

Proyek ini akan mencakup tahapan-tahapan berikut untuk mencapai tujuan bisnis yang telah ditetapkan:

1. Analisis Data Eksploratif (EDA): Melakukan investigasi awal terhadap dataset untuk memahami struktur data, distribusi fitur, mengidentifikasi outlier, dan menemukan pola atau korelasi awal antar variabel. Ini mencakup visualisasi data untuk mendapatkan insight yang lebih dalam.
2. Rekayasa Fitur (Feature Engineering): Mempersiapkan data untuk pemodelan machine learning. Ini termasuk penanganan nilai yang hilang, encoding variabel kategorikal (seperti Frequency Encoding dan One-Hot Encoding), scaling fitur numerik, dan penanganan ketidakseimbangan kelas (class imbalance) menggunakan teknik seperti SMOTE.
3. Pengembangan dan Pelatihan Model Machine Learning: Membangun dan melatih beberapa model klasifikasi yang relevan, yaitu Logistic Regression, Random Forest, dan XGBoost, untuk memprediksi risiko dropout. Model akan dilatih pada data yang telah diproses.
4. Evaluasi Model: Mengevaluasi performa setiap model menggunakan metrik yang sesuai untuk masalah klasifikasi yang tidak seimbang, seperti F1-Score, Recall, Precision, Accuracy, dan terutama ROC-AUC. Model terbaik akan dipilih berdasarkan metrik ini.
5. Pengembangan Business Dashboard: Membuat dashboard interaktif menggunakan Tableau untuk visualisasi insight kunci dari data, termasuk distribusi mahasiswa berdasarkan status, faktor-faktor risiko, dan tren performa. Dashboard ini akan menjadi alat bantu bagi stakeholder untuk pemantauan dan pengambilan keputusan.
6. Pembuatan Prototipe Sistem Machine Learning: Mengembangkan antarmuka prototipe berbasis web menggunakan Streamlit yang memungkinkan pengguna menginput data mahasiswa dan mendapatkan prediksi risiko dropout secara real-time. Prototipe ini akan menjadi bukti konsep sistem prediksi.
7. Penyusunan Rekomendasi Strategi Retensi: Berdasarkan hasil analisis data dan performa model machine learning, akan disusun rekomendasi action item konkret dan terukur bagi perusahaan edutech untuk mengembangkan strategi retensi mahasiswa yang lebih efektif.

# Persiapan

Untuk menjalankan proyek ini dan mereplikasi hasilnya, ikuti langkah-langkah di bawah ini:

# Sumber Data

Dataset yang digunakan dalam proyek ini berasal dari repositori GitHub Dicoding Academy. Dataset ini berisi 37 fitur dan 1 variabel target (Status: Dropout/Graduate), mencakup informasi demografis, latar belakang akademik, dan performa akademik mahasiswa selama dua semester pertama.

# Link Sumber Data:



https://github.com/dicodingacademy/dicoding_dataset/blob/main/students_performance/README.md



# Setup Environment:

Karena proyek ini dikembangkan di Google Colab,bisa langsung menjalankan perintah-perintah berikut di notebook Colab:

1. Membuat requirements.txt

- !pip freeze > requirements.txt

2. Menginstal dependensi dari requirements.txt:

- !pip install -r requirements.txt

  
# Business Dashboard

Dashboard ini dirancang untuk memberikan insight cepat dan mendukung pengambilan keputusan strategis bagi manajemen perusahaan edutech dan institusi pendidikan dengan berfokus pada faktor-faktor yang memengaruhi risiko dropout.

Link untuk mengakses dashboard:



https://public.tableau.com/views/DashboardStudentsPerformance/DashboardStudentsPerformance?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link



# Menjalankan Sistem Machine Learning

Prototipe sistem machine learning untuk prediksi dropout telah diimplementasikan sebagai aplikasi web sederhana menggunakan Streamlit. Prototipe ini memungkinkan pengguna untuk menginput data mahasiswa dan mendapatkan prediksi risiko dropout secara real-time.

Langkah-langkah untuk menjalankan prototipe sistem machine learning:

1. Pastikan Python Terinstal: Jika belum, instal Python pada sistem Anda.
2. Instal Dependensi: Pastikan semua pustaka yang diperlukan (misalnya streamlit, pandas, scikit-learn, xgboost, joblib, matplotlib, seaborn, imblearn) terinstal. Anda dapat menginstalnya secara massal menggunakan pip install -r requirements.txt setelah membuat file requirements.txt.
3. Siapkan Kode Aplikasi: Simpan kode aplikasi Streamlit yang telah disediakan ke dalam sebuah file Python, misalnya app.py. Pastikan juga model machine learning yang telah dilatih (xgboost_model.pkl), scaler (scaler.pkl), dan file frekuensi encoding (high_card_freq.pkl, model_features.pkl) berada dalam direktori yang sama atau jalur yang dapat diakses oleh app.py.
4. Jalankan Aplikasi Streamlit: Buka command prompt atau terminal pada komputer Anda, navigasikan ke direktori tempat Anda menyimpan file app.py, lalu jalankan perintah berikut: 'streamlit run app.py'
5. Akses Prototipe: Setelah menjalankan perintah di atas, Streamlit akan secara otomatis membuka browser web default dan menampilkan antarmuka prototipe pada alamat lokal (biasanya http://localhost:8501). Di sana, dapat memasukkan fitur-fitur mahasiswa dan mendapatkan prediksi risiko dropout.

# Link untuk mengakses prototipe:



https://proyek-2bpds-ddkkvinaibnbrdxdq5gyv7.streamlit.app/




# Conclusion

Proyek ini telah berhasil menyelesaikan permasalahan dropout mahasiswa bagi perusahaan edutech melalui pendekatan berbasis data dan machine learning. Beberapa konklusi kunci dari proyek ini adalah:

1. Identifikasi Faktor Kunci Dropout: Analisis menunjukkan bahwa performa akademik di semester pertama (terutama jumlah mata kuliah yang disetujui dan nilai rata-rata) serta kesehatan finansial mahasiswa (status pembayaran uang kuliah tepat waktu dan status debitor) merupakan prediktor paling dominan untuk risiko dropout. Ini memberikan fokus yang jelas untuk intervensi.
    - Contoh Angka: Mahasiswa yang dropout memiliki rata-rata nilai semester pertama sekitar 7.3, jauh di bawah 12.2 untuk yang tidak dropout. Hanya sekitar 2.6 mata kuliah yang disetujui oleh kelompok dropout, berbanding 5.7 pada kelompok yang lulus.
2. Signifikansi Faktor Ekonomi: Uji Chi-square mengonfirmasi bahwa status ekonomi memiliki hubungan yang sangat signifikan dengan dropout (p-value = 0.0000 untuk keduanya). Model Logistic Regression lebih lanjut menunjukkan bahwa ketepatan pembayaran uang kuliah (Tuition_fees_up_to_date) sangat kuat menurunkan risiko dropout (koefisien -2.7228), sementara status Debtor sedikit meningkatkan risiko.
3. Pengaruh Latar Belakang Pendidikan Orang Tua: Meskipun signifikan secara statistik (p-value = 0.0000), analisis Cramer's V menunjukkan bahwa hubungan antara pendidikan orang tua dengan dropout bersifat lemah hingga sedang (sekitar 0.2). Ini berarti pendidikan orang tua berkontribusi, tetapi bukan faktor penentu utama.
4. Model Prediksi yang Andal: Model machine learning XGBoost terbukti sangat efektif dalam memprediksi dropout dengan nilai AUC sebesar 0.9042. Angka ini menunjukkan bahwa model memiliki kemampuan diskriminatif yang sangat baik, mampu membedakan antara mahasiswa berisiko tinggi dan rendah.
5. Potensi Intervensi Dini: Dengan model yang akurat dan insight dari analisis data, perusahaan edutech kini memiliki dasar yang kuat untuk mendeteksi mahasiswa berisiko dropout sejak dini. Hal ini membuka peluang besar untuk intervensi proaktif dan personalisasi strategi retensi, yang pada akhirnya akan meningkatkan tingkat kelulusan dan kepuasan mahasiswa.


# Rekomendasi Action Items

Berdasarkan insight yang diperoleh dari analisis data dan model machine learning, berikut adalah beberapa rekomendasi action items konkret bagi perusahaan edutech untuk secara efektif menyelesaikan permasalahan dropout mahasiswa dan mencapai target retensi:

1. Intervensi Akademik Proaktif
    - Berikan program tutor bagi mahasiswa dengan nilai semester pertama <10.
    - Batasi jumlah SKS untuk mahasiswa berisiko di semester berikutnya.

2. Bantuan Keuangan Terarah
    - Prioritaskan beasiswa bagi mahasiswa dengan status debtor atau keterlambatan bayar.
    - Berikan diskon SPP untuk mahasiswa dengan performa akademik baik namun kesulitan ekonomi.

3. Sistem Peringatan Dini
    - Integrasikan model prediksi dengan sistem akademik kampus untuk notifikasi real-time.
    - Assign konselor akademik untuk mahasiswa dengan risiko >50%.

4. Kolaborasi dengan Orang Tua
    - Libatkan orang tua dalam pemantauan akademik melalui platform digital.
    - Sediakan workshop parenting untuk keluarga dengan latar belakang pendidikan rendah.

5. Optimalkan Dashboard
    - Tambahkan fitur tracking intervensi (e.g., status bantuan, progress akademik).
    - Implementasi alert otomatis ke departemen akademik via email/SMS.



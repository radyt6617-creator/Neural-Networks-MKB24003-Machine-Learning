**Proyek Analisis Prediktif Neural Networks
MKB24003 – Machine Learning**

Repositori ini berisi serangkaian proyek implementasi Machine Learning menggunakan berbagai arsitektur jaringan saraf (Neural Networks) untuk menyelesaikan masalah klasifikasi dan regresi pada empat domain industri yang berbeda.


**1. Online Retail II (UCI) - Prediksi Perilaku Pembelian**

Data transaksi ritel online di Inggris.
Tugas yang disarankan: Prediksi loyalitas pelanggan atau klasifikasi perilaku.
Link download:
https://archive.ics.uci.edu/dataset/502/online+retail+ii 

- Sistem ini dirancang untuk mengidentifikasi perilaku pelanggan yang cenderung membeli lebih dari satu barang dalam satu transaksi guna mendukung strategi manajemen inventaris.

- Data Understanding: Dataset transaksi retail yang mencakup informasi Quantity, Price, dan Customer ID.

- Data Preparation: Penghapusan missing value dan pembuatan target biner: pelanggan membeli >1 barang (Target=1) atau tidak (Target=0). Fitur dinormalisasi menggunakan StandardScaler.

- Model: Neural Network Sequential dengan dua hidden layer (16 & 8 neuron) dan fungsi aktivasi Sigmoid pada output layer.

- Hasil: Model mencapai akurasi sempurna (1.00) pada data uji, menunjukkan kemampuan sistem dalam membedakan pola pembelian secara presisi.



**2. Heart Failure Clinical Records - Dukungan Keputusan Medis**

Data klinis pasien gagal jantung.
Tugas yang disarankan: Prediksi risiko kematian (binary classification).
Link download:
https://archive.ics.uci.edu/dataset/519/heart+failure+clinical+records 

- Sistem pendukung keputusan medis untuk membantu tenaga kesehatan mengidentifikasi risiko kematian pasien gagal jantung berdasarkan parameter klinis secara objektif.

- Data Understanding: Meliputi 299 entri data klinis seperti usia, anemia, kadar kreatinin, dan tekanan darah.

- Data Preparation: Pembagian data latih dan uji (70:30) dengan normalisasi data untuk memastikan konvergensi model.

- Model: Arsitektur jaringan saraf dengan teknik Dropout (0.2) untuk mencegah overfitting.

- Hasil: Akurasi model sebesar 77.78%. Implementasi ini memungkinkan sistem memberikan peringatan otomatis (alert) pada EHR (Electronic Health Records) saat mendeteksi pola berisiko pada pasien.



**3. Air Quality Dataset (Italy) - Prediksi Kualitas Udara**

Data time-series kualitas udara dari sensor.
Tugas yang disarankan: Prediksi kualitas udara.
Link download:
https://archive.ics.uci.edu/dataset/501/beijing+multi+site+air+quality+data 

- Implementasi regresi untuk memprediksi nilai penutupan (Close) parameter kualitas udara sebagai komponen analitik dalam Sistem Pendukung Keputusan (DSS).

- Data Understanding: Data deret waktu (time-series) yang mencakup parameter Open, High, Low, dan Volume.

- Data Preparation: Penghapusan kolom non-numerik dan penggunaan MinMaxScaler untuk menstandarisasi skala fitur.

- Model: MLPRegressor (Multi-layer Perceptron) dengan dua hidden layer (16, 8) dan optimizer 'adam'.

- Hasil: Skor R² sebesar 0.7726, menunjukkan bahwa model mampu menjelaskan 77% variasi data target untuk pengambilan keputusan yang lebih cepat dan berbasis data.


**4. Hotel Booking Demand - Manajemen Risiko Pembatalan**

Data reservasi hotel.
Tugas yang disarankan: Prediksi pembatalan reservasi.
Link download:
https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand 

- Sistem informasi manajemen untuk memprediksi risiko kerugian akibat pembatalan pesanan hotel guna mengoptimalkan efisiensi sumber daya.

- Data Understanding: Dataset besar (119.390 entri) dengan 32 kolom, termasuk fitur kunci seperti lead_time dan country.

- Data Preparation: Penanganan nilai kosong pada kolom country dan children, serta penggunaan LabelEncoder untuk fitur kategorikal.

- Model: Neural Network Sequential (64 & 32 neuron) dengan Dropout.

- Hasil: Akurasi model 85.16%. Hasil prediksi dapat digunakan departemen pemasaran untuk mengotomatisasi konfirmasi ulang pada tamu yang terdeteksi "berisiko batal".

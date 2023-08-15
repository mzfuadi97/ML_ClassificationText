# Submission : Pemanfaatan Dataset Email 'Spam' dan 'Ham' dalam Pengenalan Pesan Spam untuk Aplikasi Bisnis

Username dicoding: mzfuadi97

| | Deskripsi |
| ----------- | ----------- |
| Dataset | [Text Classification](https://www.kaggle.com/datasets/venky73/spam-mails-dataset) |
| Masalah | Dalam konteks bisnis, dataset ini berasal dari folder enron1 yang berisi dua kategori, yaitu 'spam' (pesan spam) dan 'ham' (pesan bukan spam). Setiap kategori berisi email-email. Proses pengumpulan data melibatkan pengulangan pada setiap file teks dalam kedua folder tersebut, lalu data diolah menjadi dataframe dan disimpan dalam format CSV. Inisiatif ini dilakukan dengan harapan dapat memberikan kontribusi berharga bagi pihak lain yang memerlukan dataset semacam ini. Dataset ini dapat menjadi sumber daya yang berguna untuk pengembangan model dan analisis dalam konteks pengenalan pesan spam serta penerapan teknik-teknik pengolahan teks di berbagai aplikasi bisnis. |
| Metode pengolahan | Dataset 'spam' dan 'ham' diimpor dan dibersihkan dari nilai Null. Data dihitung secara agregat untuk setiap kategori. Teks dibersihkan dengan penghapusan karakter khusus, penggantian singkatan, dan penghapusan tanda baca. Dilakukan pula penghapusan stopwords dan stemming pada teks. Teks kemudian diubah menjadi token dan dipad agar panjangnya seragam. Model Sequential dengan lapisan LSTM dan Dense digunakan untuk klasifikasi 'spam' dan 'ham'. Model dilatih dengan metrik akurasi dan categorical cross-entropy loss, serta callback digunakan untuk menghentikan pelatihan saat akurasi di atas 75%. Metode ini bertujuan mengklasifikasikan pesan email 'spam' atau 'ham'. |
| Arsitektur model |Model arsitektur yang diterapkan dalam skrip ini mencakup input layer berupa lapisan embedding untuk mengubah kata-kata menjadi vektor numerik, disusul oleh dua lapisan LSTM yang masing-masing bertujuan untuk mengambil informasi kontekstual dari teks secara berurutan. Setelah itu, terdapat lapisan Dense yang terdiri dari 128 unit dengan fungsi aktivasi ReLU, diikuti oleh lapisan dropout untuk mengurangi overfitting, dan akhirnya dilanjutkan dengan lapisan Dense berisi 2 unit dan menggunakan fungsi aktivasi softmax sebagai lapisan output untuk klasifikasi antara 'spam' dan 'ham'. Arsitektur ini dirancang untuk efektif memproses teks berurutan dan melakukan klasifikasi pesan email. |
| Metrik evaluasi | Matriks evaluasi yang digunakan dalam skrip ini adalah akurasi (accuracy) dan categorical cross-entropy loss. Akurasi mengukur persentase jumlah prediksi yang benar dari total prediksi, sementara categorical cross-entropy loss mengukur kesesuaian prediksi model dengan label kategori yang sebenarnya. Model dikompilasi dengan optimizer Adam dan loss function 'categorical_crossentropy', dan selama pelatihan, kinerja model diukur dengan akurasi pada data pelatihan dan validasi. |
| Performa model | Pada Epoch 1 dari total 25 epoch yang direncanakan, model telah menunjukkan performa yang positif dengan akurasi sekitar 92.31% pada data pelatihan dan akurasi sekitar 97.39% pada data validasi. Hal ini mengindikasikan bahwa model memiliki kemampuan untuk memahami pola-pola dalam data pelatihan dan mampu menggeneralisasi dengan baik ke data yang belum pernah dilihat sebelumnya. Selain itu, loss function yang rendah (0.2165 untuk training dan 0.0917 untuk validasi) juga menunjukkan bahwa model cocok dengan baik terhadap kedua set data. Walaupun ini adalah awal dari proses pelatihan, hasil ini memberikan indikasi positif terhadap potensi performa yang lebih baik pada epoch-epoch berikutnya. |

### Dataset


### Model_Classification


### Validation-Vis


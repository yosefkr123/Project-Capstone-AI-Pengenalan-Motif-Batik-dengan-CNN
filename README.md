# Project-Capstone-AI-Pengenalan-Motif-Batik-dengan-CNN

Program ini adalah implementasi dari model deep learning CNN) untuk mengenali pola batik dalam gambar. Ini melibatkan proses pelatihan di mana model mempelajari fitur-fitur yang relevan dari dataset batik, dan kemudian diuji pada dataset pengujian untuk mengukur kinerjanya. Hasil evaluasi memberikan pemahaman tentang sejauh mana model dapat mengenali pola batik yang berbeda. Hasil akhir adalah model yang dapat digunakan untuk mengenali pola batik dalam gambar baru.
## Kebutuhan Utama:
1. Libraries dan Dependencies: Program ini menggunakan beberapa pustaka Python yang perlu diinstal, termasuk PyTorch, NumPy, OpenCV, scikit-learn, dan lain-lain. Program ini juga mengakses layanan IBM Cloud Object Storage untuk mengunduh dataset.
2. Dataset: Dalam program ini, diperlukan dataset gambar pola batik yang telah diunggah ke IBM Cloud Object Storage. Dataset ini harus berisi gambar-gambar dari berbagai jenis batik yang akan digunakan untuk melatih dan menguji model.
## Proses Pelatihan:
1. Inisialisasi Model: Model CNN (didefinisikan sebagai BatikCNN) diinisialisasi dengan lapisan-lapisan konvolusi, max-pooling, fully connected, dan fungsi aktivasi ReLU. Ini adalah inti dari model yang akan digunakan untuk mengenali pola batik.
2. Kompilasi Model: Model dikompilasi dengan fungsi loss nn.CrossEntropyLoss yang cocok untuk klasifikasi multi-kelas dan optimizer optim.Adam dengan learning rate yang telah ditentukan. Model akan meminimalkan loss ini selama pelatihan.
3. Pelatihan Model: Model dilatih dengan data pelatihan. Data pelatihan diambil dari dataset batik yang telah dimuat sebelumnya. Model melalui beberapa epoch (diatur ke 30 dalam kode tersebut) dan diupdate pada setiap batch data. Selama pelatihan, model belajar mengekstrak fitur-fitur dari gambar batik untuk membuat prediksi yang lebih baik.
4. Simpan Model: Setelah pelatihan, model yang telah terlatih disimpan ke dalam file dengan nama "batik_model.pth". Ini memungkinkan Anda untuk menggunakannya di masa depan tanpa harus melatih ulang.
## Proses Pengujian:
1. Evaluasi Model: Setelah pelatihan, model diubah menjadi mode evaluasi (model.eval()) sehingga tidak ada perhitungan gradien yang dilakukan.
2. Prediksi dan Perbandingan: Model melakukan prediksi pada setiap gambar dalam data pengujian (test_loader). Hasil prediksi dibandingkan dengan label sebenarnya untuk mengukur sejauh mana model dapat mengenali pola batik. Hasil evaluasi ditampilkan dalam bentuk laporan klasifikasi yang mencakup metrik-metrik seperti akurasi, presisi, recall, dan F1-score untuk setiap kategori pola batik.

## Tingkat Akurasi
![image](https://github.com/yosefkr123/Project-Capstone-AI-Pengenalan-Motif-Batik-dengan-CNN/assets/145518481/055cbd3f-e040-46b6-9ab5-10853d4eb600)

## Pengujian Gambar
![image](https://github.com/yosefkr123/Project-Capstone-AI-Pengenalan-Motif-Batik-dengan-CNN/assets/145518481/a74a819e-439c-42f3-9a46-0db5e33f4b2d)


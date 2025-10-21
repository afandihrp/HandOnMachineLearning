# APA ITU MACHINE LEARNING?

Bab ini bertujuan untuk mengklarifikasi apa itu Machine Learning (ML), mengapa ML berguna, dan memperkenalkan konsep-konsep fundamental serta kategori utama sistem ML. Ini mencakup alur kerja proyek ML tipikal, tantangan utama yang mungkin dihadapi, serta cara mengevaluasi dan menyempurnakan sistem ML. Bab ini merupakan tinjauan tingkat tinggi tanpa banyak kode.

---

## **1. Apa itu Machine Learning?**
* Definisi: Ilmu (dan seni) memprogram komputer sehingga    mereka dapat belajar dari data.
* Definisi Arthur Samuel (1959): Bidang studi yang memberi komputer kemampuan untuk belajar tanpa diprogram secara eksplisit.
* Definisi Tom Mitchell (1997): Sebuah program komputer dikatakan belajar dari pengalaman E sehubungan dengan tugas T dan ukuran kinerja P, jika kinerjanya pada T, sebagaimana diukur oleh P, meningkat seiring dengan pengalaman E.
* Contoh: Filter spam belajar membedakan email spam dan non-spam (ham) berdasarkan contoh yang diberikan.
    - Tugas (T): Menandai spam untuk email baru.
    - Pengalaman (E): Data pelatihan (contoh email spam dan ham).
    - Ukuran Kinerja (P): Rasio email yang diklasifikasikan dengan benar (akurasi).
* Istilah:
    - Training set (Set pelatihan): Contoh yang digunakan sistem untuk belajar.
    - Training instance (Contoh pelatihan) / Sampel: Setiap contoh dalam set pelatihan.
* Memiliki data saja (misalnya mengunduh Wikipedia) bukanlah ML; kinerja pada tugas tertentu harus meningkat.
---

## **2. Mengapa perlu Machine Learning?**
* **Perbandingan dengan Pemrograman Tradisional:**
    1. Pendekatan Tradisional: Membutuhkan penulisan aturan eksplisit yang panjang dan kompleks, sulit dipelihara.
    2. Pendekatan ML: Belajar secara otomatis dari data, kode lebih pendek, lebih mudah dipelihara, dan seringkali lebih akurat.
* **Adaptasi Otomatis:** Sistem ML dapat secara otomatis beradaptasi dengan perubahan (misalnya, taktik spammer baru) tanpa intervensi manual.
* **Masalah Kompleks:** ML unggul untuk masalah yang terlalu kompleks bagi pendekatan tradisional atau yang tidak memiliki algoritma yang diketahui (misalnya, pengenalan ucapan).
* **Mendapatkan Wawasan:** ML dapat membantu manusia belajar dengan menemukan pola yang tidak terlihat dalam data (data mining).
* **Kapan ML Bagus Digunakan:**
    - Masalah yang solusinya memerlukan banyak penyesuaian atau daftar aturan yang panjang.
    - Masalah kompleks yang tidak memiliki solusi baik dengan pendekatan tradisional.
    - Lingkungan yang berfluktuasi.
    - Memperoleh wawasan dari masalah kompleks dan data dalam jumlah besar.
---

## **3. Contoh-contoh penggunaan Machine Learning**
- Klasifikasi gambar produk (CNN).
- Deteksi tumor dalam pemindaian otak (Segmentasi Semantik, CNN).
- Klasifikasi artikel berita (NLP - Klasifikasi Teks, RNN, CNN, Transformer).
- Penandaan komentar ofensif (NLP - Klasifikasi Teks).
- Peringkasan dokumen (NLP - Peringkasan Teks).
- Chatbot/Asisten pribadi (NLP - NLU, Question-Answering).
- Peramalan pendapatan (Regresi - Regresi Linear/Polinomial, SVM, Random Forest, ANN, RNN, CNN, Transformer).
- Reaksi aplikasi terhadap perintah suara (Pengenalan Ucapan - RNN, CNN, Transformer).
- Deteksi penipuan kartu kredit (Deteksi Anomali).
- Segmentasi klien (Clustering).
- Visualisasi data/Pengurangan dimensi.
- Sistem rekomendasi (ANN).
- Bot game cerdas (Reinforcement Learning).
---

## **4. Jenis Sistem ML**
* Diklasifikasikan berdasarkan kriteria:
    -   Pengawasan manusia (supervised, unsupervised, semisupervised, Reinforcement Learning).
    - Kemampuan belajar secara bertahap (online vs batch learning).
    - Metode generalisasi (instance-based vs model-based learning).

* Kriteria ini tidak eksklusif dan dapat digabungkan.
    - Supervised/Unsupervised Learning: 
        - Supervised Learning: Data pelatihan berisi solusi yang diinginkan (label).
        - Tugas umum: Klasifikasi (misalnya, filter spam) dan Regresi (memprediksi nilai numerik, misalnya, harga mobil).
        - Predictors: Fitur yang digunakan untuk prediksi.
        - Attribute vs Feature: Attribute adalah tipe data, feature adalah attribute + nilainya.
        - Algoritma: k-NN, Regresi Linear/Logistik, SVM, Decision Trees, Random Forests, Neural Networks.

    - Unsupervised Learning: Data pelatihan tidak berlabel. Sistem belajar tanpa "guru".

        - Algoritma: Clustering (K-Means, DBSCAN, HCA) , Deteksi Anomali/Novelty (One-Class SVM, Isolation Forest) , Visualisasi & Pengurangan Dimensi (PCA, Kernel PCA, LLE, t-SNE) , Association Rule Learning (Apriori, Eclat).
        - Contoh: Mengelompokkan pengunjung blog , algoritma visualisasi , pengurangan dimensi (menggabungkan fitur berkorelasi, ekstraksi fitur) , deteksi anomali (mendeteksi transaksi tidak biasa) , deteksi novelty (mendeteksi instance baru yang berbeda) , association rule learning (menemukan hubungan antar atribut dalam data besar).

    - Semisupervised Learning: Menangani data yang sebagian berlabel (banyak data tak berlabel, sedikit data berlabel).
        - Contoh: Google Photos mengelompokkan wajah, pengguna memberi label nama.
        - Seringkali kombinasi algoritma unsupervised dan supervised (misalnya, Deep Belief Networks).

    - Reinforcement Learning (RL): Sistem pembelajaran (agen) mengamati lingkungan, memilih dan melakukan tindakan, dan menerima imbalan (atau hukuman). Tujuannya adalah mempelajari strategi (policy) terbaik untuk mendapatkan imbalan paling banyak dari waktu ke waktu.
        - Contoh: Robot belajar berjalan, program AlphaGo.

* Batch and Online Learning:

    - Batch Learning: Sistem tidak dapat belajar secara bertahap; harus dilatih menggunakan semua data yang tersedia (offline learning). Untuk mempelajari data baru, harus dilatih ulang dari awal pada dataset lengkap. Sederhana, tetapi memakan waktu dan sumber daya, tidak dapat beradaptasi dengan cepat, dan mungkin tidak mungkin untuk dataset yang sangat besar.
    - Online Learning: Sistem dilatih secara bertahap dengan memasukkan instance data secara berurutan (tunggal atau dalam mini-batch). Setiap langkah pembelajaran cepat dan murah, memungkinkan adaptasi on-the-fly. Cocok untuk aliran data kontinu, sumber daya terbatas, dan dataset besar (out-of-core learning). Learning rate mengontrol seberapa cepat adaptasi terhadap data baru. Tantangan: Kinerja dapat menurun jika data buruk dimasukkan; memerlukan pemantauan ketat.

* Instance-Based Versus Model-Based Learning:

    - Berfokus pada generalisasi: kemampuan membuat prediksi yang baik pada instance baru.
    - Instance-Based Learning: Sistem mempelajari contoh dengan menghafal, kemudian menggeneralisasi ke kasus baru menggunakan ukuran kesamaan untuk membandingkannya dengan contoh yang dipelajari. Contoh: k-Nearest Neighbors.

    - Model-Based Learning: Membangun model dari contoh-contoh, kemudian menggunakan model tersebut untuk membuat prediksi.
        - Langkah-langkah: Studi data , Pilih model (misalnya, model linear untuk kepuasan hidup vs. PDB) , Tentukan ukuran kinerja (fungsi utilitas/biaya) , Latih model (algoritma pembelajaran menemukan parameter model yang meminimalkan fungsi biaya) , Terapkan model untuk prediksi (inference) pada kasus baru.
        - Menjelaskan parameter model (θ) dan pemilihan model vs pelatihan model.
        - Memberikan contoh kode Python (Scikit-Learn) untuk Regresi Linear dan k-NN .
# Ringkasan Bab 1: Lanskap Machine Learning

[cite_start]Bab ini memperkenalkan konsep dasar **Machine Learning (ML)**, alasan penggunaannya, tipe-tipe sistem ML, alur kerja proyek ML, tantangan umum, serta metode evaluasi dan penyempurnaan[cite: 166].

***

## 1. Apa Itu Machine Learning?

* [cite_start]**Definisi:** Ilmu memprogram komputer agar dapat **belajar dari data**[cite: 169]. [cite_start]Tujuannya adalah meningkatkan kinerja pada tugas tertentu berdasarkan pengalaman[cite: 171].
* [cite_start]**Contoh:** Filter spam belajar dari contoh email (spam/ham) untuk mengklasifikasikan email baru[cite: 172].
* **Istilah Kunci:**
    * [cite_start]**Training set:** Kumpulan data contoh yang digunakan untuk melatih sistem[cite: 172].
    * [cite_start]**Training instance/sample:** Satu contoh data dalam training set[cite: 172].
    * [cite_start]**Pengalaman (E), Tugas (T), Ukuran Kinerja (P):** Komponen definisi formal ML[cite: 171].

***

## 2. Mengapa Menggunakan Machine Learning?

* **Mengatasi Keterbatasan Pemrograman Tradisional:**
    * [cite_start]Lebih efektif untuk **masalah kompleks** tanpa solusi algoritmik yang jelas[cite: 198].
    * [cite_start]**Menggantikan daftar aturan manual** yang panjang dan rumit[cite: 198].
    * [cite_start]Memungkinkan sistem **beradaptasi dengan lingkungan yang berubah**[cite: 199].
* [cite_start]**Memberikan Wawasan:** Membantu menemukan pola tersembunyi dalam data (*data mining*)[cite: 193].
* [cite_start]**Cocok Untuk:** Masalah dengan banyak penyesuaian, solusi tidak diketahui, lingkungan dinamis, dan analisis data besar[cite: 198, 199].

***

## 3. Contoh Aplikasi

[cite_start]ML digunakan dalam berbagai bidang [cite: 200-214]:
* Klasifikasi gambar (misalnya, produk, medis).
* Pemrosesan Bahasa Alami (NLP) (misalnya, klasifikasi teks, ringkasan, chatbot).
* Prediksi nilai numerik (Regresi) (misalnya, peramalan pendapatan).
* Pengenalan ucapan.
* Deteksi anomali (misalnya, penipuan).
* Segmentasi pelanggan (Clustering).
* Visualisasi data & Pengurangan dimensi.
* Sistem rekomendasi.
* Bot game cerdas (Reinforcement Learning).

***

## 4. Jenis Sistem Machine Learning

[cite_start]Sistem ML dapat dikategorikan berdasarkan[cite: 215]:
* **Tingkat Pengawasan:**
    * [cite_start]**Supervised Learning:** Belajar dari data **berlabel**[cite: 220]. [cite_start]Tugas utamanya **Klasifikasi** dan **Regresi**[cite: 224, 225]. [cite_start]Algoritma: k-NN, Regresi Linear/Logistik, SVM, Decision Tree, Random Forest, Neural Network [cite: 231-234].
    * [cite_start]**Unsupervised Learning:** Belajar dari data **tidak berlabel**[cite: 235]. [cite_start]Tugas utamanya **Clustering**, **Deteksi Anomali/Novelty**, **Visualisasi & Pengurangan Dimensi**, **Association Rule Learning** [cite: 239-246].
    * [cite_start]**Semisupervised Learning:** Belajar dari data yang **sebagian berlabel**[cite: 269]. [cite_start]Seringkali kombinasi algoritma supervised dan unsupervised[cite: 273].
    * [cite_start]**Reinforcement Learning (RL):** **Agen** belajar melalui **interaksi** dengan **lingkungan** untuk memaksimalkan **imbalan** kumulatif dengan mempelajari **kebijakan (policy)**[cite: 276].
* **Pembelajaran Bertahap:**
    * [cite_start]**Batch Learning:** Melatih model menggunakan **seluruh data** sekaligus (offline)[cite: 286]. [cite_start]Perlu melatih ulang dari awal untuk data baru[cite: 286].
    * [cite_start]**Online Learning:** Melatih model secara **bertahap** dengan data baru (instance tunggal atau *mini-batches*)[cite: 290]. [cite_start]Cocok untuk data streaming, sumber daya terbatas, dan *out-of-core learning*[cite: 294, 295]. [cite_start]Memerlukan pengaturan *learning rate*[cite: 296].
* **Metode Generalisasi:**
    * [cite_start]**Instance-Based Learning:** Menghafal contoh dan menggeneralisasi berdasarkan **ukuran kesamaan**[cite: 306]. [cite_start]Contoh: k-NN[cite: 357].
    * [cite_start]**Model-Based Learning:** Membangun **model** dari data latih dan menggunakannya untuk prediksi[cite: 309]. [cite_start]Melibatkan pemilihan model, pelatihan (pencarian parameter), dan inferensi [cite: 362-364]. [cite_start]Contoh: Regresi Linear[cite: 342].

***

## 5. Tantangan Utama Machine Learning

[cite_start]Tantangan utama berasal dari data dan algoritma[cite: 366]:
* **Data:**
    * [cite_start]**Kuantitas Tidak Cukup:** Algoritma ML sering membutuhkan banyak data[cite: 367]. [cite_start]Data seringkali lebih penting daripada algoritma (*The Unreasonable Effectiveness of Data*)[cite: 369, 380].
    * [cite_start]**Tidak Representatif:** Data latih harus mewakili kasus baru[cite: 385]. [cite_start]Penyebab: *sampling noise* (sampel kecil) dan *sampling bias* (metode sampling cacat)[cite: 396].
    * [cite_start]**Kualitas Buruk:** Kesalahan, *outliers*, dan *noise* menyulitkan pembelajaran[cite: 400]. [cite_start]Perlu *data cleaning*[cite: 400].
    * [cite_start]**Fitur Tidak Relevan:** Perlu *feature engineering* (seleksi, ekstraksi, pembuatan fitur) [cite: 404-406].
* **Algoritma:**
    * [cite_start]**Overfitting:** Model terlalu kompleks, berkinerja baik pada data latih tetapi buruk pada data baru[cite: 407, 416]. [cite_start]Solusi: Sederhanakan model (*regularization*), tambah data, kurangi noise[cite: 416, 417].
    * [cite_start]**Underfitting:** Model terlalu sederhana, tidak mampu mempelajari pola data[cite: 429]. [cite_start]Solusi: Gunakan model yang lebih kuat, fitur yang lebih baik, kurangi regularisasi [cite: 430-432].

***

## 6. Pengujian dan Validasi

* [cite_start]**Tujuan:** Mengestimasi seberapa baik model akan menggeneralisasi ke data baru[cite: 437].
* [cite_start]**Test Set:** Disisihkan di awal, **tidak pernah dilihat** selama pengembangan model, hanya digunakan untuk evaluasi akhir[cite: 437]. [cite_start]Mengestimasi *generalization error*[cite: 437].
* [cite_start]**Validation Set (Dev Set):** Digunakan untuk **membandingkan model** dan **menyetel hyperparameter** (*hyperparameter tuning*)[cite: 442, 459]. [cite_start]Dibuat dengan menyisihkan sebagian dari *training set* (*holdout validation*)[cite: 442].
* [cite_start]**Cross-Validation:** Alternatif untuk *holdout validation*, terutama jika validation set terlalu kecil atau besar[cite: 443]. [cite_start]Mengevaluasi model pada beberapa *fold* data[cite: 443].
* [cite_start]**Data Mismatch:** Risiko perbedaan antara data latih dan data produksi[cite: 445]. [cite_start]Gunakan *train-dev set* untuk mendiagnosis[cite: 445].
* [cite_start]**No Free Lunch Theorem:** Tidak ada model yang dijamin terbaik untuk semua dataset[cite: 448]. [cite_start]Perlu membuat asumsi dan mencoba beberapa model[cite: 448].

***

## 7. Latihan

[cite_start]Bab ini diakhiri dengan serangkaian pertanyaan untuk meninjau konsep-konsep yang telah dibahas [cite: 449-460].
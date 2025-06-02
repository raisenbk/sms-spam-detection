# Deteksi Spam SMS (SMS Spam Detection)

Proyek ini bertujuan untuk mengklasifikasikan pesan SMS sebagai spam atau bukan spam (ham) menggunakan pendekatan *machine learning*. Model yang digunakan adalah Naive Bayes Classifier dengan fitur Teks yang diekstraksi menggunakan TF-IDF.

## Deskripsi Proyek

Dalam proyek ini, saya membangun sebuah sistem untuk mendeteksi SMS spam secara otomatis. Prosesnya meliputi beberapa tahapan utama:
1.  **Pemuatan Data**: Membaca dataset SMS.
2.  **Pra-pemrosesan Data**: Membersihkan dan mempersiapkan teks SMS.
3.  **Ekstraksi Fitur**: Mengubah data teks menjadi representasi numerik menggunakan TF-IDF (Term Frequency-Inverse Document Frequency).
4.  **Pembagian Data**: Memisahkan dataset menjadi data latih dan data uji.
5.  **Pelatihan Model**: Melatih model Naive Bayes menggunakan data latih.
6.  **Evaluasi Model**: Mengukur performa model pada data uji.
7.  **Prediksi**: Menggunakan model yang telah dilatih untuk memprediksi label SMS baru.

Kode utama dan analisis terdapat dalam Jupyter Notebook: `sms-spam-detection.ipynb`.

Proyek ini dikembangkan sebagai bagian dari Ujian Akhir Semester (UAS) mata kuliah IF540L.

## Dataset

Dataset yang digunakan adalah `dataset_sms_spam_v1.csv`. Dataset ini terdiri dari dua kolom utama:
* `Teks`: Berisi teks dari pesan SMS.
* `label`: Berisi label klasifikasi SMS, yaitu 'spam' atau 'ham'.

## Teknologi yang Digunakan

* Python 3.x
* Jupyter Notebook
* **Library Python:**
    * Pandas: Untuk manipulasi dan analisis data.
    * Scikit-learn: Untuk
        * `TfidfVectorizer` (ekstraksi fitur TF-IDF)
        * `train_test_split` (pembagian data)
        * `MultinomialNB` atau `GaussianNB` (model Naive Bayes)
        * Metrik evaluasi (misalnya, `accuracy_score`, `classification_report`)

## Instalasi dan Setup

Untuk menjalankan proyek ini di lingkungan lokal Anda, ikuti langkah-langkah berikut:

1.  **Clone repositori ini (jika sudah diunggah ke GitHub):**
    ```bash
    git clone https://github.com/raisenbk/sms-spam-detection.git
    cd sms-spam-detection
    ```

2.  **Instal library Python yang dibutuhkan:**
    Pastikan Anda memiliki Python dan pip terinstal. Kemudian jalankan:
    ```bash
    pip install pandas scikit-learn jupyterlab
    ```

## Cara Menjalankan

1.  Pastikan file dataset `dataset_sms_spam_v1.csv` berada dalam direktori yang sama dengan file Jupyter Notebook.
2.  Buka Jupyter Notebook atau JupyterLab:
    ```bash
    jupyter lab
    ```
    atau
    ```bash
    jupyter notebook
    ```
3.  Buka file notebook `sms-spam-detection.ipynb`.
4.  Jalankan sel-sel kode di dalam notebook secara berurutan dari atas ke bawah.

## Hasil

Model Naive Bayes yang dilatih berhasil mencapai akurasi sebesar **92%** pada data uji. Metrik performa lainnya seperti presisi, recall, dan F1-score untuk masing-masing kelas (spam dan ham) dapat dilihat pada output sel evaluasi di dalam notebook.

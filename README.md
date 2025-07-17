# 🧠 Gojek Sentiment Analysis using Machine Learning & Deep Learning
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

Proyek ini menganalisis sentimen ulasan pengguna aplikasi Gojek menggunakan data hasil *scraping* langsung dari Google Play Store. Sistem ini mengimplementasikan berbagai algoritma Machine Learning dan Deep Learning untuk memahami opini pelanggan, mendeteksi masalah layanan, serta memberikan insight strategis bagi pengambilan keputusan produk.

Sistem ini dirancang untuk **mengklasifikasikan ulasan pelanggan ke dalam tiga kategori sentimen utama**, yaitu: **Negatif**, **Netral**, dan **Positif**. Proses klasifikasi ini bertujuan untuk:

- **Mengidentifikasi keluhan pelanggan** secara otomatis,
- **Mendukung pengambilan keputusan berbasis data** oleh tim produk dan layanan,
- **Meningkatkan kualitas pengalaman pengguna (User Experience)** dengan memberikan respon proaktif terhadap tren sentimen.

Dengan pendekatan ini, perusahaan dapat mengetahui area layanan mana yang mendapat respon buruk, memahami alasan di balik penurunan rating aplikasi, dan mengambil langkah korektif dengan lebih cepat. Klasifikasi tiga arah ini juga berguna untuk menyaring *feedback netral* sebagai dasar evaluasi fitur baru atau kebijakan yang masih perlu pengembangan.


---
## 💼 Rancangan Bisnis

Dalam era ekonomi digital, ulasan pelanggan merupakan sumber insight yang sangat penting dalam evaluasi performa layanan. Dengan ribuan ulasan yang masuk setiap minggu, tim produk kesulitan menganalisis data secara manual.

Proyek ini hadir sebagai solusi **analitik otomatis** untuk:
- **Mendeteksi tren sentimen pelanggan** secara real-time
- **Mengevaluasi kepuasan pengguna** berdasarkan fitur dan layanan tertentu
- **Memberikan umpan balik strategis** bagi pengembangan produk dan peningkatan pelayanan

Sistem ini dapat diintegrasikan ke dalam *dashboard analytics* atau digunakan untuk *alert system* apabila sentimen negatif meningkat tajam dalam waktu tertentu.

---

## 🎯 Tujuan Proyek

- Membangun pipeline analisis sentimen dari tahap *data acquisition* hingga *model evaluation*
- Menggunakan metode klasifikasi: Random Forest, SVM (TF-IDF), dan LSTM (deep learning)
- Menganalisis performa model dan membuat insight untuk rekomendasi bisnis
- Mengembangkan dokumentasi sistem sebagai bagian dari portofolio System Analyst

---

## 📂 Struktur Repository
```
analisis-sentiment-gojek/
├── README.md                         # Dokumentasi proyek
├── LICENSE                           # Lisensi proyek (MIT)
├── analisis_sentimen.ipynb           # Notebook analisis dan modeling
├── gojek_reviews.csv                 # Dataset hasil scraping
├── requirements.txt                  # Daftar library Python
└── scrapping_data.ipynb              # Notebook untuk scraping ulasan Gojek

```

---

## 🛠️ Tools dan Teknologi

- **Python**: pandas, numpy, matplotlib, seaborn
- **Machine Learning**: Scikit-learn (TF-IDF, SVM, Random Forest)
- **Deep Learning**: TensorFlow, Keras (LSTM)
- **NLP Tools**: NLTK, Sastrawi
- **Scraping**: google-play-scraper

---

## 🔍 Alur Sistem

1. **Scraping Data**  
   Mengambil ulasan pengguna aplikasi Gojek dari Google Play Store menggunakan `google-play-scraper`.

2. **Preprocessing**  
   Proses pembersihan teks: case folding, penghapusan simbol, tokenisasi, stopword removal, dan stemming.

3. **Feature Extraction**  
   - Menggunakan TF-IDF untuk model klasik (SVM, Random Forest)
   - Tokenizer & padding sequence untuk model LSTM

4. **Modeling**  
   - **SVM** dan **Random Forest** untuk baseline model
   - **LSTM** untuk representasi urutan kata dan konteks kalimat

5. **Evaluation**  
   Menggunakan metrik akurasi, klasifikasi laporan, dan visualisasi hasil prediksi.

---

## 📊 Evaluasi Model

| Model         | Akurasi | Kelebihan                  | Kekurangan                           |
|---------------|---------|----------------------------|--------------------------------------|
| Random Forest | >85%    | Cepat, sederhana           | Rentan overfitting pada data kecil   |
| SVM (TF-IDF)  | >85%    | Stabil & akurat untuk teks | Tidak memahami konteks kalimat       |
| LSTM          | ~80-85% | Pahami urutan & konteks    | Butuh tuning & data lebih besar      |


## 💡 Insight dan Rekomendasi

- Model LSTM cukup menjanjikan namun memerlukan jumlah data yang lebih besar serta tuning lanjutan.
- Data ulasan tidak seimbang → disarankan menggunakan teknik oversampling/undersampling.
- Untuk hasil yang lebih kontekstual, pertimbangkan penggunaan *word embeddings* seperti BERT atau IndoBERT.

---
## 📊 Implikasi Bisnis:
- Sistem ini dapat digunakan sebagai komponen utama dalam dashboard monitoring sentimen pelanggan, mempermudah deteksi dini atas tren negatif yang muncul di Google Play Store atau platform ulasan lainnya.
- Insight seperti "model cenderung gagal mengenali ulasan positif" memberi sinyal kepada tim bisnis bahwa pengukuran kepuasan pelanggan mungkin bias jika hanya mengandalkan satu model—sehingga memerlukan validasi silang dan intervensi data engineer.
- Rekomendasi selanjutnya adalah mengembangkan sistem yang mampu:
      - Mengelompokkan keluhan berdasar fitur aplikasi (layanan pengantaran, pembayaran, dsb.)
      - Mengukur perubahan sentimen pasca update aplikasi
      - Memberikan alert otomatis jika proporsi sentimen negatif meningkat signifikan

Dengan penerapan sistem seperti ini, tim produk dan CX dapat lebih cepat merespons masalah, meningkatkan kepuasan pelanggan, serta mempertahankan rating aplikasi di tengah persaingan platform digital.
---

## 📌 Cara Menjalankan

1. Clone repositori ini
2. Install dependency dari `Requirements.txt`:
```bash
pip install -r Requirements.txt
```
3. Jalankan notebook secara berurutan:
  - Scrapping_Data.ipynb untuk mengambil data
  - Sentiment_Analysis_Gojek.ipynb untuk analisis & modeling

---
---

## ✨ Catatan Reviewer Dicoding

> ✅ Semua kriteria utama dan saran tambahan **terpenuhi dengan sangat baik**  
> ⭐ **Rating Proyek: 5/5 (Sempurna)**  
> 📌 Proyek ini merupakan bagian dari kelas **Belajar Fundamental Deep Learning** – Dicoding  
> 📚 Submission ID: `4153632` | Tanggal Submit: `14 April 2025`

---

## 📄 Peran System Analyst

Sebagai System Analyst, tanggung jawab utama dalam proyek ini meliputi:

- **Analisis Kebutuhan Sistem**: Mendesain pipeline sentiment analysis untuk kebutuhan evaluasi layanan digital berbasis ulasan.
- **Perancangan Solusi Teknologi**: Menentukan pendekatan machine learning dan deep learning yang sesuai.
- **Dokumentasi Sistem**: Menyusun arsitektur proses, pipeline data, dan dokumentasi fungsional.
- **Evaluasi Sistem & Insight**: Memberikan insight strategis berdasarkan hasil model dan evaluasi data.

---
## 👩‍💻 Tentang Pengembang

**Faizah Rizki Auliawati**  
Mahasiswa Informatika sekaligus seorang Data Enthusiast dengan minat mendalam pada bidang Machine Learning, System Analysis, dan pengembangan solusi berbasis data. Proyek ini merupakan bagian dari portofolio ilmiah dan praktikal untuk pengembangan sistem cerdas berbasis rekomendasi.

---

## 📄 Lisensi

Proyek ini berlisensi MIT. Lihat `LICENSE` untuk detail.
    



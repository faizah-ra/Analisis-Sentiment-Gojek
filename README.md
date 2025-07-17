# 🧠 Gojek Sentiment Analysis using Machine Learning & Deep Learning
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

Proyek ini menganalisis sentimen ulasan pengguna aplikasi Gojek menggunakan data hasil *scraping* langsung dari Google Play Store. Sistem ini mengimplementasikan berbagai algoritma Machine Learning dan Deep Learning untuk memahami opini pelanggan, mendeteksi masalah layanan, serta memberikan insight strategis bagi pengambilan keputusan produk.

---

## 🎯 Tujuan Proyek

- Membangun pipeline analisis sentimen dari tahap *data acquisition* hingga *model evaluation*
- Menggunakan metode klasifikasi: Random Forest, SVM (TF-IDF), dan LSTM (deep learning)
- Menganalisis performa model dan membuat insight untuk rekomendasi bisnis
- Mengembangkan dokumentasi sistem sebagai bagian dari portofolio System Analyst

---

## 📂 Struktur Repository
```
Analisis-Sentiment-Gojek/
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

## 🔍 Ringkasan Alur Sistem

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

## 💡 Insight dan Rekomendasi

- Model LSTM cukup menjanjikan namun memerlukan jumlah data yang lebih besar serta tuning lanjutan.
- Data ulasan tidak seimbang → disarankan menggunakan teknik oversampling/undersampling.
- Untuk hasil yang lebih kontekstual, pertimbangkan penggunaan *word embeddings* seperti BERT atau IndoBERT.

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

## 👩‍💻 Tentang Pengembang

**Faizah Rizki Auliawati**  
Mahasiswa Informatika sekaligus seorang Data Enthusiast dengan minat mendalam pada bidang Machine Learning, System Analysis, dan pengembangan solusi berbasis data. Proyek ini merupakan bagian dari portofolio ilmiah dan praktikal untuk pengembangan sistem cerdas berbasis rekomendasi.

---

## 📄 Lisensi

Proyek ini berlisensi MIT. Lihat `LICENSE` untuk detail.
    



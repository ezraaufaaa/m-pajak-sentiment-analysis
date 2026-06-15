[README .md](https://github.com/user-attachments/files/28956985/README.md)
# Analisis Sentimen Ulasan DJP Pajak: Perbandingan IndoBERT vs mBERT

## Deskripsi Proyek
Proyek ini bertujuan untuk melakukan analisis sentimen terhadap ulasan pengguna aplikasi DJP Pajak yang diambil dari Google Play Store. Penelitian membandingkan performa model berbasis Transformer, yaitu IndoBERT dan mBERT, dalam mengklasifikasikan sentimen pengguna ke dalam kategori:

- Positive
- Neutral
- Negative

Selain model Transformer, notebook juga memuat eksperimen pembanding menggunakan pendekatan TF-IDF + Logistic Regression dan TF-IDF + Naive Bayes.

## Dataset
Dataset diperoleh melalui scraping Google Play Store menggunakan library:

- google-play-scraper

Aplikasi yang dianalisis:

- DJP Pajak (`id.go.pajak.djp`)

Data yang diambil meliputi:

- Isi ulasan pengguna (`text`)
- Rating pengguna (`rating`)

## Tahapan Penelitian

1. Scraping ulasan dari Google Play Store
2. Pelabelan sentimen berdasarkan rating
3. Preprocessing teks
4. Tokenisasi dan normalisasi
5. Stopword removal
6. Stemming menggunakan Sastrawi
7. Klasifikasi sentimen menggunakan IndoBERT dan mBERT
8. Evaluasi performa model
9. Visualisasi hasil sentimen

## Teknologi yang Digunakan

### Bahasa Pemrograman
- Python

### Library Utama
- pandas
- numpy
- matplotlib
- seaborn
- nltk
- Sastrawi
- scikit-learn
- transformers
- torch
- google-play-scraper

## Struktur Alur Proyek

```text
Scraping Data
      ↓
Labeling Sentimen
      ↓
Preprocessing Teks
      ↓
Tokenisasi & Stemming
      ↓
Training Model
      ↓
Evaluasi Model
      ↓
Visualisasi Hasil
```

## Pelabelan Sentimen

| Rating | Sentimen |
|----------|----------|
| 4 - 5 | Positive |
| 3 | Neutral |
| 1 - 2 | Negative |

## Instalasi

```bash
pip install google-play-scraper
pip install pandas
pip install nltk
pip install Sastrawi
pip install transformers
pip install torch
pip install scikit-learn
pip install matplotlib
pip install seaborn
```

## Menjalankan Proyek

### 1. Scraping Dataset

```bash
python scraping.py
```

### 2. Preprocessing Data

```bash
python preprocessing.py
```

### 3. Training dan Evaluasi Model

```bash
python train_model.py
```

## Evaluasi

Metode evaluasi yang digunakan:

- Accuracy
- Precision
- Recall
- F1-Score
- Classification Report
- Confusion Matrix

## Visualisasi

Proyek menghasilkan beberapa visualisasi:

- Distribusi sentimen (Bar Chart)
- Distribusi sentimen (Pie Chart)
- Perbandingan hasil IndoBERT vs mBERT
- Confusion Matrix
- Grafik performa model

## Output

File yang dihasilkan antara lain:

```text
dataset_playstore_*.csv
hasil_preprocessing.csv
dataset_djp_sentiment_fixed.csv
hasil_ringan.csv
hasil_perbandingan_model.csv
```

## Tujuan Penelitian

Mengetahui model yang memiliki performa terbaik dalam melakukan analisis sentimen berbahasa Indonesia pada ulasan pengguna aplikasi DJP Pajak.

## Author

Wenceslaus Antieka Dhitya
BINUS University

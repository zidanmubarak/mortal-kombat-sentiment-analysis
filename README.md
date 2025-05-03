# Analisis Sentimen Ulasan Aplikasi Mortal Kombat Mobile

Proyek ini melakukan analisis sentimen terhadap ulasan pengguna aplikasi Mortal Kombat Mobile dari Google Play Store menggunakan pendekatan berbasis leksikon (dictionary-based approach).

## Deskripsi

Proyek ini menggunakan teknik Natural Language Processing (NLP) untuk menganalisis sentimen dari ulasan pengguna dalam Bahasa Indonesia. Analisis dilakukan melalui beberapa tahap:

1. Pengumpulan Data

   - Menggunakan google-play-scraper untuk mengambil ulasan
   - Total 43,854 ulasan berhasil dikumpulkan
   - Data mencakup rating, konten ulasan, dan informasi pengguna

2. Preprocessing Text

   - Case folding
   - Tokenization menggunakan NLTK
   - Stopword removal (Bahasa Indonesia & Inggris)
   - Stemming menggunakan Sastrawi
   - Normalisasi kata slang/informal

3. Analisis Sentimen
   - Menggunakan pendekatan berbasis leksikon
   - Kamus sentimen positif dan negatif
   - Perhitungan skor sentimen berdasarkan kemunculan kata

## Hasil Analisis

Distribusi Sentimen:

- Positif: 56.3%
- Netral: 27.0%
- Negatif: 16.7%

Distribusi Rating:

- ⭐⭐⭐⭐⭐ (5 bintang): 23,930 ulasan
- ⭐⭐⭐⭐ (4 bintang): 4,714 ulasan
- ⭐⭐⭐ (3 bintang): 4,426 ulasan
- ⭐⭐ (2 bintang): 2,442 ulasan
- ⭐ (1 bintang): 8,342 ulasan

## Teknologi yang Digunakan

- Python 3.10
- Pandas & Numpy untuk pengolahan data
- NLTK untuk text processing
- Sastrawi untuk stemming Bahasa Indonesia
- Matplotlib & Seaborn untuk visualisasi
- Google Play Scraper untuk pengambilan data

## Cara Penggunaan

### Menggunakan Google Colab (Direkomendasikan)

Ada dua cara untuk menggunakan notebook di Google Colab:

#### Metode 1: Langsung dari GitHub

1. Klik link notebook berikut:
    - [app_scraper.ipynb](https://colab.research.google.com/github/zidanmubarak/mortal-kombat-sentiment-analysis/blob/main/app_scraper.ipynb)
    - [analisis_sentiment.ipynb](https://colab.research.google.com/github/zidanmubarak/mortal-kombat-sentiment-analysis/blob/main/analisis_sentiment.ipynb)

2. Klik tombol "Open in Colab" yang muncul di notebook
3. Simpan copy notebook ke Google Drive Anda dengan klik "File > Save a copy in Drive"
4. Install dependencies dengan menjalankan cell berikut:

```python
!pip install -r requirements.txt
```

#### Metode 2: Melalui Google Drive

1. Download repository ini sebagai ZIP
2. Extract file ZIP
3. Upload file-file berikut ke Google Drive Anda:
   - `app_scraper.ipynb`
   - `analisis_sentiment.ipynb`
   - `requirements.txt`
4. Buka file notebook dengan klik kanan > "Open with" > Google Colaboratory
5. Install dependencies dengan menjalankan cell berikut:

```python
!pip install -r requirements.txt
```

#### Langkah Selanjutnya (untuk kedua metode):

1. Jalankan semua cell secara berurutan
2. File hasil scraping (`app_reviews.csv`) akan otomatis tersimpan
3. Untuk mengakses file hasil scraping di notebook analisis:
   ```python
   from google.colab import files
   files.upload()  # Upload app_reviews.csv dari komputer Anda
   ```

### Menggunakan Localhost (Python 3.10)

1. Clone repository ini:

```bash
git clone https://github.com/zidanmubarak/mortal-kombat-sentiment-analysis.git
```

2. Buat virtual environment (opsional tapi direkomendasikan):

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

3. Install dependencies yang diperlukan:

```bash
pip install -r requirements.txt
```

4. Jalankan Jupyter Notebook:

```bash
jupyter notebook
```

5. Buka dan jalankan notebook secara berurutan:
   - `app_scraper.ipynb`
   - `analisis_sentiment.ipynb`

### Catatan Penting

- Pastikan menggunakan Python 3.10 jika menjalankan di localhost
- Beberapa package mungkin memerlukan Microsoft Visual C++ Build Tools jika menggunakan Windows
- Penggunaan Google Colab direkomendasikan karena sudah terinstal sebagian besar dependencies yang diperlukan

## Kontribusi

Silakan berkontribusi dengan membuat pull request atau melaporkan issues.
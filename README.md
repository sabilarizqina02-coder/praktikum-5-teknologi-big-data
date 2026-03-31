# PRAKTIKUM 5 TEKNOLOGI BIG DATA

## Smart Transportation – Real-Time Analytics System

---

## Deskripsi

Praktikum ini bertujuan untuk membangun sistem analisis transportasi secara real-time menggunakan teknologi Big Data. Sistem ini mensimulasikan aliran data perjalanan (trip data), memproses data menggunakan Spark Streaming, serta menampilkan hasil analisis dalam bentuk dashboard interaktif menggunakan Streamlit.

---

## Tujuan

1. Memahami konsep streaming data pada Big Data
2. Mengimplementasikan Spark Streaming untuk pemrosesan real-time
3. Melakukan analisis data transportasi secara dinamis
4. Menampilkan visualisasi data dalam dashboard interaktif
5. Menghasilkan alert berdasarkan kondisi tertentu

---

## Arsitektur Sistem

Sistem terdiri dari tiga komponen utama:

1. **Data Generator**
   Menghasilkan data perjalanan (trip) secara kontinu dalam format JSON

2. **Streaming Layer (Spark Streaming)**
   Membaca data stream dan menyimpannya ke dalam storage (parquet)

3. **Dashboard (Streamlit)**
   Menampilkan hasil analisis data secara real-time

Alur sistem:
Generator → Spark Streaming → Storage → Dashboard

---

## Struktur Project

```
BIGDATA-PROJECT
│
├── scripts/
│   └── transportation/
│       ├── streaming_trip_layer.py
│       └── trip_generator.py
│
├── analytics/
│   ├── __init__.py
│   └── transportation_analytics.py
│
├── alerts/
│   ├── __init__.py
│   └── transportation_alert.py
│
├── dashboard/
│   └── dashboard_transportation.py
│
├── data/
│   ├── serving/
│   │   └── transportation/
│   └── checkpoints/
│
└── README.md
```

---

## Teknologi yang Digunakan

* Python
* Apache Spark (PySpark)
* Streamlit
* Pandas
* JSON & Parquet

---

## Cara Menjalankan Sistem

Pastikan berada di root project:

```
cd bigdata-project
```

### 1. Jalankan Spark Streaming

```
spark-submit scripts/transportation/streaming_trip_layer.py
```

### 2. Jalankan Data Generator

```
python scripts/transportation/trip_generator.py
```

### 3. Jalankan Dashboard

```
streamlit run dashboard/dashboard_transportation.py
```

### 4. Akses Dashboard

Buka browser dan akses:

```
http://localhost:8501
```

---

## Fitur Sistem

* Monitoring jumlah perjalanan (Total Trips)
* Total pendapatan (Total Fare)
* Lokasi dengan aktivitas tertinggi
* Deteksi jam sibuk (Peak Hour)
* Visualisasi distribusi kendaraan
* Tren mobilitas
* Deteksi anomali perjalanan
* Sistem alert (High Traffic & High Fare)

---

## Hasil

Sistem berhasil menampilkan data transportasi secara real-time dalam bentuk dashboard interaktif. Data terus diperbarui secara otomatis sesuai dengan aliran data dari generator.

---

## Kesimpulan

Praktikum ini menunjukkan bahwa teknologi Big Data seperti Spark Streaming mampu memproses data secara real-time dengan efisien. Integrasi dengan dashboard memungkinkan pengguna untuk memantau kondisi transportasi secara langsung dan mengambil keputusan berbasis data.

---

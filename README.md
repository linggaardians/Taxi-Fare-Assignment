# Big Data & AI — Taxi Fare Prediction (PySpark)

## Overview

Proyek ini adalah implementasi end-to-end pemodelan prediksi tarif taksi menggunakan PySpark. Notebook ini mencakup proses mulai dari eksplorasi data, pembersihan, engineering fitur berbasis rumus Haversine, hingga pelatihan dan evaluasi model regresi.

## Objectives

* Mengolah dataset NYC Taxi Fare berukuran besar menggunakan Spark.
* Membersihkan data dan menangani outlier.
* Menghitung jarak perjalanan menggunakan rumus Haversine.
* Melatih model regresi (Linear Regression, Random Forest, Gradient Boosted Trees, dll jika digunakan).
* Mengevaluasi performa model menggunakan RMSE dan R².

## Dataset

Dataset berisi kolom-kolom umum seperti:

* `fare_amount`
* `pickup_longitude`, `pickup_latitude`
* `dropoff_longitude`, `dropoff_latitude`
* `passenger_count`
* timestamp pickup/dropoff (jika tersedia)

Notebook telah menangani:

* Penghapusan nilai yang tidak valid
* Filtering geografis
* Outlier removal

## Feature Engineering

Fitur utama:

* **Haversine distance**: Menghitung jarak antara titik pickup dan dropoff berdasarkan koordinat.
* Opsi transformasi tambahan dipertahankan jika diperlukan.

## Modeling

Model yang digunakan:

* **Linear Regression** sebagai baseline
* Model lain dapat ditambahkan sesuai kebutuhan

Output model meliputi:

* Prediksi tarif
* Evaluasi RMSE & R²

## Evaluation

Model dievaluasi menggunakan `RegressionEvaluator` dengan metrik:

* **RMSE** untuk mengukur error absolut
* **R²** untuk melihat kualitas fit

## Project Structure

```
├── taxi_fare_v2.ipynb
└── README.md (file ini)
```

## Requirements

* Python 3.9+
* PySpark
* Pandas (opsional untuk inspeksi kecil)
* Matplotlib (opsional)

Install dependencies:

```bash
pip install pyspark pandas matplotlib
```

## How to Run


## Notes

* Proyek ini disiapkan untuk tugas **Big Data & AI**.
* Cocok untuk demonstrasi pipeline big data berbasis PySpark.

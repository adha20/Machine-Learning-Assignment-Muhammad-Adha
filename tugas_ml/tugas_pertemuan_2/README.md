# Machine Learning Session 2

Proyek ini berisi latihan dan tugas tentang preprocessing data menggunakan dataset Titanic.

## Deskripsi

Notebook ini mencakup pembelajaran tentang manipulasi dan preprocessing data untuk machine learning, meliputi:

- **Data Loading**: Mengimpor dataset Titanic dari repository publik
- **Exploratory Data Analysis**: Melihat struktur data dan missing values
- **Data Cleaning**: 
  - Menghapus kolom yang tidak relevan (PassengerId, Name, Cabin, Ticket)
  - Menangani missing values pada kolom Age dengan median
  - Menghapus baris dengan missing values
- **Feature Engineering**:
  - One-hot encoding untuk kolom kategorikal (Sex, Embarked)
- **Normalisasi**:
  - MinMaxScaler
  - StandardScaler

## Requirements

```
pandas
scikit-learn
```

## Cara Menggunakan

1. Buka notebook `ML_learning_session_2_exercise_and_assignment.ipynb`
2. Jalankan cell secara berurutan dari atas ke bawah
3. Dataset Titanic akan diunduh otomatis dari URL

## Dataset

Dataset Titanic diambil dari: https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv

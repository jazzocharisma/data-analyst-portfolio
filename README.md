# Analisis Kualitas Udara Jakarta 2023

Proyek ini menganalisis data ISPU (Indeks Standar Pencemar Udara)
dari 5 stasiun pemantauan resmi di DKI Jakarta sepanjang tahun 2023.
Data bersumber dari Jakarta Open Data (data.jakarta.go.id).

## Pertanyaan yang Ingin Dijawab

- Seberapa sering udara Jakarta berada di level aman?
- Bulan apa yang paling buruk dan paling bersih?
- Wilayah mana yang paling terdampak polusi?
- Polutan apa yang paling dominan?

## Dataset

- Sumber: [Jakarta Open Data](https://data.jakarta.go.id)
- Periode: Desember 2022 – November 2023
- Jumlah data: 1.804 baris (setelah pembersihan)
- Stasiun: Bunderan HI, Kelapa Gading, Jagakarsa, Lubang Buaya, Kebon Jeruk

## Temuan Utama

1. Hanya **13.1%** hari sepanjang 2023 yang berkategori Baik —
   udara bersih adalah pengecualian di Jakarta, bukan standar.
2. **Februari** adalah bulan terbersih (indeks 48), bertepatan
   dengan puncak musim hujan.
3. **Oktober** adalah bulan terburuk (indeks 91), diperparah
   El Niño 2023 yang memperpanjang musim kemarau.
4. **Lubang Buaya (Jakarta Timur)** adalah wilayah paling kritis —
   satu-satunya stasiun yang rata-rata kategorinya mencapai
   Tidak Sehat di bulan Oktober.
5. **PM2.5** melampaui batas Sedang di semua stasiun sepanjang tahun.

## Visualisasi

| # | Judul | Deskripsi |
|---|-------|-----------|
| 1 | Distribusi Kategori Udara | Proporsi hari per kategori sepanjang 2023 |
| 2 | Rata-rata Polutan per Stasiun | Perbandingan 6 polutan antar 5 wilayah |
| 3 | Tren ISPU Bulanan | Pola musiman indeks udara sepanjang tahun |
| 4 | Heatmap Stasiun vs Bulan | Peta panas kategori udara per lokasi per bulan |

## Tools yang Digunakan

- Python 3.11
- pandas, numpy — pengolahan data
- matplotlib, seaborn — visualisasi
- Jupyter Notebook (VS Code)

## Cara Menjalankan

```bash
pip install pandas numpy matplotlib seaborn
```

Buka file `notebooks/analisis.ipynb` dan jalankan sel dari atas ke bawah.

## Struktur Folder
01-kualitas-udara-jakarta/
├── data/
│   ├── raw/
│   │   └── ispu_jakarta_2023.xls
│   ├── viz1_kategori_udara.png
│   ├── viz2_polutan_per_stasiun.png
│   ├── viz3_tren_bulanan.png
│   └── viz4_heatmap_stasiun_bulan.png
└── notebooks/
└── analisis.ipynb

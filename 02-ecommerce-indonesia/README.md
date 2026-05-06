# Analisis Perilaku Belanja E-Commerce 2016–2018

Proyek ini menganalisis dataset transaksi e-commerce dari platform
Olist yang beroperasi di Brasil — pasar berkembang dengan karakteristik
yang sangat mirip dengan Indonesia: penetrasi internet yang cepat,
dominasi pembayaran non-tunai, dan tantangan logistik antar wilayah.

Data bersumber dari Kaggle (Olist Brazilian E-Commerce Public Dataset)
dan mencakup lebih dari 96 ribu transaksi yang telah selesai.

## Pertanyaan yang Ingin Dijawab

- Seberapa cepat platform e-commerce bisa tumbuh dalam 2 tahun?
- Produk apa yang paling laris dan menghasilkan nilai tertinggi?
- Metode pembayaran apa yang paling dominan?
- Seberapa andal sistem pengiriman platform ini?
- Apakah pembeli cenderung kembali berbelanja?

## Dataset

- Sumber: [Kaggle — Olist Brazilian E-Commerce](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- Periode: September 2016 – Agustus 2018
- Jumlah transaksi selesai: 96.478
- Jumlah pembeli unik: 93.358
- Jumlah penjual aktif: 2.970
- Jumlah file: 9 tabel yang digabungkan

## Temuan Utama

1. Platform tumbuh dari nol ke **7.269 transaksi/bulan** hanya
   dalam 14 bulan — lonjakan dipicu efek Harbolnas November 2017.
2. **93.358 dari 96.478 transaksi** berasal dari pembeli unik —
   hampir tidak ada repeat buyer. Loyalitas pelanggan adalah
   tantangan terbesar yang belum terpecahkan.
3. **bed_bath_table** dan **health_beauty** memimpin sebagai
   kategori terlaris — produk rumah tangga mengalahkan elektronik.
4. **75.3% transaksi** menggunakan kartu kredit, namun transfer
   bank (boleto) tetap relevan dengan nilai transaksi yang hampir
   setara.
5. Rata-rata paket tiba **11 hari lebih cepat** dari estimasi —
   strategi under-promise over-deliver terbukti efektif menjaga
   kepuasan pembeli.

## Visualisasi

| # | Judul | Deskripsi |
|---|-------|-----------|
| 1 | Tren Transaksi Bulanan | Pertumbuhan volume transaksi 2016–2018 |
| 2 | Top 10 Kategori Terlaris | Kategori produk dengan transaksi terbanyak |
| 3 | Analisis Metode Pembayaran | Proporsi dan nilai rata-rata per metode bayar |
| 4 | Analisis Keterlambatan Pengiriman | Distribusi selisih estimasi vs aktual pengiriman |

## Tools yang Digunakan

- Python 3.11
- pandas, numpy — pengolahan dan penggabungan data
- matplotlib, seaborn — visualisasi
- Jupyter Notebook (VS Code)

## Cara Menjalankan

```bash
pip install pandas numpy matplotlib seaborn
```

Buka file `notebooks/analisis.ipynb` dan jalankan sel dari atas ke bawah.

## Struktur Folder
02-ecommerce-indonesia/
├── data/
│   ├── raw/
│   │   ├── olist_orders_dataset.csv
│   │   ├── olist_customers_dataset.csv
│   │   ├── olist_order_items_dataset.csv
│   │   ├── olist_order_payments_dataset.csv
│   │   ├── olist_order_reviews_dataset.csv
│   │   ├── olist_products_dataset.csv
│   │   ├── olist_sellers_dataset.csv
│   │   └── product_category_name_translation.csv
│   ├── viz1_tren_bulanan.png
│   ├── viz2_top_kategori.png
│   ├── viz3_pembayaran.png
│   └── viz4_keterlambatan.png
└── notebooks/
└── analisis.ipynb

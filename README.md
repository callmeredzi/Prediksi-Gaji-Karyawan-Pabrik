# Prediksi Gaji Karyawan Pabrik

Proyek ini memprediksi gaji karyawan pabrik menggunakan **Regresi Linier** berdasarkan data performa dan demografi karyawan.

## Dataset

File: `data/Data_Karyawan_Pabrik.csv` — **420 data karyawan** dengan kolom:

| Kolom | Deskripsi |
|-------|-----------|
| `id_karyawan` | ID unik (KRY-XXXX) |
| `nama_karyawan` | Nama karyawan |
| `departemen` | Produksi, Logistik, Gudang, Maintenance, Quality Control |
| `jabatan` | Operator, Teknisi, Admin, Supervisor |
| `skor_kinerja` | Skor kinerja (60–99) |
| `jam_lembur` | Jam lembur per bulan (0–49) |
| `persentase_target` | Pencapaian target (70–99%) |
| `umur` | Umur karyawan (20–54 tahun) |
| `lama_bekerja` | Lama bekerja (1–35 tahun) |
| `gaji` | Gaji dalam Rupiah **(target prediksi)** |

## Alur Notebook

Notebook: `notebooks/Prediksi_Gaji_Pabrik.ipynb`

1. **Memuat dataset** dari GitHub repository
2. **EDA** — Heatmap korelasi antar fitur numerik
3. **Training** — Regresi Linier dengan split 80:20 (fitur: `skor_kinerja`, `jam_lembur`, `persentase_target`, `umur`, `lama_bekerja`)
4. **Evaluasi** — MAE, RMSE, R²
5. **Prediksi** — Estimasi gaji untuk data karyawan baru

## Hasil Model

| Metrik | Nilai |
|--------|-------|
| R² | **0.9797** |
| MAE | Rp 160.078 |
| RMSE | Rp 206.589 |

## Cara Pakai

### Clone Repository

```bash
git clone https://github.com/callmeredzi/Prediksi-Gaji-Karyawan-Pabrik.git
cd Prediksi-Gaji-Karyawan-Pabrik
```

### Jalankan Notebook

Buka `notebooks/Prediksi_Gaji_Pabrik.ipynb` di [Google Colab](https://colab.research.google.com/) atau Jupyter Notebook, lalu jalankan semua sel.

> Dataset sudah dimuat langsung dari GitHub, tidak perlu upload manual.

### Install Dependencies (jika lokal)

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Teknologi

Python · Pandas · NumPy · Matplotlib · Seaborn · Scikit-learn

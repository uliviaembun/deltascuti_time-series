# Photometric Observation and Time-Series Analysis of GP Andromedae

Proyek ini merupakan penelitian astrofisika pengamatan yang berfokus pada analisis *time-series* dan fotometri dari **GP Andromedae**, sebuah bintang variabel *Delta Scuti* dengan amplitudo tinggi. 

Tujuan utama dari penelitian ini adalah membangun kurva cahaya (*light curve*) dalam domain fase dan mengekstraksi nilai periode pulsasi bintang secara presisi menggunakan data pengamatan dari Teleskop ITB-UNDANA. Proyek ini mendemonstrasikan penerapan teknik analisis data saintifik, pengolahan sinyal, dan pemodelan regresi non-linear menggunakan Python.

## Metodologi Analisis
Penelitian ini mencakup tahapan pengolahan data astronomi sebagai berikut:
- **Fotometri Diferensial:** Menghitung selisih fluks antara bintang target (GP Andromedae) dan bintang pembanding (AG+2295) untuk mengeliminasi efek gangguan atmosfer dan instrumen.
- **Time-Series Analysis:** Menerapkan algoritma **Lomb-Scargle Periodogram** untuk mendeteksi frekuensi dominan dan menentukan periode pulsasi bintang dari data deret waktu yang tidak beraturan (*unevenly sampled data*).
- **Phase Folding:** Mentransformasi waktu pengamatan (Julian Date) ke dalam domain fase (0 hingga 1) berdasarkan periode yang ditemukan untuk memvisualisasikan siklus pulsasi secara utuh.
- **Curve Fitting:** Memodelkan kurva cahaya hasil observasi menggunakan fungsi harmonik dengan library `scipy.optimize` untuk memvalidasi pola variasi magnitudo.

## Hasil Utama
- Bintang GP Andromedae terkonfirmasi memiliki variasi magnitudo sebesar **ΔV = 0.6 mag**.
- Algoritma Lomb-Scargle berhasil mendeteksi periode pulsasi yang sangat singkat, yaitu sekitar **0.0787 hari** (kurang lebih 1.8 jam).
- Model kurva cahaya yang dibangun sangat cocok (*fit*) dengan data observasi, merepresentasikan karakteristik asimetris yang khas dari bintang variabel tipe *Delta Scuti*.

## Teknologi & Library
Proyek ini dikembangkan menggunakan bahasa pemrograman Python dengan *library* analisis data saintifik:
- `pandas` & `numpy`: Manipulasi data dan komputasi numerik.
- `astropy.timeseries`: Pengolahan data deret waktu astronomi (Lomb-Scargle).
- `scipy.optimize`: Penyesuaian kurva matematis non-linear.
- `matplotlib`: Visualisasi grafik ilmiah (*light curve* dan periodogram).

## Struktur Repository
- `laporan-riset.pdf`: laporan penelitian berupa paper komprehensif yang berisi landasan teori, parameter instrumen observasi, dan pembahasan astrofisika.
- `presentation.pdf`: ringkasan penelitian dalam bentuk presentasi visual.
- `main-notebook.ipynb`: *source code* berupa yang memuat seluruh proses *data loading*, perhitungan Lomb-Scargle, *phase folding*, dan visualisasi kurva cahaya.

## Penulis
**Ulivia Embun Tresna Wardani**


*Fakultas Matematika dan Ilmu Pengetahuan Alam*
*Institut Teknologi Bandung (2024)*

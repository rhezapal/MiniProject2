# MiniProject2
Investigate Business Hotel using Data Visualization - Rakamin Academy

## Introduction
“Sangat penting bagi suatu perusahaan untuk selalu menganalisa performa bisnisnya. Pada kesempatan kali ini, kita sebagai data analis akan lebih mendalami bisnis dalam bidang perhotelan. Fokus yang kita tuju adalah untuk mengetahui bagaimana perilaku pelanggan kita dalam melakukan pemesanan hotel, dan hubungannya terhadap tingkat pembatalan pemesanan hotel. Hasil dari insight yang kita temukan akan kita sajikan dalam bentuk data visualisasi agar lebih mudah dipahami dan bersifat lebih persuasif. ”

## Task
1. Data Exploratory Analysis and Data Preprocessing
2. Data Visualization Monthly Hotel Booking Analysis Based on Hotel Type
3. Data Visualization Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates
4. Impact Analysis of Lead Time on Hotel Bookings Cancellation Rate

### 1. Data Exploratory Analysis and Data Preprocessing
- Hal yang dilakukan : 
1. Handling Null Value :
2. Children : diisi modus
3. City : diisi Unknown
4. Agent : didrop
5. Company : didrop
6. Meal : Nilai Undefined diganti No Meal

### 2. Data Visualization Monthly Hotel Booking Analysis Based on Hotel Type
- Hal yang dilakukan : dilakukan pengelompokan jumlah booking berdasarkan bulan dan tahun dari masing-masing jenis hotel, khusus tahun kita hitung unique, Pada bulan September dan Oktober, jumlah tahun ada 3 , sehingga kita normalisasi. Kita hitung jumlah rata-rata booking per bulan. Untuk Visualisasi : nama bulan kita ambil 3 karakter dari depan dengan teknik slicing, kemudian divisualisasikan.
- Intrepretasi : Kedua jenis hotel mengalami peningkatan jumlah booking pada periode Juni-Juli dan Periode Desember. Peningkatan jumlah booking pada periode Juni-Juli berkaitan dengan liburan semesteran anak sekolah, sedangkan Periode Desember berkaitan dengan liburan natal dan tahun baru.

### 3. Data Visualization Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates.
- Hal yang dilakukan : 
1. Melakukan filtering jumlah reservasi yang cancel, digrup berdasarkan bulan dan jenis hotel
2. Melakukan agregasi jumlah reservasi per bulan dari masing-masing hotel untuk melihat jumlah total reservasi.
melakukan merge, dan agregasi kembali untuk mendapatkan ratio reservasi yang cancel dibandingkan total reservasi. kemudian divisualisasikan.
3. Melakukan agregasi, dengan menambahkan jumlah hari stay weekeend + weekday
4. Melakukan gruping berdasarkan bulan, dari masing-masing jenis hotel. didapatkan rata-rata jumlah hari
- Intrepretasi :
1. Berdasarkan durasi lama menginap : Pada jenis Resort Hotel, pengunjung menginap paling lama 5-6 hari pada bulan Agustus. Durasi tersebut paling lama di antara bulan lainnya. Hal ini berkaitan dengan libur sekolahan,
2. Sedangkan untuk jenis City Hotel, pengunjung rata-rata menginap selama 3 hari sepanjang tahun. Tidak terjadi peningkatan yang signifikan terkait lama durasi menginap.
3. Tetapi perlu diingat, tingkat cancel rate pada hotel Resort juga meningkat pada musim liburan, tercatat tingkat cancel rate pada bulan Agustus (32%) meningkat dibanding bulan-bulan sebelumnya sampai mencapai puncaknya pada bulan Oktober (33%).
4. Tingkat cancel rate pada Resort Hotel cenderung berfluktuasi, berbeda dengan City Hotel yang cenderung bertahun di angka 35-45% sepanjang tahunnya. Tetapi perlu dicatat, tingkat cancelled rate City Hotel cukup tinggi.

## 4. Impact Analysis of Lead Time on Hotel Bookings Cancellation Rate
- Hal yang sudah dilakukan:
1. membuat kategori baru untuk lead time dengan menggunakan np.where
2. menghitung jumlah reservasi cancel dan seluruhnya per kategori, dan dari masing-masing jenis hotel
3. membuat visualisasi
- Interpretasi:
1. Dari masing-masing kategori lead time, semakin lama lead time nya semakin tinggi pula ratio cancelnya. Hal ini berlaku untuk kedua jenis hotel.
2. Cancel ratio paling tinggi terjadi pada pelanggan dengan lead time > 1 tahun, yakni > dari 70% pada city hotel, dan 45% pada resort hotel.

#  [Final Project Studi Independen Startup Campus x Kampus Merdeka] | Customer Analytics - Churn Prediction Home Credit

## Tim The Revolutionaries
🧞‍ Suprianto Dharma Sitompul - Institut Teknologi Del (Ketua Tim)
<br>
🧞‍ Sri Indrayani - Universitas Brawijaya (Anggota) 
<br>
🧞‍ Winona Timothea - Institut Teknologi Bandung (Anggota)
<br>
🧞‍ Zalfa Nurjihan - Universitas Pendidikan Indonesia (Anggota)

## Business Understanding
Home Credit Group ingin memperluas penawaran ke lebih banyak pelanggan dengan tujuan untuk meningkatkan pendapatannya. Namun, semakin banyak pinjaman yang ditawarkan perusahaan, semakin besar pula resiko yang terjadi. Jika terjadi gagal bayar di antara pelanggan meningkat, maka perusahaan akan mengalami kerugian dalam ekspansinya. 
<br>
### `Goal`
Meminimalkan jumlah pemohon yang pinjaman kreditnya disetujui tetapi sebenarnya tidak mampu membayar kredit.
<br>
### `Objective`
Membuat model Machine Learning untuk memprediksi apakah pemohon dapat membayar pinjaman atau tidak, dengan mengunakan data historis aplikasi pinjaman.


## Dataset
Terdapat 6 dataset yang akan di analisis dan setiap dataset memiliki fitur-fitur yang banyak, sehingga berdasarkan dataset tersebut kami melakukan eksplorasi untuk mendapatkan fitur-fitur yang penting. Kami melakukan eksplorasi dari setiap dataset kemudian mengambil fitur-fitur yang informatif dari setiap dataset kemudian dilakukan aggregation ke dataset lain yang sudah di pilih juga fiturnya.

<img width="338" alt="image" src="https://github.com/supriantositompul/CustomerAnalytics-ChurnPrediction/assets/71377466/d478f799-1fff-433b-a5ee-86d48d3e8e91">

## Data Understanding
<img width="613" alt="image" src="https://github.com/supriantositompul/CustomerAnalytics-ChurnPrediction/assets/71377466/26b8683b-7561-4b71-8261-4d799bc8f301">
<img width="587" alt="image" src="https://github.com/supriantositompul/CustomerAnalytics-ChurnPrediction/assets/71377466/6a96658e-b845-4d7e-a024-c8f9133716e0">
<img width="591" alt="image" src="https://github.com/supriantositompul/CustomerAnalytics-ChurnPrediction/assets/71377466/804b054b-6611-4c19-93cd-f6b2ad426679">

## Feature Engineering
<img width="608" alt="image" src="https://github.com/supriantositompul/CustomerAnalytics-ChurnPrediction/assets/71377466/da5d37ed-cdc0-497d-bc1a-52819c81cf7b">

## Data Modeling
<img width="604" alt="image" src="https://github.com/supriantositompul/CustomerAnalytics-ChurnPrediction/assets/71377466/f9a2b413-61cd-4ef0-bb5f-d0b3c5e5a3b2">

## Model Selection
Setelah melakukan evaluasi dan perbandingan dengan model lain, kami mendapatkan model **LightGBM** dengan performa yang lebih baik yang ditandai dengan Recall, Precission, dan F1-Score yang lebih baik. Berdasarkan uji ROC-AUC dan setelah divalidasi dengan threshold **LightGBM** tetap memiliki kinerja model yang lebih baik dibandingkan model lain. 

## Predict to Actual
<img width="370" alt="image" src="https://github.com/supriantositompul/CustomerAnalytics-ChurnPrediction/assets/71377466/ea9e7e4b-a564-429a-afb2-898799d7d1fc">

`Insight dari hasil prediksi dan aktual:`
<br>
1. Terdapat 267 data yang terprediksi dengan benar, baik sebagai orang yang sanggup membayar (prediksi 1 dan aktual 1) maupun tidak sanggup membayar (prediksi 0 dan aktual 0).
2. Terdapat 33 data yang terprediksi salah, yaitu 10 data yang salah terprediksi sebagai orang yang tidak sanggup membayar padahal aktualnya sanggup (prediksi 1 dan aktual 0), dan 23 data yang salah terprediksi sebagai orang yang sanggup membayar padahal aktualnya tidak sanggup (prediksi 0 dan aktual 1).
3. Model memiliki akurasi sebesar 90.0%, yang menunjukkan bahwa sebagian besar prediksi model sesuai dengan aktualnya.

## Insight from Dataset
Berdasarkan dataset yang telah dieksplorasi, dapat diketahui bahwa persentase tertinggi dari pendidikan customer yang mengajukan pinjaman adalah Secondary/Secondary Special dengan persentase 71% dan diikuti dengan Higher Education dengan persentase 24.3%.

Di sisi lain, mayoritas customer yang sanggup bayar memiliki jenis pekerjaan  Businessman beserta jumlah pendapatan yang tinggi dan jenis tempat tinggal customer adalah Rumah/Apartment dengan persentase 88.7%.

## Dashboard 
![The Revolutionaries_Dashboard_page-0001](https://github.com/supriantositompul/Customer_Analytics-Churn_Prediction/assets/71377466/017e5e45-2b52-4f75-9090-ecadd1a20b3d)
![The Revolutionaries_Dashboard_page-0002](https://github.com/supriantositompul/Customer_Analytics-Churn_Prediction/assets/71377466/82fc1834-ca79-4783-9b70-d4b612574943)

## Rekomendasi 
1. Perusahaan Home Credit Group dapat memberikan penawaran baru berupa paket pinjaman pelajar dengan bunga yang rendah.
2. Fokus pada segmen adult dan old karena berdasarkan data historis kedua rentang usia ini berpotensi tinggi churn.
3. Jika perusahaan ingin menyaring peminjam mereka harus lebih memperhatikan bidang-bidang seperti jenjang pendidikan, sumber pendapatan, dan tempat tinggal.
4. Perusahaan harus mempertimbangkan peminjam yang memiliki pinjaman ke perusahaan lain dan juga mempertimbangkan pinjaman sebelumnya yang belum diselesaikan.



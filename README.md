# E-COMMERCE CHURN PREDICTION

## Latar Belakang 
Churn Rate merupakan angka yang dapat menunjukkan tingkat persentase di mana perusahaan kehilangan pelanggan atau pendapatannya karena berbagai keadaan. Pada perusahaan ini dalam satu bulan terakhir churn rate mencapai lebih dari 5%* (standar Churn Rate perusahaan e-Commerce). Sehingga dampak yang dihasilkan akibat Churn Rate tersebut adalah adanya potensi kehilangan Revenue. Maka berdasarkan latar belakang tersebut penting untuk menurunkan churn rate tersebut dengan membuat model untuk mendeteksi pelanggan yang berpotensi berhenti berlangganan.

## Pertanyaan Riset
Bagaimana dampak terhadap perusahaan dari sebelum adanya model dan setelah penerapan model tersebut

## Data dan Asumsi
Churn Rate merupakan angka yang dapat menunjukkan tingkat persentase di mana perusahaan kehilangan pelanggan atau pendapatannya karena berbagai keadaan. Pada perusahaan ini dalam satu bulan terakhir churn rate mencapai 16,83%  yaitu lebih besar dari 5%* (standar Churn Rate perusahaan e-Commerce). Sehingga dampak yang dihasilkan akibat Churn Rate tersebut adalah adanya potensi kehilangan Revenue sebesar  $2.400.106. Maka berdasarkan latar belakang tersebut penting untuk menurunkan churn rate tersebut dengan membuat model untuk mendeteksi pelanggan yang berpotensi berhenti berlangganan (churn) dengan target churn rate <5%.

## Analisis Data
<ol> 
<li>Exploratory Data Analysis
<ul>
<li>Data terdiri dari 5630 baris</li>
<li>Tidak terdapat tipe data dan nama kolom yang kurang sesuai</li>
<li>Tampak beberapa kolom masih memiliki null/missing values (Non-Null Count < jumlah baris) diantaranya Tenure, WarehouseToHome, HourSpendOnApp, OrderAmountHikeFromlastYear, CouponUsed, OrderCount, DaySinceLastOrder</li>
<li>Kolom churn, Tenure, WarehouseToHome, HourSpendOnApp, NumberOfDeviceRegistered, SatisfactionScore, dan OrderAmountHikeFromlastYear sudah mendekati distribusi normal (median tidak jauh berbeda dengan mean)</li>
<li>Kolom CityTier, NumberOfAddress, CouponUsed, OrderCount, DaySinceLastOrder, dan CashbackAmount tampak skew ke kanan (long-right tail).</li>
<li>Kolom Churn dan Complain ternyata bernilai boolean/binary</li>
<li>Outlier terlihat utamanya pada kolom CouponUsed, OrderCount, CashbackAmount dan DaySinceLastOrder</li>
<li>Kolom HourSpendApp, NumberOfDeviceRegistered, SatisfactionScore, dan OrderAmountHikeFromlastYear tampak sudah mendekati distribusi normal</li>
</ul>
</li>

<li>Data Pre-Processing
<ul>
<li>Mengatasi null value menggunakan metode imputasi dengan nilai modus atau median</li>
<li>Menghapus data duplikasi</li>
<li>Mengatasi data outlier menggunakan metode IQR</li>
<li>Melakukan feature transformation dan standarization</li>
<li>Melakukan Feature Encoding pada beberapa value untuk menghindari makna duplikasi</li>
<li>Menghapus kolom yang tidak relevan</li>
<li>Menambah kolom baru yaitu OtherRevenue yang merupakan perkalian dari cashbackamount dengan 0.05 (nilai standar)</li>
</ul>
</li>

<li>Modelling
<ul>
<li>Membagi data menjadi data train dan data test dengan proporsi 70% dan 30%</li>
<li>Mengatasi data imbalance menggunakan Smote</li>
<li>Menentukan metriks evaluasi model yaitu recall dan precision karena berfokus untuk mengurangi false negatif</li>
<li>Menggunakan 6 model yaitu namun setelah dibandingkan hasilnya model fokus pada XGBosst</li>
</ul>
</li>
</ol>

## Simpulan
Dampak dari setelah adanya penerapan model yaitu Churn Rate menurun dari semua 16,83% menjadi 2.39% dan dapat menyelamatlan revenue  sebesar $1.039.381 atau 8,77% dari total revenue

## Saran
<ol>
<li>Memberikan welcoming gift untuk pengguna baru (gratis ongkir, cashback, promo).</li>
<li>Penawaran membership dengan keuntungan yang lebih menarik.</li>
<li>Memberikan rekomendasi produk sesuai dengan kategori gender, umur, marital status.</li>
<li>Pengembangan aplikasi agar lebih user friendly.</li>
<li>Meningkatkan kualitas produk yang dijual.</li>
<li>Meningkatkan standar layanan yang diberikan.</li>
<li>Membuat layanan pengaduan yang cepat, tanggap, dan solutif.</li>
<li>Proactive dalam menanggapi Feedback</li>
<li>Menyediakan fitur verifikasi barang original.</li>
<li>Menyediakan jasa asuransi produk.</li>
<li>Meningkatkan kualitas produk yang dijual. </li>
<li>Menawarkan harga yang bersaing.</li>
</ol>

# Proyek Analisis Data: Brazilian E-Commerce (Olist)

## Deskripsi Proyek
Proyek ini melakukan analisis mendalam terhadap **Brazilian E-Commerce Public Dataset by Olist**. Tujuan utamanya adalah untuk mengekstrak informasi strategis mengenai performa kategori produk, perilaku pembayaran pelanggan, persebaran geografis konsumen, serta faktor-faktor logistik yang memengaruhi kepuasan pelanggan (*review score*).

Analisis ini mencakup seluruh siklus pengolahan data, mulai dari *Data Wrangling*, *Exploratory Data Analysis (EDA)*, hingga tahap *Visualisasi* dan pembuatan dashboard menggunakan streamlit.

## Dataset
Dataset yang digunakan berasal dari Kaggle yang disediakan oleh Olist, toko departemen terbesar di pasar Brasil. Dataset ini mencakup informasi 100.000 pesanan dari tahun 2016 hingga 2018.

* **Sumber Dataset:** [Kaggle - Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

## Pertanyaan Bisnis
1. Apa saja 10 kategori produk dengan jumlah Penjualan Terbesar?
2. Metode pembayaran apa yang paling sering digunakan oleh pelanggan?
3. Apa saja 10 kota dengan jumlah pelanggan yang melakukan pemesanan terbanyak?
4. Bagaimana pengaruh keterlambatan pengiriman terhadap kepuasan pelanggan (*review score*)?
5. Faktor apa saja yang memengaruhi lama waktu pengiriman pesanan?

## Cara Menjalankan Proyek
1. **Clone the repository**  
   Clone repositori ini ke komputer lokal Anda menggunakan git:
   ```bash
   git clone [https://github.com/adha20/Machine-Learning-Assignment-Muhammad-Adha.git](https://github.com/adha20/Machine-Learning-Assignment-Muhammad-Adha.git)

2. **Set up a virtual environment** (Optional)  
   Sangat disarankan untuk menggunakan virtual environment agar library proyek ini terpisah dari lingkungan Python sistem Anda:

   ```bash
   python -m venv env
   ```

   Aktifkan virtual environment:

   Windows:

   ```bash
   .\env\Scripts\activate
   ```

   Unix atau MacOS:

   ```ls
   source env/bin/activate
   ```

4. **Install the dependencies**  
  Masuk ke direktori proyek dan instal semua library yang diperlukan menggunakan pip:

   ```bash
   pip install -r requirements.txt
   ```

5. **Run the project**  
  - Jupyter Notebook: Anda dapat menjalankan analisis data lengkap dengan membuka file ML_Muhammad_Adha.ipynb dan menekan tombol "Run All".

- Dashboard Streamlit: Untuk menjalankan dashboard, ketikkan perintah berikut di terminal:
  ```Bash
  streamlit run dashboard.py
  ```


##  Hasil Analisis

### Kesimpulan Pertanyaan 1:
Berdasarkan analisis Top 10 kategori produk dengan jumlah pembelian terbanyak, kategori yang paling sering dibeli oleh pelanggan adalah:
1. bed_bath_table: 11115 order
2. health_beauty: 9670 order
3. sports_leisure: 8641 order
4. furniture_decor: 8334 order
5. computers_accessories: 7827 order
6. housewares: 6964 order
7. watches_gifts: 5951 order
8. telephony: 4545 order
9. garden_tools: 4347 order
10. auto: 4235 order

Hasil ini menunjukkan bahwa kategori bed_bath_table, health_beauty, dan sports_leisure mendominasi jumlah transaksi, sehingga menjadi kontributor utama terhadap total penjualan di platform e-commerce.

Dominasi kategori tersebut mengindikasikan bahwa konsumen memiliki kecenderungan kuat untuk membeli produk yang berkaitan dengan kebutuhan rumah tangga, perawatan diri, dan gaya hidup sehari-hari. Produk dalam kategori ini umumnya bersifat rutin, repeatable, dan memiliki tingkat kebutuhan yang tinggi, sehingga mendorong frekuensi pembelian yang lebih besar dibandingkan kategori lainnya.

Dari sisi bisnis, kategori-kategori dengan volume transaksi tinggi ini dapat dijadikan fokus utama strategi pemasaran dan operasional, seperti:
- Prioritas promosi dan diskon musiman
- Bundling produk untuk meningkatkan nilai transaksi
- Optimalisasi stok dan logistik guna menghindari kehabisan barang

Sementara itu, kategori dengan volume pembelian lebih rendah seperti telephony, garden_tools, dan auto tetap memiliki potensi untuk dikembangkan melalui strategi pemasaran yang lebih spesifik atau segmentasi pelanggan yang lebih tepat.

---

## Kesimpulan Pertanyaan 2:  
Berdasarkan hasil analisis, metode pembayaran yang paling sering digunakan oleh pelanggan adalah:
1.  Kartu Kredit: 76795 transaksi
2.  Boleto: 19784 transaksi
3.  Voucher: 5775 transaksi
4.  Kartu Debit: 1529 transaksi  

Hasil ini menunjukkan bahwa kartu kredit merupakan metode pembayaran yang paling dominan digunakan oleh pelanggan, dengan jumlah transaksi yang jauh lebih tinggi dibandingkan metode lain seperti boleto, voucher, dan kartu debit.

Dominasi penggunaan kartu kredit mencerminkan beberapa hal penting. Pertama, hal ini menunjukkan tingkat kepercayaan pelanggan yang tinggi terhadap transaksi online, khususnya dalam penggunaan instrumen pembayaran non-tunai. Kedua, kartu kredit menawarkan kemudahan, fleksibilitas pembayaran, serta kemungkinan cicilan, yang membuatnya lebih menarik bagi pelanggan dalam melakukan pembelian di platform e-commerce.

Di sisi lain, metode boleto masih digunakan oleh sebagian pelanggan, yang mengindikasikan adanya segmen konsumen yang lebih memilih metode pembayaran non-kartu. Sementara itu, penggunaan voucher dan kartu debit relatif rendah, sehingga kontribusinya terhadap total transaksi tidak signifikan.

Temuan ini menegaskan bahwa ketersediaan sistem pembayaran kartu kredit yang aman, stabil, dan andal merupakan faktor krusial bagi platform e-commerce. Selain itu, optimalisasi dan variasi metode pembayaran alternatif seperti boleto tetap penting untuk menjangkau segmen pelanggan yang lebih luas, sehingga dapat meningkatkan inklusivitas dan potensi konversi transaksi secara keseluruhan.

---

### Kesimpulan Pertanyaan 3:
Berdasarkan analisis jumlah pelanggan per kota, 10 kota dengan jumlah pelanggan terbanyak adalah:
1. São Paulo: 15.540 pelanggan
2. Rio de Janeiro: 6.882 pelanggan
3. Belo Horizonte: 2.773 pelanggan
4. Brasília: 2.131 pelanggan
5. Curitiba: 1.521 pelanggan
6. Campinas: 1.444 pelanggan
7. Porto Alegre: 1.379 pelanggan
8. Salvador: 1.245 pelanggan
9. Guarulhos: 1.189 pelanggan
10. São Bernardo do Campo: 938 pelanggan

Hasil ini menunjukkan bahwa São Paulo mendominasi secara signifikan dibandingkan kota lainnya, dengan jumlah pelanggan lebih dari dua kali lipat kota peringkat kedua (Rio de Janeiro). Hal ini mengindikasikan bahwa São Paulo merupakan pusat pasar utama bagi platform e-commerce, baik dari sisi jumlah pelanggan maupun potensi transaksi.

Kota-kota besar lain seperti Rio de Janeiro, Belo Horizonte, dan Brasília juga menunjukkan konsentrasi pelanggan yang tinggi, yang menandakan bahwa aktivitas e-commerce sangat terpusat di wilayah urban dan pusat ekonomi.

Wilayah dengan konsentrasi pelanggan tinggi dapat diprioritaskan untuk:
-  Optimalisasi lokasi gudang dan fulfillment center
- Peningkatan kapasitas distribusi dan armada logistik
- Penyediaan layanan pengiriman yang lebih cepat atau premium

Fokus pada kota-kota utama berpotensi meningkatkan efisiensi logistik, menurunkan waktu pengiriman, dan meningkatkan kepuasan pelanggan.

---

### Kesimpulan Pertanyaan 4:
Berdasarkan hasil analisis hubungan antara keterlambatan pengiriman dan kepuasan pelanggan menunjukkan bahwa keterlambatan pengiriman terbukti memiliki pengaruh signifikan terhadap kepuasan pelanggan, yang diukur melalui review score.

Secara kuantitatif, pesanan yang dikirim tepat waktu memiliki rata-rata review score sebesar 4,26, sedangkan pesanan yang terlambat hanya memperoleh rata-rata review score sebesar 2,43. Perbedaan ini menunjukkan penurunan kepuasan pelanggan yang cukup besar ketika terjadi keterlambatan pengiriman.

Selain itu, hasil analisis korelasi menunjukkan adanya korelasi negatif yang cukup berarti antara status keterlambatan pengiriman dan review score, dengan nilai korelasi sebesar -0,39. Nilai ini mengindikasikan bahwa semakin besar kemungkinan pesanan terlambat, maka semakin rendah penilaian yang diberikan oleh pelanggan.

Temuan ini menegaskan bahwa ketepatan waktu pengiriman merupakan faktor krusial dalam menjaga kepuasan pelanggan. Keterlambatan pengiriman tidak hanya berdampak pada penurunan penilaian produk, tetapi juga berpotensi menurunkan loyalitas pelanggan serta merusak reputasi penjual di platform e-commerce. Oleh karena itu, optimalisasi proses logistik dan pengiriman menjadi aspek penting dalam meningkatkan kualitas layanan dan pengalaman pelanggan secara keseluruhan.

---

### Kesimpulan Pertanyaan 5:
Berdasarkan feature importance dari model Random Forest, faktor yang paling memengaruhi lama waktu pengiriman adalah freight_value. Variabel ini merepresentasikan kompleksitas logistik, seperti jarak pengiriman, berat dan ukuran paket, biaya transportasi, serta kemungkinan jenis layanan logistik yang digunakan.

Nilai freight_value yang lebih rendah kemungkinan mencerminkan penggunaan layanan pengiriman standar dengan waktu pengiriman yang relatif lebih panjang, sementara nilai freight_value yang lebih tinggi dapat mengindikasikan penggunaan layanan logistik yang lebih cepat atau prioritas. Hal ini menjelaskan mengapa freight_value menjadi faktor paling dominan dalam menentukan durasi pengiriman.

Selain itu, berat produk (product_weight_g) dan lokasi pelanggan (customer_state) juga memiliki pengaruh yang cukup besar, menunjukkan bahwa paket yang lebih berat serta pengiriman ke wilayah tertentu cenderung membutuhkan waktu lebih lama.

Sebaliknya, dimensi fisik produk (panjang, tinggi, dan lebar) memiliki pengaruh yang relatif lebih kecil, menandakan bahwa faktor logistik makro dan berat paket lebih dominan dalam menentukan durasi pengiriman.

Hasil analisis ini mendukung pengambilan keputusan berbasis data dalam upaya optimasi proses logistik. Dengan mengidentifikasi freight_value sebagai faktor paling dominan, perusahaan dapat memfokuskan strategi pada pemilihan layanan pengiriman yang tepat, pengelolaan biaya logistik, serta penyesuaian estimasi waktu pengiriman. Selain itu, pengaruh signifikan dari berat produk dan lokasi pelanggan memberikan dasar yang kuat bagi perusahaan untuk melakukan segmentasi produk, optimalisasi rute distribusi, serta penempatan gudang yang lebih strategis. Pendekatan ini memungkinkan perusahaan meningkatkan efisiensi operasional sekaligus menjaga kepuasan pelanggan melalui pengiriman yang lebih andal.


## Dashboard
<img width="1277" height="564" alt="Screenshot 2025-12-27 141035" src="https://github.com/user-attachments/assets/bd714ad1-1a3a-4445-a414-8a385e8e35e9" />

<img width="1276" height="499" alt="Screenshot 2025-12-27 141055" src="https://github.com/user-attachments/assets/dbce3ad1-4ab3-4499-b299-b2b739e653a3" />

<img width="1275" height="557" alt="Screenshot 2025-12-27 141117" src="https://github.com/user-attachments/assets/d1d43687-5379-4e29-ae97-dc198ac8a2e0" />


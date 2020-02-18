<h2>Tugas 1 Big Data </h2>

1.  <b>Business Understanding</b><br>
    Di dataset ini, kita dapat memprosesnya dan mendapatkan informasi tentang record penjualan tesla yang melonjak jauh harganya di akhir tahun 2019 <br>

2.  <b>Data Understanding</b> <br>
    Dalam dataset ini ada 2416 record dan 7 kolom, dengan kolom Date menjadi acuannya (indeks). <br>
    Kolom Open adalah harga awal dalam pelelangan. <br>
    Kolom High adalah harga termahal. <br>
    Kolom Low adalah harga terendah. <br>
    Kolom Close adalah harga terakhir/penutup. <br>
    Kolom Adj Close adalah harga terakhir yang sudah disesuaikan. <br>
    Kolom Volume adalah volume trading hari itu. <br>
    <img src="/image/grafik_TSLA.png"><br>
3.  <b>Data Preparation</b><br>
    Dataset saya baca dengan CSV Reader, dan saya lakukan splitting.<br>
    <img src="/image/read_dataset_asli.png"><br>
    Untuk melakukan splitting, saya menggunakan column splitter, dimana merupakan fungsi untuk membagi satu tabel menjadi dua tabel berbeda. <br>
    <img src="/image/split_dataset_asli.png"><br>
    Tabel pertama saya menggunakan kolom date, open, high, low. Sedangkan tabel kedua menggunakan kolom close, adj close, dan volume. <br>
    <img src="/image/split_dataset_asli_config.png"><br>
    Tabel pertama saya write ke csv, dengan CSV Writer.<br>
    Tabel kedua saya write ke database, dengan database writer.<br>
    <img src="/image/write_dataset_split.png"><br>
    Untuk melakukan database writer, saya juga harus melakukan koneksi ke database. Karena saya menggunakan mysql, maka saya gunakan MySQL Connector.<br>
    <img src="/image/MySQL_config.png"><br>
    Preparasi data selesai.<br>
4.  <b>Modelling</b><br>
    Setelah dilakukan splitting, untuk membaca file csv, saya menggunakan CSV Reader.<br>
    Untuk membaca table di database, saya menggunakan Database Reader.<br>
    <img src="/image/read_split_dataset.png"><br>
    Setelah saya baca dua tabel berbeda tersebut, saya lakukan append ke kedua tabel tersebut.<br>
    Append tersebut dilakukan dengan row id yang identik, karena dua tabel mempunyai row id yang sama.<br>
    <img src="/image/append_split_dataset.png"><br>
5.  <b>Evaluation</b><br>
    Append telah berhasil dilakukan. Untuk mengecek apakah append berhasil atau tidak, kita bisa mengeceknya apakah sama dengan dataset asli atau bukan. Dan ternyata hasilnya sama, dengan jumlah kolom dan baris yang sama.<br>
    <img src="/image/jumlah_kolom_baris_dataset_akhir.png"><br>
    <img src="/image/jumlah_kolom_baris_dataset_asli.png"><br>
6.  <b>Deployment</b><br>
    Simpan file dalam database dengan database writer dan simpan dalam csv dengan CSV writer.<br>
    <img src="/image/write_dataset_split.png"><br>

Sekian, terima kasih.
    

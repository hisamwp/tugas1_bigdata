<h2>Tugas 1 Big Data </h2>

1.  <b>Business Understanding</b><br>
    Di dataset ini, kita dapat memprosesnya dan mendapatkan informasi tentang record penjualan tesla yang melonjak jauh harganya di akhir tahun 2019

2.  <b>Data Understanding</b> <br>
    Dalam dataset ini ada 2416 record dan 7 kolom, dengan kolom Date menjadi acuannya (indeks). <br>
    Kolom Open adalah harga awal dalam pelelangan. <br>
    Kolom High adalah harga termahal. <br>
    Kolom Low adalah harga terendah. <br>
    Kolom Close adalah harga terakhir/penutup. <br>
    Kolom Adj Close adalah harga terakhir yang sudah disesuaikan. <br>
    Kolom Volume adalah volume trading hari itu. <br>
    <img src="/image/grafik_TSLA.png">
3.  <b>Data Preparation</b><br>
    Dataset saya baca dengan CSV Reader, dan saya lakukan splitting.
    <img>
    Untuk melakukan splitting, saya menggunakan column splitter, dimana merupakan fungsi untuk membagi satu tabel menjadi dua tabel berbeda. <br>
    <img src=><br>
    Tabel pertama saya menggunakan kolom date, open, high, low. Sedangkan tabel kedua menggunakan kolom close, adj close, dan volume. <br>
    <img><br>
    Tabel pertama saya write ke csv, dengan CSV Writer.<br>
    <img><br>
    Tabel kedua saya write ke database, dengan database writer.<br>
    <img><br>
    Untuk melakukan database writer, saya juga harus melakukan koneksi ke database. Karena saya menggunakan mysql, maka saya gunakan MySQL Connector.<br>
    <img><br>
    Preparasi data selesai.<br>
4.  

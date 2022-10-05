# langkah-langkah Working-with-Attributes-QGIS3-
Langkah Membuat Working with Attributes (QGIS3)
1.	Pertama kita download terlebih dahulu https://www.qgistutorials.com/downloads/ne_10m_populated_places_simple.zip
2.	Temukan file yang kita download  ne_10m_populated_places_simple.zip di Browser QGIS dan perluas. Pilih file ne_10m_populated_places_simple.shp dan seret ke kanvas.
3.	Lapisan baru ne_10m_populated_places_simple sekarang akan dimuat di QGIS dan Anda akan melihat banyak titik yang mewakili tempat-tempat berpenduduk di dunia. Tampilan default di kanvas QGIS menunjukkan geometri lapisan GIS. Setiap poin juga memiliki atribut terkait. Mari kita lihat mereka. Temukan Toolbar Atribut. Toolbar ini berisi banyak alat yang berguna untuk memeriksa, melihat, memilih, dan memodifikasi atribut lapisan.
4.	Klik tombol Identifikasi pada Toolbar Atribut. Setelah alat dipilih, klik pada titik mana pun di kanvas. Atribut terkait dari titik tersebut akan ditampilkan di panel Identifikasi Hasil baru. Setelah Anda selesai menjelajahi atribut dari poin yang berbeda, Anda dapat mengklik tombol Tutup.
5.	Klik tombol Buka Tabel Atribut pada Toolbar Atribut. Anda juga dapat mengklik kanan layer ne_10m_populated_places_simple dan memilih Open Attribute Table.
6.	You can scroll horizontally and locate the pop_max column. This field contains the population of the associated place. You can click twice on the field header to sort the column in descending order.
7.	Sekarang kita siap untuk melakukan kueri kita pada atribut ini. QGIS menggunakan ekspresi seperti SQL untuk melakukan kueri. Klik Pilih fitur menggunakan tombol ekspresi.
8.	Di jendela Pilih Menurut Ekspresi, perluas bagian Bidang dan Nilai dan klik ganda label pop_max. Anda akan melihat bahwa itu ditambahkan ke bagian ekspresi di bagian bawah. Jika Anda tidak yakin tentang nilai bidang, Anda dapat mengklik tombol Semua Unik untuk melihat apa nilai atribut yang ada dalam himpunan data. Untuk latihan ini, kami ingin menemukan semua fitur yang memiliki populasi lebih dari 1 juta. Jadi lengkapi ekspresi seperti di bawah ini dan klik Pilih Fitur lalu Tutup.
9.	Anda akan melihat bahwa beberapa baris dalam tabel atribut sekarang dipilih. Jendela label juga berubah dan menunjukkan jumlah fitur yang dipilih.
10.	Tutup jendela tabel atribut dan kembali ke jendela QGIS utama. Anda akan melihat bahwa subset poin sekarang diberikan dalam warna kuning. Ini adalah hasil dari kueri kami dan poin yang dipilih adalah poin yang memiliki nilai atribut pop_max lebih besar dari 10000000.
11.	Mari kita perbarui kueri kami untuk menyertakan syarat bahwa tempat tersebut juga harus menjadi modal selain memiliki populasi yang lebih besar dari 1 juta. Untuk masuk ke editor ekspresi dengan cepat, Anda bisa menggunakan tombol Pilih Fitur menurut Ekspresi di Toolbar Atribut.
12.	Bidang yang berisi data tentang huruf kapital adalah adm0cap. Nilai 1 menunjukkan bahwa tempat itu adalah modal. Kita dapat menambahkan kriteria ini ke ekspresi kita sebelumnya menggunakan dan operator. Masukkan ekspresi seperti di bawah ini dan klik Pilih Fitur lalu Tutup.
13.	Return to the main QGIS window. Now you will see a smaller subset of the points selected. This is the result of the second query and shows all places from the dataset that are country capitals as well as have population greater than 1 million.
14.	Sekarang kita akan mengekspor fitur yang dipilih sebagai layer baru. Klik kanan layer ne_10m_populated_places_simple dan pergi ke Export -> Save Selected Features As
15.	Anda dapat memilih format apa pun yang Anda sukai sebagai Format. Untuk latihan ini, kami akan memilih GeoJSON. GeoJSON adalah format berbasis teks yang digunakan secara luas dalam pemetaan web. Klik tombol ... di sebelah Nama file dan masukkan populated_capitals.geojson sebagai file output.
16.	The input data has many columns. You are able to choose only a subset of the original columns for export. Expand the Select fields to export and their export options section. Click Deselect All and check the name and pop_max columns. Click OK.
17.	Data input memiliki banyak kolom. Anda hanya dapat memilih subset dari kolom asli untuk diekspor. Perluas bagian Pilih bidang untuk diekspor dan opsi ekspornya. Klik Batal pilih Semua dan periksa nama dan kolom pop_max. Klik Oke.
18.	Layer baru populated_capitals akan dimuat di QGIS. Anda dapat menghapus centang pada layer ne_10m_populated_places_simple untuk menyembunyikannya dan melihat titik-titik dari layer yang baru diekspor.




<h1> Connecting & Renaming Table </h1>

1. Buka DBeaver lalu pilih sqlite<br>
<img src="/1_DB/Dokumentasi/img/sqlite.jpg"><br>

2. Buka newCensus.sqlite<br>
<img src="/1_DB/Dokumentasi/img/newcensus.jpg"><br>

3. Mengubah nama table dan menambahkan NRP didepan table.<br>
<img src="/1_DB/Dokumentasi/img/rtable1.jpg"><br>
<img src="/1_DB/Dokumentasi/img/rtable2.jpg"><br>

4. Lakukan hal ini untuk 2 table (ss13pme dan ss13hme)<br>

<h1> DB Connect</h1><br>
1. Execute SQLite Connector<br>
<img src="/1_DB/Dokumentasi/img/connect.jpg"><br>
2. Configure DB Table Selector dan pilih table. Lalu execute node tsb.<br>
<img src="/1_DB/Dokumentasi/img/insert1.jpg"><br>
3. Execute DB Reader dan Buka table<br>
<img src="/1_DB/Dokumentasi/img/dbread.jpg"><br>
<img src="/1_DB/Dokumentasi/img/result1.jpg"><br>

<h1> In DB Processing</h1><br>
1. Execute SQLite Connector<br>
<img src="/1_DB/Dokumentasi/img/connect.jpg"><br>
2. Pilih table yg akan digunakan dengan DB Table Selector<br>
<img src="/1_DB/Dokumentasi/img/select2.jpg"><br>
<img src="/1_DB/Dokumentasi/img/select3.jpg"><br>
3. Tambahkan Column Filter dan remove puma* dan pwgtp* pada tabel <br>
<img src="/1_DB/Dokumentasi/img/filter.jpg"><br>
4. Lakukan join antara 2 table sebelumnya dengan Joiner dan lakukan setting dengan serialno sebagai penanda<br>
<img src="/1_DB/Dokumentasi/img/joinserialno.jpg"><br>
5. Gunakan DB Reader. Hasil joiner sebagai berikut :
<img src="/1_DB/Dokumentasi/img/result2.jpg"><br>
6. Menambahkan Row Filter dan melakukan filter pada tabel dengan COW yang tidak NULL
<img src="/1_DB/Dokumentasi/img/filter1.jpg"><br>
7. Gunakan DB Reader untuk membaca hasil table
<img src="/1_DB/Dokumentasi/img/result3.jpg"><br>
8. Tambahkan Row Filter pada tabel dengan filter COW yang NULL
<img src="/1_DB/Dokumentasi/img/filter2.jpg"><br>
9. Gunakan DB Reader untuk membaca hasil table
<img src="/1_DB/Dokumentasi/img/result4.jpg"><br>
10. Tambahkan Node GroupBy dan kelompokkan berdasarkan jenis kelamin(sex) 
<img src="/1_DB/Dokumentasi/img/groupby.jpg"><br>
11. Gunakan DB Reader untuk membaca hasil table
<img src="/1_DB/Dokumentasi/img/result5.jpg"><br>
12. Sorting Umur scr descending dan ambil 10 besar (gunakan limit 10 pada sql statement)
<img src="/1_DB/Dokumentasi/img/sort.jpg"><br>
13. Gunakan DB Reader untuk membaca hasil table
<img src="/1_DB/Dokumentasi/img/result6.jpg"><br>

<h1> Modelling </h1>
1. Untuk data preparation hampir mirip dengan In DB Processing sampai ke percabangan row filter(cow is null dan cow is not null). <br>
2. Convert Number to String untuk cow IS NOT NULL <br>
3. Tambahkan column filter untuk menghapus row COW pada COW IS NULL <br> 
Gambar : 
<img src="/1_DB/Dokumentasi/img/modelling.jpg"><br>
4. Hasil dari tabel COW IS NOT NULL dan COW IS NULL<br>
<img src="/1_DB/Dokumentasi/img/cowisntnull.jpg"><br>
<img src="/1_DB/Dokumentasi/img/cowisnull.jpg"><br>

5. Hasil dari Decision Tree Predictor <br>
<img src="/1_DB/Dokumentasi/dtree.jpg"><br>

<h1> Writing To DB </h1>
Skema :
<img src="/1_DB/Dokumentasi/img/skema.jpg"><br>
1. Simpan file awal sebelum diproses 
<img src="/1_DB/Dokumentasi/img/ori.jpg"><br>
2. Simpan model dengan time stamp
<img src="/1_DB/Dokumentasi/img/time.jpg"><br>
3. Update database dengan DB Update lalu dilakukan filtering
<img src="/1_DB/Dokumentasi/img/dbup2.jpg"><br>
4. Hasil dari DB Update setelah difilter
<img src="/1_DB/Dokumentasi/img/result7.jpg"><br>


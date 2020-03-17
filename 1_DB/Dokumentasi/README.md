<h1> Connecting & Renaming Table </h1>

1. Buka DBeaver lalu pilih sqlite<br>
<img src="/1_DB/Dokumentasi/sqlite.jpg"><br>

2. Buka newCensus.sqlite<br>
<img src="/1_DB/Dokumentasi/newcensus.jpg"><br>

3. Mengubah nama table dan menambahkan NRP didepan table.<br>
<img src="/1_DB/Dokumentasi/rtable1.jpg"><br>
<img src="/1_DB/Dokumentasi/rtable2.jpg"><br>

4. Lakukan hal ini untuk 2 table (ss13pme dan ss13hme)<br>

<h1> DB Connect</h1><br>
1. Execute SQLite Connector<br>
<img src="/1_DB/Dokumentasi/connect.jpg"><br>
2. Configure DB Table Selector dan pilih table. Lalu execute node tsb.<br>
<img src="/1_DB/Dokumentasi/insert1.jpg"><br>
3. Execute DB Reader dan Buka table<br>
<img src="/1_DB/Dokumentasi/dbread.jpg"><br>
<img src="/1_DB/Dokumentasi/result1.jpg"><br>

<h1> In DB Processing</h1><br>
1. Execute SQLite Connector<br>
<img src="/1_DB/Dokumentasi/connect.jpg"><br>
2. Pilih table yg akan digunakan dengan DB Table Selector<br>
<img src="/1_DB/Dokumentasi/select2.jpg"><br>
<img src="/1_DB/Dokumentasi/select3.jpg"><br>
3. Tambahkan Column Filter dan remove puma* dan pwgtp* pada tabel <br>
<img src="/1_DB/Dokumentasi/filter.jpg"><br>
4. Lakukan join antara 2 table sebelumnya dengan Joiner dan lakukan setting dengan serialno sebagai penanda<br>
<img src="/1_DB/Dokumentasi/joinserialno.jpg"><br>
5. Gunakan DB Reader. Hasil joiner sebagai berikut :
<img src="/1_DB/Dokumentasi/result2.jpg"><br>
6. Menambahkan Row Filter dan melakukan filter pada tabel dengan COW yang tidak NULL
<img src="/1_DB/Dokumentasi/filter1.jpg"><br>
7. Gunakan DB Reader untuk membaca hasil table
<img src="/1_DB/Dokumentasi/result3.jpg"><br>

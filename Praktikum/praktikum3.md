# Instalasi MongoDB dan Express <br>
### Percobaan Instalasi NodeJ
<br>
1. Setelah instalasi selesai jalankan command node -v untuk memeriksa apakah NodeJS sudah terinstall <br>

### Inisiasi project Express dan pemasangan package
<br>
1. Lakukan pembuatan folder dengan nama express-mongodb dan masuk ke dalam folder tersebut lalu buka melalui text editor masing-masing <br>
2. Lakukan npm init untuk mengenerate file package.json dengan menggunakan command npm init -y <br>
3. Lakukan instalasi express, mongose, dan dotenv dengan menggunakan command npm i express mongose dotenv <br>

   ### Koneksi Express ke MongoDB
<br>
   1. Buatlah file index.js pada root folder dan masukkan kode di bawah ini <br>
   2. Setelah itu coba jalankan aplikasi dengan command node index.js <br>
   3. Lakukan pembuatan file .env dan masukkan baris berikut. Setelah itu ubahlah kode pada listening port menjadi berikut dan coba jalankan aplikasi kembali <br>
   4. Copy connection string yang terdapat pada compas atau atlas dan paste kan pada .env seperti berikut <br>
   5. Tambahkan baris kode berikut pada file index.js. Setelah itu coba jalankan aplikasi kembali. <br>

   ### Pembuatan routing
   <br>
   1. Lakukan pembuatan direktori routes di tingkat yang sama dengan index.js <br>
   2. Buatlah file book.route.js di dalamnya <br>
   3. Tambahkan baris kode berikut untuk fungsi getAllBooks<br>
   4. Lakukan hal yang sama untuk getOneBook, createBook, updateBook, dan deleteBook <br>
  5. Lakukan import book.route.js pada file index.js dan tambahkan baris kode berikut <br>
  6. Uji salah satu endpoint dengan Postman <br>

   ### Pembuatan controller
   <br>
   1. Lakukan pembuatan direktori controllers di tingkat yang sama dengan index.js <br>
   2. Buatlah file book.controller.js di dalamnya <br>
   3. Salin baris kode dari routes untuk fungsi getAllBooks <br>
   4. Lakukan hal yang sama untuk getOneBook, createBook, updateBook, dan deleteBook <br>
5. Lakukan import book.controller.js pada file book.route.js <br>
6. Lakukan perubahan pada fungsi agar dapat memanggil fungsi dari book.controller.js <br>
7. Lakukan pengujian kembali, pastikan response tetap sama <br>

   ### Pembuatan model
   <br>
   Berikut adalah gambaran bentuk data dari modul sebelumnya <br>
   1. Lakukan pembuatan direktori models di tingkat yang sama dengan index.js <br>
   2. Buatlah file book.model.js di dalamnya <br>
   3. Tambahkan baris kode berikut sesuai dengan tabel di atas <br>

   ### Operasi CRUD
   <br>
   1. Hapus semua data pada collection books <br>
   2. Lakukan import book.model.js pada file book.controller.js <br>
   3. Lakukan perubahan pada fungsi createBook <br>
   4. Buatlah dua buah buku dengan data di bawah ini dengan Postman <br>
   5. Lakukan perubahan pada fungsi getAllBooks <br>
   6. Lakukan perubahan pada fungsi getOneBook <br>
   7. Tampilkan semua buku dengan Postman <br>
   8. Tampilkan buku Dilan 1990 dengan Postman <br>
   9. Lakukan perubahan pada fungsi updateBook <br>
   10. Ubah judul buku Dilan 1991 menjadi “<NAMA PANGGILAN> 1991” dengan
  
Postman
  11. Lakukan perubahan pada fungsi deleteBook
  12. Hapus buku Dilan 1990 dengan Postman
  13. 

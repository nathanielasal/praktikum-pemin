# Instalasi MongoDB dan Express <br>
### Percobaan Instalasi NodeJS

1. Setelah instalasi selesai jalankan command node -v untuk memeriksa apakah NodeJS sudah terinstall <br>
  ![Screenshot](../Screenshot3/1_node_v.png) <br>

### Inisiasi project Express dan pemasangan package
1. Lakukan pembuatan folder dengan nama express-mongodb dan masuk ke dalam folder tersebut lalu buka melalui text editor masing-masing <br>
![Screenshot](../Screenshot3/1_2_expressfolder.png) <br>
2. Lakukan npm init untuk mengenerate file package.json dengan menggunakan command npm init -y <br>
 ![Screenshot](../Screenshot3/2_npm_init-y.png) <br>
3. Lakukan instalasi express, mongose, dan dotenv dengan menggunakan command npm i express mongose dotenv <br>
 ![Screenshot](../Screenshot3/3_npm_express.png) <br>

   ### Koneksi Express ke MongoDB
   1. Buatlah file index.js pada root folder dan masukkan kode di bawah ini <br>
  ` require('dotenv').config();
const express = require('express');
const mongoose = require('mongoose');
const app = express();
app.use(express.json());
app.get('/', (req, res) => {
res.status(200).json({
message: '<nama>,<nim>'
})
})
const PORT = 8000;
app.listen(PORT, () => {
console.log(`Running on port ${PORT}`);
})`
   ![Screenshot](../Screenshot3/4_indexjs.png) <br> 
   2. Setelah itu coba jalankan aplikasi dengan command node index.js <br>
    ![Screenshot](../Screenshot3/5_node.png) <br>
   3. Lakukan pembuatan file .env dan masukkan baris berikut. Setelah itu ubahlah kode pada listening port menjadi berikut dan coba jalankan aplikasi kembali <br>
   ![Screenshot](../Screenshot3/6_env.png) <br>
   4. Copy connection string yang terdapat pada compas atau atlas dan paste kan pada .env seperti berikut <br>
    ![Screenshot](../Screenshot3/7_mongoconnect.png) <br>
   5. Tambahkan baris kode berikut pada file index.js. Setelah itu coba jalankan aplikasi kembali. <br>
    ![Screenshot](../Screenshot3/8_mongodb_connect.png) <br>

   ### Pembuatan routing
   1. Lakukan pembuatan direktori routes di tingkat yang sama dengan index.js <br>
   ![Screenshot](../Screenshot3/1_3_folderroute.png) <br>
   2. Buatlah file book.route.js di dalamnya <br>
   ![Screenshot](../Screenshot3/10_book_route_js.png) <br>
   3. Tambahkan baris kode berikut untuk fungsi getAllBooks, getOneBook, createBook, updateBook, dan deleteBook <br>
   ![Screenshot](../Screenshot3/11_getall.png) <br>
  4. Lakukan import book.route.js pada file index.js dan tambahkan baris kode berikut <br>
  ![Screenshot](../Screenshot3/1_5_routingindex.png) <br>
  5. Uji salah satu endpoint dengan Postman <br>
  ![Screenshot](../Screenshot3/1_6_postman1.png) <br>

   ### Pembuatan controller
   1. Lakukan pembuatan direktori controllers di tingkat yang sama dengan index.js <br>
   ![Screenshot](../Screenshot3/1_9_foldercontroller.png) <br>
   2. Buatlah file book.controller.js di dalamnya <br>
   ![Screenshot](../Screenshot3/1_10_bookcontrollerjs.png) <br>
   3. Salin baris kode dari routes untuk fungsi getAllBooks, getOneBook, createBook, updateBook, dan deleteBook <br>
    ![Screenshot](../Screenshot3/1_7_controllerjs.png) <br>
  4. Lakukan import book.controller.js pada file book.route.js dan lakukan perubahan pada fungsi agar dapat memanggil fungsi dari book.controller.js <br>
    ![Screenshot](../Screenshot3/1_8_routejs.png) <br>
  5. Lakukan pengujian kembali, pastikan response tetap sama <br>
   ![Screenshot](../Screenshot3/1_6_postman1.png) <br>


   ### Pembuatan model
   1. Lakukan pembuatan direktori models di tingkat yang sama dengan index.js <br>
   ![Screenshot](../Screenshot3/1_11_modelfolder.png) <br>
   2. Buatlah file book.model.js di dalamnya <br>
    ![Screenshot](../Screenshot3/1_11_modelfolder.png) <br>
   3. Tambahkan baris kode berikut sesuai dengan tabel di atas <br>
    ![Screenshot](../Screenshot3/1_12_bookmodeljs.png) <br>

   ### Operasi CRUD
   1. Hapus semua data pada collection books <br>
    ![Screenshot](../Screenshot3/12_deletecoll.png) <br>
   2. Lakukan import book.model.js pada file book.controller.js <br>
    ![Screenshot](../Screenshot3/1_11_modelfolder.png) <br>
   3. Lakukan perubahan pada fungsi createBook <br>
   ![Screenshot](../Screenshot3/13_createbook.png) <br>
   4. Buatlah dua buah buku dengan data di bawah ini dengan Postman <br>
   ![Screenshot](../Screenshot3/14_bukubaru1.png) <br>
    ![Screenshot](../Screenshot3/14_bukubaru2.png) <br>
   5. Lakukan perubahan pada fungsi getAllBooks <br>
    ![Screenshot](../Screenshot3/17_getallbook.png) <br>
   6. Lakukan perubahan pada fungsi getOneBook <br>
    ![Screenshot](../Screenshot3/16_getonebook.png) <br>
   7. Tampilkan semua buku dengan Postman <br>
    ![Screenshot](../Screenshot3/18_postman_getall.png) <br>
   8. Tampilkan buku Dilan 1990 dengan Postman <br>
    ![Screenshot](../Screenshot3/23_getbooksdilan.png) <br>
   9. Lakukan perubahan pada fungsi updateBook <br>
    ![Screenshot](../Screenshot3/19_updatebook.png) <br>
   10. Ubah judul buku Dilan 1991 menjadi “<NAMA PANGGILAN> 1991” dengan Postman <br>
    ![Screenshot](../Screenshot3/20_postmanupdatebook.png) <br>
  11. Lakukan perubahan pada fungsi deleteBook <br>
   ![Screenshot](../Screenshot3/21_deletebook.png) <br>
  12. Hapus buku Dilan 1990 dengan Postman 
   ![Screenshot](../Screenshot3/22_postmandelete.png) <br>
   


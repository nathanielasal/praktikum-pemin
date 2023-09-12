# Praktikum 1 : Instalasi Lumen, MongoDB, dan Konfirgurasi App Key

### composer 
instalasi composer sudah dilakukan sebelumnya, cek apakah composer sudah berjalan.
![Screenshot mongodb](../Screenshot1/1_composer.png) 
### instalasi mongodb
install mongodb dari halaman https://www.mongodb.com/try/download/community 
![Screenshot mongodb](../Screenshot1/2_mongodb.png)
<br>
pilih complete install pada instalasi mongodb
![Screenshot mongodb](../Screenshot1/3_mongodb.png)
<br>
tanpa mengubah settingan apapun, klik next
![Screenshot mongodb](../Screenshot1/4_mongodb.png)
<br>
centang pada pilihan "Install MongoDB Compass", lalu next
![Screenshot mongodb](../Screenshot1/5_mongodb.png)
<br>
pilih option install, lalu tunggu hingga instalasi selesai
![Screenshot mongodb](../Screenshot1/6_mongodb.png)
<br>
setelah instalasi berhasil, mongodb compass akan muncul
![Screenshot mongodb](../Screenshot1/7_mongodb.png)

### lumen dan konfigurasi app key
buka direktori tempat lumen akan diinstall
![Screenshot mongodb](../Screenshot1/8.png)
<br>
masuk ke terminal dan buka folder tempat lumen akan diinstall, lalu ketikkan composer create-project --prefer-dist laravel/lumen lumenapi 
![Screenshot mongodb](../Screenshot1/9.png) 
<br>
untuk menjalankan server, ketikkan php -S localhost:8000 -t public pada terminal visual studio code
![Screenshot mongodb](../Screenshot1/10.png)
<br>
Buka file web.php pada folder routes, kemudian buat endpoint yang akan mengembalikan random string dengan panjang 32
![Screenshot](../Screenshot1/11.png)
<br>
buka "localhost:8000" pada browser untuk mnengecek apakah lumen sudah terinstall
![Screenshot](../Screenshot1/12_localhost8000.png)

<br>
tambahkan "/key" untuk melakukan generate app key
![Screenshot](../Screenshot1/13_appkey.png)

<br>
copy key tersebut ke file .env pada projek lumenapi
![Screenshot](../Screenshot1/14_envappkey.png) 

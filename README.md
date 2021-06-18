# **PRAKTIKUM 12 : PHP Framework (Codeinteger)**<br/>
</br>


+ Konfigurasi ekstensi PHP yang perlu diaktifkan seperti di gambar ini. Untuk mengaktifkan ekstensinya, hapus tanda <b> ; </b>
![1 1](https://user-images.githubusercontent.com/56438848/122497153-1f20ca80-d017-11eb-89f1-a8dd2366c7d0.jpg)

Ada beberapa ekstensi lainnya juga untuk pengembangan Codeinteger, seperti berikut.
- <b>php-json</b> ekstension untuk bekerja dengan JSON;
- <b>php-mysqlnd</b> native driver untuk MySQL;
- <b>php-xml</b> ekstension untuk bekerja dengan XML;
- <b>php-intl</b> ekstensi untuk membuat aplikasi multibahasa;
- <b>libcurl</b> (opsional), jika ingin pakai Curl.

+ Buat folder baru pada htdocs bernama <i>lab11_ci</i>.
+ Unduh <b>Codeinteger</b> di web https://codeigniter.com/download
+ Ubah nama direktory framework-4.x.xx menjadi ci4. Dan taruh kedalam folder lab11_ci
+ Buka browser dengan alamat http://localhost/lab11_ci/ci4/public/
![1 2](https://user-images.githubusercontent.com/56438848/122497158-20ea8e00-d017-11eb-946e-74b038d787c3.jpg)


+ <b>Menjalankan CLI (Command Line Interface)</b>
Buka XAMPP Control Panel, pilih <b>Shell</b> untuk membuka terminal/command prompt, arahkan sesuai dengan direktori folder <b>lab11_ci</b> seperti pada gambar ini. Perintah yang dapat dijalankan untuk memanggil CLI Codeinteegr adalah <b><i> php spark </b></i>
![2](https://user-images.githubusercontent.com/56438848/122503373-842ded80-d022-11eb-9d95-f5edbf912b42.JPG)


+ <b>Mengaktifkan Mode Debugging</b>
Codeinteger menyediakan firut <b>Debugging</b> untuk memudahkan developer untuk mengetahui pesan error. Semua jenis error akan ditampilkan. Untuk mengaktifkannya, ubah nilai konfigurasi pada environtmen variable <b>CI_ENVIRONMENT</b> menjadi <b>development</b> seperti pada gambar ini. Dan ubah nama file <b> env </b> menjadi <b> .env </b>
![4](https://user-images.githubusercontent.com/56438848/122504534-b2143180-d024-11eb-8f21-21592bb5092e.jpg)

Error sebelum diubah
![4 2](https://user-images.githubusercontent.com/56438848/122504640-e0920c80-d024-11eb-9221-c3ad0fd5380b.JPG)

Gambar dibawah ini adalah setelah mengaktifkan fitur <b>Debugging</b>. Setelah menghapus tanda <b>;</b> pada file <b>app/Controller/Home.php</b>
![5](https://user-images.githubusercontent.com/56438848/122504766-2353e480-d025-11eb-8283-3cada7459840.jpg)


+ <b>Membuat Route Baru</b>
![7 1](https://user-images.githubusercontent.com/56438848/122505032-ba20a100-d025-11eb-8142-45f33d3bcd60.jpg)

Selanjutnya, akses alamat url http://localhost:8080/about untuk mencoba route yang telah dibuat.
Ketika diakses akan muncul tampilan error, artinya file/page tersebut tudak ada. Untuk dapat mengakses halaman tersebut, buat Controller yang sesuai dengan rooting yang dibuat di <b>Controller Page</b>.
![7 2](https://user-images.githubusercontent.com/56438848/122505042-bd1b9180-d025-11eb-8747-14f8c20bc98e.JPG)


+ <b>Membuat Controller Page</b>
Buat file baru dengan nama <b>page.php</b> pada direktori Controller, masukkan kode seperti gambar atau bisa mengakses file diatas. Setelah itu, save dan refresh halaman web yang tadi error.
![Extra](https://user-images.githubusercontent.com/56438848/122505387-75e1d080-d026-11eb-899c-34cead6048ea.JPG)


> - <b>Tambahan</b> </br>
Ketika halaman tidak muncul dan masih error, coba untuk mengaktifkan perintah <b>php spark serve</b> pada command prompt seperti gambar ini.
![8 0](https://user-images.githubusercontent.com/56438848/122505651-fb658080-d026-11eb-81bf-9e69aef6a0b1.JPG)


+ <b> Auto Routing</b>
Auto Routing secara default sudah aktif, untuk mengubah nilai variablenya dapat mengubah <b>true</b> menjadi </b>false<b>. </br>
Sebelum diubah
![8 1](https://user-images.githubusercontent.com/56438848/122506264-29979000-d028-11eb-8c28-19d906f1caad.JPG)

Setelah diubah
![8 2](https://user-images.githubusercontent.com/56438848/122506268-2b615380-d028-11eb-90b7-5d03a648bac3.JPG)

+ <b>Membuat View</b>









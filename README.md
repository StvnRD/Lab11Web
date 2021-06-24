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
</br>
Buka XAMPP Control Panel, pilih <b>Shell</b> untuk membuka terminal/command prompt, arahkan sesuai dengan direktori folder <b>lab11_ci</b> seperti pada gambar ini. Perintah yang dapat dijalankan untuk memanggil CLI Codeinteegr adalah <b><i> php spark </b></i>
![2](https://user-images.githubusercontent.com/56438848/122503373-842ded80-d022-11eb-9d95-f5edbf912b42.JPG)


+ <b>Mengaktifkan Mode Debugging</b>
</br>
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
</br>
Buat file baru dengan nama <b>page.php</b> pada direktori Controller, masukkan kode seperti gambar atau bisa mengakses file diatas. Setelah itu, save dan refresh halaman web yang tadi error.
```<?php

namespace App\Controllers;

class Page extends BaseController
{
    public function about()
    {
        echo "Ini halaman About";
    }

    public function contact()
    {
        echo "Ini halaman Contact";
    }

    public function faqs()
    {
        echo "Ini halaman FAQ";
    }
}
```

> - <b>Tambahan</b> </br>
Ketika halaman tidak muncul dan masih error, coba untuk mengaktifkan perintah <b>php spark serve</b> pada command prompt seperti gambar ini. Pastikan untuk tetap berjalan pada latar belakang.
![8 0](https://user-images.githubusercontent.com/56438848/122505651-fb658080-d026-11eb-81bf-9e69aef6a0b1.JPG)


+ <b> Auto Routing</b>
</br>
Auto Routing secara default sudah aktif, untuk mengubah nilai variablenya dapat mengubah <b>true</b> menjadi </b>false<b>. </br>
Sebelum diubah
![8 1](https://user-images.githubusercontent.com/56438848/122506264-29979000-d028-11eb-8c28-19d906f1caad.JPG)

Setelah diubah
![8 2](https://user-images.githubusercontent.com/56438848/122506268-2b615380-d028-11eb-90b7-5d03a648bac3.JPG)

+ <b>Membuat View</b>
</br>
Buat file baru dengan nama <b>about.php</b> pada direktori <b>app/views</b>. Lihat gambar untuk lebih jelas.
![8 3](https://user-images.githubusercontent.com/56438848/122507617-b6dbe400-d02a-11eb-80fa-d11e9e2d929b.JPG)
</br>
</br>
</br>


# **Membuat Layout Web dengan CSS**<br/>
</br>

+ Buat file css pada direktori <b>Public</b> dengan nama <b>style.css</b>.
</br>
> <i>copy file layout dari Praktikum 4</i>
![8 1](https://user-images.githubusercontent.com/56438848/122508213-cd366f80-d02b-11eb-9452-960209b920cd.JPG)

+ Buat folder <b>template</b> pada direktori view. Kemudian buat file <b>header.php</b> dan <b>footer.php</b>
![8 2](https://user-images.githubusercontent.com/56438848/122508398-269e9e80-d02c-11eb-8afc-813243eb24f8.JPG)

+ Isikan kode seperti dibawah ini, bisa diakses pada file diatas. Save dan buka url http://localhost:8080/about
![8 3](https://user-images.githubusercontent.com/56438848/122508436-33bb8d80-d02c-11eb-9083-d9fc382d11ac.JPG)
</br>
</br>

# **Tugas**<br/>
Lengkapi kode program untuk menu lainnya yang ada pada Controller Page, sehingga semua link pada navigasi header dapat menampilkan tampilan dengan layout yang sama.

![9](https://user-images.githubusercontent.com/56438848/122508832-d542df00-d02c-11eb-9a17-d844fe4611c4.JPG)


# **LANJUTAN (CRUD)**<br/>
</br>

+ Membuat Database dan Tabel pada <b>phpmyadmin</b> dan mengatur koneksi Database

``` Membuat Database
CREATE DATABASE lab_ci4
```

``` Membuat Tabel
CREATE TABLE artikel ( 
    id INT(11) auto_increment, 
    judul VARCHAR(200) NOT NULL, 
    isi TEXT, gambar VARCHAR(200), 
    status TINYINT(1) DEFAULT 0, 
    slug VARCHAR(200), 
    PRIMARY KEY(id) 
);
``` 
![1 Koneksi Database  env](https://user-images.githubusercontent.com/56438848/123295366-da79bf80-d53f-11eb-9667-fdf4911cae49.jpg)

+ Membuat Model
Buat file baru pada direktori/folder <b>app/Models</b> dengan nama <b>ArtikelModel.php</b>

```
<?php 

namespace App\Models; 

use CodeIgniter\Model; 

class ArtikelModel extends Model 
{ 
    protected $table = 'artikel'; 
    protected $primaryKey = 'id'; 
    protected $useAutoIncrement = true; 
    protected $allowedFields = ['judul', 'isi', 'status', 'slug', 'gambar']; 

} 
```

+ Membuat Controller
Buat controller baru dengan nama <b>Artikel.php</b> pada direktori/folder <b>app/Controller</b>

```
<?php

namespace App\Controllers;

use App\Models\ArtikelModel;

class Artikel extends BaseController
{
    public function index()
    {
        $title = 'Daftar Artikel';
        $model = new ArtikelModel();
        $artikel = $model->findAll();
        return view('artikel/index', compact('artikel', 'title'));
    }
}
```

+ Membuat View
Buat direktori/folder baru dengan nama <b>artikel</b> didalam direktori/folder <b>app/Views</b>, kemudian buat file baru dengan nama <b>index.php</b>.

```
<?= $this->include('template/header'); ?> 

<?php if($artikel): foreach($artikel as $row): ?> 
<article class="entry"> 
    <h2<a href="<?= base_url('/artikel/' . $row['slug']);?>"><?= $row['judul']; ?></a> 
</h2> 
    <img src="<?= base_url('/gambar/' . $row['gambar']);?>" alt="<?= $row['judul']; ?>"> 
    <p><?= substr($row['isi'], 0, 200); ?></p> 
</article> 
<hr class="divider" /> 
<?php endforeach; else: ?> 
<article class="entry"> 
    <h2>Belum ada data.</h2> 
</article> 
<?php endif; ?> 

<?= $this->include('template/footer'); ?> 
```






</br>
</br>

> <i>Akses full file - https://drive.google.com/drive/folders/1a9dQBmXQ8vKfxCNv_kuaf2mN3ZcamSSy?usp=sharing </i>

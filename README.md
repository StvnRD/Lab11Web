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




# **LANJUTAN CRUD (Create, Read, Update, Delete)**<br/>
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
Buat direktori/folder baru dengan nama <b>artikel</b> didalam direktori/folder <b>app/Views</b>, kemudian buat file baru dengan nama <b>index.php</b>. Jangan lupa menambahkan kode pada file Routing jika tidak muncul sesuai dengan gambar dibawah.

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
![5 Buat Routing Artikel](https://user-images.githubusercontent.com/56438848/123397957-376f8700-d5cd-11eb-8930-9038cffbea82.jpg)


+ Menambahkan data pada database agar dapat menampilkan data pada halaman artikel.

```
INSERT INTO artikel (judul, isi, slug) 
VALUE ('Artikel pertama', 'Lorem Ipsum adalah contoh teks atau dummy dalam industri percetakan dan penataan huruf atau typesetting.
Lorem Ipsum telah menjadi standar contoh teks sejak tahun 1500an, 
saat seorang tukang cetak yang tidak dikenal mengambil sebuah kumpulan teks dan mengacaknya untuk menjadi sebuah buku contoh huruf.', 'artikel-pertama'), 
('Artikel kedua', 'Tidak seperti anggapan banyak orang, Lorem Ipsum bukanlah teks-teks yang diacak. 
Ia berakar dari sebuah naskah sastra latin klasik dari era 45 sebelum masehi, hingga bisa dipastikan usianya telah mencapai lebih dari 2000 tahun.', 'artikel-kedua');
```
![6 1](https://user-images.githubusercontent.com/56438848/123398466-c5e40880-d5cd-11eb-93a7-316e5631f3e1.JPG)
![6 2](https://user-images.githubusercontent.com/56438848/123398228-79003200-d5cd-11eb-899c-7e2646748fde.JPG)


+ Membuat Tampilan Detail Artikel
Pada saat judul berita di klik, maka akan diarahkan ke halaman yang berbeda. Tambahkan kode berikut pada <b>app/Controller/Artikel.php</b>

```
    public function view($slug)
    {
        $model = new ArtikelModel();
        $artikel = $model->where([
            'slug' => $slug
        ])->first();

        // Menampilkan error apabila data tidak ada.
        if (!$artikel)
        {
            throw PageNotFoundException::forPageNotFound();
        }

        $title = $artikel['judul'];
        return view('artikel/detail', compact('artikel', 'title'));
    }
```


+ Membuat View Detail
Membuat view baru untuk halaman detail. Buat file baru pada direktori <b>app/Views/artikel</b> dengan nama <b>detail.phpl</b>
```
<?= $this->include('template/header'); ?> 

<article class="entry"> 
    <h2><?= $artikel['judul']; ?></h2> 
    <img src="<?= base_url('/gambar/' . $artikel['gambar']);?>" alt="<?= $artikel['judul']; ?>"> 
    <p><?= $row['isi']; ?></p> 
</article> 

<?= $this->include('template/footer'); ?> 
```

+ Membuat Routing
Buka file <b>app/config/Routes.php</b> kemudian tambahkan routing code ini untuk artikel detail.
```
$routes->get('/artikel/(:any)', 'Artikel::view/$1');
```
![Tambahan](https://user-images.githubusercontent.com/56438848/123399507-e1034800-d5ce-11eb-948d-eeab43094868.jpg)


+ Membuat menu admin
Tambahkan method baru pada <b>app/Controllers/Artikel.php</b>
```
 public function admin_index() 
    { 
        $title = 'Daftar Artikel'; 
        $model = new ArtikelModel(); 
        $artikel = $model->findAll(); 
        return view('artikel/admin_index', compact('artikel', 'title')); 
    } 
```
![Tambahan 2](https://user-images.githubusercontent.com/56438848/123400380-e6ad5d80-d5cf-11eb-863b-f3f171f98a1c.JPG)


+ Selanjutnya buat view untuk tampilan admin dengan nama <b>admin_index..php</b> pada direktri <b>app/Views/artikel</b>
```
<?= $this->include('template/admin_header'); ?>

<table class="table">
    <thread>
        <tr>
            <th>ID</th>
            <th>ID</th>
            <th>Status</th>
            <th>Aksi</th>
        <tr>
    </thread>
    <tbody>
    <?php if($artikel): foreach($artikel as $row): ?>
    <tr>
        <td><?= $row['id']; ?></td>
        <td>
            <b><?= $row['judul']; ?></b>
            <p><small><?= substr($row['isi'], 0, 50); ?></small></p>
            </td>
            <td><?= $row['status']; ?></td>
            <td>
                <a class="btn" href="<?= base_url('/admin/artikel/edit/' . $row['id']);?>">Ubah</a>
                <a class="btn btn-danger" onclick="return confirm('Yakin menghapus data?');" href="
                    <?= base_url('/admin/artikel/delete/' . $row['id']);?>">Hapus</a>
            </td>
        </tr>
        <?php endforeach; else: ?>
        <tr>
            <td colspan="4">Belum ada data.</td>
        </tr>
    <?php endif; ?>
    </tbody>
</table> 

<?= $this->include('template/admin_footer'); ?> 
```
![Tambahan 3](https://user-images.githubusercontent.com/56438848/123400646-2ffdad00-d5d0-11eb-9483-582bb80ac9c6.JPG)


+ Tambahkan Routing pada <b>app/Config/Routes.php</b>
```
$routes->group('admin', function($routes) { 
	$routes->get('artikel', 'Artikel::admin_index'); 
	$routes->add('artikel/add', 'Artikel::add'); 
	$routes->add('artikel/edit/(:any)', 'Artikel::edit/$1'); 
	$routes->get('artikel/delete/(:any)', 'Artikel::delete/$1'); 
	}); 
```
![Tambahan 4](https://user-images.githubusercontent.com/56438848/123400977-88cd4580-d5d0-11eb-879c-12389e8ae0a3.JPG)
![9](https://user-images.githubusercontent.com/56438848/123401115-aac6c800-d5d0-11eb-9ab0-b04989296ce4.JPG)


+ Tambah Data Artikel pada <b>app/Controllers/Artikel.php</b>
```
    public function add() 
    { 
        // validasi data. 
        $validation = \Config\Services::validation(); 
        $validation->setRules(['judul' => 'required']); 
        $isDataValid = $validation->withRequest($this->request)->run(); 
        
        if ($isDataValid) 
        { 
            $artikel = new ArtikelModel(); 
            $artikel->insert([ 
                'judul' => $this->request->getPost('judul'), 
                'isi' => $this->request->getPost('isi'), 
                'slug' => url_title($this->request->getPost('judul')), 
            ]); 
            return redirect('admin/artikel'); 
        } 
        $title = "Tambah Artikel"; 
        return view('artikel/form_add', compact('title')); 
        } 
```
![Tambahan 5](https://user-images.githubusercontent.com/56438848/123401534-1a3cb780-d5d1-11eb-88e0-1835b8f119bb.JPG)

+ Buat view untuk form tambah dengan nama <b>form_add.php</b> pada <app/Views/artikel>
```
<?= $this->include('template/admin_header'); ?>

<h2><?= $title; ?></h2>
<form action="" method="post">
    <p>
        <input type="text" name="judul">
    </p>
    <p>
        <textarea name="isi" cols="50" rows="10"></textarea>
    </p>
    <p><input type="submit" value="Kirim" class="btn btn-large"></p>
</form>

<?= $this->include('template/admin_footer'); ?>
```
![10](https://user-images.githubusercontent.com/56438848/123401928-6ee03280-d5d1-11eb-8af8-afb5d0785b74.JPG)


+ Menambah Data edit dengan menambahkan fungsi pada <b>app/Controllers/Artikel.php</b>
```
        public function edit($id) 
        { 
            $artikel = new ArtikelModel(); 

            // validasi data. 
            $validation = \Config\Services::validation(); 
            $validation->setRules(['judul' => 'required']); 
            $isDataValid = $validation->withRequest($this->request)->run(); 

            if ($isDataValid) 
            { 
                $artikel->update($id, [ 
                    'judul' => $this->request->getPost('judul'), 
                    'isi' => $this->request->getPost('isi'), 
                ]); 
                return redirect('admin/artikel'); 
            } 

            // ambil data lama 
            $data = $artikel->where('id', $id)->first(); 
            $title = "Edit Artikel"; 
            return view('artikel/form_edit', compact('title', 'data')); 
        } 
```
![Tambahan 6](https://user-images.githubusercontent.com/56438848/123402735-3ee55f00-d5d2-11eb-80a1-c799bf5170e5.JPG)


+ Buat view untuk form tambah pada direktori <b>app/Views/artikel</b> dengan nama <b>form_edit.php</b>
```
<?= $this->include('template/admin_header'); ?>

<h2><?= $title; ?></h2>
<form action="" method="post">
    <p>
        <input type="text" name="judul" value="<?= $data['judul'];?>" >
    </p>
    <p>
        <textarea name="isi" cols="50" rows="10"><?=$data['isi'];?></textarea>
    </p>
    <p><input type="submit" value="Kirim" class="btn btn-large"></p>
</form>
<?= $this->include('template/admin_footer'); ?>
```
![11](https://user-images.githubusercontent.com/56438848/123403346-e2367400-d5d2-11eb-8e09-c9df01b99ecc.JPG)


+ Tambahkan fungsi delete pada <b>app/Controllers/Artikel.php</b>
```
        public function delete($id)
        {
            $artikel = new ArtikelModel();
            $artikel->delete($id);
            return redirect('admin/artikel');
        }
```
![Tambahan 7](https://user-images.githubusercontent.com/56438848/123404335-2d508700-d5d3-11eb-94cc-cd9842e4343a.JPG)


</br>
</br>

> <i>Jangan lupa untuk selalu menyimpan file sebelum refresh halaman web. Jika error, coba teliti tiap langkah pada file dan folder</i>

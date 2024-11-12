# Lab7Web
# Dita Tiara Putri  
# 312310131
# TI 23 A1  


# Praktikum 7: PHP Dasar  
# 1 Menjalankan web server (XAMPP)  
![image](https://github.com/user-attachments/assets/42bbd26b-84c9-4bda-82e1-3bc622780118)  

# 2 Memulai PHP  
Buat folder lab7_php_dasar pada root directory web server ``(:\xampp\htdocs)``  
![image](https://github.com/user-attachments/assets/46214687-84e3-4134-b3ce-21712b874f91)  
Kemudian untuk mengakses direktory tersebut pada web server dengan mengakses URL:http://localhost/lab7_php_dasar/  
![image](https://github.com/user-attachments/assets/76995126-ec07-413c-b919-c1b75129eb27)  

# 3 PHP Dasar
Buat file baru dengan nama php_dasar.php pada directory tersebut.  
Kemudian untuk mengakses hasilnya melalui URL:http://localhost/lab7_php_dasar/php_dasar.php  
```sh
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>PHP Dasar</title>
</head>
<body>
    <h1>Belajar PHP Dasar</h1>
    <?php
        echo "Hello World";
    ?>
</body>
</html>
```
File ``php_dasar.php`` ini adalah contoh sederhana dari kode PHP yang menampilkan teks “Hello World” di halaman web.  
![image](https://github.com/user-attachments/assets/620f3d3e-3ede-4047-9b3a-9a0b855f56df)  

# 4 Variable PHP
Menambahkan variable pada program.
```sh
 <h2>Menggunakan Variable</h2>
    <?php
        $nim = "312310131";
        $nama = 'Dita Tiara Putri';
        echo "NIM : " . $nim . "<br>";
        echo "Nama : $nama";
    ?>
```
Kode PHP ini menambahkan variabel untuk menyimpan data seperti NIM dan nama, lalu menampilkannya di halaman web. Variabel ``$nim`` menyimpan "312310131", dan ``$nama`` menyimpan 'Dita Tiara Putri'. Kode echo digunakan untuk mencetak nilai variabel tersebut.  
![image](https://github.com/user-attachments/assets/14237a7c-36b7-47d6-b35e-466d52cb7e93)  

# 5 Predefine Variable $_GET  
```sh
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PHP Dasar</title>
</head>
<body>
    <h1>Predefine Variable</h1>
    <?php
        echo 'Selamat Datang ' . $_GET['nama'];
    ?>
</body>
</html>
```  
Kode PHP ini menggunakan variabel predefined ``$_GET`` untuk mengambil data dari URL dan menampilkannya di halaman web.  
``$_GET['nama']`` menangkap nilai dari parameter nama di URL, seperti ``http://localhost/lab7_php_dasar/php_dasar.php?nama=Agung.``  
echo ``'Selamat Datang '`` . ``$_GET['nama']``; menampilkan teks ``“Selamat Datang”`` diikuti nama yang dimasukkan di URL.  

![image](https://github.com/user-attachments/assets/6bf64eec-d6bf-44da-8a5b-43015a08278a)  
Jika URL berisi ?nama=Dita, output akan menjadi:  
![image](https://github.com/user-attachments/assets/fbde9e45-7ba3-46e4-8190-047596e334e4)  

# 6 Membuat Form Input  
```sh
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>PHP Dasar</title>
</head>
<body>
<h2>Form Input</h2>
    <form method="post">
    <label>Nama: </label>
    <input type="text" name="nama">
    <input type="submit" value="Kirim">
</form>
<?php
echo 'Selamat Datang ' . $_POST['nama'];
?>
</body>
</html>
```
Kode HTML dan PHP ini membuat form input sederhana untuk memasukkan nama, yang kemudian ditampilkan di halaman web.  
Formulir ini menggunakan metode post untuk mengirim data ke server.  
echo ``'Selamat Datang '`` . ``$_POST['nama'];`` menampilkan teks ``“Selamat Datang”`` diikuti dengan nama yang dimasukkan pengguna.  
Jika form belum disubmit, ``$_POST['nama']`` belum diisi dan akan menimbulkan error.   
![image](https://github.com/user-attachments/assets/72bb0dd9-bbff-45d9-9a77-0274938a25c2)  

# 7 











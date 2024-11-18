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

# 7 Operator 
```sh
<?php
$gaji = 1000000;
$pajak = 0.1;
$thp = $gaji - ($gaji*$pajak);
echo "Gaji sebelum pajak = Rp. $gaji <br>";
echo "Gaji yang dibawa pulang = Rp. $thp";
?>
```
Pajak dihitung sebagai persentase dari gaji kotor.  
Hasil akhir (gaji bersih) dicetak setelah dikurangi nilai pajak.  
Menggunakan <br> untuk membuat baris baru pada output di browser.  
![image](https://github.com/user-attachments/assets/c7e38d46-9a03-41a8-97ee-5c2b9a4c6a46) 

# 8 Kondisi if
```sh
<?php
$nama_hari = date("l");
if ($nama_hari == "Sunday") {
    echo "Minggu";
} elseif ($nama_hari == "Monday") {
    echo "Senin";
} else {
    echo "Selasa";
}
?>
```
Kode tersebut akan mencetak "Minggu" jika hari ini adalah Sunday, "Senin" jika Monday, dan "Selasa" untuk hari lainnya.  
![image](https://github.com/user-attachments/assets/4fb8bbf9-c63c-49ac-82fe-42e5c67ea0a9) 

# 9 Kondisi Switch
```sh
<?php
$nama_hari = date("l");
switch ($nama_hari) {
    case "Sunday":
        echo "Minggu";
        break;
    case "Monday":
        echo "Senin";
        break;
    case "Tuesday":
        echo "Selasa";
        break;
default:
    echo "Sabtu";
}
```
Kode PHP tersebut menggunakan struktur kontrol switch untuk memeriksa nilai variabel ``$nama_hari`` dan mencetak nama hari dalam bahasa Indonesia sesuai dengan kondisi yang terpenuhi.  
![image](https://github.com/user-attachments/assets/848f500b-0b2e-443a-9de9-9afefa3eda7a)  

# 10 Perulangan for 
```sh
<?php
echo "Perulangan 1 sampai 10 <br />";
for ($i=1; $i<=10; $i++) {
    echo "Perulangan ke: " . $i . '<br />';
}
echo "Perulangan Menurun dari 10 ke 1 <br />";
for ($i=10; $i>=1; $i--) {
    echo "Perulangan ke: " . $i . '<br />';
}
?>
``` 
Kode PHP ini menggunakan struktur perulangan for untuk mencetak angka secara naik dan turun.  
![image](https://github.com/user-attachments/assets/5f9275fd-a4a1-43aa-b0be-33e92a4f0486) 

# 11 Perulangan While 
```sh
<?php
echo "Perulangan 1 sampai 10 <br />";
$i=1;
while ($i<=10) {
    echo "Perulangan ke: " . $i . '<br />';
    $i++;
}
?>
```  
Kode PHP ini menggunakan perulangan ``while`` untuk mencetak angka dari 1 sampai 10.  
![image](https://github.com/user-attachments/assets/c64a47cb-3d18-4f72-8620-82ab17b9b096) 

# 12 Perulangan dowhile
```sh
<?php
echo "Perulangan 1 sampai 10 <br />";
$i=1;
while ($i<=10) {
    echo "Perulangan ke: " . $i . '<br />';
    $i++;
}
?>
```
Kode PHP di atas menggunakan struktur perulangan ``do-while`` untuk mencetak angka dari 1 sampai 10.  
![image](https://github.com/user-attachments/assets/25b441c0-fa5f-413c-b685-4b30d8604bd1)  

# Tugas
Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang berbeda-beda sesuai pilihan pekerjaan.  
```sh
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Input Data</title>
</head>
<body>
    <h2>Form Input Data</h2>
    <form method="POST" action="">
        <label for="nama">Nama:</label><br>
        <input type="text" id="nama" name="nama" required><br><br>

        <label for="tanggal_lahir">Tanggal Lahir:</label><br>
        <input type="date" id="tanggal_lahir" name="tanggal_lahir" required><br><br>

        <label for="pekerjaan">Pekerjaan:</label><br>
        <select id="pekerjaan" name="pekerjaan" required>
            <option value="Programmer">Programmer</option>
            <option value="Designer">Designer</option>
            <option value="Manager">Manager</option>
        </select><br><br>

        <button type="submit" name="submit">Submit</button>
    </form>

    <?php
    if (isset($_POST['submit'])) {
        $nama = $_POST['nama'];
        $tanggal_lahir = $_POST['tanggal_lahir'];
        $pekerjaan = $_POST['pekerjaan'];
        $lahir = new DateTime($tanggal_lahir);
        $sekarang = new DateTime();
        $umur = $sekarang->diff($lahir)->y;
        $gaji = 0;
        switch ($pekerjaan) {
            case "Programmer":
                $gaji = 8000000;
                break;
            case "Designer":
                $gaji = 6000000;
                break;
            case "Manager":
                $gaji = 10000000;
                break;
        }

        echo "<h3>Hasil Input</h3>";
        echo "Nama: $nama<br>";
        echo "Tanggal Lahir: $tanggal_lahir<br>";
        echo "Umur: $umur tahun<br>";
        echo "Pekerjaan: $pekerjaan<br>";
        echo "Gaji: Rp " . number_format($gaji, 0, ',', '.') . "<br>";
    }
    ?>
</body>
</html>
```
1. Pengguna memasukkan nama, tanggal lahir, dan memilih pekerjaan.  
2. Setelah tombol submit ditekan:  
   Data dikirim ke server melalui POST.  
   Tanggal lahir digunakan untuk menghitung umur.  
   Pilihan pekerjaan menentukan gaji.  
3. Program menampilkan nama, tanggal lahir, umur, pekerjaan, dan gaji di layar.

![image](https://github.com/user-attachments/assets/4f6f45d0-38d9-4646-a664-0c4971903e99)  
![image](https://github.com/user-attachments/assets/18bb4fd9-cc4c-46f3-92ce-8e0995fd621c)  
![image](https://github.com/user-attachments/assets/6d05a2da-d5a9-463f-9f36-94f9ea07bb23) 
![image](https://github.com/user-attachments/assets/8cf17e82-13f4-43be-9eb5-fd28594b4104)





















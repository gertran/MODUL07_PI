MODEL, CONTROLLER DAN REQUEST RESPONSE HANDLER
------------------------------------------------
Langkah 1) Buat database dengan nama "lumenpost" dan atur konfigurasi database di file .env.
Aktifkan library bawaan Lumen dalam file app.php, dan lakukan generate file migration.
Setelah itu, ubah fungsi up() di file "create_posts_table," "create_comments_table,"
"create_tags_table," dan "create_post_tag_table" sesuai struktur database. Terakhir,
jalankan perintah "php artisan migrate" untuk migrasi database, dan Anda dapat melihat
hasilnya melalui phpMyAdmin.

<img src="1.jpg">
<img src="2.jpg">
<img src="3.jpg">
<img src="4.jpg">
<img src="5.jpg">
<img src="6.jpg">

Langkah 2) Buatlah file dengan nama "Post.php" , "Comment.php" dan juga file "Tag.php" di dalam
direktori Models.

<img src="7.jpg">
<img src="8.jpg">
<img src="9.jpg">

Langkah 3) Tambahkan metode "comments()" di dalam file "Post.php". Selanjutnya, tambahkan
metode "post()" dan atribut "postId" ke dalam $fillable pada file "Comment.php." Setelah
itu, buat file "PostController.php" di dalam direktori "app>Http>Controllers," dan juga
buat file "CommentController.php" di direktori yang sama. Selanjutnya, tambahkan prefix
"posts" dan "comments" ke dalam file "routes/web.php". Setelah itu, buat satu posting
yang berisi konten "disana engkau berdua" menggunakan Postman dengan metode POST,
dan juga buat satu komentar yang berisi ulasan "disini aku yang sendiri" dan postId "1"
menggunakan Postman dengan metode POST. Terakhir, tampilkan posting dengan id "1"
menggunakan Postman dengan metode GET.

Buatlah satu post menggunakan Postman
<img src="10.jpg">
Buatlah satu comment menggunakan Postman
<img src="11.jpg">
Tampilkan post menggunakan Postman
<img src="12.jpg">
<img src="13.jpg">
<img src="14.jpg">
<img src="15.jpg">
<img src="16.jpg">

Langkah 4) Tambahkan metode "tags()" di dalam file "Post.php". Selanjutnya, pada file "Tag.php",
tambahkan metode "posts()" untuk mendapatkan semua posting terkait dengan tag
tersebut. Buat file "TagController.php" di direktori "app>Http>Controllers" untuk
mengelola operasi terkait tag. Di dalam "PostController.php," tambahkan metode
"addTag" untuk menambahkan tag ke posting dan respons yang mengembalikan daftar tag
pada posting tersebut.
Selanjutnya, pada file "routes/web.php", tambahkan prefix "posts" untuk mengelola rute
terkait posting. Kemudian, menggunakan Postman dengan metode POST, buat satu tag
dengan nama "jadul". Setelah itu, menggunakan metode PUT, tambahkan tag "jadul" ke
dalam posting "disana engkau berdua".
Selanjutnya, gunakan metode GET pada Postman untuk menampilkan detail dari posting
"disana engkau berdua" dan pastikan tag "jadul" terhubung dengan posting tersebut.
Buat posting baru dengan konten "tanpamu apa artinya" menggunakan Postman dengan
metode POST. Setelah itu, menggunakan metode PUT, tambahkan tag "jadul" ke dalam
posting "tanpamu apa artinya". Selanjutnya, buat tag baru dengan nama "lagu"
menggunakan metode POST, dan menggunakan metode PUT, tambahkan tag "lagu" ke
dalam posting "tanpamu apa artinya".
Terakhir, menggunakan Postman dengan metode GET, tampilkan detail dari posting
pertama ("disana engkau berdua") dan posting kedua ("tanpamu apa artinya") untuk
memastikan semua perubahan telah diimplementasikan.

Buatlah satu tag menggunakan Postman
<img src="17.jpg">
 Tambahkan tag “jadul” pada post “disana engkau berdua”
<img src="18.jpg">
Tampilkan post “disana engkau berdua” menggunakan Postman
<img src="19.jpg">
Buatlah postingan “tanpamu apa artinya” menggunakan Postman
<img src="20.jpg">
Tambahkan tag “jadul” pada postingan “tanpamu apa artinya”
<img src="21.jpg">
 Buatlah tag “lagu” menggunakan Postman
<img src="22.jpg">
Tambahkan tag “lagu” pada postingan “tanpamu apa artinya”
<img src="23.jpg">
Tampilkan post pertama
<img src="24.jpg">
 Tampilkan post kedua
<img src="25.jpg">
<img src="26.jpg">
<img src="27.jpg">
<img src="28.jpg">
<img src="29.jpg">
<img src="30.jpg">
<img src="31.jpg">
<img src="32.jpg">
<img src="33.jpg">
<img src="34.jpg">
<img src="35.jpg">
<img src="36.jpg">
<img src="37.jpg">

Langkah 6) Lakukan perubahan summary pada buku “No Longer Human” menjadi “Buku
yang bagus (<NAMA>,<NIM>) dengan melakukan klik “Edit Document”
(berlambang pensil), mengisi nilai summary yang baru, dan melakukan klik
“Update”
<img src="8.jpg">

Langkah 7) Lakukan penghapusan pada buku “I Am a Cat” dengan melakukan klik
“Remove Document” (berlambang tong sampah) dan melakukan klik “Delete”
<img src="9.jpg">
<img src="10.jpg">


MongoDB SHELL
------------------------------------------------
Langkah 1) Lakukan koneksi ke MongoDB server dengan menjalankan command mongosh bagi yang
menggunakan terminal build in OS sehingga tampilan terminal kalian menjadi seperti
berikut.
<img src="11.jpg">

Langkah 2) Mencoba melihat list database yang ada di server dengan menjalankan command show
dbs
Untuk berpindah ke database “bookstore” gunakan command use bookstore , kalian
dapatmemastikan telah berpindah ke database yang benar dengan melihat tulisan sebelum
tanda “>”
<img src="12.jpg">

Langkah 3) Lakukan insert buku “Overlord I” dengan menggunakan command
db.books.insertOne(<data kalian>) , setelah insert buku berhasil maka MongoDB akan
mengembalikan pesan sebagai berikut.
<img src="13.jpg">

Langkah 4) Lakukan insert buku “The Setting Sun” dan “Hujan” dengan insert many dengan
menggunakan command db.books.insertMany(<data kalian>) , dan akan mengembalikan
pesan seperti pada modul
<img src="14.jpg">

Langkah 5) Lakukan pencarian buku dengan menggunakan command db.books.find() untuk
melakukan pencarian semua buku.
<img src="15.jpg">

Langkah 6) Tampilkan seluruh buku dengan author “Osamu Dazai” dengan mengisi argument pada
find() dengan menggunakan command db.books.find({<filter yang ingin diisi>})
<img src="16.jpg">

Langkah 7) Lakukan perubahan summary pada buku “Hujan” menjadi “Buku yang bagus
(<NAMA>,<NIM>) dengan mengunakan command db.books.updateOne({<filter>},
{$set: {<data yang akan di update>}}) sehingga output yang dihasilkan oleh MongoDB
akan menjadi seperti pada modul
<img src="17.jpg">

Langkah 8) Lakukan perubahan publisher menjadi “Yen Press” pada semua buku “Osamu Dazai”
dengan menggunakan command db.books.updateMany({<filter>}, {$set: {<data yang
akan di update>}})
<img src="18.jpg">

Langkah 9) Lakukan penghapusan pada buku “Overlord I” dengan menggunakan command
db.books.deleteOne({<argument>})
<img src="19.jpg">

Langkah 10) Lakukan penghapusan pada semua buku “Osamu Dazai dengan menggunakan
command db.books.deleteMany({<argument>})
<img src="20.jpg">

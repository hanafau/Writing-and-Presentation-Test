# Writing and Presentation Test Week 1
----------------------------------------------------------
## Unix Command Line
+ SHELL adalah perantara user untuk memberikan perintah kepada sistem operasi dalam komputer.
+ Command Line Interface adalah suatu yang berbentuk seperti CMD yang berguna untuk mengetikkan perintah dalam bentuk teks dan memberikan instruksi pada komputer untuk mengerjakan tugas tertentu

#### Command
1. pwd --> untuk mengetahui lokasi saat ini
2. ls--> mengetahui isi dari lokasi yg saat ini ditempati
3. cd--> perintah untuk pindah directory/folder
4. mkdir--> perintah membuat directory/folder
5. touch--> membuat file
6. head--> menampilkan beberapa isi file bagian atas
7. tail--> menampilkan beberapa isi file bagian bawah
8. cat--> melihat isi file seluruhnya
9. cp--> menyalin file
10. mv--> memindah file dan bisa untuk merename
11. rm--> untuk menghapus file

 
## Git dan Github
+ Git bertugas untuk mencatat perubahan seluruh file atau repository suatu project.
+ Github adalah website yang digunakan untuk menyimpan dan mengelola kode suatu project.
###### Kenapa git penting?
 Git dapat membantu melacak perubahan dan pembaruan. Programmer bisa melihat siapa yang membuat perubahan dan Git juga menyediakan data kapan dan mengapa perubahan dilakukan lewat Log.
 Dan github dapat memudahkan kolaborasi antar developer dalam menjalankan project.

+ git init digunakan untuk membuat repository baru.
+ git commit -m " " digunakan untuk menyimpan perubahan pada Git.
+ git push origin digunakan untuk mempublish file ke github.
+ git clone digunakan untuk melakukan cloning dari github ke local.

## HTML
- HTML adalah singkatan dari Hypertext Markup Language yaitu bahasa untuk membuat kerangka suatu website.
- Tools yang bisa digunakan membuat html visual studio code, sublime, dll.
- Beberapa extention yg dapat mempermudah saat ngoding ada live server, prettier, dll yang bisa di instal di extention code editor masing masing.

### Contoh HTML Sederhana

        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Document</title>
        </head>
            <body>
                <h1>My Profile</h1>
                    <ul>
                      <li>Nama: Hana Fauziah</li>
                      <li>Kelas: FE32</li>
                      <li>Asal: Yogyakarta</li>
                      <li>Instagram: <a href="www.instagram.com">klik disini</a></li>
                    </ul>
                    <img src="https://i.pinimg.com/736x/46/8d/79/468d79d34b2526bf5655524c0f59e5b4.jpg" width="200px" />
            </body>
        </html>

### Tag
##### Basic 
1.  <html> --> membuka dokumen html
2. <title> --> membuat judul halaman
3. <body> --> membuat tubuh/inti dari halaman
##### Paragraf
1. <h1> sampai <h6> --> membuat heading
2. <p> --> membuat paragraf
##### Form
1. <form> --> membuat form html untuk pengguna
2. <input> --> membuat kontrol input
3. <button> --> membuat tombol yang dapat di klik
##### Gambar
1. <img> --> untuk memasukan gambar
2. <audio> --> untuk memasukan audio
3. <video> --> untuk memasukan video
##### Link
1. <a> --> untuk membuat hyperlink
2. <link> --> tag untuk menghubungkan antara dokumen dengan dokumen eksternal / biasanya untuk link ke style sheet
3. <nav> --> membuat navigasi
##### List
1. <ul>- -> membuat daftar selain nomor
2. <ol> --> membuat daftar dengan nomor
3. <li> --> membuat item daftar
##### Table
1. <table> --> membuat table
2. <tr> --> membuat baris dalam table
3. <td> --> membuat kolom dalam table

### Semantik
Semantic artinya kita menggunakan element html yang sesuai dengan kebutuhan konten.
misalnya **<div class="footer">** kita bisa menuliskannya hanya seperti ini **<footer>** jadi lebih mempermudah.
Beberapa semantic tag yang dibawa oleh HTML5 adalah sebagai berikut:
+ <article>
+ <aside>
+ <figcaption>
+ <figure>
+ <footer>
+ <header>
+ <main>
+ <mark>
+ <nav>
+ <section>
+ <summary>
+ <time>

### Deployment
Deployment adalah kegiatan yang bertujuan untuk menyebarkan aplikasi yang telah dikerjakan oleh developer. Kita dapat mendeploy suatu aplikasi dengen menggunakan salah satu layanan bernama Netlify.

## CSS
CSS adalah singkatan dari *Cascading Style Sheets* yaitu bahasa yang digunakan untuk menentukan tampilan dan format halaman website, misalnya jenis font, warna tulisan, dan latar belakang halaman.
##### 3 cara menggunakan CSS, yaitu:
1. Inline: menggunakan css langsng di atribute element html.
2. Internal: menggunakan tag style di bagian head.
3. External: menggunakan file css terpisah dengan html.

CSS syntax terdiri dari selector, property, dan value.
contohnya 

    .title{
        color: red;
    }

### Flexbox
+ Flexbox adalah konsep layout pada CSS yang digunakan untuk mengatur elemen atau container pada halaman web.
+ Untuk tampilan contoh penggunaan bisa di lihat [disini](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) atau [disini](https://www.w3schools.com/css/css3_flexbox.asp)


## Algoritma dan Data Structures
+ Algoritma adalah langkah langkah yang disusun untuk menyelesaikan suatu masalah.
+ Struktur Data adalah cara menyimpan dan mengatur data secara terstruktur pada sistem komputer atau database sehingga lebih mudah diakses.
###### Kenapa harus menggunakan algoritma?
+ Menyederhanakan program agar lebih runtut.
+ Mempermudah membuat program sehingga lebih efisien.
##### Contoh Algoritma
    baca nama dan nilai mahasiswa.
    jika nilai >= 60 maka
    keterangan = lulus
    tetapi jika
    keterangan = tidak lulus
    tulis keterangan
    
##### Bentuk Pseudocode
    read (nama, nilai)
    if nilai >= 60 then
    keterangan = ‘lulus’
    else
    keterangan = ‘tidak lulus’
    write(nama, keterangan)

##### Bentuk Program Javascript
    let nama = andi;
    let nilai = 95;
    if (nilai >= 60) {
      console.log("lulus");
    } else {
      console.log("tidak lulus");
    }



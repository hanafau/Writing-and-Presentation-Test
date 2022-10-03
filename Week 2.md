# Writing Week 2
----------------------------------------------------------
## **JavaScript**
+ JavaScript adalah bahasa pemrograman untuk membuat website yang interaktif. JavaScript juga dapat dikombinasikan dengan HTML dan CSS.
+ Program JavaScript dapat kita buat menggunakan text editor seperti visual studio code dan untuk menjalankannya kita bisa menggunakan web browser.

#### Tipe Data
+ number : tipe data yang isinya berupa angka termasuk angka desimal.
+ string : tipe data yang isinya bisa berupa huruf, angka, dan simbol. Dalam penulisan dilengkapi dengan tanda petik (' ') atau tanda kutip (" ").
+ boolean : tipe data yang memiliki nilai true dan false.
+ null : tipe data yang tidak memiliki nilai.
+ undefined : tipe data yang merepresentasikan varibel/data yang tidak memiliki nilai.
+ object : tipe data yg dapat berisi berbagai nilai dan berhubungan dengan dunia nyata.

#### Operator
1. Assignment Operator (=) : digunakan untuk menyimpan sebuah nilai pada variabel.
2. Mathematical Assignment Operator : digunakan untuk memberikan tugas kepada variabel untuk melakukan operasi.
3. Increment dan Decrement : digunakan untuk menambah atau mengurangi bernilai 1.
4. Arithmetic Operator : digunakan untuk melibatkan operasi matematika.
    + Tambah (+)
    + Kuramg (-)
    + Perkalian (*)
    + Pembagian (/)
    + Modulus (%)
5. Comparison Operator : operator yang membandingkan satu nilai dengan nilai lainnya. hasilnya antara true atau false.
    + Lebih kecil dari : <
    + Lebih besar dari: >
    + Lebih kecil atau sama dengan: <=
    + Lebih besar atau sama dengan: >=
    + Sama dengan: ===
    + Tidak sama dengan: !==
6. Logical Operator : digunakan untuk menyatakan suatu kondisi.
    + AND : &&
    + OR : ||
    + NOT : !
 
## **Conditional**
Conditional merupakan statement percabangan yang menggambarkan suatu kondisi. biasanya statement ini mengecek dan menjalankan perintah berdasarkan kondisi.
**Contoh**
+ If Statement
    let nilai = 50;
    if (nilai === 50){
      console.log('variabel bernilai 50');
    }

+ If Else Statement
    let nama = "Andi";
    if (nama == "Andi"){
        console.log("nama dia andi")
    } else {
        console.log("namanya bukan andi")
    }

+ If Else If Statement
let nilai = 92;
    if (nilai >85){
        console.log("A")
    }
    else if (nilai >70){
        console.log("B")
    }
    else if (nilai >55){
        console.log("C")
    } else {
        console.log("D")
    }

+ Switch Case Conditional
switch case dapat digunakan saat kondisi dan percabangan terlalu banyak.
  let warna = "merah";
  	switch (warna){
  		case "merah":
  			console.log ("warna merah tanda berhenti");
  			break;
  		case "kuning":
  			console.log ("warna kuning tanda hati-hati");
  			break;
  		case "hijau":
  			console.log ("warna hijau tanda jalan");
  			break;
  		default:
  		    console.log ("warna tidak ada");
  	}

+ Ternary Operator merupakan short-syntax dari statement if else.
    let lapar = true;
    lapar ? console.log("aku belum makan") : console.log("aku sudah makan");


## **Looping**
Looping adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi stop/berhenti tercapai.
jenis looping dan contohnya antara lain:
1. for loop merupakan instruksi pengulangan yang dapat kita berikan pada program.
    + contoh program
    let angka=1;
    for(angka; angka<5; angka++){
        console.log(angka);
    }

2. while loop akan menjalankan pengulangan apabila kondisi bernilai TRUE.
    + contoh program while
    let angka=1;
    while (angka<=5){
        console.log(angka);
        angka++;
    }

    + contoh program do while
    angka= 1 ;
    do {
        console.log(angka);
        angka ++ ;
    } while (angka <= 5)
    
## **Scope and Function**
#### Scope
+ Scope adalah konsep dalam flow data variabel. 
+ Scope digunakan untuk menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.
+ Scope ada 2 macam yaitu global scope dan local scope
    1. Global scope yaitu variabel yang dapat diakses dimanapun dalam suatu file.
    contoh programnya:
    let myName = "zahra" ; 
    function greeting() {
        return myName;
    }
        console.log(myName); //output: zahra

    2. Local scope yaitu mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping.
    contoh programnya:
    function greeting() {
    let myName = "zahra" ; 
    return myName;
    }
    console.log(greeting()); //output: zahra
    console.log(myName); //output: eror
    
#### Function
Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task. dalam 1 function yang sudah kita buat nantinya dapat kita menggunakannya kembali.
+ cara membuat function
    function say(){
        return 'hallo';
    };
+ cara memanggil function 
    say();
    console.log(say()); // output: hallo

#### Parameter dan Argumen
+ argumen adalah nilai yang digunakan saat memanggil function.
    + contoh program
    function tambah (a,b) {
        return a + b;
    }
    console.log (tambah(10, 10)); // output: 20
+ parameter berfungsi untuk menerima inputan data yang digunakan untuk melakukan task.
    + contoh program
    function say(nama = 'gibran'){
        return 'hallo ' + nama;
    }
    console.log(say('levi')); //output: hallo levi
    console.log(say()); //output: hallo gibran

## **DOM**
DOM adalah jembatan antara bahasa pemrograman dengan HTML agar dapat berinteraksi. penggunaan DOM juga membuat developer dapat memanipulasi konten, struktur, dan style situs web.
+ Cara memanggil DOM antara :
    + Memanggil tag HTML berdasarkan ID console.log(document.getElementByID("header))
    + Memanggil tag HTML berdasarkan Class Name console.log(document.getElementByClassName("text-color-red"))
    + Memanggil tag html berdasarkan query selector console.log(document.querySelector("#header"))
+ DOM event adalah aktivitas yang dikerjakan pada halaman web.
jenis HTML DOM Event antara lain:
    + Click
    + Scroll
    + Change
    + Focus
    + Hover
    + Submit
    + Blur

+ Menangkap Interaksi User
    + Element.addEventListener(“event”)
    + Element.onevent
    
+ EventListener
    + Contoh EventListener-Click
    misalkan kita mempunyai element <input id=”user-input” />  dan <button id=”alert-button”>show</button>. 
    lalu memanggil element berdasarkan id
    const input = document.getElementById(“user-input”)
    const button = document.getElementById(“alert-button”)
    saat ditambahkan eventListener menjadi
    button.addEventListener(“click”, function() {
	alert(input.value)
    })

    + EventListener - Blur
    event di mana sebuah element kehilangan fokus dari user (misal user klk mouse di luar element tersebut atau user klik tab untuk berpindah element).
    contohnya:
    Misalkan kita ingin memvalidasi isi dari <input id=”username” /> agar panjangnya minimal 6 karakter.
    lalu memanggil element berdasarkan id
    const input = document.getElementById(“username”)
    saat ditambahkan eventListener menjadi
    input.addEventListener(“blur”, () => {
    	if(input.value.length < 6) alert(“Panjang username minimal 6”)
    })
    
    + Contoh EventListener - Form Submission
    Misalkan kita mempunyai element beberapa input dalam sebuah form <input name=”email /> dan <input type=”password” name=”password” />.
    const form = document.getElementById(“form”)
    form.addEventListener(“submit”, function(event) {
	event.preventDefault()
	const formData = new FormData(form)
	const values = Object.fromEntries(formData) // { email: ... }
})

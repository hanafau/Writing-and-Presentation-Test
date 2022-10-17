# Writing Week 3
----------------------------------------------------------
## **Array**
Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya. Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya. Data array dapat dihitung mulai dari index ke-0.

##### Contoh Array
```
let data=['ini', 'nilai', 'dari', 'array'];
console.log(data); //outputnya: ['ini', 'nilai', 'dari', 'array']
```

#### Method Array
+ Push adalah method untuk menambahkan item array pada urutan yang paling akhir.
    ```
    let cars = ['tesla', 'honda', 'toyota'];
    cars.push('hyundai')
    console.log(cars) // output:['tesla','honda','toyota','hyundai']
    ```
+ Pop adalah method yang menghapus item array index terakhir.
    ```
    let cars = ['tesla', 'honda', 'toyota'];
    cars.pop()
    console.log(cars) // output: ['tesla','honda']
    ```
+ Shift adalah method untuk menghapus item Array pada index pertama
    ```
    let cars = ['tesla', 'honda', 'toyota'];
    cars.shift()
    console.log(cars) // output: ['honda','toyota']
     ```
+ Unshift adalah method untuk menambahkan array pada index pertama
    ```
     let cars = ['tesla', 'honda', 'toyota'];
     cars.unshift('hyundai')
     console.log(cars) // output:['hyundai','tesla','honda','toyota',]
     ```
+ Sort adalah method untuk mengurutkan array secara ascending atau descending
    ```
    const numbers = [1,3,5,2,4];
    numbers.sort();
    console.log(numbers) // output : [1,2,3,4,5]
    ```

##### Looping pada Array
+ forEach() adalah method untuk melakukan looping pada setiap elemen array.
forEach() digunakan jika hanya memerlukan looping untuk menampilkan saja atau menyimpan ke database.
 **Contoh**
    ```
    const cars = ['tesla', 'honda', 'toyota'];
    cars.forEach(element => {
        console.log(element); //output: ['tesla', 'honda', 'toyota']
    });
    ```

+ map() adalah method untuk melakukan perulangan/looping dengan membuat array baru.
 map() digunakan jika akan melakukan operasi pada array seperti yang dapat mengubah nilai array sebelumnya.
**Contoh**
    ```
    let arr = [1,2,3,4,5];
    let doubled = arr.map(num => {
        return num * 2;
    });
    console.log(doubled); //output: ['2', '4', '6', '8', '10']
    ```
## **Multidimensional Array**
Multidimensional Array bisa dianalogikan dengan array of array atau ada array di dalam array.
**Contoh**
```
let inventory = [
['kaos oversize', 50],
['kemeja', 45]
['sepatu', 50],
['celana', 20]
];
console.log(inventory[1][0]);
```

## **Object**
Object adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method)
Properti adalah data lengkap dari sebuah object.
Method adalah action dari sebuah object. 

+ Contoh object
    ```
    let person = {
        name : 'Gibran',
        age : 7,
        isVerified: true
    }
    ```
+ Cara mengakses object
    ```
    let person = {
        name : 'Gibran',
        age : 7,
        isVerified: true
    }
    console.log(person);
    ```

+ Cara mengakses properti pada object
    ```
    let person = {
        name : 'Gibran',
        age : 7,
        isVerified: true
    }
    console.log(person.name)
    ```

+ Update object
Object dapat mengupdate value dari key yang sudah tersedia
Object dapat menambah key dan value baru
    ```
    let person = {
        name : 'Gibran',
        age : 7,
        isVerified: true
    }
    person.age = 8;
    console.log(person);
    ```

+ Delete object properti
    ```
    let person = {
        name : 'Gibran',
        age : 7,
        isVerified: true
    }
    delete person.age;
    console.log(person);
    ```

## **Recursive**
Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu.
**Contoh**
```
function pow(x,n) {
    if (n=1){
        return x;
    } else {
        return x * pow(x, n-1);
    }
}
console.log(pow(2,3)) // output: 8
```

## **Asynchronous**
+ Asynchronous adalah sebuah teknik yang menyelesaikan fungsi secara paralel atau bisa dijalankan dalam waktu yang bersamaan.
+ Asynchronous - Promise merupakan suatu object dan digunakan hanya untuk satu event dengan menyimpan hasil dari sebuah operasi asynchronous baik itu hasil yang diinginkan (resolved value) atau alasan kenapa operasi itu gagal (failure reason).
+ Asynchronous - Async-Await merupakan fitur yang hadir sejak ES2017 bekerja dengan cara menunda eksekusi hingga proses asynchronous selesai
+ Asynchronous - Fetch merupakan cara baru dalam melakukan network request yang memanfaatkan sebuah Promise dalam penggunaanya. Karen Fetch mengembalikan sebuah Promise maka respon handling yang digunakan adalah then jika promise mengembalikan resolve dan catch jika promise mengembalikan nilai reject

## **Web Storage**
Web Storage adalah wadah untuk sebuah data yang digunakan untuk penyimpanan data yang terikat di browsernya.
Web Storage yang umumnya digunakan adalah : 
+ Local Storage : data yang tersimpan tidak memiliki waktu expired (tidak ada batasan waktu penyimpanan)
+ Session storage : data yang tersimpan akan hilang ketika kita menutup browser yang akan kita gunakan.
+ IndexDB
+ Cookies

Cara menyimpan data pada local storage
```
let token = "coba" //key
localStorage.setItem("token", token);
```
Cara mengambil token
```
localstorage.getItem("token", token);
console.log(localStorage.getItem('token");
```
Cara menghapus data
```
localStorage.removeItem("token")
```

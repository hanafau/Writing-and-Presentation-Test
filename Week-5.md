# Writing Week 5

## **React.js**
+ React JS merupakan library single page aplication untuk mempermudah dalam membuat project react.
+ React JS membagi 1 tempilan website menjadi komponen kecil-kecil.
+ React JS dapat digunakan pada aplikasi bersekala kecil, besar, dan kompleks.
+ File extension dari javascript pada react adalah JSX

#### Cara mengakses React JS
+ instal node.js [disini](https://nodejs.org/en/download/)
+ install create react app
    ```npm install -g create-react-app```
+ membuat project react
    ```npx create-react-app [name-project]```
+ menjalankan react
    ```npm start```

#### Component
+ Component pada React JS merupakan core pada React JS yang bersifat enkapsulasi atau pembungkus pada react dimana dalam 1 page dapat terdiri dari beberapa component.
+ Cara membuat component ada 2 yaitu:
    + menggunakan function
    + menggunakan class 
+ Component hanya bisa menggunakan satu element yaitu ```<></>``` atau ```<div></div>```

#### State dan Props 
+ State dan props berhubungan dengan statefull component dan stateless component.
+ Stateless component berarti tidak memiliki state, hanya memiliki props.
+ Statefull berarti memiliki state dan bisa mengirim state tersebut ke component.
+ Props merupakan data yang dapat kita kirimkan dari suatu component ke component lain.
+ State adalah  digunakan untuk menghandle data yang sifatnya berubah-ubah dan data yang bersifat private yang hanya dapat diakses oleh component tersebut saja.

#### Lifecycle
+ Lifecycle adalah siklus hidup pada React js.
+ Struktur Lifecycle :
    + Constructor: inisialisasi struktur data pada suatu component.
    + Function : fungsi yg dibutuhkan pada komponen.
    + Render: proses return atau mengembalikan component asli.
+ Jenis - jenis Lifecycle Component Class:
    + componentDidMount adalah ketika memuat aplikasi sebelum di render.
    + componentWillMount adalah ketika aplikasi dimuat setelah proses render dilakukan.
    + Updating : Ketika component di update atau diubah.
    + Unmount : Proses menghancurkan component yang sebelumnya di definisikan.
    
#### Styling CSS
Contoh menambahkan style pada react dengan cara inline.
    
    class MyHeader extends React.Component {
        render() {
        return (
        <div>
        <h1 style={{backgroundColor: "lightblue"}}>Hello Style!</h1>
        <p>Add a little style!</p>
        </div>
        );
       }
    }
    
#### Hooks
+ Hooks merupakan sebuah fitur yang baru yang memudahkan functional component agar bisa menggunakan state dan lifecycle lainnya. 
+ Hooks yang sering digunakan adalah useState dan useEffect.
+ useState biasanya digunakan untuk penyimpanan data pada form yang selanjutnya data tersebut akan di post ke api lalu diproses.
+ Contoh
    ```
    import {useState} from "react";
    function App(){
        const [nama, SetNama] = useState("Gibran");
    return (
        <div className="App">
            <p>halo, saya {nama}</p>
            <button onClick={() => setNama("aska")}></button>
        </div>
        );
    }
    ```
+ useEffect merupakan hooks yang digunakan untuk menggunakan lifecycle pada functional component dengan mudah.
+ Lifecycle pada hooks hanya menggunakan useEffect yang menyatukan component DidMount, ComponentDidUpdate dan componenetWillUnmount.

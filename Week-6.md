# Writing Week 6

## **PropTypes**
+ PropTypes merupakan sebuah library yang dapat membantu dalam memeriksa tipe data props apabila tidak sesuai maka akan memunculkan pesan error.
+ Instal PropTypes
```npm install prop-types```
+ Contoh kode
    ```
    import PropTypes from "prop-types";
    
    const StudentsInfo = ({ nama, age }) => {
      return (
        <>
          <h2>{nama}</h2>
          <h2>{age + 1}</h2>
        </>
      );
    };
    
    StudentsInfo.propTypes = {
      nama: PropTypes.string,
      age: PropTypes.number,
    };
    
    export default StudentsInfo;
    
    ```
    
+ error

## **React Router**
+ React Router digunakan sebagai library React JS untuk mengarahkan website dari page satu ke page lainnya, dimana page tersebut diarahkan menggunakan URL. 
+ Cara menggunakan router
    + instal router
    ```npm install react-router-dom@6```
    + menambahkan import pada main.jsx
    ```import { BrowserRouter } from "react-router-dom"```
    + menambahkan pembungkus untuk data yang ingin di routing
        ```
        <BrowserRouter>
        ....
        </BrowserRouter>
        ```
        
+ <Link> merupakan double tag yang bertujuan untuk mengarahkan suatu menu ke menu lain sifatnya seperti seperti tag <a> </a>.
+ to merupakan atribut untuk mengarahkan ke suatu path / nilai untuk ke suatu page.

+ contoh program 
    ```
    import { Routes, Route, Link } from "react-router-dom";
    import HomePage from "./pages/HomePage";
    import AboutPage from "./pages/AboutPage";
    
    function App() {
      return (
        <>
          <nav>
            <Link to={"/"}>Home | </Link>
            <Link to={"/about"}>About</Link>
          </nav>
    
          <Routes>
            <Route path="/" element={<HomePage />} />
            <Route path="/about" element={<AboutPage />} />
          </Routes>
        </>
      );
    }
    
    export default App;

    ```
    
+ contoh program nested route
    ```
    import { Routes, Route, Link } from "react-router-dom";
    import HomePage from "./pages/HomePage";
    import AboutPage from "./pages/AboutPage";
    import AboutStudents from "./pages/AboutStudents";
    import AboutTeacher from "./pages/AboutTeacher";
    
    function App() {
      return (
        <>
          <nav>
            <Link to={"/"}>Home | </Link>
            <Link to={"/about"}>About</Link>
          </nav>
    
          <Routes>
            <Route path="/" element={<HomePage />} />
            <Route path="/about" element={<AboutPage />}>
              <Route path="students" element={<AboutStudents />} />
              <Route path="teacher" element={<AboutTeacher />} />
            </Route>
          </Routes>
        </>
      );
    }
    
    export default App;
    
    ```
    
## **Redux** ##
+ Redux berguna untuk mengelola perubahan state yang terjadi didalam aplikasi.
+ Komponen redux yaitu:
    - Action:  sebuah function yang mereturn sebuah objek.
    - Reducer: sebuah fungsi yang tugasnya untuk mengolah state yang ada di store.
    - Store: tempat untuk menampung state
+ Instal react-redux
```install redux react-redux```
+ Contoh 
    ```
    //components
    import React from "react";
    import { useDispatch, useSelector } from "react-redux";
    import { decrement, increment } from "../redux/action/counterAction";
    
    function Counter() {
      const dispatch = useDispatch();
      const { count } = useSelector((state) => state);
    
      return (
        <div>
          <button onClick={() => dispatch(decrement())}>-</button>
          <span>{count}</span>
          <button onClick={() => dispatch(increment())}>+</button>
        </div>
      );
    }
    
    export default Counter;
    
    -----------------------------------------------
    //action
    export const INCREMENT = "INCREMENT";
    export const DECREMENT = "DECREMENT";
    
    export function increment() {
      return {
        type: INCREMENT,
      };
    }
    
    export function decrement() {
      return {
        type: DECREMENT,
      };
    }
    -----------------------------------------------
    //reducer
    import { DECREMENT, INCREMENT } from "../action/counterAction";
    
    const initialState = {
      count: 0,
    };
    
    function counterReducer(state = initialState, action) {
      switch (action.type) {
        case INCREMENT:
          return {
            count: state.count + 1,
          };
        case DECREMENT:
          return {
            count: state.count - 1,
          };
        default:
          return state;
      }
    }
    
    export default counterReducer;
    -----------------------------------------------
    //store
    import { createStore } from "redux";
    import counterReducer from "../reducer/counterReducer";
    
    const store = createStore(counterReducer);
    
    export default store;

    ```

## **Redux Thunk**
+ Redux Thunk adalah middleware yang memungkinkan kita memanggil pembuat aksi yang mengembalikan fungsi sebagai ganti objek aksi. Fungsi itu menerima metode pengiriman penyimpanan, yang kemudian digunakan untuk mengirim aksi sinkron di dalam isi fungsi setelah operasi asinkron selesai.
+ Instal Thunk
    ```
    npm install redux-thunk
    ```
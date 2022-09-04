# REACT JS DASAR
## Introduction
React JS adalah framework view library Javascript untuk membuat tampilan pada website. React JS dibuat oleh Tim Engineer Facebook dan digunakan pada sisi front-end. Menurut Google Trends, React JS masih unggul di antara framework Javascript lainnya seperti Vue dan Angular.

Bberapa keunggulan dari React JS adalah sebagai berikut:

1. Membuat aplikasi front-end menjadi lebih cepat walaupun harus menghandle berbagai data. 
2. Bisa diterapkan konsep Modular Javascript. React JS membagi tampilan pada website menjadi komponen-komponen kecil.
3. Dapat digunakan pada aplikasi berskala kecil hingga besar dan kompleks.

### Instalasi React JS
#### Install Node JS
![](assets/a.PNG)

https://nodejs.org

#### Gunakan Library `create-react-app`
![](assets/b.PNG)

https://create-react-app.dev

Pada CMD, kita juga bisa ketikkan perintah berikut

    npm install -g create-react-app

#### Check Node dan NPM
Ketikkan perintah berikut pada Command Prompt (CMD)
 
    node --version
    npm --version
    
### Inisialisasi Proyek
Buka Command Prompt (CMD) kemudian ketikkan perintah berikut:

    npx create-react-app [name-project]

Contoh :

    npx create-react-app example-project-1

Kemudian install library react-router dengan perintah:

    npm install react-router-dom@6

### Menjalankan Proyek
Buka folder proyek yang telah dibuat, kemudian jalankan CMD pada folder tersebut. Ketikkan perintah

    npm run start

Setelah itu secara otomatis akan diarahkan ke tampilan browser.

## Component
Component merupakan salah satu core dari React JS. Component membagi UI dalam satuan-satuan kecil, artinya dalam 1 page terdapat beberapa component yang bisa kita buat. Component dibuat jika component tersebut bersifat reusable code. Pada sebuah project, kita membuat component jika component tersebut akan dibutuhkan di page lain.

### Class Component dan Functional Component 
React JS merupakan component based yang dapat dibagi menjadi 2 bagian, yaitu class component dan functionanl component.

#### Class Component
Contoh penulisan class component:

    import React, {Component} from "react";

    class CourseCard extends Component {
        render() {
            return (
                <div>

                </div>
            )
        }
    }

    export default CourseCard;

#### Functional Component
Penulisan functional component ada 2, yaitu function biasa dan arrow function.
1. Function biasa
        
        import React from 'react'

        function CourseCard() {
            return (
              <div>CourseCard</div>
            )
        };

        export default CourseCard;

2. Arrow function

        import React from "react";

        const CourseCard = () => {
            return(
                <>
                <h2>My Courses</h2>
                </>
            )
        };

        export default CourseCard;

Dalam 1 file component hanya memiliki 1 export default. Jika memiliki lebih dari 1 fungsi dalam 1 file component kita bisa menggunakan export agar bisa di render. Satu component hanya bisa me-render 1 element, jadi jika lebih dari satu element, harus dibungkus dengan parent element yaitu `<></>` atau `<div></div>`.

### Props dan State 
State dan props berhubungan dengan statefull component dan stateless component. Stateless component berarti tidak memiliki state, hanya memiliki props. Statefull berarti memiliki state dan bisa mengirim state tersebut ke component.

#### Props
Props digunakan agar component memiliki data yang dinamis yang dikirim dari component lain (bisa reusable).

#### State
State adalah data lokal. Data yang ada pada lokal component, ketika ada perubahan data, maka akan di-render ulang. Data ini hanya tersedia untuk component tersebut dan tidak bisa di akses dari component lain. State ini hanya berlaku untuk componentnya sendiri.

### Styling CSS
Kalau di React JS untuk styling bisa menggunakan 3 cara, yaitu:
- External CSS
- Internal CSS
- Inline Style

Selain 3 cara di atas, agar lebih mudah kita bisa menggunakan bootstrap. Jika kita ingin menginstall bootstrap pada project react, ketikkan perintah berikut pada CMD

    npm i bootstrap@5.2.0
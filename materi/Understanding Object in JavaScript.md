### Introduction

Kali ini kita akan berkenalan dengan tipe data _objek_. Sebuah tipe data yang sangat berguna dalam pengembangan aplikasi dengan JavaScript. objek mampu menyimpan nilai dari beragam tipe data dan membentuk data yang lebih kompleks.

Dalam kehidupan nyata, kita sering menjumpai objek. Objek adalah segala sesuatu yang ada di dunia ini. Entah itu benda mati ataupun makhluk hidup. Semuanya objek.

## Apa itu Objek di Javascript dan Bagaimana cara Membuatnya?

Objek sebenarnya adalah sebuah variabel yang menyimpan nilai (properti) dan fungsi (method).

![](https://i.imgur.com/oMy4aXj.png)

Untuk menetapkan objek pada sebuah variabel kita gunakan tanda kurung kurawal {}.

```JavaScript
const car = {}
```

objek berisi pasangan key dan value yang juga dikenal dengan properti. 
contoh:

![](https://i.imgur.com/nRfPsci.png)

Key harus berupa string dan dituliskan sebelum titik dua (:), lalu diikuti dengan value-nya. Meskipun key merupakan string, kita tidak perlu menuliskan tanda petik kecuali ada karakter khusus seperti spasi.

Dari objek mobil sebelumnya kita dapat menuliskan ke dalam kode seperti berikut

```JavaScript
const car = {type: "Fiat", model: "500", weight: "850Kg"}
```

Kode sebelumnya bisa ditulis seperti berikut

```JavaScript
const car = {    
    type: "Fiat", 
    model: "500", 
    color: "white",
}
```

### Apa Perbedaan Properti dan Method?

Pada kode-kode di atas, kita telah membuat properti saja. 

Properti adalah ciri khas dari objek (variabel). Sedangkan method adalah perilaku dari objek (fungsi).

Lalu bagiaman kita membuat method di dalam objek? Method dapat dibuat dengan cara mengisi nilai (value) dengan sebuah fungsi.

```javascript
const car = {
    // properti
    type: "Fiat", 
    model: "500", 
    color: "white",

    // method
    start: function(){
        console.log("ini method start");
    },
    drive: function(){
        console.log("ini method drive");
    },
    brake: function(){
        console.log("ini method brake");
    },
    stop: function(){
        console.log("ini method stop");
    }
    
};
```

### Cara Mengakses Properti dan Method Objek

Bagaimana cara mengakses properti dan method dari objek? Caranya menggunakan tanda titik atau dot (.), lalu diikuti dengan nama properti atau method.

```javascript
console.log(car.type);
console.log(car.color);

car.start();
car.drive();
```

Untuk mengakses properti, kita cukup gunakan nama `objek.properti`. Sedangkan untuk method, kita harus menggunakan tanda kurung. Ini menyatakan kalau kita ingin mengeksekusi fungsi.

## Modifikasi Properti Objek

Setelah mempelajari bagaimana membuat objek dan menampilkan properti di dalamnya, selanjutnya kita akan memodifikasi sebuah objek. Untuk mengubah nilai properti di dalam objek kita gunakan _assignment operator_ (=).

```javascript
const car = {    
    type: "Fiat", 
    model: "500", 
    color: "white",
}


car.color = "Red"
car["model"] = "12000"
console.log(car)
```


## Tugas

Buatlah sebuah objek dengan nama person yang memilii properti `name`, `age`, `sex` dan buatkakan method objek person `makan`, `minum`, `tidur`


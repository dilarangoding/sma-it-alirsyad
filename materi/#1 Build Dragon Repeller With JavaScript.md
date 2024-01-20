# Build RPG - Dragon Repeller With JavaScript


### Introduction

Dalam project latihan ini, Kita akan mempelajari konsep pemrograman dasar dalam JavaScript dengan membuat coding Role Playing Game Kita sendiri. Kita akan belajar cara bekerja dengan array, string, objek, fungsi, perulangan, pernyataan if/else, dan banyak lagi.

Hasil akhir dari project ini kita akan mendapatkan pemahaman mengenai dasar pemograman dalam JavaScript. 

![image alt text](https://imgur.com/RoQyqYQ.gif "Final Result")

## Prerequisites

Sebelum mulai kita perlu menyiapkan:
* Teks Editor [VS Code]
* Web Browser [Google Chrome]
* Live Server [Extension VS Code]

## Step 1 — Clone Template Project

Pertama silahkan clone project [Dragon Repeller](https://github.com/dilarangoding/sma-it-alirsyad/tree/master/project) kita. Selanjut nya buat folder dengan nama dragon-repller di komputer kita.

![image alt text](https://imgur.com/S3JB28g.png "Struktur Folder")

## Step 2 — Declaring Variable

Buka file script.js dan kita deklrasikan beberapa variable

```
var xp = 0;
var health = 100;
var gold = 50;
var currentWeapon = 0;
```

Kita telah mendeklarasikan variable dengan keyword `var`. Namun, di JavasScript modern lebih disarankan menggunakan keyword `let` sebagai gantinya. Hal ini akan memberbaiki beberapa perilaku yang tidak biasa pada `var` yang dapat membuat kode kita sulit untuk di-debug

```
let xp = 0;
let health = 100;
let gold = 50;
let currentWeapon = 0;
```

Selanjutnya tambahkan 3 variabel lagi dengan nama `fighting`, `monsterHealth` dan `inventory` tapi jangan inisialisasi variablenya.

```
let fighting;
let monsterHealth;
let inventory;
```

pada variable `inventory` assign array dengan value `stick`, `dagger`, dan`sword`
```
let inventory = ["stick","dagger","sword"];
```

Untuk saat ini, kita ingin pemain memulai hanya dengan `stick`. Ubah array inventory untuk menjadikan `stick` sebagai satu-satunya nilai.

```
let inventory = ["stick"];
```

Full kode variable
```
let xp = 0;
let health = 100;
let gold = 50;
let currentWeapon = 0;
let fighting;
let monsterHealth;
let inventory = ["stick"];
```

## Step 3 — DOM In JavaScript
Buat variabel button1 dan gunakan querySelector() untuk menetapkannya sebagai elemen dengan id button1. Perlu diingat bahwa pemilih id CSS diawali dengan tanda #

```
const button1 = document.querySelector("#button1");
```

Gunakan querySelector() untuk mendapatkan dua elemen button lainya dengan menggunakan id button2 dan button3. Simpan dalam variabel bernama button2 dan button3. Ingat untuk menggunakan const
```
const button2 = document.querySelector("#button2");
const button3 = document.querySelector("#button3");
```
Sama seperti yang kita lakukan pada button, buat variae untuk id berikut menggunakan querySelector():

`text`, `xpText`, `healthText`, `goldText`, `monsterStats`, dan `monsterName`.

```
const text = document.querySelector("#text");
const xpText = document.querySelector("#xpText");
const healthText = document.querySelector("#healthText");
const goldText = document.querySelector("#goldText");
const monsterStats = document.querySelector("#monsterStats");
const monsterName = document.querySelector("#monsterName");
```

Terakhir, gunakan `querySelector()` untuk mendapatkan elemen `#monsterHealth`. Karena Kita telah mendeklarasikan variabel `monsterHealth` sebelumnya, Kita perlu menggunakan nama variabel yang berbeda untuk elemen ini.

Deklarasikan variabel baru dengan kata keyword `const` dan beri nama `monsterHealthText`.


```
const monsterHealthText = document.querySelector("#monsterHealth");
```

## 4 - Make it Interactive

Function adalah special tools yang memungkinkan kita menjalankan bagian kode pada waktu tertentu. kita dapat mendeklarasikan function menggunakan keyword function.

Buat function goStore, keluarkan pesan `Going to store.` ke console

```
function goStore(){
console.log("Going to store.");
}
```



Kemudian buat function `goCave` yang mencetak `Going to cave.` di console.

```
function goCave(){
console.log("Going to cave.");
}
```

sekarang buat function `fightDragon` yang mencetak `Fighting dragon.` di console

```
function fightDragon(){
  console.log("Fighting dragon.")
}
```

button1 merepresentasikan elemen tombol pertama Kita. Elemen ini memiliki properti khusus yang disebut onclick, yang dapat Kita gunakan untuk menentukan apa yang terjadi ketika seseorang mengklik tombol tersebut.

Gunakan notasi titik untuk mengatur properti onclick pada button1 kita ke referensi fungsi goStore. Perhatikan bahwa button1 sudah dideklarasikan, jadi Kita tidak perlu menggunakan let atau const

```
 button1.onclick = goStore;
```

Dengan menggunakan sintaks yang sama, atur properti onclick pada button2 dan button3 masing-masing menjadi goCave dan fightDragon.

```
button2.onclick = goCave;
button3.onclick = fightDragon;
```
Setelah Kita selesai melakukannya, buka konsol Kita dan coba klik tombol-tombol pada project Kita.

Properti innerText di DOM mengontrol teks yang muncul dalam elemen HTML.

-----------------------------------------------------

Ketika seorang pemain mengklik button Go to store, kita ingin mengubah button dan teks. Hapus kode di dalam function goStore dan tambahkan baris yang memperbarui teks button1 dengan `Buy 10 health (10 gold)`

```
function goStore() {
  button1.innerText = "Buy 10 health (10 gold)";
}
```

Sekarang, tambahkan kode untuk memperbarui teks button2 menjadi `Buy weapon (30 gold)` dan button3 menjadi `Go to town square`.

```
  button2.innerText = "Buy weapon (30 gold)";
  button3.innerText = "Go to town square";
```
## Conclusion

Pada materi ini kita dapat pemahaman mengenai materi `Variable`, `Array`, `DOM`, `Event Handling` dan juga `Function`  pada JavaScript

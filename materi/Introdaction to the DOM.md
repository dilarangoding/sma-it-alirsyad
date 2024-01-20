# Introduction to the DOM

### Introduction

Document Object Model, biasanya disebut sebagai DOM, adalah bagian penting untuk membuat web menjadi interkatif. DOM adalah interface yang memungkinkan JavaScript untuk memanipulasi konten, struktur, dan style web.

Hampir setiap kali web melakukan suatu tindakan, seperti menampilkan kesalahan saat user mengirim form yang tidak lengkap atau mengganti navigasi, itu adalah hasil dari JavaScript yang mengakses dan memanipulasi DOM.


## What is the DOM?

Struktur pada suatu website disusun oleh HTML dan juga CSS secara statis. Supaya website menjadi dinamis  bisa mengunakan JavaScript. DOM bisa dibuat untuk penghubung JavaScript dengan HTML atau CSS. DOM berperan membuat JavaScript dapat mengakses dan mengubah seluruh elemen statis yang terdapat di suatu halaman website.

![The Dom](https://i.imgur.com/j19bFuy.png)

##  How To Access Elements in the DOM

1. **Accessing Elements by ID**: Cara termudah untuk mengakses sebuah elemen dalam DOM adalah dengan ID uniknya. Kita bisa  mendapatkan elemen berdasarkan ID dengan method getElementById()
 ```
 const demoId = document.getElementById('demo');
 ```
2. **Accessing Elements by Class**: Attribute class pada html digunakan untuk mengakses satu atau beberapa elemen tertentu di dalam DOM. Kita bsia mendapatkan semua elemen dengan nama class tertentu dengan method getElementsByClassName()
```
<div class="demo">Access me by class (1)</div>
<div class="demo">Access me by class (2)</div>
const demoClass = document.getElementsByClassName('demo');
```
3. **Accessing Elements by Tag**: Kita bisa mengakses elemen HTML dengan nama tag HTML-nya. Kita mengakses elemen berdasarkan tag dengan method getElementsByTagName()
```
<article>Access me by tag (1)</article>
<article>Access me by tag (2)</article>
const demoTag = document.getElementsByTagName('article');
```
4. **Query Selectors**: Cara mengambil elemen HTML menggunakan QuerySelector ini memungkinkan Kita untuk dapat mengembalikan pada elemen yang pertama. Pengembalian ini sesuai dengan SS Selector yang sudah Kita tentukan sebelumnya. Kita bisa mendapatkan elemen memakai ID kelas, tag atau semua CSS Selector yang valid
```
<div id="demo-query">Access me by query</div>
<div class="demo-query-all">Access me by query all (1)</div>
<div class="demo-query-all">Access me by query all (2)</div>

const demoQuery = document.querySelector('#demo-query');
const demoQueryAll = document.querySelectorAll('.demo-query-all');
```
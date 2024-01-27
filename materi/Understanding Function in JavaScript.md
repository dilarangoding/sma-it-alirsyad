# Understanding Function in JavaScript


### Introduction

Fungsi merupakan bagian penting dalam bahasa pemrograman. Tanpa sadar, sebenarnya kita sudah menggunakan sebuah fungsi pada kode kita sebelumnya. log() pada console.log() merupakan sebuah function yang berguna untuk menampilkan data pada konsol.


## What is Function?

Fungsi adalah sub-program yang bisa digunakan kembali baik di dalam program itu sendiri, maupun di program yang lain. Pada dasarnya fungsi dibuat agar kode program kita dapat lebih mudah digunakan kembali dan lebih mudah dipahami

## Defining a Function

Fungsi dideklarasikan dengan keyword function dan nama fungsinya. Nama fungsi selalu diikuti dengan tanda kurung (parentheses) tanpa spasi, lalu terdapat sepasang kurung kurawal yang berisi logika dari fungsi tersebut.

```JavaScript

	function nameOfFunction() {
		// Code to be executed
	}
	
```

Contoh fungsi untuk mencetak kata `Hello World` di console

```JavaScript

	// Initialize greeting function
	function greet() {
		console.log("Hello, World!");
	}


```

Pada contoh kode diatas kita mempunyai function dengan nama `greet` function tersebut tidak akan dieksekusi sampai kita memangil function tersebut. Kita dapat memanggil sebuah function dengan menuliskan nama function diikuti dengan tanda kurung.

```JavaScript
	
	greet()
	
```

Sekarang kita dapat mendefinisikan function kita dan memanggilnya

```JavaScript

	// Initialize greeting function
	function greet() {
		console.log("Hello, World!");
	}
	
	// Invoke the function
	greet();
	

```


## Function Parameters & Arguments

Pada kode sebelumnya kita membuat function sederhana untuk mencetak `Hello, World` ke console. Dengan menggunakan parameter, kita dapat membuat fungsionalitas tambahan yang membuat kode program kita lebih fleksibel lagi. **Parameter merupakan variabel yang didefinisikan sebagai input dari sebuah fungsi.** 

Ketika user masuk ke sebuah aplikasi, kita mau program kita menyapa sesuai dengan namanya. 

Kita akan menambahkan parameter ke dalam function kita, yaitu `name`, untuk merepresentasikan nama orang yang ingin disapa.

```

	// Initialize custom greeting function
	function greet(name) {
		console.log(`Hello, ${name}!`);
	}
	

```

Kita sudah menambahkan sebuah parameter ke function kita, lalu bagaimana caranya untuk memanggil function yang memiliki parameter? Caranya cukup sederhana seperti memanggil function biasa pada umumnya namun kita perlu memberikan nilai atau argumen ke dalam function kita. **Argument merupakan nilai atau expression yang dimasukkan ke dalam fungsi**

```JavaScript
	
	// Invoke greet function with "Sammy" as the argument
	greet("Sammy");
	

```


Kode lengkapnya

```JavaScript

	// Initialize custom greeting function
	function greet(name) {
		console.log(`Hello, ${name}!`);
	}
	
	// Invoke greet function with "Sammy" as the argument
	greet("Sammy");
	

```



## Returning Values

Sebuah function dapat memiliki banyak sekali parameter (tergantung kebutuhan kita seperti apa). Dari paramter tersebut kita bisa mengolah nilai nya, agar hasil pengolahan nilai di dalam fungsi dapat digunakan untuk proses berikutnya, maka fungsi harus mengembalikan nilai.

Pengembalian nilai pada fungsi menggunakan kata kunci `return` kemudian diikuti dengan nilai atau variabel yang akan dikembalikan. Contoh:


```JavaScript

	// Initialize add function
	function add(x, y) {
		return x + y;
	}

	// Invoke function to find the sum
	add(9, 7);


```


Pada program diatas, kita mendifinisikan sebuah function dengan parameter x, y dan kemudian mengoper nilai 9, 7 ke dalam fungsi tersebut. Ketika kita menjalankan program, kita akan menerima jumlah angka-angka tersebut sebagai output.


## Conclusion

Dalam materi kali ini kita telah membahas deklarasi sebuah function, bagaimana cara menggunakan paramter dan argumen pada function dan mengembalikan nilai dari function.

Function adalah blok kode yang mengembalikan suatu nilai atau melakukan suatu tindakan, dengan begitu kode program kita menjadi lebih sederhana dan lebih mudah di-maintain

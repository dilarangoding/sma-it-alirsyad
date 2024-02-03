# Understanding Loop In JavaScript

### Introduction

Dalam pembuatan program, terkadang kita harus melakukan pengulangan suatu aksi, misalnya untuk melakukan perhitungan berulangan dengan menggunakan formula yang sama. Sebagai contoh, misalnya kita ingin membuat program yang dapat menampilkan sebuah teks "Saya berjanji tidak telat lagi" sebanya 10 kali, maka kita tidak perlu untuk menuliskan 5 buah statemen melainkan kita hanya tinggal menempatkan suatu buah statmen ke dalam struktur pengulangan. Dengan demikian program kita akan lebih efesien.

## For loop

Dari beberapa cara melakukan proses loop pada JavaScript, `for` merupakan salah satu cara yang banyak digunakan. Struktur dasar dari for tampak seperti berikut:

```JavaScript
	 for(inisialisasi variabel; test kondisi; perubahan nilai variabel) {
		  // do something
	 }
```

Berikut ini contoh penerapannya secara nyata:

```JavaScript
	for(let i = 0; i < 5; i++) {
	  console.log(i);
	}
```

Mari kita bahas sedikit demi sedikit. Terdapat tiga bagian utama dalam sintaks for di atas:

- Pertama, variabel `i` sebagai index iterasi. Pada variabel ini kita menginisialisasi nilai awal dari perulangan.
- Kedua, operasi perbandingan. Pada bagian ini, JavaScript akan melakukan pengecekan kondisi apakah perulangan masih perlu dilakukan. Jika bernilai true, maka kode di dalam blok for akan dijalankan.
- Ketiga, increment/decrement. Di sini kita melakukan penambahan atau pengurangan variabel iterasi. Jadi, pada contoh di atas variabel `i` akan ditambah dengan 1 di setiap akhir perulangan. Perubahan nilai ini penting karena jika kita mengubah nilainya, proses perulangan dapat terus berjalan selama kondisinya terpenuhi.

JIka diartikan, maka kode di atas bisa dimaknai dengan “Jika i kurang dari 5, maka tampilkan nilai i.”

## While and do-while

Metode lain untuk melakukan looping adalah dengan statement while. Sama seperti for, instruksi while mengevaluasi ekspresi boolean dan menjalankan kode di dalam blok while ketika bernilai true.

Untuk menampilkan angka 1 sampai 100 dengan while kita bisa menulis kode seperti berikut:

```JavaScript
	let i = 1;

	while (i <= 100) {
	  console.log(i);
	  i++;
	}
```

Bisa dilihat pada kode di atas bahwa looping dengan while tidak memiliki ketergantungan dengan variabel iterasi seperti pada for loop. Karena itu, meskipun while dapat melakukan perulangan yang sama dengan for, while lebih cocok digunakan pada kasus di mana kita tidak tahu pasti berapa banyak perulangan yang diperlukan.

Bentuk lain dari while adalah perulangan do-while.

```JavaScript
	let i = 1;

	do {
	  console.log(i);
	  i++;
	} while (i <= 100);
```

Kondisi pada while akan dievaluasi sebelum blok kode di dalamnya dijalankan, sedangkan do-while akan mengevaluasi boolean expression setelah blok kodenya berjalan. Ini artinya kode di dalam do-while akan dijalankan setidaknya satu kali.

## Infinite loops

Ketika menerapkan perulangan pada program, ada satu kondisi yang perlu kita hindari yaitu infinite loop. Infinite loop atau endless loop adalah kondisi di mana program kita stucked di dalam perulangan. Ia akan berjalan terus hingga menyebabkan crash pada aplikasi dan komputer kecuali ada intervensi secara eksternal, seperti mematikan aplikasi.

Kode berikut ini adalah contoh di mana kondisi infinite loop dapat terjadi:

```JavaScript
    let i = 1;

    while (i <= 5) {
      console.log(i);
    }
```

Apa yang salah dari kode di atas sehingga terjadi infinite loop?

Jawabannya adalah karena variabel `i` selalu bernilai 1. Alhasil, kondisi `i <= 5` akan selalu bernilai `true` yang mengakibatkan aplikasi akan terus mencetak 1 ke konsol sehingga mengalami crash.

### Conclusion

Dalam materi ini kita telah mempelajari apa itu `for` loop, `while` loop, `do..while` loop dan juga infinite loop di JavaScript.

Automatisasi tugas-tugas yang bersifat berulang merupakan bagian yang sangat penting dalam pemrograman, dan penggunaan perulangan (loops) ini dapat membantu membuat program-program kita menjadi lebih efisien dan ringkas

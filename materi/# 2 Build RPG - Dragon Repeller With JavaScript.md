# Build RPG - Dragon Repeller With JavaScript (Part 2)

### Introduction

Di-part 1 kita sudah setup project dan membuat functionalitas program Dragon Repeller kita, pada part kali kita akan menambahkan beberapa fungsionalitas pada project Drago Repller.


## Step 1 - Update Function `goStore()`

Pada function `goStore` update property `onclick` kita untuk menjalakan button `buyHealth`, `buyWeapon` , `goTown`. Lalu ubah display text pada menu `goStore` menjadi `You enter the store.` 

```

	function goStore() {
	  button1.innerText = "Buy 10 health (10 gold)";
	  button2.innerText = "Buy weapon (30 gold)";
	  button3.innerText = "Go to town square";
	  
	  // tambah kode ini
	  button1.onclick = buyHealth;
	  button2.onclick = buyWeapon;
	  button3.onclick = goTown;
	  text.innerText = "You enter the store.";
	}


```


## Step 2  - Buat 3 Function baru

Buat 3 function kosong baru dengan nama function `buyHealth` , `buyWeapon` , `goTown`. 


```

	function goTown(){

	}
	
	function buyHealth(){
	
	}
	
	function buyWeapon(){
	
	}


```

Pindahkan function `goTown` diatas function `goStore` lalu copy dan paste seluruh kode di dalam function `goStore` ke dalam function `goTown`


```

	function goTown(){
		button1.innerText = "Buy 10 health (10 gold)";
		button2.innerText = "Buy weapon (30 gold)";
		button3.innerText = "Go to town square";
		button1.onclick = buyHealth;
		button2.onclick = buyWeapon;
		button3.onclick = goTown;
		text.innerText = "You enter the store.";
	}
	
	function goStore(){
		button1.innerText = "Buy 10 health (10 gold)";
		button2.innerText = "Buy weapon (30 gold)";
		button3.innerText = "Go to town square";
		button1.onclick = buyHealth;
		button2.onclick = buyWeapon;
		button3.onclick = goTown;
		text.innerText = "You enter the store.";
	}


```

Didalam function `goTown` ubah innerText tiap button menjadi `Go to Store`, `Go to cave` , `Fight dragon`. Lalu update properti onclick menjadi `goStore` , `goCave`, dan `fighDragon`.

Yang terakhir, update properti innerText dari `text` menjadi `You are in the town square. You see a sign that says Store.`

```
	function goTown() {
	  button1.innerText = "Go to store";
	  button2.innerText = "Go to cave";
	  button3.innerText = "Fight dragon";
	  button1.onclick = goStore;
	  button2.onclick = goCave;
	  button3.onclick = fightDragon;
	  text.innerText = 'You are in the town square. You see a sign that says Store.';
	}


```


## Step 3 - Buat Function Parameter

Buat 1 function kosong dengan nama update lalu memiliki parameter `location`.


```

	function update(location){
	
	}


```



## Conclusion

Pada part ini, kita telah membuat berbagai fungsi yang memiliki kegunaan yang berbeda. Dengan demikian, kode program kita dapat lebih mudah dipelihara (maintain) dan dikembangkan. Pada part berikutnya, kita akan membahas lebih detail mengenai penggunaan parameter dalam fungsi dan menjelajahi cara menggunakan array dan objek di JavaScript.
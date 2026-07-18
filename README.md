<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Rockstar Storage</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
background:#111;
color:white;
}

header{
background:#1b1b1b;
padding:18px;
text-align:center;
font-size:30px;
font-weight:bold;
box-shadow:0 0 15px black;
}

.grid{
width:95%;
margin:auto;
padding:20px;
display:grid;
grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:20px;
}

.card{

background:#1e1e1e;
border-radius:18px;
overflow:hidden;
box-shadow:0 0 12px rgba(0,0,0,.6);

}

.card img{

width:100%;
height:240px;
object-fit:cover;

}

.info{

padding:15px;

}

.info h2{

font-size:24px;
margin-bottom:10px;

}

.price{

font-size:26px;
color:#00ff66;
font-weight:bold;
margin-bottom:10px;

}

.stock{

margin-bottom:15px;
color:#7cff7c;

}

button{

width:100%;
padding:15px;
background:#005eff;
border:none;
border-radius:10px;
font-size:20px;
color:white;
cursor:pointer;

}

button:hover{

background:#0045c7;

}

.cart{

position:fixed;
bottom:20px;
right:20px;
background:#222;
padding:18px;
border-radius:15px;
width:260px;
box-shadow:0 0 20px blue;

}

.checkout{

margin-top:10px;
background:#16a34a;

}

</style>

</head>

<body>

<header>

ROCKSTAR STORAGE

</header>

<div class="grid">

<div class="card">

<img src="dragon.jpg">

<div class="info">

<h2>Dragon Breath Seed</h2>

<div class="price">

Rp3.000

</div>

<div class="stock">

Stok : 7

</div>

<button onclick="add('Dragon Breath Seed',3000)">

Tambah

</button>

</div>

</div>

<div class="card">

<img src="moon.jpg">

<div class="info">

<h2>Moon Bloom Seed</h2>

<div class="price">

Rp2.000

</div>

<div class="stock">

Stok : 5

</div>

<button onclick="add('Moon Bloom Seed',2000)">

Tambah

</button>

</div>

</div><div class="card">

<img src="hypno.jpg">

<div class="info">

<h2>Hypno Bloom Seed</h2>

<div class="price">
Rp2.000
</div>

<div class="stock">
Stok : 5
</div>

<button onclick="add('Hypno Bloom Seed',2000)">
Tambah
</button>

</div>

</div>

<div class="card">

<img src="venom.jpg">

<div class="info">

<h2>Venom Seed</h2>

<div class="price">
Rp1.000
</div>

<div class="stock">
Stok : 10
</div>

<button onclick="add('Venom Seed',1000)">
Tambah
</button>

</div>

</div>

<div class="card">

<img src="ghost.jpg">

<div class="info">

<h2>Ghost Pepper Seed</h2>

<div class="price">
Rp2.000
</div>

<div class="stock">
Stok : 8
</div>

<button onclick="add('Ghost Pepper Seed',2000)">
Tambah
</button>

</div>

</div>

<div class="card">

<img src="watering.jpg">

<div class="info">

<h2>Super Watering</h2>

<div class="price">
Rp1.000
</div>

<div class="stock">
Dapat 3-5 sesuai stok
</div>

<button onclick="add('Super Watering',1000)">
Tambah
</button>

</div>

</div><div class="card">

<img src="sprinkle.jpg">

<div class="info">

<h2>Super Sprinkle</h2>

<div class="price">
Rp2.000
</div>

<div class="stock">
Dapat 2-5 sesuai stok
</div>

<button onclick="add('Super Sprinkle',2000)">
Tambah
</button>

</div>

</div>

<div class="card">

<img src="1b.jpg">

<div class="info">

<h2>1B Sheckles via Buah</h2>

<div class="price">
Rp5.000
</div>

<div class="stock">
Ready
</div>

<button onclick="add('1B Sheckles',5000)">
Tambah
</button>

</div>

</div>

</div>

<div class="cart">

<h3>🛒 Keranjang</h3>

<p id="jumlah">0 Item</p>

<p id="total">Rp0</p>

<button class="checkout" onclick="checkout()">
Checkout WhatsApp
</button>

</div>

<script>

let cart = [];
let total = 0;

function add(nama,harga){

cart.push({nama,harga});

total += harga;

document.getElementById("jumlah").innerHTML =
cart.length + " Item";

document.getElementById("total").innerHTML =
"Rp" + total.toLocaleString("id-ID");

}

function checkout(){

if(cart.length==0){

alert("Keranjang masih kosong");

return;

}

let pesan="Halo Admin, saya ingin membeli:%0A%0A";

cart.forEach(function(item,i){

pesan += (i+1)+". "+item.nama+" - Rp"+item.harga.toLocaleString("id-ID")+"%0A";

});

pesan += "%0ATotal: Rp"+total.toLocaleString("id-ID");

window.open(
"https://wa.me/6283849070499?text="+pesan,
"_blank"
);

}

</script>

</body>
</html>

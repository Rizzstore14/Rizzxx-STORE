<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rockstar Storage</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,Helvetica,sans-serif;
}

body{
background:#111;
color:#fff;
}

header{
padding:20px;
text-align:center;
font-size:28px;
font-weight:bold;
background:#181818;
box-shadow:0 0 20px #000;
}

.container{
width:95%;
max-width:1200px;
margin:auto;
display:grid;
grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:25px;
padding:20px;
}

.card{
background:#222;
border-radius:20px;
overflow:hidden;
box-shadow:0 0 15px rgba(0,0,0,.5);
transition:.3s;
}

.card:hover{
transform:translateY(-8px);
}

.card img{
width:100%;
height:240px;
object-fit:cover;
}

.content{
padding:20px;
text-align:center;
}

.content h2{
font-size:25px;
margin-bottom:15px;
}

.price{
font-size:28px;
color:#00ff5e;
font-weight:bold;
margin-bottom:10px;
}

.stock{
color:#00ff88;
font-size:22px;
margin-bottom:15px;
}

button{
width:100%;
padding:15px;
border:none;
border-radius:12px;
background:linear-gradient(90deg,#000,#0022ff);
color:white;
font-size:20px;
cursor:pointer;
}

button:hover{
opacity:.9;
}

.cart{
position:fixed;
bottom:20px;
right:20px;
background:#111;
border:2px solid blue;
padding:15px;
border-radius:15px;
box-shadow:0 0 20px blue;
}

.cart h3{
margin-bottom:10px;
}

.checkout{
margin-top:10px;
background:green;
}
</style>
</head>

<body>

<header>
ROCKSTAR STORAGE
</header>

<div class="container">

<div class="card">
<img src="images/dragon.jpg">
<div class="content">
<h2>Dragon Breath Seed</h2>
<div class="price">Rp3.000</div>
<div class="stock">Stok : 7</div>
<button onclick="add('Dragon Breath Seed',3000)">Tambah</button>
</div>
</div>

<div class="card">
<img src="images/moon.jpg">
<div class="content">
<h2>Moon Bloom Seed</h2>
<div class="price">Rp2.000</div>
<div class="stock">Stok : 4</div>
<button onclick="add('Moon Bloom Seed',2000)">Tambah</button>
</div>
</div>

<div class="card">
<img src="images/hypno.jpg">
<div class="content">
<h2>Hypno Bloom Seed</h2>
<div class="price">Rp2.000</div>
<div class="stock">Stok : 10</div>
<button onclick="add('Hypno Bloom Seed',2000)">Tambah</button>
</div>
</div>

<div class="card">
<img src="images/venom.jpg">
<div class="content">
<h2>Venom Seed</h2>
<div class="price">Rp1.000</div>
<div class="stock">Stok : 10</div>
<button onclick="add('Venom Seed',1000)">Tambah</button>
</div>
</div>

<div class="card">
<img src="images/ghost.jpg">
<div class="content">
<h2>Ghost Pepper Seed</h2>
<div class="price">Rp2.000</div>
<div class="stock">Stok : 10</div>
<button onclick="add('Ghost Pepper Seed',2000)">Tambah</button>
</div>
</div>

<div class="card">
<img src="images/watering.jpg">
<div class="content">
<h2>Super Watering</h2>
<div class="price">Rp1.000</div>
<div class="stock">3-5 sesuai stok</div>
<button onclick="add('Super Watering',1000)">Tambah</button>
</div>
</div>

<div class="card">
<img src="images/sprinkle.jpg">
<div class="content">
<h2>Super Sprinkle</h2>
<div class="price">Rp2.000</div>
<div class="stock">2-5 sesuai stok</div>
<button onclick="add('Super Sprinkle',2000)">Tambah</button>
</div>
</div>

<div class="card">
<img src="images/sheckles.jpg">
<div class="content">
<h2>1B Sheckles via Buah</h2>
<div class="price">Rp5.000</div>
<div class="stock">Stok : 3</div>
<button onclick="add('1B Sheckles',5000)">Tambah</button>
</div>
</div>

</div>

<div class="cart">

<h3>🛒 Keranjang</h3>

<p id="jumlah">0 Item</p>

<p id="total">Rp0</p>

<button class="checkout" onclick="checkout()">
Checkout
</button>

</div>

<script>

let total=0;
let item=0;

function add(nama,harga){

item++;

total+=harga;

document.getElementById("jumlah").innerHTML=item+" Item";

document.getElementById("total").innerHTML=
"Rp"+total.toLocaleString("id-ID");

}

function checkout(){

let wa="https://wa.me/628966429957?text=Halo Admin saya ingin membeli total Rp"+total;

window.open(wa);

}

</script>

</body>
</html>

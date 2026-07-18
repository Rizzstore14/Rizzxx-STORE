<!DOCTYPE html>
<html lang="id">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>RIZZXX STORE</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,Helvetica,sans-serif;
}

body{
background:#0f0f0f;
color:#fff;
padding-bottom:120px;
}

header{
background:#181818;
padding:20px;
text-align:center;
border-bottom:3px solid #007bff;
position:sticky;
top:0;
z-index:1000;
}

header h1{
font-size:34px;
color:#4da3ff;
}

header p{
margin-top:5px;
color:#ccc;
font-size:15px;
}

.search{
width:95%;
margin:20px auto;
}

.search input{
width:100%;
padding:15px;
border:none;
border-radius:12px;
background:#1d1d1d;
color:white;
font-size:16px;
outline:none;
}

.container{
width:95%;
margin:auto;
display:grid;
grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:20px;
}

.card{
background:#1b1b1b;
border-radius:15px;
overflow:hidden;
box-shadow:0 0 12px rgba(0,0,0,.5);
transition:.3s;
}

.card:hover{
transform:translateY(-6px);
box-shadow:0 0 20px #007bff;
}

.card img{
width:100%;
height:220px;
object-fit:cover;
}

.info{
padding:15px;
}

.info h2{
font-size:22px;
margin-bottom:10px;
}

.price{
font-size:24px;
font-weight:bold;
color:#00ff66;
margin-bottom:10px;
}

.stock{
color:#77ff77;
margin-bottom:15px;
}

button{
width:100%;
padding:14px;
border:none;
border-radius:10px;
background:#007bff;
color:white;
font-size:18px;
cursor:pointer;
transition:.3s;
}

button:hover{
background:#005fd1;
}

.cart{
position:fixed;
right:20px;
bottom:20px;
width:260px;
background:#1a1a1a;
padding:18px;
border-radius:15px;
box-shadow:0 0 20px #007bff;
}

.checkout{
background:#16a34a;
margin-top:10px;
}

footer{
margin-top:40px;
padding:20px;
background:#181818;
text-align:center;
color:#aaa;
}

</style>

</head>

<body>

<header>

<h1>RIZZXX STORE</h1>

<p>Grow A Garden Shop</p>

</header>

<div class="search">

<input
type="text"
id="search"
placeholder="🔍 Cari Produk..."
onkeyup="cariProduk()">

</div>

<div class="container">
<!-- Dragon Breath Seed -->
<div class="card">
    <img src="images/dragon.jpg" alt="Dragon Breath Seed">
    <div class="info">
        <h2>🐉 Dragon Breath Seed</h2>
        <div class="price">Rp3.000 / Seed</div>
        <div class="stock">✅ Ready Stock</div>
        <button onclick="add('Dragon Breath Seed',3000)">
            Tambah ke Keranjang
        </button>
    </div>
</div>

<!-- Moon Bloom Seed -->
<div class="card">
    <img src="images/moon.jpg" alt="Moon Bloom Seed">
    <div class="info">
        <h2>🌙 Moon Bloom Seed</h2>
        <div class="price">Rp2.000 / Seed</div>
        <div class="stock">✅ Ready Stock</div>
        <button onclick="add('Moon Bloom Seed',2000)">
            Tambah ke Keranjang
        </button>
    </div>
</div>

<!-- Hypno Bloom Seed -->
<div class="card">
    <img src="images/hypno.jpg" alt="Hypno Bloom Seed">
    <div class="info">
        <h2>🌀 Hypno Bloom Seed</h2>
        <div class="price">Rp2.000 / Seed</div>
        <div class="stock">✅ Ready Stock</div>
        <button onclick="add('Hypno Bloom Seed',2000)">
            Tambah ke Keranjang
        </button>
    </div>
</div>

<!-- Venom Seed -->
<div class="card">
    <img src="images/venom.jpg" alt="Venom Seed">
    <div class="info">
        <h2>☠️ Venom Seed</h2>
        <div class="price">Rp1.000 / Seed</div>
        <div class="stock">✅ Ready Stock</div>
        <button onclick="add('Venom Seed',1000)">
            Tambah ke Keranjang
        </button>
    </div>
</div>
<!-- Ghost Pepper Seed -->
<div class="card">
    <img src="images/ghost.jpg" alt="Ghost Pepper Seed">
    <div class="info">
        <h2>👻 Ghost Pepper Seed</h2>
        <div class="price">Rp2.000 / Seed</div>
        <div class="stock">✅ Ready Stock</div>
        <button onclick="add('Ghost Pepper Seed',2000)">
            Tambah ke Keranjang
        </button>
    </div>
</div>

<!-- Super Watering -->
<div class="card">
    <img src="images/watering.jpg" alt="Super Watering">
    <div class="info">
        <h2>💧 Super Watering</h2>
        <div class="price">Rp1.000</div>
        <div class="stock">🎁 Dapat 3–5 (sesuai stok)</div>
        <button onclick="add('Super Watering',1000)">
            Tambah ke Keranjang
        </button>
    </div>
</div>

<!-- Super Sprinkle -->
<div class="card">
    <img src="images/sprinkle.jpg" alt="Super Sprinkle">
    <div class="info">
        <h2>✨ Super Sprinkle</h2>
        <div class="price">Rp2.000</div>
        <div class="stock">🎁 Dapat 2–5 (sesuai stok)</div>
        <button onclick="add('Super Sprinkle',2000)">
            Tambah ke Keranjang
        </button>
    </div>
</div>

<!-- 10M Sheckles -->
<div class="card">
    <img src="images/10m.jpg" alt="10M Sheckles">
    <div class="info">
        <h2>💰 10M Sheckles</h2>
        <div class="price">Rp1.000</div>
        <div class="stock">✅ Ready Stock</div>
        <button onclick="add('10M Sheckles',1000)">
            Tambah ke Keranjang
        </button>
    </div>
</div>

<!-- 50M Sheckles -->
<div class="card">
    <img src="images/50m.jpg" alt="50M Sheckles">
    <div class="info">
        <h2>💰 50M Sheckles</h2>
        <div class="price">Rp2.000</div>
        <div class="stock">✅ Ready Stock</div>
        <button onclick="add('50M Sheckles',2000)">
            Tambah ke Keranjang
        </button>
    </div>
</div>
<!-- 100M Sheckles -->
<div class="card">
    <img src="images/100m.jpg" alt="100M Sheckles">
    <div class="info">
        <h2>💰 100M Sheckles</h2>
        <div class="price">Rp3.000</div>
        <div class="stock">✅ Ready Stock</div>
        <button onclick="add('100M Sheckles',3000)">
            Tambah ke Keranjang
        </button>
    </div>
</div>

<!-- 500M Sheckles -->
<div class="card">
    <img src="images/500m.jpg" alt="500M Sheckles">
    <div class="info">
        <h2>💰 500M Sheckles</h2>
        <div class="price">Rp5.000</div>
        <div class="stock">✅ Ready Stock</div>
        <button onclick="add('500M Sheckles',5000)">
            Tambah ke Keranjang
        </button>
    </div>
</div>

<!-- 1B Sheckles -->
<div class="card">
    <img src="images/1b.jpg" alt="1B Sheckles">
    <div class="info">
        <h2>💎 1B Sheckles</h2>
        <div class="price">Rp10.000</div>
        <div class="stock">✅ Ready Stock</div>
        <button onclick="add('1B Sheckles',10000)">
            Tambah ke Keranjang
        </button>
    </div>
</div>

</div>

<!-- Keranjang -->
<div class="cart">

<h3>🛒 Keranjang</h3>

<p id="jumlah">0 Item</p>

<p id="total">Rp0</p>

<button class="checkout" onclick="checkout()">
Checkout WhatsApp
</button>

</div>

<script>

let cart=[];
let total=0;

function add(nama,harga){

cart.push({nama,harga});

total+=harga;

document.getElementById("jumlah").innerHTML=cart.length+" Item";

document.getElementById("total").innerHTML="Rp "+total.toLocaleString("id-ID");

alert("✅ "+nama+" berhasil ditambahkan!");

}

function checkout(){

if(cart.length===0){
alert("Keranjang masih kosong!");
return;
}

let pesan="Halo Admin RIZZXX STORE 👋%0A%0ASaya ingin membeli:%0A%0A";

cart.forEach(function(item,index){

pesan+=(index+1)+". "+item.nama+" - Rp"+item.harga.toLocaleString("id-ID")+"%0A";

});

pesan+="%0ATotal: Rp"+total.toLocaleString("id-ID");
pesan+="%0A%0ANama Roblox: ";
pesan+="%0AUsername: ";

window.open(
"https://wa.me/6283849070499?text="+pesan,
"_blank"
);

}

function cariProduk(){

let input=document.getElementById("search").value.toLowerCase();

let card=document.querySelectorAll(".card");

card.forEach(function(item){

if(item.innerText.toLowerCase().includes(input)){
item.style.display="";
}else{
item.style.display="none";
}

});

}

</script>

<footer>

© 2026 RIZZXX STORE<br>
Grow A Garden Shop

</footer>

</body>
</html>

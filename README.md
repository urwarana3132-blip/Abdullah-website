<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Abdullah Egg Store</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: #111;
    color: white;
}

header {
    background: #000;
    padding: 25px 10px;
    text-align: center;
    border-bottom: 3px solid gold;
}

header h1 {
    color: gold;
    font-size: 30px;
}

nav {
    background: #222;
    padding: 15px;
    text-align: center;
}

nav a {
    color: gold;
    text-decoration: none;
    margin: 10px;
    font-weight: bold;
}

.hero {
    text-align: center;
    padding: 55px 15px;
    background: linear-gradient(135deg, #222, #000);
}

.hero h2 {
    color: gold;
    font-size: 30px;
}

.hero button {
    background: gold;
    color: black;
    padding: 13px 25px;
    border: none;
    border-radius: 8px;
    font-weight: bold;
}

h2.section-title {
    text-align: center;
    color: gold;
    margin-top: 35px;
}

.products {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    padding: 20px;
}

.card {
    background: #222;
    width: 270px;
    padding: 22px;
    text-align: center;
    border: 1px solid gold;
    border-radius: 15px;
}

.egg {
    font-size: 75px;
}

.card h3 {
    color: gold;
}

.price {
    color: #00ff80;
    font-weight: bold;
}

button {
    cursor: pointer;
}

.card button {
    background: gold;
    color: black;
    padding: 12px 20px;
    border: none;
    border-radius: 8px;
    font-weight: bold;
}

.cart {
    background: #222;
    margin: 25px 15px;
    padding: 25px;
    border: 1px solid gold;
    border-radius: 15px;
    text-align: center;
}

.cart h2 {
    color: gold;
}

.whatsapp {
    display: inline-block;
    background: #25D366;
    color: white;
    padding: 15px 25px;
    text-decoration: none;
    border-radius: 10px;
    font-weight: bold;
    margin-top: 15px;
}

footer {
    background: black;
    border-top: 2px solid gold;
    text-align: center;
    padding: 25px;
    color: gold;
}
</style>
</head>

<body>

<header>
<h1>🥚 ABDULLAH EGG STORE</h1>
<p>Fresh Eggs | Best Quality | Best Service</p>
</header>

<nav>
<a href="#home">Home</a>
<a href="#products">Products</a>
<a href="#cart">My Cart</a>
</nav>

<section class="hero" id="home">
<h2>Welcome To Abdullah Egg Store</h2>
<p>Fresh And Quality Eggs Available Here!</p>

<button onclick="location.href='#products'">
Shop Now
</button>
</section>

<h2 class="section-title" id="products">
OUR PRODUCTS
</h2>

<div class="products">

<div class="card">
<div class="egg">🥚</div>
<h3>Farm Fresh Eggs</h3>
<p>Fresh Quality Eggs</p>
<p class="price">Price on Request</p>
<button onclick="addCart('Farm Fresh Eggs')">
Add To Cart
</button>
</div>

<div class="card">
<div class="egg">🐣</div>
<h3>Desi Eggs</h3>
<p>Natural Desi Eggs</p>
<p class="price">Price on Request</p>
<button onclick="addCart('Desi Eggs')">
Add To Cart
</button>
</div>

<div class="card">
<div class="egg">🥚</div>
<h3>White Eggs</h3>
<p>Premium Quality Eggs</p>
<p class="price">Price on Request</p>
<button onclick="addCart('White Eggs')">
Add To Cart
</button>
</div>

</div>

<div class="cart" id="cart">

<h2>🛒 MY SHOPPING CART</h2>

<p id="items">Your Cart Is Empty</p>

<button onclick="clearCart()">
Clear Cart
</button>

<br>

<a class="whatsapp"
id="whatsapp"
href="https://wa.me/923214684901"
target="_blank">
Order On WhatsApp
</a>

</div>

<footer>
<h3>ABDULLAH EGG STORE</h3>
<p>Thank You For Visiting Our Store!</p>
<p>WhatsApp: 923214684901</p>
</footer>

<script>

let cart = [];

function addCart(product) {

cart.push(product);

document.getElementById("items").innerHTML =
cart.map(item => "🥚 " + item).join("<br>");

let message =
"Hello Abdullah Egg Store! I want to order:\n" +
cart.join("\n");

document.getElementById("whatsapp").href =
"https://wa.me/923214684901?text=" +
encodeURIComponent(message);

}

function clearCart() {

cart = [];

document.getElementById("items").innerHTML =
"Your Cart Is Empty";

document.getElementById("whatsapp").href =
"https://wa.me/923214684901";

}

</script>

</body>
</html>

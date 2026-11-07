<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Abdullah Egg Store</title>

<style>
body {
    margin: 0;
    font-family: Arial;
    background: #f5f5f5;
    text-align: center;
}

header {
    background: #142d20;
    color: white;
    padding: 25px;
}

nav {
    background: #e6ad20;
    padding: 15px;
}

nav a {
    color: black;
    margin: 12px;
    text-decoration: none;
    font-weight: bold;
}

.hero {
    padding: 40px;
    background: #fff1c9;
}

.products {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
    padding: 20px;
}

.card {
    background: white;
    width: 250px;
    padding: 20px;
    border-radius: 15px;
}

.egg {
    font-size: 70px;
}

button {
    background: #142d20;
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 8px;
}

.cart {
    background: white;
    margin: 20px;
    padding: 20px;
}

footer {
    background: #142d20;
    color: white;
    padding: 20px;
}
</style>
</head>

<body>

<header>
<h1>🥚 Abdullah Egg Store</h1>
<p>Fresh Eggs, Best Quality!</p>
</header>

<nav>
<a href="#home">Home</a>
<a href="#products">Products</a>
<a href="#cart">My Cart</a>
</nav>

<section class="hero" id="home">
<h2>Welcome To Abdullah Egg Store</h2>
<p>Fresh Eggs Available Here!</p>
</section>

<h2 id="products">Our Products 🥚</h2>

<div class="products">

<div class="card">
<div class="egg">🥚</div>
<h3>Farm Fresh Eggs</h3>
<p>Price on Request</p>
<button onclick="addCart('Farm Fresh Eggs')">Add To Cart</button>
</div>

<div class="card">
<div class="egg">🐣</div>
<h3>Desi Eggs</h3>
<p>Price on Request</p>
<button onclick="addCart('Desi Eggs')">Add To Cart</button>
</div>

<div class="card">
<div class="egg">🥚</div>
<h3>White Eggs</h3>
<p>Price on Request</p>
<button onclick="addCart('White Eggs')">Add To Cart</button>
</div>

</div>

<div class="cart" id="cart">
<h2>🛒 My Shopping Cart</h2>
<p id="items">Your cart is empty.</p>
<button onclick="orderNow()">Order On WhatsApp</button>
</div>

<footer>
<h3>Abdullah Egg Store</h3>
<p>Thank You For Visiting!</p>
<p>WhatsApp: 923214684901</p>
</footer>

<script>

let cart = [];

function addCart(product) {
cart.push(product);

document.getElementById("items").innerHTML =
cart.map(item => "🥚 " + item).join("<br>");

alert("Product Added To Cart!");
}

function orderNow() {
if (cart.length === 0) {
alert("Please Add Products First!");
return;
}

let message = "Hello Abdullah Egg Store! I want to order:\n" + cart.join("\n");

let phone = "923214684901";

window.open("https://wa.me/" + phone + "?text=" + encodeURIComponent(message), "_blank");
}

</script>

</body>
</html>

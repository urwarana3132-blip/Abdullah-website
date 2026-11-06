<!DOCTYPE html>
<html>
<head>
    <title>Abdullah Egg Store</title>

    <style>
        body {
            background-color: lightyellow;
            font-family: Arial;
            text-align: center;
            margin: 0;
        }

        header {
            background-color: darkgreen;
            color: white;
            padding: 25px;
        }

        .product {
            background-color: white;
            margin: 20px;
            padding: 20px;
            border-radius: 12px;
        }

        button {
            background-color: green;
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 8px;
            font-size: 17px;
        }

        footer {
            background-color: darkgreen;
            color: white;
            padding: 20px;
        }
    </style>
</head>

<body>

<header>
    <h1>🥚 Abdullah Egg Store 🥚</h1>
    <h2>Fresh Eggs Available</h2>
    <p>Fresh Eggs at Best Prices!</p>
</header>

<div class="product">
    <h2>Our Products</h2>

    <h3>Farm Fresh Eggs 🥚</h3>
    <p> 12 eggs desi Price: Rs. 600</p>

    <button onclick="orderNow()">Order Now</button>
</div>

<div>
    <h2>Delivery Areas</h2>
    <p>lahore</p>
    <p>sheikhupura</p>
</div>

<div>
    <h2>Customer Reviews</h2>
    <p>Fresh Eggs and Best Quality!</p>
</div>

<div>
    <h2>Contact Us</h2>
    <p>Phone: 03214684901</p>
</div>

<footer>
    <p>© 2026 Abdullah Egg Store</p>
</footer>

<script>
function orderNow() {
    alert("Welcome to Abdullah Egg Store! Contact us to order.");
}
</script>

</body>
</html>

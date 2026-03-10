# lumiere-store
lumiere-store
│
├── index.html
├── shop.html
├── cart.html
├── admin.html
│
├── css
│   └── style.css
│
├── js
│   ├── store.js
│   └── admin.js
│
└── images
<!DOCTYPE html>
<html>
<head>
<title>LUMIÈRE Admin</title>
</head>

<body>

<h2>Add Clothing Product</h2>

<input id="name" placeholder="Product Name">
<input id="price" placeholder="Price">
<input id="image" placeholder="Image URL">

<button onclick="addProduct()">Add Product</button>

<script>

function addProduct(){

let name=document.getElementById("name").value
let price=document.getElementById("price").value
let image=document.getElementById("image").value

let products=JSON.parse(localStorage.getItem("products")) || []

products.push({name,price,image})

localStorage.setItem("products",JSON.stringify(products))

alert("Product added")

}

</script>
<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>LUMIÈRE Clothing</title>

<style>

body{
font-family:Arial;
margin:0;
background:white;
color:black;
}

header{
display:flex;
justify-content:space-between;
padding:20px;
border-bottom:2px solid black;
}

nav a{
margin:10px;
text-decoration:none;
color:black;
font-weight:bold;
}

.hero{
text-align:center;
padding:80px;
background:#f5f5f5;
}

.products{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
gap:20px;
padding:30px;
}

.card{
border:1px solid #ddd;
padding:15px;
border-radius:8px;
text-align:center;
}

.card img{
width:100%;
}

button{
background:black;
color:white;
border:none;
padding:10px;
cursor:pointer;
}

</style>
</head>

<body>

<header>

<h2>LUMIÈRE</h2>

<nav>
<a href="#">Home</a>
<a href="#">Shop</a>
<a href="#">Cart</a>
<a href="#">Contact</a>
</nav>

</header>

<section class="hero">

<h1>Modern Clothing Collection</h1>
<p>Minimal • Elegant • Timeless</p>

</section>

<section class="products">

<div class="card">
<img src="https://via.placeholder.com/250">
<h3>White Shirt</h3>
<p>$35</p>
<button>Add to Cart</button>
</div>

<div class="card">
<img src="https://via.placeholder.com/250">
<h3>Black Jacket</h3>
<p>$80</p>
<button>Add to Cart</button>
</div>

<div class="card">
<img src="https://via.placeholder.com/250">
<h3>Casual Hoodie</h3>
<p>$50</p>
<button>Add to Cart</button>
</div>

</section>

</body>
</html>
</body>
</html>

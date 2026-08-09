<!DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Sadikur Fashion House</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,sans-serif;
}

body{
    background:#f5f5f5;
    color:#222;
}

/* HEADER */
header{
    background:#111827;
    color:white;
    padding:15px 5%;
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:15px;
    position:sticky;
    top:0;
    z-index:1000;
}

.logo{
    font-size:25px;
    font-weight:bold;
}

.logo span{
    color:#f59e0b;
}

.owner{
    font-size:14px;
}

nav a{
    color:white;
    text-decoration:none;
    margin:0 7px;
}

.cart{
    background:#f59e0b;
    color:#111;
    padding:9px 14px;
    border-radius:7px;
    font-weight:bold;
}

/* HERO */
.hero{
    min-height:430px;
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    padding:40px 20px;
    background:linear-gradient(135deg,#111827,#4b5563);
    color:white;
}

.hero h1{
    font-size:48px;
    margin-bottom:15px;
}

.hero p{
    font-size:18px;
    margin-bottom:25px;
}

.shop-btn{
    display:inline-block;
    padding:13px 28px;
    background:#f59e0b;
    color:#111;
    text-decoration:none;
    border-radius:7px;
    font-weight:bold;
}

/* SEARCH */
.search-box{
    background:white;
    padding:25px 5%;
    text-align:center;
}

.search-box input{
    width:90%;
    max-width:600px;
    padding:14px;
    border:1px solid #ddd;
    border-radius:8px;
    font-size:16px;
}

/* SECTIONS */
section{
    padding:50px 5%;
}

.title{
    text-align:center;
    margin-bottom:30px;
}

.title h2{
    font-size:32px;
    margin-bottom:8px;
}

/* CATEGORY */
.categories{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(120px,1fr));
    gap:15px;
}

.category{
    background:white;
    padding:22px 10px;
    text-align:center;
    border-radius:12px;
    cursor:pointer;
    box-shadow:0 4px 15px rgba(0,0,0,.08);
    transition:.3s;
}

.category:hover{
    transform:translateY(-5px);
    background:#fff7e6;
}

.category .icon{
    font-size:38px;
    margin-bottom:8px;
}

/* PRODUCTS */
.products{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:25px;
}

.product{
    background:white;
    border-radius:12px;
    overflow:hidden;
    box-shadow:0 4px 15px rgba(0,0,0,.08);
    transition:.3s;
}

.product:hover{
    transform:translateY(-5px);
}

.product-img{
    height:220px;
    background:#e5e7eb;
    display:flex;
    justify-content:center;
    align-items:center;
    font-size:75px;
}

.product-info{
    padding:18px;
}

.product-info h3{
    margin-bottom:8px;
}

.info{
    color:#666;
    font-size:14px;
    margin:5px 0;
}

.price{
    font-size:22px;
    font-weight:bold;
    color:#e11d48;
    margin:12px 0;
}

.stock{
    color:green;
    font-size:14px;
}

.buy-btn{
    width:100%;
    border:0;
    padding:12px;
    background:#111827;
    color:white;
    border-radius:7px;
    cursor:pointer;
    font-weight:bold;
    margin-top:10px;
}

.buy-btn:hover{
    background:#f59e0b;
    color:#111;
}

/* OFFER */
.offer{
    background:#f59e0b;
    text-align:center;
    padding:45px 20px;
}

.offer h2{
    font-size:34px;
    margin-bottom:10px;
}

/* CONTACT */
.contact{
    background:white;
    text-align:center;
}

.contact p{
    margin:12px;
}

.contact a{
    color:#0d6efd;
    text-decoration:none;
    font-weight:bold;
}

.whatsapp{
    display:inline-block;
    margin-top:15px;
    background:#25D366 !important;
    color:white !important;
    padding:13px 25px;
    border-radius:7px;
}

/* FOOTER */
footer{
    background:#111827;
    color:white;
    text-align:center;
    padding:25px;
}

footer p{
    margin:7px;
}

/* MOBILE */
@media(max-width:750px){

    header{
        flex-direction:column;
    }

    nav{
        text-align:center;
    }

    nav a{
        display:inline-block;
        margin:5px;
    }

    .hero h1{
        font-size:35px;
    }

    .hero p{
        font-size:16px;
    }
}
</style>
</head>

<body>


<!-- HEADER -->
<header>

<div class="logo">
Sadikur<span>Fashion</span>
</div>

<div class="owner">
👤 Sadikur Rahman
</div>

<nav>
<a href="#home">Home</a>
<a href="#categories">Categories</a>
<a href="#products">Products</a>
<a href="#contact">Contact</a>
</nav>

<div class="cart">
🛒 Cart:
<span id="cartCount">0</span>
</div>

</header>


<!-- HERO -->
<section class="hero" id="home">

<div>

<h1>Welcome to Sadikur Fashion</h1>

<p>
Shirt, Pant, Panjabi, Payjama, Shoes,
Genji, T-Shirt, Sari এবং আরও অনেক কিছু
</p>

<a href="#products" class="shop-btn">
🛍️ Shop Now
</a>

</div>

</section>


<!-- SEARCH -->
<div class="search-box">

<input
type="text"
id="search"
placeholder="🔍 Search product..."
onkeyup="searchProduct()">

</div>


<!-- CATEGORIES -->
<section id="categories">

<div class="title">

<h2>All Categories</h2>

<p>আপনার পছন্দের ক্যাটাগরি নির্বাচন করুন</p>

</div>


<div class="categories">

<div class="category" onclick="filterCategory('Shirt')">
<div class="icon">👔</div>
<h3>Shirt</h3>
</div>

<div class="category" onclick="filterCategory('Pant')">
<div class="icon">👖</div>
<h3>Pant</h3>
</div>

<div class="category" onclick="filterCategory('Panjabi')">
<div class="icon">🥻</div>
<h3>Panjabi</h3>
</div>

<div class="category" onclick="filterCategory('Payjama')">
<div class="icon">👖</div>
<h3>Payjama</h3>
</div>

<div class="category" onclick="filterCategory('Shoes')">
<div class="icon">👟</div>
<h3>Shoes</h3>
</div>

<div class="category" onclick="filterCategory('Genji')">
<div class="icon">👕</div>
<h3>Genji</h3>
</div>

<div class="category" onclick="filterCategory('T-Shirt')">
<div class="icon">👕</div>
<h3>T-Shirt</h3>
</div>

<div class="category" onclick="filterCategory('Sari')">
<div class="icon">🥻</div>
<h3>Sari</h3>
</div>

</div>

</section>


<!-- PRODUCTS -->
<section id="products">

<div class="title">

<h2>Our Products</h2>

<p>সকল পণ্য একসাথে</p>

</div>


<div class="products">


<!-- SHIRT -->
<div class="product" data-category="Shirt">

<div class="product-img">👔</div>

<div class="product-info">

<h3>Premium Shirt</h3>

<p class="info">Category: Shirt</p>
<p class="info">Size: M, L, XL, XXL</p>

<div class="price">৳850</div>

<p class="stock">✔ Stock Available</p>

<button
class="buy-btn"
onclick="orderProduct('Premium Shirt','850')">

Order Now

</button>

</div>
</div>


<!-- PANT -->
<div class="product" data-category="Pant">

<div class="product-img">👖</div>

<div class="product-info">

<h3>Premium Denim Pant</h3>

<p class="info">Category: Pant</p>
<p class="info">Size: 30, 32, 34, 36</p>

<div class="price">৳1,200</div>

<p class="stock">✔ Stock Available</p>

<button
class="buy-btn"
onclick="orderProduct('Premium Denim Pant','1200')">

Order Now

</button>

</div>
</div>


<!-- PANJABI -->
<div class="product" data-category="Panjabi">

<div class="product-img">🥻</div>

<div class="product-info">

<h3>Premium Panjabi</h3>

<p class="info">Category: Panjabi</p>
<p class="info">Size: M, L, XL, XXL</p>

<div class="price">৳1,500</div>

<p class="stock">✔ Stock Available</p>

<button
class="buy-btn"
onclick="orderProduct('Premium Panjabi','1500')">

Order Now

</button>

</div>
</div>


<!-- PAYJAMA -->
<div class="product" data-category="Payjama">

<div class="product-img">👖</div>

<div class="product-info">

<h3>Comfort Payjama</h3>

<p class="info">Category: Payjama</p>
<p class="info">Size: M, L, XL, XXL</p>

<div class="price">৳650</div>

<p class="stock">✔ Stock Available</p>

<button
class="buy-btn"
onclick="orderProduct('Comfort Payjama','650')">

Order Now

</button>

</div>
</div>


<!-- SHOES -->
<div class="product" data-category="Shoes">

<div class="product-img">👟</div>

<div class="product-info">

<h3>Premium Casual Shoes</h3>

<p class="info">Category: Shoes</p>
<p class="info">Size: 39, 40, 41, 42, 43</p>

<div class="price">৳1,300</div>

<p class="stock">✔ Stock Available</p>

<button
class="buy-btn"
onclick="orderProduct('Premium Casual Shoes','1300')">

Order Now

</button>

</div>
</div>


<!-- GENJI -->
<div class="product" data-category="Genji">

<div class="product-img">👕</div>

<div class="product-info">

<h3>Premium Cotton Genji</h3>

<p class="info">Category: Genji</p>
<p class="info">Size: M, L, XL, XXL</p>

<div class="price">৳450</div>

<p class="stock">✔ Stock Available</p>

<button
class="buy-btn"
onclick="orderProduct('Premium Cotton Genji','450')">

Order Now

</button>

</div>
</div>


<!-- T-SHIRT -->
<div class="product" data-category="T-Shirt">

<div class="product-img">👕</div>

<div class="product-info">

<h3>Premium T-Shirt</h3>

<p class="info">Category: T-Shirt</p>
<p class="info">Size: M, L, XL, XXL</p>

<div class="price">৳700</div>

<p class="stock">✔ Stock Available</p>

<button
class="buy-btn"
onclick="orderProduct('Premium T-Shirt','700')">

Order Now

</button>

</div>
</div>


<!-- SARI -->
<div class="product" data-category="Sari">

<div class="product-img">🥻</div>

<div class="product-info">

<h3>Premium Sari</h3>

<p class="info">Category: Sari</p>
<p class="info">Color: Multiple</p>

<div class="price">৳1,800</div>

<p class="stock">✔ Stock Available</p>

<button
class="buy-btn"
onclick="orderProduct('Premium Sari','1800')">

Order Now

</button>

</div>
</div>


</div>

</section>


<!-- OFFER -->
<section class="offer">

<h2>🔥 Special Offer</h2>

<p>
নির্বাচিত পণ্যে আকর্ষণীয় ডিসকাউন্ট!
আজই অর্ডার করুন।
</p>

</section>


<!-- CONTACT -->
<section class="contact" id="contact">

<div class="title">

<h2>Contact Us</h2>

<p>
অর্ডার বা যেকোনো তথ্যের জন্য যোগাযোগ করুন
</p>

</div>

<p>
👤 Owner:
<strong>Sadikur Rahman</strong>
</p>

<p>
📞 Phone:
<a href="tel:01733308665">
01733308665
</a>
</p>

<p>
📱 WhatsApp:
<a
href="https://wa.me/8801733308665"
target="_blank">

01733308665

</a>
</p>

<a
class="whatsapp"
href="https://wa.me/8801733308665"
target="_blank">

💬 WhatsApp এ অর্ডার করুন

</a>

</section>


<!-- FOOTER -->
<footer>

<p>👤 Sadikur Rahman</p>

<p>📞 01733308665</p>

<p>
© 2026 Sadikur Fashion | All Rights Reserved.
</p>

</footer>


<script>

/* CART */
let cartCount = 0;


/* ORDER */
function orderProduct(product, price){

cartCount++;

document.getElementById("cartCount").innerText = cartCount;

let message =
"Assalamu Alaikum,%0A%0A"+
"I want to order:%0A"+
"Product: "+product+"%0A"+
"Price: ৳"+price+"%0A%0A"+
"Please contact me for delivery.";

let whatsapp =
"https://wa.me/8801733308665?text="+message;

window.open(whatsapp,"_blank");

}


/* SEARCH */
function searchProduct(){

let input =
document
.getElementById("search")
.value
.toLowerCase();

let products =
document.querySelectorAll(".product");

products.forEach(function(product){

let text =
product.innerText.toLowerCase();

if(text.includes(input)){

product.style.display="block";

}else{

product.style.display="none";

}

});

}


/* CATEGORY FILTER */
function filterCategory(category){

let products =
document.querySelectorAll(".product");

products.forEach(function(product){

if(product.dataset.category === category){

product.style.display="block";

}else{

product.style.display="none";

}

});

document
.getElementById("products")
.scrollIntoView({
behavior:"smooth"
});

}

</script>

</body>
</html>

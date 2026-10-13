
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#087443">
<title>Africart Zimbabwe | Shop Local</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial,sans-serif;background:#f5f7f5;color:#17231c}
header{background:#087443;color:white;padding:20px 5%}
.brand{font-size:29px;font-weight:800}
.brand span{color:#ffda55}
header p{font-size:14px}
.search{display:flex;gap:8px}
input{flex:1;min-width:0;padding:13px;border:0;border-radius:8px;font-size:15px}
button{border:0;border-radius:8px;padding:12px 15px;background:#ffda55;font-weight:bold;cursor:pointer}
nav{display:flex;gap:20px;overflow-x:auto;padding:15px 5%;background:white}
nav a{color:#087443;text-decoration:none;font-weight:bold;white-space:nowrap}
main{max-width:1100px;margin:auto;padding:20px 16px}
.hero{background:linear-gradient(120deg,#075c36,#11935a);color:white;padding:30px 22px;border-radius:15px;margin-bottom:25px}
.hero h1{font-size:clamp(28px,6vw,43px);margin:0 0 12px}
.hero p{line-height:1.6}
h2{font-size:22px}
.notice{background:#fff5d6;padding:12px;border-radius:8px;font-size:13px;line-height:1.5}
.products{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:13px}
.card{background:white;border-radius:12px;overflow:hidden;border:1px solid #e5eae6}
.photo{width:100%;height:135px;object-fit:cover;background:#e4eee7}
.details{padding:12px}
.details h3{font-size:15px;margin:0 0 8px}
.seller{font-size:12px;color:#647168;line-height:1.5}
.price{font-size:19px;font-weight:800;color:#087443;margin:10px 0}
.contact{display:block;text-align:center;padding:11px 5px;background:#087443;color:white;border-radius:7px;text-decoration:none;font-size:13px;font-weight:bold}
footer{background:#13251b;color:white;padding:25px 5%;margin-top:30px;line-height:1.8;font-size:14px}
#empty{display:none;padding:20px}
@media(min-width:650px){.products{grid-template-columns:repeat(4,minmax(0,1fr))}.photo{height:180px}}
</style>
</head>
<body>
<header>
  <div class="brand">Africart<span>.</span></div>
  <p>Zimbabwe's marketplace. Shop local.</p>
  <div class="search">
    <input id="search" type="search" placeholder="Search products..." aria-label="Search products">
    <button onclick="searchProducts()">Search</button>
  </div>
</header>

<nav>
  <a href="#products">All products</a>
  <a href="#products">Electronics</a>
  <a href="#products">Fashion</a>
  <a href="#products">Home</a>
  <a href="#sell">Sell on Africart</a>
</nav>

<main>
<section class="hero">
  <h1>Discover more.<br>Shop Zimbabwe.</h1>
  <p>Explore products and discover local businesses across Zimbabwe. Prices displayed in USD.</p>
  <button onclick="document.getElementById('products').scrollIntoView({behavior:'smooth'})">Explore products →</button>
</section>

<h2 id="products">Products to discover</h2>
<p class="notice">Demo catalogue: these are sample listings, not verified offers. Seller details, prices and stock must be confirmed before purchase.</p>

<div class="products">
<article class="card" data-search="wireless headphones electronics">
<img class="photo" src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?w=500" alt="Headphones">
<div class="details"><h3>Wireless Headphones</h3><div class="seller">Electronics · Sample seller</div><div class="price">$15.00</div><a class="contact" href="#sell">Seller not connected</a></div>
</article>

<article class="card" data-search="trainers shoes fashion">
<img class="photo" src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?w=500" alt="Trainers">
<div class="details"><h3>Everyday Trainers</h3><div class="seller">Fashion · Sample seller</div><div class="price">$25.00</div><a class="contact" href="#sell">Seller not connected</a></div>
</article>

<article class="card" data-search="backpack bag school">
<img class="photo" src="https://images.unsplash.com/photo-1553062407-98eeb64c6a62?w=500" alt="Backpack">
<div class="details"><h3>Everyday Backpack</h3><div class="seller">Bags · Sample seller</div><div class="price">$18.00</div><a class="contact" href="#sell">Seller not connected</a></div>
</article>

<article class="card" data-search="watch accessories">
<img class="photo" src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?w=500" alt="Watch">
<div class="details"><h3>Classic Watch</h3><div class="seller">Accessories · Sample seller</div><div class="price">$20.00</div><a class="contact" href="#sell">Seller not connected</a></div>
</article>
</div>

<p id="empty">No matching products found. Try another search.</p>

<section id="sell">
<h2>Sell on Africart</h2>
<p>We aim to help Zimbabwean businesses reach more customers.</p>
<p><strong>Seller registration coming soon.</strong> Accounts, orders and payments are not active yet.</p>
</section>
</main>

<footer>
<strong>Africart Zimbabwe</strong><br>
Connecting Zimbabwean buyers and local sellers.<br>
Prices shown in USD. Confirm seller details, stock and delivery before paying.<br>
<small>© 2026 Africart. Marketplace under development.</small>
</footer>

<script>
function searchProducts(){
 const query=document.getElementById('search').value.toLowerCase().trim();
 const cards=document.querySelectorAll('.card');
 let visible=0;
 cards.forEach(card=>{
  const match=(card.innerText+' '+card.dataset.search).toLowerCase().includes(query);
  card.style.display=match?'':'none';
  if(match)visible++;
 });
 document.getElementById('empty').style.display=visible?'none':'block';
}
document.getElementById('search').addEventListener('input',searchProducts);
</script>
</body>
</html>


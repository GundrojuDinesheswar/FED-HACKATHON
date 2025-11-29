<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tribal Artisan Marketplace</title>
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:Arial;background:#FAF0E6;color:#333;}
section{padding:80px 0;display:none;}
.active{display:block;}
h2{text-align:center;margin-bottom:25px;color:#5D4037;}
.btn{background:#8B4513;border:none;color:white;padding:10px 20px;border-radius:5px;cursor:pointer;}
.btn:hover{background:#D2691E;}
header{background:#fff;box-shadow:0 4px 6px rgba(0,0,0,0.2);position:fixed;width:100%;top:0;z-index:10;}
nav{display:flex;justify-content:space-between;align-items:center;padding:15px 30px;}
nav a{margin-left:20px;color:#8B4513;font-weight:bold;text-decoration:none;cursor:pointer;}
nav a:hover{color:#D2691E;}
.hero{background:#B88A6E;height:300px;color:white;text-align:center;padding-top:120px;}
.login-box{width:380px;margin:120px auto;background:#fff;padding:30px;border-radius:8px;box-shadow:0 4px 10px rgba(0,0,0,0.3);}
.login-box input{width:100%;padding:12px;margin:8px 0;border:1px solid #bbb;border-radius:6px;}
.container{width:90%;max-width:1100px;margin:auto;}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:24px;}
.card{background:white;border-radius:8px;box-shadow:0 4px 12px rgba(0,0,0,0.2);overflow:hidden;}
.card img{width:100%;height:210px;object-fit:cover;}
.card .info{padding:15px;}
.price{color:#8B4513;font-weight:bold;margin:6px 0;font-size:18px;}
.pay-box{width:420px;margin:120px auto;background:white;padding:25px;border-radius:8px;box-shadow:0 4px 12px rgba(0,0,0,0.3);}
.pay-box input{width:100%;padding:12px;margin:10px 0;border-radius:6px;border:1px solid #ccc;}
</style>
</head>
<body>

<header>
  <nav>
    <h2 style="color:#8B4513;">Tribal Artisan</h2>
    <div id="adminNav" style="display:none;">
      <a onclick="show('home')">Home</a>
      <a onclick="show('products')">Products</a>
      <a onclick="show('track')">Track Order</a>
      <a onclick="openAdminPanel()">Admin Panel</a>
    </div>
  </nav>
</header>

<!-- 1️⃣ ADMIN SIGNUP (FIRST PAGE) -->
<section id="adminSignup" class="active">
  <div class="login-box">
    <h2>Admin Signup</h2>
    <input id="adName" placeholder="Full Name">
    <input id="adAge" type="number" placeholder="Age">
    <input id="adPhone" placeholder="Phone">
    <input id="adEmail" placeholder="Email">
    <input id="adPass" type="password" placeholder="Password">
    <button class="btn" onclick="signupAdmin()">Sign Up</button>
  </div>
</section>

<!-- 2️⃣ ADMIN LOGIN -->
<section id="adminLogin">
  <div class="login-box">
    <h2>Admin Login</h2>
    <input id="adminUser" placeholder="Email / Phone">
    <input id="adminPass" type="password" placeholder="Password">
    <button class="btn" onclick="loginAdmin()">Login</button>
  </div>
</section>

<!-- 3️⃣ HOME -->
<section id="home">
  <div class="hero">
    <h1>Welcome Admin</h1>
    <p>Manage your tribal artisan marketplace and orders.</p>
    <button class="btn" onclick="show('products')">Go to Products</button>
  </div>
</section>

<!-- 4️⃣ PRODUCTS -->
<section id="products">
  <div class="container">
    <h2>All Handmade Products</h2>
    <div class="grid">
      <div class="card">
        <img src="https://images.stockcake.com/public/7/b/d/7bdf46ce-dd9b-42a0-bf53-002aeb11214f_large/vibrant-textile-patterns-stockcake.jpg">
        <div class="info">
          <h3>Handwoven Textiles</h3>
          <p class="price">₹500</p>
          <button class="btn" onclick="buy('Handwoven Textiles',500)">Buy</button>
        </div>
      </div>
      <div class="card">
        <img src="https://c9admin.cottage9.com/uploads/6167/The-Art-Of-Wood-Carving-Famous-Techniques-And-Tools-Cottage9.jpg">
        <div class="info">
          <h3>Wood Carvings</h3>
          <p class="price">₹200</p>
          <button class="btn" onclick="buy('Wood Carvings',200)">Buy</button>
        </div>
      </div>
      <div class="card">
        <img src="https://kreateworld.in/cdn/shop/products/e39f231c-270c-41c1-9a62-2be16acdffe7.jpg?v=1673000884">
        <div class="info">
          <h3>Beaded Jewelry</h3>
          <p class="price">₹100</p>
          <button class="btn" onclick="buy('Beaded Jewelry',100)">Buy</button>
        </div>
      </div>
          <div class="card">
        <img src="https://veronicapock.com/wp-content/uploads/2022/06/waste-paper-weaving-full-piece.jpg">
        <div class="info">
          <h3>Handwoven Textiles</h3>
          <p class="price">₹200</p>
          <button class="btn" onclick="buy('Handwoven Textiles',500)">Buy</button>
        </div>
      </div>
      <div class="card">
        <img src="https://tse2.mm.bing.net/th/id/OIP.xtqqa3j48p61m0LkbDSxhgHaHa?w=626&h=626&rs=1&pid=ImgDetMain&o=7&rm=3">
        <div class="info">
          <h3>Wood Carvings</h3>
          <p class="price">₹200</p>
          <button class="btn" onclick="buy('Wood Carvings',200)">Buy</button>
        </div>
      </div>
      <div class="card">
        <img src="https://tse3.mm.bing.net/th/id/OIP.HwVs8hk7qFrrvDpKetyEtQHaJQ?rs=1&pid=ImgDetMain&o=7&rm=3">
        <div class="info">
          <h3>Beaded Jewelry</h3>
          <p class="price">₹100</p>
          <button class="btn" onclick="buy('Beaded Jewelry',100)">Buy</button>
        </div>
      </div>
          <div class="card">
        <img src="https://th.bing.com/th/id/OIP.Y15R3HFRL3UEVXyRbHTy1AAAAA?o=7rm=3&rs=1&pid=ImgDetMain&o=7&rm=3">
        <div class="info">
          <h3>Handwoven Textiles</h3>
          <p class="price">₹500</p>
          <button class="btn" onclick="buy('Handwoven Textiles',500)">Buy</button>
        </div>
      </div>
      <div class="card">
        <img src="https://tse4.mm.bing.net/th/id/OIP.ZQM1aTwwesuFJv61sF4udAHaJ_?rs=1&pid=ImgDetMain&o=7&rm=3">
        <div class="info">
          <h3>Wood Carvings</h3>
          <p class="price">₹200</p>
          <button class="btn" onclick="buy('Wood Carvings',200)">Buy</button>
        </div>
      </div>
      <div class="card">
        <img src="https://tse3.mm.bing.net/th/id/OIP.2MtdvgsKOaahnUIBZ8xqKwHaE8?rs=1&pid=ImgDetMain&o=7&rm=3">
        <div class="info">
          <h3>Beaded Jewelry</h3>
          <p class="price">₹100</p>
          <button class="btn" onclick="buy('Beaded Jewelry',100)">Buy</button>
        </div>
      </div>
          <div class="card">
        <img src="https://tse2.mm.bing.net/th/id/OIP.iJMXmV9jOPJTwguV2OMVLgHaEJ?rs=1&pid=ImgDetMain&o=7&rm=3">
        <div class="info">
          <h3>Handwoven Textiles</h3>
          <p class="price">₹500</p>
          <button class="btn" onclick="buy('Handwoven Textiles',500)">Buy</button>
        </div>
      </div>
      <div class="card">
        <img src="https://i.pinimg.com/originals/48/d5/a4/48d5a4d436e50b8c422e3c7ba3ea5b2f.jpg">
        <div class="info">
          <h3>Wood Carvings</h3>
          <p class="price">₹500</p>
          <button class="btn" onclick="buy('Wood Carvings',500)">Buy</button>
        </div>
      </div>
      <div class="card">
        <img src="https://i.ytimg.com/vi/ItKBMxyf6Uk/maxresdefault.jpg">
        <div class="info">
          <h3>Beaded Jewelry</h3>
          <p class="price">₹100</p>
          <button class="btn" onclick="buy('Beaded Jewelry',100)">Buy</button>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- 5️⃣ PAYMENT -->
<section id="payment">
  <div class="pay-box">
    <h2>Secure Payment</h2>
    <p><b>Product:</b> <span id="pName"></span></p>
    <p><b>Price:</b> ₹<span id="pPrice"></span></p>
    <input id="custName" placeholder="Full Name">
    <input id="custPhone" placeholder="Phone Number">
    <input id="custAddress" placeholder="Delivery Address">
    <input id="custUpi" placeholder="UPI ID (PhonePe / GPay / Paytm)">
    <button class="btn" onclick="pay()">Pay Now</button>
  </div>
</section>

<!-- 6️⃣ ORDER TRACKING -->
<section id="track">
  <div class="login-box">
    <h2>Track Order</h2>
    <input id="trackId" placeholder="Enter Order ID">
    <button class="btn" onclick="trackOrder()">Check</button>
    <p id="trackResult" style="margin-top:10px;font-weight:bold;"></p>
  </div>
</section>

<!-- 7️⃣ ADMIN PANEL (DETAILS + ORDERS) -->
<section id="adminPanel">
  <div class="container">
    <h2>Admin Panel</h2>
    <h3>Admin Details</h3>
    <p id="adminDetails"></p>
    <h3>Orders</h3>
    <div id="adminOrders"></div>
  </div>
</section>

<script>
// Generic section switcher
function show(page){
  document.querySelectorAll("section").forEach(s=>s.classList.remove("active"));
  document.getElementById(page).classList.add("active");
  window.scrollTo(0,0);
}

// Global orders array (from localStorage)
let orders = JSON.parse(localStorage.getItem("orders") || "[]");

// 1) SIGNUP ADMIN
function signupAdmin(){
  const admin = {
    name: document.getElementById("adName").value.trim(),
    age: document.getElementById("adAge").value.trim(),
    phone: document.getElementById("adPhone").value.trim(),
    email: document.getElementById("adEmail").value.trim(),
    pass: document.getElementById("adPass").value.trim()
  };

  if(!admin.name || !admin.age || !admin.phone || !admin.email || !admin.pass){
    alert("Please fill all signup details.");
    return;
  }

  localStorage.setItem("admin", JSON.stringify(admin));
  alert("Signup successful! Now login.");
  show("adminLogin");
}

// 2) LOGIN ADMIN
function loginAdmin(){
  const admin = JSON.parse(localStorage.getItem("admin") || "null");
  if(!admin){
    alert("No admin registered. Please sign up first.");
    show("adminSignup");
    return;
  }

  const user = document.getElementById("adminUser").value.trim();
  const pass = document.getElementById("adminPass").value.trim();

  if((user === admin.email || user === admin.phone) && pass === admin.pass){
    document.getElementById("adminNav").style.display = "block";
    show("home");
  } else {
    alert("Incorrect email/phone or password.");
  }
}

// 3) BUY → GO TO PAYMENT
function buy(name, price){
  localStorage.setItem("product", name);
  localStorage.setItem("price", price);
  document.getElementById("pName").innerText = name;
  document.getElementById("pPrice").innerText = price;
  show("payment");
}

// 4) PAYMENT → SAVE ORDER → GO TO TRACK
function pay(){
  const customer = {
    name: document.getElementById("custName").value.trim(),
    phone: document.getElementById("custPhone").value.trim(),
    address: document.getElementById("custAddress").value.trim(),
    upi: document.getElementById("custUpi").value.trim()
  };

  if(!customer.name || !customer.phone || !customer.address || !customer.upi){
    alert("Please fill all payment details.");
    return;
  }

  const id = Math.floor(Math.random()*900000) + 100000;
  const order = {
    id,
    product: localStorage.getItem("product"),
    price: localStorage.getItem("price"),
    name: customer.name,
    phone: customer.phone,
    address: customer.address,
    upi: customer.upi,
    status: "Order Placed"
  };

  orders.push(order);
  localStorage.setItem("orders", JSON.stringify(orders));

  alert("Payment successful! Your Order ID: " + id);
  show("track");
  document.getElementById("trackId").value = id; // auto-fill for user
  trackOrder();
}

// 5) TRACK ORDER
function trackOrder(){
  const id = document.getElementById("trackId").value.trim();
  const o = orders.find(x => String(x.id) === id);
  const el = document.getElementById("trackResult");

  if(!o){
    el.innerHTML = "❌ Order Not Found";
  } else {
    el.innerHTML = `
      ✅ Order Found<br>
      <b>ID:</b> ${o.id}<br>
      <b>Product:</b> ${o.product}<br>
      <b>Price:</b> ₹${o.price}<br>
      <b>Status:</b> ${o.status}
    `;
  }
}

// 6) OPEN ADMIN PANEL (SHOW DETAILS + ORDERS)
function openAdminPanel(){
  show("adminPanel");
  renderAdminPanel();
}

function renderAdminPanel(){
  const admin = JSON.parse(localStorage.getItem("admin") || "null");
  const adminDetails = document.getElementById("adminDetails");
  const adminOrders = document.getElementById("adminOrders");

  if(!admin){
    adminDetails.innerHTML = "No admin details found. Please sign up again.";
    adminOrders.innerHTML = "";
    return;
  }

  adminDetails.innerHTML = `
    <b>Name:</b> ${admin.name}<br>
    <b>Age:</b> ${admin.age}<br>
    <b>Phone:</b> ${admin.phone}<br>
    <b>Email:</b> ${admin.email}<br>
    <b>Total Orders:</b> ${orders.length}
  `;

  if(orders.length === 0){
    adminOrders.innerHTML = "<p>No orders yet.</p>";
    return;
  }

  adminOrders.innerHTML = orders.map(o => `
    <p>
      <b>ID:</b> ${o.id} | 
      <b>${o.product}</b> | 
      ₹${o.price} | 
      Status: ${o.status}
    </p>
  `).join("");
}
</script>
</body>
</html>

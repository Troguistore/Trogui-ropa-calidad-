<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TROGÜI - Tienda Online Colombia</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700;800;900&family=Nunito:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
:root{
  --orange:#FF5200;
  --dark:#1a1a2e;
  --white:#fff;
  --light:#f8f8f8;
  --green:#00b050;
  --red:#e00;
  --gray:#666;
  --border:#e5e5e5;
  --shadow:0 4px 20px rgba(0,0,0,.10);
}
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'Nunito',sans-serif;background:#f4f4f4;color:var(--dark);overflow-x:hidden}
a{text-decoration:none;color:inherit}
img{max-width:100%;border-radius:8px}

/* TOP BAR */
.topbar{background:var(--dark);color:#fff;text-align:center;padding:7px;font-size:13px;font-weight:700;letter-spacing:.5px}
.topbar span{color:var(--orange)}

/* HEADER */
header{background:#fff;box-shadow:0 2px 12px rgba(0,0,0,.09);position:sticky;top:0;z-index:900}
.header-inner{max-width:1300px;margin:0 auto;display:flex;align-items:center;gap:16px;padding:12px 16px;flex-wrap:wrap}
.logo-area{display:flex;align-items:center;gap:8px;min-width:160px}
.logo-svg{width:130px;height:44px}
.search-bar{flex:1;min-width:180px;position:relative}
.search-bar input{width:100%;padding:10px 44px 10px 16px;border:2px solid var(--border);border-radius:30px;font-size:15px;font-family:'Nunito',sans-serif;outline:none;transition:.2s}
.search-bar input:focus{border-color:var(--orange)}
.search-bar button{position:absolute;right:8px;top:50%;transform:translateY(-50%);background:var(--orange);border:none;border-radius:50%;width:32px;height:32px;color:#fff;cursor:pointer;font-size:15px}
.header-actions{display:flex;align-items:center;gap:14px;flex-wrap:wrap}
.whatsapp-btn{display:flex;align-items:center;gap:6px;background:#25D366;color:#fff;padding:8px 14px;border-radius:20px;font-weight:700;font-size:13px;transition:.2s}
.whatsapp-btn:hover{background:#128C7E}
.cart-btn{position:relative;background:var(--orange);color:#fff;border:none;border-radius:20px;padding:8px 16px;font-weight:700;font-size:14px;cursor:pointer;display:flex;align-items:center;gap:6px}
.cart-count{background:#fff;color:var(--orange);border-radius:50%;width:20px;height:20px;font-size:12px;font-weight:900;display:flex;align-items:center;justify-content:center}
.social-links{display:flex;gap:8px}
.social-links a{width:34px;height:34px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:17px;transition:.2s}
.social-links a.ig{background:linear-gradient(45deg,#f09433,#e6683c,#dc2743,#cc2366,#bc1888)}
.social-links a.tk{background:#010101;color:#fff}
.social-links a.wa{background:#25D366;color:#fff}
.social-links a:hover{transform:scale(1.13)}

/* NAV */
nav{background:var(--orange);padding:0 16px}
.nav-inner{max-width:1300px;margin:0 auto;display:flex;gap:4px;overflow-x:auto;padding:0}
.nav-inner a{color:#fff;padding:12px 18px;font-weight:700;font-size:14px;white-space:nowrap;border-bottom:3px solid transparent;transition:.2s}
.nav-inner a:hover,.nav-inner a.active{border-bottom-color:#fff;background:rgba(255,255,255,.12)}

/* BANNERS SLIDER */
.slider-section{background:#fff;padding:0}
.slider-wrap{position:relative;overflow:hidden;max-height:320px}
.slider-track{display:flex;transition:transform .6s ease}
.slide{min-width:100%;height:260px;display:flex;align-items:center;justify-content:center;position:relative;overflow:hidden}
.slide-1{background:linear-gradient(135deg,#1a1a2e 60%,#FF5200 100%)}
.slide-2{background:linear-gradient(135deg,#0f3460 60%,#e94560 100%)}
.slide-3{background:linear-gradient(135deg,#16213e 60%,#0f3460 100%)}
.slide-content{color:#fff;padding:32px;z-index:2}
.slide-content h2{font-size:clamp(22px,4vw,42px);font-weight:900;line-height:1.2;font-family:'Poppins',sans-serif}
.slide-content h2 span{color:var(--orange)}
.slide-content p{font-size:15px;margin:10px 0 18px;opacity:.9}
.slide-btn{background:var(--orange);color:#fff;padding:12px 28px;border-radius:30px;font-weight:800;font-size:15px;display:inline-block;transition:.2s}
.slide-btn:hover{background:#e04800;transform:scale(1.05)}
.slider-dots{display:flex;justify-content:center;gap:8px;padding:12px;background:#fff}
.dot{width:10px;height:10px;border-radius:50%;background:#ccc;cursor:pointer;transition:.2s}
.dot.active{background:var(--orange);width:24px;border-radius:5px}
.slider-arrow{position:absolute;top:50%;transform:translateY(-50%);background:rgba(255,255,255,.2);color:#fff;border:none;font-size:22px;width:42px;height:42px;border-radius:50%;cursor:pointer;z-index:10;transition:.2s}
.slider-arrow:hover{background:rgba(255,255,255,.4)}
.slider-arrow.prev{left:12px}
.slider-arrow.next{right:12px}

/* BADGES STRIP */
.badges-strip{background:#fff;border-bottom:2px solid var(--border)}
.badges-inner{max-width:1300px;margin:0 auto;display:flex;justify-content:center;flex-wrap:wrap;gap:0}
.badge-item{display:flex;align-items:center;gap:8px;padding:14px 24px;font-weight:700;font-size:13px;border-right:1px solid var(--border)}
.badge-item:last-child{border-right:none}
.badge-item svg,.badge-item span.ico{font-size:22px;color:var(--orange)}

/* NOTIFICATION */
.notif{position:fixed;bottom:80px;left:16px;background:var(--dark);color:#fff;padding:10px 16px;border-radius:12px;font-size:13px;font-weight:700;z-index:1200;display:none;max-width:280px;box-shadow:0 4px 20px rgba(0,0,0,.3);animation:slideUp .4s}
@keyframes slideUp{from{opacity:0;transform:translateY(20px)}to{opacity:1;transform:translateY(0)}}
.notif .notif-name{color:var(--orange)}

/* SECTION TITLES */
.section-title{text-align:center;padding:30px 16px 8px;font-size:clamp(20px,3vw,28px);font-weight:900;font-family:'Poppins',sans-serif;color:var(--dark)}
.section-title span{color:var(--orange)}
.section-sub{text-align:center;color:var(--gray);margin-bottom:20px;font-size:14px}

/* PRODUCTS GRID */
.products-section{max-width:1300px;margin:0 auto;padding:0 12px 40px}
.products-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:16px}

/* PRODUCT CARD */
.product-card{background:#fff;border-radius:16px;overflow:hidden;box-shadow:var(--shadow);transition:.25s;position:relative;cursor:pointer}
.product-card:hover{transform:translateY(-4px);box-shadow:0 8px 32px rgba(0,0,0,.15)}
.product-img-wrap{position:relative;background:#f8f8f8;height:200px;overflow:hidden;display:flex;align-items:center;justify-content:center}
.product-img-wrap img{height:180px;width:100%;object-fit:cover;transition:.3s}
.product-card:hover .product-img-wrap img{transform:scale(1.06)}
.badge-offer{position:absolute;top:10px;left:10px;background:var(--orange);color:#fff;font-size:11px;font-weight:800;padding:4px 10px;border-radius:20px}
.badge-sold{position:absolute;top:10px;right:10px;background:var(--dark);color:#fff;font-size:10px;font-weight:700;padding:3px 8px;border-radius:10px}
.badge-last{position:absolute;bottom:10px;left:10px;background:var(--red);color:#fff;font-size:10px;font-weight:800;padding:3px 8px;border-radius:10px;animation:pulse 1.2s infinite}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:.6}}
.product-info{padding:12px}
.product-name{font-weight:800;font-size:14px;line-height:1.3;margin-bottom:6px;font-family:'Poppins',sans-serif}
.stars{color:#f5c518;font-size:14px;margin-bottom:4px}
.stars span{color:var(--gray);font-size:12px;margin-left:4px}
.price-wrap{display:flex;align-items:center;gap:8px;flex-wrap:wrap}
.price-old{color:var(--gray);font-size:13px;text-decoration:line-through}
.price-new{color:var(--orange);font-size:20px;font-weight:900}
.timer-badge{background:#fff3e0;border:1px solid var(--orange);border-radius:8px;padding:4px 8px;font-size:11px;font-weight:800;color:var(--orange);margin-top:6px;display:flex;align-items:center;gap:4px}
.btn-add{width:100%;background:var(--orange);color:#fff;border:none;padding:10px;border-radius:10px;font-weight:800;font-size:14px;cursor:pointer;margin-top:10px;transition:.2s;font-family:'Nunito',sans-serif}
.btn-add:hover{background:#e04800}
.free-ship{font-size:11px;color:var(--green);font-weight:800;display:flex;align-items:center;gap:3px;margin-top:4px}
.delivery-info{font-size:11px;color:var(--gray);margin-top:3px}

/* PRODUCT MODAL */
.modal-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.55);z-index:1100;align-items:center;justify-content:center;padding:16px}
.modal-overlay.active{display:flex}
.modal-box{background:#fff;border-radius:20px;max-width:700px;width:100%;max-height:90vh;overflow-y:auto;position:relative;padding:0}
.modal-close{position:absolute;top:14px;right:14px;background:var(--dark);color:#fff;border:none;border-radius:50%;width:32px;height:32px;font-size:18px;cursor:pointer;z-index:10}
.modal-content{padding:24px}
.modal-imgs{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:16px}
.modal-imgs img{border-radius:10px;height:200px;object-fit:cover}
.modal-title{font-size:20px;font-weight:900;font-family:'Poppins',sans-serif;margin-bottom:8px}
.modal-price-wrap{display:flex;align-items:center;gap:12px;margin:10px 0}
.modal-price-old{font-size:16px;text-decoration:line-through;color:var(--gray)}
.modal-price-new{font-size:28px;font-weight:900;color:var(--orange)}
.modal-desc{font-size:14px;color:var(--gray);line-height:1.6;margin:10px 0}
.modal-delivery{background:#f0fff4;border:1px solid var(--green);border-radius:10px;padding:12px;margin:12px 0;font-size:13px}
.modal-delivery strong{color:var(--green)}
.btn-order{width:100%;background:var(--orange);color:#fff;border:none;padding:14px;border-radius:14px;font-weight:900;font-size:16px;cursor:pointer;margin-top:12px;font-family:'Nunito',sans-serif;transition:.2s}
.btn-order:hover{background:#e04800}

/* REVIEWS */
.review-list{margin-top:20px}
.review-item{border:1px solid var(--border);border-radius:12px;padding:12px;margin-bottom:10px}
.review-top{display:flex;align-items:center;gap:10px;margin-bottom:6px}
.review-avatar{width:36px;height:36px;border-radius:50%;background:var(--orange);color:#fff;display:flex;align-items:center;justify-content:center;font-weight:900;font-size:15px}
.review-name{font-weight:800;font-size:14px}
.review-stars{color:#f5c518;font-size:13px}
.review-text{font-size:13px;color:#444;line-height:1.5}

/* ORDER FORM */
.order-form-section{display:none;position:fixed;inset:0;background:rgba(0,0,0,.6);z-index:1200;align-items:center;justify-content:center;padding:16px}
.order-form-section.active{display:flex}
.order-form-box{background:#fff;border-radius:20px;max-width:540px;width:100%;max-height:90vh;overflow-y:auto;padding:28px;position:relative}
.form-title{font-size:20px;font-weight:900;font-family:'Poppins',sans-serif;margin-bottom:6px}
.form-prod{font-size:14px;color:var(--gray);margin-bottom:16px}
.form-price-show{background:#fff8f0;border:2px solid var(--orange);border-radius:12px;padding:12px;margin-bottom:16px;display:flex;justify-content:space-between;align-items:center}
.form-price-show .fprice{font-size:22px;font-weight:900;color:var(--orange)}
.form-price-show .fold{font-size:13px;text-decoration:line-through;color:var(--gray)}
.form-group{margin-bottom:14px}
.form-group label{font-weight:700;font-size:14px;display:block;margin-bottom:4px}
.form-group label span.req{color:var(--red)}
.form-group input,.form-group textarea,.form-group select{width:100%;padding:11px 14px;border:2px solid var(--border);border-radius:10px;font-size:14px;font-family:'Nunito',sans-serif;outline:none;transition:.2s;color:var(--dark)}
.form-group input:focus,.form-group textarea:focus{border-color:var(--orange)}
.form-group textarea{resize:vertical;min-height:70px}
.btn-confirm{width:100%;background:var(--green);color:#fff;border:none;padding:14px;border-radius:14px;font-weight:900;font-size:16px;cursor:pointer;margin-top:8px;font-family:'Nunito',sans-serif;transition:.2s}
.btn-confirm:hover{background:#009040}
.btn-cancel{width:100%;background:#eee;color:var(--dark);border:none;padding:11px;border-radius:14px;font-weight:700;font-size:14px;cursor:pointer;margin-top:8px;font-family:'Nunito',sans-serif}

/* CART DRAWER */
.cart-drawer{position:fixed;right:-400px;top:0;height:100vh;width:370px;background:#fff;box-shadow:-4px 0 30px rgba(0,0,0,.2);z-index:1300;transition:.35s;overflow-y:auto;padding:20px}
.cart-drawer.open{right:0}
.cart-drawer-title{font-size:20px;font-weight:900;font-family:'Poppins',sans-serif;margin-bottom:16px;display:flex;justify-content:space-between;align-items:center}
.cart-item{display:flex;gap:12px;border-bottom:1px solid var(--border);padding:12px 0}
.cart-item img{width:70px;height:70px;object-fit:cover;border-radius:8px;background:#f4f4f4}
.cart-item-info{flex:1}
.cart-item-name{font-weight:700;font-size:14px}
.cart-item-price{color:var(--orange);font-weight:900;font-size:15px}
.cart-item-remove{color:var(--red);font-size:18px;cursor:pointer;background:none;border:none}
.cart-total{font-size:18px;font-weight:900;color:var(--orange);text-align:right;margin:16px 0}
.btn-checkout{width:100%;background:var(--orange);color:#fff;border:none;padding:14px;border-radius:14px;font-weight:900;font-size:16px;cursor:pointer;font-family:'Nunito',sans-serif}
.empty-cart{text-align:center;color:var(--gray);padding:40px 0;font-size:15px}

/* DELIVERY CALCULATOR */
.delivery-calc{background:#fff;max-width:500px;margin:0 auto 30px;border-radius:16px;padding:20px;box-shadow:var(--shadow)}
.delivery-calc h3{font-size:17px;font-weight:900;margin-bottom:12px;font-family:'Poppins',sans-serif}
.delivery-result{background:#f0fff4;border:1px solid var(--green);border-radius:10px;padding:12px;font-size:14px;font-weight:700;color:var(--green);margin-top:10px}

/* FOOTER */
footer{background:var(--dark);color:#fff;padding:40px 16px 20px;margin-top:20px}
.footer-grid{max-width:1300px;margin:0 auto;display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:30px}
.footer-logo{font-size:28px;font-weight:900;color:var(--orange);margin-bottom:12px}
.footer-col h4{font-weight:800;margin-bottom:12px;color:var(--orange)}
.footer-col p,.footer-col li{font-size:13px;color:#bbb;line-height:1.9;list-style:none}
.footer-bottom{text-align:center;margin-top:30px;padding-top:20px;border-top:1px solid #333;font-size:12px;color:#888}

/* WHATSAPP FLOAT */
.wa-float{position:fixed;bottom:90px;right:20px;background:#25D366;color:#fff;width:54px;height:54px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:26px;box-shadow:0 4px 16px rgba(0,0,0,.3);z-index:1000;transition:.2s;text-decoration:none}
.wa-float:hover{transform:scale(1.1);background:#128C7E}

/* ADMIN BUTTONS */
.admin-btns{position:fixed;bottom:16px;right:16px;display:flex;gap:8px;z-index:1100}
.admin-btn{width:36px;height:36px;border-radius:50%;border:none;font-weight:900;font-size:14px;cursor:pointer;opacity:.6;transition:.2s;box-shadow:0 2px 8px rgba(0,0,0,.2)}
.admin-btn:hover{opacity:1;transform:scale(1.1)}
.admin-btn.r-btn{background:var(--orange);color:#fff}
.admin-btn.c-btn{background:var(--dark);color:#fff}
.admin-btn.e-btn{background:#0f3460;color:#fff}

/* ADMIN PANELS */
.admin-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.6);z-index:2000;align-items:flex-start;justify-content:center;padding:16px;overflow-y:auto}
.admin-overlay.active{display:flex}
.admin-panel{background:#fff;border-radius:20px;max-width:900px;width:100%;margin:20px auto;padding:24px;position:relative;max-height:90vh;overflow-y:auto}
.admin-panel h2{font-size:22px;font-weight:900;font-family:'Poppins',sans-serif;color:var(--orange);margin-bottom:20px}
.admin-product-list{display:grid;gap:12px}
.admin-product-item{border:2px solid var(--border);border-radius:12px;padding:16px;display:grid;gap:8px}
.admin-product-item label{font-weight:700;font-size:13px;margin-bottom:2px;display:block}
.admin-product-item input,.admin-product-item textarea{width:100%;padding:8px 12px;border:1.5px solid var(--border);border-radius:8px;font-size:13px;font-family:'Nunito',sans-serif}
.admin-product-item .row2{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.btn-save-admin{background:var(--green);color:#fff;border:none;padding:10px 20px;border-radius:10px;font-weight:800;cursor:pointer;font-family:'Nunito',sans-serif;margin-top:8px}
.btn-del-admin{background:var(--red);color:#fff;border:none;padding:6px 12px;border-radius:8px;font-weight:700;cursor:pointer;font-size:12px;font-family:'Nunito',sans-serif}
.btn-add-prod{background:var(--orange);color:#fff;border:none;padding:12px 24px;border-radius:12px;font-weight:800;cursor:pointer;font-size:15px;font-family:'Nunito',sans-serif;margin-bottom:20px}
.admin-orders{display:grid;gap:10px}
.order-item{border:2px solid var(--border);border-radius:12px;padding:14px;font-size:13px}
.order-item strong{color:var(--orange)}
.order-item .order-meta{color:var(--gray);font-size:12px;margin-top:4px}
/* Page editor */
.page-editor-section{display:grid;gap:14px}
.page-editor-group{border:1px solid var(--border);border-radius:12px;padding:14px}
.page-editor-group label{font-weight:800;font-size:14px;display:block;margin-bottom:6px;color:var(--dark)}
.page-editor-group input,.page-editor-group textarea{width:100%;padding:9px 13px;border:1.5px solid var(--border);border-radius:8px;font-size:13px;font-family:'Nunito',sans-serif}
.page-editor-group textarea{min-height:60px;resize:vertical}

/* VISITORS */
.visitors-badge{background:var(--dark);color:#fff;border-radius:12px;padding:10px 16px;font-size:13px;font-weight:700;margin-bottom:16px;display:flex;align-items:center;gap:8px}
.visitors-dot{width:10px;height:10px;border-radius:50%;background:var(--green);display:inline-block;animation:blink 1s infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.2}}

/* SEARCH DROPDOWN */
.search-dropdown{position:absolute;top:110%;left:0;right:0;background:#fff;border-radius:12px;box-shadow:0 8px 24px rgba(0,0,0,.15);z-index:500;display:none;max-height:280px;overflow-y:auto}
.search-dropdown.open{display:block}
.search-dropdown-item{padding:10px 16px;cursor:pointer;font-size:14px;border-bottom:1px solid var(--border);transition:.15s;display:flex;align-items:center;gap:10px}
.search-dropdown-item:hover{background:#fff8f0}
.search-dropdown-item img{width:36px;height:36px;object-fit:cover;border-radius:6px;background:#f4f4f4}

/* RESPONSIVE */
@media(max-width:700px){
  .header-inner{flex-wrap:wrap;gap:10px}
  .products-grid{grid-template-columns:repeat(2,1fr)}
  .modal-imgs{grid-template-columns:1fr}
  .cart-drawer{width:100%;right:-110%}
  .admin-product-item .row2{grid-template-columns:1fr}
  .badges-inner{gap:0}
  .badge-item{padding:10px 12px;font-size:12px}
}
@media(max-width:400px){
  .products-grid{grid-template-columns:1fr}
}

/* AUDIO */
#audio-autoplay{display:none}

/* REVIEW in admin */
.admin-review-item{border:1.5px solid var(--border);border-radius:10px;padding:12px;display:grid;gap:6px;margin-bottom:10px}
.admin-review-item input,.admin-review-item textarea,.admin-review-item select{width:100%;padding:7px 10px;border:1.5px solid var(--border);border-radius:7px;font-size:13px;font-family:'Nunito',sans-serif}

</style>
</head>
<body>

<!-- AUDIO AUTOPLAY -->
<audio id="audio-autoplay" autoplay loop>
  <source id="audio-src" src="" type="audio/mpeg">
</audio>

<!-- TOPBAR -->
<div class="topbar">🇨🇴 Envíos a toda Colombia &nbsp;|&nbsp; <span>¡PAGO CONTRA ENTREGA!</span> &nbsp;|&nbsp; 📦 Interrapidísimo · Coordinadora · Envia</div>

<!-- HEADER -->
<header>
  <div class="header-inner">
    <div class="logo-area">
      <svg class="logo-svg" viewBox="0 0 200 70" xmlns="http://www.w3.org/2000/svg" id="main-logo">
        <rect width="200" height="70" rx="10" fill="#FF5200"/>
        <text x="16" y="52" font-family="Poppins,sans-serif" font-weight="900" font-size="38" fill="#1a1a2e" letter-spacing="-1">TROGÜI</text>
      </svg>
    </div>
    <div class="search-bar" style="position:relative">
      <input type="text" id="search-input" placeholder="🔍  Buscar productos..." autocomplete="off" oninput="searchProducts(this.value)">
      <button onclick="searchProducts(document.getElementById('search-input').value)">🔍</button>
      <div class="search-dropdown" id="search-dropdown"></div>
    </div>
    <div class="header-actions">
      <a href="https://wa.link/lhneng" target="_blank" class="whatsapp-btn">📱 320 657 2598</a>
      <div class="social-links">
        <a href="https://www.instagram.com/store_trog?igsh=MWZleXFlY21weDhnMQ%3D%3D&utm_source=qr" target="_blank" class="ig" title="Instagram">📸</a>
        <a href="https://www.tiktok.com/@trogui_store?_r=1&_t=ZS-96QXU6BiNk2" target="_blank" class="tk" title="TikTok">🎵</a>
        <a href="https://wa.link/lhneng" target="_blank" class="wa" title="WhatsApp">💬</a>
      </div>
      <button class="cart-btn" onclick="toggleCart()">🛒 Carrito <span class="cart-count" id="cart-count">0</span></button>
    </div>
  </div>
</header>

<!-- NAV -->
<nav>
  <div class="nav-inner">
    <a href="#" class="active" onclick="filterCat('all',this)">🏠 Tienda</a>
    <a href="#" onclick="filterCat('belleza',this)">💄 Belleza</a>
    <a href="#" onclick="filterCat('hogar',this)">🏡 Hogar</a>
    <a href="#" onclick="filterCat('tecnologia',this)">📱 Tecnología</a>
    <a href="#" onclick="filterCat('salud',this)">💊 Salud</a>
    <a href="#" onclick="filterCat('fitness',this)">🏋️ Fitness</a>
    <a href="#" onclick="filterCat('juguetes',this)">🧸 Juguetes</a>
    <a href="#" onclick="filterCat('accesorios',this)">👜 Accesorios</a>
  </div>
</nav>

<!-- SLIDER -->
<div class="slider-section">
  <div class="slider-wrap" id="main-slider">
    <div class="slider-track" id="slider-track">
      <div class="slide slide-1">
        <div class="slide-content">
          <h2>🇨🇴 Envíos Gratis<br>a <span>Toda Colombia</span></h2>
          <p>Más de 45 productos con descuentos increíbles • Pago contra entrega</p>
          <a href="#products" class="slide-btn">¡Ver Ofertas!</a>
        </div>
      </div>
      <div class="slide slide-2">
        <div class="slide-content">
          <h2>⚡ Pago<br><span>Contra Entrega</span></h2>
          <p>Sin riesgo, sin tarjetas. Pagas cuando recibes tu pedido en casa.</p>
          <a href="#products" class="slide-btn">Ver Productos</a>
        </div>
      </div>
      <div class="slide slide-3">
        <div class="slide-content">
          <h2>📦 Recibe en<br><span>3 a 7 Días</span></h2>
          <p>Coordinadora · Interrapidísimo · Envia · Entrega a domicilio</p>
          <a href="#products" class="slide-btn">Comprar Ahora</a>
        </div>
      </div>
    </div>
    <button class="slider-arrow prev" onclick="moveSlider(-1)">‹</button>
    <button class="slider-arrow next" onclick="moveSlider(1)">›</button>
  </div>
  <div class="slider-dots" id="slider-dots">
    <div class="dot active" onclick="goSlide(0)"></div>
    <div class="dot" onclick="goSlide(1)"></div>
    <div class="dot" onclick="goSlide(2)"></div>
  </div>
</div>

<!-- BADGES -->
<div class="badges-strip">
  <div class="badges-inner">
    <div class="badge-item">✅ <b>Pago Contra Entrega</b></div>
    <div class="badge-item">🚚 <b>Envío Gratis Colombia</b></div>
    <div class="badge-item">📦 <b>3 a 7 días hábiles</b></div>
    <div class="badge-item">🔒 <b>Compra 100% Segura</b></div>
    <div class="badge-item">⭐ <b>+500 Clientes Felices</b></div>
  </div>
</div>

<!-- NOTIFICATION -->
<div class="notif" id="notif-box"></div>

<!-- PRODUCTS -->
<div id="products">
  <h2 class="section-title">🔥 Productos en <span>OFERTA</span></h2>
  <p class="section-sub">Envío gratis a toda Colombia · Pago contra entrega · Solo quedan pocas unidades</p>
  <div class="products-section">
    <div class="products-grid" id="products-grid">
      <!-- Rendered by JS -->
    </div>
  </div>
</div>

<!-- DELIVERY CALC -->
<div style="max-width:1300px;margin:0 auto;padding:0 12px 20px">
  <div class="delivery-calc">
    <h3>📅 ¿Cuándo llega mi pedido?</h3>
    <p style="font-size:13px;color:var(--gray);margin-bottom:10px">Ingresa tu ciudad y te decimos la fecha estimada de entrega:</p>
    <select id="delivery-city" style="width:100%;padding:10px;border:2px solid var(--border);border-radius:10px;font-size:14px;margin-bottom:8px;font-family:'Nunito',sans-serif">
      <option value="">-- Selecciona tu ciudad --</option>
      <option value="3">Bogotá</option>
      <option value="4">Medellín</option>
      <option value="4">Cali</option>
      <option value="5">Barranquilla</option>
      <option value="5">Cartagena</option>
      <option value="5">Bucaramanga</option>
      <option value="6">Pereira</option>
      <option value="6">Manizales</option>
      <option value="7">Pasto</option>
      <option value="7">Montería</option>
      <option value="7">Leticia</option>
    </select>
    <button onclick="calcDelivery()" style="background:var(--orange);color:#fff;border:none;padding:10px 24px;border-radius:10px;font-weight:800;cursor:pointer;font-family:'Nunito',sans-serif">Calcular</button>
    <div class="delivery-result" id="delivery-result" style="display:none"></div>
  </div>
</div>

<!-- PRODUCT MODAL -->
<div class="modal-overlay" id="product-modal">
  <div class="modal-box">
    <button class="modal-close" onclick="closeModal()">✕</button>
    <div class="modal-content" id="modal-content"></div>
  </div>
</div>

<!-- ORDER FORM -->
<div class="order-form-section" id="order-form-section">
  <div class="order-form-box">
    <button onclick="closeOrderForm()" style="position:absolute;top:14px;right:14px;background:#1a1a2e;color:#fff;border:none;border-radius:50%;width:32px;height:32px;font-size:18px;cursor:pointer;z-index:10">✕</button>
    <h2 class="form-title">🛒 Confirmar Pedido</h2>
    <p class="form-prod" id="form-prod-name" style="color:#FF5200;font-weight:800;margin-bottom:8px"></p>
    <div class="form-price-show" id="form-price-show"></div>

    <!-- Transportadoras image -->
    <div style="text-align:center;margin:14px 0 10px">
      <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAA0JCgsKCA0LCgsODg0PEyAVExISEyccHhcgLikxMC4pLSwzOko+MzZGNywtQFdBRkxOUlNSMj5aYVpQYEpRUk//2wBDAQ4ODhMREyYVFSZPNS01T09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT0//wAARCASXArwDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwDv6KWigBKKWigBKKWigBKKWigBKKWigBKKKWgBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWkoAKKWigBKKKWgBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWigBKKWkoAKKWigBKKWigAopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAEopaKAFooooAMUYpaKAExRilooATFGKWigBMUYpaKAExRilooATFGKWigBMUYpaKAExRilooATFGKWigBMUYpaKAExRilooATFGKWigBMUYpaKAExRilooATFGKWigBMUYpaKAExRilooATFGKWigBMUYpaKAExRilooATFGKWigBMUYpaKAExRilooATFGKWigBMUYpaKAExRilooATFGKWigBMUYpaKAExRilooATFGKWigBMUYpaKAExRilooATFFLRQAlFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFAC0UUUAFFLRQMSilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooASilooEJRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAtFFFABS0UUAFJS0UDCiiigBKKWigAooooASilooAKKKKAEpaKKACiiigBKWiigAooooASloooAKSlooASloooAKSlooASloooAKSlooAKKKKACkpaKACiiigApKWigAooooASilooAKKKKAEopaKACiiigBKWiigApKWigBKWiigAooooASloooAKSlooASilooEJRRRQAUUUUAFFFFABRS0lABRRRQAUUUUAFFFFABRS0lABRS0lABRRRQAtFFFABRS0UDMxtWRfEUej+Udz25n8zPAAOMYqbWL9dK0m5v2jMgt03lQcZrltc1OHSfiBbXM8U0iGwK4hQu2S3pUPibxbZX3hy/tYrPUEaWIqGktyqj6ntQI7e2mFxaxTgbRIgfHpkZqSsO41aPRvDFpctGZZXjjjhiXrI5AwBVVLfxlKnntfadAx5FsYSwHsWoA6alrmdA12/1DxBeafe26wNa2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" alt="Transportadoras" style="width:100%;max-width:440px;border-radius:14px;box-shadow:0 4px 16px rgba(0,0,0,.13)">
    </div>

    <div class="form-group">
      <label>Nombre <span class="req">*</span></label>
      <input type="text" id="f-nombre" placeholder="Escribe tu nombre">
    </div>
    <div class="form-group">
      <label>Apellido <span class="req">*</span></label>
      <input type="text" id="f-apellido" placeholder="Escribe tu apellido">
    </div>
    <div class="form-group">
      <label>Departamento <span class="req">*</span></label>
      <select id="f-depto" onchange="loadCities()" style="width:100%;padding:11px 14px;border:2px solid #e5e5e5;border-radius:10px;font-size:14px;font-family:Nunito,sans-serif;outline:none">
        <option value="">-- Selecciona tu departamento --</option>
        <option>Amazonas</option><option>Antioquia</option><option>Arauca</option>
        <option>Atlántico</option><option>Bolívar</option><option>Boyacá</option>
        <option>Caldas</option><option>Caquetá</option><option>Casanare</option>
        <option>Cauca</option><option>Cesar</option><option>Chocó</option>
        <option>Córdoba</option><option>Cundinamarca</option><option>Guainía</option>
        <option>Guaviare</option><option>Huila</option><option>La Guajira</option>
        <option>Magdalena</option><option>Meta</option><option>Nariño</option>
        <option>Norte de Santander</option><option>Putumayo</option><option>Quindío</option>
        <option>Risaralda</option><option>San Andrés</option><option>Santander</option>
        <option>Sucre</option><option>Tolima</option><option>Valle del Cauca</option>
        <option>Vaupés</option><option>Vichada</option>
        <option>Bogotá D.C.</option>
      </select>
    </div>
    <div class="form-group">
      <label>Ciudad o Municipio <span class="req">*</span></label>
      <input type="text" id="f-ciudad" placeholder="Escribe tu ciudad o municipio">
    </div>
    <div class="form-group">
      <label>Tipo de entrega <span class="req">*</span></label>
      <div style="display:flex;gap:10px;margin-top:4px;flex-wrap:wrap">
        <label style="flex:1;min-width:140px;border:2px solid #e5e5e5;border-radius:10px;padding:10px;cursor:pointer;display:flex;align-items:center;gap:8px;font-weight:700;font-size:13px" id="lbl-domicilio">
          <input type="radio" name="entrega" value="domicilio" onchange="toggleEntrega()" checked> 🏠 A mi domicilio
        </label>
        <label style="flex:1;min-width:140px;border:2px solid #e5e5e5;border-radius:10px;padding:10px;cursor:pointer;display:flex;align-items:center;gap:8px;font-weight:700;font-size:13px" id="lbl-oficina">
          <input type="radio" name="entrega" value="oficina" onchange="toggleEntrega()"> 📦 Recoger en oficina Interrapidísimo
        </label>
      </div>
    </div>
    <div class="form-group" id="grp-direccion">
      <label>Dirección de entrega <span class="req">*</span></label>
      <input type="text" id="f-direccion" placeholder="Ej: Calle 45 #12-30, Apto 201, Barrio El Poblado">
      <div style="font-size:11px;color:#888;margin-top:3px">Incluye barrio o referencia para facilitar la entrega</div>
    </div>
    <div class="form-group" id="grp-oficina" style="display:none">
      <div style="background:#e8f4fd;border:1px solid #2196f3;border-radius:10px;padding:12px;font-size:13px;font-weight:700;color:#1565c0">
        📦 Recogerás tu pedido en la oficina de <b>Interrapidísimo</b> más cercana a tu ciudad. Te enviaremos el número de guía por WhatsApp.
      </div>
    </div>
    <div class="form-group">
      <label>Teléfono / Celular <span class="req">*</span></label>
      <input type="tel" id="f-telefono" placeholder="Ej: 3001234567">
    </div>
    <div class="form-group">
      <label>Nota <span style="color:#888;font-size:12px;font-weight:400">(opcional — talla, color, instrucciones...)</span></label>
      <textarea id="f-nota" placeholder="Ej: Talla M, color azul, tocar el timbre del segundo piso..." rows="3" style="width:100%;padding:11px 14px;border:2px solid #e5e5e5;border-radius:10px;font-size:14px;font-family:Nunito,sans-serif;resize:vertical"></textarea>
    </div>
    <div style="background:#f0fff4;border:1px solid #00b050;border-radius:12px;padding:12px;margin-bottom:14px;font-size:13px;font-weight:700;color:#00b050;display:flex;align-items:center;gap:8px">
      💵 Pago 100% Contra Entrega — pagas cuando recibes tu pedido
    </div>
    <button class="btn-confirm" onclick="confirmOrder()">✅ Confirmar Pedido por WhatsApp</button>
    <button class="btn-cancel" onclick="closeOrderForm()">✕ Cancelar</button>
  </div>
</div>

<!-- CART DRAWER -->
<div class="cart-drawer" id="cart-drawer">
  <div class="cart-drawer-title">
    🛒 Mi Carrito
    <button onclick="toggleCart()" style="background:none;border:none;font-size:22px;cursor:pointer">✕</button>
  </div>
  <div id="cart-items-list"></div>
  <div class="cart-total" id="cart-total"></div>
  <button class="btn-checkout" onclick="checkoutCart()" id="btn-checkout" style="display:none">Pedir por WhatsApp 💬</button>
</div>

<!-- FOOTER -->
<footer>
  <div class="footer-grid">
    <div class="footer-col">
      <div class="footer-logo">TROGÜI</div>
      <p>Tienda colombiana de confianza. Enviamos a todo el país con las mejores transportadoras.</p>
      <div style="display:flex;gap:10px;margin-top:12px">
        <a href="https://wa.link/lhneng" target="_blank" style="color:#25D366;font-size:22px">💬</a>
        <a href="https://www.instagram.com/store_trog?igsh=MWZleXFlY21weDhnMQ%3D%3D&utm_source=qr" target="_blank" style="font-size:22px">📸</a>
        <a href="https://www.tiktok.com/@trogui_store?_r=1&_t=ZS-96QXU6BiNk2" target="_blank" style="color:#fff;font-size:22px">🎵</a>
      </div>
    </div>
    <div class="footer-col">
      <h4>Información</h4>
      <ul>
        <li>📞 Línea: 320 657 2598</li>
        <li>📧 trogui.store@gmail.com</li>
        <li>🇨🇴 Colombia - Nacional</li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Transportadoras</h4>
      <ul>
        <li>📦 Interrapidísimo</li>
        <li>📦 Coordinadora</li>
        <li>📦 Envia</li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Métodos de Pago</h4>
      <ul>
        <li>💵 Contra Entrega</li>
        <li>🏦 Transferencia</li>
        <li>💳 Nequi / Daviplata</li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">© 2025 TROGÜI · Tienda Colombiana de Confianza 🇨🇴</div>
</footer>

<!-- WHATSAPP FLOAT -->
<a href="https://wa.link/lhneng" target="_blank" class="wa-float" title="WhatsApp">💬</a>

<!-- ADMIN BUTTONS -->
<div class="admin-btns">
  <button class="admin-btn r-btn" title="Editar Productos" onclick="adminAuth('r')">R</button>
  <button class="admin-btn c-btn" title="Ver Pedidos" onclick="adminAuth('c')">C</button>
  <button class="admin-btn e-btn" title="Editar Página" onclick="adminAuth('e')">E</button>
</div>

<!-- ADMIN PANEL R - PRODUCTOS -->
<div class="admin-overlay" id="admin-r">
  <div class="admin-panel">
    <h2>✏️ Editor de Productos</h2>
    <div class="visitors-badge">
      <span class="visitors-dot"></span>
      <span id="visitors-count">0</span> personas viendo la página ahora
    </div>
    <button class="btn-add-prod" onclick="addNewProduct()">+ Agregar Nuevo Producto</button>
    <div class="admin-product-list" id="admin-product-list"></div>
    <div style="display:flex;gap:10px;margin-top:20px">
      <button class="btn-save-admin" onclick="saveProducts()">💾 Guardar Cambios</button>
      <button onclick="closeAdmin('admin-r')" style="background:#eee;border:none;padding:10px 20px;border-radius:10px;cursor:pointer;font-weight:700">Cerrar</button>
    </div>
  </div>
</div>

<!-- ADMIN PANEL C - PEDIDOS -->
<div class="admin-overlay" id="admin-c">
  <div class="admin-panel">
    <h2>📦 Pedidos Recibidos</h2>
    <div class="visitors-badge">
      <span class="visitors-dot"></span>
      <span id="visitors-count2">0</span> personas viendo la página ahora
    </div>
    <div class="admin-orders" id="admin-orders-list"></div>
    <div style="margin-top:20px">
      <button onclick="closeAdmin('admin-c')" style="background:#eee;border:none;padding:10px 20px;border-radius:10px;cursor:pointer;font-weight:700">Cerrar</button>
      <button onclick="clearOrders()" style="background:var(--red);color:#fff;border:none;padding:10px 20px;border-radius:10px;cursor:pointer;font-weight:700;margin-left:10px">Limpiar Pedidos</button>
    </div>
  </div>
</div>

<!-- ADMIN PANEL E - PÁGINA -->
<div class="admin-overlay" id="admin-e">
  <div class="admin-panel">
    <h2>🎨 Editor de Página</h2>
    <div class="page-editor-section">
      <div class="page-editor-group">
        <label>🔊 Audio de Bienvenida (URL o link directo de MP3)</label>
        <input type="text" id="audio-url-input" placeholder="https://... .mp3 o URL de audio">
        <button class="btn-save-admin" onclick="setAudio()" style="margin-top:8px">Establecer Audio</button>
      </div>
      <div class="page-editor-group">
        <label>🏷️ Texto del TopBar</label>
        <input type="text" id="edit-topbar" placeholder="Texto del top bar">
        <button class="btn-save-admin" onclick="savePageSetting('topbar')" style="margin-top:8px">Guardar</button>
      </div>
      <div class="page-editor-group">
        <label>📝 Título Sección Productos</label>
        <input type="text" id="edit-prod-title" placeholder="Título de sección">
        <button class="btn-save-admin" onclick="savePageSetting('prod-title')" style="margin-top:8px">Guardar</button>
      </div>
      <div class="page-editor-group">
        <label>⭐ Editar Reseñas</label>
        <div id="admin-reviews-list"></div>
        <button class="btn-save-admin" onclick="saveReviews()">💾 Guardar Reseñas</button>
      </div>
    </div>
    <div style="margin-top:20px">
      <button onclick="closeAdmin('admin-e')" style="background:#eee;border:none;padding:10px 20px;border-radius:10px;cursor:pointer;font-weight:700">Cerrar</button>
    </div>
  </div>
</div>

<script>
// ===================== DATA =====================
const ADMIN_PASS = '4325';

let products = JSON.parse(localStorage.getItem('trogui_products') || 'null') || [
  {id:'P001',name:'Quita Callos Profesional',cat:'belleza',img:'https://images.unsplash.com/photo-1556228578-8c89e6adf883?w=400',img2:'https://images.unsplash.com/photo-1607462109225-6b64ae2dd3cb?w=400',price:49000,oldPrice:89000,desc:'Elimina callos y durezas de forma rápida y segura. Resultado desde la primera aplicación. Incluye lima especial.',sold:120,stars:5,lastUnits:true,timer:30*60,cat:'belleza'},
  {id:'P002',name:'Masajeador Eléctrico Cervical',cat:'salud',img:'https://images.unsplash.com/photo-1544367567-0f2fcb009e0b?w=400',img2:'https://images.unsplash.com/photo-1585559609834-b89c95c17c72?w=400',price:79000,oldPrice:130000,desc:'Alivio inmediato del dolor de cuello y espalda. 8 modos de masaje. Calor infrarrojo. Recargable USB.',sold:300,stars:5,lastUnits:false,timer:2*60*60,cat:'salud'},
  {id:'P003',name:'Plancha de Cabello Profesional',cat:'belleza',img:'https://images.unsplash.com/photo-1522337360788-8b13dee7a37e?w=400',img2:'https://images.unsplash.com/photo-1527799820374-87ae27d38c85?w=400',price:89000,oldPrice:160000,desc:'Plancha cerámica profesional con control de temperatura. Alisado perfecto sin dañar el cabello.',sold:80,stars:4,lastUnits:true,timer:60*60,cat:'belleza'},
  {id:'P004',name:'Rodillo Facial Jade Anti-Edad',cat:'belleza',img:'https://images.unsplash.com/photo-1616394584738-fc6e612e71b9?w=400',img2:'https://images.unsplash.com/photo-1570172619644-dfd03ed5d881?w=400',price:44000,oldPrice:75000,desc:'Reduce bolsas, ojeras y arrugas. Mejora la circulación facial. Piedra de jade natural.',sold:210,stars:5,lastUnits:false,timer:45*60,cat:'belleza'},
  {id:'P005',name:'Organizador Cocina Giratorio',cat:'hogar',img:'https://images.unsplash.com/photo-1556909114-f6e7ad7d3136?w=400',img2:'https://images.unsplash.com/photo-1556909190-eccf4a8bf97a?w=400',price:54000,oldPrice:90000,desc:'Organizador 360° para especias, salsas y condimentos. Ahorra espacio. Fácil limpieza.',sold:175,stars:5,lastUnits:false,timer:24*60*60,cat:'hogar'},
  {id:'P006',name:'Lámpara LED Solar Jardín',cat:'hogar',img:'https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=400',img2:'https://images.unsplash.com/photo-1513694203232-719a280e022f?w=400',price:49000,oldPrice:85000,desc:'Pack x4 lámparas solares. Enciende automáticamente al oscurecer. Resistente al agua. Sin cables.',sold:90,stars:4,lastUnits:true,timer:3*60*60,cat:'hogar'},
  {id:'P007',name:'Banda Resistencia Fitness',cat:'fitness',img:'https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?w=400',img2:'https://images.unsplash.com/photo-1540497077202-7c8a3999166f?w=400',price:39000,oldPrice:70000,desc:'Set de 5 bandas elásticas. Ideal para glúteos, piernas y brazos. Material premium antirasgado.',sold:400,stars:5,lastUnits:false,timer:2*60*60,cat:'fitness'},
  {id:'P008',name:'Smartwatch Deportivo',cat:'tecnologia',img:'https://images.unsplash.com/photo-1523275335684-37898b6baf30?w=400',img2:'https://images.unsplash.com/photo-1508685096489-7aacd43bd3b1?w=400',price:119000,oldPrice:199000,desc:'Monitor cardíaco, GPS, 20+ modos deporte. Batería 7 días. Compatible Android/iPhone.',sold:150,stars:5,lastUnits:true,timer:60*60,cat:'tecnologia'},
  {id:'P009',name:'Audífonos Bluetooth Inalámbricos',cat:'tecnologia',img:'https://images.unsplash.com/photo-1505740420928-5e560c06d30e?w=400',img2:'https://images.unsplash.com/photo-1484704849700-f032a568e944?w=400',price:84000,oldPrice:149000,desc:'Sonido HD. Cancelación de ruido activa. Batería 40 horas. Carga rápida 15 min.',sold:320,stars:5,lastUnits:false,timer:6*60*60,cat:'tecnologia'},
  {id:'P010',name:'Cepillo Eléctrico Ultrasónico',cat:'salud',img:'https://images.unsplash.com/photo-1559304787-1a0c9c1a2c2e?w=400',img2:'https://images.unsplash.com/photo-1607613009820-a29f7bb81c04?w=400',price:69000,oldPrice:110000,desc:'40,000 vibraciones por minuto. 3 modos de limpieza. Cabezal de repuesto incluido. Batería 30 días.',sold:88,stars:4,lastUnits:false,timer:30*60,cat:'salud'},
  {id:'P011',name:'Juego Yoga Mat Antideslizante',cat:'fitness',img:'https://images.unsplash.com/photo-1544367567-0f2fcb009e0b?w=400',img2:'https://images.unsplash.com/photo-1517963879433-6ad2b056d712?w=400',price:74000,oldPrice:120000,desc:'Mat 6mm ultra grip. Incluye bolsa de transporte y banda. 183x61cm. Ecológico TPE.',sold:60,stars:5,lastUnits:true,timer:4*60*60,cat:'fitness'},
  {id:'P012',name:'Vaporizador Facial Portátil',cat:'belleza',img:'https://images.unsplash.com/photo-1596755094514-f87e34085b2c?w=400',img2:'https://images.unsplash.com/photo-1522337913716-6a5aa24e2c3c?w=400',price:59000,oldPrice:95000,desc:'Hidratación profunda, abre poros, limpieza facial. Nano vapor frío. Uso en casa o viaje.',sold:140,stars:5,lastUnits:false,timer:2*60*60,cat:'belleza'},
  {id:'P013',name:'Organizador Cables USB',cat:'hogar',img:'https://images.unsplash.com/photo-1558618047-f4f89e5e1e7b?w=400',img2:'https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=400',price:34000,oldPrice:60000,desc:'Pack x10 organizadores de cables. Adhesivo fuerte. Ideal escritorio, televisor, consola.',sold:500,stars:5,lastUnits:false,timer:30*60,cat:'hogar'},
  {id:'P014',name:'Crema Reductora Anticelulítica',cat:'belleza',img:'https://images.unsplash.com/photo-1587293852726-70cdb56c2866?w=400',img2:'https://images.unsplash.com/photo-1556228578-8c89e6adf883?w=400',price:64000,oldPrice:105000,desc:'Reduce medidas y celulitis. Con cafeína, retinol y aloe vera. Resultados en 30 días.',sold:230,stars:4,lastUnits:true,timer:60*60,cat:'belleza'},
  {id:'P015',name:'Mini Ventilador USB de Escritorio',cat:'hogar',img:'https://images.unsplash.com/photo-1589275862052-c5b5bb9c7a93?w=400',img2:'https://images.unsplash.com/photo-1557804506-669a67965ba0?w=400',price:44000,oldPrice:75000,desc:'3 velocidades silencioso. Rotación 360°. Conexión USB o banco de energía. Ideal oficina.',sold:190,stars:5,lastUnits:false,timer:45*60,cat:'hogar'},
  {id:'P016',name:'Cargador Inalámbrico 15W',cat:'tecnologia',img:'https://images.unsplash.com/photo-1586953208448-b95a79798f07?w=400',img2:'https://images.unsplash.com/photo-1612815153805-37df13efa28e?w=400',price:49000,oldPrice:89000,desc:'Carga rápida compatible con iPhone y Android. Diseño ultrafino. LED indicador.',sold:280,stars:5,lastUnits:false,timer:3*60*60,cat:'tecnologia'},
  {id:'P017',name:'Kit Pesas Mancuernas Ajustables',cat:'fitness',img:'https://images.unsplash.com/photo-1517836357463-d25dfeac3438?w=400',img2:'https://images.unsplash.com/photo-1534438327276-14e5300c3a48?w=400',price:149000,oldPrice:250000,desc:'Set 2kg a 10kg ajustables. Agarre antideslizante. Ideal para ejercicios en casa.',sold:70,stars:5,lastUnits:true,timer:24*60*60,cat:'fitness'},
  {id:'P018',name:'Mascarilla LED Facial',cat:'belleza',img:'https://images.unsplash.com/photo-1570172619644-dfd03ed5d881?w=400',img2:'https://images.unsplash.com/photo-1516975080664-ed2fc6a32937?w=400',price:129000,oldPrice:220000,desc:'7 colores terapia de luz. Anti-acné, anti-arrugas, rejuvenecimiento. Uso profesional en casa.',sold:55,stars:5,lastUnits:true,timer:2*60*60,cat:'belleza'},
  {id:'P019',name:'Termómetro Digital Infrarrojo',cat:'salud',img:'https://images.unsplash.com/photo-1584515933487-779824d29309?w=400',img2:'https://images.unsplash.com/photo-1584515933487-779824d29309?w=400',price:49000,oldPrice:90000,desc:'Sin contacto. Resultado en 1 segundo. Indicador de fiebre. Apto bebés y adultos.',sold:350,stars:5,lastUnits:false,timer:4*60*60,cat:'salud'},
  {id:'P020',name:'Bolsa Térmica Lonchera',cat:'hogar',img:'https://images.unsplash.com/photo-1553361371-9b22f78e8b1d?w=400',img2:'https://images.unsplash.com/photo-1556909114-f6e7ad7d3136?w=400',price:54000,oldPrice:90000,desc:'Mantiene frío o calor 8 horas. Impermeable. Capacidad 8L. Varios colores.',sold:160,stars:4,lastUnits:false,timer:6*60*60,cat:'hogar'},
  {id:'P021',name:'Collar Anti-Pulgas Perro/Gato',cat:'accesorios',img:'https://images.unsplash.com/photo-1587300003388-59208cc962cb?w=400',img2:'https://images.unsplash.com/photo-1546422072-7a5d6e8c2f44?w=400',price:39000,oldPrice:70000,desc:'Protege por 8 meses. Efecto repelente natural. Ajustable. Para mascotas hasta 50kg.',sold:420,stars:5,lastUnits:false,timer:30*60,cat:'accesorios'},
  {id:'P022',name:'Faja Reductora Cintura',cat:'fitness',img:'https://images.unsplash.com/photo-1576013551627-0cc20b96c2a7?w=400',img2:'https://images.unsplash.com/photo-1518611012118-696072aa579a?w=400',price:59000,oldPrice:100000,desc:'Reduce cintura, control postural. Neopreno de alta compresión. Tallas S-XXXL.',sold:310,stars:4,lastUnits:true,timer:60*60,cat:'fitness'},
  {id:'P023',name:'Silla Gaming Ergonómica',cat:'hogar',img:'https://images.unsplash.com/photo-1586023492125-27b2c045efd7?w=400',img2:'https://images.unsplash.com/photo-1555041469-a586c61ea9bc?w=400',price:349000,oldPrice:580000,desc:'Espaldar reclinable 180°. Descansabrazos ajustables. Cojín lumbar y cervical.',sold:45,stars:5,lastUnits:true,timer:24*60*60,cat:'hogar'},
  {id:'P024',name:'Set Pincel Maquillaje 15pcs',cat:'belleza',img:'https://images.unsplash.com/photo-1522337913716-6a5aa24e2c3c?w=400',img2:'https://images.unsplash.com/photo-1503236823255-94609f598e71?w=400',price:44000,oldPrice:79000,desc:'Cerdas sintéticas ultra suaves. Incluye estuche. Aptos para polvo, líquido y crema.',sold:260,stars:5,lastUnits:false,timer:45*60,cat:'belleza'},
  {id:'P025',name:'Purificador Aire USB',cat:'hogar',img:'https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=400',img2:'https://images.unsplash.com/photo-1555041469-a586c61ea9bc?w=400',price:74000,oldPrice:130000,desc:'Filtro HEPA. Elimina polvo, alérgenos y bacterias. Silencioso. Para habitaciones hasta 20m².',sold:100,stars:4,lastUnits:false,timer:3*60*60,cat:'hogar'},
  {id:'P026',name:'Pastillero Semanal Electrónico',cat:'salud',img:'https://images.unsplash.com/photo-1584515933487-779824d29309?w=400',img2:'https://images.unsplash.com/photo-1631549916768-4119b2e5f926?w=400',price:54000,oldPrice:90000,desc:'Alarma para recordar tus medicamentos. 7 compartimentos. Pantalla LCD. Portátil.',sold:75,stars:5,lastUnits:false,timer:2*60*60,cat:'salud'},
  {id:'P027',name:'Cuerda para Saltar Profesional',cat:'fitness',img:'https://images.unsplash.com/photo-1571019614242-c5c5dee9f50b?w=400',img2:'https://images.unsplash.com/photo-1534438327276-14e5300c3a48?w=400',price:34000,oldPrice:60000,desc:'Ajustable. Mango ergonómico con contador de saltos y calorías. Acero recubierto.',sold:380,stars:5,lastUnits:false,timer:30*60,cat:'fitness'},
  {id:'P028',name:'Mascarilla Puntos Negros',cat:'belleza',img:'https://images.unsplash.com/photo-1587293852726-70cdb56c2866?w=400',img2:'https://images.unsplash.com/photo-1556228578-8c89e6adf883?w=400',price:39000,oldPrice:69000,desc:'Peel-off de carbón activo. Elimina puntos negros, impurezas y poros dilatados en 20 min.',sold:190,stars:4,lastUnits:true,timer:45*60,cat:'belleza'},
  {id:'P029',name:'Luz LED RGB Escritorio',cat:'tecnologia',img:'https://images.unsplash.com/photo-1593640408182-31c70c8268f5?w=400',img2:'https://images.unsplash.com/photo-1587202372775-e229f172b9d7?w=400',price:59000,oldPrice:100000,desc:'16 millones de colores. Control por app. Ideal gaming, streaming y estudiar.',sold:215,stars:5,lastUnits:false,timer:6*60*60,cat:'tecnologia'},
  {id:'P030',name:'Soporte Celular Auto Magnético',cat:'accesorios',img:'https://images.unsplash.com/photo-1586953208448-b95a79798f07?w=400',img2:'https://images.unsplash.com/photo-1612815153805-37df13efa28e?w=400',price:34000,oldPrice:60000,desc:'Imán potente 360°. Ajuste por rejilla o parabrisas. Compatible todos los celulares.',sold:550,stars:5,lastUnits:false,timer:30*60,cat:'accesorios'},
  {id:'P031',name:'Almohada Ortopédica Cervical',cat:'hogar',img:'https://images.unsplash.com/photo-1555041469-a586c61ea9bc?w=400',img2:'https://images.unsplash.com/photo-1559494007-9f5847c49d94?w=400',price:89000,oldPrice:149000,desc:'Espuma viscoelástica. Alivia dolor de cuello y mejora postura al dormir. Funda lavable.',sold:130,stars:5,lastUnits:true,timer:60*60,cat:'hogar'},
  {id:'P032',name:'Depiladora Eléctrica Facial',cat:'belleza',img:'https://images.unsplash.com/photo-1522337913716-6a5aa24e2c3c?w=400',img2:'https://images.unsplash.com/photo-1516975080664-ed2fc6a32937?w=400',price:49000,oldPrice:85000,desc:'Elimina el vello no deseado de raíz. Sin dolor. Recargable USB. Para dama.',sold:290,stars:5,lastUnits:false,timer:45*60,cat:'belleza'},
  {id:'P033',name:'Bolígrafo Espía HD 1080p',cat:'tecnologia',img:'https://images.unsplash.com/photo-1586953208448-b95a79798f07?w=400',img2:'https://images.unsplash.com/photo-1612815153805-37df13efa28e?w=400',price:74000,oldPrice:125000,desc:'Cámara oculta en bolígrafo. Graba video Full HD. Detección de movimiento. 32GB.',sold:85,stars:4,lastUnits:true,timer:2*60*60,cat:'tecnologia'},
  {id:'P034',name:'Guantes Box Entrenamiento',cat:'fitness',img:'https://images.unsplash.com/photo-1538805060514-97d9cc17730c?w=400',img2:'https://images.unsplash.com/photo-1517836357463-d25dfeac3438?w=400',price:79000,oldPrice:140000,desc:'Cuero sintético PU. Relleno gel. Tallas S-XL. Para saco, sparring y entrenamiento.',sold:65,stars:5,lastUnits:false,timer:24*60*60,cat:'fitness'},
  {id:'P035',name:'Mochila USB Antirrobo',cat:'accesorios',img:'https://images.unsplash.com/photo-1553361371-9b22f78e8b1d?w=400',img2:'https://images.unsplash.com/photo-1573100925118-870b8efc799d?w=400',price:119000,oldPrice:200000,desc:'Puerto USB integrado, cerradura oculta. Impermeable. Capacidad 30L. Para laptop 15.6".',sold:170,stars:5,lastUnits:true,timer:3*60*60,cat:'accesorios'},
  {id:'P036',name:'Secadora de Uñas UV/LED',cat:'belleza',img:'https://images.unsplash.com/photo-1503236823255-94609f598e71?w=400',img2:'https://images.unsplash.com/photo-1522337913716-6a5aa24e2c3c?w=400',price:64000,oldPrice:110000,desc:'36W. Seca gel en 30 segundos. Timer automático. Temporizador. Para manos y pies.',sold:200,stars:5,lastUnits:false,timer:45*60,cat:'belleza'},
  {id:'P037',name:'Tensiometro Digital Brazo',cat:'salud',img:'https://images.unsplash.com/photo-1584515933487-779824d29309?w=400',img2:'https://images.unsplash.com/photo-1631549916768-4119b2e5f926?w=400',price:89000,oldPrice:149000,desc:'Medición precisa ±2mmHg. Detecta arritmias. Memoria 60 mediciones. Pantalla grande.',sold:95,stars:5,lastUnits:false,timer:6*60*60,cat:'salud'},
  {id:'P038',name:'Taza Calentadora USB Inteligente',cat:'hogar',img:'https://images.unsplash.com/photo-1510972527921-ce03766a1cf1?w=400',img2:'https://images.unsplash.com/photo-1556909114-f6e7ad7d3136?w=400',price:54000,oldPrice:89000,desc:'Mantiene tu bebida a 55°C. Base calentadora inteligente. Control de temperatura.',sold:240,stars:5,lastUnits:false,timer:30*60,cat:'hogar'},
  {id:'P039',name:'Tapete Acupuntura Spa',cat:'salud',img:'https://images.unsplash.com/photo-1544367567-0f2fcb009e0b?w=400',img2:'https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?w=400',price:69000,oldPrice:120000,desc:'6,210 puntos de acupuntura. Reduce estrés, dolor muscular. Incluye almohada.',sold:145,stars:4,lastUnits:true,timer:2*60*60,cat:'salud'},
  {id:'P040',name:'Sombra de Ojos 18 Tonos',cat:'belleza',img:'https://images.unsplash.com/photo-1503236823255-94609f598e71?w=400',img2:'https://images.unsplash.com/photo-1522337913716-6a5aa24e2c3c?w=400',price:44000,oldPrice:79000,desc:'Paleta pigmentada mate y brillante. Larga duración 24h. Sin grumos.',sold:310,stars:5,lastUnits:false,timer:60*60,cat:'belleza'},
  {id:'P041',name:'Altavoz Bluetooth Resistente Agua',cat:'tecnologia',img:'https://images.unsplash.com/photo-1608043152269-423dbba4e7e1?w=400',img2:'https://images.unsplash.com/photo-1606220945770-b5b6c2c55bf1?w=400',price:99000,oldPrice:169000,desc:'IPX7 sumergible. 360° sonido. Batería 20h. Ideal ducha, piscina, camping.',sold:195,stars:5,lastUnits:true,timer:3*60*60,cat:'tecnologia'},
  {id:'P042',name:'Kit Herramientas Reparación Celular',cat:'tecnologia',img:'https://images.unsplash.com/photo-1586953208448-b95a79798f07?w=400',img2:'https://images.unsplash.com/photo-1612815153805-37df13efa28e?w=400',price:39000,oldPrice:70000,desc:'25 piezas. Abre pantallas, destornilladores de precisión, palancas, pinzas.',sold:115,stars:4,lastUnits:false,timer:4*60*60,cat:'tecnologia'},
  {id:'P043',name:'Aceite Esencial Relajante',cat:'salud',img:'https://images.unsplash.com/photo-1544161515-4ab6ce6db874?w=400',img2:'https://images.unsplash.com/photo-1580618672591-eb180b1a973f?w=400',price:44000,oldPrice:75000,desc:'100% natural. Lavanda, eucalipto y menta. Difusor, masajes o baño relajante.',sold:280,stars:5,lastUnits:false,timer:45*60,cat:'salud'},
  {id:'P044',name:'Plantillas Ortopédicas',cat:'salud',img:'https://images.unsplash.com/photo-1542291026-7eec264c27ff?w=400',img2:'https://images.unsplash.com/photo-1542291026-7eec264c27ff?w=400',price:49000,oldPrice:85000,desc:'Corrección de pisada plana. Gel silicona. Alivio fascitis plantar. Tallas 35-45.',sold:165,stars:5,lastUnits:false,timer:6*60*60,cat:'salud'},
  {id:'P045',name:'Collar GPS para Mascotas',cat:'accesorios',img:'https://images.unsplash.com/photo-1587300003388-59208cc962cb?w=400',img2:'https://images.unsplash.com/photo-1546422072-7a5d6e8c2f44?w=400',price:119000,oldPrice:199000,desc:'Rastreo tiempo real por app. Alerta zona segura. Resistente al agua. Batería 7 días.',sold:55,stars:4,lastUnits:true,timer:24*60*60,cat:'accesorios'},
];

let reviews = JSON.parse(localStorage.getItem('trogui_reviews') || 'null') || [
  {name:'Valentina Torres',city:'Bogotá',stars:5,text:'Me llegó super rápido, en 4 días! El producto está 10/10, lo recomiendo 😍'},
  {name:'Juan Camilo Restrepo',city:'Medellín',stars:5,text:'Pagé contra entrega y todo bien. La calidad es buenísima, gracias trogui!'},
  {name:'Luisa Fernanda Gómez',city:'Cali',stars:4,text:'lindo producto aunq la entrega demoro un poco pero llegó bien, lo recomiendo'},
  {name:'Andrés Felipe Ospina',city:'Bucaramanga',stars:5,text:'Segunda vez que compro aquí y siempre quedo satisfecho. 100% confiable'},
  {name:'Natalia Suárez',city:'Barranquilla',stars:5,text:'Excelente! El quita callos me funcionó de maravilla desde el primer uso jajaja'},
];

let cart = [];
let orders = JSON.parse(localStorage.getItem('trogui_orders') || '[]');
let currentOrderProduct = null;
let timers = {};
let sliderIndex = 0;
let sliderAutoInterval;
let visitors = Math.floor(Math.random()*40)+15;

// ===================== INIT =====================
document.addEventListener('DOMContentLoaded', ()=>{
  renderProducts(products);
  startSlider();
  startNotifications();
  updateVisitors();
  loadPageSettings();
  startVisitorCount();
});

function loadPageSettings(){
  const tb = localStorage.getItem('trogui_topbar');
  if(tb) document.querySelector('.topbar').innerHTML = tb;
  const pt = localStorage.getItem('trogui_prod_title');
  if(pt) document.querySelector('.section-title').innerHTML = pt;
  const au = localStorage.getItem('trogui_audio');
  if(au){ document.getElementById('audio-src').src=au; document.getElementById('audio-autoplay').load(); }
}

// ===================== SLIDER =====================
function moveSlider(dir){
  sliderIndex=(sliderIndex+dir+3)%3;
  updateSlider();
}
function goSlide(i){sliderIndex=i;updateSlider();}
function updateSlider(){
  document.getElementById('slider-track').style.transform=`translateX(-${sliderIndex*100}%)`;
  document.querySelectorAll('.dot').forEach((d,i)=>d.classList.toggle('active',i===sliderIndex));
}
function startSlider(){
  sliderAutoInterval=setInterval(()=>moveSlider(1),6000);
}

// ===================== PRODUCTS =====================
function fmt(n){return n.toLocaleString('es-CO');}

function renderProducts(prods){
  const grid=document.getElementById('products-grid');
  grid.innerHTML='';
  prods.forEach(p=>{
    const disc=Math.round((1-p.price/p.oldPrice)*100);
    const el=document.createElement('div');
    el.className='product-card';
    el.id='card-'+p.id;
    el.onclick=()=>openModal(p.id);
    el.innerHTML=`
      <div class="product-img-wrap">
        <img src="${p.img}" alt="${p.name}" onerror="this.src='https://via.placeholder.com/400x300?text=TROGUI'">
        <div class="badge-offer">-${disc}% OFF</div>
        <div class="badge-sold">✅ ${p.sold}+ vendidos</div>
        ${p.lastUnits?'<div class="badge-last">⚠️ Últimas unidades</div>':''}
      </div>
      <div class="product-info">
        <div class="product-name">${p.name}</div>
        <div class="stars">${'⭐'.repeat(p.stars)}<span>(${p.stars}.0)</span></div>
        <div class="price-wrap">
          <span class="price-old">$${fmt(p.oldPrice)}</span>
          <span class="price-new">$${fmt(p.price)}</span>
        </div>
        <div class="timer-badge" id="timer-${p.id}">⏰ Cargando...</div>
        <div class="free-ship">🚚 Envío GRATIS a toda Colombia</div>
        <div class="delivery-info">💵 Pago contra entrega disponible</div>
        <button class="btn-add" onclick="event.stopPropagation();addToCart('${p.id}')">🛒 Agregar al Carrito</button>
      </div>`;
    grid.appendChild(el);
    startTimer(p.id,p.timer);
  });
}

function filterCat(cat,el){
  document.querySelectorAll('.nav-inner a').forEach(a=>a.classList.remove('active'));
  el.classList.add('active');
  const filtered=cat==='all'?products:products.filter(p=>p.cat===cat);
  renderProducts(filtered);
}

// ===================== TIMER =====================
function startTimer(id,seconds){
  if(timers[id]) clearInterval(timers[id]);
  let remaining=seconds;
  function update(){
    const el=document.getElementById('timer-'+id);
    if(!el) return;
    if(remaining<=0){el.innerHTML='⚡ ¡Oferta vigente!';return;}
    const h=Math.floor(remaining/3600);
    const m=Math.floor((remaining%3600)/60);
    const s=remaining%60;
    let label=h>0?`${h}h ${m}m ${s}s`:m>0?`${m}m ${s}s`:`${s}s`;
    el.innerHTML=`⏰ Oferta acaba en: <b>${label}</b>`;
    remaining--;
  }
  update();
  timers[id]=setInterval(update,1000);
}

// ===================== MODAL =====================
function openModal(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  const disc=Math.round((1-p.price/p.oldPrice)*100);
  const revHtml=reviews.map(r=>`
    <div class="review-item">
      <div class="review-top">
        <div class="review-avatar">${r.name[0]}</div>
        <div><div class="review-name">${r.name} - ${r.city}</div><div class="review-stars">${'⭐'.repeat(r.stars)}</div></div>
      </div>
      <div class="review-text">${r.text}</div>
    </div>`).join('');
  document.getElementById('modal-content').innerHTML=`
    <div class="modal-imgs">
      <img src="${p.img}" alt="${p.name}" onerror="this.src='https://via.placeholder.com/400x300?text=TROGUI'">
      <img src="${p.img2||p.img}" alt="${p.name}" onerror="this.src='https://via.placeholder.com/400x300?text=TROGUI'">
    </div>
    <div class="product-name" style="font-size:11px;color:var(--gray);margin-bottom:4px">ID: ${p.id}</div>
    <div class="modal-title">${p.name}</div>
    <div class="stars">${'⭐'.repeat(p.stars)} <span style="color:var(--gray);font-size:13px">${p.stars}.0 (${p.sold}+ vendidos)</span></div>
    <div class="modal-price-wrap">
      <span class="modal-price-old">$${fmt(p.oldPrice)}</span>
      <span class="modal-price-new">$${fmt(p.price)}</span>
      <span style="background:#ffe0cc;color:var(--orange);font-weight:800;padding:4px 10px;border-radius:20px;font-size:13px">-${disc}%</span>
    </div>
    <div class="modal-delivery">
      🚚 <strong>Envío GRATIS</strong> a toda Colombia · Entrega en <strong>3 a 7 días hábiles</strong><br>
      💵 <strong>Pago Contra Entrega</strong> disponible · Interrapidísimo · Coordinadora · Envia
    </div>
    <div class="modal-desc">${p.desc}</div>
    ${p.lastUnits?'<div style="background:#fff0f0;border:1px solid var(--red);border-radius:10px;padding:10px;font-size:13px;font-weight:800;color:var(--red)">⚠️ ¡ÚLTIMAS UNIDADES! Stock limitado</div>':''}
    <button class="btn-order" onclick="openOrderForm('${p.id}')">🛒 ¡Pedir Ahora - Pago Contra Entrega!</button>
    <h3 style="margin:20px 0 12px;font-family:'Poppins',sans-serif">⭐ Reseñas de Clientes</h3>
    <div class="review-list">${revHtml}</div>`;
  document.getElementById('product-modal').classList.add('active');
}
function closeModal(){document.getElementById('product-modal').classList.remove('active');}

// ===================== ORDER FORM =====================
function openOrderForm(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  currentOrderProduct=p;
  closeModal();
  document.getElementById('form-prod-name').textContent=p.name+' (ID: '+p.id+')';
  document.getElementById('form-price-show').innerHTML=`
    <div><div style="font-size:13px;color:var(--gray);font-weight:700">Precio anterior:</div><div class="fold">$${fmt(p.oldPrice)}</div></div>
    <div style="text-align:right"><div style="font-size:13px;font-weight:700;color:var(--gray)">Pagas hoy:</div><div class="fprice">$${fmt(p.price)}</div></div>`;
  document.getElementById('order-form-section').classList.add('active');
}
function closeOrderForm(){document.getElementById('order-form-section').classList.remove('active');}

function toggleEntrega(){
  const val=document.querySelector('input[name="entrega"]:checked').value;
  document.getElementById('grp-direccion').style.display=val==='domicilio'?'block':'none';
  document.getElementById('grp-oficina').style.display=val==='oficina'?'block':'none';
  // Highlight selected
  document.getElementById('lbl-domicilio').style.border=val==='domicilio'?'2px solid #FF5200':'2px solid #e5e5e5';
  document.getElementById('lbl-oficina').style.border=val==='oficina'?'2px solid #FF5200':'2px solid #e5e5e5';
}

function confirmOrder(){
  const nombre   = document.getElementById('f-nombre').value.trim();
  const apellido = document.getElementById('f-apellido').value.trim();
  const depto    = document.getElementById('f-depto').value.trim();
  const ciudad   = document.getElementById('f-ciudad').value.trim();
  const telefono = document.getElementById('f-telefono').value.trim();
  const nota     = document.getElementById('f-nota').value.trim();
  const tipoEntrega = document.querySelector('input[name="entrega"]:checked').value;
  const direccion = tipoEntrega==='domicilio'
    ? document.getElementById('f-direccion').value.trim()
    : 'RECOGER EN OFICINA INTERRAPIDÍSIMO';

  if(!nombre){alert('Por favor escribe tu nombre.');return;}
  if(!apellido){alert('Por favor escribe tu apellido.');return;}
  if(!depto){alert('Por favor selecciona tu departamento.');return;}
  if(!ciudad){alert('Por favor escribe tu ciudad o municipio.');return;}
  if(tipoEntrega==='domicilio'&&!direccion){alert('Por favor escribe tu dirección de entrega.');return;}
  if(!telefono){alert('Por favor escribe tu teléfono.');return;}

  const p=currentOrderProduct;
  const ahorro=p.oldPrice-p.price;
  const now=new Date();
  const fechaStr=now.toLocaleString('es-CO',{dateStyle:'full',timeStyle:'short'});
  const llegada=new Date(now); llegada.setDate(llegada.getDate()+5);
  const llegadaStr=llegada.toLocaleDateString('es-CO',{weekday:'long',day:'numeric',month:'long'});

  const order={
    id:'ORD'+Date.now(),
    product:p.name, productId:p.id,
    price:p.price, oldPrice:p.oldPrice, ahorro,
    nombre, apellido, depto, ciudad,
    tipoEntrega, direccion, telefono, nota,
    fecha: fechaStr,
    llegadaEst: llegadaStr
  };
  orders.push(order);
  localStorage.setItem('trogui_orders',JSON.stringify(orders));

  const entregaTexto = tipoEntrega==='domicilio'
    ? '🏠 A domicilio: '+direccion
    : '📦 Recoger en oficina Interrapidísimo';

  const msg=encodeURIComponent(
    `🛍️ *NUEVO PEDIDO — TROGÜI* 🇨🇴\n`+
    `━━━━━━━━━━━━━━━━━\n`+
    `📦 *Producto:* ${p.name}\n`+
    `🆔 *ID Producto:* ${p.id}\n`+
    `💰 *Precio:* $${fmt(p.price)}\n`+
    `🏷️ *Precio anterior:* $${fmt(p.oldPrice)}\n`+
    `✂️ *Ahorro:* $${fmt(ahorro)}\n`+
    `━━━━━━━━━━━━━━━━━\n`+
    `👤 *Nombre:* ${nombre} ${apellido}\n`+
    `🗺️ *Departamento:* ${depto}\n`+
    `🏙️ *Ciudad:* ${ciudad}\n`+
    `🚚 *Entrega:* ${entregaTexto}\n`+
    `📞 *Teléfono:* ${telefono}\n`+
    `📝 *Nota:* ${nota||'Sin nota'}\n`+
    `━━━━━━━━━━━━━━━━━\n`+
    `📅 *Pedido:* ${fechaStr}\n`+
    `📆 *Entrega est.:* ${llegadaStr}\n`+
    `💵 *Pago:* Contra Entrega ✅`
  );
  closeOrderForm();
  // clear form
  ['f-nombre','f-apellido','f-ciudad','f-direccion','f-telefono','f-nota'].forEach(id=>{
    const el=document.getElementById(id); if(el) el.value='';
  });
  document.getElementById('f-depto').value='';
  window.open(`https://wa.me/573206572598?text=${msg}`,'_blank');
}

// ===================== CART =====================
function addToCart(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  const existing=cart.find(x=>x.id===id);
  if(existing) existing.qty++;
  else cart.push({...p,qty:1});
  updateCartUI();
  showFloatMsg('✅ '+p.name+' agregado al carrito');
}
function removeFromCart(id){cart=cart.filter(x=>x.id!==id);updateCartUI();}
function updateCartUI(){
  const count=cart.reduce((a,b)=>a+b.qty,0);
  document.getElementById('cart-count').textContent=count;
  const list=document.getElementById('cart-items-list');
  if(cart.length===0){list.innerHTML='<div class="empty-cart">🛒 Tu carrito está vacío</div>';document.getElementById('cart-total').textContent='';document.getElementById('btn-checkout').style.display='none';return;}
  list.innerHTML=cart.map(item=>`
    <div class="cart-item">
      <img src="${item.img}" alt="${item.name}" onerror="this.src='https://via.placeholder.com/70?text=T'">
      <div class="cart-item-info">
        <div class="cart-item-name">${item.name}</div>
        <div class="cart-item-price">$${fmt(item.price)} × ${item.qty}</div>
      </div>
      <button class="cart-item-remove" onclick="removeFromCart('${item.id}')">✕</button>
    </div>`).join('');
  const total=cart.reduce((a,b)=>a+b.price*b.qty,0);
  document.getElementById('cart-total').innerHTML=`Total: <span style="color:var(--orange)">$${fmt(total)}</span>`;
  document.getElementById('btn-checkout').style.display='block';
}
function toggleCart(){document.getElementById('cart-drawer').classList.toggle('open');}
function checkoutCart(){
  if(cart.length===0) return;
  const lines=cart.map(i=>`• ${i.name} x${i.qty} = $${fmt(i.price*i.qty)}`).join('\n');
  const total=cart.reduce((a,b)=>a+b.price*b.qty,0);
  const msg=encodeURIComponent(`🛍️ *PEDIDO CARRITO - TROGÜI*\n\n${lines}\n\n💰 *Total: $${fmt(total)}*\n\nDeseo pagar contra entrega 🙏`);
  window.open(`https://wa.me/573206572598?text=${msg}`,'_blank');
}

// ===================== SEARCH =====================
function levenshtein(a,b){
  const m=a.length,n=b.length,dp=Array.from({length:m+1},(_,i)=>[i,...Array(n).fill(0)]);
  for(let j=0;j<=n;j++) dp[0][j]=j;
  for(let i=1;i<=m;i++) for(let j=1;j<=n;j++) dp[i][j]=a[i-1]===b[j-1]?dp[i-1][j-1]:1+Math.min(dp[i-1][j],dp[i][j-1],dp[i-1][j-1]);
  return dp[m][n];
}
function searchProducts(q){
  const dd=document.getElementById('search-dropdown');
  if(!q||q.length<2){dd.classList.remove('open');renderProducts(products);return;}
  const ql=q.toLowerCase();
  const scored=products.map(p=>{
    const nl=p.name.toLowerCase();
    const exact=nl.includes(ql)?0:1;
    const lev=Math.min(...nl.split(' ').map(w=>levenshtein(ql,w)));
    return{p,score:exact*10+lev};
  }).filter(x=>x.score<6).sort((a,b)=>a.score-b.score).slice(0,8);
  if(scored.length===0){dd.innerHTML='<div style="padding:12px 16px;color:var(--gray);font-size:14px">No se encontraron productos</div>';dd.classList.add('open');return;}
  dd.innerHTML=scored.map(({p})=>`
    <div class="search-dropdown-item" onclick="openModal('${p.id}');document.getElementById('search-dropdown').classList.remove('open')">
      <img src="${p.img}" alt="${p.name}" onerror="this.src='https://via.placeholder.com/36?text=T'">
      <div><div style="font-weight:700;font-size:14px">${p.name}</div><div style="color:var(--orange);font-weight:800;font-size:13px">$${fmt(p.price)}</div></div>
    </div>`).join('');
  dd.classList.add('open');
  renderProducts(scored.map(x=>x.p));
}
document.addEventListener('click',e=>{if(!e.target.closest('.search-bar')) document.getElementById('search-dropdown').classList.remove('open');});

// ===================== DELIVERY CALC =====================
function calcDelivery(){
  const sel=document.getElementById('delivery-city');
  const days=parseInt(sel.value)||5;
  if(!sel.value){alert('Selecciona una ciudad');return;}
  const now=new Date();
  now.setDate(now.getDate()+days);
  const opts={weekday:'long',year:'numeric',month:'long',day:'numeric'};
  const dateStr=now.toLocaleDateString('es-CO',opts);
  const el=document.getElementById('delivery-result');
  el.style.display='block';
  el.innerHTML=`📦 Tu pedido llegaría aproximadamente el <strong>${dateStr}</strong> (entre ${days} y ${days+1} días hábiles). Entrega por Interrapidísimo, Coordinadora o Envia.`;
}

// ===================== NOTIFICATIONS =====================
const notifNames=[
  {name:'Juan Camilo Paz',city:'Medellín'},{name:'Valentina Torres',city:'Bogotá'},
  {name:'Luisa Gómez',city:'Cali'},{name:'Andrés Ospina',city:'Bucaramanga'},
  {name:'Natalia Suárez',city:'Barranquilla'},{name:'Carlos Herrera',city:'Pereira'},
  {name:'María José López',city:'Manizales'},{name:'Felipe Restrepo',city:'Cartagena'},
  {name:'Sofía Martínez',city:'Ibagué'},{name:'Daniel Vargas',city:'Santa Marta'},
];
function startNotifications(){
  let i=0;
  setInterval(()=>{
    const {name,city}=notifNames[i%notifNames.length];
    const p=products[Math.floor(Math.random()*products.length)];
    showNotif(`🛍️ <span class="notif-name">${name}</span> de ${city} hizo un pedido de <b>${p.name}</b>`);
    i++;
  },8000);
}
function showNotif(html){
  const nb=document.getElementById('notif-box');
  nb.innerHTML=html;
  nb.style.display='block';
  setTimeout(()=>nb.style.display='none',4000);
}
function showFloatMsg(msg){
  const div=document.createElement('div');
  div.style.cssText='position:fixed;bottom:150px;left:50%;transform:translateX(-50%);background:var(--dark);color:#fff;padding:10px 20px;border-radius:20px;font-weight:700;font-size:14px;z-index:9999;animation:slideUp .4s';
  div.textContent=msg;
  document.body.appendChild(div);
  setTimeout(()=>div.remove(),2500);
}
function updateVisitors(){
  setInterval(()=>{
    visitors=Math.max(8,visitors+Math.floor(Math.random()*5)-2);
    document.querySelectorAll('#visitors-count,#visitors-count2').forEach(el=>el.textContent=visitors);
  },5000);
}
function startVisitorCount(){
  document.querySelectorAll('#visitors-count,#visitors-count2').forEach(el=>el.textContent=visitors);
}

// ===================== ADMIN AUTH =====================
function adminAuth(panel){
  const pass=prompt('Ingresa la contraseña de administrador:');
  if(pass!==ADMIN_PASS){alert('Contraseña incorrecta');return;}
  if(panel==='r') openAdminR();
  else if(panel==='c') openAdminC();
  else if(panel==='e') openAdminE();
}
function closeAdmin(id){document.getElementById(id).classList.remove('active');}

// ===================== ADMIN R - PRODUCTS =====================
function openAdminR(){
  renderAdminProducts();
  document.getElementById('admin-r').classList.add('active');
}

function mkEl(tag,props,styles,children){
  const el=document.createElement(tag);
  if(props) Object.entries(props).forEach(([k,v])=>{ if(k==='textContent') el.textContent=v; else el.setAttribute(k,v); });
  if(styles) Object.assign(el.style,styles);
  if(children) children.forEach(c=>c&&el.appendChild(c));
  return el;
}
function mkLabel(text,styles){
  const l=document.createElement('label');
  l.textContent=text;
  Object.assign(l.style,{fontWeight:'800',fontSize:'13px',display:'block',marginBottom:'3px',marginTop:'8px',...(styles||{})});
  return l;
}
function mkInput(id,value,type,placeholder){
  const inp=document.createElement('input');
  inp.type=type||'text'; inp.id=id; inp.value=value||'';
  if(placeholder) inp.placeholder=placeholder;
  Object.assign(inp.style,{width:'100%',padding:'8px 10px',border:'1.5px solid #e5e5e5',borderRadius:'8px',fontSize:'13px',fontFamily:'Nunito,sans-serif',boxSizing:'border-box'});
  return inp;
}

function buildImgRow(pid, suffix, currentSrc, label){
  // preview image
  const prevImg = document.createElement('img');
  prevImg.id = 'prev'+suffix+'-'+pid;
  prevImg.src = currentSrc || 'https://via.placeholder.com/80?text=IMG';
  prevImg.alt = 'preview';
  Object.assign(prevImg.style,{width:'80px',height:'80px',objectFit:'cover',borderRadius:'10px',border:'2px solid #e5e5e5',background:'#f4f4f4',flexShrink:'0'});
  prevImg.onerror = function(){ this.src='https://via.placeholder.com/80?text=IMG'; };

  // URL input
  const urlInp = mkInput('ai'+suffix+'-'+pid, currentSrc, 'text', '🔗 Pega URL de imagen (https://...)');
  urlInp.addEventListener('input', function(){
    const v = this.value.trim();
    if(v){ prevImg.src=v; prevImg.onerror=function(){this.src='https://via.placeholder.com/80?text=Error';}; }
  });

  // File upload button
  const fileInp = document.createElement('input');
  fileInp.type='file'; fileInp.accept='image/*';
  fileInp.style.cssText='display:none';
  fileInp.addEventListener('change', function(){
    const file=this.files[0]; if(!file) return;
    const reader=new FileReader();
    reader.onload=function(e){
      const b64=e.target.result;
      urlInp.value=b64;
      prevImg.src=b64;
      showFloatMsg('✅ Imagen cargada. Pulsa Guardar.');
    };
    reader.readAsDataURL(file);
  });
  const fileBtn = document.createElement('label');
  fileBtn.textContent='📁 Subir foto';
  fileBtn.appendChild(fileInp);
  Object.assign(fileBtn.style,{display:'block',background:'#FF5200',color:'#fff',padding:'7px 10px',borderRadius:'8px',cursor:'pointer',fontSize:'12px',fontWeight:'800',textAlign:'center',marginTop:'4px'});

  const col = document.createElement('div');
  Object.assign(col.style,{flex:'1',minWidth:'160px',display:'flex',flexDirection:'column',gap:'4px'});
  col.appendChild(urlInp);
  col.appendChild(fileBtn);

  const row = document.createElement('div');
  Object.assign(row.style,{display:'flex',gap:'10px',alignItems:'flex-start',flexWrap:'wrap',marginBottom:'6px'});
  row.appendChild(prevImg);
  row.appendChild(col);

  const lbl = mkLabel(label, {color:'#FF5200'});
  const wrap = document.createElement('div');
  wrap.appendChild(lbl);
  wrap.appendChild(row);
  return wrap;
}

function buildProductCard(p){
  const card = document.createElement('div');
  card.className='admin-product-item';
  card.id='aitem-'+p.id;

  // Header
  const hdr = document.createElement('div');
  Object.assign(hdr.style,{display:'flex',justifyContent:'space-between',alignItems:'center',marginBottom:'8px'});
  const title = document.createElement('b');
  title.textContent = p.id+' — '+p.name;
  Object.assign(title.style,{fontSize:'13px',color:'#FF5200'});
  const delBtn = document.createElement('button');
  delBtn.textContent='🗑️ Eliminar'; delBtn.className='btn-del-admin';
  delBtn.onclick=()=>deleteProduct(p.id);
  hdr.appendChild(title); hdr.appendChild(delBtn);
  card.appendChild(hdr);

  // Nombre
  card.appendChild(mkLabel('Nombre del producto'));
  card.appendChild(mkInput('an-'+p.id, p.name));

  // Descripción
  card.appendChild(mkLabel('Descripción'));
  const ta = document.createElement('textarea');
  ta.id='ad-'+p.id; ta.rows=2; ta.textContent=p.desc||'';
  Object.assign(ta.style,{width:'100%',padding:'8px 10px',border:'1.5px solid #e5e5e5',borderRadius:'8px',fontSize:'13px',fontFamily:'Nunito,sans-serif',resize:'vertical',boxSizing:'border-box'});
  card.appendChild(ta);

  // Precios
  const r1=document.createElement('div'); r1.className='row2';
  const c1=document.createElement('div'); c1.appendChild(mkLabel('Precio actual ($)')); c1.appendChild(mkInput('ap-'+p.id,p.price,'number')); r1.appendChild(c1);
  const c2=document.createElement('div'); c2.appendChild(mkLabel('Precio anterior ($)')); c2.appendChild(mkInput('ao-'+p.id,p.oldPrice,'number')); r1.appendChild(c2);
  card.appendChild(r1);

  // Vendidos / estrellas
  const r2=document.createElement('div'); r2.className='row2';
  const c3=document.createElement('div'); c3.appendChild(mkLabel('Vendidos')); c3.appendChild(mkInput('av-'+p.id,p.sold,'number')); r2.appendChild(c3);
  const c4=document.createElement('div'); c4.appendChild(mkLabel('Estrellas (1-5)')); const sinp=mkInput('as-'+p.id,p.stars,'number'); sinp.min='1';sinp.max='5'; c4.appendChild(sinp); r2.appendChild(c4);
  card.appendChild(r2);

  // Imágenes
  card.appendChild(buildImgRow(p.id,'', p.img, '📷 Imagen Principal'));
  card.appendChild(buildImgRow(p.id,'2', p.img2||p.img, '📷 Imagen Secundaria'));

  // Categoría
  card.appendChild(mkLabel('Categoría'));
  const sel=document.createElement('select'); sel.id='ac-'+p.id;
  Object.assign(sel.style,{width:'100%',padding:'8px',border:'1.5px solid #e5e5e5',borderRadius:'8px',fontSize:'13px',fontFamily:'Nunito,sans-serif'});
  ['belleza','hogar','tecnologia','salud','fitness','juguetes','accesorios'].forEach(c=>{
    const opt=document.createElement('option'); opt.value=c; opt.textContent=c; if(p.cat===c) opt.selected=true; sel.appendChild(opt);
  });
  card.appendChild(sel);

  // Últimas unidades / timer
  const r3=document.createElement('div'); r3.className='row2'; Object.assign(r3.style,{marginTop:'6px'});
  const c5=document.createElement('div'); c5.appendChild(mkLabel('Últimas unidades'));
  const sel2=document.createElement('select'); sel2.id='alu-'+p.id;
  Object.assign(sel2.style,{width:'100%',padding:'8px',border:'1.5px solid #e5e5e5',borderRadius:'8px',fontSize:'13px',fontFamily:'Nunito,sans-serif'});
  [{v:'true',t:'Sí'},{v:'false',t:'No'}].forEach(({v,t})=>{ const o=document.createElement('option');o.value=v;o.textContent=t;if((p.lastUnits?'true':'false')===v)o.selected=true;sel2.appendChild(o);});
  c5.appendChild(sel2); r3.appendChild(c5);
  const c6=document.createElement('div'); c6.appendChild(mkLabel('Timer (segundos)')); c6.appendChild(mkInput('at-'+p.id,p.timer,'number')); r3.appendChild(c6);
  card.appendChild(r3);

  // Botón guardar
  const saveBtn=document.createElement('button');
  saveBtn.textContent='💾 Guardar este producto'; saveBtn.className='btn-save-admin';
  Object.assign(saveBtn.style,{marginTop:'12px',width:'100%',fontSize:'14px'});
  saveBtn.onclick=()=>saveOneProduct(p.id);
  card.appendChild(saveBtn);

  return card;
}

function renderAdminProducts(){
  const list=document.getElementById('admin-product-list');
  list.innerHTML='';
  products.forEach(p=> list.appendChild(buildProductCard(p)));
}

function deleteProduct(id){
  if(!confirm('¿Eliminar este producto?')) return;
  products=products.filter(p=>p.id!==id);
  localStorage.setItem('trogui_products',JSON.stringify(products));
  renderAdminProducts();
  renderProducts(products);
}

function addNewProduct(){
  const newId='P'+String(Date.now()).slice(-5);
  products.push({id:newId,name:'Nuevo Producto',cat:'hogar',
    img:'https://images.unsplash.com/photo-1512436991641-6745cdb1723f?w=400',
    img2:'https://images.unsplash.com/photo-1512436991641-6745cdb1723f?w=400',
    price:49000,oldPrice:89000,desc:'Descripción del producto.',sold:10,stars:5,lastUnits:false,timer:3600});
  localStorage.setItem('trogui_products',JSON.stringify(products));
  renderAdminProducts();
  renderProducts(products);
  setTimeout(()=>document.getElementById('admin-product-list').lastElementChild?.scrollIntoView({behavior:'smooth'}),150);
}

function saveOneProduct(id){
  const p=products.find(x=>x.id===id);
  if(!p) return;
  const nEl=document.getElementById('an-'+id); if(!nEl) return;
  p.name  = nEl.value || p.name;
  p.desc  = document.getElementById('ad-'+id).value;
  p.price = parseInt(document.getElementById('ap-'+id).value)||p.price;
  p.oldPrice = parseInt(document.getElementById('ao-'+id).value)||p.oldPrice;
  p.sold  = parseInt(document.getElementById('av-'+id).value)||p.sold;
  p.stars = parseInt(document.getElementById('as-'+id).value)||p.stars;
  const img1 = document.getElementById('ai-'+id).value.trim();
  const img2 = document.getElementById('ai2-'+id).value.trim();
  if(img1) p.img=img1;
  if(img2) p.img2=img2;
  p.cat   = document.getElementById('ac-'+id).value;
  p.lastUnits = document.getElementById('alu-'+id).value==='true';
  p.timer = parseInt(document.getElementById('at-'+id).value)||p.timer;
  localStorage.setItem('trogui_products',JSON.stringify(products));
  renderProducts(products);
  showFloatMsg('✅ "'+p.name+'" guardado!');
}

function saveProducts(silent){
  products.forEach(p=>saveOneProduct(p.id));
  localStorage.setItem('trogui_products',JSON.stringify(products));
  renderProducts(products);
  if(!silent) showFloatMsg('✅ Todos los productos guardados!');
}

// ===================== ADMIN C - ORDERS =====================
function openAdminC(){
  const list=document.getElementById('admin-orders-list');
  if(orders.length===0){
    list.innerHTML='<div style="text-align:center;padding:40px;color:#888;font-size:15px">📭 No hay pedidos registrados aún.</div>';
  } else {
    list.innerHTML=orders.slice().reverse().map(o=>`
      <div class="order-item" style="border:2px solid #e5e5e5;border-radius:14px;padding:16px;margin-bottom:12px;background:#fff;box-shadow:0 2px 8px rgba(0,0,0,.06)">
        <div style="display:flex;justify-content:space-between;align-items:flex-start;flex-wrap:wrap;gap:8px;margin-bottom:10px">
          <div>
            <span style="background:#FF5200;color:#fff;padding:3px 10px;border-radius:20px;font-size:12px;font-weight:800">#${o.id}</span>
            <span style="background:#00b050;color:#fff;padding:3px 10px;border-radius:20px;font-size:12px;font-weight:800;margin-left:6px">Contra Entrega</span>
          </div>
          <div style="font-size:12px;color:#888;font-weight:700">📅 ${o.fecha}</div>
        </div>
        <div style="display:grid;grid-template-columns:1fr 1fr;gap:8px;font-size:13px">
          <div style="grid-column:1/-1;background:#fff8f0;border:1px solid #FF5200;border-radius:10px;padding:10px">
            <div style="font-weight:800;font-size:14px;color:#FF5200">📦 ${o.product}</div>
            <div style="color:#888;font-size:12px">ID Producto: ${o.productId}</div>
            <div style="display:flex;gap:16px;margin-top:6px;flex-wrap:wrap">
              <div><span style="text-decoration:line-through;color:#aaa;font-size:12px">Antes: $${fmt(o.oldPrice||0)}</span></div>
              <div style="font-weight:900;color:#FF5200;font-size:16px">Paga: $${fmt(o.price)}</div>
              <div style="color:#00b050;font-weight:800">Ahorro: $${fmt(o.ahorro||((o.oldPrice||0)-(o.price||0)))}</div>
            </div>
          </div>
          <div style="background:#f8f8f8;border-radius:10px;padding:10px">
            <div style="font-weight:800;margin-bottom:4px;color:#1a1a2e">👤 Cliente</div>
            <div>${o.nombre} ${o.apellido}</div>
            <div style="color:#FF5200;font-weight:800">📞 ${o.telefono}</div>
          </div>
          <div style="background:#f8f8f8;border-radius:10px;padding:10px">
            <div style="font-weight:800;margin-bottom:4px;color:#1a1a2e">📍 Ubicación</div>
            <div>${o.depto||''}</div>
            <div style="font-weight:700">${o.ciudad}</div>
          </div>
          <div style="grid-column:1/-1;background:#f0fff4;border:1px solid #00b050;border-radius:10px;padding:10px">
            <div style="font-weight:800;color:#00b050;margin-bottom:2px">🚚 Entrega: ${(o.tipoEntrega==='oficina')?'📦 Oficina Interrapidísimo':'🏠 A domicilio'}</div>
            <div style="font-size:13px">${o.direccion}</div>
          </div>
          ${o.nota?`<div style="grid-column:1/-1;background:#fffbe6;border:1px solid #f5c518;border-radius:10px;padding:10px;font-size:13px"><b>📝 Nota:</b> ${o.nota}</div>`:''}
          ${o.llegadaEst?`<div style="grid-column:1/-1;font-size:12px;color:#888;font-weight:700">📆 Entrega estimada: ${o.llegadaEst}</div>`:''}
        </div>
        <div style="margin-top:10px;display:flex;gap:8px;flex-wrap:wrap">
          <a href="https://wa.me/57${o.telefono}" target="_blank"
            style="background:#25D366;color:#fff;padding:7px 14px;border-radius:8px;font-weight:800;font-size:12px;text-decoration:none">
            💬 WhatsApp cliente
          </a>
          <button onclick="deleteOrder('${o.id}')"
            style="background:#fee;color:#c00;border:1px solid #fcc;padding:7px 14px;border-radius:8px;font-weight:800;font-size:12px;cursor:pointer">
            🗑️ Eliminar
          </button>
        </div>
      </div>`).join('');
  }
  document.getElementById('admin-c').classList.add('active');
}

function deleteOrder(id){
  if(!confirm('¿Eliminar este pedido?')) return;
  orders=orders.filter(o=>o.id!==id);
  localStorage.setItem('trogui_orders',JSON.stringify(orders));
  openAdminC();
}
function clearOrders(){if(confirm('¿Limpiar TODOS los pedidos?')){orders=[];localStorage.removeItem('trogui_orders');openAdminC();}}

// ===================== ADMIN E - PAGE =====================
function openAdminE(){
  document.getElementById('edit-topbar').value=document.querySelector('.topbar').innerHTML.replace(/<[^>]+>/g,'');
  document.getElementById('edit-prod-title').value=document.querySelector('.section-title').textContent;
  const au=localStorage.getItem('trogui_audio')||'';
  document.getElementById('audio-url-input').value=au;
  renderAdminReviews();
  document.getElementById('admin-e').classList.add('active');
}
function savePageSetting(key){
  if(key==='topbar'){
    const val=document.getElementById('edit-topbar').value;
    document.querySelector('.topbar').textContent=val;
    localStorage.setItem('trogui_topbar',val);
  } else if(key==='prod-title'){
    const val=document.getElementById('edit-prod-title').value;
    document.querySelector('.section-title').innerHTML=val;
    localStorage.setItem('trogui_prod_title',val);
  }
  showFloatMsg('✅ Guardado correctamente');
}
function setAudio(){
  const url=document.getElementById('audio-url-input').value.trim();
  if(!url){alert('Ingresa una URL de audio');return;}
  document.getElementById('audio-src').src=url;
  document.getElementById('audio-autoplay').load();
  document.getElementById('audio-autoplay').play();
  localStorage.setItem('trogui_audio',url);
  showFloatMsg('✅ Audio establecido');
}
function renderAdminReviews(){
  const cont=document.getElementById('admin-reviews-list');
  cont.innerHTML=reviews.map((r,i)=>`
    <div class="admin-review-item">
      <input type="text" id="rn-${i}" value="${r.name}" placeholder="Nombre">
      <input type="text" id="rc-${i}" value="${r.city}" placeholder="Ciudad">
      <select id="rs-${i}">${[1,2,3,4,5].map(s=>`<option value="${s}"${r.stars===s?' selected':''}>${s} ⭐</option>`).join('')}</select>
      <textarea id="rt-${i}" rows="2">${r.text}</textarea>
    </div>`).join('');
}
function saveReviews(){
  reviews=reviews.map((r,i)=>({
    name:document.getElementById('rn-'+i).value||r.name,
    city:document.getElementById('rc-'+i).value||r.city,
    stars:parseInt(document.getElementById('rs-'+i).value)||r.stars,
    text:document.getElementById('rt-'+i).value||r.text,
  }));
  localStorage.setItem('trogui_reviews',JSON.stringify(reviews));
  showFloatMsg('✅ Reseñas guardadas');
}
</script>
</body>
</html>

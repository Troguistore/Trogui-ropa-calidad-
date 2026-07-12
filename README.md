<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>PRIMO STORE — Tienda Colombia 🇨🇴</title>
<meta name="description" content="Envío gratis a toda Colombia, pago contra entrega. Bazar, belleza, hogar, tecnología y más.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@500;700;800&family=Inter:wght@400;500;600;700&family=IBM+Plex+Mono:wght@500;600&display=swap" rel="stylesheet">
<style>
:root{
  --ink:#151417;
  --ink-soft:#5b5763;
  --paper:#ffffff;
  --paper-soft:#faf7f2;
  --line:#ece7e0;
  --coral:#ff5470;
  --coral-deep:#e13a56;
  --mango:#ff8a3d;
  --teal:#0b8a72;
  --teal-deep:#066a58;
  --yellow:#ffc93c;
  --radius:16px;
  --shadow:0 10px 30px -12px rgba(20,15,10,.18);
  --fs-h1:clamp(1.7rem,1.15rem + 2.4vw,3.1rem);
  --fs-h2:clamp(1.25rem,1rem + 1.1vw,2rem);
  --fs-h3:clamp(1.02rem,0.94rem + 0.4vw,1.25rem);
  --fs-body:clamp(0.92rem,0.88rem + 0.2vw,1rem);
  --fs-small:clamp(0.76rem,0.73rem + 0.15vw,0.85rem);
  --fs-price:clamp(1.05rem,0.95rem + 0.4vw,1.3rem);
}
*{box-sizing:border-box;}
html{-webkit-text-size-adjust:100%;scroll-behavior:smooth;}
body{
  margin:0;font-family:'Inter',system-ui,sans-serif;color:var(--ink);
  background:var(--paper-soft);font-size:var(--fs-body);line-height:1.5;
  overflow-x:hidden;
}
h1,h2,h3{font-family:'Baloo 2',system-ui,sans-serif;margin:0;line-height:1.08;letter-spacing:.2px;}
img,video{max-width:100%;display:block;}
button{font-family:inherit;cursor:pointer;}
a{color:inherit;text-decoration:none;}
.mono{font-family:'IBM Plex Mono',monospace;}
.container{max-width:1180px;margin:0 auto;padding:0 clamp(14px,3vw,32px);}

/* ---------- MARQUEE ---------- */
.marquee-bar{background:var(--ink);color:#fff;overflow:hidden;white-space:nowrap;font-size:var(--fs-small);}
.marquee-track{display:inline-block;padding:7px 0;animation:scrollmarquee 24s linear infinite;}
.marquee-track span{margin:0 28px;}
@keyframes scrollmarquee{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}

/* ---------- HEADER ---------- */
header.site-header{
  position:sticky;top:0;z-index:60;background:rgba(255,255,255,.92);
  backdrop-filter:blur(8px);border-bottom:1px solid var(--line);
}
.header-row{display:flex;align-items:center;gap:14px;padding:10px clamp(14px,3vw,32px);max-width:1180px;margin:0 auto;}
.brand{display:flex;align-items:center;gap:8px;font-family:'Baloo 2';font-weight:800;font-size:clamp(1.1rem,1rem + .6vw,1.5rem);color:var(--coral-deep);white-space:nowrap;}
.brand .dot{width:9px;height:9px;border-radius:50%;background:var(--teal);display:inline-block;}
.search-wrap{flex:1;min-width:0;position:relative;}
.search-wrap input{
  width:100%;padding:10px 14px 10px 36px;border-radius:999px;border:1.5px solid var(--line);
  background:var(--paper-soft);font-size:var(--fs-small);outline:none;
}
.search-wrap input:focus{border-color:var(--coral);}
.search-wrap .ic{position:absolute;left:12px;top:50%;transform:translateY(-50%);opacity:.6;font-size:.9rem;}
.header-actions{display:flex;align-items:center;gap:10px;}
.icon-btn{
  position:relative;width:38px;height:38px;border-radius:50%;border:1.5px solid var(--line);
  background:#fff;display:flex;align-items:center;justify-content:center;font-size:1.05rem;flex-shrink:0;
}
.icon-btn .badge{
  position:absolute;top:-6px;right:-6px;background:var(--coral);color:#fff;font-size:.65rem;
  min-width:18px;height:18px;border-radius:999px;display:flex;align-items:center;justify-content:center;
  font-weight:700;padding:0 4px;
}
.wa-btn{
  background:var(--teal);color:#fff;border-radius:999px;padding:9px 14px;font-weight:600;
  font-size:var(--fs-small);display:flex;align-items:center;gap:6px;white-space:nowrap;
}

/* category nav */
nav.cats{display:flex;gap:8px;overflow-x:auto;padding:10px clamp(14px,3vw,32px) 12px;scrollbar-width:none;}
nav.cats::-webkit-scrollbar{display:none;}
nav.cats button{
  flex-shrink:0;border:1.5px solid var(--line);background:#fff;border-radius:999px;
  padding:7px 14px;font-size:var(--fs-small);font-weight:600;color:var(--ink-soft);
  display:flex;align-items:center;gap:6px;transition:.15s;
}
nav.cats button.active,nav.cats button:hover{background:var(--ink);color:#fff;border-color:var(--ink);}

/* ---------- HERO ---------- */
.hero{position:relative;overflow:hidden;background:linear-gradient(135deg,#fff3e9,#fdeaf0 55%,#eaf7f2);}
.hero-slides{position:relative;height:clamp(260px,42vw,420px);}
.hero-slide{
  position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center;
  text-align:center;padding:20px;opacity:0;transition:opacity .6s ease;pointer-events:none;
}
.hero-slide.active{opacity:1;pointer-events:auto;}
.hero-slide .eyebrow{
  font-family:'IBM Plex Mono';font-size:var(--fs-small);letter-spacing:.08em;text-transform:uppercase;
  background:#fff;padding:5px 12px;border-radius:999px;border:1.5px dashed var(--coral);color:var(--coral-deep);margin-bottom:14px;
}
.hero-slide h1{font-size:var(--fs-h1);max-width:720px;color:var(--ink);}
.hero-slide h1 em{font-style:normal;color:var(--coral-deep);}
.hero-slide p{margin-top:10px;color:var(--ink-soft);font-size:var(--fs-body);max-width:520px;}
.hero-cta{
  margin-top:18px;background:var(--coral);color:#fff;border:none;padding:12px 26px;border-radius:999px;
  font-weight:700;font-size:var(--fs-body);box-shadow:var(--shadow);
}
.hero-dots{position:absolute;bottom:16px;left:50%;transform:translateX(-50%);display:flex;gap:7px;z-index:5;}
.hero-dots span{width:7px;height:7px;border-radius:50%;background:#d9d3c8;cursor:pointer;}
.hero-dots span.active{background:var(--coral);width:20px;border-radius:6px;}
.hero-arrow{
  position:absolute;top:50%;transform:translateY(-50%);width:34px;height:34px;border-radius:50%;
  background:#fff;border:1px solid var(--line);display:flex;align-items:center;justify-content:center;z-index:5;
  font-size:1rem;color:var(--ink);
}
.hero-arrow.left{left:12px}.hero-arrow.right{right:12px}

.trust-strip{display:flex;flex-wrap:wrap;gap:10px 22px;justify-content:center;padding:14px 16px;
  background:#fff;border-top:1px solid var(--line);border-bottom:1px solid var(--line);font-size:var(--fs-small);color:var(--ink-soft);}
.trust-strip span{white-space:nowrap;}

/* ---------- TICKETS / SECTION TITLES ---------- */
.section{padding:clamp(28px,5vw,52px) 0;}
.section-head{display:flex;align-items:flex-end;justify-content:space-between;gap:14px;margin-bottom:18px;flex-wrap:wrap;}
.ticket-title{position:relative;display:inline-block;}
.ticket-title h2{font-size:var(--fs-h2);}
.ticket-title .tag{
  display:inline-block;margin-top:4px;background:var(--yellow);color:var(--ink);
  padding:3px 12px;border-radius:4px;font-family:'IBM Plex Mono';font-size:var(--fs-small);font-weight:600;
  transform:rotate(-1.5deg);
}
.section-sub{color:var(--ink-soft);font-size:var(--fs-small);max-width:420px;}

/* ---------- PRODUCT GRID ---------- */
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(155px,1fr));gap:clamp(10px,1.8vw,18px);}
.card{
  background:#fff;border:1px solid var(--line);border-radius:var(--radius);overflow:hidden;
  display:flex;flex-direction:column;transition:transform .18s ease,box-shadow .18s ease;position:relative;
}
.card:hover{transform:translateY(-4px);box-shadow:var(--shadow);}
.card .media{aspect-ratio:1/1;background:var(--paper-soft);overflow:hidden;position:relative;}
.card .media img,.card .media video{width:100%;height:100%;object-fit:cover;}
.card .kit-flag{
  position:absolute;top:8px;left:8px;background:var(--teal);color:#fff;font-size:.65rem;font-weight:700;
  padding:3px 8px;border-radius:999px;letter-spacing:.03em;text-transform:uppercase;
}
.card .off-flag{
  position:absolute;top:8px;right:8px;background:var(--coral);color:#fff;font-size:.68rem;font-weight:700;
  padding:3px 7px;border-radius:6px;
}
.card .body{padding:10px 12px 12px;display:flex;flex-direction:column;gap:6px;flex:1;}
.card .cat{font-size:.68rem;color:var(--ink-soft);text-transform:uppercase;letter-spacing:.04em;font-weight:600;}
.card h3{font-size:var(--fs-h3);font-weight:600;font-family:'Inter';min-height:2.4em;}
.price-row{display:flex;align-items:baseline;gap:7px;margin-top:auto;flex-wrap:wrap;}
.price-row .now{font-family:'IBM Plex Mono';font-weight:700;font-size:var(--fs-price);color:var(--coral-deep);}
.price-row .old{font-family:'IBM Plex Mono';font-size:.78rem;color:#b3aca3;text-decoration:line-through;}
.add-btn{
  margin-top:8px;width:100%;padding:9px;border:none;border-radius:10px;background:var(--ink);color:#fff;
  font-weight:600;font-size:var(--fs-small);transition:.15s;
}
.add-btn:active{transform:scale(.97);}
.add-btn.added{background:var(--teal);}

/* ---------- DELIVERY CALCULATOR ---------- */
.calc-box{
  background:#fff;border:1.5px dashed var(--teal);border-radius:var(--radius);padding:clamp(18px,3vw,30px);
  display:flex;flex-wrap:wrap;gap:14px;align-items:center;justify-content:space-between;
}
.calc-box select,.calc-box button{
  padding:11px 14px;border-radius:10px;border:1.5px solid var(--line);font-size:var(--fs-small);background:var(--paper-soft);
}
.calc-box button{background:var(--teal);color:#fff;border:none;font-weight:700;}
#calcResult{font-size:var(--fs-small);font-weight:600;color:var(--teal-deep);}

/* ---------- REVIEWS ---------- */
.reviews-strip{display:flex;gap:14px;overflow-x:auto;padding-bottom:6px;}
.review-card{
  flex:0 0 260px;background:#fff;border:1px solid var(--line);border-radius:var(--radius);padding:16px;
}
.review-card .stars{color:var(--yellow);letter-spacing:2px;font-size:.9rem;}
.review-card p{font-size:var(--fs-small);color:var(--ink-soft);margin:8px 0;}
.review-card .who{font-weight:700;font-size:var(--fs-small);}

/* ---------- FOOTER ---------- */
footer{background:var(--ink);color:#fff;padding:clamp(30px,5vw,56px) 0 20px;margin-top:20px;}
.foot-grid{display:grid;grid-template-columns:1.4fr 1fr 1fr 1fr;gap:26px;}
footer h4{font-size:.85rem;text-transform:uppercase;letter-spacing:.06em;color:#ffc93c;margin-bottom:10px;}
footer p,footer li{color:#cfcbd4;font-size:var(--fs-small);}
footer ul{list-style:none;padding:0;margin:0;display:flex;flex-direction:column;gap:6px;}
.foot-bottom{border-top:1px solid #333;margin-top:26px;padding-top:16px;text-align:center;font-size:.75rem;color:#8b8794;}
@media(max-width:720px){.foot-grid{grid-template-columns:1fr 1fr;}}

/* ---------- FLOATING BUTTONS ---------- */
.fab-wa{
  position:fixed;bottom:20px;right:16px;z-index:70;background:var(--teal);color:#fff;width:56px;height:56px;
  border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:1.6rem;box-shadow:var(--shadow);
}
.fab-cart{
  position:fixed;bottom:20px;left:16px;z-index:70;background:var(--ink);color:#fff;width:56px;height:56px;
  border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:1.5rem;box-shadow:var(--shadow);
}
.fab-cart .badge{
  position:absolute;top:-4px;right:-4px;background:var(--coral);min-width:20px;height:20px;border-radius:999px;
  font-size:.7rem;display:flex;align-items:center;justify-content:center;font-weight:700;
}
.admin-triggers{position:fixed;bottom:4px;left:50%;transform:translateX(-50%);z-index:65;display:flex;gap:2px;opacity:.28;}
.admin-triggers button{
  width:16px;height:16px;font-size:.55rem;border:none;background:transparent;color:#555;font-family:'IBM Plex Mono';
}
.admin-triggers:hover{opacity:.85;}

/* ---------- MODALS ---------- */
.overlay{
  position:fixed;inset:0;background:rgba(15,12,10,.55);z-index:100;display:none;align-items:flex-end;justify-content:center;
}
.overlay.show{display:flex;}
@media(min-width:720px){.overlay{align-items:center;}}
.sheet{
  background:#fff;width:100%;max-width:520px;max-height:88vh;overflow-y:auto;border-radius:20px 20px 0 0;
  padding:20px;position:relative;animation:sheetup .25s ease;
}
@media(min-width:720px){.sheet{border-radius:20px;}}
@keyframes sheetup{from{transform:translateY(30px);opacity:0}to{transform:translateY(0);opacity:1}}
.sheet.wide{max-width:820px;}
.sheet-close{position:absolute;top:14px;right:14px;width:32px;height:32px;border-radius:50%;border:none;background:var(--paper-soft);font-size:1rem;}
.sheet h2{font-size:var(--fs-h2);margin-bottom:14px;padding-right:30px;}
.form-row{margin-bottom:12px;}
.form-row label{display:block;font-size:.75rem;font-weight:600;color:var(--ink-soft);margin-bottom:4px;}
.form-row input,.form-row select,.form-row textarea{
  width:100%;padding:10px 12px;border:1.5px solid var(--line);border-radius:10px;font-size:var(--fs-small);
  font-family:inherit;background:var(--paper-soft);
}
.two-col{display:grid;grid-template-columns:1fr 1fr;gap:10px;}
.btn-primary{
  width:100%;padding:13px;border:none;border-radius:12px;background:var(--teal);color:#fff;font-weight:700;
  font-size:var(--fs-body);margin-top:6px;
}
.btn-secondary{
  width:100%;padding:11px;border:1.5px solid var(--line);border-radius:12px;background:#fff;color:var(--ink);
  font-weight:600;font-size:var(--fs-small);margin-top:8px;
}

/* cart items */
.cart-item{display:flex;gap:10px;align-items:center;padding:10px 0;border-bottom:1px solid var(--line);}
.cart-item img{width:56px;height:56px;border-radius:10px;object-fit:cover;flex-shrink:0;}
.cart-item .ci-info{flex:1;min-width:0;}
.cart-item .ci-info h4{font-size:var(--fs-small);font-weight:600;margin:0 0 4px;}
.qty-ctrl{display:flex;align-items:center;gap:8px;}
.qty-ctrl button{width:26px;height:26px;border-radius:50%;border:1px solid var(--line);background:#fff;font-weight:700;}
.cart-total-row{display:flex;justify-content:space-between;align-items:center;padding:14px 0 4px;font-weight:700;font-size:var(--fs-h3);}
.remove-x{background:none;border:none;color:#b3aca3;font-size:.85rem;}

/* wheel */
.wheel-wrap{display:flex;flex-direction:column;align-items:center;gap:14px;}
.wheel{
  width:220px;height:220px;border-radius:50%;position:relative;
  background:conic-gradient(var(--coral) 0 60deg,var(--mango) 0 120deg,var(--teal) 0 180deg,var(--yellow) 0 240deg,var(--coral-deep) 0 300deg,var(--teal-deep) 0 360deg);
  transition:transform 4s cubic-bezier(.17,.67,.16,1);border:6px solid #fff;box-shadow:var(--shadow);
}
.wheel-pointer{position:absolute;top:-4px;left:50%;transform:translateX(-50%);font-size:1.6rem;z-index:2;}
.wheel-labels{position:absolute;inset:0;}
.wheel-labels span{position:absolute;color:#fff;font-weight:800;font-size:.72rem;font-family:'IBM Plex Mono';}

/* admin */
.admin-product-row{border:1px solid var(--line);border-radius:12px;padding:12px;margin-bottom:10px;}
.admin-product-row .arow-top{display:flex;gap:10px;}
.admin-product-row img,.admin-product-row video{width:64px;height:64px;object-fit:cover;border-radius:8px;flex-shrink:0;background:var(--paper-soft);}
.admin-product-row .arow-fields{flex:1;display:grid;grid-template-columns:1fr 1fr;gap:6px;}
.admin-product-row input,.admin-product-row select{padding:7px 8px;font-size:.75rem;border:1px solid var(--line);border-radius:6px;}
.admin-product-row .del-btn{background:var(--coral);color:#fff;border:none;border-radius:8px;padding:5px 9px;font-size:.7rem;margin-top:6px;}
.admin-tabs{display:flex;gap:8px;margin-bottom:14px;}
.admin-tabs button{padding:8px 12px;border-radius:8px;border:1px solid var(--line);background:#fff;font-size:.75rem;font-weight:600;}
.admin-tabs button.active{background:var(--ink);color:#fff;}
table.orders-table{width:100%;border-collapse:collapse;font-size:.75rem;}
table.orders-table th,table.orders-table td{border:1px solid var(--line);padding:6px;text-align:left;}
.small-note{font-size:.7rem;color:var(--ink-soft);margin-top:4px;}
.hidden{display:none !important;}
:focus-visible{outline:3px solid var(--coral);outline-offset:2px;}
@media(prefers-reduced-motion:reduce){*{animation-duration:.001ms !important;transition-duration:.001ms !important;}}
</style>
</head>
<body>

<div class="marquee-bar"><div class="marquee-track" id="marqueeTrack"></div></div>

<header class="site-header">
  <div class="header-row">
    <div class="brand"><span class="dot"></span>PRIMO<span style="color:var(--teal)">STORE</span></div>
    <div class="search-wrap">
      <span class="ic">🔍</span>
      <input id="searchInput" type="text" placeholder="Buscar producto...">
    </div>
    <div class="header-actions">
      <a class="wa-btn" id="waHeaderBtn" href="#" target="_blank">💬 <span class="mono" id="waHeaderNum">320 657 2598</span></a>
      <button class="icon-btn" id="cartIconBtn">🛒<span class="badge" id="cartBadge">0</span></button>
    </div>
  </div>
  <nav class="cats" id="catNav"></nav>
</header>

<section class="hero">
  <div class="hero-slides" id="heroSlides"></div>
  <div class="hero-dots" id="heroDots"></div>
  <button class="hero-arrow left" onclick="prevSlide()">‹</button>
  <button class="hero-arrow right" onclick="nextSlide()">›</button>
</section>
<div class="trust-strip">
  <span>✅ Pago contra entrega</span><span>🚚 Envío gratis a toda Colombia</span>
  <span>📦 3 a 7 días hábiles</span><span>🔒 Compra 100% segura</span><span>⭐ Clientes felices</span>
</div>

<main class="container">

  <section class="section" id="products">
    <div class="section-head">
      <div class="ticket-title">
        <h2 id="sectionTitleText">🔥 Productos en Oferta</h2>
        <span class="tag">precio de bazar, calidad premium</span>
      </div>
      <p class="section-sub">Envío gratis · Pago contra entrega · Toca una categoría para filtrar.</p>
    </div>
    <div class="grid" id="productGrid"></div>
  </section>

  <section class="section">
    <div class="calc-box">
      <div>
        <h3 style="font-size:var(--fs-h3);margin-bottom:6px;">📅 ¿Cuándo llega mi pedido?</h3>
        <p class="section-sub" style="margin:0;">Selecciona tu ciudad y calculamos la fecha estimada.</p>
      </div>
      <div style="display:flex;gap:8px;flex-wrap:wrap;align-items:center;">
        <select id="citySelect">
          <option value="">-- Selecciona tu ciudad --</option>
        </select>
        <button onclick="calcularFecha()">Calcular fecha</button>
      </div>
      <div id="calcResult"></div>
    </div>
  </section>

  <section class="section">
    <div class="section-head">
      <div class="ticket-title"><h2>⭐ Lo que dicen nuestros clientes</h2></div>
    </div>
    <div class="reviews-strip" id="reviewsStrip"></div>
  </section>

</main>

<footer>
  <div class="container foot-grid">
    <div>
      <div class="brand" style="color:#fff;margin-bottom:8px;">PRIMO<span style="color:var(--yellow)">STORE</span></div>
      <p>Tienda colombiana de confianza. Envío gratis y pago contra entrega a todo el país.</p>
      <div style="display:flex;gap:10px;margin-top:10px;font-size:1.2rem;">
        <a href="https://www.instagram.com" target="_blank">📸</a>
        <a href="https://www.tiktok.com" target="_blank">🎵</a>
        <a href="#" id="waFootIcon" target="_blank">💬</a>
      </div>
    </div>
    <div>
      <h4>Contacto</h4>
      <ul><li id="waFootText">📞 320 657 2598</li><li>📧 pedidos@primostore.co</li><li>🇨🇴 Colombia — Nacional</li></ul>
    </div>
    <div>
      <h4>Transportadoras</h4>
      <ul><li>📦 Interrapidísimo</li><li>📦 Coordinadora</li><li>📦 Envía</li></ul>
    </div>
    <div>
      <h4>Pagos</h4>
      <ul><li>💵 Contra entrega</li><li>🏦 Transferencia</li><li>💳 Nequi / Daviplata</li></ul>
    </div>
  </div>
  <div class="foot-bottom">© 2026 PRIMOSTORE · Tienda colombiana de confianza 🇨🇴</div>
</footer>

<audio id="bgAudio" loop></audio>

<!-- floating buttons -->
<a class="fab-wa" id="fabWa" href="#" target="_blank">💬</a>
<button class="fab-cart" id="fabCartBtn">🛒<span class="badge" id="fabCartBadge">0</span></button>
<div class="admin-triggers">
  <button onclick="openAdmin('R')">R</button>
  <button onclick="openAdmin('C')">C</button>
  <button onclick="openAdmin('E')">E</button>
</div>

<!-- CART MODAL -->
<div class="overlay" id="cartOverlay">
  <div class="sheet">
    <button class="sheet-close" onclick="closeModal('cartOverlay')">✕</button>
    <h2>🛒 Mi carrito</h2>
    <div id="cartItemsWrap"></div>
    <div class="cart-total-row"><span>Total</span><span class="mono" id="cartTotal">$0</span></div>
    <button class="btn-primary" onclick="openCheckout()">Pedir por WhatsApp 💬</button>
  </div>
</div>

<!-- CHECKOUT MODAL -->
<div class="overlay" id="checkoutOverlay">
  <div class="sheet">
    <button class="sheet-close" onclick="closeModal('checkoutOverlay')">✕</button>
    <h2>📋 Confirmar pedido</h2>
    <form id="checkoutForm" onsubmit="submitOrder(event)">
      <div class="two-col">
        <div class="form-row"><label>Nombre *</label><input required id="ckNombre"></div>
        <div class="form-row"><label>Apellido *</label><input required id="ckApellido"></div>
      </div>
      <div class="two-col">
        <div class="form-row"><label>Departamento *</label><select required id="ckDepto"></select></div>
        <div class="form-row"><label>Ciudad *</label><input required id="ckCiudad"></div>
      </div>
      <div class="form-row"><label>Dirección completa *</label><input required id="ckDireccion"></div>
      <div class="form-row"><label>Teléfono *</label><input required id="ckTelefono" type="tel"></div>
      <div class="form-row"><label>Nota (opcional)</label><textarea id="ckNota" rows="2"></textarea></div>
      <button class="btn-primary" type="submit">✅ Confirmar pedido por WhatsApp</button>
    </form>
  </div>
</div>

<!-- WHEEL MODAL -->
<div class="overlay" id="wheelOverlay">
  <div class="sheet">
    <button class="sheet-close" onclick="closeModal('wheelOverlay')">✕</button>
    <h2>🎡 ¡Gira y gana!</h2>
    <p class="section-sub">Gira la ruleta y obtén un premio para tu pedido.</p>
    <div class="wheel-wrap">
      <div style="position:relative;">
        <div class="wheel-pointer">▼</div>
        <div class="wheel" id="wheelEl">
          <div class="wheel-labels" id="wheelLabels"></div>
        </div>
      </div>
      <button class="btn-primary" style="width:auto;padding:12px 26px;" onclick="spinWheel()">¡Girar ruleta! 🎉</button>
      <p id="wheelResult" style="font-weight:700;"></p>
    </div>
  </div>
</div>

<!-- ADMIN PASSWORD -->
<div class="overlay" id="pwOverlay">
  <div class="sheet" style="max-width:340px;">
    <button class="sheet-close" onclick="closeModal('pwOverlay')">✕</button>
    <h2>🔒 Acceso admin</h2>
    <div class="form-row"><label>Contraseña</label><input id="pwInput" type="password" autocomplete="off"></div>
    <button class="btn-primary" onclick="checkPassword()">Entrar</button>
  </div>
</div>

<!-- ADMIN R: PRODUCTOS -->
<div class="overlay" id="adminROverlay">
  <div class="sheet wide">
    <button class="sheet-close" onclick="closeModal('adminROverlay')">✕</button>
    <h2>✏️ Editor de productos</h2>
    <button class="btn-secondary" onclick="addNewProduct()">➕ Agregar producto</button>
    <div id="adminProductList" style="margin-top:14px;"></div>
    <button class="btn-primary" onclick="saveAllProducts()">💾 Guardar todos</button>
  </div>
</div>

<!-- ADMIN C: PEDIDOS -->
<div class="overlay" id="adminCOverlay">
  <div class="sheet wide">
    <button class="sheet-close" onclick="closeModal('adminCOverlay')">✕</button>
    <h2>📦 Pedidos recibidos</h2>
    <div style="display:flex;gap:8px;margin-bottom:12px;">
      <button class="btn-secondary" style="margin:0;" onclick="exportOrdersCSV()">📥 Exportar CSV</button>
      <button class="btn-secondary" style="margin:0;color:var(--coral-deep);" onclick="clearOrders()">🗑️ Limpiar</button>
    </div>
    <div style="overflow-x:auto;"><table class="orders-table" id="ordersTable"></table></div>
  </div>
</div>

<!-- ADMIN E: PAGINA -->
<div class="overlay" id="adminEOverlay">
  <div class="sheet">
    <button class="sheet-close" onclick="closeModal('adminEOverlay')">✕</button>
    <h2>🎨 Editor de página</h2>
    <div class="form-row"><label>📢 Texto del marquee (separa frases con "|")</label><textarea id="eMarquee" rows="2"></textarea></div>
    <div class="form-row"><label>Título del hero (usa | entre líneas)</label><input id="eHeroTitle"></div>
    <div class="form-row"><label>Subtítulo del hero</label><input id="eHeroSub"></div>
    <div class="form-row"><label>🏷️ Título de sección productos</label><input id="eSectionTitle"></div>
    <div class="form-row"><label>📱 Número de WhatsApp (formato 57XXXXXXXXXX)</label><input id="eWhatsapp"></div>
    <div class="form-row"><label>🔊 URL de audio/música de fondo (mp3)</label><input id="eAudio"></div>
    <div class="form-row"><label>⭐ Reseñas (una por línea: Nombre|Estrellas|Texto)</label><textarea id="eReviews" rows="5"></textarea></div>
    <button class="btn-primary" onclick="saveSettingsPanel()">💾 Guardar cambios</button>
  </div>
</div>

<script>
/* ================= DATA ================= */
const DEPTOS = ["Amazonas","Antioquia","Arauca","Atlántico","Bolívar","Boyacá","Caldas","Caquetá","Casanare","Cauca","Cesar","Chocó","Córdoba","Cundinamarca","Guainía","Guaviare","Huila","La Guajira","Magdalena","Meta","Nariño","Norte de Santander","Putumayo","Quindío","Risaralda","San Andrés y Providencia","Santander","Sucre","Tolima","Valle del Cauca","Vaupés","Vichada","Bogotá D.C."];
const CIUDADES = ["Bogotá D.C.","Medellín","Cali","Barranquilla","Cartagena","Bucaramanga","Pereira","Manizales","Pasto","Montería","Leticia"];
const CATS = [
  {key:"Todo",emoji:"🛍️"},{key:"Hogar",emoji:"🏡"},{key:"Tecnología",emoji:"📱"},{key:"Salud",emoji:"💊"},
  {key:"Belleza",emoji:"💄"},{key:"Fitness",emoji:"🏋️"},{key:"Accesorios",emoji:"👜"},{key:"Juguetes",emoji:"🧸"},{key:"Cocina",emoji:"🍳"}
];

const DEFAULT_PRODUCTS = [
 {id:"p1",name:"Combo Reflectores Solares GD-077 30W",price:56000,oldPrice:0,category:"Hogar",image:"https://primoscolombia.com/cdn/shop/files/Copiade2lampara_panelsolarPOST.jpg?v=1758209691&width=533",mediaType:"image",badge:""},
 {id:"p2",name:"Combo Tapetes + Silicona de Cocina",price:60000,oldPrice:0,category:"Cocina",image:"https://primoscolombia.com/cdn/shop/files/COMBOCOCINAPOST_1.jpg?v=1759182830&width=533",mediaType:"image",badge:""},
 {id:"p3",name:"Combo Tapetes Cocina",price:35000,oldPrice:0,category:"Cocina",image:"https://primoscolombia.com/cdn/shop/files/TAPETECOCINAPOST.jpg?v=1759419569&width=533",mediaType:"image",badge:""},
 {id:"p4",name:"Combo Ventilador + Enfriador de Cuello",price:30000,oldPrice:0,category:"Hogar",image:"https://primoscolombia.com/cdn/shop/files/COMBOVENTILADOR_ENFRIADORDECUELLOPOST.jpg?v=1758213470&width=533",mediaType:"image",badge:""},
 {id:"p5",name:"Combo x3 Siliconas de Grifo Premium",price:45000,oldPrice:0,category:"Cocina",image:"https://primoscolombia.com/cdn/shop/files/SILICONAANTIDERRAMEPOST_1.jpg?v=1758648385&width=533",mediaType:"image",badge:""},
 {id:"p6",name:"Compresor de Llanta Premium",price:35000,oldPrice:0,category:"Accesorios",image:"https://primoscolombia.com/cdn/shop/files/INFLADORDELLANTASPOST.jpg?v=1758923643&width=533",mediaType:"image",badge:""},
 {id:"p7",name:"Consola Game Stick Premium",price:85000,oldPrice:0,category:"Tecnología",image:"https://primoscolombia.com/cdn/shop/files/EMULADORDEJUEGOSPOST_1.jpg?v=1759949115&width=533",mediaType:"image",badge:""},
 {id:"p8",name:"Consola Retro Classic F5",price:85000,oldPrice:0,category:"Tecnología",image:"https://primoscolombia.com/cdn/shop/files/JUEGOSUPPOST.jpg?v=1759174768&width=533",mediaType:"image",badge:""},
 {id:"p9",name:"Corrector de Juanete 556-1",price:22000,oldPrice:0,category:"Salud",image:"https://primoscolombia.com/cdn/shop/files/PIESS1POST.jpg?v=1759942360&width=533",mediaType:"image",badge:""},
 {id:"p10",name:"Corrector de Postura Inteligente",price:52000,oldPrice:0,category:"Salud",image:"https://primoscolombia.com/cdn/shop/files/MASAJEDORESPALDAPOST.jpg?v=1759958251&width=533",mediaType:"image",badge:""},
 {id:"p11",name:"Cortador Cocina 2 en 1 Cuchillo Tijeras",price:23000,oldPrice:0,category:"Cocina",image:"https://primoscolombia.com/cdn/shop/files/TIJERASMULTIPOST.jpg?v=1758562239&width=533",mediaType:"image",badge:""},
 {id:"p12",name:"Cosmetiquera con Espejo y Luz LED",price:69000,oldPrice:0,category:"Belleza",image:"https://primoscolombia.com/cdn/shop/files/COSMETIQUERAPOST.jpg?v=1758644869&width=533",mediaType:"image",badge:""},
 {id:"p13",name:"Cuello Inflable",price:45800,oldPrice:0,category:"Fitness",image:"https://primoscolombia.com/cdn/shop/files/CUELLO1.1POST.jpg?v=1759948059&width=533",mediaType:"image",badge:""},
 {id:"p14",name:"Cupping Premium 3 en 1",price:78900,oldPrice:0,category:"Salud",image:"https://primoscolombia.com/cdn/shop/files/MASAJEADOR1.1POST.jpg?v=1759957418&width=533",mediaType:"image",badge:""},
 {id:"p15",name:"Cupping Ventosa Eléctrica",price:45000,oldPrice:0,category:"Salud",image:"https://primoscolombia.com/cdn/shop/files/CUPPINGPOST.jpg?v=1758215014&width=533",mediaType:"image",badge:""},
 {id:"p16",name:"Depilador Yes Recargable",price:48000,oldPrice:0,category:"Belleza",image:"https://primoscolombia.com/cdn/shop/files/MAQUINADEPILADORMUJERPOST.jpg?v=1758316369&width=533",mediaType:"image",badge:""},
 {id:"p17",name:"Desmechador de Carne",price:25000,oldPrice:0,category:"Cocina",image:"https://primoscolombia.com/cdn/shop/files/DESMECHADORDEPOLLOPOST.jpg?v=1758306491&width=533",mediaType:"image",badge:""},
 {id:"p18",name:"Dilatador Nasal Magnético",price:24578,oldPrice:0,category:"Fitness",image:"https://primoscolombia.com/cdn/shop/files/nasal_POSTs.jpg?v=1762894565&width=533",mediaType:"image",badge:""},
 {id:"p19",name:"Dinosaurio con Control Remoto Premium",price:235000,oldPrice:0,category:"Juguetes",image:"https://primoscolombia.com/cdn/shop/files/DINNOSAURIOCONTROLREMOTOPOST.jpg?v=1758917112&width=533",mediaType:"image",badge:""},
 {id:"k1",name:"Kit Cabello de Salón en Casa",price:129900,oldPrice:155900,category:"Belleza",image:"https://primoscolombia.com/cdn/shop/files/PLANCHA2.2POST.jpg?v=1758554331&width=533",mediaType:"image",badge:"KIT"},
 {id:"k2",name:"Kit Skin Glow Facial",price:119900,oldPrice:151000,category:"Belleza",image:"https://primoscolombia.com/cdn/shop/files/MASAJEADORROSTROPOST.jpg?v=1758316793&width=533",mediaType:"image",badge:"KIT"},
 {id:"k3",name:"Kit Belleza Total (Spa Day)",price:99900,oldPrice:142000,category:"Belleza",image:"https://primoscolombia.com/cdn/shop/files/COSMETIQUERAPOST.jpg?v=1758644869&width=533",mediaType:"image",badge:"KIT"},
 {id:"k4",name:"Kit Glow Up Desde Adentro",price:119900,oldPrice:150789,category:"Belleza",image:"https://primoscolombia.com/cdn/shop/files/ANTISMOKEPARCHEPOST_2.jpg?v=1763150507&width=533",mediaType:"image",badge:"KIT"},
 {id:"k5",name:"Kit Depilación Sin Dolor",price:65900,oldPrice:76000,category:"Belleza",image:"https://primoscolombia.com/cdn/shop/files/MAQUINADEPILADORMUJERPOST.jpg?v=1758316369&width=533",mediaType:"image",badge:"KIT"}
];

const DEFAULT_SETTINGS = {
  marquee:"🇨🇴 Envíos a TODA Colombia | 💵 PAGO CONTRA ENTREGA | 📦 Interrapidísimo · Coordinadora · Envía | 🔒 Compra 100% segura | 🚚 Envío GRATIS en todos los productos",
  heroTitle:"Todo lo que necesitas|con envío GRATIS a Colombia",
  heroSub:"Bazar, belleza, hogar y tecnología. Paga cuando recibes tu pedido, sin riesgo.",
  sectionTitle:"🔥 Productos en Oferta",
  whatsapp:"573206572598",
  audio:"",
  reviews:"María P.|5|Llegó rapidísimo y pagué contra entrega, todo perfecto.\nCarlos R.|5|El kit de belleza superó mis expectativas, buena calidad.\nLuisa G.|4|Buen servicio, la app de WhatsApp fue muy fácil."
};

const HERO_SLIDES = [
  {eyebrow:"🇨🇴 Envío Gratis a Toda Colombia", useTitle:true, cta:"¡Ver ofertas!"},
  {eyebrow:"💵 Pago Contra Entrega", text:"Pagas cuando recibes tu pedido. Sin tarjeta, sin riesgo.", cta:"Comprar ahora"},
  {eyebrow:"📦 Recibe en 3 a 7 días", text:"Enviamos con Coordinadora, Interrapidísimo y Envía a todo el país.", cta:"Ver productos"}
];

/* ================= STATE ================= */
let products = loadJSON('ps_products', DEFAULT_PRODUCTS);
let settings = Object.assign({}, DEFAULT_SETTINGS, loadJSON('ps_settings', {}));
let orders = loadJSON('ps_orders', []);
let cart = loadJSON('ps_cart', {});
let activeCat = "Todo";
let slideIndex = 0;
let adminOK = sessionStorage.getItem('ps_admin_ok') === '1';
let pendingPanel = null;

function loadJSON(key,fallback){
  try{ const v = localStorage.getItem(key); return v? JSON.parse(v) : fallback; }catch(e){ return fallback; }
}
function saveJSON(key,val){ try{ localStorage.setItem(key, JSON.stringify(val)); }catch(e){ console.warn('storage full',e); } }
function money(n){ return '$' + Math.round(n).toLocaleString('es-CO'); }

/* ================= INIT ================= */
function init(){
  fillDeptoSelect(); fillCitySelect();
  renderMarquee(); renderHero(); renderCatNav(); renderProducts();
  renderReviews(); renderWaLinks(); renderAudio();
  updateCartBadge();
  setInterval(()=>{ nextSlide(); },5500);
}
function renderWaLinks(){
  const num = settings.whatsapp || "573206572598";
  const display = "+"+num.slice(0,2)+" "+num.slice(2,5)+" "+num.slice(5,8)+" "+num.slice(8);
  document.getElementById('waHeaderNum').textContent = display;
  document.getElementById('waHeaderBtn').href = "https://wa.me/"+num;
  document.getElementById('fabWa').href = "https://wa.me/"+num;
  document.getElementById('waFootIcon').href = "https://wa.me/"+num;
  document.getElementById('waFootText').textContent = "📞 "+display;
}
function renderAudio(){
  const a = document.getElementById('bgAudio');
  if(settings.audio){ a.src = settings.audio; }
}
function renderMarquee(){
  const parts = settings.marquee.split('|');
  const track = document.getElementById('marqueeTrack');
  track.innerHTML = parts.concat(parts).map(p=>`<span>${p.trim()}</span>`).join('');
}
function renderCatNav(){
  const nav = document.getElementById('catNav');
  nav.innerHTML = CATS.map(c=>`<button class="${c.key===activeCat?'active':''}" onclick="setCat('${c.key}')">${c.emoji} ${c.key}</button>`).join('');
}
function setCat(cat){ activeCat = cat; renderCatNav(); renderProducts(); }

function renderHero(){
  const wrap = document.getElementById('heroSlides');
  const titleParts = settings.heroTitle.split('|');
  wrap.innerHTML = HERO_SLIDES.map((s,i)=>{
    const html = s.useTitle
      ? `<h1>${titleParts[0]||''} <em>${titleParts[1]||''}</em></h1><p>${settings.heroSub}</p>`
      : `<h1>${s.text}</h1>`;
    return `<div class="hero-slide ${i===0?'active':''}" data-i="${i}">
      <span class="eyebrow">${s.eyebrow}</span>
      ${html}
      <button class="hero-cta" onclick="document.getElementById('products').scrollIntoView({behavior:'smooth'})">${s.cta}</button>
    </div>`;
  }).join('');
  const dots = document.getElementById('heroDots');
  dots.innerHTML = HERO_SLIDES.map((s,i)=>`<span class="${i===0?'active':''}" onclick="gotoSlide(${i})"></span>`).join('');
}
function gotoSlide(i){
  slideIndex = i;
  document.querySelectorAll('.hero-slide').forEach((el,idx)=>el.classList.toggle('active',idx===i));
  document.querySelectorAll('.hero-dots span').forEach((el,idx)=>el.classList.toggle('active',idx===i));
}
function nextSlide(){ gotoSlide((slideIndex+1)%HERO_SLIDES.length); }
function prevSlide(){ gotoSlide((slideIndex-1+HERO_SLIDES.length)%HERO_SLIDES.length); }

function renderProducts(){
  const term = (document.getElementById('searchInput').value||'').toLowerCase();
  const grid = document.getElementById('productGrid');
  const list = products.filter(p=>{
    const catOk = activeCat==="Todo" || p.category===activeCat;
    const searchOk = !term || p.name.toLowerCase().includes(term);
    return catOk && searchOk;
  });
  if(!list.length){ grid.innerHTML = `<p style="grid-column:1/-1;text-align:center;color:var(--ink-soft);">Sin resultados por ahora.</p>`; return; }
  grid.innerHTML = list.map(p=>{
    const off = p.oldPrice && p.oldPrice>p.price ? Math.round((1-p.price/p.oldPrice)*100) : 0;
    let mediaTag = '';
    if(p.mediaType==='video'){ mediaTag = `<video src="${p.image}" muted loop autoplay playsinline></video>`; }
    else { mediaTag = `<img src="${p.image}" alt="${p.name}" loading="lazy" width="300" height="300">`; }
    return `<div class="card">
      <div class="media">
        ${p.badge==='KIT'?'<span class="kit-flag">KIT</span>':''}
        ${off>0?`<span class="off-flag">-${off}%</span>`:''}
        ${mediaTag}
      </div>
      <div class="body">
        <span class="cat">${p.category}</span>
        <h3>${p.name}</h3>
        <div class="price-row">
          <span class="now mono">${money(p.price)}</span>
          ${off>0?`<span class="old mono">${money(p.oldPrice)}</span>`:''}
        </div>
        <button class="add-btn" onclick="addToCart('${p.id}',this)">Agregar al carrito</button>
      </div>
    </div>`;
  }).join('');
}
document.getElementById('searchInput').addEventListener('input',renderProducts);

/* ================= CART ================= */
function addToCart(id,btn){
  cart[id] = (cart[id]||0)+1;
  saveJSON('ps_cart',cart);
  updateCartBadge();
  if(btn){ btn.textContent='✔ Agregado'; btn.classList.add('added'); setTimeout(()=>{btn.textContent='Agregar al carrito';btn.classList.remove('added');},1100); }
}
function changeQty(id,delta){
  cart[id] = (cart[id]||0)+delta;
  if(cart[id]<=0) delete cart[id];
  saveJSON('ps_cart',cart);
  updateCartBadge(); renderCartItems();
}
function removeFromCart(id){ delete cart[id]; saveJSON('ps_cart',cart); updateCartBadge(); renderCartItems(); }
function cartCount(){ return Object.values(cart).reduce((a,b)=>a+b,0); }
function cartTotal(){
  return Object.entries(cart).reduce((sum,[id,qty])=>{
    const p = products.find(x=>x.id===id); return sum + (p? p.price*qty : 0);
  },0);
}
function updateCartBadge(){
  const c = cartCount();
  document.getElementById('cartBadge').textContent = c;
  document.getElementById('fabCartBadge').textContent = c;
}
function renderCartItems(){
  const wrap = document.getElementById('cartItemsWrap');
  const entries = Object.entries(cart);
  if(!entries.length){ wrap.innerHTML = `<p style="color:var(--ink-soft);text-align:center;padding:20px 0;">Tu carrito está vacío.</p>`; }
  else{
    wrap.innerHTML = entries.map(([id,qty])=>{
      const p = products.find(x=>x.id===id);
      if(!p) return '';
      return `<div class="cart-item">
        <img src="${p.image}" alt="${p.name}">
        <div class="ci-info">
          <h4>${p.name}</h4>
          <div class="qty-ctrl">
            <button onclick="changeQty('${id}',-1)">−</button><span class="mono">${qty}</span><button onclick="changeQty('${id}',1)">+</button>
            <span class="mono" style="margin-left:auto;">${money(p.price*qty)}</span>
          </div>
        </div>
        <button class="remove-x" onclick="removeFromCart('${id}')">✕</button>
      </div>`;
    }).join('');
  }
  document.getElementById('cartTotal').textContent = money(cartTotal());
}
document.getElementById('cartIconBtn').onclick = ()=>{ renderCartItems(); openModal('cartOverlay'); };
document.getElementById('fabCartBtn').onclick = ()=>{ renderCartItems(); openModal('cartOverlay'); };

/* ================= CHECKOUT ================= */
function fillDeptoSelect(){
  document.getElementById('ckDepto').innerHTML = '<option value="">-- Selecciona --</option>' + DEPTOS.map(d=>`<option>${d}</option>`).join('');
}
function fillCitySelect(){
  document.getElementById('citySelect').innerHTML += CIUDADES.map(c=>`<option>${c}</option>`).join('');
}
function openCheckout(){
  if(!cartCount()){ alert('Tu carrito está vacío.'); return; }
  closeModal('cartOverlay'); openModal('checkoutOverlay');
}
function submitOrder(e){
  e.preventDefault();
  const nombre=document.getElementById('ckNombre').value, apellido=document.getElementById('ckApellido').value;
  const depto=document.getElementById('ckDepto').value, ciudad=document.getElementById('ckCiudad').value;
  const direccion=document.getElementById('ckDireccion').value, telefono=document.getElementById('ckTelefono').value;
  const nota=document.getElementById('ckNota').value;
  const items = Object.entries(cart).map(([id,qty])=>{
    const p=products.find(x=>x.id===id); return p? {name:p.name,qty,price:p.price,subtotal:p.price*qty} : null;
  }).filter(Boolean);
  const total = cartTotal();
  const order = {date:new Date().toISOString(),nombre,apellido,depto,ciudad,direccion,telefono,nota,items,total};
  orders.push(order); saveJSON('ps_orders',orders);

  let msg = `🛒 *Nuevo pedido PRIMOSTORE*\n\n👤 ${nombre} ${apellido}\n📍 ${direccion}, ${ciudad}, ${depto}\n📞 ${telefono}\n`;
  if(nota) msg += `📝 Nota: ${nota}\n`;
  msg += `\n*Productos:*\n`;
  items.forEach(it=>{ msg += `• ${it.qty}x ${it.name} — ${money(it.subtotal)}\n`; });
  msg += `\n*Total: ${money(total)}*\n💵 Pago contra entrega`;

  window.open("https://wa.me/"+(settings.whatsapp||"573206572598")+"?text="+encodeURIComponent(msg),"_blank");
  cart = {}; saveJSON('ps_cart',cart); updateCartBadge();
  closeModal('checkoutOverlay');
  document.getElementById('checkoutForm').reset();
}

/* ================= DELIVERY CALCULATOR ================= */
function calcularFecha(){
  const city = document.getElementById('citySelect').value;
  const result = document.getElementById('calcResult');
  if(!city){ result.textContent = 'Selecciona una ciudad primero.'; return; }
  const mainCities = ["Bogotá D.C.","Medellín","Cali","Barranquilla"];
  const minDays = mainCities.includes(city) ? 3 : 4;
  const maxDays = mainCities.includes(city) ? 5 : 7;
  const d1 = new Date(); d1.setDate(d1.getDate()+minDays);
  const d2 = new Date(); d2.setDate(d2.getDate()+maxDays);
  const opts = {day:'numeric',month:'long'};
  result.textContent = `📦 Tu pedido a ${city} llega entre el ${d1.toLocaleDateString('es-CO',opts)} y el ${d2.toLocaleDateString('es-CO',opts)}.`;
}

/* ================= REVIEWS ================= */
function renderReviews(){
  const lines = settings.reviews.split('\n').filter(Boolean);
  const strip = document.getElementById('reviewsStrip');
  strip.innerHTML = lines.map(l=>{
    const [who,stars,text] = l.split('|');
    return `<div class="review-card">
      <div class="stars">${'★'.repeat(parseInt(stars)||5)}${'☆'.repeat(5-(parseInt(stars)||5))}</div>
      <p>"${text||''}"</p>
      <div class="who">${who||'Cliente'}</div>
    </div>`;
  }).join('');
}

/* ================= WHEEL ================= */
const PRIZES = [
  {label:"5% OFF",angle:30},{label:"10% OFF",angle:90},{label:"Envío VIP",angle:150},
  {label:"Otra vez",angle:210},{label:"15% OFF",angle:270},{label:"20% OFF",angle:330}
];
function renderWheelLabels(){
  const wrap = document.getElementById('wheelLabels');
  wrap.innerHTML = PRIZES.map(p=>{
    const rad = (p.angle-90) * Math.PI/180;
    const x = 110 + 70*Math.cos(rad), y = 110 + 70*Math.sin(rad);
    return `<span style="left:${x}px;top:${y}px;transform:translate(-50%,-50%) rotate(${p.angle}deg);">${p.label}</span>`;
  }).join('');
}
let wheelSpinning = false;
function spinWheel(){
  if(wheelSpinning) return;
  wheelSpinning = true;
  const wheel = document.getElementById('wheelEl');
  const chosen = PRIZES[Math.floor(Math.random()*PRIZES.length)];
  const extraTurns = 5*360;
  const finalRotation = extraTurns + (360 - chosen.angle);
  wheel.style.transform = `rotate(${finalRotation}deg)`;
  document.getElementById('wheelResult').textContent = '';
  setTimeout(()=>{
    document.getElementById('wheelResult').textContent = `🎉 ¡Ganaste: ${chosen.label}! Menciónalo al confirmar tu pedido por WhatsApp.`;
    wheelSpinning = false;
  },4100);
}
document.getElementById('fabWa').addEventListener('dblclick',()=>{ /* easter egg not needed */ });

/* ================= MODALS ================= */
function openModal(id){ document.getElementById(id).classList.add('show'); }
function closeModal(id){ document.getElementById(id).classList.remove('show'); }
document.querySelectorAll('.overlay').forEach(o=>{
  o.addEventListener('click',e=>{ if(e.target===o) o.classList.remove('show'); });
});

/* ================= ADMIN ================= */
function openAdmin(panel){
  pendingPanel = panel;
  if(adminOK){ launchPanel(panel); return; }
  document.getElementById('pwInput').value='';
  openModal('pwOverlay');
}
function checkPassword(){
  const val = document.getElementById('pwInput').value;
  if(val === '4321'){
    adminOK = true; sessionStorage.setItem('ps_admin_ok','1');
    closeModal('pwOverlay'); launchPanel(pendingPanel);
  } else { alert('Contraseña incorrecta'); }
}
function launchPanel(panel){
  if(panel==='R'){ renderAdminProducts(); openModal('adminROverlay'); }
  else if(panel==='C'){ renderAdminOrders(); openModal('adminCOverlay'); }
  else if(panel==='E'){ fillAdminSettingsForm(); openModal('adminEOverlay'); }
}

/* --- R: products editor --- */
function renderAdminProducts(){
  const wrap = document.getElementById('adminProductList');
  wrap.innerHTML = products.map((p,idx)=>{
    let preview = p.mediaType==='video' ? `<video src="${p.image}" muted></video>` : `<img src="${p.image}">`;
    return `<div class="admin-product-row" data-idx="${idx}">
      <div class="arow-top">
        ${preview}
        <div class="arow-fields">
          <input value="${p.name.replace(/"/g,'&quot;')}" oninput="updateProdField(${idx},'name',this.value)" placeholder="Nombre">
          <select onchange="updateProdField(${idx},'category',this.value)">
            ${CATS.filter(c=>c.key!=='Todo').map(c=>`<option ${c.key===p.category?'selected':''}>${c.key}</option>`).join('')}
          </select>
          <input type="number" value="${p.price}" oninput="updateProdField(${idx},'price',parseFloat(this.value)||0)" placeholder="Precio">
          <input type="number" value="${p.oldPrice||0}" oninput="updateProdField(${idx},'oldPrice',parseFloat(this.value)||0)" placeholder="Precio anterior (opcional)">
          <input value="${p.image}" oninput="updateProdField(${idx},'image',this.value)" placeholder="URL imagen/video/gif" style="grid-column:1/-1;">
          <label style="grid-column:1/-1;font-size:.7rem;">📁 Subir desde galería (imagen/video/gif):
            <input type="file" accept="image/*,video/*" onchange="handleFileUpload(event,${idx})">
          </label>
          <select onchange="updateProdField(${idx},'mediaType',this.value)" style="grid-column:1/-1;">
            <option value="image" ${p.mediaType==='image'?'selected':''}>Imagen / GIF</option>
            <option value="video" ${p.mediaType==='video'?'selected':''}>Video</option>
          </select>
        </div>
      </div>
      <button class="del-btn" onclick="deleteProduct(${idx})">🗑️ Eliminar producto</button>
    </div>`;
  }).join('');
}
function updateProdField(idx,field,value){ products[idx][field] = value; }
function handleFileUpload(evt,idx){
  const file = evt.target.files[0];
  if(!file) return;
  const reader = new FileReader();
  reader.onload = ()=>{
    products[idx].image = reader.result;
    products[idx].mediaType = file.type.startsWith('video') ? 'video' : 'image';
    renderAdminProducts();
  };
  reader.readAsDataURL(file);
}
function addNewProduct(){
  products.push({id:'p'+Date.now(),name:'Nuevo producto',price:0,oldPrice:0,category:'Hogar',image:'',mediaType:'image',badge:''});
  renderAdminProducts();
}
function deleteProduct(idx){
  if(!confirm('¿Eliminar este producto?')) return;
  products.splice(idx,1); renderAdminProducts();
}
function saveAllProducts(){
  saveJSON('ps_products',products);
  renderProducts();
  alert('Productos guardados ✅');
}

/* --- C: orders --- */
function renderAdminOrders(){
  const table = document.getElementById('ordersTable');
  if(!orders.length){ table.innerHTML = '<tr><td>No hay pedidos aún.</td></tr>'; return; }
  let rows = '<tr><th>Fecha</th><th>Cliente</th><th>Ciudad</th><th>Teléfono</th><th>Productos</th><th>Total</th></tr>';
  orders.slice().reverse().forEach(o=>{
    const itemsStr = o.items.map(it=>`${it.qty}x ${it.name}`).join(', ');
    rows += `<tr><td>${new Date(o.date).toLocaleString('es-CO')}</td><td>${o.nombre} ${o.apellido}</td><td>${o.ciudad}, ${o.depto}</td><td>${o.telefono}</td><td>${itemsStr}</td><td>${money(o.total)}</td></tr>`;
  });
  table.innerHTML = rows;
}
function exportOrdersCSV(){
  if(!orders.length){ alert('No hay pedidos para exportar.'); return; }
  let csv = 'Fecha,Nombre,Apellido,Departamento,Ciudad,Direccion,Telefono,Nota,Productos,Total\n';
  orders.forEach(o=>{
    const itemsStr = o.items.map(it=>`${it.qty}x ${it.name}`).join(' | ');
    csv += [o.date,o.nombre,o.apellido,o.depto,o.ciudad,o.direccion,o.telefono,(o.nota||''),itemsStr,o.total]
      .map(v=>`"${String(v).replace(/"/g,'""')}"`).join(',') + '\n';
  });
  const blob = new Blob([csv],{type:'text/csv;charset=utf-8;'});
  const a = document.createElement('a');
  a.href = URL.createObjectURL(blob); a.download = 'pedidos_primostore.csv'; a.click();
}
function clearOrders(){
  if(!confirm('¿Borrar todos los pedidos?')) return;
  orders = []; saveJSON('ps_orders',orders); renderAdminOrders();
}

/* --- E: page editor --- */
function fillAdminSettingsForm(){
  document.getElementById('eMarquee').value = settings.marquee;
  document.getElementById('eHeroTitle').value = settings.heroTitle;
  document.getElementById('eHeroSub').value = settings.heroSub;
  document.getElementById('eSectionTitle').value = settings.sectionTitle;
  document.getElementById('eWhatsapp').value = settings.whatsapp;
  document.getElementById('eAudio').value = settings.audio;
  document.getElementById('eReviews').value = settings.reviews;
}
function saveSettingsPanel(){
  settings.marquee = document.getElementById('eMarquee').value;
  settings.heroTitle = document.getElementById('eHeroTitle').value;
  settings.heroSub = document.getElementById('eHeroSub').value;
  settings.sectionTitle = document.getElementById('eSectionTitle').value;
  settings.whatsapp = document.getElementById('eWhatsapp').value.replace(/\D/g,'');
  settings.audio = document.getElementById('eAudio').value;
  settings.reviews = document.getElementById('eReviews').value;
  saveJSON('ps_settings',settings);
  document.getElementById('sectionTitleText').textContent = settings.sectionTitle;
  renderMarquee(); renderHero(); renderReviews(); renderWaLinks(); renderAudio();
  alert('Página actualizada ✅');
  closeModal('adminEOverlay');
}

/* ================= START ================= */
renderWheelLabels();
init();
</script>
</body>
</html>

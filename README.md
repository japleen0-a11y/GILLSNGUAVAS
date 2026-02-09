<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gills N Guavas</title>
  <style>
    :root{
      --bg:#fbfaf6;
      --card:rgba(255,255,255,.85);
      --card2:rgba(255,255,255,.72);
      --text:#0f172a;
      --muted:#475569;
      --muted2:#64748b;
      --ring:rgba(15,23,42,.10);
      --shadow:0 10px 25px rgba(15,23,42,.06);
      --emerald:#14532d;
      --emerald2:#1f7a44;
      --soft:#ecfdf5;
      --softRing:#d1fae5;
      --rose:#e11d48;
      --btn:#0b3a1f;
      --btnHover:#0e4a28;
      --white:#ffffff;
    }
    *{box-sizing:border-box}
    html,body{margin:0;padding:0;font-family:system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,Cantarell,Noto Sans,sans-serif;color:var(--text);background:var(--bg)}
    a{color:inherit;text-decoration:none}
    img{max-width:100%;display:block}
    .container{max-width:1120px;margin:0 auto;padding:0 16px}
    .shadow{box-shadow:var(--shadow)}
    .ring{border:1px solid var(--ring)}
    .round-xl{border-radius:14px}
    .round-2xl{border-radius:20px}
    .round-3xl{border-radius:28px}
    .btn{display:inline-flex;align-items:center;justify-content:center;gap:10px;border:0;border-radius:18px;padding:12px 16px;font-weight:700;cursor:pointer;transition:.15s}
    .btn:active{transform:scale(.99)}
    .btn-primary{background:var(--emerald);color:#fff}
    .btn-primary:hover{background:var(--btnHover)}
    .btn-wa{background:var(--emerald2);color:#fff}
    .btn-wa:hover{opacity:.95}
    .btn-ghost{background:rgba(255,255,255,.85);border:1px solid var(--ring);color:var(--text)}
    .btn-ghost:hover{background:#fff}
    .pill{display:inline-flex;align-items:center;border-radius:999px;background:#f1f5f9;padding:6px 10px;font-size:12px;font-weight:600;color:#334155;gap:8px}
    .kicker{display:inline-flex;align-items:center;gap:8px;border-radius:999px;background:var(--soft);border:1px solid var(--softRing);padding:6px 10px;font-size:13px;font-weight:700;color:var(--emerald)}
    .section{padding:56px 0}
    .section.soft{background:rgba(255,255,255,.55);border-top:1px solid rgba(15,23,42,.06);border-bottom:1px solid rgba(15,23,42,.06)}
    h1{font-size:40px;line-height:1.1;margin:14px 0 0}
    h2{font-size:32px;line-height:1.15;margin:12px 0 0}
    p{margin:10px 0 0;color:var(--muted)}
    .grid{display:grid;gap:16px}
    .grid-2{grid-template-columns:repeat(2,minmax(0,1fr))}
    .grid-3{grid-template-columns:repeat(3,minmax(0,1fr))}
    .grid-4{grid-template-columns:repeat(4,minmax(0,1fr))}
    @media (max-width: 980px){.grid-4{grid-template-columns:repeat(2,minmax(0,1fr))}}
    @media (max-width: 820px){.grid-3{grid-template-columns:repeat(2,minmax(0,1fr))}}
    @media (max-width: 640px){h1{font-size:34px}h2{font-size:28px}.grid-2,.grid-3,.grid-4{grid-template-columns:1fr}}
    .topbar-wrap{position:sticky;top:0;z-index:50}
    .topbar{background:rgba(255,255,255,.72);backdrop-filter:blur(10px);border-bottom:1px solid rgba(15,23,42,.10)}
    .topbar-inner{display:flex;align-items:center;justify-content:space-between;padding:12px 0;gap:12px}
    .brand{display:flex;align-items:center;gap:10px}
    .logo{height:40px;width:40px;border-radius:16px;background:rgba(255,255,255,.8);border:1px solid var(--ring);overflow:hidden;display:flex;align-items:center;justify-content:center}
    .brand-title{font-weight:800}
    .brand-sub{font-size:12px;color:var(--muted2)}
    .navlinks{display:flex;gap:6px;flex-wrap:wrap}
    .navlinks button{background:transparent;border:1px solid transparent;border-radius:14px;padding:10px 12px;font-weight:700;color:#334155;cursor:pointer}
    .navlinks button:hover{background:#fff;border-color:var(--ring)}
    @media (max-width: 820px){.navlinks{display:none}}
    .cart-btn{position:relative}
    .badge{position:absolute;top:-8px;right:-8px;background:var(--rose);color:#fff;border-radius:999px;font-size:12px;font-weight:800;min-width:24px;height:24px;padding:0 6px;display:flex;align-items:center;justify-content:center}
    .hero{position:relative;overflow:hidden}
    .hero-bg{position:absolute;inset:0;background-size:cover;background-position:center;filter:saturate(1.05)}
    .hero-overlay{position:absolute;inset:0;background:linear-gradient(180deg, rgba(251,250,246,.92), rgba(251,250,246,.55))}
    .hero-inner{position:relative;padding:64px 0}
    .hero-grid{display:grid;grid-template-columns:1.1fr .9fr;gap:28px;align-items:center}
    @media (max-width: 980px){.hero-grid{grid-template-columns:1fr}}
    .card{background:var(--card);border:1px solid var(--ring);border-radius:28px;box-shadow:var(--shadow)}
    .card2{background:var(--card2);border:1px solid var(--ring);border-radius:28px;box-shadow:var(--shadow)}
    .card-pad{padding:18px}
    .feature-row{display:flex;gap:12px;align-items:center}
    .ic{width:38px;height:38px;border-radius:14px;background:var(--soft);border:1px solid var(--softRing);display:flex;align-items:center;justify-content:center}
    .ic svg{width:18px;height:18px;fill:none;stroke:var(--emerald);stroke-width:2}
    .meta{font-size:13px;color:var(--muted2)}
    .filters{display:flex;gap:10px;flex-wrap:wrap;align-items:center;justify-content:space-between}
    .cats{display:flex;gap:8px;flex-wrap:wrap}
    .chip{border-radius:999px;padding:10px 14px;font-weight:800;font-size:13px;border:1px solid var(--ring);background:rgba(255,255,255,.75);cursor:pointer}
    .chip.active{background:var(--emerald);border-color:var(--emerald);color:#fff}
    .search{position:relative;min-width:260px;max-width:340px;width:100%}
    .search input{width:100%;padding:12px 14px 12px 40px;border-radius:18px;border:1px solid var(--ring);background:rgba(255,255,255,.8);outline:none}
    .search svg{position:absolute;left:12px;top:50%;transform:translateY(-50%);width:16px;height:16px;stroke:#64748b;stroke-width:2;fill:none}
    .prod{display:flex;flex-direction:column;overflow:hidden}
    .prod img{height:176px;object-fit:cover}
    .prod-body{padding:18px;display:flex;flex-direction:column;gap:10px}
    .prod-top{display:flex;justify-content:space-between;gap:10px}
    .prod-name{font-weight:900}
    .prod-size{font-size:13px;color:var(--muted2);margin-top:4px}
    .price{font-weight:900;color:var(--emerald);font-size:18px}
    .prod-tags{display:flex;gap:8px;flex-wrap:wrap}
    .prod-bottom{margin-top:6px;display:flex;gap:10px}
    .prod-bottom .btn{flex:1}
    .badgeTag{position:absolute;left:12px;top:12px;background:rgba(255,255,255,.88);border:1px solid var(--ring);border-radius:999px;padding:6px 10px;font-size:12px;font-weight:900;color:#334155}
    .rel{position:relative}
    .timeline .step{display:flex;gap:12px;align-items:flex-start}
    .num{height:36px;width:36px;border-radius:16px;background:var(--emerald);color:#fff;font-weight:900;display:flex;align-items:center;justify-content:center}
    .faq-item{overflow:hidden}
    .faq-q{width:100%;text-align:left;display:flex;justify-content:space-between;gap:10px;align-items:center;background:transparent;border:0;padding:16px 18px;font-weight:900;cursor:pointer}
    .faq-a{padding:0 18px 16px 18px;color:var(--muted);font-size:14px;display:none}
    .faq-item.open .faq-a{display:block}
    .caret{width:18px;height:18px;stroke:#64748b;stroke-width:2;fill:none;transition:.15s}
    .faq-item.open .caret{transform:rotate(180deg)}
    .footer{border-top:1px solid rgba(15,23,42,.10);padding:34px 0}
    .small{font-size:12px;color:var(--muted2)}
    /* Drawer */
    .overlay{position:fixed;inset:0;background:rgba(0,0,0,.35);z-index:70;display:none}
    .drawer{position:fixed;top:0;right:0;bottom:0;width:100%;max-width:420px;background:var(--bg);border-left:1px solid rgba(15,23,42,.10);z-index:80;transform:translateX(440px);transition:transform .25s ease;box-shadow:0 20px 40px rgba(0,0,0,.18)}
    .drawer.open{transform:translateX(0)}
    .overlay.open{display:block}
    .drawer-head{padding:18px;border-bottom:1px solid rgba(15,23,42,.10);display:flex;justify-content:space-between;gap:10px;align-items:center}
    .drawer-body{padding:18px;overflow:auto;height:calc(100% - 210px)}
    .drawer-foot{padding:18px;border-top:1px solid rgba(15,23,42,.10)}
    .cart-item{display:flex;gap:12px}
    .cart-item img{width:80px;height:64px;border-radius:14px;object-fit:cover;border:1px solid var(--ring)}
    .cart-row{display:flex;justify-content:space-between;align-items:center;gap:10px;margin-top:10px}
    .stepper{display:inline-flex;align-items:center;gap:10px;padding:6px 8px;border-radius:14px;background:rgba(241,245,249,.9);border:1px solid var(--ring)}
    .stepper button{border:0;background:#fff;border:1px solid var(--ring);width:28px;height:28px;border-radius:10px;cursor:pointer;font-weight:900}
    .stepper span{min-width:18px;text-align:center;font-weight:900}
    .toast{position:fixed;left:50%;bottom:18px;transform:translateX(-50%);background:#0f172a;color:#fff;padding:10px 14px;border-radius:16px;font-size:13px;z-index:90;display:none;box-shadow:0 12px 30px rgba(0,0,0,.25)}
    .toast.show{display:block}
    /* Simple inline icon strokes */
    svg.i{width:18px;height:18px;fill:none;stroke:currentColor;stroke-width:2;stroke-linecap:round;stroke-linejoin:round}
  </style>
</head>

<body>
  <div class="topbar-wrap">
    <div class="topbar">
      <div class="container">
        <div class="topbar-inner">
          <button class="brand" id="jumpTop" style="background:transparent;border:0;cursor:pointer">
            <div class="logo"><img id="logoImg" alt="logo" /></div>
            <div style="text-align:left;line-height:1.1">
              <div class="brand-title">Gills N Guavas</div>
              <div class="brand-sub">Guava, made right</div>
            </div>
          </button>

          <div class="navlinks">
            <button data-jump="shop">Shop</button>
            <button data-jump="values">Why Us</button>
            <button data-jump="process">Process</button>
            <button data-jump="reviews">Reviews</button>
            <button data-jump="faq">FAQ</button>
            <button data-jump="contact">Contact</button>
          </div>

          <button class="btn btn-primary cart-btn" id="openCart">
            <!-- shopping-bag -->
            <svg class="i" viewBox="0 0 24 24" aria-hidden="true"><path d="M6 2l1.5 2H20l-2 9H7L5 4"/><path d="M7 13l-1 9h14l-1-9"/><path d="M9 22a1 1 0 1 0 0-2 1 1 0 0 0 0 2z"/><path d="M18 22a1 1 0 1 0 0-2 1 1 0 0 0 0 2z"/></svg>
            Cart
            <span class="badge" id="cartBadge" style="display:none">0</span>
          </button>
        </div>
      </div>
    </div>
  </div>

  <!-- HERO -->
  <header class="hero" id="top">
    <div class="hero-bg" id="heroBg"></div>
    <div class="hero-overlay"></div>

    <div class="container hero-inner">
      <div class="hero-grid">
        <div>
          <div class="kicker">
            <!-- sparkles -->
            <svg class="i" viewBox="0 0 24 24"><path d="M12 3l1.2 4.2L18 9l-4.8 1.8L12 15l-1.2-4.2L6 9l4.8-1.8L12 3z"/><path d="M5 3l.7 2.2L8 6l-2.3.8L5 9l-.7-2.2L2 6l2.3-.8L5 3z"/><path d="M19 13l.7 2.2L22 16l-2.3.8L19 19l-.7-2.2L16 16l2.3-.8L19 13z"/></svg>
            Small-batch • Fresh guava • Premium quality
          </div>

          <h1>Guava, made the right way.</h1>
          <p style="max-width:560px">
            <b style="color:var(--text)">Gills N Guavas</b> crafts guava products with care—fresh fruit,
            simple ingredients, and no shortcuts.
          </p>

          <div style="margin-top:18px;display:flex;gap:10px;flex-wrap:wrap">
            <button class="btn btn-primary" data-jump="shop">Shop products</button>
            <button class="btn btn-ghost" data-jump="process">Explore our process</button>
            <a class="btn btn-wa" id="heroWA" href="#" target="_blank" rel="noreferrer">Order on WhatsApp</a>
          </div>

          <div class="grid grid-3" style="margin-top:22px">
            <div class="card2 card-pad">
              <div class="feature-row">
                <div class="ic">
                  <!-- shield-check -->
                  <svg class="i" viewBox="0 0 24 24"><path d="M12 2l7 4v6c0 5-3 9-7 10-4-1-7-5-7-10V6l7-4z"/><path d="M9 12l2 2 4-4"/></svg>
                </div>
                <div>
                  <div style="font-weight:900">No artificial colours</div>
                  <div class="meta">Clean labels, honest taste.</div>
                </div>
              </div>
            </div>

            <div class="card2 card-pad">
              <div class="feature-row">
                <div class="ic">
                  <!-- badge-check -->
                  <svg class="i" viewBox="0 0 24 24"><path d="M12 2l3 5 6 1-4 4 1 6-6-3-6 3 1-6-4-4 6-1 3-5z"/><path d="M9 12l2 2 4-4"/></svg>
                </div>
                <div>
                  <div style="font-weight:900">Quality checked</div>
                  <div class="meta">Every batch is tasted.</div>
                </div>
              </div>
            </div>

            <div class="card2 card-pad">
              <div class="feature-row">
                <div class="ic">
                  <!-- truck -->
                  <svg class="i" viewBox="0 0 24 24"><path d="M3 7h11v10H3z"/><path d="M14 10h4l3 3v4h-7z"/><path d="M7 17a2 2 0 1 0 0 4 2 2 0 0 0 0-4z"/><path d="M17 17a2 2 0 1 0 0 4 2 2 0 0 0 0-4z"/></svg>
                </div>
                <div>
                  <div style="font-weight:900">Ship-ready packs</div>
                  <div class="meta">Sturdy packaging for delivery.</div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Featured card -->
        <div class="card">
          <div style="padding:18px;border-bottom:1px solid rgba(15,23,42,.10);display:flex;justify-content:space-between;align-items:center;gap:10px">
            <div>
              <div style="font-weight:900">Featured</div>
              <div class="small">Try our bestsellers</div>
            </div>
            <span class="pill">Premium</span>
          </div>

          <div style="padding:18px" id="featuredList"></div>

          <div style="padding:0 18px 18px 18px">
            <div style="background:var(--soft);border:1px solid var(--softRing);border-radius:20px;padding:14px">
              <div class="feature-row" style="align-items:flex-start">
                <div class="ic" style="background:#fff;border-color:var(--softRing)">
                  <svg class="i" viewBox="0 0 24 24" style="color:var(--emerald)"><path d="M12 3l1.2 4.2L18 9l-4.8 1.8L12 15l-1.2-4.2L6 9l4.8-1.8L12 3z"/><path d="M5 3l.7 2.2L8 6l-2.3.8L5 9l-.7-2.2L2 6l2.3-.8L5 3z"/><path d="M19 13l.7 2.2L22 16l-2.3.8L19 19l-.7-2.2L16 16l2.3-.8L19 13z"/></svg>
                </div>
                <div>
                  <div style="font-weight:900">Launch tip for your brand</div>
                  <div class="meta" style="margin-top:4px;color:#0f172a">
                    Start with 3 SKUs, focus on reviews, then expand. Keep packaging premium.
                  </div>
                </div>
              </div>
            </div>
          </div>

        </div>
      </div>
    </div>
  </header>

  <!-- SHOP -->
  <section class="section" id="shop">
    <div class="container">
      <div style="max-width:640px">
        <div class="kicker">
          <svg class="i" viewBox="0 0 24 24"><path d="M12 2c-2 4-2 7 0 10 2-3 2-6 0-10z"/><path d="M4 12c4 0 7 2 10 6-4 0-7-2-10-6z"/><path d="M20 12c-4 0-7 2-10 6 4 0 7-2 10-6z"/></svg>
          Shop
        </div>
        <h2>Pick your guava favourites</h2>
        <p>Use the filters to explore products. Add to cart and order instantly on WhatsApp.</p>
      </div>

      <div class="filters" style="margin-top:18px">
        <div class="cats" id="cats"></div>

        <div class="search">
          <svg viewBox="0 0 24 24"><circle cx="11" cy="11" r="7"></circle><path d="M20 20l-3.2-3.2"></path></svg>
          <input id="searchInput" placeholder="Search (jam, chutney, 200g...)" />
        </div>
      </div>

      <div class="grid grid-3" style="margin-top:18px" id="productGrid"></div>
    </div>
  </section>

  <!-- VALUES -->
  <section class="section soft" id="values">
    <div class="container">
      <div style="max-width:640px">
        <div class="kicker">
          <svg class="i" viewBox="0 0 24 24"><path d="M12 2c-2 4-2 7 0 10 2-3 2-6 0-10z"/><path d="M4 12c4 0 7 2 10 6-4 0-7-2-10-6z"/><path d="M20 12c-4 0-7 2-10 6 4 0 7-2 10-6z"/></svg>
          Why us
        </div>
        <h2>Simple ingredients. Serious care.</h2>
        <p>Position your brand as premium with honest claims you can stand behind.</p>
      </div>

      <div class="grid grid-4" style="margin-top:18px">
        <div class="card2 card-pad">
          <div class="feature-row">
            <div class="ic"><svg class="i" viewBox="0 0 24 24"><path d="M12 2c-2 4-2 7 0 10 2-3 2-6 0-10z"/><path d="M4 12c4 0 7 2 10 6-4 0-7-2-10-6z"/></svg></div>
            <div><div style="font-weight:900">Fresh guava only</div><div class="meta">Sourced and processed with care.</div></div>
          </div>
        </div>
        <div class="card2 card-pad">
          <div class="feature-row">
            <div class="ic"><svg class="i" viewBox="0 0 24 24"><path d="M12 3l1.2 4.2L18 9l-4.8 1.8L12 15l-1.2-4.2L6 9l4.8-1.8L12 3z"/></svg></div>
            <div><div style="font-weight:900">Small batch cooking</div><div class="meta">Better taste and texture.</div></div>
          </div>
        </div>
        <div class="card2 card-pad">
          <div class="feature-row">
            <div class="ic"><svg class="i" viewBox="0 0 24 24"><path d="M12 2l7 4v6c0 5-3 9-7 10-4-1-7-5-7-10V6l7-4z"/><path d="M9 12l2 2 4-4"/></svg></div>
            <div><div style="font-weight:900">Clean & safe</div><div class="meta">Hygiene-first workspace.</div></div>
          </div>
        </div>
        <div class="card2 card-pad">
          <div class="feature-row">
            <div class="ic"><svg class="i" viewBox="0 0 24 24"><path d="M3 7h11v10H3z"/><path d="M14 10h4l3 3v4h-7z"/></svg></div>
            <div><div style="font-weight:900">Packed for travel</div><div class="meta">Designed for shipping & gifting.</div></div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- PROCESS -->
  <section class="section" id="process">
    <div class="container">
      <div style="max-width:640px">
        <div class="kicker">
          <svg class="i" viewBox="0 0 24 24"><path d="M12 2c-2 4-2 7 0 10 2-3 2-6 0-10z"/><path d="M4 12c4 0 7 2 10 6-4 0-7-2-10-6z"/></svg>
          Our process
        </div>
        <h2>From fruit to jar</h2>
        <p>A simple, believable process page builds trust and boosts conversions.</p>
      </div>

      <div class="grid grid-2" style="margin-top:18px">
        <div class="card2 card-pad">
          <div style="font-weight:900">Our promise</div>
          <p style="margin-top:8px">
            We keep processes simple and honest—so you can maintain quality easily as you scale.
          </p>
          <div class="grid" style="margin-top:14px">
            <div class="card2 card-pad" style="box-shadow:none">
              <div class="feature-row">
                <div class="ic"><svg class="i" viewBox="0 0 24 24"><path d="M12 2l7 4v6c0 5-3 9-7 10-4-1-7-5-7-10V6l7-4z"/><path d="M9 12l2 2 4-4"/></svg></div>
                <div><div style="font-weight:900">Quality-first</div><div class="meta">Taste + texture checks every batch.</div></div>
              </div>
            </div>
            <div class="card2 card-pad" style="box-shadow:none">
              <div class="feature-row">
                <div class="ic"><svg class="i" viewBox="0 0 24 24"><path d="M12 2c-2 4-2 7 0 10 2-3 2-6 0-10z"/><path d="M4 12c4 0 7 2 10 6-4 0-7-2-10-6z"/></svg></div>
                <div><div style="font-weight:900">Ingredient clarity</div><div class="meta">Simple ingredients customers understand.</div></div>
              </div>
            </div>
          </div>
        </div>

        <div class="grid timeline">
          <div class="card2 card-pad step">
            <div class="num">1</div>
            <div><div style="font-weight:900">Select fresh guavas</div><div class="meta">We choose fruit for aroma and ripeness—not for speed.</div></div>
          </div>
          <div class="card2 card-pad step">
            <div class="num">2</div>
            <div><div style="font-weight:900">Wash & prep</div><div class="meta">Clean handling and careful preparation in-house.</div></div>
          </div>
          <div class="card2 card-pad step">
            <div class="num">3</div>
            <div><div style="font-weight:900">Small-batch cooking</div><div class="meta">Slow cooking helps build flavour and texture.</div></div>
          </div>
          <div class="card2 card-pad step">
            <div class="num">4</div>
            <div><div style="font-weight:900">Fill & seal</div><div class="meta">Hand-filled jars with batch checks.</div></div>
          </div>
          <div class="card2 card-pad step">
            <div class="num">5</div>
            <div><div style="font-weight:900">Pack for delivery</div><div class="meta">Secure packaging designed for gifting and shipping.</div></div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- REVIEWS -->
  <section class="section soft" id="reviews">
    <div class="container">
      <div style="max-width:640px">
        <div class="kicker">
          <svg class="i" viewBox="0 0 24 24"><path d="M12 3l1.2 4.2L18 9l-4.8 1.8L12 15l-1.2-4.2L6 9l4.8-1.8L12 3z"/></svg>
          Loved by customers
        </div>
        <h2>What people say</h2>
        <p>These are placeholders—swap with real reviews after launch.</p>
      </div>

      <div class="grid grid-3" style="margin-top:18px">
        <div class="card2 card-pad">
          <div style="display:flex;align-items:center;gap:8px">
            <svg class="i" viewBox="0 0 24 24" style="color:var(--emerald)"><path d="M12 3l1.2 4.2L18 9l-4.8 1.8L12 15l-1.2-4.2L6 9l4.8-1.8L12 3z"/></svg>
            <div style="font-weight:900">Aman, Ludhiana</div>
          </div>
          <p style="margin-top:10px;color:#334155">“The jam tastes like real guava—no artificial vibe. Packaging was premium too.”</p>
        </div>
        <div class="card2 card-pad">
          <div style="display:flex;align-items:center;gap:8px">
            <svg class="i" viewBox="0 0 24 24" style="color:var(--emerald)"><path d="M12 3l1.2 4.2L18 9l-4.8 1.8L12 15l-1.2-4.2L6 9l4.8-1.8L12 3z"/></svg>
            <div style="font-weight:900">Simran, Chandigarh</div>
          </div>
          <p style="margin-top:10px;color:#334155">“Chutney is perfect with paratha. Sweet + spicy balance is on point.”</p>
        </div>
        <div class="card2 card-pad">
          <div style="display:flex;align-items:center;gap:8px">
            <svg class="i" viewBox="0 0 24 24" style="color:var(--emerald)"><path d="M12 3l1.2 4.2L18 9l-4.8 1.8L12 15l-1.2-4.2L6 9l4.8-1.8L12 3z"/></svg>
            <div style="font-weight:900">Karan, Amritsar</div>
          </div>
          <p style="margin-top:10px;color:#334155">“Dehydrated guava is a great snack for travel. Not oily, not overly sweet.”</p>
        </div>
      </div>
    </div>
  </section>

  <!-- FAQ -->
  <section class="section" id="faq">
    <div class="container">
      <div style="max-width:640px">
        <div class="kicker">
          <svg class="i" viewBox="0 0 24 24"><path d="M12 19v.5"/><path d="M9 9a3 3 0 1 1 5.2 2c-.9 1-1.2 1.5-1.2 3"/></svg>
          FAQ
        </div>
        <h2>Quick answers</h2>
        <p>Reduce order friction with clear, short FAQs.</p>
      </div>

      <div style="margin-top:18px;max-width:800px;margin-left:auto;margin-right:auto" id="faqList"></div>
    </div>
  </section>

  <!-- CONTACT -->
  <section class="section soft" id="contact">
    <div class="container">
      <div style="max-width:740px">
        <div class="kicker">
          <svg class="i" viewBox="0 0 24 24"><path d="M22 16.9V21H3v-4.1"/><path d="M21 8l-9 6L3 8"/><path d="M3 21V7a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2v14"/></svg>
          Contact
        </div>
        <h2>Bulk orders, gifting, and store enquiries</h2>
        <p>Add a simple contact box. You can plug this into a real form provider later.</p>
      </div>

      <div class="grid grid-2" style="margin-top:18px">
        <div class="card2 card-pad">
          <div style="display:flex;align-items:center;gap:8px">
            <svg class="i" viewBox="0 0 24 24" style="color:var(--emerald)"><path d="M22 16.9V21H3v-4.1"/><path d="M21 8l-9 6L3 8"/><path d="M3 21V7a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2v14"/></svg>
            <div style="font-weight:900">Fast ordering</div>
          </div>
          <p style="margin-top:8px">
            Add items to cart and place your order on WhatsApp. We’ll confirm availability, delivery, and payment.
          </p>
          <div style="margin-top:14px;display:flex;gap:10px;flex-wrap:wrap">
            <a class="btn btn-wa" id="contactWA" href="#" target="_blank" rel="noreferrer">Order on WhatsApp</a>
            <a class="btn btn-ghost" href="mailto:hello@gillsnguavas.com">Email us</a>
          </div>

          <div class="grid" style="margin-top:14px">
            <div class="card2 card-pad" style="box-shadow:none">
              <div class="feature-row" style="align-items:flex-start">
                <div class="ic" style="background:#fff"><svg class="i" viewBox="0 0 24 24"><path d="M12 21s7-4.4 7-10a7 7 0 1 0-14 0c0 5.6 7 10 7 10z"/><circle cx="12" cy="11" r="2.5"/></svg></div>
                <div><div style="font-weight:900">Punjab, India</div><div class="meta">Update address after you finalize.</div></div>
              </div>
            </div>

            <div class="card2 card-pad" style="box-shadow:none">
              <div class="feature-row" style="align-items:flex-start">
                <div class="ic" style="background:#fff"><svg class="i" viewBox="0 0 24 24"><path d="M22 16.9V21H3v-4.1"/><path d="M21 8l-9 6L3 8"/><path d="M3 21V7a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2v14"/></svg></div>
                <div><div style="font-weight:900">hello@gillsnguavas.com</div><div class="meta">Replace with your business email.</div></div>
              </div>
            </div>
          </div>
        </div>

        <div class="card2 card-pad">
          <div style="font-weight:900">Bulk & gifting enquiry (placeholder)</div>
          <p style="margin-top:8px">
            This is a visual form. Connect it later to a real backend (Google Form, Tally, Typeform, Shopify, etc.).
          </p>

          <div class="grid" style="margin-top:14px">
            <input class="round-2xl ring" style="padding:12px 14px;background:rgba(255,255,255,.9);border:1px solid var(--ring)" placeholder="Name" />
            <input class="round-2xl ring" style="padding:12px 14px;background:rgba(255,255,255,.9);border:1px solid var(--ring)" placeholder="Phone / WhatsApp" />
            <input class="round-2xl ring" style="padding:12px 14px;background:rgba(255,255,255,.9);border:1px solid var(--ring)" placeholder="City" />
            <textarea rows="4" class="round-2xl ring" style="padding:12px 14px;background:rgba(255,255,255,.9);border:1px solid var(--ring)" placeholder="Tell us what you need (quantity, products, timeline)"></textarea>
            <button class="btn btn-primary" type="button">Submit enquiry</button>
            <div class="small">Tip: For fastest launch, link this to a Google Form.</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer class="footer">
    <div class="container">
      <div class="grid grid-3">
        <div>
          <div class="brand" style="gap:10px">
            <div class="logo"><img id="logoImg2" alt="logo" /></div>
            <div>
              <div style="font-weight:900">Gills N Guavas</div>
              <div class="small">Pure guava. Thoughtfully made.</div>
            </div>
          </div>
          <p style="max-width:420px;margin-top:10px">
            Small-batch guava products made with care. Replace placeholder content with your real brand story.
          </p>
        </div>

        <div class="grid grid-2" style="gap:10px">
          <div>
            <div style="font-weight:900">Shop</div>
            <div class="small" style="margin-top:10px;line-height:1.9">
              Guava Jam<br/>Guava Chutney<br/>Guava Snacks<br/>Combo Boxes
            </div>
          </div>
          <div>
            <div style="font-weight:900">Support</div>
            <div class="small" style="margin-top:10px;line-height:1.9">
              Shipping & returns<br/>Bulk orders<br/>Contact
            </div>
          </div>
        </div>

        <div>
          <div style="font-weight:900">Follow</div>
          <div style="margin-top:10px;display:flex;gap:10px;flex-wrap:wrap">
            <button class="btn btn-ghost" type="button" aria-label="Instagram">
              <svg class="i" viewBox="0 0 24 24"><rect x="4" y="4" width="16" height="16" rx="4"/><circle cx="12" cy="12" r="3.5"/><path d="M17.5 6.5h.01"/></svg>
            </button>
            <button class="btn btn-ghost" type="button" aria-label="Facebook">
              <svg class="i" viewBox="0 0 24 24"><path d="M14 9h3V6h-3c-2 0-4 2-4 4v3H7v3h3v6h3v-6h3l1-3h-4v-3c0-.6.4-1 1-1z"/></svg>
            </button>
            <button class="btn btn-ghost" type="button" aria-label="Email">
              <svg class="i" viewBox="0 0 24 24"><path d="M22 16.9V21H3v-4.1"/><path d="M21 8l-9 6L3 8"/><path d="M3 21V7a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2v14"/></svg>
            </button>
          </div>
          <div class="small" style="margin-top:10px">Images shown are placeholders for representation.</div>
        </div>
      </div>

      <div style="margin-top:22px;display:flex;flex-wrap:wrap;gap:10px;justify-content:space-between" class="small">
        <div>© <span id="year"></span> Gills N Guavas. All rights reserved.</div>
        <div>Made with care in India 🇮🇳</div>
      </div>
    </div>
  </footer>

  <!-- CART -->
  <div class="overlay" id="overlay"></div>
  <aside class="drawer" id="drawer" aria-hidden="true">
    <div class="drawer-head">
      <div>
        <div style="font-weight:900">Your cart</div>
        <div class="small">Add items and order on WhatsApp</div>
      </div>
      <button class="btn btn-ghost" id="closeCart">Close</button>
    </div>

    <div class="drawer-body" id="cartItems"></div>

    <div class="drawer-foot">
      <div style="display:flex;justify-content:space-between;align-items:center">
        <div class="small">Subtotal</div>
        <div style="font-weight:900;font-size:18px" id="subtotal">₹0</div>
      </div>

      <div class="grid" style="margin-top:12px">
        <a class="btn btn-wa" id="waOrder" href="#" target="_blank" rel="noreferrer" style="text-align:center">Order on WhatsApp</a>
        <button class="btn btn-ghost" id="clearCart">Clear cart</button>
        <div class="small">Tip: Replace WhatsApp number in code: <b>WA_NUMBER</b>.</div>
      </div>
    </div>
  </aside>

  <div class="toast" id="toast">Added to cart</div>

  <script>
    // ====== EDIT THIS ======
    const WA_NUMBER = "919999999999"; // country code + number, no + sign, no spaces
    // =======================

    // Images (same as your React version; works in Notepad too as long as you have internet)
    const IMG_GUAVA = "https://images.unsplash.com/photo-1536511132770-e5058c7e8c46?auto=format&fit=crop&fm=jpg&q=80&w=2400";
    const IMG_JAM_JAR = "https://images.unsplash.com/photo-1610135373101-89aeeab8fa50?auto=format&fit=crop&fm=jpg&q=80&w=2400";
    const IMG_JAM_TOAST = "https://images.unsplash.com/photo-1707092009843-2b5a919d17b0?auto=format&fit=crop&fm=jpg&q=80&w=2400";
    const IMG_DARK_JAM = "https://images.unsplash.com/photo-1695088956481-6c46b7714537?auto=format&fit=crop&fm=jpg&q=80&w=2400";

    // Simple logo as data URI (no external file)
    const LOGO = "data:image/svg+xml;charset=UTF-8," + encodeURIComponent(`
      <svg xmlns='http://www.w3.org/2000/svg' width='256' height='256' viewBox='0 0 256 256'>
        <defs>
          <linearGradient id='lg' x1='0' y1='0' x2='1' y2='1'>
            <stop offset='0' stop-color='#14532d'/>
            <stop offset='1' stop-color='#1f7a44'/>
          </linearGradient>
        </defs>
        <rect x='16' y='16' width='224' height='224' rx='56' fill='url(#lg)'/>
        <g fill='#ffffff'>
          <path d='M128 64c-26 0-48 20-48 44 0 26 22 44 48 44 20 0 34-8 42-18v18c0 22-18 40-42 40-14 0-26-5-36-14l-18 18c14 14 33 22 54 22 38 0 70-28 70-66V108c0-24-22-44-70-44zm0 22c28 0 40 8 40 22 0 12-14 22-40 22-14 0-26-10-26-22 0-14 12-22 26-22z'/>
          <path d='M176 64c6-18 20-28 36-30-8 16-18 26-36 30z' opacity='0.9'/>
          <circle cx='196' cy='60' r='6' opacity='0.9'/>
        </g>
      </svg>
    `);

    const CATEGORIES = ["All", "Jam", "Chutney", "Snacks", "Combos"];

    const PRODUCTS = [
      { id:"jam-200", name:"Guava Jam (Seedless)", category:"Jam", size:"200g Glass Jar", price:199, badge:"Bestseller", notes:["No artificial colour","Small-batch cooked","Smooth & seedless"], useWith:"Roti • Toast • Paratha • Desserts", img:IMG_JAM_JAR },
      { id:"jam-350", name:"Guava Jam (Seedless)", category:"Jam", size:"350g Glass Jar", price:299, badge:"Family Size", notes:["No artificial colour","Small-batch cooked","Rich guava flavour"], useWith:"Breakfast • Baking • Gifting", img:IMG_JAM_TOAST },
      { id:"chutney-200", name:"Sweet & Spicy Guava Chutney", category:"Chutney", size:"200g Glass Jar", price:169, badge:"Punjabi Favourite", notes:["Sweet-tangy balance","No preservatives","Handcrafted"], useWith:"Paratha • Snacks • Sandwich", img:IMG_DARK_JAM },
      { id:"snack-50", name:"Dehydrated Guava Slices", category:"Snacks", size:"50g Pouch", price:139, badge:"No Deep Fry", notes:["Slow dehydrated","Naturally sweet","Travel-friendly"], useWith:"Healthy snacking", img:IMG_GUAVA },
      { id:"snack-100", name:"Chatpata Masala Guava Bites", category:"Snacks", size:"100g Pouch", price:249, badge:"Chatpata", notes:["Masala coated","Non-fried","Perfect with chai"], useWith:"Chai time • Movie night", img:IMG_GUAVA },
      { id:"combo-starter", name:"Guava Starter Box", category:"Combos", size:"Jam 200g + Chutney 200g", price:349, badge:"Value Combo", notes:["Perfect to try","Gift-ready","Save vs. single"], useWith:"Everyday essentials", img:IMG_JAM_TOAST }
    ];

    const FAQS = [
      { q:"Are these photos real?", a:"These are clean placeholder images so your site looks premium from day one. Replace them later with your real product photos—just swap the product image links." },
      { q:"Do you use artificial colours or flavours?", a:"No. We keep it simple—fresh guava, carefully selected ingredients, and small-batch cooking." },
      { q:"How do I place an order?", a:"Add items to cart and tap ‘Order on WhatsApp’. We’ll confirm address, shipping and payment." },
      { q:"What is the shelf life?", a:"Varies by product. Typically, jam/chutney has longer shelf life than snacks. Mention the exact shelf life on your label and product page once finalized." }
    ];

    // State
    let activeCategory = "All";
    let query = "";
    let cart = {}; // {id: qty}

    // DOM
    const heroBg = document.getElementById("heroBg");
    const logoImg = document.getElementById("logoImg");
    const logoImg2 = document.getElementById("logoImg2");
    const catsEl = document.getElementById("cats");
    const gridEl = document.getElementById("productGrid");
    const featuredEl = document.getElementById("featuredList");
    const searchInput = document.getElementById("searchInput");
    const cartBadge = document.getElementById("cartBadge");
    const overlay = document.getElementById("overlay");
    const drawer = document.getElementById("drawer");
    const cartItemsEl = document.getElementById("cartItems");
    const subtotalEl = document.getElementById("subtotal");
    const waOrder = document.getElementById("waOrder");
    const heroWA = document.getElementById("heroWA");
    const contactWA = document.getElementById("contactWA");
    const toast = document.getElementById("toast");

    // Setup visuals
    heroBg.style.backgroundImage = `linear-gradient(180deg, rgba(251,250,246,.35), rgba(251,250,246,.35)), url(${IMG_GUAVA})`;
    logoImg.src = LOGO; logoImg2.src = LOGO;
    document.getElementById("year").textContent = new Date().getFullYear();

    // Smooth jumps
    function jumpTo(id){
      const el = document.getElementById(id);
      if(el) el.scrollIntoView({behavior:"smooth"});
    }
    document.querySelectorAll("[data-jump]").forEach(b=>{
      b.addEventListener("click", ()=> jumpTo(b.getAttribute("data-jump")));
    });
    document.getElementById("jumpTop").addEventListener("click", ()=> window.scrollTo({top:0,behavior:"smooth"}));

    // Currency
    function currency(n){
      return "₹" + Math.round(n).toLocaleString("en-IN");
    }

    function cartItems(){
      return Object.entries(cart).map(([id,qty])=>{
        const p = PRODUCTS.find(x=>x.id===id);
        return p ? {...p, qty:+qty} : null;
      }).filter(Boolean);
    }

    function cartCount(){
      return cartItems().reduce((a,x)=>a+x.qty,0);
    }

    function subtotal(){
      return cartItems().reduce((a,x)=>a+x.qty*x.price,0);
    }

    function waLink(){
      const items = cartItems();
      const lines = items.map(x=>`• ${x.name} — ${x.size} × ${x.qty} = ${currency(x.qty*x.price)}`);
      const msg =
        "Hi Gills N Guavas! I want to place an order:%0A%0A" +
        lines.join("%0A") +
        `%0A%0ASubtotal: ${currency(subtotal())}%0A%0AName:%0AAddress:%0APincode:%0APhone:%0APayment preference (UPI/COD):`;
      return `https://wa.me/${WA_NUMBER}?text=${msg}`;
    }

    function showToast(text){
      toast.textContent = text;
      toast.classList.add("show");
      setTimeout(()=>toast.classList.remove("show"), 1400);
    }

    function addToCart(id){
      cart[id] = (cart[id]||0)+1;
      showToast("Added to cart");
      renderCart();
      renderBadge();
    }

    function setQty(id, qty){
      if(qty<=0) delete cart[id];
      else cart[id]=qty;
      renderCart();
      renderBadge();
    }

    function clearCart(){
      cart = {};
      renderCart();
      renderBadge();
    }

    // Render categories
    function renderCategories(){
      catsEl.innerHTML = "";
      CATEGORIES.forEach(c=>{
        const btn = document.createElement("button");
        btn.className = "chip" + (c===activeCategory ? " active" : "");
        btn.textContent = c;
        btn.addEventListener("click", ()=>{
          activeCategory = c;
          renderCategories();
          renderProducts();
        });
        catsEl.appendChild(btn);
      });
    }

    // Render products
    function productMatches(p){
      const catOk = (activeCategory==="All") || (p.category===activeCategory);
      if(!catOk) return false;
      const q = query.trim().toLowerCase();
      if(!q) return true;
      const hay = [p.name,p.category,p.size,p.badge,p.useWith].filter(Boolean).join(" ").toLowerCase();
      return hay.includes(q);
    }

    function renderProducts(){
      gridEl.innerHTML = "";
      PRODUCTS.filter(productMatches).forEach(p=>{
        const card = document.createElement("div");
        card.className = "card2 prod shadow ring";
        card.innerHTML = `
          <div class="rel">
            <img src="${p.img}" alt="${p.name}">
            ${p.badge ? `<div class="badgeTag">${p.badge}</div>` : ""}
          </div>
          <div class="prod-body">
            <div class="prod-top">
              <div style="min-width:0">
                <div class="prod-name" title="${p.name}">${p.name}</div>
                <div class="prod-size">${p.size}</div>
              </div>
              <div style="text-align:right">
                <div class="price">${currency(p.price)}</div>
              </div>
            </div>

            <div class="prod-tags">
              <span class="pill">${p.category}</span>
              <span class="pill">${p.notes[0]}</span>
              <span class="pill">${p.notes[1]}</span>
            </div>

            <div class="meta"><b style="color:var(--text)">Best with:</b> ${p.useWith}</div>

            <div class="prod-bottom">
              <button class="btn btn-primary" type="button">Add to cart</button>
              <button class="btn btn-ghost" type="button">Details</button>
            </div>
          </div>
        `;
        card.querySelector(".btn-primary").addEventListener("click", ()=> addToCart(p.id));
        card.querySelector(".btn-ghost").addEventListener("click", ()=> openCart());
        gridEl.appendChild(card);
      });
    }

    // Featured list
    function renderFeatured(){
      featuredEl.innerHTML = "";
      PRODUCTS.slice(0,3).forEach(p=>{
        const row = document.createElement("div");
        row.className = "card2 ring round-2xl";
        row.style.padding = "12px";
        row.style.display = "flex";
        row.style.gap = "12px";
        row.style.alignItems = "center";
        row.innerHTML = `
          <img src="${p.img}" alt="${p.name}" style="height:64px;width:86px;border-radius:14px;object-fit:cover;border:1px solid var(--ring)">
          <div style="min-width:0;flex:1">
            <div style="font-weight:900;white-space:nowrap;overflow:hidden;text-overflow:ellipsis">${p.name}</div>
            <div class="small" style="white-space:nowrap;overflow:hidden;text-overflow:ellipsis">${p.size}</div>
            <div style="font-weight:900;color:var(--emerald);margin-top:4px">${currency(p.price)}</div>
          </div>
          <button class="btn btn-primary" type="button" style="padding:10px 12px;border-radius:14px;font-size:12px">Add</button>
        `;
        row.querySelector("button").addEventListener("click", ()=> addToCart(p.id));
        featuredEl.appendChild(row);
        featuredEl.appendChild(document.createElement("div")).style.height="10px";
      });
    }

    // FAQ
    function renderFAQ(){
      const faqList = document.getElementById("faqList");
      faqList.innerHTML = "";
      FAQS.forEach((f, idx)=>{
        const item = document.createElement("div");
        item.className = "card2 ring round-3xl faq-item";
        item.style.marginBottom = "10px";
        item.innerHTML = `
          <button class="faq-q" type="button">
            <span>${f.q}</span>
            <svg class="caret" viewBox="0 0 24 24"><path d="M6 9l6 6 6-6"/></svg>
          </button>
          <div class="faq-a">${f.a}</div>
        `;
        const btn = item.querySelector(".faq-q");
        btn.addEventListener("click", ()=>{
          const open = item.classList.contains("open");
          document.querySelectorAll(".faq-item").forEach(x=>x.classList.remove("open"));
          if(!open) item.classList.add("open");
        });
        if(idx===0) item.classList.add("open");
        faqList.appendChild(item);
      });
    }

    // Cart drawer
    function openCart(){
      overlay.classList.add("open");
      drawer.classList.add("open");
      drawer.setAttribute("aria-hidden","false");
      renderCart();
    }
    function closeCart(){
      overlay.classList.remove("open");
      drawer.classList.remove("open");
      drawer.setAttribute("aria-hidden","true");
    }

    document.getElementById("openCart").addEventListener("click", openCart);
    document.getElementById("closeCart").addEventListener("click", closeCart);
    overlay.addEventListener("click", closeCart);
    document.getElementById("clearCart").addEventListener("click", clearCart);

    function renderBadge(){
      const count = cartCount();
      if(count>0){
        cartBadge.style.display="flex";
        cartBadge.textContent = count;
      } else {
        cartBadge.style.display="none";
      }
    }

    function renderCart(){
      const items = cartItems();
      cartItemsEl.innerHTML = "";

      const link = waLink();
      heroWA.href = link;
      contactWA.href = link;

      if(items.length===0){
        const empty = document.createElement("div");
        empty.className = "card2 ring round-3xl";
        empty.style.padding = "16px";
        empty.innerHTML = `<div style="font-weight:900">Cart is empty</div><div class="meta" style="margin-top:6px">Add products from the Shop section.</div>`;
        cartItemsEl.appendChild(empty);

        waOrder.href = "#";
        waOrder.style.opacity = ".55";
        waOrder.style.pointerEvents = "none";
        document.getElementById("clearCart").disabled = true;
        document.getElementById("clearCart").style.opacity = ".6";
      } else {
        waOrder.href = link;
        waOrder.style.opacity = "1";
        waOrder.style.pointerEvents = "auto";
        document.getElementById("clearCart").disabled = false;
        document.getElementById("clearCart").style.opacity = "1";

        items.forEach(x=>{
          const wrap = document.createElement("div");
          wrap.className = "card2 ring round-3xl";
          wrap.style.padding = "14px";
          wrap.style.marginBottom = "10px";
          wrap.innerHTML = `
            <div class="cart-item">
              <img src="${x.img}" alt="${x.name}">
              <div style="min-width:0;flex:1">
                <div style="font-weight:900;white-space:nowrap;overflow:hidden;text-overflow:ellipsis">${x.name}</div>
                <div class="small" style="white-space:nowrap;overflow:hidden;text-overflow:ellipsis">${x.size}</div>
                <div style="margin-top:6px;font-weight:900;color:var(--emerald)">${currency(x.price)}</div>
              </div>
            </div>
            <div class="cart-row">
              <div class="stepper">
                <button type="button" aria-label="Decrease">-</button>
                <span>${x.qty}</span>
                <button type="button" aria-label="Increase">+</button>
              </div>
              <div style="font-weight:900">${currency(x.qty*x.price)}</div>
            </div>
          `;
          const [decBtn, incBtn] = wrap.querySelectorAll(".stepper button");
          decBtn.addEventListener("click", ()=> setQty(x.id, x.qty-1));
          incBtn.addEventListener("click", ()=> setQty(x.id, x.qty+1));
          cartItemsEl.appendChild(wrap);
        });
      }

      subtotalEl.textContent = currency(subtotal());
    }

    // Search
    searchInput.addEventListener("input", (e)=>{
      query = e.target.value;
      renderProducts();
    });

    // Initial render
    renderCategories();
    renderFeatured();
    renderProducts();
    renderFAQ();
    renderCart();
    renderBadge();
  </script>
</body>
</html>

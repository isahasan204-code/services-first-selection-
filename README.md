<!-- ===== CODE 1: FROM START UNTIL BEFORE PROJECTS SECTION ===== -->



  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Elite Home Services - Professional Home Improvement | London, ON</title>

  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&amp;family=Inter:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet">

  <style>
    *{margin:0;padding:0;box-sizing:border-box}
    :root{
      --background:#faf8f6;
      --foreground:#2d2520;
      --primary:#5D4037;
      --primary-foreground:#faf8f6;
      --accent:#c4784a;
      --muted:#6b5c52;
      --card:#f5f2ef;
      --border:#e8e2dc;

      --radius:16px;
      --shadow:0 14px 40px -14px rgba(45,37,32,0.18);
    }

    body{
      font-family:'Inter',sans-serif;
      background:var(--background);
      color:var(--foreground);
      line-height:1.6;
    }
    h1,h2,h3,h4{font-family:'Playfair Display',serif}
    a{color:inherit}
    .container{max-width:1100px;margin:0 auto;padding:0 16px}

    /* HEADER */
    .header{
      background:var(--primary);
      color:var(--primary-foreground);
      border-bottom:1px solid rgba(255,255,255,0.12);
    }
    .header-wrap{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:12px;
      padding:14px 0;
      flex-wrap:wrap;
    }
    .brand{display:flex;flex-direction:column;gap:2px;min-width:220px}
    .brand h1{font-size:18px;font-weight:700;letter-spacing:.2px;line-height:1.15}
    .brand p{font-size:12.5px;opacity:.85}

    .header-actions{
      display:flex;
      gap:10px;
      flex-wrap:wrap;
      justify-content:flex-end;
    }
    .pill{
      display:inline-flex;
      align-items:center;
      gap:8px;
      text-decoration:none;
      padding:10px 12px;
      border-radius:999px;
      border:1px solid rgba(255,255,255,0.18);
      background:rgba(255,255,255,0.08);
      font-size:13px;
      font-weight:600;
      transition:transform .15s ease, opacity .15s ease;
      white-space:nowrap;
    }
    .pill:hover{opacity:0.9;transform:translateY(-1px)}
    .pill strong{font-weight:700}

    /* HERO */
    .hero{
      position:relative;
      background:
        linear-gradient(to bottom, rgba(45,37,32,0.78), rgba(45,37,32,0.35)),
        url("https://images.unsplash.com/photo-1600596542815-ffad4c1539a9?w=1920") center/cover no-repeat;
      color:var(--primary-foreground);
    }
    .hero .container{padding:34px 16px 28px}
    .hero-card{
      max-width:720px;
      background:rgba(0,0,0,0.15);
      border:1px solid rgba(255,255,255,0.14);
      border-radius:var(--radius);
      padding:18px;
      box-shadow:0 18px 50px -26px rgba(0,0,0,0.55);
      backdrop-filter: blur(8px);
    }
    .hero h2{font-size:28px;line-height:1.15;margin-bottom:10px}
    .hero p{font-size:15.5px;opacity:.92;margin-bottom:14px;max-width:60ch}
    .hero-cta{display:flex;gap:10px;flex-wrap:wrap;margin-bottom:14px}
    .btn{
      display:inline-flex;
      align-items:center;
      justify-content:center;
      gap:10px;
      padding:12px 16px;
      border-radius:999px;
      text-decoration:none;
      font-weight:700;
      font-size:14px;
      border:1px solid rgba(255,255,255,0.0);
      transition:transform .15s ease, opacity .15s ease;
      white-space:nowrap;
    }
    .btn:hover{transform:translateY(-1px);opacity:0.95}
    .btn-primary{
      background:var(--accent);
      color:#1f140f;
      border:1px solid rgba(255,255,255,0.12);
    }
    .btn-outline{
      background:rgba(255,255,255,0.10);
      color:var(--primary-foreground);
      border:1px solid rgba(255,255,255,0.18);
    }
    .badges{display:flex;flex-wrap:wrap;gap:8px}
    .badge{
      display:inline-flex;
      align-items:center;
      gap:8px;
      padding:8px 12px;
      border-radius:999px;
      background:rgba(255,255,255,0.10);
      border:1px solid rgba(255,255,255,0.16);
      font-size:12.5px;
      font-weight:600;
    }
    .dot{width:8px;height:8px;border-radius:50%;background:var(--accent)}

    /* SECTION TITLES */
    .section{padding:34px 0}
    .section-head{text-align:center;margin-bottom:16px}
    .section-head h2{font-size:24px;margin-bottom:8px}
    .section-head p{color:var(--muted);font-size:15px;max-width:70ch;margin:0 auto}

    /* SERVICES GRID */
    .services{
      background:var(--card);
      border-top:1px solid var(--border);
      border-bottom:1px solid var(--border);
    }
    .grid{
      display:grid;
      grid-template-columns:1fr;
      gap:14px;
      margin-top:18px;
    }
    .card{
      background:#fff;
      border:1px solid var(--border);
      border-radius:var(--radius);
      padding:16px;
      box-shadow:0 10px 24px -18px rgba(45,37,32,0.18);
    }
    .card h3{font-size:18px;line-height:1.2;margin-bottom:8px}
    .card p{color:var(--muted);font-size:14.5px;line-height:1.65}

    .feature-row{
      margin-top:18px;
      display:flex;
      gap:8px;
      flex-wrap:wrap;
      justify-content:center;
    }
    .chip{
      background:#fff;
      border:1px solid var(--border);
      border-radius:999px;
      padding:8px 12px;
      font-size:12.5px;
      font-weight:600;
      color:var(--foreground);
    }

    /* CTA + FOOTER (used later in code 3) */
    .cta{
      background:linear-gradient(180deg, #fff, var(--card));
      border-top:1px solid var(--border);
      padding:34px 0;
      text-align:center;
    }
    .cta h2{font-size:24px;margin-bottom:8px}
    .cta p{
      color:var(--muted);
      font-size:15px;
      max-width:70ch;
      margin:0 auto 16px;
    }

    .footer{
      background:var(--primary);
      color:var(--primary-foreground);
      padding:32px 0 18px;
      margin-top:0;
    }
    .footer-grid{
      display:grid;
      grid-template-columns:1fr;
      gap:18px;
    }
    .footer h3{font-size:18px;margin-bottom:8px}
    .footer h4{
      font-family:'Inter',sans-serif;
      font-size:14px;
      font-weight:700;
      margin-bottom:8px;
      opacity:0.95;
    }
    .footer p, .footer li{font-size:13.5px;opacity:0.86}
    .footer ul{list-style:none}
    .footer li{margin-bottom:6px}
    .footer a{color:var(--primary-foreground);text-decoration:none}
    .footer a:hover{opacity:0.9;text-decoration:underline}
    .footer-bottom{
      border-top:1px solid rgba(255,255,255,0.16);
      margin-top:18px;
      padding-top:14px;
      text-align:center;
      font-size:12.5px;
      opacity:0.7;
    }

    /* RESPONSIVE */
    @media (min-width: 640px){
      .container{padding:0 20px}
      .hero .container{padding:44px 20px 34px}
      .hero h2{font-size:34px}
      .grid{grid-template-columns:repeat(2, minmax(0,1fr))}
      .footer-grid{grid-template-columns:repeat(2, minmax(0,1fr))}
    }
    @media (min-width: 980px){
      .hero .container{padding:68px 24px 48px}
      .hero-card{padding:22px}
      .hero h2{font-size:44px}
      .hero p{font-size:16.5px}
      .grid{grid-template-columns:repeat(3, minmax(0,1fr))}
      .footer-grid{grid-template-columns:repeat(3, minmax(0,1fr))}
    }
    html{scroll-behavior:smooth}
  </style>




  <!-- HEADER -->
  <header class="header">
    <div class="container">
      <div class="header-wrap">
        <div class="brand">
          <h1>Elite Home Services</h1>
          <p>Professional Home Improvement • London, ON</p>
        </div>

        <div class="header-actions">
          <a class="pill" href="tel:+15196972361">📞 <strong>(519) 697-2361</strong></a>
          <a class="pill" href="mailto:contact@elitehomeservices.ca">✉️ <strong>contact@elitehomeservices.ca</strong></a>
        </div>
      </div>
    </div>
  </header>

  <!-- HERO -->
  <section class="hero">
    <div class="container">
      <div class="hero-card hero-content">
        <h2>Professional Home Services You Can Trust</h2>
        <p>
          Elite Home Services provides clean, reliable home improvement solutions with attention to detail and professional finishing.
          Serving London, ON and surrounding areas.
        </p>

        <div class="hero-cta">
          <a class="btn btn-primary" href="tel:+15196972361">Call Now</a>
          <a class="btn btn-outline" href="mailto:contact@elitehomeservices.ca">Email Us</a>
        </div>

        <div class="badges">
          <span class="badge"><span class="dot"></span> Free Estimates</span>
          <span class="badge"><span class="dot"></span> Clean &amp; Professional</span>
          <span class="badge"><span class="dot"></span> Transparent Pricing</span>
          <span class="badge"><span class="dot"></span> On-Time Service</span>
        </div>
      </div>
    </div>
  </section>

  <!-- SERVICES -->
  <section class="section services">
    <div class="container">
      <div class="section-head">
        <h2>Our Professional Home Services</h2>
        <p>
          Elite Home Services provides clean, reliable home improvement solutions with attention to detail and professional finishing.
        </p>
      </div>

      <div class="grid">
        <div class="card">
          <h3>Painting, Wall Repair &amp; Wood Finishing</h3>
          <p>
            Interior and exterior painting with clean, smooth results. We also provide wall putty, wall repairs,
            and surface corrections for a flawless finish. Interior wood painting and wood staining are available
            for stair railings, handrails, and other indoor wooden elements.
          </p>
        </div>

        <div class="card">
          <h3>Flooring Installation &amp; Removal</h3>
          <p>
            Professional laminate and vinyl flooring installation with proper leveling, precise alignment, and clean finishing.
            We also remove old flooring and prepare surfaces to ensure long-lasting results.
          </p>
        </div>

        <div class="card">
          <h3>Fence &amp; Gate Services</h3>
          <p>
            Residential fence and gate installation, repair, and removal — including backyard wooden fencing solutions
            designed for durability and a clean, finished look.
          </p>
        </div>

        <div class="card">
          <h3>Custom Wall &amp; Room Décor</h3>
          <p>
            Modern TV back wall decoration with clean finishing and optional LED lighting.
            We also create custom bedroom décor and wall features based on your style and needs.
          </p>
        </div>

        <div class="card">
          <h3>Laundry Room Improvement &amp; Organization</h3>
          <p>
            Functional and decorative laundry room upgrades, including shelving and custom solutions to make the space
            more practical, organized, and easier to use.
          </p>
        </div>

        <div class="card">
          <h3>Small Home Installations</h3>
          <p>
            TV mounting, shelf installation, and a variety of small home improvement and installation services
            completed carefully and efficiently.
          </p>
        </div>
      </div>

      <div class="feature-row" aria-label="service highlights">
        <span class="chip">On-time Work</span>
        <span class="chip">Clean Results</span>
        <span class="chip">Fair Pricing</span>
        <span class="chip">Customer Satisfaction</span>
      </div>
    </div>
  </section>

  <!-- STOP HERE (before Projects section) -->     









  services second selection


  

  <!-- ===== CODE 2: FROM PROJECTS SECTION UNTIL BEFORE CTA (Looking for Reliable Home Services?) ===== -->

  <!-- PROJECTS BY SERVICE -->
  <section class="projects-by-service">
    <div class="container">
      <div class="section-head">
        <h2>Projects by Service</h2>
        <p>
          Browse a few examples for each service. Tap any photo to view it larger and swipe through the set.
        </p>
      </div>

      <div class="pbs-grid">
        <!-- Painting -->
        <article class="pbs-card" data-gallery="painting">
          <h3>Painting Projects</h3>
          <div class="pbs-photos">
            <button class="pbs-photo" data-gallery="painting" data-index="0" aria-label="Open painting photo 1">
              <img src="https://images.unsplash.com/photo-1589939705384-5185138a047a?w=1200" alt="Painting project photo 1">
            </button>
            <button class="pbs-photo" data-gallery="painting" data-index="1" aria-label="Open painting photo 2">
              <img src="https://images.unsplash.com/photo-1562259949-e8e7689d7828?w=1200" alt="Painting project photo 2">
            </button>
            <button class="pbs-photo" data-gallery="painting" data-index="2" aria-label="Open painting photo 3">
              <img src="https://images.unsplash.com/photo-1523413651479-597eb2da0ad6?w=1200" alt="Painting project photo 3">
            </button>
          </div>
        </article>

        <!-- Flooring -->
        <article class="pbs-card" data-gallery="flooring">
          <h3>Flooring Projects</h3>
          <div class="pbs-photos">
            <button class="pbs-photo" data-gallery="flooring" data-index="0" aria-label="Open flooring photo 1">
              <img src="https://images.unsplash.com/photo-1581858726788-75bc0f6a952d?w=1200" alt="Flooring project photo 1">
            </button>
            <button class="pbs-photo" data-gallery="flooring" data-index="1" aria-label="Open flooring photo 2">
              <img src="https://images.unsplash.com/photo-1556912167-f556f1f39faa?w=1200" alt="Flooring project photo 2">
            </button>
            <button class="pbs-photo" data-gallery="flooring" data-index="2" aria-label="Open flooring photo 3">
              <img src="https://images.unsplash.com/photo-1560185009-5bf9f2849488?w=1200" alt="Flooring project photo 3">
            </button>
          </div>
        </article>

        <!-- Fence & Gate -->
        <article class="pbs-card" data-gallery="fence">
          <h3>Fence &amp; Gate Projects</h3>
          <div class="pbs-photos">
            <button class="pbs-photo" data-gallery="fence" data-index="0" aria-label="Open fence photo 1">
              <img src="https://images.unsplash.com/photo-1626646187146-1d867144062f?w=1200" alt="Fence project photo 1">
            </button>
            <button class="pbs-photo" data-gallery="fence" data-index="1" aria-label="Open fence photo 2">
              <img src="https://images.unsplash.com/photo-1615873968403-89e068629265?w=1200" alt="Fence project photo 2">
            </button>
            <button class="pbs-photo" data-gallery="fence" data-index="2" aria-label="Open fence photo 3">
              <img src="https://images.unsplash.com/photo-1523413651479-597eb2da0ad6?w=1200" alt="Fence project photo 3">
            </button>
          </div>
        </article>

        <!-- TV Wall & Decor -->
        <article class="pbs-card" data-gallery="decor">
          <h3>TV Wall &amp; Room Décor Projects</h3>
          <div class="pbs-photos">
            <button class="pbs-photo" data-gallery="decor" data-index="0" aria-label="Open decor photo 1">
              <img src="https://images.unsplash.com/photo-1618221195710-dd6b41faaea6?w=1200" alt="Decor project photo 1">
            </button>
            <button class="pbs-photo" data-gallery="decor" data-index="1" aria-label="Open decor photo 2">
              <img src="https://images.unsplash.com/photo-1615873968403-89e068629265?w=1200" alt="Decor project photo 2">
            </button>
            <button class="pbs-photo" data-gallery="decor" data-index="2" aria-label="Open decor photo 3">
              <img src="https://images.unsplash.com/photo-1554995207-c18c203602cb?w=1200" alt="Decor project photo 3">
            </button>
          </div>
        </article>

        <!-- Laundry -->
        <article class="pbs-card" data-gallery="laundry">
          <h3>Laundry Room Projects</h3>
          <div class="pbs-photos">
            <button class="pbs-photo" data-gallery="laundry" data-index="0" aria-label="Open laundry photo 1">
              <img src="https://images.unsplash.com/photo-1567168544813-cc03465b4fa8?w=1200" alt="Laundry project photo 1">
            </button>
            <button class="pbs-photo" data-gallery="laundry" data-index="1" aria-label="Open laundry photo 2">
              <img src="https://images.unsplash.com/photo-1556912167-f556f1f39faa?w=1200" alt="Laundry project photo 2">
            </button>
            <button class="pbs-photo" data-gallery="laundry" data-index="2" aria-label="Open laundry photo 3">
              <img src="https://images.unsplash.com/photo-1554995207-c18c203602cb?w=1200" alt="Laundry project photo 3">
            </button>
          </div>
        </article>

        <!-- Small Installations -->
        <article class="pbs-card" data-gallery="install">
          <h3>Small Installations Projects</h3>
          <div class="pbs-photos">
            <button class="pbs-photo" data-gallery="install" data-index="0" aria-label="Open installations photo 1">
              <img src="https://images.unsplash.com/photo-1544450173-8c8d038670b1?w=1200" alt="Installations project photo 1">
            </button>
            <button class="pbs-photo" data-gallery="install" data-index="1" aria-label="Open installations photo 2">
              <img src="https://images.unsplash.com/photo-1554995207-c18c203602cb?w=1200" alt="Installations project photo 2">
            </button>
            <button class="pbs-photo" data-gallery="install" data-index="2" aria-label="Open installations photo 3">
              <img src="https://images.unsplash.com/photo-1560185009-5bf9f2849488?w=1200" alt="Installations project photo 3">
            </button>
          </div>
        </article>
      </div>
    </div>
  </section>

  <!-- LIGHTBOX -->
  <div class="pbs-lightbox" id="pbsLightbox" aria-hidden="true">
    <button class="pbs-lb-close" id="pbsClose" aria-label="Close">✕</button>
    <button class="pbs-lb-nav pbs-lb-prev" id="pbsPrev" aria-label="Previous">‹</button>

    <figure class="pbs-lb-figure">
      <img id="pbsLbImg" src="" alt="">
      <figcaption class="pbs-lb-caption" id="pbsCaption"></figcaption>
    </figure>

    <button class="pbs-lb-nav pbs-lb-next" id="pbsNext" aria-label="Next">›</button>
  </div>

  <style>
    .projects-by-service{ padding:34px 0; }

    .pbs-grid{
      display:grid;
      grid-template-columns:1fr;
      gap:14px;
      margin-top:18px;
    }
    .pbs-card{
      background:#fff;
      border:1px solid var(--border);
      border-radius:var(--radius);
      padding:14px;
      box-shadow: var(--shadow);
    }
    .pbs-card h3{
      font-size:18px;
      margin-bottom:10px;
      line-height:1.2;
    }
    .pbs-photos{
      display:grid;
      grid-template-columns:repeat(3, minmax(0,1fr));
      gap:10px;
    }
    .pbs-photo{
      border:0;
      padding:0;
      background:transparent;
      cursor:pointer;
      border-radius:12px;
      overflow:hidden;
      outline:none;
    }
    .pbs-photo img{
      width:100%;
      height:120px;
      object-fit:cover;
      display:block;
      transition:transform .18s ease, opacity .18s ease;
    }
    .pbs-photo:hover img{transform:scale(1.02);opacity:0.95}

    @media (min-width: 640px){
      .pbs-grid{ grid-template-columns:repeat(2, minmax(0,1fr)); }
      .pbs-photo img{ height:140px; }
    }
    @media (min-width: 980px){
      .pbs-grid{ grid-template-columns:repeat(3, minmax(0,1fr)); }
      .pbs-photo img{ height:150px; }
    }
    @media (max-width: 420px){
      .pbs-photos{ gap:8px; }
      .pbs-photo img{ height:105px; }
    }

    .pbs-lightbox{
      position:fixed;
      inset:0;
      background:rgba(0,0,0,0.78);
      display:none;
      align-items:center;
      justify-content:center;
      z-index:9999;
      padding:18px;
    }
    .pbs-lightbox.is-open{ display:flex; }
    .pbs-lb-figure{
      max-width: 980px;
      width: 100%;
      margin:0;
      text-align:center;
    }
    .pbs-lb-figure img{
      width:100%;
      max-height:78vh;
      object-fit:contain;
      border-radius:16px;
      background: rgba(255,255,255,0.04);
    }
    .pbs-lb-caption{
      margin-top:10px;
      color:#fff;
      font-size:13.5px;
      opacity:0.9;
    }
    .pbs-lb-close{
      position:absolute;
      top:14px;
      right:14px;
      width:44px;height:44px;
      border-radius:999px;
      border:1px solid rgba(255,255,255,0.25);
      background:rgba(255,255,255,0.12);
      color:#fff;
      font-size:18px;
      cursor:pointer;
    }
    .pbs-lb-nav{
      position:absolute;
      top:50%;
      transform:translateY(-50%);
      width:46px;height:46px;
      border-radius:999px;
      border:1px solid rgba(255,255,255,0.25);
      background:rgba(255,255,255,0.12);
      color:#fff;
      font-size:28px;
      cursor:pointer;
      display:flex;
      align-items:center;
      justify-content:center;
    }
    .pbs-lb-prev{ left:14px; }
    .pbs-lb-next{ right:14px; }

    @media (max-width: 520px){
      .pbs-lb-prev{ left:8px; }
      .pbs-lb-next{ right:8px; }
      .pbs-lb-nav{ width:42px; height:42px; }
    }
  </style>

  <script>
    const galleries = {};
    document.querySelectorAll('.pbs-photo').forEach(btn => {
      const g = btn.dataset.gallery;
      const img = btn.querySelector('img');
      if (!galleries[g]) galleries[g] = [];
      galleries[g].push({
        src: img.getAttribute('src'),
        alt: img.getAttribute('alt') || ''
      });
    });

    const lb = document.getElementById('pbsLightbox');
    const lbImg = document.getElementById('pbsLbImg');
    const lbCap = document.getElementById('pbsCaption');
    const btnClose = document.getElementById('pbsClose');
    const btnPrev = document.getElementById('pbsPrev');
    const btnNext = document.getElementById('pbsNext');

    let currentGallery = null;
    let currentIndex = 0;

    function openLightbox(galleryName, index){
      currentGallery = galleryName;
      currentIndex = index;
      renderLightbox();
      lb.classList.add('is-open');
      lb.setAttribute('aria-hidden', 'false');
      document.body.style.overflow = 'hidden';
    }

    function closeLightbox(){
      lb.classList.remove('is-open');
      lb.setAttribute('aria-hidden', 'true');
      document.body.style.overflow = '';
    }

    function renderLightbox(){
      const items = galleries[currentGallery] || [];
      if (!items.length) return;
      const item = items[currentIndex];
      lbImg.src = item.src;
      lbImg.alt = item.alt;
      lbCap.textContent = item.alt;
    }

    function prev(){
      const items = galleries[currentGallery] || [];
      if (!items.length) return;
      currentIndex = (currentIndex - 1 + items.length) % items.length;
      renderLightbox();
    }

    function next(){
      const items = galleries[currentGallery] || [];
      if (!items.length) return;
      currentIndex = (currentIndex + 1) % items.length;
      renderLightbox();
    }

    document.querySelectorAll('.pbs-photo').forEach(btn => {
      btn.addEventListener('click', () => {
        openLightbox(btn.dataset.gallery, Number(btn.dataset.index || 0));
      });
    });

    btnClose.addEventListener('click', closeLightbox);
    btnPrev.addEventListener('click', prev);
    btnNext.addEventListener('click', next);

    lb.addEventListener('click', (e) => {
      if (e.target === lb) closeLightbox();
    });

    document.addEventListener('keydown', (e) => {
      if (!lb.classList.contains('is-open')) return;
      if (e.key === 'Escape') closeLightbox();
      if (e.key === 'ArrowLeft') prev();
      if (e.key === 'ArrowRight') next();
    });
  </script>

  <!-- STOP HERE (before CTA: Looking for Reliable Home Services?) -->
















  services 3rd selection  

 <!-- ===== CODE 3 (UPDATED): CTA + ONE PREMIUM FOOTER (REPLACES BOTH FOOTERS) ===== -->

<!-- CTA -->
<section class="cta">
  <div class="container">
    <h2>Looking for Reliable Home Services?</h2>
    <p>
      Contact us today for a free estimate. We focus on quality workmanship, transparent pricing, and customer satisfaction.
    </p>
    <div class="ehs-cta-actions">
      <a class="btn btn-primary" href="tel:+15196972361">Call Now</a>
      <a class="btn btn-outline" href="mailto:contact@elitehomeservices.ca">Email Us</a>
      <a class="btn btn-outline" href="https://wa.me/15198518887">WhatsApp</a>
    </div>
  </div>
</section>

<!-- PREMIUM FOOTER -->
<footer class="ehs-footer">
  <div class="container">
    <div class="ehs-footer-top">
      <!-- Brand / About -->
      <div class="ehs-footer-col ehs-footer-brand">
        <div class="ehs-footer-logo">Elite Home Services</div>
        <p class="ehs-footer-desc">
          Professional home improvement based in London, Ontario. We pride ourselves on clean finishing, reliable scheduling,
          and high-quality results for every homeowner.
        </p>

        <div class="ehs-footer-badges" aria-label="highlights">
          <span>Clean Finishing</span>
          <span>Reliable Scheduling</span>
          <span>Quality Results</span>
        </div>

        <div class="ehs-footer-social" aria-label="social links">
          <a class="ehs-social" href="#" aria-label="Facebook" title="Facebook">FB</a>
          <a class="ehs-social" href="#" aria-label="Instagram" title="Instagram">IG</a>
          <a class="ehs-social" href="https://wa.me/15198518887" aria-label="WhatsApp" title="WhatsApp">WA</a>
        </div>
      </div>

      <!-- Navigation -->
      <div class="ehs-footer-col">
        <h4 class="ehs-footer-title">Navigation</h4>

        <div class="ehs-footer-links">
          <ul>
            <li><a href="/">Home</a></li>
            <li><a href="/services/">Services</a></li>
            <li><a href="/projects/">Projects</a></li>
            <li><a href="/gallery/">Gallery</a></li>
          </ul>
          <ul>
            <li><a href="/about/">About Us</a></li>
            <li><a href="/faqs/">FAQs</a></li>
            <li><a href="/customer-reviews/">Reviews</a></li>
            <li><a href="/contact/">Contact</a></li>
          </ul>
        </div>
      </div>

      <!-- Contact -->
      <div class="ehs-footer-col">
        <h4 class="ehs-footer-title">Get In Touch</h4>

        <div class="ehs-footer-contact">
          <div class="ehs-contact-row">
            <span class="ehs-ico">📍</span>
            <div class="ehs-contact-text">1157 Oakcrossing Rd, London, ON N6H 0E9</div>
          </div>

          <div class="ehs-contact-row">
            <span class="ehs-ico">✉️</span>
            <div class="ehs-contact-text">
              <a href="mailto:contact@elitehomeservices.ca">contact@elitehomeservices.ca</a>
            </div>
          </div>

          <div class="ehs-team">
            <div class="ehs-team-card">
              <div class="ehs-team-name">Isa Hasan</div>
              <a class="ehs-team-phone" href="tel:+15196972361">(519) 697-2361</a>
            </div>

            <div class="ehs-team-card">
              <div class="ehs-team-name">Musa Hasan</div>
              <a class="ehs-team-phone" href="tel:+12265040348">(226) 504-0348</a>
            </div>

            <div class="ehs-team-card">
              <div class="ehs-team-name">Abdul Alali</div>
              <a class="ehs-team-phone" href="tel:+12264486508">(226) 448-6508</a>
            </div>
          </div>

          <div class="ehs-footer-mini-cta">
            <a class="ehs-mini-btn" href="/contact/">Request a Quote</a>
            <a class="ehs-mini-btn ehs-mini-btn-outline" href="mailto:contact@elitehomeservices.ca">Send Email</a>
          </div>
        </div>
      </div>
    </div>

    <div class="ehs-footer-bottom">
      <p>© <span id="ehs-year"></span> Elite Home Services. Serving Ontario with Excellence.</p>
    </div>
  </div>
</footer>

<style>
  /* CTA actions layout (keeps your existing CTA look, just improves button wrapping) */
  .ehs-cta-actions{
    display:flex;
    gap:10px;
    justify-content:center;
    flex-wrap:wrap;
    margin-top:12px;
  }

  /* PREMIUM FOOTER - matches your theme variables */
  .ehs-footer{
    background: var(--primary);
    color: var(--primary-foreground);
    border-top: 1px solid rgba(255,255,255,0.14);
    padding: 42px 0 18px;
  }

  .ehs-footer-top{
    display:grid;
    grid-template-columns: 1.15fr 0.9fr 1.2fr;
    gap: 24px;
    align-items:start;
  }

  .ehs-footer-col{
    background: rgba(255,255,255,0.06);
    border: 1px solid rgba(255,255,255,0.10);
    border-radius: 16px;
    padding: 16px;
  }

  .ehs-footer-brand{
    padding: 18px;
  }

  .ehs-footer-logo{
    font-family: 'Playfair Display', serif;
    font-size: 20px;
    font-weight: 700;
    letter-spacing: 0.3px;
    margin-bottom: 8px;
  }

  .ehs-footer-desc{
    opacity: 0.9;
    font-size: 13.5px;
    line-height: 1.7;
    margin-bottom: 14px;
    max-width: 52ch;
  }

  .ehs-footer-title{
    font-family: 'Inter', sans-serif;
    font-size: 14px;
    font-weight: 800;
    letter-spacing: 0.2px;
    margin: 0 0 12px 0;
    position: relative;
    padding-bottom: 10px;
  }

  .ehs-footer-title::after{
    content:"";
    position:absolute;
    left:0;
    bottom:0;
    width:42px;
    height:2px;
    background: var(--accent);
    border-radius: 999px;
  }

  /* badges */
  .ehs-footer-badges{
    display:flex;
    flex-wrap:wrap;
    gap:8px;
    margin-bottom: 12px;
  }
  .ehs-footer-badges span{
    font-size: 12px;
    font-weight: 700;
    padding: 8px 10px;
    border-radius: 999px;
    background: rgba(255,255,255,0.08);
    border: 1px solid rgba(255,255,255,0.12);
    color: var(--primary-foreground);
    opacity: 0.95;
  }

  /* social */
  .ehs-footer-social{
    display:flex;
    gap:10px;
    flex-wrap:wrap;
  }
  .ehs-social{
    width:40px;
    height:40px;
    display:inline-flex;
    align-items:center;
    justify-content:center;
    border-radius: 999px;
    text-decoration:none;
    font-weight: 900;
    font-size: 12px;
    color: var(--primary-foreground);
    background: rgba(255,255,255,0.08);
    border: 1px solid rgba(255,255,255,0.12);
    transition: transform .15s ease, opacity .15s ease, background .15s ease;
  }
  .ehs-social:hover{
    transform: translateY(-1px);
    background: rgba(255,255,255,0.14);
    opacity: 0.95;
  }

  /* footer links */
  .ehs-footer-links{
    display:grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px 18px;
  }

  .ehs-footer ul{ list-style:none; padding:0; margin:0; }
  .ehs-footer li{ margin-bottom: 10px; }

  .ehs-footer a{
    color: var(--primary-foreground);
    text-decoration:none;
    opacity: 0.9;
    font-size: 13.5px;
    font-weight: 600;
  }

  .ehs-footer a:hover{
    opacity: 1;
    text-decoration: underline;
  }

  /* contact rows */
  .ehs-footer-contact{ margin-top: 4px; }
  .ehs-contact-row{
    display:flex;
    gap:10px;
    align-items:flex-start;
    margin-bottom: 12px;
  }
  .ehs-ico{
    width:28px;
    height:28px;
    display:flex;
    align-items:center;
    justify-content:center;
    border-radius: 10px;
    background: rgba(255,255,255,0.08);
    border: 1px solid rgba(255,255,255,0.12);
    flex: 0 0 auto;
  }
  .ehs-contact-text{
    font-size: 13.5px;
    line-height: 1.55;
    opacity: 0.92;
  }

  /* team phones */
  .ehs-team{
    display:grid;
    grid-template-columns: 1fr;
    gap: 10px;
    margin-top: 12px;
  }
  .ehs-team-card{
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:10px;
    padding: 12px 12px;
    border-radius: 12px;
    background: rgba(0,0,0,0.12);
    border: 1px solid rgba(255,255,255,0.10);
  }
  .ehs-team-name{
    font-weight: 800;
    font-size: 13px;
    opacity: 0.95;
  }
  .ehs-team-phone{
    font-weight: 900;
    font-size: 13.5px;
    color: #fff;
    opacity: 0.95;
    white-space: nowrap;
  }

  /* mini CTA buttons inside footer */
  .ehs-footer-mini-cta{
    display:flex;
    gap:10px;
    flex-wrap:wrap;
    margin-top: 14px;
  }
  .ehs-mini-btn{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    padding: 10px 14px;
    border-radius: 999px;
    font-weight: 900;
    font-size: 13px;
    text-decoration:none;
    border: 1px solid rgba(255,255,255,0.18);
    background: var(--accent);
    color: #1f140f;
    transition: transform .15s ease, opacity .15s ease;
  }
  .ehs-mini-btn:hover{ transform: translateY(-1px); opacity: 0.95; }

  .ehs-mini-btn-outline{
    background: rgba(255,255,255,0.08);
    color: var(--primary-foreground);
  }

  /* bottom bar */
  .ehs-footer-bottom{
    border-top: 1px solid rgba(255,255,255,0.14);
    margin-top: 18px;
    padding-top: 14px;
    text-align:center;
    font-size: 12.5px;
    opacity: 0.78;
  }

  /* Responsive */
  @media (max-width: 980px){
    .ehs-footer-top{
      grid-template-columns: 1fr 1fr;
    }
  }
  @media (max-width: 680px){
    .ehs-footer-top{
      grid-template-columns: 1fr;
    }
    .ehs-footer-links{
      grid-template-columns: 1fr 1fr;
    }
    .ehs-team-card{
      flex-direction: column;
      align-items:flex-start;
    }
  }
  @media (max-width: 420px){
    .ehs-footer-links{ grid-template-columns: 1fr; }
  }
</style>

<script>
  // year
  (function(){
    var el = document.getElementById("ehs-year");
    if(el) el.textContent = new Date().getFullYear();
  })();
</script> 

  

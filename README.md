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

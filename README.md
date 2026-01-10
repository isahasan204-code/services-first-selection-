services  first selection   



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
      color:#ffffff;
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
    .hero h2{font-size:28px;line-height:1.15;margin-bottom:10px;color:#ffffff}
    .hero p{font-size:15.5px;color:#ffffff;opacity:1;margin-bottom:14px;max-width:60ch}
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
      color:#ffffff;
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
      color:#ffffff;
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
          <a class="pill" href="tel:+15198518887">📞 <strong>(519) 851-8887</strong></a>
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
          <a class="btn btn-primary" href="tel:+15198518887">Call Now</a>
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



 <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Elite Home Services | Portfolio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        :root { --elite-brown: #5D4037; }
        body { font-family: 'Inter', sans-serif; background-color: #ffffff; color: #1a1a1a; }
        
        /* Main Service Cards */
        .service-card {
            position: relative;
            height: 480px;
            border-radius: 24px;
            overflow: hidden;
            cursor: pointer;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        .service-card img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .service-card:hover img { transform: scale(1.1); }
        
        /* Text Overlay - Ensuring Titles are White */
        .service-overlay {
            position: absolute;
            inset: 0;
            background: linear-gradient(to top, rgba(0,0,0,0.85) 10%, rgba(0,0,0,0.3) 50%, transparent 100%);
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            padding: 40px;
        }
        
        /* White Title Style */
        .service-title {
            color: #ffffff !important;
            font-size: 1.875rem; /* 30px */
            font-weight: 800;
            margin-bottom: 0.75rem;
            text-shadow: 0 2px 4px rgba(0,0,0,0.3);
        }

        .service-desc {
            color: rgba(255, 255, 255, 0.9);
            font-size: 1rem;
            margin-bottom: 1.5rem;
        }

        /* Project Selection Modal */
        .modal {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(0,0,0,0.9);
            z-index: 1000;
            backdrop-filter: blur(10px);
            overflow-y: auto;
            padding: 20px;
        }
        .modal-content {
            background: white;
            max-width: 900px;
            margin: 50px auto;
            border-radius: 30px;
            padding: 40px;
            position: relative;
        }
        
        /* Two-Column Grid for 6 Photos */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }
        .gallery-grid img {
            width: 100%;
            height: 280px;
            object-fit: cover;
            border-radius: 16px;
            cursor: pointer;
            transition: transform 0.3s;
        }
        .gallery-grid img:hover { transform: scale(1.02); }

        /* Full Screen Lightbox */
        .lightbox {
            display: none;
            position: fixed;
            inset: 0;
            background: #000;
            z-index: 2000;
            justify-content: center;
            align-items: center;
        }
        .lightbox img { max-width: 95%; max-height: 85vh; border-radius: 4px; }
        .nav-btn {
            position: absolute;
            color: white;
            font-size: 60px;
            background: none;
            border: none;
            cursor: pointer;
            padding: 20px;
            user-select: none;
        }
    </style>



    <section class="py-20 px-6">
        <div class="max-w-7xl mx-auto">
            <h2 class="text-5xl font-black text-center mb-16 tracking-tight text-stone-900">Our Professional Home Services</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
                
                <div class="service-card" onclick="openModal('painting')">
                    <img src="https://images.unsplash.com/photo-1721901950428-56e381bfc8fe?q=80&amp;w=1170&amp;auto=format&amp;fit=crop&amp;ixlib=rb-4.1.0&amp;ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Painting">
                    <div class="service-overlay">
                        <h3 class="service-title">Painting Project</h3>
                        <p class="service-desc">Expert interior and exterior painting with wall repairs and smooth wood finishing.</p>
                        <button class="bg-white text-black font-bold py-3 px-8 rounded-full w-fit hover:bg-[#5D4037] hover:text-white transition-all">View Projects</button>
                    </div>
                </div>

                <div class="service-card" onclick="openModal('flooring')">
                    <img src="https://images.unsplash.com/photo-1581858726788-75bc0f6a952d?q=80&amp;w=687&amp;auto=format&amp;fit=crop&amp;ixlib=rb-4.1.0&amp;ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Flooring">
                    <div class="service-overlay">
                        <h3 class="service-title">Flooring Project</h3>
                        <p class="service-desc">Expert laminate and vinyl flooring installation with precise alignment and removal.</p>
                        <button class="bg-white text-black font-bold py-3 px-8 rounded-full w-fit hover:bg-[#5D4037] hover:text-white transition-all">View Projects</button>
                    </div>
                </div>

                <div class="service-card" onclick="openModal('fence')">
                    <img src="https://plus.unsplash.com/premium_photo-1725408143029-d2e589ae5037?q=80&amp;w=1956&amp;auto=format&amp;fit=crop&amp;ixlib=rb-4.1.0&amp;ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Fence">
                    <div class="service-overlay">
                        <h3 class="service-title">Fence &amp; Gate Project</h3>
                        <p class="service-desc">Complete fence and gate installation, repair, and removal with durable materials.</p>
                        <button class="bg-white text-black font-bold py-3 px-8 rounded-full w-fit hover:bg-[#5D4037] hover:text-white transition-all">View Projects</button>
                    </div>
                </div>

                <div class="service-card" onclick="openModal('decor')">
                    <img src="https://i.pinimg.com/736x/42/4a/fc/424afc91e5642c3b1ba64d9ebfc2f5e6.jpg" alt="Decor">
                    <div class="service-overlay">
                        <h3 class="service-title">Wall &amp; Room Decoration</h3>
                        <p class="service-desc">Modern TV wall décor with LED lighting options and custom room features.</p>
                        <button class="bg-white text-black font-bold py-3 px-8 rounded-full w-fit hover:bg-[#5D4037] hover:text-white transition-all">View Projects</button>
                    </div>
                </div>

                <div class="service-card" onclick="openModal('laundry')">
                    <img src="https://i.pinimg.com/1200x/2f/36/75/2f3675dbbb87588a0ebcac9a9a1b3ede.jpg" alt="Laundry">
                    <div class="service-overlay">
                        <h3 class="service-title">Laundry Room Project</h3>
                        <p class="service-desc">Upgrade your laundry room with practical shelving and organization solutions.</p>
                        <button class="bg-white text-black font-bold py-3 px-8 rounded-full w-fit hover:bg-[#5D4037] hover:text-white transition-all">View Projects</button>
                    </div>
                </div>

                <div class="service-card" onclick="openModal('small')">
                    <img src="https://plus.unsplash.com/premium_photo-1680127401819-d9cac7c99dd3?w=1200" alt="Installation">
                    <div class="service-overlay">
                        <h4 class="service-title">Small Installations</h4>
                        <p class="service-desc">TV mounting, shelves, curtain rods, and other small home installations.</p>
                        <button class="bg-white text-black font-bold py-4 px-8 rounded-full w-fit hover:bg-[#5D4037] hover:text-white transition-all">View Projects</button>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <div id="projectModal" class="modal" onclick="closeModalOnOut(event)">
        <div class="modal-content">
            <button onclick="closeModal()" class="absolute top-6 right-8 text-4xl text-gray-400 hover:text-black">×</button>
            <h2 id="modalTitle" class="text-3xl font-black mb-10 text-center uppercase tracking-widest text-stone-800">Projects</h2>
            <div id="galleryGrid" class="gallery-grid">
                </div>
        </div>
    </div>

    <div id="lightbox" class="lightbox">
        <button onclick="closeLightbox()" class="absolute top-10 right-10 text-white text-5xl">×</button>
        <button onclick="prevImg()" class="nav-btn left-10">‹</button>
        <img id="lightboxImg" src="">
        <button onclick="nextImg()" class="nav-btn right-10">›</button>
    </div>

    <script>
        const projectData = {
            painting: ["https://images.unsplash.com/photo-1646592491465-884cd869ba7e?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", "https://images.unsplash.com/photo-1721901948510-e69c0eb88156?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", "https://images.unsplash.com/photo-1721901946103-55f0d09a0b1e?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", "https://images.unsplash.com/photo-1721901950428-56e381bfc8fe?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", "https://images.unsplash.com/photo-1668910235656-0f4dc37e0114?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", "https://images.unsplash.com/photo-1722650271185-46755e3b099a?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"],

            flooring: ["https://images.unsplash.com/photo-1581858726788-75bc0f6a952d?q=80&w=687&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", "https://images.unsplash.com/photo-1630699376289-b62375a35505?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", "https://images.unsplash.com/photo-1722603931789-aea8bd4f5d01?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", "https://images.unsplash.com/photo-1721739495220-20bf20b12173?q=80&w=687&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", "https://plus.unsplash.com/premium_photo-1744839107659-0c3475e53c4f?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1yZWxhdGVkfDh8fHxlbnwwfHx8fHw%3D", "https://plus.unsplash.com/premium_photo-1676823552681-bf1d1135fa2f?w=600&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1yZWxhdGVkfDE2fHx8ZW58MHx8fHx8"],
            
fence: ["https://media.istockphoto.com/id/1655896254/photo/nice-wooden-fence-around-house-wooden-fence-with-green-lawn-street-photo.jpg?s=612x612&w=0&k=20&c=MP1aodxGTTxmRps3eGatWgwv7QIZLJeyf-tCV0-bM94=", "https://media.istockphoto.com/id/2169166406/photo/big-new-wooden-fence-around-the-house-and-trees-street-photo-fencing-and-gates.jpg?s=612x612&w=0&k=20&c=9_mWTvmhFQ9-dI5TSSi-en9TnyE73GAjkI1AV_XUN3c=", "https://media.istockphoto.com/id/2169166406/photo/big-new-wooden-fence-around-the-house-and-trees-street-photo-fencing-and-gates.jpg?s=612x612&w=0&k=20&c=9_mWTvmhFQ9-dI5TSSi-en9TnyE73GAjkI1AV_XUN3c=", "https://media.istockphoto.com/id/183042127/photo/timber-fence.jpg?s=612x612&w=0&k=20&c=DWRq8b5mwC83p1QBKKAidaQHrvLPRjP8x9aPyWke5y0=", "https://media.istockphoto.com/id/1141372977/photo/rotten-tree-fell-on-the-top-of-a-fence-and-shattered-in-multiple-pieces-due-to-high-winds.jpg?s=612x612&w=0&k=20&c=VxQ4nPCdENogm6kM5_1viFZvMa_B8DhQX9uEj4oF8rk=", "https://media.istockphoto.com/id/940833722/photo/home-garden-backyard-cedar-wood-fence-with-gate-door.jpg?s=612x612&w=0&k=20&c=JLTHcGva1v0TyCFmccWN0bJh1OHKjeBG4dDHOxXgU6w="],
            
decor: ["https://i.pinimg.com/736x/be/67/7a/be677ab3acf6356b1de0f87bbd43812a.jpg", "https://i.pinimg.com/1200x/eb/d0/ad/ebd0ade3fd7cd8ff4621ef3f21ea8f4a.jpg", "https://i.pinimg.com/736x/07/bf/9a/07bf9a2ddc38589aacec79b9d7a1fa62.jpg", "https://i.pinimg.com/1200x/64/da/8f/64da8fa5868efcfe530a7fcb2d2f668c.jpg", "https://i.pinimg.com/736x/6b/10/28/6b10287c8c9d8c33afe704de265080fa.jpg", "https://i.pinimg.com/1200x/16/23/e4/1623e4dc2281a373f22409f73cf87c13.jpg"],
            
laundry: ["https://i.pinimg.com/1200x/70/3f/e0/703fe0fc150798ecbd7c850151716926.jpg", "https://i.pinimg.com/1200x/9a/c3/2b/9ac32ba8cb7e877b53a7f30d2c8d1476.jpg", "https://i.pinimg.com/1200x/f0/5c/88/f05c889db57eb4c651a87068fd220751.jpg", "https://i.pinimg.com/1200x/01/62/0d/01620dd6d208b0e5efbfbe5ea5f67f43.jpg", "https://i.pinimg.com/1200x/c7/b8/a0/c7b8a0cb3b7f84f5e900cae39a7c762b.jpg", "https://i.pinimg.com/736x/f5/50/fe/f550fec39d0e3dfe716d372d45cb812c.jpg"],
         
small: ["https://i.pinimg.com/1200x/86/5c/14/865c14f8c9eae155ffa896784aa2c5a2.jpg", "https://i.pinimg.com/736x/e9/e3/c3/e9e3c3c495e7c2e48b6a9c819c6fc721.jpg", "https://i.pinimg.com/736x/76/80/d4/7680d49cfd8fbc13bb2cbff2e4f0c9ee.jpg", "https://i.pinimg.com/1200x/be/e5/40/bee5400c018c43102a4345fad67b0339.jpg",
"https://i.pinimg.com/736x/9f/45/86/9f45868ba286f08bfd486dc93db8a538.jpg",
"https://i.pinimg.com/1200x/b7/e8/92/b7e8928b65c8821218431cde70bb6543.jpg", 
"https://i.pinimg.com/1200x/91/c6/a1/91c6a1944b992bbaff1dd4b4b0bc5223.jpg", "https://i.pinimg.com/736x/fd/45/05/fd4505c486928c1f76f48c5b863744bc.jpg"]
        };

        let currentGallery = [];
        let currentIndex = 0;

        function openModal(service) {
            const modal = document.getElementById('projectModal');
            const grid = document.getElementById('galleryGrid');
            const title = document.getElementById('modalTitle');
            
            currentGallery = projectData[service];
            title.innerText = service.charAt(0).toUpperCase() + service.slice(1) + " Projects";
            grid.innerHTML = "";
            
            currentGallery.forEach((imgSrc, index) => {
                const img = document.createElement('img');
                img.src = imgSrc;
                img.onclick = () => openLightbox(index);
                grid.appendChild(img);
            });
            
            modal.style.display = 'block';
            document.body.style.overflow = 'hidden';
        }

        function closeModal() {
            document.getElementById('projectModal').style.display = 'none';
            document.body.style.overflow = 'auto';
        }

        function closeModalOnOut(e) { if (e.target.id === 'projectModal') closeModal(); }

        function openLightbox(index) {
            currentIndex = index;
            const lb = document.getElementById('lightbox');
            const lbImg = document.getElementById('lightboxImg');
            lbImg.src = currentGallery[currentIndex];
            lb.style.display = 'flex';
        }

        function closeLightbox() { document.getElementById('lightbox').style.display = 'none'; }
        function nextImg() { currentIndex = (currentIndex + 1) % currentGallery.length; document.getElementById('lightboxImg').src = currentGallery[currentIndex]; }
        function prevImg() { currentIndex = (currentIndex - 1 + currentGallery.length) % currentGallery.length; document.getElementById('lightboxImg').src = currentGallery[currentIndex]; }
    </script>












    services Footer selection  



 <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Elite Home Services Footer</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&amp;display=swap" rel="stylesheet">
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
        }
    </style>



    <section class="py-12 text-white" style="background: linear-gradient(135deg, rgb(93,64,55) 0%, rgb(120,85,70) 50%, rgb(196,120,74) 100%);">
        <div class="container max-w-4xl mx-auto px-4 text-center">
            <h2 class="text-3xl md:text-4xl font-bold mb-4">Looking for Reliable Home Services?</h2>
            <p class="text-base md:text-lg opacity-90 mb-10 max-w-2xl mx-auto">
                Contact us today for a free estimate. We focus on quality workmanship, transparent pricing, and customer satisfaction.
            </p>
            
            <div class="flex flex-col justify-center items-center gap-3 mb-16">
                <a href="tel:+15198518887" class="flex items-center gap-2 bg-white/10 hover:bg-white/20 border border-white/20 rounded-full px-4 py-2 transition-all duration-300 hover:scale-105 text-sm md:text-base">
                    <span class="w-7 h-7 rounded-full bg-green-500 flex items-center justify-center flex-shrink-0">
                        <svg class="h-4 w-4 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path>
                        </svg>
                    </span>
                    <span class="font-bold">Call Now</span>
                </a>

                <a href="mailto:contact@elitehomeservices.ca" class="flex items-center gap-2 bg-white/10 hover:bg-white/20 border border-white/20 rounded-full px-4 py-2 transition-all duration-300 hover:scale-105 text-sm md:text-base">
                    <span class="w-7 h-7 rounded-full bg-amber-600 flex items-center justify-center flex-shrink-0">
                        <svg class="h-4 w-4 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                        </svg>
                    </span>
                    <span class="font-bold">Email Us</span>
                </a>

                <a href="https://wa.me/15198518887" class="flex items-center gap-2 bg-white/10 hover:bg-white/20 border border-white/20 rounded-full px-4 py-2 transition-all duration-300 hover:scale-105 text-sm md:text-base">
                    <span class="w-7 h-7 rounded-full bg-emerald-500 flex items-center justify-center flex-shrink-0">
                        <svg class="h-4 w-4 text-white" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.890-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"></path>
                        </svg>
                    </span>
                    <span class="font-bold">WhatsApp</span>
                </a>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 text-left border-t border-white/10 pt-12">
                
                <div class="bg-white/5 backdrop-blur-sm border border-white/10 rounded-2xl p-6">
                    <div class="text-2xl font-bold mb-4" style="font-family: 'Playfair Display', serif;">Elite Home Services</div>
                    <p class="opacity-80 text-sm leading-relaxed mb-4">
                        Professional home improvement based in London, Ontario. We pride ourselves on clean finishing and reliable scheduling.
                    </p>
                    <div class="flex flex-wrap gap-2 mb-4">
                        <span class="text-xs font-bold px-3 py-1 rounded-full bg-white/10 border border-white/20">Clean Finishing</span>
                        <span class="text-xs font-bold px-3 py-1 rounded-full bg-white/10 border border-white/20">Reliable Scheduling</span>
                        <span class="text-xs font-bold px-3 py-1 rounded-full bg-white/10 border border-white/20">Quality Results</span>
                    </div>
                </div>

                <div class="bg-white/5 backdrop-blur-sm border border-white/10 rounded-2xl p-6">
                    <h4 class="text-base font-bold mb-4 pb-2 border-b border-amber-400 inline-block">Navigation</h4>
                    <div class="grid grid-cols-2 gap-4">
                        <ul class="space-y-2 text-sm opacity-80">
                            <li><a href="/" class="hover:underline hover:opacity-100">Home</a></li>
                            <li><a href="/services/" class="hover:underline hover:opacity-100">Services</a></li>
                            <li><a href="/Our Projects/" class="hover:underline hover:opacity-100">Our Projects</a></li>
                        </ul>
                        <ul class="space-y-2 text-sm opacity-80">
                            <li><a href="/about/" class="hover:underline hover:opacity-100">About Us</a></li>
                            <li><a href="/faqs/" class="hover:underline hover:opacity-100">FAQs</a></li>
                            <li><a href="/customer-reviews/" class="hover:underline hover:opacity-100">Reviews</a></li>
                            <li><a href="/contact/" class="hover:underline hover:opacity-100">Contact</a></li>
                        </ul>
                    </div>
                </div>

                <div class="bg-white/5 backdrop-blur-sm border border-white/10 rounded-2xl p-6">
                    <h4 class="text-base font-bold mb-4 pb-2 border-b border-amber-400 inline-block">Our Team</h4>
                    
                    <div class="space-y-2">
                        <div class="flex justify-between items-center bg-black/20 p-3 rounded-lg border border-white/5">
                            <span class="text-sm font-bold">Isa Hasan</span>
                            <a href="tel:+15196972361" class="text-sm opacity-90 hover:text-amber-300 font-mono">(519) 697-2361</a>
                        </div>
                        <div class="flex justify-between items-center bg-black/20 p-3 rounded-lg border border-white/5">
                            <span class="text-sm font-bold">Musa Hasan</span>
                            <a href="tel:+12265040348" class="text-sm opacity-90 hover:text-amber-300 font-mono">(226) 504-0348</a>
                        </div>
                        <div class="flex justify-between items-center bg-black/20 p-3 rounded-lg border border-white/5">
                            <span class="text-sm font-bold">Abdul Alali</span>
                            <a href="tel:+12264486508" class="text-sm opacity-90 hover:text-amber-300 font-mono">(226) 448-6508</a>
                        </div>
                    </div>

                    <div class="mt-4 pt-4 border-t border-white/10 flex flex-col gap-2">
                        <div class="flex gap-2 items-center text-sm opacity-80">
                            <span>📍</span> 1157 Oakcrossing Rd, London, ON
                        </div>
                        <div class="flex gap-2 items-center text-sm opacity-80">
                            <span>✉️</span> contact@elitehomeservices.ca
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="mt-12 text-center text-xs opacity-50">
                © 2026 Elite Home Services. Serving Ontario with Excellence.
            </div>
        </div>
    </section>

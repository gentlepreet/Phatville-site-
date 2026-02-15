<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Phatville | Street Food & Catering</title>
  <meta name="description" content="Phatville serves bold, phat flavours. Street food, pop-ups, and catering across the same areas as Phat Buns. Order on Uber Eats or Deliveroo." />

  <style>
    :root{
      --bg:#0b0b0c; --card:#141416; --text:#f2f2f2; --muted:#b7b7b7;
      --accent:#ffcc00; --accent2:#ff4d6d; --radius:18px;
      --shadow: 0 12px 30px rgba(0,0,0,.35); --max: 1080px;
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial;
      background: radial-gradient(1200px 600px at 80% -10%, rgba(255,204,0,.22), transparent 60%),
                  radial-gradient(1000px 600px at 0% 10%, rgba(255,77,109,.18), transparent 55%),
                  var(--bg);
      color:var(--text); line-height:1.5;
    }
    a{color:inherit; text-decoration:none}
    .wrap{max-width:var(--max); margin:0 auto; padding:24px}
    .nav{
      position:sticky; top:0;
      backdrop-filter: blur(10px);
      background: rgba(11,11,12,.6);
      border-bottom:1px solid rgba(255,255,255,.06);
      z-index:10;
    }
    .nav-inner{display:flex; align-items:center; justify-content:space-between; gap:14px}
    .brand{display:flex; align-items:center; gap:10px; font-weight:800; letter-spacing:.3px}
    .logo{
      width:38px; height:38px; border-radius:12px;
      background: linear-gradient(135deg, var(--accent), var(--accent2));
      box-shadow: var(--shadow);
    }
    .links{display:flex; gap:16px; flex-wrap:wrap; align-items:center}
    .links a{opacity:.9; font-weight:600}
    .links a:hover{opacity:1; text-decoration:underline}
    .btn{
      display:inline-flex; align-items:center; justify-content:center;
      padding:12px 16px; border-radius:999px;
      border:1px solid rgba(255,255,255,.12);
      background: rgba(255,255,255,.06);
      font-weight:800;
      transition: transform .08s ease, background .2s ease;
      cursor:pointer;
    }
    .btn:hover{background: rgba(255,255,255,.1)}
    .btn:active{transform: translateY(1px)}
    .btn.primary{
      border-color: rgba(255,204,0,.55);
      background: linear-gradient(135deg, rgba(255,204,0,.92), rgba(255,77,109,.85));
      color:#121212;
    }

    .hero{
      padding:48px 0 22px;
      display:grid;
      grid-template-columns: 1.2fr .8fr;
      gap:24px;
      align-items:stretch;
    }
    @media (max-width: 900px){ .hero{grid-template-columns:1fr; padding-top:28px} }
    .h-card{
      background: rgba(20,20,22,.72);
      border:1px solid rgba(255,255,255,.08);
      border-radius: var(--radius);
      padding:26px;
      box-shadow: var(--shadow);
    }
    .kicker{color:var(--muted); font-weight:700; letter-spacing:.2px}
    h1{margin:10px 0 8px; font-size:48px; line-height:1.05}
    @media (max-width: 520px){h1{font-size:38px}}
    .lead{color:rgba(242,242,242,.9); font-size:18px; max-width:60ch}
    .cta{display:flex; gap:12px; flex-wrap:wrap; margin-top:18px}
    .pill-row{display:flex; gap:10px; flex-wrap:wrap; margin-top:18px}
    .pill{
      padding:9px 12px; border-radius:999px;
      border:1px solid rgba(255,255,255,.12);
      color:rgba(242,242,242,.9);
      background: rgba(255,255,255,.04);
      font-weight:700;
      font-size:13px;
    }
    .photo{
      border-radius: var(--radius);
      overflow:hidden;
      position:relative;
      min-height: 320px;
      background:
        radial-gradient(700px 380px at 30% 20%, rgba(255,204,0,.32), transparent 60%),
        radial-gradient(800px 420px at 80% 20%, rgba(255,77,109,.25), transparent 65%),
        linear-gradient(135deg, rgba(255,255,255,.06), rgba(255,255,255,0));
      border:1px solid rgba(255,255,255,.08);
      box-shadow: var(--shadow);
    }
    .photo .tag{
      position:absolute; left:16px; bottom:16px;
      padding:10px 12px;
      border-radius:14px;
      background: rgba(0,0,0,.45);
      border:1px solid rgba(255,255,255,.12);
      color:rgba(242,242,242,.95);
      font-weight:800;
    }

    section{padding:22px 0}
    .section-title{display:flex; align-items:flex-end; justify-content:space-between; gap:16px; margin-bottom:12px}
    .section-title h2{margin:0; font-size:26px}
    .section-title p{margin:0; color:var(--muted); max-width:72ch}
    .grid{display:grid; grid-template-columns: repeat(3, 1fr); gap:14px}
    @media (max-width: 900px){.grid{grid-template-columns:1fr}}
    .card{
      background: rgba(20,20,22,.72);
      border:1px solid rgba(255,255,255,.08);
      border-radius: var(--radius);
      padding:18px;
    }
    .card h3{margin:0 0 6px}
    .card p{margin:0; color:rgba(242,242,242,.86)}
    .muted{color:var(--muted)}
    .menu{display:grid; grid-template-columns: 1fr 1fr; gap:14px}
    @media (max-width: 900px){.menu{grid-template-columns:1fr}}
    .item{
      padding:16px; border-radius: var(--radius);
      border:1px solid rgba(255,255,255,.08);
      background: rgba(255,255,255,.03);
      display:flex; justify-content:space-between; gap:12px; align-items:flex-start;
    }
    .item b{display:block; margin-bottom:4px}
    .price{
      font-weight:900; color:#111;
      background: linear-gradient(135deg, var(--accent), var(--accent2));
      padding:6px 10px; border-radius:999px; white-space:nowrap
    }
    .fine{font-size:13px; color:var(--muted)}
    .split{display:grid; grid-template-columns: 1fr 1fr; gap:14px; align-items:stretch}
    @media (max-width: 900px){.split{grid-template-columns:1fr}}
    form{display:grid; gap:10px}
    input, textarea, select{
      width:100%; padding:12px 12px;
      border-radius:12px;
      border:1px solid rgba(255,255,255,.12);
      background: rgba(0,0,0,.22);
      color:var(--text); outline:none;
    }
    textarea{min-height:120px; resize:vertical}
    .locs{display:flex; gap:10px; flex-wrap:wrap; margin-top:10px}
    .loc{
      padding:8px 12px; border-radius:999px;
      border:1px solid rgba(255,255,255,.12);
      background: rgba(255,255,255,.04);
      font-weight:750; font-size:13px; color:rgba(242,242,242,.92);
    }
    .foot{
      margin-top:26px; padding:22px 0 12px;
      border-top:1px solid rgba(255,255,255,.08);
      color:var(--muted);
      display:flex; justify-content:space-between; flex-wrap:wrap; gap:10px;
      font-size:14px;
    }
  </style>
</head>

<body>
  <!-- Your ordering links -->
  <script>
    const UBER_EATS_URL = "https://www.ubereats.com/gb/store/phat-ville-wolverhampton/gTlUj8n7VP6IMmSs4au8zA?srsltid=AfmBOopJzItnUVkM29Nt0men-SSBVLUopB9d3Ea_jJJvHgIKKoeJ-Qey";
    const DELIVEROO_URL = "https://deliveroo.co.uk/menu/birmingham/wolverhampton-city-centre/phatville-wolverhampton";
  </script>

  <div class="nav">
    <div class="wrap nav-inner">
      <div class="brand">
        <div class="logo" aria-hidden="true"></div>
        <div>PHATVILLE</div>
      </div>
      <div class="links">
        <a href="#menu">Menu</a>
        <a href="#catering">Catering</a>
        <a href="#areas">Areas</a>
        <a href="https://instagram.com/phatville" target="_blank" rel="noreferrer" class="btn">Instagram</a>
        <a href="#order" class="btn primary">Order</a>
      </div>
    </div>
  </div>

  <div class="wrap">
    <div class="hero">
      <div class="h-card">
        <div class="kicker">Street food • Pop-ups • Catering</div>
        <h1>Big flavour.<br/>Phat portions.</h1>
        <p class="lead">
          Phatville serves bold, feel-good food made fresh. We operate across <b>the same areas as Phat Buns</b>.
          Order on <b>Uber Eats</b> or <b>Deliveroo</b>, or message us for catering.
        </p>
        <div class="cta">
          <a class="btn primary" href="#order">Order now</a>
          <a class="btn" href="https://instagram.com/phatville" target="_blank" rel="noreferrer">Follow @phatville</a>
          <a class="btn" href="#contact">Catering enquiry</a>
        </div>
        <div class="pill-row">
          <span class="pill">Fresh & made-to-order</span>
          <span class="pill">Vegan options</span>
          <span class="pill">Halal options</span>
          <span class="pill">Event catering</span>
        </div>
      </div>

      <div class="photo" role="img" aria-label="Phatville food hero image placeholder">
        <div class="tag">Drop your best food photo here</div>
      </div>
    </div>

    <section id="menu">
      <div class="section-title">
        <div>
          <h2>Menu highlights</h2>
          <p>Replace these example items with your real best-sellers.</p>
        </div>
      </div>

      <div class="menu">
        <div class="item">
          <div>
            <b>Phat Chicken Box</b>
            <div class="muted">Crispy chicken, seasoned fries, slaw, signature sauce.</div>
            <div class="fine">Allergens: gluten, dairy (edit as needed)</div>
          </div>
          <div class="price">£9.50</div>
        </div>

        <div class="item">
          <div>
            <b>Loaded Fries (V)</b>
            <div class="muted">Fries loaded with cheese sauce, jalapeños, house spice.</div>
            <div class="fine">Make it vegan: swap sauce</div>
          </div>
          <div class="price">£6.50</div>
        </div>

        <div class="item">
          <div>
            <b>Phat Burger</b>
            <div class="muted">Juicy patty, melted cheese, pickles, sauce, toasted bun.</div>
            <div class="fine">Add-ons: bacon / extra patty</div>
          </div>
          <div class="price">£8.95</div>
        </div>

        <div class="item">
          <div>
            <b>Cauli Bites (VG)</b>
            <div class="muted">Crispy cauliflower bites with sticky glaze.</div>
            <div class="fine">Crowd favourite</div>
          </div>
          <div class="price">£6.95</div>
        </div>
      </div>
    </section>

    <section id="catering">
      <div class="section-title">
        <div>
          <h2>Catering & events</h2>
          <p>Weddings, birthdays, office lunches, festivals — we’ll bring the vibes and the food.</p>
        </div>
      </div>

      <div class="grid">
        <div class="card">
          <h3>Private events</h3>
          <p>Custom menus, dietary options, and smooth service so you can enjoy your day.</p>
        </div>
        <div class="card">
          <h3>Corporate</h3>
          <p>Feed the team with crowd-pleasers. Easy set-up, clear pricing, fast turnaround.</p>
        </div>
        <div class="card">
          <h3>Pop-ups</h3>
          <p>Let’s collaborate. We love partnering with venues, markets, and community events.</p>
        </div>
      </div>
    </section>

    <section id="areas">
      <div class="section-title">
        <div>
          <h2>Areas we cover</h2>
          <p>Phatville operates in the same areas as Phat Buns. If you’re nearby, we can usually make it happen.</p>
        </div>
      </div>

      <div class="card">
        <h3>Core areas</h3>
        <div class="locs" aria-label="Areas we cover">
          <span class="loc">Birmingham</span>
          <span class="loc">Coventry</span>
          <span class="loc">Derby</span>
          <span class="loc">Forest Gate</span>
          <span class="loc">Hounslow</span>
          <span class="loc">Leicester</span>
          <span class="loc">Liverpool</span>
          <span class="loc">Loughborough</span>
          <span class="loc">Lozells</span>
          <span class="loc">Mansfield</span>
          <span class="loc">Nottingham</span>
          <span class="loc">Nuneaton</span>
          <span class="loc">London (Palmers Green)</span>
          <span class="loc">Preston</span>
          <span class="loc">Sheffield</span>
          <span class="loc">Slough</span>
          <span class="loc">Wolverhampton</span>
          <span class="loc">Romford (coming soon)</span>
        </div>
      </div>
    </section>

    <section id="order">
      <div class="section-title">
        <div>
          <h2>Order now</h2>
          <p>Choose your platform:</p>
        </div>
      </div>

      <div class="split">
        <div class="card">
          <h3>Delivery</h3>
          <p class="muted">Order for delivery on Uber Eats or Deliveroo.</p>

          <div class="cta" style="margin-top:12px">
            <a class="btn primary" href="https://www.ubereats.com/gb/store/phat-ville-wolverhampton/gTlUj8n7VP6IMmSs4au8zA?srsltid=AfmBOopJzItnUVkM29Nt0men-SSBVLUopB9d3Ea_jJJvHgIKKoeJ-Qey" target="_blank" rel="noreferrer">
              Order on Uber Eats
            </a>

            <a class="btn" href="https://deliveroo.co.uk/menu/birmingham/wolverhampton-city-centre/phatville-wolverhampton" target="_blank" rel="noreferrer">
              Order on Deliveroo
            </a>
          </div>
        </div>

        <div class="card">
          <h3>For updates</h3>
          <p class="muted">Locations and specials drop on Instagram first.</p>
          <div class="cta" style="margin-top:12px">
            <a class="btn" href="https://instagram.com/phatville" target="_blank" rel="noreferrer">Follow @phatville</a>
            <a class="btn" href="#contact">Catering enquiry</a>
          </div>
        </div>
      </div>
    </section>

    <section id="contact">
      <div class="section-title">
        <div>
          <h2>Contact Phatville</h2>
          <p>Fastest way: Instagram DMs. For catering, use the form.</p>
        </div>
      </div>

      <div class="split">
        <div class="card">
          <h3>Catering enquiry</h3>

          <!-- Option: Formspree (simple). Replace YOUR_ID with your Formspree form ID. -->
          <form action="https://formspree.io/f/YOUR_ID" method="POST">
            <input name="name" placeholder="Name" required />
            <input name="email" type="email" placeholder="Email" required />
            <select name="reason" required>
              <option value="" disabled selected>What’s this about?</option>
              <option>Catering / event</option>
              <option>Collab / pop-up</option>
              <option>General question</option>
            </select>
            <textarea name="message" placeholder="Date, area, guest count, and what you’re after…" required></textarea>
            <button class="btn primary" type="submit">Send enquiry</button>
            <div class="fine">Replace <b>YOUR_ID</b> with your Formspree ID (free tier works).</div>
          </form>
        </div>

        <div class="card">
          <h3>DM us</h3>
          <p class="muted">
            📱 Instagram: <b><a href="https://instagram.com/phatville" target="_blank" rel="noreferrer">@phatville</a></b><br/>
            🚚 Order: <b><a href="https://www.ubereats.com/gb/store/phat-ville-wolverhampton/gTlUj8n7VP6IMmSs4au8zA?srsltid=AfmBOopJzItnUVkM29Nt0men-SSBVLUopB9d3Ea_jJJvHgIKKoeJ-Qey" target="_blank" rel="noreferrer">Uber Eats</a></b>
            + <b><a href="https://deliveroo.co.uk/menu/birmingham/wolverhampton-city-centre/phatville-wolverhampton" target="_blank" rel="noreferrer">Deliveroo</a></b><br/>
            📍 Areas: same as <b>Phat Buns</b>
          </p>

          <div class="cta" style="margin-top:12px">
            <a class="btn primary" href="https://instagram.com/phatville" target="_blank" rel="noreferrer">Message on Instagram</a>
            <a class="btn" href="#order">Order now</a>
          </div>
        </div>
      </div>
    </section>

    <div class="foot">
      <div>© <span id="year"></span> Phatville. All rights reserved.</div>
      <div class="muted">One-page site • Mobile-friendly</div>
    </div>
  </div>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>

# portfolio-<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Dinesh — Creative Graphic Designer</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&family=Playfair+Display:wght@600;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0b0b0f;
      --card:#0f1116;
      --muted:rgba(255,255,255,0.72);
      --accent1:#ff6b6b;
      --accent2:#7c5cff;
      --glass: rgba(255,255,255,0.04);
    }
    *{box-sizing:border-box}
    html,body{height:100%;}
    body{
      margin:0;
      font-family:Inter,system-ui,Segoe UI,Roboto,"Helvetica Neue",Arial;
      background: radial-gradient(1200px 600px at 10% 10%, rgba(124,92,255,0.14), transparent 6%),
                  radial-gradient(900px 400px at 90% 90%, rgba(255,107,107,0.08), transparent 6%),
                  var(--bg);
      color:#fff;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      padding:36px;
    }
    .container{max-width:1100px;margin:0 auto}

    /* Header */
    header{display:flex;align-items:center;justify-content:space-between;margin-bottom:28px}
    .brand{display:flex;gap:14px;align-items:center}
    .logo{width:56px;height:56px;border-radius:12px;background:linear-gradient(135deg,var(--accent2),var(--accent1));display:flex;align-items:center;justify-content:center;font-weight:800;font-family:'Playfair Display',serif;color:white;box-shadow:0 8px 30px rgba(0,0,0,0.6)}
    .brand h1{font-size:20px;margin:0}
    .brand p{margin:0;font-size:12px;color:var(--muted)}
    nav{display:flex;gap:12px}
    .btn{background:transparent;border:1px solid rgba(255,255,255,0.06);padding:10px 14px;border-radius:10px;color:var(--muted);font-weight:600;cursor:pointer}

    /* Hero */
    .hero{display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center;margin-bottom:36px}
    .hero-left h2{font-family:'Playfair Display',serif;font-size:44px;margin:0 0 10px 0}
    .hero-left p{color:var(--muted);margin:0 0 20px 0;font-size:16px;line-height:1.5}
    .cta-row{display:flex;gap:12px;align-items:center}
    .primary{background:linear-gradient(90deg,var(--accent2),var(--accent1));border:none;padding:14px 18px;border-radius:12px;color:#fff;font-weight:700;cursor:pointer;box-shadow:0 12px 30px rgba(124,92,255,0.12)}
    .secondary{background:transparent;border:1px solid rgba(255,255,255,0.06);padding:12px 16px;border-radius:10px;color:var(--muted);cursor:pointer}

    /* glass card */
    .card{
      background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border-radius:16px;padding:18px;backdrop-filter:blur(6px);border:1px solid rgba(255,255,255,0.04)
    }

    /* Portrait area */
    .portrait{height:340px;border-radius:14px;background:linear-gradient(135deg, rgba(124,92,255,0.16), rgba(255,107,107,0.12));display:flex;align-items:center;justify-content:center;position:relative;overflow:hidden}
    .portrait .blob{position:absolute;width:220px;height:220px;border-radius:50%;filter:blur(40px);opacity:0.65}
    .blob.b1{background:linear-gradient(90deg,#7c5cff,#7ce8ff);left:-40px;top:-30px}
    .blob.b2{background:linear-gradient(90deg,#ff6b6b,#ffd36b);right:-40px;bottom:-30px}
    .avatar{width:160px;height:160px;border-radius:10px;background:linear-gradient(180deg,#222,#111);display:flex;align-items:center;justify-content:center;font-weight:700;font-size:28px;color:white;z-index:2;box-shadow:0 10px 40px rgba(0,0,0,0.5)}

    /* Sections */
    section{margin-bottom:28px}
    .section-title{display:flex;align-items:center;gap:12px;margin-bottom:12px}
    .section-title h3{margin:0;font-size:18px}
    .section-title p{margin:0;color:var(--muted);font-size:13px}

    /* Skills */
    .skills{display:flex;gap:12px;flex-wrap:wrap}
    .skill{background:var(--glass);padding:10px 12px;border-radius:10px;border:1px solid rgba(255,255,255,0.03);font-weight:600}

    /* Projects grid */
    .projects-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
    .project{padding:14px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);cursor:pointer;transition:transform .28s ease, box-shadow .28s ease}
    .project:hover{transform:translateY(-8px);box-shadow:0 20px 60px rgba(0,0,0,0.6)}
    .project img{width:100%;height:140px;object-fit:cover;border-radius:8px;margin-bottom:10px}
    .project h4{margin:0 0 6px 0}
    .project p{margin:0;color:var(--muted);font-size:13px}

    /* Contact */
    .contact-grid{display:grid;grid-template-columns:1fr 320px;gap:18px}
    form input, form textarea{width:100%;padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,0.04);background:transparent;color:white;margin-bottom:10px}
    form button{width:100%;padding:12px;border-radius:10px;border:none;background:linear-gradient(90deg,var(--accent2),var(--accent1));font-weight:700;color:white;cursor:pointer}

    /* footer */
    footer{margin-top:30px;color:var(--muted);font-size:13px;text-align:center}

    /* Responsive */
    @media (max-width:980px){
      .hero{grid-template-columns:1fr}
      .projects-grid{grid-template-columns:repeat(2,1fr)}
      .contact-grid{grid-template-columns:1fr}
    }
    @media (max-width:600px){
      body{padding:20px}
      .projects-grid{grid-template-columns:1fr}
      .logo{width:44px;height:44px;font-size:16px}
      .hero-left h2{font-size:32px}
    }

    /* subtle animated dots */
    .dot{position:absolute;width:8px;height:8px;border-radius:50%;opacity:0.7}
    .dot.d1{left:8%;top:6%;background:#7c5cff;animation:float 6s ease-in-out infinite}
    .dot.d2{left:52%;top:2%;background:#ff6b6b;animation:float 5s ease-in-out infinite}
    .dot.d3{left:88%;top:26%;background:#ffd36b;animation:float 7s ease-in-out infinite}
    @keyframes float{0%{transform:translateY(0)}50%{transform:translateY(-18px)}100%{transform:translateY(0)}}

  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">DK</div>
        <div>
          <h1>Dinesh — Graphic Designer</h1>
          <p>Animation • VFX • UI/UX • Industrial Design</p>
        </div>
      </div>
      <nav>
        <button class="btn">Portfolio</button>
        <button class="btn">About</button>
        <button class="btn">Contact</button>
      </nav>
    </header>

    <main>
      <section class="hero">
        <div class="hero-left">
          <h2>Creative Visuals that tell a story</h2>
          <p>I design motion-rich visuals, characters, and polished interfaces. I blend animation techniques with practical design to create work that feels alive.</p>
          <div class="cta-row">
            <button class="primary" onclick="location.href='#contact'">Hire me</button>
            <button class="secondary" onclick="location.href='#projects'">See projects</button>
          </div>

          <div style="margin-top:22px;" class="card">
            <div style="display:flex;justify-content:space-between;align-items:center">
              <div>
                <div style="font-size:13px;color:var(--muted)">Located</div>
                <div style="font-weight:700">Chennai, India</div>
              </div>
              <div>
                <div style="font-size:13px;color:var(--muted)">Availability</div>
                <div style="font-weight:700;color:#bfe9ff">Open to work</div>
              </div>
            </div>
          </div>
        </div>

        <div>
          <div class="card portrait">
            <div class="blob b1"></div>
            <div class="blob b2"></div>
            <div class="avatar">DK</div>
          </div>
        </div>
      </section>

      <section id="about">
        <div class="section-title"><h3>About</h3><p>Who I am &amp; what I do</p></div>
        <div class="card">
          <p style="margin:0;color:var(--muted);line-height:1.6">I’m Dinesh — a B.Sc Graphics, Animation &amp; VFX student with a passion for industrial design and motion. I craft brand stories using motion, illustration and interface design. I focus on clarity and personality: clean visuals, readable typography, and delightful motion.</p>
        </div>
      </section>

      <section>
        <div class="section-title"><h3>Skills</h3><p>Tools & strengths</p></div>
        <div class="skills">
          <div class="skill">After Effects</div>
          <div class="skill">Photoshop</div>
          <div class="skill">Illustrator</div>
          <div class="skill">Unreal Engine</div>
          <div class="skill">Figma</div>
          <div class="skill">3D &amp; Modeling</div>
        </div>
      </section>

      <section id="projects">
        <div class="section-title"><h3>Selected Projects</h3><p>Motion • VFX • UI</p></div>
        <div class="projects-grid">
          <div class="project card">
            <img src="https://images.unsplash.com/photo-1547658719-da2b51169166?q=80&w=1400&auto=format&fit=crop&ixlib=rb-4.0.3&s=9cde3fe2c7d2b3b8b7b2e66f2a6f8f4d" alt="project">
            <h4>Car-Wheel Health Explainer</h4>
            <p>A short 2D explainer using wheels as UI metaphors for body functions (diabetes awareness).</p>
          </div>
          <div class="project card">
            <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?q=80&w=1400&auto=format&fit=crop&ixlib=rb-4.0.3&s=8f7a6cec2c4c5b6d0a8a7f33c8c9f9a7" alt="project">
            <h4>Motion Poster Series</h4>
            <p>Animated poster set for a local festival — bold typography and kinetic rhythm.</p>
          </div>
          <div class="project card">
            <img src="https://images.unsplash.com/photo-1503602642458-232111445657?q=80&w=1400&auto=format&fit=crop&ixlib=rb-4.0.3&s=6a9d3b2d8c8fb6d6eef2c9b1e3b2a7a9" alt="project">
            <h4>UI Micro-interactions</h4>
            <p>Small, delightful UI interactions for a mobile onboarding flow.</p>
          </div>
        </div>
      </section>

      <section id="contact">
        <div class="section-title"><h3>Contact</h3><p>Let's make something together</p></div>
        <div class="contact-grid">
          <div class="card">
            <p style="margin-top:0;color:var(--muted)">I’m available for freelance and full-time roles. Tell me about your project: timeline, budget, and goals.</p>
            <div style="display:flex;gap:12px;margin-top:14px">
              <div style="flex:1">
                <div style="font-size:13px;color:var(--muted)">Email</div>
                <div style="font-weight:700">dinesh@example.com</div>
              </div>
              <div style="flex:1">
                <div style="font-size:13px;color:var(--muted)">Phone</div>
                <div style="font-weight:700">+91 9XXXXXXXX</div>
              </div>
            </div>
            <div style="margin-top:12px;color:var(--muted);font-size:13px">Or connect on social:</div>
            <div style="display:flex;gap:10px;margin-top:8px">
              <a class="btn" href="#">Dribbble</a>
              <a class="btn" href="#">Behance</a>
              <a class="btn" href="#">LinkedIn</a>
            </div>
          </div>

          <form class="card" action="mailto:dinesh@example.com" method="post" enctype="text/plain">
            <input name="name" placeholder="Your name" required>
            <input name="email" placeholder="Your email" required>
            <textarea name="message" placeholder="Brief message" rows="5" required></textarea>
            <button type="submit">Send message</button>
          </form>
        </div>
      </section>

      <footer>
        <div>&copy; <span id="year"></span> Dinesh — Designed &amp; animated by me</div>
      </footer>
    </main>

    <div class="dot d1"></div>
    <div class="dot d2"></div>
    <div class="dot d3"></div>

  </div>

  <script>
    document.getElementById('year').innerText = new Date().getFullYear();
  </script>
</body>
</html>

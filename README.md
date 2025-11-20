<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Nahidul Islam — MIS Executive</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg-gradient: linear-gradient(135deg,#0f172a 0%,#0b2545 50%,#0b3a6b 100%);
      --card-bg: rgba(255,255,255,0.06);
      --glass-border: rgba(255,255,255,0.12);
      --accent: #60a5fa; /* light blue */
      --muted: rgba(255,255,255,0.75);
      --glass-strong: rgba(255,255,255,0.08);
    }
    *{box-sizing:border-box}
    body{margin:0;font-family:'Poppins',system-ui,Arial;background:var(--bg-gradient);color:var(--muted);-webkit-font-smoothing:antialiased;min-height:100vh}

    /* page container */
    .wrap{max-width:1100px;margin:48px auto;padding:20px}

    /* header */
    .hero{display:grid;grid-template-columns:160px 1fr;gap:28px;align-items:center;padding:28px;border-radius:16px;background:var(--card-bg);border:1px solid var(--glass-border);backdrop-filter:blur(10px) saturate(120%);box-shadow:0 8px 30px rgba(2,6,23,0.6);}
    .avatar{width:140px;height:140px;border-radius:50%;overflow:hidden;display:block;margin:auto;border:4px solid rgba(255,255,255,0.12);box-shadow:0 6px 20px rgba(2,6,23,0.6)}
    .hero h1{margin:0;font-size:26px;color:#fff;font-weight:700}
    .hero p{margin:6px 0;color:rgba(255,255,255,0.85)}

    /* nav */
    .nav{display:flex;gap:12px;justify-self:end}
    .nav a{color:rgba(255,255,255,0.8);text-decoration:none;padding:8px 12px;border-radius:10px;font-weight:600}
    .nav a:hover{background:linear-gradient(90deg,rgba(255,255,255,0.06),rgba(255,255,255,0.02));box-shadow:inset 0 0 0 1px rgba(255,255,255,0.02)}

    /* layout sections */
    .grid{display:grid;grid-template-columns:1fr 360px;gap:28px;margin-top:28px}
    .card{background:var(--card-bg);border:1px solid var(--glass-border);border-radius:14px;padding:20px;backdrop-filter: blur(8px) saturate(120%);box-shadow:0 6px 18px rgba(2,6,23,0.5)}

    h2{color:#fff;margin:0 0 12px 0;font-size:20px}
    p{line-height:1.5;color:rgba(255,255,255,0.88)}
    ul{padding-left:18px}

    /* skills */
    .skills{display:flex;flex-wrap:wrap;gap:8px}
    .chip{background:linear-gradient(90deg,var(--accent),#3b82f6);color:#04263b;padding:8px 12px;border-radius:999px;font-weight:600;font-size:13px;box-shadow:0 6px 18px rgba(59,130,246,0.12)}

    /* projects grid */
    .projects{display:grid;grid-template-columns:repeat(2,1fr);gap:14px}
    .project{padding:14px;border-radius:12px;background:linear-gradient(180deg,rgba(255,255,255,0.03),rgba(255,255,255,0.02));border:1px solid rgba(255,255,255,0.04);transition:transform .28s ease,box-shadow .28s ease}
    .project:hover{transform:translateY(-8px);box-shadow:0 18px 40px rgba(2,6,23,0.6)}
    .project h3{margin:0 0 8px 0;color:#fff}

    /* right column */
    .side .card + .card{margin-top:18px}
    .meta{display:flex;flex-direction:column;gap:10px}
    .meta b{color:#fff}

    /* footer */
    footer{opacity:0.9;text-align:center;margin:34px 0;color:rgba(255,255,255,0.6)}

    /* buttons */
    .btn{display:inline-block;background:linear-gradient(90deg,#60a5fa,#3b82f6);color:#04263b;padding:10px 18px;border-radius:999px;text-decoration:none;font-weight:700}
    .outline{background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--muted);padding:8px 12px;border-radius:10px}

    /* responsive */
    @media(max-width:980px){
      .grid{grid-template-columns:1fr}
      .hero{grid-template-columns:120px 1fr}
      .projects{grid-template-columns:1fr}
    }

    @media(max-width:520px){
      .wrap{margin:18px}
      .hero{grid-template-columns:100px 1fr;padding:18px}
      .avatar{width:100px;height:100px}
      .nav{display:none}
    }

    /* subtle entrance animations */
    .fade-in{opacity:0;transform:translateY(10px);animation:enter .6s forwards}
    .delay-1{animation-delay:0.12s}
    .delay-2{animation-delay:0.24s}
    .delay-3{animation-delay:0.36s}

    @keyframes enter{to{opacity:1;transform:none}}

  </style>
</head>
<body>
  <div class="wrap">

    <!-- Header / Hero -->
    <header class="hero fade-in">
      <img class="avatar" src="me.png" alt="Nahidul Islam" />
      <div>
        <div style="display:flex;align-items:center;justify-content:space-between;gap:12px">
          <div>
            <h1>Nahidul Islam</h1>
            <p style="margin:6px 0 0;font-weight:600">MIS Executive — Labib Dyeing Mills Ltd (Labib Group)</p>
            <p style="margin:6px 0 0;font-size:13px;opacity:0.85">Since May 15, 2023 • Abdullahpur, Dhaka</p>
          </div>
          <nav class="nav">
            <a href="#about">About</a>
            <a href="#experience">Experience</a>
            <a href="#projects">Projects</a>
            <a href="#contact">Contact</a>
          </nav>
        </div>

        <div style="margin-top:12px;display:flex;gap:10px;align-items:center">
          <a class="btn" href="cv.pdf" download>Download CV</a>
          <a class="outline" href="mailto:meghnahid@gmail.com">Email</a>
          <div class="card fade-in">
</div>
        </div>
      </div>
    </header>

    <!-- Main content -->
    <main class="grid">
      <!-- left column -->
      <div>
        <!-- About -->
        <section id="about" class="card fade-in delay-1">
          <h2>About Me</h2>
          <p>I am <strong>Nahidul Islam</strong>, a dedicated MIS Executive with expertise in data analysis, MIS reporting, Power BI dashboards, and process optimisation. I turn raw operational data into clear, actionable insights that help management make better decisions.</p>
          <div style="margin-top:12px" class="skills">
            <span class="chip">MS Excel</span>
            <span class="chip">Power BI</span>
            <span class="chip">SQL</span>
            <span class="chip">ERP / CRM</span>
            <span class="chip">Reporting</span>
            <span class="chip">Project Mgmt</span>
          </div>
        </section>

        <!-- Experience -->
        <section id="experience" class="card fade-in delay-2" style="margin-top:18px">
          <h2>Experience</h2>

          <div style="margin-top:8px">
            <h3 style="color:#fff;margin:0">MIS Executive</h3>
            <p style="margin:6px 0 0;font-size:14px">Labib Dyeing Mills Ltd • <em>2023 – Present</em></p>
            <ul>
              <li>Analyze complex datasets and prepare management-ready MIS reports.</li>
              <li>Design & maintain automated dashboards (Excel, Power BI).</li>
              <li>Coordinate with multiple departments to ensure data accuracy.</li>
              <li>Present insights and KPI reports to senior management.</li>
            </ul>
          </div>

          <div style="margin-top:12px">
            <h3 style="color:#fff;margin:0">Tele Sales Executive</h3>
            <p style="margin:6px 0 0;font-size:14px">bdCalling IT Ltd • <em>2022 – 2023</em></p>
            <ul>
              <li>Generated leads, qualified prospects, and closed sales via phone.</li>
              <li>Maintained high customer satisfaction through tailored solutions.</li>
            </ul>
          </div>

          <div style="margin-top:12px">
            <h3 style="color:#fff;margin:0">Computer Operator</h3>
            <p style="margin:6px 0 0;font-size:14px">Goldenline Medical Center • <em>2020 – 2021</em></p>
            <ul>
              <li>Managed health information systems, accurate data entry and reporting.</li>
            </ul>
          </div>
        </section>

        <!-- Projects -->
        <section id="projects" class="card fade-in delay-3" style="margin-top:18px">
          <h2>Projects</h2>
          <div class="projects" style="margin-top:12px">
            <article class="project">
              <h3>Automated Daily Production Report</h3>
              <p>Excel + Power Query system that reduced manual workload by ~60% and improved accuracy of daily production figures.</p>
            </article>
            <article class="project">
              <h3>Production Dashboard (Power BI)</h3>
              <p>Interactive Power BI dashboard for production KPIs, efficiency and department performance monitoring.</p>
            </article>
            <article class="project">
              <h3>Inventory Monitoring Sheet</h3>
              <p>Smart Google Sheet tracker for real-time stock updates and automated alerts to procurement.</p>
            </article>
            <article class="project">
              <h3>MIS Automation Toolkit</h3>
              <p>Collection of templates and scripts to standardize MIS reporting across departments.</p>
            </article>
          </div>
        </section>

      </div>

      <!-- right column -->
      <aside class="side">
        <div class="card fade-in">
  <h2>Contact</h2>
  <div class="meta">
    <div><b>Email</b><div>meghnahid@gmail.com</div></div>
    <div><b>Phone</b><div>01609597666</div></div>
    <div><b>Location</b><div>Abdullahpur, Dhaka</div></div>
    
    <div>
        <b>GitHub</b>
        <div><a href="https://github.com/nahidkhan070/" style="color:var(--accent);text-decoration:none;" target="_blank">nahidkhan070</a></div>
    </div>
    
    <div>
        <b>LinkedIn</b>
        <div><a href="https://www.linkedin.com/in/nahidkhan0070" style="color:var(--accent);text-decoration:none;" target="_blank">Nahidul Islam</a></div>
    </div>
  </div>
</div>

        <div class="card fade-in" style="margin-top:18px">
          <h2>Education</h2>
          <p><b>B.Sc (CSE)</b><br>Bangabandhu Sheikh Mujibur Rahman Science & Technology University<br><em>2016 – 2017</em></p>
          <p><b>HSC (Science)</b><br>Birshreshtha Noor Mohammad Public College<br><em>2016</em></p>
        </div>

        <div class="card fade-in" style="margin-top:18px">
          <h2>Languages & Expertise</h2>
          <p><b>Languages:</b> Bangla (Main), English (Fluent), Hindi (Basic)</p>
          <p><b>Expertise:</b> Management, CRM, Microsoft Office, Communication & Negotiation</p>
        </div>
      </aside>
    </main>

    <footer>
      © 2025 <strong>Nahidul Islam</strong> • Crafted with care
    </footer>

  </div>

  <script>
    // Smooth scroll for navigation
    document.querySelectorAll('.nav a').forEach(a=>{
      a.addEventListener('click',function(e){
        e.preventDefault();
        const id = this.getAttribute('href');
        document.querySelector(id).scrollIntoView({behavior:'smooth',block:'start'});
      })
    })

    // Lazy animate on intersection
    const obs = new IntersectionObserver(entries=>{
      entries.forEach(ent=>{ if(ent.isIntersecting) ent.target.classList.add('visible') })
    },{threshold:0.12});
    document.querySelectorAll('.fade-in').forEach(el=>obs.observe(el));
  </script>
</body>
</html>

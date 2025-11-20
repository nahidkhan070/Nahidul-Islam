<html lang="en">
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <title>Nahidul Islam — MIS Executive & Data Analyst</title>
    <!-- Importing Poppins for Body Text & Playfair Display for Headings -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* --- 1. PREMIUM COLOR PALETTE & TYPOGRAPHY VARIABLES --- */
        :root{
            --bg-gradient: linear-gradient(135deg, #09090b 0%, #171717 50%, #202020 100%); /* Deep Graphite/Black */
            --card-bg: rgba(255,255,255,0.04);
            --glass-border: rgba(255,255,255,0.08);
            --accent: #3dc4ff; /* Luminous Teal */
            --accent-rgb: 61, 196, 255; /* RGB for the shadow glow */
            --muted: rgba(255,255,255,0.8);
            --header-font: 'Playfair Display', serif;
            --body-font: 'Poppins', system-ui, Arial;
        }
        
        /* --- 2. GLOBAL STYLES & RESET --- */
        *{box-sizing:border-box}
        body{
            margin:0;
            font-family:var(--body-font);
            background:var(--bg-gradient);
            color:var(--muted);
            -webkit-font-smoothing:antialiased;
            min-height:100vh;
            line-height:1.6;
        }

        /* --- 3. LAYOUT & CARDS --- */
        .wrap{max-width:1200px;margin:48px auto;padding:0 24px;}
        .grid{display:grid;grid-template-columns:1fr 360px;gap:40px;margin-top:40px}
        .card{
            background:var(--card-bg);
            border:1px solid var(--glass-border);
            border-radius:18px; /* Slightly more generous radius */
            padding:24px;
            backdrop-filter: blur(12px) saturate(150%);
            box-shadow:0 8px 30px rgba(0,0,0,0.5); /* Stronger shadow for depth */
        }
        
        /* --- 4. TYPOGRAPHY & HEADINGS --- */
        h1, h2, h3{
            font-family:var(--header-font);
            color:#fff;
            margin:0 0 16px 0;
            line-height:1.2;
        }
        h1{font-size:32px;}
        h2{font-size:24px; margin-bottom: 12px;}
        h3{font-size:18px;}
        p{margin:8px 0; color:rgba(255,255,255,0.85);}
        ul{padding-left:18px; margin-top: 4px; margin-bottom: 4px; font-size: 15px;}
        li {margin-bottom: 4px;}

        /* --- 5. HEADER/HERO SECTION --- */
        .hero{
            display:grid;
            grid-template-columns:160px 1fr;
            gap:36px;
            align-items:center;
            padding:32px;
            border-radius:20px;
            background:var(--card-bg);
            border:1px solid var(--glass-border);
            backdrop-filter:blur(12px) saturate(150%);
            box-shadow:0 12px 40px rgba(0,0,0,0.7);
        }
        .avatar{
            width:140px;
            height:140px;
            border-radius:50%;
            overflow:hidden;
            display:block;
            margin:auto;
            border:4px solid var(--accent); /* Accent border */
            box-shadow:0 0 10px 2px rgba(61, 196, 255, 0.4); /* Subtle glow */
            object-fit: cover;
        }
        .hero h1{margin:0;font-size:38px;color:#fff;font-weight:900;}
        .hero .job-title{margin:4px 0 0;font-weight:600;font-size:18px;color:var(--accent);}
        .hero .job-dates{margin:4px 0 0;font-size:14px;opacity:0.6;}

        /* --- 6. NAVIGATION & BUTTONS --- */
        .nav{display:flex;gap:12px;justify-self:end}
        .nav a{
            color:var(--accent);
            text-decoration:none;
            padding:8px 12px;
            border-radius:10px;
            font-weight:600;
            transition:background 0.3s ease, color 0.3s ease;
        }
        .nav a:hover{
            background:var(--accent);
            color:#171717; /* Dark text on hover */
            box-shadow:0 0 15px rgba(61, 196, 255, 0.5);
        }
        
        .btn, .outline{
            display:inline-block;
            padding:10px 20px;
            border-radius:999px;
            text-decoration:none;
            font-weight:700;
            transition:transform 0.2s, box-shadow 0.2s;
            font-size:15px;
        }
        .btn{
            background:var(--accent);
            color:#09090b;
        }
        .btn:hover{
            transform:translateY(-2px);
            box-shadow:0 8px 20px rgba(61, 196, 255, 0.4);
        }
        .outline{
            background:transparent;
            border:1px solid var(--glass-border);
            color:var(--muted);
            padding:8px 16px;
            border-radius:12px;
        }
        .outline:hover{
            border-color:var(--accent);
            color:var(--accent);
            box-shadow:0 0 10px rgba(61, 196, 255, 0.3);
        }

        /* --- 7. SKILLS & CHIPS --- */
        .skills{display:flex;flex-wrap:wrap;gap:10px;margin-top:16px;}
        .chip{
            background:rgba(61, 196, 255, 0.1);
            color:var(--accent);
            padding:8px 14px;
            border-radius:999px;
            font-weight:600;
            font-size:13px;
            border: 1px solid rgba(61, 196, 255, 0.3);
        }

        /* --- 8. PROJECTS GRID --- */
        .projects-container{display:grid;grid-template-columns:repeat(2,1fr);gap:20px;margin-top:12px}
        .project{
            padding:20px;
            border-radius:14px;
            background:rgba(255,255,255,0.02);
            border:1px solid rgba(255,255,255,0.06);
            transition:transform .3s ease, box-shadow .3s ease, background-color .3s;
        }
        /* Elegant Hover Effect */
        .project:hover{
            transform:translateY(-5px);
            background:rgba(255,255,255,0.04);
            box-shadow:0 15px 40px rgba(var(--accent-rgb),0.3); /* Teal glow on hover */
        }
        .project p {font-size: 14px;}
        .project-link {
            color: var(--accent);
            text-decoration: none;
            font-weight: 600;
            font-size: 13px;
            margin-top: 10px;
            display: inline-block;
        }

        /* --- 9. ASIDE/SIDE COLUMN --- */
        .side .card + .card{margin-top:20px}
        .meta{display:flex;flex-direction:column;gap:12px}
        .meta b{color:#fff; min-width: 80px; display: inline-block;}
        .meta > div {display: flex; gap: 10px; align-items: center; font-size: 15px;}
        .meta a {color: var(--accent); text-decoration: none; transition: color 0.2s;}
        .meta a:hover {color: #fff;}

        /* --- 10. FOOTER --- */
        footer{opacity:0.7;text-align:center;margin:40px 0;font-size:14px;}

        /* --- 11. RESPONSIVE DESIGN --- */
        @media(max-width:980px){
            .grid{grid-template-columns:1fr; gap: 30px;}
            .hero{grid-template-columns:120px 1fr; gap: 24px;}
            .projects-container{grid-template-columns:1fr}
        }
        @media(max-width:520px){
            .wrap{margin:24px 16px;}
            .hero{grid-template-columns:100px 1fr;padding:20px;}
            .avatar{width:90px;height:90px;}
            .nav{display:none} /* Hide secondary nav on smallest screens */
            .hero h1{font-size: 28px;}
            .hero .job-title{font-size: 16px;}
            .card {padding: 20px; border-radius: 16px;}
        }

        /* --- 12. ELEGANT ENTRANCE ANIMATIONS --- */
        .fade-in{
            opacity:0;
            transform:translateY(15px);
            animation:enter .7s forwards cubic-bezier(0.25, 0.46, 0.45, 0.94); /* Smoother curve */
        }
        .delay-1{animation-delay:0.1s}
        .delay-2{animation-delay:0.2s}
        .delay-3{animation-delay:0.3s}
        .delay-4{animation-delay:0.4s}

        @keyframes enter{
            to{opacity:1;transform:none}
        }
    </style>
</head>
<body>
    <div class="wrap">

        <!-- Header / Hero (The initial card) -->
        <header class="hero fade-in">
            <!-- NOTE: me.png must be present in your repository root -->
            <img class="avatar" src="me.png" alt="Nahidul Islam" />
            <div>
                <div style="display:flex;align-items:center;justify-content:space-between;gap:12px">
                    <div>
                        <h1>Nahidul Islam</h1>
                        <p class="job-title">MIS Executive — Labib Dyeing Mills Ltd</p>
                        <p class="job-dates">Since May 15, 2023 • Abdullahpur, Dhaka</p>
                    </div>
                    <!-- Navigation (Hidden on small screens) -->
                    <nav class="nav">
                        <a href="#about">About</a>
                        <a href="#experience">Experience</a>
                        <a href="#projects">Projects</a>
                        <a href="#contact">Contact</a>
                    </nav>
                </div>

                <!-- Action Links: CV, Email, GitHub, LinkedIn -->
                <div style="margin-top:16px;display:flex;gap:12px;align-items:center">
                    <a class="btn" href="cv.pdf" download>Download CV</a>
                    <a class="outline" href="mailto:meghnahid@gmail.com">Email</a>
                    <a class="outline" href="https://github.com/nahidkhan070/" target="_blank">GitHub</a>
                    <a class="outline" href="https://www.linkedin.com/in/nahidkhan0070" target="_blank">LinkedIn</a>
                </div>
            </div>
        </header>

        <!-- Main content: Left and Right Columns -->
        <main class="grid">
            <!-- LEFT COLUMN: About, Experience, Projects -->
            <div>
                <!-- About -->
                <section id="about" class="card fade-in delay-1">
                    <h2>About Me</h2>
                    <p>I am <strong>Nahidul Islam</strong>, a dedicated MIS Executive with expertise in data analysis, reporting automation, and process optimization. I leverage tools like MS Excel, Power BI, and SQL to transform complex operational data into clear, strategic insights that drive management decisions.</p>
                    
                    <div class="skills">
                        <span class="chip">MS Excel (Advanced)</span>
                        <span class="chip">Power BI / Data Visualization</span>
                        <span class="chip">SQL / Database Management</span>
                        <span class="chip">ERP / CRM Systems</span>
                        <span class="chip">MIS Reporting</span>
                        <span class="chip">VBA / Scripting</span>
                        <span class="chip">Process Optimization</span>
                    </div>
                </section>

                <!-- Experience -->
                <section id="experience" class="card fade-in delay-2" style="margin-top:30px">
                    <h2>Professional History</h2>

                    <div style="margin-top:16px; border-left: 3px solid var(--accent); padding-left: 15px;">
                        <h3 style="margin-bottom: 4px;">MIS Executive</h3>
                        <p style="margin:0;font-size:14px; opacity: 0.8;">Labib Dyeing Mills Ltd • <em>May 2023 – Present</em></p>
                        <ul>
                            <li>Analyze complex datasets and prepare management-ready MIS reports on production, inventory, and efficiency.</li>
                            <li>Designed and maintain automated Power BI dashboards, reducing reporting time by 40%.</li>
                            <li>Coordinated with IT and operations to ensure data integrity and streamlined ERP inputs.</li>
                            <li>Key focus on presenting actionable KPI reports to senior leadership.</li>
                        </ul>
                    </div>

                    <div style="margin-top:20px; border-left: 3px solid rgba(255,255,255,0.1); padding-left: 15px;">
                        <h3 style="margin-bottom: 4px;">Tele Sales Executive</h3>
                        <p style="margin:0;font-size:14px; opacity: 0.8;">bdCalling IT Ltd • <em>2022 – 2023</em></p>
                        <ul>
                            <li>Generated leads, qualified prospects, and closed sales via phone, achieving 110% of quarterly targets.</li>
                            <li>Maintained high customer satisfaction through tailored solution presentations and negotiation.</li>
                        </ul>
                    </div>
                </section>

                <!-- Projects -->
                <section id="projects" class="card fade-in delay-3" style="margin-top:30px">
                    <h2>Key Projects & Automations</h2>
                    <div class="projects-container">
                        
                        <!-- Project 1 -->
                        <article class="project">
                            <h3>Automated Daily Production Report</h3>
                            <p>Implemented an Excel and Power Query system that reduced manual workload by ~60% and ensured real-time accuracy of daily production figures and downtime analysis.</p>
                            <a href="[LINK_TO_TEMPLATE_OR_GITHUB]" class="project-link" target="_blank">View GitHub/Template Link &rarr;</a>
                        </article>
                        
                        <!-- Project 2 -->
                        <article class="project">
                            <h3>Production Dashboard (Power BI)</h3>
                            <p>Interactive Power BI dashboard for visualizing production KPIs, machine efficiency (OEE), capacity utilization, and department performance monitoring.</p>
                            <a href="[LINK_TO_LIVE_DEMO_OR_GITHUB]" class="project-link" target="_blank">View Live Demo/Details &rarr;</a>
                        </article>
                        
                        <!-- Project 3 -->
                        <article class="project">
                            <h3>Inventory Monitoring & Alert System</h3>
                            <p>Smart Google Sheet tracker, utilizing advanced formulas and scripts for real-time stock updates, automated re-order alerts, and consumption trend reporting.</p>
                            <a href="[LINK_TO_TEMPLATE_OR_GITHUB]" class="project-link" target="_blank">View Template/Code &rarr;</a>
                        </article>
                        
                        <!-- Project 4 -->
                        <article class="project">
                            <h3>MIS Automation Toolkit</h3>
                            <p>A repository of VBA scripts and standardized templates used to streamline and error-proof recurring MIS reporting tasks across various non-ERP departments.</p>
                            <a href="[LINK_TO_TEMPLATE_OR_GITHUB]" class="project-link" target="_blank">View Toolkit Repository &rarr;</a>
                        </article>
                        
                    </div>
                </section>

            </div>

            <!-- RIGHT COLUMN: Contact, Education, Details -->
            <aside class="side">
                <!-- Contact Card -->
                <div id="contact" class="card fade-in delay-1">
                    <h2>Connect with Me</h2>
                    <div class="meta">
                        <div><b>Email</b><div style="color:#fff;">meghnahid@gmail.com</div></div>
                        <div><b>Phone</b><div style="color:#fff;">01609597666</div></div>
                        <div><b>Location</b><div style="color:#fff;">Abdullahpur, Dhaka</div></div>
                        
                        <!-- Links repeated from header for clarity -->
                        <div><b>GitHub</b><div><a href="https://github.com/nahidkhan070/" target="_blank">nahidkhan070</a></div></div>
                        <div><b>LinkedIn</b><div><a href="https://www.linkedin.com/in/nahidkhan0070" target="_blank">Nahidul Islam</a></div></div>
                    </div>
                </div>

                <!-- Education -->
                <div class="card fade-in delay-2" style="margin-top:30px">
                    <h2>Education</h2>
                    <div style="margin-top: 10px;">
                        <p style="margin-top: 0; margin-bottom: 2px;"><b>B.Sc (Computer Science & Engineering)</b></p>
                        <p style="margin:0;font-size:14px; opacity: 0.8;">Bangabandhu Sheikh Mujibur Rahman Science & Technology University</p>
                        <p style="margin:4px 0 0;font-size:13px; opacity: 0.7;"><em>2016 – 2017</em></p>
                    </div>
                    <div style="margin-top: 15px;">
                        <p style="margin-top: 0; margin-bottom: 2px;"><b>HSC (Science Group)</b></p>
                        <p style="margin:0;font-size:14px; opacity: 0.8;">Birshreshtha Noor Mohammad Public College</p>
                        <p style="margin:4px 0 0;font-size:13px; opacity: 0.7;"><em>2016</em></p>
                    </div>
                </div>

                <!-- Languages & Expertise -->
                <div class="card fade-in delay-3" style="margin-top:30px">
                    <h2>Core Competencies</h2>
                    <p style="margin-bottom: 12px;"><b>Languages:</b> Bangla (Native), English (Fluent), Hindi (Basic)</p>
                    <p><b>Soft Skills:</b> Management, Stakeholder Communication, Negotiation, Problem-Solving, Team Leadership.</p>
                </div>
            </aside>
        </main>

        <footer>
            © 2025 <strong>Nahidul Islam</strong> • Built with elegance and care.
        </footer>

    </div>

    <script>
        // --- 1. SMOOTH SCROLL FOR NAVIGATION ---
        document.querySelectorAll('.nav a').forEach(a => {
            a.addEventListener('click', function(e) {
                e.preventDefault();
                const id = this.getAttribute('href');
                document.querySelector(id).scrollIntoView({ behavior: 'smooth', block: 'start', inline: 'nearest' });
            });
        });

        // --- 2. LAZY ANIMATE ON INTERSECTION (Modern way to trigger fade-in) ---
        const obs = new IntersectionObserver(entries => {
            entries.forEach(ent => {
                // If the element is intersecting (visible), add the 'visible' class
                if (ent.isIntersecting) {
                    ent.target.classList.add('visible');
                    // Stop observing once visible to prevent re-triggering
                    obs.unobserve(ent.target);
                }
            });
        }, { 
            threshold: 0.15, // Trigger when 15% of the element is visible
            rootMargin: '0px 0px -50px 0px' // Start loading slightly before it hits the bottom
        });
        
        // Observe all elements with the 'fade-in' class
        document.querySelectorAll('.fade-in').forEach(el => obs.observe(el));
    </script>
</body>
</html>

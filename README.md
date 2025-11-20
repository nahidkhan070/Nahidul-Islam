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
            display:inline-flex; /* Use flex to align text and icon */
            align-items:center;
            gap:6px; /* Space between icon and text */
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
        /* Icon styling */
        .icon {
            width: 18px;
            height: 18px;
            fill: currentColor; /* Use the parent element's color */
            flex-shrink: 0; /* Prevents icon from shrinking in flex container */
        }
        .btn .icon { fill: #09090b; } /* Ensure dark fill on bright button */
        .outline:hover .icon, .meta a .icon { fill: var(--accent); }


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
        .meta b{color:#fff; min-width: 80px; display: inline-block; display: flex; align-items: center; gap: 8px;}
        .meta > div {display: flex; gap: 10px; align-items: center; font-size: 15px;}
        .meta a {color: var(--accent); text-decoration: none; transition: color 0.2s; display: flex; align-items: center; gap: 6px;}
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

        /* --- 13. AI INSIGHT FEATURE STYLES --- */
        .project-details { 
            display: flex; 
            flex-direction: column; 
            min-height: 150px; /* Ensure consistent height for project cards */
        }
        .ai-button {
            background: transparent;
            border: 1px solid var(--accent);
            color: var(--accent);
            padding: 6px 12px;
            border-radius: 999px;
            font-size: 13px;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.2s, box-shadow 0.2s;
            margin-top: 10px;
            align-self: flex-start;
        }
        .ai-button:hover {
            background: rgba(61, 196, 255, 0.2);
            box-shadow: 0 0 10px rgba(61, 196, 255, 0.4);
        }
        .insight-box {
            margin-top: 15px;
            padding: 15px;
            border-left: 4px solid var(--accent);
            background: rgba(61, 196, 255, 0.05);
            border-radius: 4px;
            font-size: 14px;
            min-height: 40px;
            display: flex;
            align-items: center;
        }
        .ai-text {
            margin: 0;
            color: #fff;
            font-style: italic;
            font-weight: 500;
            animation: fadeInResult 0.5s ease;
        }
        .error-text {
            margin: 0;
            color: #ff5555;
            font-weight: 600;
        }

        /* Spinner Styles */
        .loader {
            border: 3px solid rgba(255, 255, 255, 0.1);
            border-top: 3px solid var(--accent);
            border-radius: 50%;
            width: 20px;
            height: 20px;
            animation: spin 1s linear infinite;
            display: none; /* hidden by default */
            align-items: center;
            justify-content: center;
            margin: auto;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        @keyframes fadeInResult {
            from { opacity: 0; transform: translateY(5px); }
            to { opacity: 1; transform: translateY(0); }
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

                <!-- Action Links: CV, Email, GitHub, LinkedIn - NOW WITH ICONS -->
                <div style="margin-top:16px;display:flex;gap:12px;align-items:center">
                    <a class="btn" href="cv.pdf" download>
                        <svg class="icon" viewBox="0 0 24 24"><path d="M14 2H6a2 2 0 00-2 2v16a2 2 0 002 2h12a2 2 0 002-2V8l-6-6zM6 20V4h7v4h4v12H6zm2-8h8v2H8v-2zm0 4h8v2H8v-2z"/></svg>
                        Download CV
                    </a>
                    <a class="outline" href="mailto:meghnahid@gmail.com">
                        <svg class="icon" viewBox="0 0 24 24"><path d="M2.003 5.884L10 11l7.997-5.116M18 19H2a2 2 0 01-2-2V4a2 2 0 012-2h16a2 2 0 012 2v13a2 2 0 01-2 2z"/></svg>
                        Email
                    </a>
                    <a class="outline" href="https://github.com/nahidkhan070/" target="_blank">
                        <svg class="icon" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.804 8.207 11.387.599.111.793-.261.793-.577 0-.285-.011-1.04-.016-2.04c-3.338.724-4.042-1.61-4.042-1.61-.542-1.36-.788-1.724-.788-1.724-1.117-.764.083-.748.083-.748 1.237.082 1.885 1.266 1.885 1.266 1.036 1.87 2.73 1.332 3.398 1.012.1-.787.404-1.332.738-1.643-2.6-.295-5.339-1.3-5.339-5.797 0-1.284.485-2.333 1.272-3.149-.125-.295-.551-1.485.121-3.102 0 0 1.03-.315 3.38.12.983-.275 2.032-.412 3.078-.416 1.046.004 2.095.141 3.078.416 2.35-.435 3.375-.12 3.375-.12.673 1.617.247 2.801.12 3.102.788.816 1.273 1.865 1.273 3.149 0 4.498-2.744 5.5-5.353 5.786.416.357.791 1.01.791 2.032 0 1.47-.013 2.656-.013 3.003 0 .318.192.694.8 0C20.562 21.803 24 17.301 24 12c0-6.627-5.373-12-12-12z"/></svg>
                        GitHub
                    </a>
                    <a class="outline" href="https://www.linkedin.com/in/nahidkhan0070" target="_blank">
                         <svg class="icon" viewBox="0 0 24 24"><path d="M20.447 20.452h-3.554v-9.48a1.666 1.666 0 00-1.665-1.667 1.667 1.667 0 00-1.666 1.667v9.48H10.04v-9.48a4.99 4.99 0 014.99-4.99c2.753 0 4.99 2.237 4.99 4.99v9.48zM5.337 4.972a2.883 2.883 0 110-5.766 2.883 2.883 0 010 5.766zm1.777 15.48h-3.554V7.042h3.554v13.41z"/></svg>
                        LinkedIn
                    </a>
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
                    <p style="font-size: 14px; opacity: 0.8; margin-bottom: 20px;">
                        Click **"✨ Generate Impact Analysis"** below any project to see an AI-generated, executive-level summary of its business value, demonstrating advanced analytical interpretation.
                    </p>
                    <div class="projects-container">
                        
                        <!-- Project 1 -->
                        <article class="project" data-id="p1">
                            <div class="project-details">
                                <h3>Automated Daily Production Report</h3>
                                <p class="project-description">Implemented an Excel and Power Query system that reduced manual workload by ~60% and ensured real-time accuracy of daily production figures and downtime analysis.</p>
                                
                                <button class="ai-button" data-id="p1">✨ Generate Impact Analysis</button>
                                <div class="insight-box" id="insight-p1">
                                    <div class="loader" id="loading-p1"></div>
                                </div>
                            </div>
                            <a href="[LINK_TO_TEMPLATE_OR_GITHUB]" class="project-link" target="_blank">View GitHub/Template Link &rarr;</a>
                        </article>
                        
                        <!-- Project 2 -->
                        <article class="project" data-id="p2">
                            <div class="project-details">
                                <h3>Production Dashboard (Power BI)</h3>
                                <p class="project-description">Interactive Power BI dashboard for visualizing production KPIs, machine efficiency (OEE), capacity utilization, and department performance monitoring.</p>
                                
                                <button class="ai-button" data-id="p2">✨ Generate Impact Analysis</button>
                                <div class="insight-box" id="insight-p2">
                                    <div class="loader" id="loading-p2"></div>
                                </div>
                            </div>
                            <a href="[LINK_TO_LIVE_DEMO_OR_GITHUB]" class="project-link" target="_blank">View Live Demo/Details &rarr;</a>
                        </article>
                        
                        <!-- Project 3 -->
                        <article class="project" data-id="p3">
                            <div class="project-details">
                                <h3>Inventory Monitoring & Alert System</h3>
                                <p class="project-description">Smart Google Sheet tracker, utilizing advanced formulas and scripts for real-time stock updates, automated re-order alerts, and consumption trend reporting.</p>
                                
                                <button class="ai-button" data-id="p3">✨ Generate Impact Analysis</button>
                                <div class="insight-box" id="insight-p3">
                                    <div class="loader" id="loading-p3"></div>
                                </div>
                            </div>
                            <a href="[LINK_TO_TEMPLATE_OR_GITHUB]" class="project-link" target="_blank">View Template/Code &rarr;</a>
                        </article>
                        
                        <!-- Project 4 -->
                        <article class="project" data-id="p4">
                            <div class="project-details">
                                <h3>MIS Automation Toolkit</h3>
                                <p class="project-description">A repository of VBA scripts and standardized templates used to streamline and error-proof recurring MIS reporting tasks across various non-ERP departments.</p>
                                
                                <button class="ai-button" data-id="p4">✨ Generate Impact Analysis</button>
                                <div class="insight-box" id="insight-p4">
                                    <div class="loader" id="loading-p4"></div>
                                </div>
                            </div>
                            <a href="[LINK_TO_TEMPLATE_OR_GITHUB]" class="project-link" target="_blank">View Toolkit Repository &rarr;</a>
                        </article>
                        
                    </div>
                </section>

            </div>

            <!-- RIGHT COLUMN: Contact, Education, Details -->
            <aside class="side">
                <!-- Contact Card - NOW WITH ICONS -->
                <div id="contact" class="card fade-in delay-1">
                    <h2>Connect with Me</h2>
                    <div class="meta">
                        <div>
                            <b><svg class="icon" viewBox="0 0 24 24"><path d="M2.003 5.884L10 11l7.997-5.116M18 19H2a2 2 0 01-2-2V4a2 2 0 012-2h16a2 2 0 012 2v13a2 2 0 01-2 2z"/></svg>Email</b>
                            <div style="color:#fff;">meghnahid@gmail.com</div>
                        </div>
                        <div>
                            <b><svg class="icon" viewBox="0 0 24 24"><path d="M16.5 19.5h-9a1 1 0 01-1-1v-15a1 1 0 011-1h9a1 1 0 011 1v15a1 1 0 01-1 1zm-4.5 2a1 1 0 100-2 1 1 0 000 2z"/></svg>Phone</b>
                            <div style="color:#fff;">01609597666</div>
                        </div>
                        <div>
                            <b><svg class="icon" viewBox="0 0 24 24"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5S10.62 6.5 12 6.5s2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg>Location</b>
                            <div style="color:#fff;">Abdullahpur, Dhaka</div>
                        </div>
                        
                        <!-- Links repeated from header for clarity -->
                        <div>
                            <b><svg class="icon" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.804 8.207 11.387.599.111.793-.261.793-.577 0-.285-.011-1.04-.016-2.04c-3.338.724-4.042-1.61-4.042-1.61-.542-1.36-.788-1.724-.788-1.724-1.117-.764.083-.748.083-.748 1.237.082 1.885 1.266 1.885 1.266 1.036 1.87 2.73 1.332 3.398 1.012.1-.787.404-1.332.738-1.643-2.6-.295-5.339-1.3-5.339-5.797 0-1.284.485-2.333 1.272-3.149-.125-.295-.551-1.485.121-3.102 0 0 1.03-.315 3.38.12.983-.275 2.032-.412 3.078-.416 1.046.004 2.095.141 3.078.416 2.35-.435 3.375-.12 3.375-.12.673 1.617.247 2.801.12 3.102.788.816 1.273 1.865 1.273 3.149 0 4.498-2.744 5.5-5.353 5.786.416.357.791 1.01.791 2.032 0 1.47-.013 2.656-.013 3.003 0 .318.192.694.8 0C20.562 21.803 24 17.301 24 12c0-6.627-5.373-12-12-12z"/></svg>GitHub</b>
                            <div><a href="https://github.com/nahidkhan070/" target="_blank">nahidkhan070</a></div>
                        </div>
                        <div>
                            <b><svg class="icon" viewBox="0 0 24 24"><path d="M20.447 20.452h-3.554v-9.48a1.666 1.666 0 00-1.665-1.667 1.667 1.667 0 00-1.666 1.667v9.48H10.04v-9.48a4.99 4.99 0 014.99-4.99c2.753 0 4.99 2.237 4.99 4.99v9.48zM5.337 4.972a2.883 2.883 0 110-5.766 2.883 2.883 0 010 5.766zm1.777 15.48h-3.554V7.042h3.554v13.41z"/></svg>LinkedIn</b>
                            <div><a href="https://www.linkedin.com/in/nahidkhan0070" target="_blank">Nahidul Islam</a></div>
                        </div>
                         <div>
                            <b><svg class="icon" viewBox="0 0 24 24"><path d="M14 0H9a5 5 0 00-5 5v3H1v4h3v9h5v-9h4l1-4H9V5a1 1 0 011-1h4V0z"/></svg>Facebook</b>
                            <div><a href="https://facebook.com/[your-profile-name]" target="_blank">[your-profile-name]</a></div>
                        </div>
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
        // --- GEMINI API CONSTANTS AND UTILITY ---
        const apiKey = ""; // Provided by the execution environment
        const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;

        // Function for retrying API calls with exponential backoff
        async function exponentialBackoffFetch(url, options, maxRetries = 5) {
            for (let i = 0; i < maxRetries; i++) {
                try {
                    const response = await fetch(url, options);
                    if (!response.ok) {
                        // If 429 (Too Many Requests), throw error to trigger retry
                        if (response.status === 429 && i < maxRetries - 1) {
                            throw new Error("Rate limit exceeded. Retrying...");
                        }
                        // For other errors, process the JSON response for context
                        const errorBody = await response.json().catch(() => ({ message: 'Unknown server error' }));
                        throw new Error(`API Error: ${response.status} - ${errorBody.message || 'Server responded with error.'}`);
                    }
                    return response;
                } catch (error) {
                    if (i === maxRetries - 1) {
                        console.error("Max retries reached. Failing request.", error);
                        throw error;
                    }
                    const delay = Math.pow(2, i) * 1000 + Math.random() * 1000;
                    // Wait for the calculated delay before retrying
                    await new Promise(resolve => setTimeout(resolve, delay));
                }
            }
        }

        // --- GEMINI API CALL FUNCTION ---
        async function generateProjectInsight(projectId, projectTitle, projectDescription) {
            const insightBox = document.getElementById(`insight-${projectId}`);
            const loadingEl = document.getElementById(`loading-${projectId}`);

            insightBox.innerHTML = '';
            // Show the loading spinner
            loadingEl.style.display = 'block';
            insightBox.style.justifyContent = 'center';

            const systemPrompt = "You are a specialized business impact analyst. Your task is to review a given project description and, acting as a third-party consultant, generate a maximum 50-word, punchy, professional summary highlighting the key business value, quantifiable impact, and executive-level takeaway. Do not use quotes. Start directly with the insight.";
            const userQuery = `Project Title: ${projectTitle}. Project Description: ${projectDescription}`;

            const payload = {
                contents: [{ parts: [{ text: userQuery }] }],
                systemInstruction: { parts: [{ text: systemPrompt }] },
            };

            try {
                const response = await exponentialBackoffFetch(apiUrl, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify(payload)
                });

                const result = await response.json();
                const candidate = result.candidates?.[0];

                // Remove loading spinner
                loadingEl.style.display = 'none';
                insightBox.style.justifyContent = 'flex-start';


                if (candidate && candidate.content?.parts?.[0]?.text) {
                    const text = candidate.content.parts[0].text;
                    insightBox.innerHTML = `<p class="ai-text"><strong>Impact Insight:</strong> ${text}</p>`;
                } else {
                    insightBox.innerHTML = `<p class="error-text">❌ Error: Could not generate insight. The model response was empty.</p>`;
                }

            } catch (error) {
                console.error("Gemini API call failed:", error);
                loadingEl.style.display = 'none';
                insightBox.style.justifyContent = 'flex-start';
                insightBox.innerHTML = `<p class="error-text">❌ Network Error: Failed to fetch insight. Try again later.</p>`;
            } finally {
                // Ensure the user sees the result box by scrolling to it
                insightBox.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
            }
        }


        // --- DOM EVENT LISTENERS ---
        document.addEventListener('DOMContentLoaded', () => {
            // 1. SMOOTH SCROLL FOR NAVIGATION
            document.querySelectorAll('.nav a').forEach(a => {
                a.addEventListener('click', function(e) {
                    e.preventDefault();
                    const id = this.getAttribute('href');
                    document.querySelector(id).scrollIntoView({ behavior: 'smooth', block: 'start', inline: 'nearest' });
                });
            });

            // 2. LAZY ANIMATE ON INTERSECTION
            const obs = new IntersectionObserver(entries => {
                entries.forEach(ent => {
                    if (ent.isIntersecting) {
                        ent.target.classList.add('visible');
                        obs.unobserve(ent.target);
                    }
                });
            }, { 
                threshold: 0.15,
                rootMargin: '0px 0px -50px 0px'
            });
            
            document.querySelectorAll('.fade-in').forEach(el => obs.observe(el));

            // 3. ATTACH AI BUTTON HANDLERS
            document.querySelectorAll('.ai-button').forEach(button => {
                button.addEventListener('click', function() {
                    const projectId = this.dataset.id;
                    const project = document.querySelector(`.project[data-id="${projectId}"]`);
                    // Find title and description within the project article
                    const title = project.querySelector('h3').textContent;
                    const description = project.querySelector('.project-description').textContent;
                    
                    generateProjectInsight(projectId, title, description);
                });
            });
        });
    </script>
</body>
</html>

<html lang="en">
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <title>Nahidul Islam — MIS Executive & Data Analyst</title>
    

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* --- 1. PREMIUM COLOR PALETTE & VARIABLES --- */
        :root{
            /* UPDATED FOR NEON OCEAN/SEA GREEN RADIANT BACKGROUND */
            /* New base background is a deep ocean teal that animates */
            --bg-gradient: linear-gradient(125deg, #002120 0%, #013330 50%, #002120 100%); 
            --card-bg: rgba(255,255,255,0.03);
            --glass-border: rgba(255,255,255,0.08);
            
            /* The accent color is shifted to a vibrant, electric sea green/cyan */
            --accent: #00FFFF; /* Electric Cyan */
            --accent-rgb: 0, 255, 255; 
            --muted: rgba(255,255,255,0.8);
            --header-font: 'Playfair Display', serif;
            --body-font: 'Poppins', system-ui, Arial;
        }
        
        /* --- 2. GLOBAL STYLES & ANIMATED BACKGROUND --- */
        *{box-sizing:border-box}
        body{
            margin:0;
            font-family:var(--body-font);
            
            /* Apply the new vibrant gradient and animation */
            background: var(--bg-gradient);
            background-size: 400% 400%;
            animation: gradientBG 20s cubic-bezier(0.4, 0, 0.6, 1) infinite; 
            transform: translate3d(0, 0, 0); 
            
            color:var(--muted);
            -webkit-font-smoothing:antialiased;
            min-height:100vh;
            line-height:1.6;
        }

        /* Keyframes adjusted to use the new neon ocean colors */
        @keyframes gradientBG {
            0% { background-position: 0% 50%; background-color: #002120; } /* Dark Teal Base */
            50% { background-position: 100% 50%; background-color: #00FFC0; } /* Neon Sea Green */
            100% { background-position: 0% 50%; background-color: #002120; } /* Dark Teal Base */
        }

        /* Animation 5: Scroll Progress Bar */
        .progress-bar {
            position: fixed;
            top: 0;
            left: 0;
            height: 3px;
            background: var(--accent);
            width: 0%;
            z-index: 1000;
            transition: width 0.1s;
            /* Stronger neon shadow */
            box-shadow: 0 0 15px var(--accent);
        }

        /* --- NEON RIPPLE / SPARKLE EFFECT (UPDATED) --- */
        .sparkle-container {
            position: absolute;
            border-radius: 50%;
            transform: scale(0);
            animation: ripple 0.6s linear;
            /* Use the new electric sea green accent color */
            background: radial-gradient(circle, rgba(0, 255, 255, 0.9) 0%, rgba(0, 255, 255, 0.4) 50%, transparent 100%);
            pointer-events: none; 
            z-index: 10;
        }

        @keyframes ripple {
            0% {
                transform: scale(0);
                opacity: 1;
                box-shadow: 0 0 15px var(--accent); /* Increased shadow for intensity */
            }
            100% {
                transform: scale(4);
                opacity: 0;
            }
        }
        
        /* --- 3. LAYOUT & CARDS --- */
        .wrap{max-width:1200px;margin:48px auto;padding:0 24px;}
        .grid{display:grid;grid-template-columns:1fr 360px;gap:40px;margin-top:40px}
        .card{
            background:var(--card-bg);
            border:1px solid var(--glass-border);
            border-radius:18px;
            padding:24px;
            backdrop-filter: blur(12px) saturate(150%);
            box-shadow:0 8px 30px rgba(0,0,0,0.5);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        /* --- 4. TYPOGRAPHY --- */
        h1, h2, h3{
            font-family:var(--header-font);
            color:#fff;
            margin:0 0 16px 0;
            line-height:1.2;
            text-shadow: 0 0 5px rgba(0, 255, 255, 0.5); /* Subtle neon glow for headers */
        }
        h1{font-size:32px;}
        h2{font-size:24px; margin-bottom: 12px;}
        h3{font-size:18px;}
        p{margin:8px 0; color:rgba(255,255,255,0.85);}
        ul{padding-left:18px; margin-top: 4px; margin-bottom: 4px; font-size: 15px;}
        li {margin-bottom: 4px;}

        /* --- 5. HERO SECTION & FLOATING AVATAR (UPDATED GLOW) --- */
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
            border:4px solid var(--accent);
            /* Avatar neon glow */
            box-shadow:0 0 20px 3px rgba(0, 255, 255, 0.5); 
            object-fit: cover;
            animation: float 5s ease-in-out infinite; 
            transform: translate3d(0, 0, 0); 
        }
        @keyframes float {
            0% { transform: translateY(0px) translate3d(0, 0, 0); }
            50% { transform: translateY(-10px) translate3d(0, 0, 0); } 
            100% { transform: translateY(0px) translate3d(0, 0, 0); }
        }
        
        .hero h1{margin:0;font-size:38px;color:#fff;font-weight:900;}
        .hero .job-title{margin:4px 0 0;font-weight:600;font-size:18px;color:var(--accent);}
        .hero .job-dates{margin:4px 0 0;font-size:14px;opacity:0.6;}

        /* --- 6. NAVIGATION WITH ELEGANT UNDERLINE (UPDATED GLOW) --- */
        .nav{display:flex;gap:12px;justify-self:end}
        .nav a{
            color:var(--accent);
            text-decoration:none;
            padding:8px 12px;
            font-weight:600;
            position: relative; 
            transition: color 0.3s ease;
        }
        .nav a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: 4px;
            left: 50%;
            background-color: var(--accent);
            transition: width 0.3s ease, left 0.3s ease;
            box-shadow: 0 0 5px var(--accent);
        }
        .nav a:hover::after {
            width: 80%;
            left: 10%;
        }
        .nav a:hover {
            color: #fff;
            text-shadow: 0 0 12px rgba(0, 255, 255, 0.8);
        }

        /* Buttons (UPDATED GLOW) */
        .btn-group {
            margin-top:16px;
            display:flex;
            gap:12px;
            /* Allow buttons to wrap to the next line if the screen is too small */
            flex-wrap: wrap; 
            align-items:center;
            width: 100%; /* Ensure it takes full width of the hero content area */
        }
        .btn, .outline, .ai-button{ 
            display:inline-flex;
            align-items:center;
            gap:6px;
            padding:10px 20px;
            border-radius:999px;
            text-decoration:none;
            font-weight:700;
            transition: all 0.3s ease;
            font-size:15px;
            position: relative; 
            overflow: hidden; 
            /* Flex properties for wrapping/responsiveness */
            flex-grow: 1; /* Allow stretching in responsive mode */
            flex-shrink: 0; /* Prevent shrinking below content size */
            white-space: nowrap; /* Keep text on one line */
            max-width: fit-content; /* Reset max width for flex */
        }
        .btn{
            background:var(--accent);
            color:#002120; /* Darker text for contrast */
        }
        .btn:hover{
            transform:translateY(-3px);
            box-shadow:0 0 30px rgba(0, 255, 255, 0.8); /* Intense glow on hover */
        }
        .outline{
            background:transparent;
            border:1px solid var(--glass-border);
            color:var(--muted);
        }
        .outline:hover{
            border-color:var(--accent);
            color:var(--accent);
            box-shadow:0 0 20px rgba(0, 255, 255, 0.4); /* Subtle outline glow */
            transform: translateY(-2px);
        }
        .icon {
            width: 18px;
            height: 18px;
            fill: currentColor;
            flex-shrink: 0;
        }
        .btn .icon { fill: #002120; }

        /* --- 7. STAGGERED SKILLS (UPDATED GLOW) --- */
        .skills{display:flex;flex-wrap:wrap;gap:10px;margin-top:16px;}
        .chip{
            background:rgba(0, 255, 255, 0.1);
            color:var(--accent);
            padding:8px 14px;
            border-radius:999px;
            font-weight:600;
            font-size:13px;
            border: 1px solid rgba(0, 255, 255, 0.3);
            transition: transform 0.2s, background 0.2s, box-shadow 0.2s;
            
            opacity: 0;
            transform: translateY(10px);
        }
        .chip.pop-in {
            opacity: 1;
            transform: translateY(0);
        }
        .chip:hover {
            background: rgba(0, 255, 255, 0.2);
            transform: scale(1.05);
            cursor: default;
            box-shadow: 0 0 10px rgba(0, 255, 255, 0.5); /* Chip hover glow */
        }

        /* --- 8. PROJECTS GRID & SHIMMER EFFECT --- */
        .projects-container{display:grid;grid-template-columns:repeat(2,1fr);gap:20px;margin-top:12px}
        .project{
            padding:20px;
            border-radius:14px;
            background:rgba(255,255,255,0.02);
            border:1px solid rgba(255,255,255,0.06);
            transition:transform .3s ease, box-shadow .3s ease;
            position: relative;
            overflow: hidden; 
        }
        .project::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(
                90deg,
                transparent,
                rgba(255, 255, 255, 0.08),
                transparent
            );
            transition: 0.6s;
            z-index: 1;
            pointer-events: none;
        }
        .project:hover::before {
            left: 100%;
        }
        
        .project:hover{
            transform:translateY(-7px);
            background:rgba(255,255,255,0.04);
            box-shadow:0 0 35px rgba(0, 255, 255, 0.4); /* Intense project card glow on hover */
            border-color: rgba(0, 255, 255, 0.5);
        }
        .project p {font-size: 14px;}
        .project-link {
            color: var(--accent);
            text-decoration: none;
            font-weight: 600;
            font-size: 13px;
            margin-top: 10px;
            display: inline-block;
            position: relative;
            z-index: 2;
        }

        /* --- 9. SIDEBAR & METADATA --- */
        .side .card + .card{margin-top:20px}
        .meta{display:flex;flex-direction:column;gap:12px}
        .meta b{color:#fff; display: flex; align-items: center; gap: 8px;}
        .meta > div {display: flex; gap: 10px; align-items: center; font-size: 15px;}
        .meta a {color: var(--accent); text-decoration: none; transition: color 0.2s; display: flex; align-items: center; gap: 6px;}
        .meta a:hover {color: #fff; text-shadow: 0 0 10px rgba(0, 255, 255, 0.5);}

        /* --- 10. RESPONSIVE (UPDATED FOR FULL FLUIDITY) --- */
        /* Tablet/Desktop adjustments */
        @media(max-width:1080px){ 
            .wrap{max-width:1000px; margin: 48px auto 60px; padding: 0 30px;}
        }
        @media(max-width:980px){
            /* Switch main layout to single column */
            .grid{grid-template-columns:1fr; gap: 30px;}
            /* Keep hero side-by-side on tablet/smaller desktop */
            .hero{grid-template-columns:120px 1fr; gap: 24px;}
            /* Switch projects to single column */
            .projects-container{grid-template-columns:1fr}
        }
        /* Mobile phone (below 520px) */
        @media(max-width:520px){
            .wrap{margin:24px 16px;}
            /* Stack avatar and text vertically */
            .hero{grid-template-columns:1fr; padding:20px; text-align: center;} 
            .avatar{width:100px;height:100px; margin-bottom: 12px;} /* Centered avatar */
            .nav{display:none}
            .hero h1{font-size: 28px;}
            
            /* Center text block contents */
            .hero > div > div:first-child { 
                display: block; 
                text-align: center;
            }
            .hero .job-title, .hero .job-dates { 
                text-align: center; 
            }
            
            /* --- ACTION BUTTONS: Stack vertically and stretch to full width --- */
            .btn-group{
                flex-direction: column; /* Stack vertically */
                gap: 10px; /* Reduce gap slightly when stacked */
                align-items: stretch; /* Stretch all buttons to fill container width */
            }
            .btn, .outline, .ai-button {
                justify-content: center; /* Center button text */
                padding: 12px 20px;
                width: 100%; /* Ensure full width when stacked */
                max-width: 100%; /* Override max-width when stacked */
            }
        }
        /* Extra small mobile (below 400px) */
        @media(max-width:400px){
             .wrap{margin:20px 10px;}
             .hero h1{font-size: 26px;}
        }

        /* --- 11. ENTRANCE ANIMATIONS --- */
        .fade-in{
            opacity:0;
            transform:translateY(20px);
            animation:enter .8s cubic-bezier(0.22, 1, 0.36, 1) forwards;
        }
        .delay-1{animation-delay:0.1s}
        .delay-2{animation-delay:0.2s}
        .delay-3{animation-delay:0.3s}
        .delay-4{animation-delay:0.4s}

        @keyframes enter{
            to{opacity:1;transform:none}
        }

        /* --- 12. AI FEATURE STYLES (UPDATED GLOW) --- */
        .project-details { display: flex; flex-direction: column; min-height: 150px; position: relative; z-index: 2;}
        .ai-button {
            background: transparent;
            border: 1px solid var(--accent);
            color: var(--accent);
            padding: 6px 12px;
            border-radius: 999px;
            font-size: 13px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s;
            margin-top: 10px;
            align-self: flex-start;
        }
        .ai-button:hover {
            background: var(--accent);
            color: #002120;
            box-shadow: 0 0 20px rgba(0, 255, 255, 0.8);
        }
        .insight-box {
            margin-top: 15px;
            padding: 15px;
            border-left: 4px solid var(--accent);
            background: rgba(0, 255, 255, 0.05);
            border-radius: 4px;
            font-size: 14px;
            min-height: 40px;
            display: flex;
            align-items: center;
        }
        .ai-text { margin: 0; color: #fff; font-style: italic; font-weight: 500; animation: fadeInResult 0.5s ease; }
        .loader {
            border: 3px solid rgba(255, 255, 255, 0.1);
            border-top: 3px solid var(--accent);
            border-radius: 50%;
            width: 20px;
            height: 20px;
            animation: spin 1s linear infinite;
            display: none; margin: auto;
        }
        @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
        @keyframes fadeInResult { from { opacity: 0; transform: translateY(5px); } to { opacity: 1; transform: translateY(0); } }
        
        footer { opacity: 0.7; text-align: center; margin: 60px 0; font-size: 14px; }
    </style>
</head>
<body>
    

<div class="progress-bar" id="progressBar"></div>

    <div class="wrap">
        <header class="hero fade-in">
            <img class="avatar" src="me.png" alt="Nahidul Islam" onerror="this.onerror=null; this.src='https://placehold.co/140x140/00FFFF/002120?text=NI'" />
            <div>
                <div style="display:flex;align-items:center;justify-content:space-between;gap:12px">
                    <div>
                        <h1>Nahidul Islam</h1>
                        <p class="job-title">MIS Executive — Labib Dyeing Mills Ltd</p>
                        <p class="job-dates">Since May 2023 • Abdullahpur, Dhaka</p>
                    </div>
                    <nav class="nav">
                        <a href="#about">About</a>
                        <a href="#experience">Experience</a>
                        <a href="#projects">Projects</a>
                        <a href="#training">Training</a> 
                        <a href="#contact">Contact</a>
                    </nav>
                </div>
                <!-- Action Button Group (Renamed and Styled with Flexbox Class) -->
                <div class="btn-group" id="button-group-hero">
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

        <main class="grid">
            <div>
                

<section id="about" class="card fade-in delay-1">
                    <h2>About Me</h2>
                    <p>I am <strong>Nahidul Islam</strong>, a dedicated MIS Executive with expertise in data analysis, reporting automation, and process optimization.</p>
                    

<div class="skills" id="skillsContainer">
                        <span class="chip">MS Excel (Advanced)</span>
                        <span class="chip">Power BI</span>
                        <span class="chip">SQL</span>
                        <span class="chip">ERP / CRM</span>
                        <span class="chip">MIS Reporting</span>
                        <span class="chip">VBA / Scripting</span>
                        <span class="chip">Process Optimization</span>
                    </div>
                </section>

                

<section id="experience" class="card fade-in delay-2" style="margin-top:30px">
                    <h2>Professional History</h2>
                    
                    <!-- Role 1: MIS Executive (Current) -->
                    <div style="margin-top:16px; border-left: 3px solid var(--accent); padding-left: 15px;">
                        <h3 style="margin-bottom: 4px;">MIS Executive</h3>
                        <p style="margin:0;font-size:14px; opacity: 0.8;">Labib Dyeing Mills Ltd • <em>2023 – Present</em></p>
                        <ul>
                            <li>Proficient in analyzing complex datasets to provide actionable insights that support strategic decision-making.</li>
                            <li>Skilled in utilizing advanced Excel functions, SQL, and data visualization tools to enhance operational efficiency.</li>
                            <li>Proven track record in developing and maintaining MIS reports, dashboards, and presentations for senior management.</li>
                        </ul>
                    </div>

                    <!-- Role 2: Tele Sales Executive -->
                    <div style="margin-top:20px; border-left: 3px solid rgba(255,255,255,0.1); padding-left: 15px;">
                        <h3 style="margin-bottom: 4px;">Tele Sales Executive</h3>
                        <p style="margin:0;font-size:14px; opacity: 0.8;">bdCalling IT Ltd • <em>2022 – 2023</em></p>
                        <ul>
                            <li>Driving sales growth through effective communication and relationship-building.</li>
                            <li>Proven ability to generate leads, qualify prospects, and close sales over the phone.</li>
                            <li>Expertise in conducting needs assessments and providing tailored solutions to meet client requirements.</li>
                            <li>Strong track record of meeting and exceeding sales targets while maintaining high customer satisfaction levels.</li>
                            <li>Excellent negotiation skills and a customer-centric approach to foster long-term client relationships.</li>
                        </ul>
                    </div>
                    
                    <!-- Role 3: Computer Operator -->
                    <div style="margin-top:20px; border-left: 3px solid rgba(255,255,255,0.1); padding-left: 15px;">
                        <h3 style="margin-bottom: 4px;">Computer Operator</h3>
                        <p style="margin:0;font-size:14px; opacity: 0.8;">Goldenline Medical Center • <em>2020 – 2021</em></p>
                        <ul>
                            <li>Proficient in managing and maintaining health information systems, ensuring accurate data entry and integrity of patient records.</li>
                            <li>Skilled in operating various software applications for scheduling, billing, and reporting, while adhering to strict confidentiality and compliance standards.</li>
                            <li>Strong communication skills enable effective collaboration with healthcare professionals to support patient care and administrative processes.</li>
                        </ul>
                    </div>
                </section>

                <!-- Professional Training Section (Updated) -->
                <section id="training" class="card fade-in delay-3" style="margin-top:30px">
                    <h2>Professional Training</h2>
                    
                    <div style="margin-top:16px; border-left: 3px solid var(--accent); padding-left: 15px;">
                        <h3 style="margin-bottom: 4px;">Python 101 for Data Science</h3>
                        <p style="margin:0;font-size:14px; opacity: 0.8;">IBM Developer Skills Network • <em>Certified on 25 March 2021</em></p>
                    </div>

                    <div style="margin-top:20px; border-left: 3px solid var(--accent); padding-left: 15px;">
                        <h3 style="margin-bottom: 4px;">Introduction to Python</h3>
                        <p style="margin:0;font-size:14px; opacity: 0.8;">Analytics Vidhya • <em>Certified on 16 March 2021</em></p>
                    </div>
                </section>


                

<section id="projects" class="card fade-in delay-4" style="margin-top:30px">
                    <h2>Key Projects & Automations</h2>
                    <p style="font-size: 14px; opacity: 0.8; margin-bottom: 20px;">
                        Click **"✨ Generate Impact Analysis"** for an AI summary.
                    </p>
                    <div class="projects-container">
                        <article class="project" data-id="p1">
                            <div class="project-details">
                                <h3>Automated Daily Production Report</h3>
                                <p class="project-description">Excel + Power Query system reducing manual workload by ~60% with real-time accuracy.</p>
                                <button class="ai-button" data-id="p1">✨ Generate Impact Analysis</button>
                                <div class="insight-box" id="insight-p1"><div class="loader" id="loading-p1"></div></div>
                            </div>
                            <a href="#" class="project-link" target="_blank">View GitHub/Template Link &rarr;</a>
                        </article>
                        <article class="project" data-id="p2">
                            <div class="project-details">
                                <h3>Production Dashboard (Power BI)</h3>
                                <p class="project-description">Interactive Power BI dashboard for visualizing production KPIs, OEE, and capacity utilization.</p>
                                <button class="ai-button" data-id="p2">✨ Generate Impact Analysis</button>
                                <div class="insight-box" id="insight-p2"><div class="loader" id="loading-p2"></div></div>
                            </div>
                            <a href="#" class="project-link" target="_blank">View Live Demo/Details &rarr;</a>
                        </article>
                        <article class="project" data-id="p3">
                            <div class="project-details">
                                <h3>Inventory Monitoring System</h3>
                                <p class="project-description">Smart Google Sheet tracker for real-time stock updates and automated re-order alerts.</p>
                                <button class="ai-button" data-id="p3">✨ Generate Impact Analysis</button>
                                <div class="insight-box" id="insight-p3"><div class="loader" id="loading-p3"></div></div>
                            </div>
                            <a href="#" class="project-link" target="_blank">View Template/Code &rarr;</a>
                        </article>
                        <article class="project" data-id="p4">
                            <div class="project-details">
                                <h3>MIS Automation Toolkit</h3>
                                <p class="project-description">VBA scripts and standardized templates to streamline reporting tasks.</p>
                                <button class="ai-button" data-id="p4">✨ Generate Impact Analysis</button>
                                <div class="insight-box" id="insight-p4"><div class="loader" id="loading-p4"></div></div>
                            </div>
                            <a href="#" class="project-link" target="_blank">View Toolkit Repository &rarr;</a>
                        </article>
                    </div>
                </section>
            </div>

            <aside class="side">
                <div id="contact" class="card fade-in delay-1">
                    <h2>Connect</h2>
                    <div class="meta">
                        <div><b><svg class="icon" viewBox="0 0 24 24"><path d="M2.003 5.884L10 11l7.997-5.116M18 19H2a2 2 0 01-2-2V4a2 2 0 012-2h16a2 2 0 012 2v13a2 2 0 01-2 2z"/></svg>Email</b><div style="color:#fff;">meghnahid@gmail.com</div></div>
                        <div><b><svg class="icon" viewBox="0 0 24 24"><path d="M16.5 19.5h-9a1 1 0 01-1-1v-15a1 1 0 011-1h9a1 1 0 011 1v15a1 1 0 01-1 1zm-4.5 2a1 1 0 100-2 1 1 0 000 2z"/></svg>Phone</b><div style="color:#fff;">01609597666</div></div>
                        <div><b><svg class="icon" viewBox="0 0 24 24"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5S10.62 6.5 12 6.5s2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg>Location</b><div style="color:#fff;">Abdullahpur, Dhaka</div></div>
                        <div><b><svg class="icon" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.804 8.207 11.387.599.111.793-.261.793-.577 0-.285-.011-1.04-.016-2.04c-3.338.724-4.042-1.61-4.042-1.61-.542-1.36-.788-1.724-.788-1.724-1.117-.764.083-.748.083-.748 1.237.082 1.885 1.266 1.885 1.266 1.036 1.87 2.73 1.332 3.398 1.012.1-.787.404-1.332.738-1.643-2.6-.295-5.339-1.3-5.339-5.797 0-1.284.485-2.333 1.272-3.149-.125-.295-.551-1.485.121-3.102 0 0 1.03-.315 3.38.12.983-.275 2.032-.412 3.078-.416 1.046.004 2.095.141 3.078.416 2.35-.435 3.375-.12 3.375-.12.673 1.617.247 2.801.12 3.102.788.816 1.273 1.865 1.273 3.149 0 4.498-2.744 5.5-5.353 5.786.416.357.791 1.01.791 2.032 0 1.47-.013 2.656-.013 3.003 0 .318.192.694.8 0C20.562 21.803 24 17.301 24 12c0-6.627-5.373-12-12-12z"/></svg>GitHub</b><div><a href="https://github.com/nahidkhan070/" target="_blank">nahidkhan070</a></div></div>
                        <div><b><svg class="icon" viewBox="0 0 24 24"><path d="M20.447 20.452h-3.554v-9.48a1.666 1.666 0 00-1.665-1.667 1.667 1.667 0 00-1.666 1.667v9.48H10.04v-9.48a4.99 4.99 0 014.99-4.99c2.753 0 4.99 2.237 4.99 4.99v9.48zM5.337 4.972a2.883 2.883 0 110-5.766 2.883 2.883 0 010 5.766zm1.777 15.48h-3.554V7.042h3.554v13.41z"/></svg>LinkedIn</b><div><a href="https://www.linkedin.com/in/nahidkhan0070" target="_blank">Nahidul Islam</a></div></div>
                         <div><b><svg class="icon" viewBox="0 0 24 24"><path d="M14 0H9a5 5 0 00-5 5v3H1v4h3v9h5v-9h4l1-4H9V5a1 1 0 011-1h4V0z"/></svg>Facebook</b><div><a href="https://facebook.com/" target="_blank">Nahidul Islam</a></div></div>
                    </div>
                </div>
                <div class="card fade-in delay-2" style="margin-top:30px">
                    <h2>Education</h2>
                    <div style="margin-top: 10px;">
                        <p style="margin-top: 0; margin-bottom: 2px;"><b>B.Sc (Bachelor of Science) in CSE</b></p>
                        <p style="margin:0;font-size:14px; opacity: 0.8;">Bangabandhu Sheikh Mujibur Rahman Science and Technology University (2016–2017)</p>
                    </div>
                    <div style="margin-top: 15px;">
                        <p style="margin-top: 0; margin-bottom: 2px;"><b>HSC in Science</b></p>
                        <p style="margin:0;font-size:14px; opacity: 0.8;">Birshreshtha Noor Mohammad Public College, Dhaka (2016)</p>
                    </div>
                </div>
            </aside>
        </main>
        <footer>© 2025 <strong>Nahidul Islam</strong> • Built with elegance and care.</footer>
    </div>

    <script>
        // --- GEMINI API (Placeholder Key - Requires Valid Key) ---
        const apiKey = ""; 
        const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;

        async function exponentialBackoffFetch(url, options, maxRetries = 5) {
            for (let i = 0; i < maxRetries; i++) {
                try {
                    const response = await fetch(url, options);
                    if (!response.ok) {
                         if (response.status === 429 && i < maxRetries - 1) throw new Error("Rate limit exceeded.");
                         throw new Error(`API Error: ${response.status}`);
                    }
                    return response;
                } catch (error) {
                    if (i === maxRetries - 1) throw error;
                    await new Promise(resolve => setTimeout(resolve, Math.pow(2, i) * 1000));
                }
            }
        }

        async function generateProjectInsight(projectId, projectTitle, projectDescription) {
            const insightBox = document.getElementById(`insight-${projectId}`);
            const loadingEl = document.getElementById(`loading-${projectId}`);
            insightBox.innerHTML = '';
            loadingEl.style.display = 'block';
            insightBox.style.justifyContent = 'center';
            const systemPrompt = "You are a business impact analyst. Generate a max 40-word executive summary of the project's value.";
            const payload = { contents: [{ parts: [{ text: `Project: ${projectTitle}. Desc: ${projectDescription}` }] }], systemInstruction: { parts: [{ text: systemPrompt }] } };
            
            try {
                const response = await exponentialBackoffFetch(apiUrl, { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify(payload) });
                const result = await response.json();
                const text = result.candidates?.[0]?.content?.parts?.[0]?.text;
                loadingEl.style.display = 'none';
                insightBox.style.justifyContent = 'flex-start';
                if (text) insightBox.innerHTML = `<p class="ai-text"><strong>Insight:</strong> ${text}</p>`;
                else insightBox.innerHTML = `<p class="error-text">Error: No response.</p>`;
            } catch (error) {
                loadingEl.style.display = 'none';
                insightBox.style.justifyContent = 'flex-start';
                insightBox.innerHTML = `<p class="error-text">Failed to fetch insight.</p>`;
            }
        }

        // --- SCROLL PROGRESS BAR ---
        window.onscroll = function() {
            var winScroll = document.body.scrollTop || document.documentElement.scrollTop;
            var height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            var scrolled = (winScroll / height) * 100;
            document.getElementById("progressBar").style.width = scrolled + "%";
        };

        // --- NEON RIPPLE EFFECT LOGIC (NEW) ---
        function createSparkle(event) {
            const button = event.currentTarget;
            
            // 1. Calculate the position of the click relative to the button
            const rect = button.getBoundingClientRect();
            const size = Math.max(rect.width, rect.height);
            const x = event.clientX - rect.left;
            const y = event.clientY - rect.top;

            // 2. Create the ripple element
            const sparkle = document.createElement('span');
            sparkle.classList.add('sparkle-container');

            // 3. Position and size the element
            sparkle.style.width = sparkle.style.height = `${size}px`;
            sparkle.style.left = `${x - size / 2}px`;
            sparkle.style.top = `${y - size / 2}px`;

            // 4. Append it to the button
            button.appendChild(sparkle);

            // 5. Clean up after the animation finishes (0.6s)
            setTimeout(() => {
                sparkle.remove();
            }, 600);
        }

        // --- DOM LOAD ---
        document.addEventListener('DOMContentLoaded', () => {
            // Smooth Scroll
            document.querySelectorAll('.nav a').forEach(a => {
                a.addEventListener('click', function(e) {
                    e.preventDefault();
                    document.querySelector(this.getAttribute('href')).scrollIntoView({ behavior: 'smooth', block: 'start' });
                });
            });

            // Staggered Skills Animation
            const skillsContainer = document.getElementById('skillsContainer');
            const chips = skillsContainer.querySelectorAll('.chip');
            const skillObs = new IntersectionObserver(entries => {
                if(entries[0].isIntersecting) {
                    chips.forEach((chip, index) => {
                        setTimeout(() => { chip.classList.add('pop-in'); }, index * 100); // 100ms delay per chip
                    });
                    skillObs.unobserve(skillsContainer);
                }
            }, { threshold: 0.2 });
            skillObs.observe(skillsContainer);

            // General Fade In
            const obs = new IntersectionObserver(entries => {
                entries.forEach(ent => { if (ent.isIntersecting) { ent.target.classList.add('visible'); obs.unobserve(ent.target); } });
            }, { threshold: 0.15, rootMargin: '0px 0px -50px 0px' });
            document.querySelectorAll('.fade-in').forEach(el => obs.observe(el));

            // AI Buttons and Ripple/Sparkle Initialization
            const sparkleTargets = document.querySelectorAll('.btn, .outline, .ai-button');
            
            sparkleTargets.forEach(el => {
                // Attach the new ripple effect listener
                el.addEventListener('click', createSparkle);
            });


            document.querySelectorAll('.ai-button').forEach(btn => {
                btn.addEventListener('click', function(e) {
                    // Prevent sparkle effect from applying twice if already handled by the general listener
                    e.stopPropagation(); 
                    
                    const pid = this.dataset.id;
                    const proj = document.querySelector(`.project[data-id="${pid}"]`);
                    generateProjectInsight(pid, proj.querySelector('h3').textContent, proj.querySelector('.project-description').textContent);
                });
            });
        });
    </script>
</body>
</html>

<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Nahidul Islam | Portfolio</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap');

        body {
            margin: 0;
            font-family: 'Poppins', sans-serif;
            background: #eef2f7;
            color: #1f2937;
            overflow-x: hidden;
        }
        header {
            background: linear-gradient(135deg, #1d4ed8, #3b82f6);
            color: white;
            padding: 70px 20px;
            text-align: center;
            animation: fadeIn 1s ease-in-out;
        }
        header h1 {
            margin: 0;
            font-size: 42px;
            font-weight: 700;
        }
        header p {
            margin: 10px 0 0;
            opacity: 0.9;
            font-size: 18px;
        }
        section {
            max-width: 950px;
            margin: 40px auto;
            padding: 30px;
            background: white;
            border-radius: 16px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            animation: slideUp 0.8s ease;
        }
        h2 {
            border-left: 6px solid #2563eb;
            padding-left: 12px;
            font-size: 24px;
            margin-bottom: 20px;
        }
        .skills span {
            display: inline-block;
            background: #2563eb;
            color: white;
            padding: 8px 14px;
            border-radius: 20px;
            margin: 6px;
            font-size: 14px;
        }
        .projects {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
        .project-card {
            background: #f8fafc;
            padding: 20px;
            border-radius: 14px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
            transition: transform 0.3s;
        }
        .project-card:hover {
            transform: translateY(-5px);
        }
        .cv-btn {
            display: inline-block;
            padding: 12px 24px;
            background: #1d4ed8;
            color: white;
            text-decoration: none;
            border-radius: 30px;
            margin-top: 15px;
            font-weight: 600;
            transition: background 0.3s;
        }
        .cv-btn:hover {
            background: #0f3ab7;
        }
        footer {
            text-align: center;
            padding: 25px;
            color: #555;
            margin-top: 40px;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        @keyframes slideUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        @media(max-width: 600px) {
            header h1 { font-size: 32px; }
            section { padding: 20px; margin: 20px; }
        }
    </style>
</head>
<body>
    <header>
        <img src="me.png" alt="Nahidul Islam" 
style="width:140px;height:140px;border-radius:50%;object-fit:cover;border:4px solid white;margin-bottom:20px;" />

        <h1>Nahidul Islam</h1>
        <p>Executive MIS | Labib Dyeing Mills Ltd (Labib Group)</p>
        <p>Since May 15, 2023</p>
    </header>

    <section>
        <h2>About Me</h2>
        <p>I am Nahidul Islam, a dedicated MIS Executive with strong expertise in data analysis, reporting, and business process optimization. I specialize in using Excel, SQL, Power BI, and ERP/CRM systems to convert raw data into meaningful insights that support strategic decision-making. I have a proven record of developing automated dashboards, MIS systems, and performance reports for senior management.</p>
        <a class="cv-btn" href="cv.pdf" download>Download CV</a>
    </section>

    <section>
        <h2>Experience</h2>

        <p><strong>MIS Executive</strong> — Labib Dyeing Mills Ltd<br>
        <em>2023 – Present</em></p>
        <ul>
            <li>Analyze complex datasets to generate actionable insights for management.</li>
            <li>Create and maintain MIS dashboards and automated reporting systems.</li>
            <li>Develop Power BI dashboards for real-time production, sales, and efficiency tracking.</li>
            <li>Coordinate with departments to ensure data accuracy and improve workflow efficiency.</li>
            <li>Prepare presentations and reports for senior management.</li>
        </ul>

        <p><strong>Tele Sales Executive</strong> — bdCalling IT Ltd<br>
        <em>2022 – 2023</em></p>
        <ul>
            <li>Generated leads and closed sales through strong communication and negotiation.</li>
            <li>Provided tailored solutions to meet client needs and maintain high satisfaction.</li>
            <li>Achieved sales targets consistently.</li>
        </ul>

        <p><strong>Computer Operator</strong> — Goldenline Medical Center<br>
        <em>2020 – 2021</em></p>
        <ul>
            <li>Managed health information systems and ensured accurate data entry.</li>
            <li>Handled scheduling, patient billing, and reporting systems.</li>
            <li>Collaborated with healthcare professionals to support patient care workflows.</li>
        </ul>
    </section>

    <section>
        <h2>Skills</h2>
        <div class="skills">
            <span>Management Skills</span>
            <span>Creativity</span>
            <span>CRM Software</span>
            <span>Microsoft Office</span>
            <span>Communication & Negotiation</span>
            <span>Project Management</span>
            <span>SQL & ERP</span>
        </div>
    </section>

    <section>
        <h2>Projects</h2>
        <div class="projects">
            <div class="project-card">
                <h3>Automated Daily Production Report</h3>
                <p>A fully automated Excel + Power Query based reporting system reducing daily manual work by 60%.</p>
            </div>
            <div class="project-card">
                <h3>Production Dashboard (Power BI)</h3>
                <p>Interactive dashboard showing production KPIs, efficiency, and department performance.</p>
            </div>
            <div class="project-card">
                <h3>Inventory Monitoring Sheet</h3>
                <p>A smart Google Sheet tracker for real‑time stock updates and alerts.</p>
            </div>
        </div>
    </section>

    <section>
        <h2>Contact</h2>
        <p>Email: meghnahid@gmail.com</p>
        <p>Phone: 01609597666</p>
        <p>Address: Abdullahpur, Dhaka</p>
    </section>

    <footer>
        © 2025 Nahidul Islam — Portfolio Website
    </footer>
</body>
</html>

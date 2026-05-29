<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Naveen N — Cybersecurity Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Mono:wght@300;400;500&family=Fraunces:ital,wght@0,300;0,600;1,300&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0a0e0f;
    --surface: #111618;
    --card: #141a1c;
    --accent: #00e5a0;
    --accent2: #00b8d4;
    --accent3: #ff6b35;
    --text: #e8f0ef;
    --muted: #7a9090;
    --border: #1e2c2e;
    --glow: 0 0 24px rgba(0,229,160,0.15);
  }

  * { margin:0; padding:0; box-sizing:border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    line-height: 1.6;
    min-height: 100vh;
  }

  .page {
    width: 210mm;
    min-height: 297mm;
    margin: 0 auto;
    background: var(--bg);
    position: relative;
    overflow: hidden;
  }

  /* Background grid */
  .page::before {
    content: '';
    position: absolute;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,229,160,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,229,160,0.03) 1px, transparent 1px);
    background-size: 28px 28px;
    pointer-events: none;
  }

  /* Glow orb */
  .page::after {
    content: '';
    position: absolute;
    top: -80px;
    right: -80px;
    width: 320px;
    height: 320px;
    background: radial-gradient(circle, rgba(0,229,160,0.07) 0%, transparent 70%);
    pointer-events: none;
  }

  /* ─── HEADER ─── */
  .header {
    padding: 36px 40px 24px;
    border-bottom: 1px solid var(--border);
    position: relative;
  }

  .header-top {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: 24px;
  }

  .name-block {}

  .name {
    font-family: 'Syne', sans-serif;
    font-size: 42px;
    font-weight: 800;
    letter-spacing: -1px;
    line-height: 1;
    color: var(--text);
  }

  .name span {
    color: var(--accent);
  }

  .tagline {
    font-family: 'DM Mono', monospace;
    font-size: 10.5px;
    color: var(--accent);
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-top: 8px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .tagline::before {
    content: '';
    display: inline-block;
    width: 18px;
    height: 1px;
    background: var(--accent);
  }

  .contact-block {
    display: flex;
    flex-direction: column;
    gap: 5px;
    align-items: flex-end;
    padding-top: 4px;
  }

  .contact-item {
    font-size: 9.5px;
    color: var(--muted);
    display: flex;
    align-items: center;
    gap: 6px;
    font-family: 'DM Mono', monospace;
  }

  .contact-item .icon {
    color: var(--accent);
    font-size: 9px;
  }

  .contact-item a {
    color: var(--muted);
    text-decoration: none;
  }
  .contact-item a:hover { color: var(--accent); }

  /* ─── BODY LAYOUT ─── */
  .body {
    display: grid;
    grid-template-columns: 1fr 220px;
    gap: 0;
    padding: 0;
  }

  .main-col {
    padding: 24px 28px 32px 40px;
    border-right: 1px solid var(--border);
  }

  .side-col {
    padding: 24px 24px 32px 20px;
  }

  /* ─── SECTION ─── */
  .section {
    margin-bottom: 22px;
  }

  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: 9px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }

  /* ─── OBJECTIVE ─── */
  .objective-text {
    font-family: 'Fraunces', serif;
    font-size: 11px;
    font-weight: 300;
    color: #b0c4c2;
    line-height: 1.75;
    font-style: italic;
    border-left: 2px solid var(--accent);
    padding-left: 12px;
  }

  /* ─── PROJECT ─── */
  .project {
    margin-bottom: 14px;
    padding: 10px 12px;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 4px;
    position: relative;
  }

  .project::before {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    bottom: 0;
    width: 2px;
    background: linear-gradient(180deg, var(--accent), var(--accent2));
    border-radius: 4px 0 0 4px;
  }

  .project-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-bottom: 4px;
    gap: 8px;
  }

  .project-name {
    font-family: 'Syne', sans-serif;
    font-size: 10.5px;
    font-weight: 700;
    color: var(--text);
  }

  .project-year {
    font-size: 8.5px;
    color: var(--accent);
    white-space: nowrap;
    font-family: 'DM Mono', monospace;
    background: rgba(0,229,160,0.08);
    padding: 1px 6px;
    border-radius: 2px;
  }

  .project-stack {
    font-size: 8.5px;
    color: var(--accent2);
    margin-bottom: 6px;
    font-family: 'DM Mono', monospace;
  }

  .project-points {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 3px;
  }

  .project-points li {
    font-size: 9.5px;
    color: #8ea8a5;
    padding-left: 12px;
    position: relative;
    line-height: 1.5;
  }

  .project-points li::before {
    content: '▸';
    position: absolute;
    left: 0;
    color: var(--accent);
    font-size: 8px;
    top: 1px;
  }

  /* ─── INTERNSHIP ─── */
  .internship {
    margin-bottom: 12px;
    padding-left: 10px;
    border-left: 1px solid var(--border);
  }

  .intern-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-bottom: 3px;
  }

  .intern-name {
    font-family: 'Syne', sans-serif;
    font-size: 10px;
    font-weight: 700;
    color: var(--text);
  }

  .intern-date {
    font-size: 8.5px;
    color: var(--accent3);
    font-family: 'DM Mono', monospace;
  }

  .intern-org {
    font-size: 9px;
    color: var(--muted);
    margin-bottom: 4px;
    font-style: italic;
  }

  .intern-points {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 2px;
  }

  .intern-points li {
    font-size: 9px;
    color: #8ea8a5;
    padding-left: 10px;
    position: relative;
    line-height: 1.5;
  }

  .intern-points li::before {
    content: '◆';
    position: absolute;
    left: 0;
    color: var(--accent2);
    font-size: 5px;
    top: 3px;
  }

  /* ─── SIDEBAR COMPONENTS ─── */

  /* Education */
  .edu-item {
    margin-bottom: 12px;
    padding: 8px 10px;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 4px;
  }

  .edu-degree {
    font-family: 'Syne', sans-serif;
    font-size: 9.5px;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 2px;
  }

  .edu-school {
    font-size: 8.5px;
    color: var(--muted);
    margin-bottom: 3px;
    line-height: 1.4;
  }

  .edu-meta {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .edu-score {
    font-size: 9px;
    color: var(--accent);
    font-weight: 500;
  }

  .edu-year {
    font-size: 8px;
    color: var(--muted);
  }

  /* Skills */
  .skill-group {
    margin-bottom: 10px;
  }

  .skill-label {
    font-size: 8px;
    color: var(--accent2);
    text-transform: uppercase;
    letter-spacing: 1.5px;
    margin-bottom: 5px;
    font-family: 'Syne', sans-serif;
    font-weight: 600;
  }

  .skill-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 4px;
  }

  .tag {
    font-size: 8px;
    padding: 2px 6px;
    border-radius: 2px;
    font-family: 'DM Mono', monospace;
    background: rgba(255,255,255,0.04);
    border: 1px solid var(--border);
    color: #9ab8b5;
  }

  .tag.accent { border-color: rgba(0,229,160,0.3); color: var(--accent); background: rgba(0,229,160,0.05); }
  .tag.accent2 { border-color: rgba(0,184,212,0.3); color: var(--accent2); background: rgba(0,184,212,0.05); }

  /* Certifications */
  .cert-item {
    margin-bottom: 6px;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: 6px;
  }

  .cert-name {
    font-size: 8.5px;
    color: #9ab8b5;
    flex: 1;
    line-height: 1.4;
  }

  .cert-date {
    font-size: 7.5px;
    color: var(--muted);
    white-space: nowrap;
    font-family: 'DM Mono', monospace;
  }

  /* Responsibilities */
  .resp-item {
    margin-bottom: 6px;
    display: flex;
    align-items: flex-start;
    gap: 6px;
  }

  .resp-dot {
    width: 5px;
    height: 5px;
    border-radius: 50%;
    background: var(--accent);
    margin-top: 4px;
    flex-shrink: 0;
  }

  .resp-text {
    font-size: 8.5px;
    color: #9ab8b5;
    line-height: 1.4;
  }

  .resp-role {
    font-weight: 500;
    color: var(--text);
    font-family: 'Syne', sans-serif;
    font-size: 8.5px;
  }

  /* Achievements */
  .achievement-item {
    margin-bottom: 6px;
    padding: 6px 8px;
    background: rgba(255,107,53,0.06);
    border: 1px solid rgba(255,107,53,0.2);
    border-radius: 3px;
    font-size: 8.5px;
    color: #c0a898;
    line-height: 1.4;
  }

  .achievement-item::before {
    content: '🏆 ';
    font-size: 9px;
  }

  /* Status badge */
  .status-badge {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    font-size: 8px;
    color: var(--accent);
    letter-spacing: 1.5px;
    text-transform: uppercase;
    margin-top: 6px;
    font-family: 'DM Mono', monospace;
  }

  .status-dot {
    width: 5px;
    height: 5px;
    border-radius: 50%;
    background: var(--accent);
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(0.8); }
  }

  /* Print */
  @media print {
    body { background: #0a0e0f !important; -webkit-print-color-adjust: exact; print-color-adjust: exact; }
    .page { width: 100%; }
    * { animation: none !important; }
  }

  @media screen {
    body { padding: 20px 0 40px; }
    .page { box-shadow: 0 0 80px rgba(0,0,0,0.8), 0 0 1px rgba(0,229,160,0.2); }
  }
</style>
</head>
<body>
<div class="page">

  <!-- HEADER -->
  <div class="header">
    <div class="header-top">
      <div class="name-block">
        <div class="name">NAVEEN<span> N</span></div>
        <div class="tagline">Turning Vulnerabilities into Victories</div>
        <div class="status-badge">
          <span class="status-dot"></span>
          Cybersecurity Engineer
        </div>
      </div>
      <div class="contact-block">
        <div class="contact-item"><span class="icon">📞</span> +91-6379731157</div>
        <div class="contact-item"><span class="icon">✉</span> naveen171105@gmail.com</div>
        <div class="contact-item"><span class="icon">📍</span> Chennai, Tamil Nadu</div>
        <div class="contact-item"><span class="icon">🔗</span> <a href="https://linkedin.com/in/naveen-cys">linkedin.com/in/naveen-cys</a></div>
        <div class="contact-item"><span class="icon">🐙</span> <a href="https://github.com/naveen-n0">github.com/naveen-n0</a></div>
      </div>
    </div>
  </div>

  <!-- BODY -->
  <div class="body">

    <!-- MAIN COLUMN -->
    <div class="main-col">

      <!-- Career Objective -->
      <div class="section">
        <div class="section-title">Career Objective</div>
        <div class="objective-text">
          Aspiring Cybersecurity professional with a strong foundation in network security, threat analysis, and ethical hacking, seeking a challenging role as a System Engineer. Eager to leverage technical expertise to design, implement, and maintain secure systems, ensuring robust protection of organizational IT infrastructure while contributing to innovative cybersecurity solutions.
        </div>
      </div>

      <!-- Projects -->
      <div class="section">
        <div class="section-title">Projects</div>

        <div class="project">
          <div class="project-header">
            <div class="project-name">ML-Powered Malware Detector</div>
            <div class="project-year">2025</div>
          </div>
          <div class="project-stack">Python · Random Forest · Flask · CICIDS-2017</div>
          <ul class="project-points">
            <li>Developed an ML-powered web tool to detect malware in network traffic by analyzing PCAP files.</li>
            <li>Enabled users to upload and analyze traffic to identify potential malicious activity.</li>
            <li>Applied Random Forest for classifying traffic as benign or malicious based on extracted features.</li>
          </ul>
        </div>

        <div class="project">
          <div class="project-header">
            <div class="project-name">Dual-Layer Defense Framework for Aadhaar-Based Identity Leaks</div>
            <div class="project-year">2026</div>
          </div>
          <div class="project-stack">Python · Flask · SQLite · Regex · Telethon</div>
          <ul class="project-points">
            <li>Developed a real-time PII leak detection system for Aadhaar, PAN, UPI, and mobile data from public sources.</li>
            <li>Built automated scraping, severity scoring, and alert mechanisms using Flask and regex-based analysis.</li>
            <li>Implemented canary records for breach attribution and forensic tracking.</li>
          </ul>
        </div>

        <div class="project">
          <div class="project-header">
            <div class="project-name">SecureScan Enterprise — AI-Powered Document Threat Detector</div>
            <div class="project-year">2025</div>
          </div>
          <div class="project-stack">Python · Flask · YARA · SQLite · ReportLab · Three.js · PyInstaller</div>
          <ul class="project-points">
            <li>Built a self-contained Windows application to scan PDF and DOCX files for hidden malware using YARA signatures and deep heuristic analysis.</li>
            <li>Engineered a unique Metadata Forensics Engine to extract author, revision history, and creation-tool anomalies as forensic indicators.</li>
            <li>Implemented CDR (Content Disarm & Reconstruction) to de-weaponize malicious files and serve clean downloads.</li>
            <li>Delivered a 3D holographic report viewer (Three.js), PDF audit reports, rate-limited REST API, and session-based auth portal.</li>
          </ul>
        </div>
      </div>

      <!-- Internships -->
      <div class="section">
        <div class="section-title">Internships</div>

        <div class="internship">
          <div class="intern-header">
            <div class="intern-name">Cybersecurity Internship</div>
            <div class="intern-date">Jul – Oct 2025</div>
          </div>
          <div class="intern-org">AICTE Edu-Tantr · Online / Offline</div>
          <ul class="intern-points">
            <li>Received practical exposure to cybersecurity principles and network defense mechanisms.</li>
            <li>Studied cryptography, authentication protocols, and system security practices.</li>
            <li>Worked with Kali Linux, Wireshark, Nmap, and cyber forensics utilities.</li>
          </ul>
        </div>

        <div class="internship">
          <div class="intern-header">
            <div class="intern-name">Cybersecurity Internship</div>
            <div class="intern-date">2025</div>
          </div>
          <div class="intern-org">Prodigy InfoTech · Online</div>
          <ul class="intern-points">
            <li>Gained hands-on experience in ethical hacking and vulnerability assessment.</li>
            <li>Worked on network scanning, traffic analysis, and security testing using industry-standard tools.</li>
            <li>Utilized Kali Linux, Wireshark, Nmap, and penetration testing utilities.</li>
          </ul>
        </div>
      </div>

    </div>

    <!-- SIDE COLUMN -->
    <div class="side-col">

      <!-- Education -->
      <div class="section">
        <div class="section-title">Education</div>

        <div class="edu-item">
          <div class="edu-degree">B.E. in Cyber Security</div>
          <div class="edu-school">SRM Valliammai Engineering College, Kattankulathur</div>
          <div class="edu-meta">
            <span class="edu-score">Current</span>
            <span class="edu-year">2023 – Present</span>
          </div>
        </div>

        <div class="edu-item">
          <div class="edu-degree">HSC</div>
          <div class="edu-school">Saraswathi Matric. Hr. Sec. School, Salem</div>
          <div class="edu-meta">
            <span class="edu-score">88%</span>
            <span class="edu-year">2022 – 2023</span>
          </div>
        </div>
      </div>

      <!-- Technical Skills -->
      <div class="section">
        <div class="section-title">Technical Skills</div>

        <div class="skill-group">
          <div class="skill-label">Languages</div>
          <div class="skill-tags">
            <span class="tag accent">Python</span>
            <span class="tag accent">Java</span>
            <span class="tag">SQL</span>
            <span class="tag">HTML</span>
            <span class="tag">CSS</span>
          </div>
        </div>

        <div class="skill-group">
          <div class="skill-label">Security Tools</div>
          <div class="skill-tags">
            <span class="tag accent2">Wireshark</span>
            <span class="tag accent2">Nmap</span>
            <span class="tag accent2">Burp Suite</span>
            <span class="tag">VMware</span>
            <span class="tag">VirtualBox</span>
            <span class="tag">Git</span>
          </div>
        </div>

        <div class="skill-group">
          <div class="skill-label">Operating Systems</div>
          <div class="skill-tags">
            <span class="tag">Kali Linux</span>
            <span class="tag">Windows</span>
            <span class="tag">iOS</span>
          </div>
        </div>

        <div class="skill-group">
          <div class="skill-label">Cloud (Learning)</div>
          <div class="skill-tags">
            <span class="tag">AWS VPC</span>
            <span class="tag">IAM</span>
            <span class="tag">EC2</span>
            <span class="tag">S3</span>
          </div>
        </div>

        <div class="skill-group">
          <div class="skill-label">Interests</div>
          <div class="skill-tags">
            <span class="tag">Network Security</span>
            <span class="tag">Malware Analysis</span>
            <span class="tag">Digital Forensics</span>
            <span class="tag">Cloud Security</span>
          </div>
        </div>
      </div>

      <!-- Certifications -->
      <div class="section">
        <div class="section-title">Certifications</div>
        <div class="cert-item">
          <div class="cert-name">Digital Maturity Diagnostic Framework</div>
          <div class="cert-date">Apr 2026</div>
        </div>
        <div class="cert-item">
          <div class="cert-name">Cloud Security (VAC)</div>
          <div class="cert-date">Jul–Oct 2025</div>
        </div>
        <div class="cert-item">
          <div class="cert-name">Penetration Testing (VAC)</div>
          <div class="cert-date">Aug–Oct 2024</div>
        </div>
        <div class="cert-item">
          <div class="cert-name">Python Full Stack Web Dev (Django)</div>
          <div class="cert-date">Jan–Jun 2024</div>
        </div>
        <div class="cert-item">
          <div class="cert-name">Diploma in Computer Application</div>
          <div class="cert-date">2018</div>
        </div>
      </div>

      <!-- Roles -->
      <div class="section">
        <div class="section-title">Leadership</div>
        <div class="resp-item">
          <div class="resp-dot"></div>
          <div class="resp-text"><span class="resp-role">Vice President</span> — Whitehatians Club</div>
        </div>
        <div class="resp-item">
          <div class="resp-dot"></div>
          <div class="resp-text"><span class="resp-role">Administrative Head</span> — CSI Student Branch</div>
        </div>
        <div class="resp-item">
          <div class="resp-dot"></div>
          <div class="resp-text"><span class="resp-role">Event Manager</span> — Zyverse 2k25</div>
        </div>
        <div class="resp-item">
          <div class="resp-dot"></div>
          <div class="resp-text"><span class="resp-role">Volunteer</span> — Zyverse 2k24</div>
        </div>
        <div class="resp-item">
          <div class="resp-dot"></div>
          <div class="resp-text"><span class="resp-role">Member</span> — ISTE</div>
        </div>
      </div>

      <!-- Achievements -->
      <div class="section">
        <div class="section-title">Achievements</div>
        <div class="achievement-item">Highest CGPA — 4th Semester, College Day 2026</div>
        <div class="achievement-item">Junior Grade Typewriting English — First Class</div>
      </div>

    </div>
  </div>
</div>
</body>
</html>

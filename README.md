# EAP2-Skills-Webpage-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Abu Bakar · EAP2 Employability Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;0,9..40,600;1,9..40,300&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0d0d0d;
    --surface: #141414;
    --surface2: #1a1a1a;
    --border: #2a2a2a;
    --accent: #eb1000;
    --accent2: #ff4444;
    --text: #f0f0f0;
    --muted: #888;
    --dim: #555;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    font-weight: 300;
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 48px;
    height: 64px;
    background: rgba(13,13,13,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
  }

  .nav-logo {
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .nav-logo-mark {
    width: 32px; height: 32px;
    background: var(--accent);
    display: flex; align-items: center; justify-content: center;
    font-family: 'Bebas Neue', sans-serif;
    font-size: 18px;
    letter-spacing: 0;
    color: #fff;
  }

  .nav-logo-text {
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--muted);
  }

  .nav-links {
    display: flex;
    gap: 40px;
    list-style: none;
  }

  .nav-links a {
    text-decoration: none;
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--muted);
    transition: color 0.2s;
  }

  .nav-links a:hover { color: var(--text); }

  .nav-badge {
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--accent);
    border: 1px solid var(--accent);
    padding: 4px 10px;
  }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    padding: 0 48px 80px;
    position: relative;
    overflow: hidden;
  }

  .hero-grid {
    position: absolute;
    inset: 0;
    background-image:
      linear-gradient(rgba(235,16,0,0.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(235,16,0,0.04) 1px, transparent 1px);
    background-size: 80px 80px;
    animation: gridFade 3s ease forwards;
  }

  @keyframes gridFade {
    from { opacity: 0; }
    to { opacity: 1; }
  }

  .hero-glow {
    position: absolute;
    top: -200px; right: -200px;
    width: 700px; height: 700px;
    background: radial-gradient(circle, rgba(235,16,0,0.12) 0%, transparent 60%);
    pointer-events: none;
  }

  .hero-eyebrow {
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 24px;
    opacity: 0;
    animation: slideUp 0.6s 0.2s ease forwards;
  }

  .hero-name {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(80px, 14vw, 180px);
    line-height: 0.88;
    letter-spacing: -0.01em;
    color: var(--text);
    opacity: 0;
    animation: slideUp 0.7s 0.35s ease forwards;
  }

  .hero-name span { color: var(--accent); }

  .hero-sub {
    margin-top: 32px;
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
    gap: 32px;
    opacity: 0;
    animation: slideUp 0.7s 0.5s ease forwards;
  }

  .hero-desc {
    max-width: 460px;
    font-size: 15px;
    color: var(--muted);
    line-height: 1.8;
  }

  .hero-meta {
    text-align: right;
    font-size: 12px;
    color: var(--dim);
    line-height: 2;
    letter-spacing: 0.04em;
  }

  .hero-meta strong { color: var(--muted); font-weight: 500; }

  .hero-divider {
    width: 100%;
    height: 1px;
    background: var(--border);
    margin-top: 60px;
    opacity: 0;
    animation: slideUp 0.6s 0.65s ease forwards;
  }

  @keyframes slideUp {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* ── SECTIONS ── */
  section {
    padding: 100px 48px;
    border-bottom: 1px solid var(--border);
  }

  .section-header {
    display: flex;
    align-items: baseline;
    gap: 20px;
    margin-bottom: 64px;
  }

  .section-num {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 13px;
    color: var(--accent);
    letter-spacing: 0.12em;
  }

  .section-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: clamp(36px, 5vw, 60px);
    letter-spacing: 0.02em;
    color: var(--text);
  }

  .section-line {
    flex: 1;
    height: 1px;
    background: var(--border);
    margin-bottom: 6px;
  }

  /* ── ABOUT ── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: start;
  }

  .about-heading {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 28px;
    letter-spacing: 0.04em;
    color: var(--muted);
    margin-bottom: 24px;
  }

  .about-body {
    font-size: 15px;
    color: #aaa;
    line-height: 1.9;
  }

  .about-stats {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2px;
  }

  .stat-box {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 28px;
    transition: border-color 0.2s;
  }

  .stat-box:hover { border-color: var(--accent); }

  .stat-label {
    font-size: 10px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--dim);
    margin-bottom: 10px;
  }

  .stat-value {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 28px;
    color: var(--text);
    letter-spacing: 0.04em;
  }

  .stat-sub {
    font-size: 12px;
    color: var(--muted);
    margin-top: 4px;
  }

  /* ── SKILLS ── */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2px;
  }

  .skill-card {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 36px 32px;
    position: relative;
    overflow: hidden;
    transition: border-color 0.25s, background 0.25s;
  }

  .skill-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: var(--accent);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s ease;
  }

  .skill-card:hover::before { transform: scaleX(1); }
  .skill-card:hover { border-color: #333; background: var(--surface2); }

  .skill-tag {
    font-size: 9px;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--accent);
    font-weight: 600;
    margin-bottom: 16px;
  }

  .skill-icon {
    font-size: 28px;
    margin-bottom: 12px;
    display: block;
  }

  .skill-name {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 26px;
    letter-spacing: 0.04em;
    color: var(--text);
    margin-bottom: 16px;
  }

  .skill-body {
    font-size: 13.5px;
    color: #888;
    line-height: 1.85;
    margin-bottom: 28px;
  }

  .skill-bar-label {
    display: flex;
    justify-content: space-between;
    font-size: 11px;
    color: var(--dim);
    letter-spacing: 0.06em;
    text-transform: uppercase;
    margin-bottom: 8px;
  }

  .skill-bar {
    height: 2px;
    background: var(--border);
    position: relative;
    overflow: hidden;
  }

  .skill-bar-fill {
    position: absolute;
    top: 0; left: 0; height: 100%;
    background: var(--accent);
    width: 0;
    transition: width 1.2s cubic-bezier(0.4, 0, 0.2, 1);
  }

  .skill-evidence {
    margin-top: 20px;
    padding-top: 20px;
    border-top: 1px solid var(--border);
    font-size: 12px;
    color: var(--dim);
    line-height: 1.6;
  }

  /* ── EVIDENCE ── */
  .evidence-list {
    display: flex;
    flex-direction: column;
    gap: 2px;
  }

  .evidence-card {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 40px 44px;
    display: grid;
    grid-template-columns: 120px 1fr auto;
    gap: 48px;
    align-items: start;
    transition: border-color 0.2s;
  }

  .evidence-card:hover { border-color: #333; }

  .ev-type {
    font-size: 10px;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: var(--accent);
    font-weight: 600;
    padding-top: 4px;
  }

  .ev-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 24px;
    letter-spacing: 0.04em;
    color: var(--text);
    margin-bottom: 12px;
  }

  .ev-body {
    font-size: 13.5px;
    color: #888;
    line-height: 1.85;
  }

  .ev-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
    margin-top: 16px;
  }

  .ev-tag {
    font-size: 10px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--dim);
    border: 1px solid var(--border);
    padding: 3px 8px;
  }

  .ev-meta {
    text-align: right;
    font-size: 12px;
    color: var(--dim);
    line-height: 2.2;
    white-space: nowrap;
  }

  .ev-meta strong { color: var(--muted); display: block; font-weight: 500; }

  /* ── CERT HIGHLIGHT ── */
  .cert-card {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 48px;
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 48px;
    align-items: center;
    position: relative;
    overflow: hidden;
  }

  .cert-card::after {
    content: '';
    position: absolute;
    top: 0; right: 0;
    width: 3px; height: 100%;
    background: var(--accent);
  }

  .cert-badge-row {
    display: flex;
    gap: 16px;
    flex-wrap: wrap;
    margin-top: 24px;
  }

  .cert-badge {
    font-size: 11px;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--muted);
    border: 1px solid var(--border);
    padding: 6px 14px;
    display: flex;
    align-items: center;
    gap: 6px;
  }

  .cert-badge span { color: var(--accent); }

  .cert-number {
    text-align: center;
  }

  .cert-number-val {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 72px;
    line-height: 1;
    color: var(--accent);
    letter-spacing: -0.02em;
  }

  .cert-number-label {
    font-size: 11px;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--dim);
    margin-top: 6px;
  }

  /* ── FOOTER ── */
  footer {
    padding: 48px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .footer-left {
    font-size: 13px;
    color: var(--dim);
    line-height: 2;
  }

  .footer-right {
    font-size: 11px;
    color: var(--dim);
    text-align: right;
    letter-spacing: 0.06em;
    line-height: 2;
  }

  /* ── SCROLL REVEAL ── */
  .reveal {
    opacity: 0;
    transform: translateY(30px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }

  .reveal.visible {
    opacity: 1;
    transform: none;
  }

  @media (max-width: 900px) {
    nav { padding: 0 24px; }
    .nav-links { display: none; }
    .hero { padding: 0 24px 60px; }
    .hero-sub { flex-direction: column; }
    .hero-meta { text-align: left; }
    section { padding: 72px 24px; }
    .about-grid { grid-template-columns: 1fr; gap: 48px; }
    .skills-grid { grid-template-columns: 1fr; }
    .evidence-card { grid-template-columns: 1fr; gap: 24px; }
    .ev-meta { text-align: left; }
    .cert-card { grid-template-columns: 1fr; }
    .cert-number { text-align: left; }
    footer { flex-direction: column; gap: 20px; }
    .footer-right { text-align: left; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">
    <div class="nav-logo-mark">AB</div>
    <span class="nav-logo-text">Abu Bakar</span>
  </div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#evidence">Evidence</a></li>
  </ul>
  <div class="nav-badge">EAP2 · 2025/26</div>
</nav>

<!-- HERO -->
<div class="hero">
  <div class="hero-grid"></div>
  <div class="hero-glow"></div>
  <div class="hero-eyebrow">BSc (Hons) Business Management · Ravensbourne University London · Student ID 98732425</div>
  <div class="hero-name">Abu<br><span>Bakar</span></div>
  <div class="hero-sub">
    <p class="hero-desc">EAP2 — English for Academic Purposes 2 · Employability Skills Portfolio. Level 4, Semester 2, documenting six core skills developed through academic and independent work.</p>
    <div class="hero-meta">
      <strong>Assignment 3</strong>
      Employability Skills Webpage<br>
      <strong>Module</strong>
      English for Academic Purposes 2<br>
      <strong>Year</strong>
      2025 / 26
    </div>
  </div>
  <div class="hero-divider"></div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="section-header reveal">
    <span class="section-num">01</span>
    <h2 class="section-title">About This Portfolio</h2>
    <div class="section-line"></div>
  </div>
  <div class="about-grid">
    <div class="reveal">
      <div class="about-heading">What This Page Covers</div>
      <p class="about-body">This page documents the employability skills I have developed throughout the EAP2 module at Ravensbourne University London. The skills shown here are ones I actively worked on and can evidence through the assignments I completed this semester — the academic essay on NGO partnerships and CSR, the Bentley product placement presentation, and a LinkedIn Learning Critical Thinking course I completed independently.</p>
      <br>
      <p class="about-body">Each section explains what the skill is, how I developed it, and what evidence I have to show for it.</p>
    </div>
    <div class="about-stats reveal">
      <div class="stat-box">
        <div class="stat-label">Skills Documented</div>
        <div class="stat-value">06</div>
        <div class="stat-sub">Core EAP2 employability skills</div>
      </div>
      <div class="stat-box">
        <div class="stat-label">Assignments</div>
        <div class="stat-value">02</div>
        <div class="stat-sub">Essay + Presentation</div>
      </div>
      <div class="stat-box">
        <div class="stat-label">Harvard References</div>
        <div class="stat-value">10</div>
        <div class="stat-sub">NGO & CSR essay</div>
      </div>
      <div class="stat-box">
        <div class="stat-label">CPE Credits</div>
        <div class="stat-value">2.4</div>
        <div class="stat-sub">LinkedIn Learning · NASBA</div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-header reveal">
    <span class="section-num">02</span>
    <h2 class="section-title">Skills Developed</h2>
    <div class="section-line"></div>
  </div>
  <div class="skills-grid">

    <div class="skill-card reveal" data-fill="82">
      <div class="skill-tag">Core EAP2 Skill</div>
      <span class="skill-icon">✍️</span>
      <div class="skill-name">Academic Writing</div>
      <p class="skill-body">Academic writing is the ability to communicate ideas in a structured, evidence-based way that meets university standards. It means building a clear argument, organising paragraphs logically, and supporting every claim with credible sources.<br><br>The EAP2 essay on NGO partnerships and CSR forced me to follow the PEEL structure — Point, Explain, Evidence, Link — for every paragraph. By the final draft I was building arguments rather than listing ideas.</p>
      <div class="skill-bar-label"><span>Confidence Level</span><span>82%</span></div>
      <div class="skill-bar"><div class="skill-bar-fill"></div></div>
      <div class="skill-evidence">📄 NGO & CSR Essay · 1,200 words · PEEL structure · 10 Harvard references</div>
    </div>

    <div class="skill-card reveal" data-fill="80">
      <div class="skill-tag">Core EAP2 Skill</div>
      <span class="skill-icon">🔍</span>
      <div class="skill-name">Research Skills</div>
      <p class="skill-body">Research skills mean being able to find relevant, credible information from the right sources and use it to support academic work — knowing the difference between a reliable academic journal and a website anyone could have written.<br><br>I used sources from the Journal of Business Ethics, a 2025 study by Chaudhri, O'Connor and Tankovski, and Unilever's official sustainability reports. Learning to judge whether a source was actually credible was a real shift in how I work.</p>
      <div class="skill-bar-label"><span>Confidence Level</span><span>80%</span></div>
      <div class="skill-bar"><div class="skill-bar-fill"></div></div>
      <div class="skill-evidence">📄 NGO essay · Journal of Business Ethics · Chaudhri et al. (2025) · Unilever (2024)</div>
    </div>

    <div class="skill-card reveal" data-fill="78">
      <div class="skill-tag">Core EAP2 Skill</div>
      <span class="skill-icon">📚</span>
      <div class="skill-name">Harvard Referencing</div>
      <p class="skill-body">Harvard referencing acknowledges sources with in-text citations and a full reference list. Getting both right shows academic honesty and lets the reader trace the original source.<br><br>This was the skill I struggled with most. I kept mixing up formats — wrong order, missing year, unsure when to use narrative vs parenthetical citation. By the final essay I had ten properly formatted references and applied this consistently across the Bentley presentation too.</p>
      <div class="skill-bar-label"><span>Confidence Level</span><span>78%</span></div>
      <div class="skill-bar"><div class="skill-bar-fill"></div></div>
      <div class="skill-evidence">📄 Essay reference list (10 sources) + citation on every slide of Bentley presentation</div>
    </div>

    <div class="skill-card reveal" data-fill="75">
      <div class="skill-tag">Core EAP2 Skill</div>
      <span class="skill-icon">🎤</span>
      <div class="skill-name">Presentation Skills</div>
      <p class="skill-body">Presentation skills cover communicating ideas clearly and professionally using both visual and verbal methods. A good presentation tells a story, uses evidence and keeps the audience engaged from start to finish.<br><br>I developed this through a 10-slide PowerPoint on Bentley Motors' product placement across film, TV and social media — covering the James Bond franchise, The Crown, Peaky Blinders and Bentley's 2024 campaign. Every slide had a Harvard citation.</p>
      <div class="skill-bar-label"><span>Confidence Level</span><span>75%</span></div>
      <div class="skill-bar"><div class="skill-bar-fill"></div></div>
      <div class="skill-evidence">📊 10-slide Bentley product placement presentation · film, TV and social media examples</div>
    </div>

    <div class="skill-card reveal" data-fill="79">
      <div class="skill-tag">Core EAP2 Skill</div>
      <span class="skill-icon">💡</span>
      <div class="skill-name">Critical Thinking</div>
      <p class="skill-body">Critical thinking means going beyond description to question, analyse and evaluate ideas — not just saying what something is, but asking why it happens, what the evidence actually shows, and whether the conclusions hold up.<br><br>I developed this through the NGO essay and by completing a LinkedIn Learning course titled Critical Thinking, accredited by NASBA as a CPE programme. Completed 19 April 2026 — independently, beyond module requirements.</p>
      <div class="skill-bar-label"><span>Confidence Level</span><span>79%</span></div>
      <div class="skill-bar"><div class="skill-bar-fill"></div></div>
      <div class="skill-evidence">🎍 LinkedIn Learning Certificate · Critical Thinking (NASBA CPE, 19 April 2026) + NGO essay</div>
    </div>

    <div class="skill-card reveal" data-fill="84">
      <div class="skill-tag">Core EAP2 Skill</div>
      <span class="skill-icon">💻</span>
      <div class="skill-name">Digital Literacy</div>
      <p class="skill-body">Digital literacy is the ability to use digital tools effectively and responsibly — finding credible information online, using platforms for self-development, and creating professional digital content.<br><br>I used academic databases for peer-reviewed sources, built the Bentley presentation with digital design tools, completed LinkedIn Learning independently, and built this webpage as portfolio evidence. This connects to my PLP2 webinar on "Using AI Tools Ethically for Students."</p>
      <div class="skill-bar-label"><span>Confidence Level</span><span>84%</span></div>
      <div class="skill-bar"><div class="skill-bar-fill"></div></div>
      <div class="skill-evidence">🌐 LinkedIn Learning certificate + this ESL webpage + PLP2 AI Ethics webinar</div>
    </div>

  </div>
</section>

<!-- EVIDENCE -->
<section id="evidence">
  <div class="section-header reveal">
    <span class="section-num">03</span>
    <h2 class="section-title">Evidence</h2>
    <div class="section-line"></div>
  </div>

  <div class="evidence-list">

    <!-- LinkedIn Cert -->
    <div class="cert-card reveal">
      <div>
        <div class="skill-tag" style="margin-bottom:16px;">🎍 LinkedIn Learning · NASBA Accredited Certificate</div>
        <div class="ev-title">Critical Thinking — Course Completion Certificate</div>
        <p class="ev-body">This certificate was awarded by LinkedIn Learning on 19 April 2026 after completing the Critical Thinking course. The course is accredited by the National Association of State Boards of Accountancy (NASBA) as a Continuing Professional Education (CPE) programme with 2.40 CPE credits.<br><br>The course covered critical thinking and decision-making — specifically how to question assumptions, evaluate arguments and make informed decisions. Completed independently as additional evidence beyond EAP2 module requirements.</p>
        <div class="cert-badge-row">
          <div class="cert-badge">📅 <span>Completed</span> 19 April 2026</div>
          <div class="cert-badge">🎓 <span>Platform</span> LinkedIn Learning</div>
          <div class="cert-badge">📋 <span>Credits</span> 2.40 CPE</div>
          <div class="cert-badge">🏛 <span>Accredited by</span> NASBA</div>
          <div class="cert-badge">📂 <span>Registry</span> #140940</div>
        </div>
      </div>
      <div class="cert-number">
        <div class="cert-number-val">2.4</div>
        <div class="cert-number-label">CPE Credits</div>
      </div>
    </div>

    <!-- Essay -->
    <div class="evidence-card reveal">
      <div class="ev-type">Essay · Assignment 2</div>
      <div>
        <div class="ev-title">NGO & CSR Academic Essay</div>
        <p class="ev-body">1,200-word evidence-based essay on two mechanisms through which NGO partnerships strengthen CSR — legitimacy transfer and knowledge transfer. Written using PEEL paragraph structure. Ten properly formatted Harvard references including Journal of Business Ethics, Chaudhri et al. (2025) and Unilever's official sustainability reports.</p>
        <div class="ev-tags">
          <span class="ev-tag">Academic Writing</span>
          <span class="ev-tag">Research Skills</span>
          <span class="ev-tag">Harvard Referencing</span>
          <span class="ev-tag">Critical Thinking</span>
        </div>
      </div>
      <div class="ev-meta">
        <strong>1,200 words</strong>
        PEEL Structure<br>
        <strong>10 References</strong>
        Harvard Format
      </div>
    </div>

    <!-- Presentation -->
    <div class="evidence-card reveal">
      <div class="ev-type">Presentation · Assignment 1</div>
      <div>
        <div class="ev-title">Bentley Motors — Product Placement Presentation</div>
        <p class="ev-body">10-slide PowerPoint on Bentley's product placement strategy across film (Bond franchise, Layer Cake, Ocean's Eight), TV (The Crown, Peaky Blinders, Good Omens) and social media (11M Instagram followers, 2024 Gen B campaign). Harvard citations on every slide. Research question answered across all slides.</p>
        <div class="ev-tags">
          <span class="ev-tag">Presentation Skills</span>
          <span class="ev-tag">Research Skills</span>
          <span class="ev-tag">Harvard Referencing</span>
        </div>
      </div>
      <div class="ev-meta">
        <strong>10 Slides</strong>
        PowerPoint<br>
        <strong>Citations</strong>
        Every Slide
      </div>
    </div>

  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-left">
    Abu Bakar · Student ID: 98732425<br>
    BSc (Hons) Business Management · Ravensbourne University London 2025/26
  </div>
  <div class="footer-right">
    EAP2 · English for Academic Purposes 2<br>
    Assignment 3: Employability Skills Webpage
  </div>
</footer>

<script>
  // Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((e, i) => {
      if (e.isIntersecting) {
        setTimeout(() => e.target.classList.add('visible'), i * 80);
        observer.unobserve(e.target);
      }
    });
  }, { threshold: 0.08 });
  reveals.forEach(el => observer.observe(el));

  // Skill bar animation
  const barObserver = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        const card = e.target;
        const fill = card.querySelector('.skill-bar-fill');
        const pct = card.dataset.fill;
        if (fill && pct) fill.style.width = pct + '%';
        barObserver.unobserve(card);
      }
    });
  }, { threshold: 0.3 });
  document.querySelectorAll('.skill-card').forEach(el => barObserver.observe(el));
</script>
</body>
</html>

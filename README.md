<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ibtasam Ul Hassan Shah — Data Analyst</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=IBM+Plex+Mono:wght@300;400;500&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #080c10;
    --bg2: #0d1117;
    --bg3: #111820;
    --surface: #161e28;
    --surface2: #1c2534;
    --accent: #00e5b0;
    --accent2: #0099ff;
    --accent3: #ff5e5e;
    --text: #e8edf5;
    --text2: #8a9bb5;
    --text3: #4a5a72;
    --border: rgba(255,255,255,0.07);
    --border2: rgba(0,229,176,0.2);
    --glow: rgba(0,229,176,0.08);
    --ff-head: 'Syne', sans-serif;
    --ff-body: 'DM Sans', sans-serif;
    --ff-mono: 'IBM Plex Mono', monospace;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--ff-body);
    font-size: 16px;
    line-height: 1.7;
    overflow-x: hidden;
  }

  ::selection { background: rgba(0,229,176,0.25); color: var(--text); }

  /* ── SCROLLBAR ── */
  ::-webkit-scrollbar { width: 4px; }
  ::-webkit-scrollbar-track { background: var(--bg); }
  ::-webkit-scrollbar-thumb { background: var(--accent); border-radius: 4px; }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; justify-content: space-between; align-items: center;
    padding: 1.25rem 3rem;
    background: rgba(8,12,16,0.85);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
    transition: padding 0.3s ease;
  }
  .nav-logo {
    font-family: var(--ff-mono);
    font-size: 14px;
    color: var(--accent);
    letter-spacing: 0.05em;
  }
  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a {
    font-size: 13px;
    font-family: var(--ff-mono);
    color: var(--text2);
    text-decoration: none;
    letter-spacing: 0.08em;
    transition: color 0.2s;
    text-transform: uppercase;
  }
  .nav-links a:hover { color: var(--accent); }

  /* ── HERO ── */
  #hero {
    min-height: 100vh;
    display: flex; flex-direction: column; justify-content: center;
    padding: 7rem 3rem 4rem;
    position: relative;
    overflow: hidden;
  }

  .hero-grid {
    position: absolute; inset: 0; z-index: 0;
    background-image:
      linear-gradient(rgba(0,229,176,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,229,176,0.03) 1px, transparent 1px);
    background-size: 60px 60px;
    mask-image: radial-gradient(ellipse 80% 70% at 50% 50%, black, transparent);
  }

  .hero-orb {
    position: absolute;
    border-radius: 50%;
    filter: blur(80px);
    z-index: 0;
    pointer-events: none;
  }
  .orb1 {
    width: 500px; height: 500px;
    background: radial-gradient(circle, rgba(0,229,176,0.12), transparent 70%);
    top: -100px; right: 10%;
    animation: orb-float 8s ease-in-out infinite;
  }
  .orb2 {
    width: 400px; height: 400px;
    background: radial-gradient(circle, rgba(0,153,255,0.09), transparent 70%);
    bottom: 0; left: 5%;
    animation: orb-float 10s ease-in-out infinite reverse;
  }

  @keyframes orb-float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-30px); }
  }

  .hero-inner { position: relative; z-index: 1; max-width: 900px; }

  .hero-tag {
    display: inline-flex; align-items: center; gap: 8px;
    background: rgba(0,229,176,0.06);
    border: 1px solid var(--border2);
    border-radius: 100px;
    padding: 6px 16px;
    font-family: var(--ff-mono);
    font-size: 12px;
    color: var(--accent);
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 1.5rem;
    animation: fade-up 0.6s ease both;
  }
  .hero-tag::before {
    content: '';
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--accent);
    animation: pulse 2s ease infinite;
  }
  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(0.7); }
  }

  .hero-name {
    font-family: var(--ff-head);
    font-size: clamp(3rem, 8vw, 7rem);
    font-weight: 800;
    line-height: 0.95;
    letter-spacing: -0.03em;
    color: var(--text);
    animation: fade-up 0.6s ease 0.1s both;
  }
  .hero-name span {
    color: transparent;
    -webkit-text-stroke: 1px rgba(0,229,176,0.4);
  }

  .hero-title {
    font-family: var(--ff-head);
    font-size: clamp(1.5rem, 3.5vw, 2.8rem);
    font-weight: 600;
    color: var(--text2);
    margin-top: 0.5rem;
    animation: fade-up 0.6s ease 0.2s both;
  }
  .hero-title em {
    color: var(--accent);
    font-style: normal;
  }

  .hero-desc {
    max-width: 580px;
    color: var(--text2);
    margin-top: 1.5rem;
    font-size: 1.05rem;
    animation: fade-up 0.6s ease 0.3s both;
  }

  .hero-ctas {
    display: flex; gap: 1rem; flex-wrap: wrap;
    margin-top: 2.5rem;
    animation: fade-up 0.6s ease 0.4s both;
  }

  .btn-primary {
    display: inline-flex; align-items: center; gap: 8px;
    background: var(--accent);
    color: #000;
    font-family: var(--ff-mono);
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.05em;
    padding: 12px 24px;
    border-radius: 8px;
    text-decoration: none;
    border: none; cursor: pointer;
    transition: transform 0.15s, box-shadow 0.15s, background 0.15s;
  }
  .btn-primary:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 24px rgba(0,229,176,0.3);
  }

  .btn-ghost {
    display: inline-flex; align-items: center; gap: 8px;
    background: transparent;
    color: var(--text2);
    font-family: var(--ff-mono);
    font-size: 13px;
    letter-spacing: 0.05em;
    padding: 12px 24px;
    border-radius: 8px;
    text-decoration: none;
    border: 1px solid var(--border);
    cursor: pointer;
    transition: border-color 0.2s, color 0.2s, transform 0.15s;
  }
  .btn-ghost:hover {
    border-color: var(--accent);
    color: var(--accent);
    transform: translateY(-2px);
  }

  .hero-stats {
    display: flex; gap: 3rem; flex-wrap: wrap;
    margin-top: 4rem;
    padding-top: 2rem;
    border-top: 1px solid var(--border);
    animation: fade-up 0.6s ease 0.5s both;
  }
  .stat-item {}
  .stat-num {
    font-family: var(--ff-head);
    font-size: 2rem;
    font-weight: 700;
    color: var(--accent);
  }
  .stat-label {
    font-size: 13px;
    color: var(--text3);
    font-family: var(--ff-mono);
  }

  /* ── SECTION COMMON ── */
  section { padding: 6rem 3rem; }

  .section-header {
    display: flex; align-items: flex-end; gap: 1.5rem;
    margin-bottom: 4rem;
  }
  .section-num {
    font-family: var(--ff-mono);
    font-size: 13px;
    color: var(--accent);
    letter-spacing: 0.1em;
    padding-bottom: 0.4rem;
  }
  .section-title {
    font-family: var(--ff-head);
    font-size: clamp(1.8rem, 4vw, 3rem);
    font-weight: 700;
    line-height: 1.1;
    letter-spacing: -0.02em;
  }
  .section-line {
    flex: 1;
    height: 1px;
    background: var(--border);
    margin-bottom: 0.5rem;
    max-width: 200px;
  }

  /* ── ABOUT ── */
  #about { background: var(--bg2); }
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: start;
  }
  .about-text p { color: var(--text2); margin-bottom: 1.25rem; }
  .about-text p strong { color: var(--text); font-weight: 500; }

  .about-education { display: flex; flex-direction: column; gap: 1.5rem; }
  .edu-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.5rem;
    position: relative;
    overflow: hidden;
    transition: border-color 0.2s, transform 0.2s;
  }
  .edu-card::before {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 3px;
    background: var(--accent);
    border-radius: 3px 0 0 3px;
  }
  .edu-card:hover { border-color: var(--border2); transform: translateX(4px); }
  .edu-school {
    font-family: var(--ff-head);
    font-size: 1rem;
    font-weight: 700;
    color: var(--text);
  }
  .edu-degree {
    font-size: 14px;
    color: var(--text2);
    margin-top: 4px;
  }
  .edu-year {
    font-family: var(--ff-mono);
    font-size: 12px;
    color: var(--accent);
    margin-top: 8px;
  }

  .langs-grid {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 0.75rem;
    margin-top: 2rem;
  }
  .lang-item {
    display: flex; align-items: center; gap: 10px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 10px 14px;
    font-size: 13px;
  }
  .lang-flag { font-size: 18px; }
  .lang-name { color: var(--text); font-weight: 500; }
  .lang-level { color: var(--text3); font-family: var(--ff-mono); font-size: 11px; }

  /* ── EXPERIENCE ── */
  #experience { background: var(--bg3); }
  .timeline { position: relative; }
  .timeline::before {
    content: '';
    position: absolute;
    left: 18px; top: 0; bottom: 0;
    width: 1px;
    background: linear-gradient(to bottom, var(--accent), transparent);
  }
  .timeline-item {
    display: flex; gap: 2.5rem;
    margin-bottom: 3rem;
    opacity: 0;
    transform: translateX(-20px);
    transition: opacity 0.5s ease, transform 0.5s ease;
  }
  .timeline-item.visible { opacity: 1; transform: translateX(0); }

  .timeline-dot {
    width: 38px; height: 38px;
    flex-shrink: 0;
    border-radius: 50%;
    background: var(--surface);
    border: 2px solid var(--accent);
    display: flex; align-items: center; justify-content: center;
    font-size: 16px;
    position: relative; z-index: 1;
    margin-top: 2px;
  }

  .timeline-content {
    flex: 1;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.75rem;
    transition: border-color 0.2s;
  }
  .timeline-content:hover { border-color: var(--border2); }

  .xp-header { display: flex; justify-content: space-between; align-items: flex-start; gap: 1rem; flex-wrap: wrap; }
  .xp-company { font-family: var(--ff-mono); font-size: 12px; color: var(--accent); letter-spacing: 0.08em; text-transform: uppercase; }
  .xp-role { font-family: var(--ff-head); font-size: 1.15rem; font-weight: 700; color: var(--text); margin-top: 4px; }
  .xp-period {
    background: rgba(0,229,176,0.06);
    border: 1px solid var(--border2);
    border-radius: 100px;
    font-family: var(--ff-mono);
    font-size: 11px;
    color: var(--accent);
    padding: 4px 12px;
    white-space: nowrap;
  }
  .xp-tasks { margin-top: 1rem; display: flex; flex-direction: column; gap: 0.5rem; }
  .xp-task {
    display: flex; align-items: flex-start; gap: 10px;
    font-size: 14px; color: var(--text2);
  }
  .xp-task::before {
    content: '→';
    color: var(--accent);
    flex-shrink: 0;
    font-family: var(--ff-mono);
    margin-top: 2px;
  }
  .xp-tools { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 1.25rem; }
  .tool-tag {
    background: rgba(255,255,255,0.04);
    border: 1px solid var(--border);
    border-radius: 6px;
    font-family: var(--ff-mono);
    font-size: 11px;
    color: var(--text2);
    padding: 4px 10px;
    transition: background 0.2s, color 0.2s, border-color 0.2s;
  }
  .tool-tag:hover {
    background: rgba(0,229,176,0.06);
    color: var(--accent);
    border-color: var(--border2);
  }

  /* ── PROJECTS ── */
  #projects { background: var(--bg2); }
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
  }
  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 2rem;
    position: relative;
    overflow: hidden;
    cursor: default;
    transition: border-color 0.3s, transform 0.3s;
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.5s ease, transform 0.5s ease, border-color 0.2s;
  }
  .project-card.visible { opacity: 1; transform: translateY(0); }
  .project-card:hover { border-color: var(--border2); }

  .project-card::after {
    content: '';
    position: absolute;
    inset: 0;
    border-radius: 16px;
    background: radial-gradient(circle at 60% 0%, rgba(0,229,176,0.05), transparent 60%);
    opacity: 0;
    transition: opacity 0.3s;
    pointer-events: none;
  }
  .project-card:hover::after { opacity: 1; }

  .project-icon {
    width: 48px; height: 48px;
    border-radius: 12px;
    display: flex; align-items: center; justify-content: center;
    font-size: 22px;
    margin-bottom: 1.25rem;
  }
  .icon-teal { background: rgba(0,229,176,0.1); }
  .icon-blue { background: rgba(0,153,255,0.1); }
  .icon-coral { background: rgba(255,94,94,0.1); }

  .project-title {
    font-family: var(--ff-head);
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 0.5rem;
  }
  .project-type {
    font-family: var(--ff-mono);
    font-size: 11px;
    color: var(--accent);
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 1rem;
  }
  .project-desc { font-size: 14px; color: var(--text2); }
  .project-tags { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 1.5rem; }
  .project-tag {
    background: rgba(255,255,255,0.03);
    border: 1px solid var(--border);
    border-radius: 4px;
    font-family: var(--ff-mono);
    font-size: 11px;
    color: var(--text3);
    padding: 3px 8px;
  }

  /* ── SKILLS ── */
  #skills { background: var(--bg3); }
  .skills-wrapper {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
  }
  .skill-category-title {
    font-family: var(--ff-mono);
    font-size: 12px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 1.5rem;
  }
  .skill-items { display: flex; flex-direction: column; gap: 1rem; }
  .skill-item {}
  .skill-info { display: flex; justify-content: space-between; margin-bottom: 6px; }
  .skill-name { font-size: 14px; color: var(--text); }
  .skill-pct { font-family: var(--ff-mono); font-size: 12px; color: var(--accent); }
  .skill-bar {
    height: 3px;
    background: var(--surface2);
    border-radius: 3px;
    overflow: hidden;
  }
  .skill-fill {
    height: 100%;
    border-radius: 3px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    width: 0;
    transition: width 1s ease;
  }

  .tech-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
    gap: 0.75rem;
    margin-top: 2rem;
  }
  .tech-item {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 12px 8px;
    text-align: center;
    font-family: var(--ff-mono);
    font-size: 12px;
    color: var(--text2);
    transition: border-color 0.2s, color 0.2s, transform 0.2s;
  }
  .tech-item:hover {
    border-color: var(--border2);
    color: var(--accent);
    transform: translateY(-3px);
  }
  .tech-icon { font-size: 20px; margin-bottom: 6px; display: block; }

  /* ── CONTACT ── */
  #contact {
    background: var(--bg2);
    text-align: center;
  }
  .contact-inner { max-width: 640px; margin: 0 auto; }
  .contact-heading {
    font-family: var(--ff-head);
    font-size: clamp(2rem, 5vw, 4rem);
    font-weight: 800;
    letter-spacing: -0.03em;
    color: var(--text);
    line-height: 1.1;
    margin-bottom: 1.5rem;
  }
  .contact-heading span { color: var(--accent); }
  .contact-sub { color: var(--text2); font-size: 1.05rem; margin-bottom: 3rem; }
  .contact-links {
    display: flex; justify-content: center; flex-wrap: wrap; gap: 1rem;
  }
  .contact-link {
    display: flex; align-items: center; gap: 10px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 14px 20px;
    text-decoration: none;
    color: var(--text2);
    font-size: 14px;
    transition: border-color 0.2s, color 0.2s, transform 0.2s;
  }
  .contact-link:hover {
    border-color: var(--border2);
    color: var(--accent);
    transform: translateY(-2px);
  }
  .contact-link svg { width: 18px; height: 18px; }

  /* ── FOOTER ── */
  footer {
    background: var(--bg);
    border-top: 1px solid var(--border);
    padding: 2rem 3rem;
    display: flex; justify-content: space-between; align-items: center;
    flex-wrap: wrap; gap: 1rem;
  }
  .footer-brand {
    font-family: var(--ff-mono);
    font-size: 13px;
    color: var(--accent);
  }
  .footer-copy {
    font-size: 12px;
    color: var(--text3);
    font-family: var(--ff-mono);
  }

  /* ── SCROLL REVEAL ── */
  @keyframes fade-up {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 768px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    section { padding: 4rem 1.5rem; }
    #hero { padding: 6rem 1.5rem 3rem; }
    .about-grid { grid-template-columns: 1fr; }
    .skills-wrapper { grid-template-columns: 1fr; }
    .hero-stats { gap: 2rem; }
    footer { padding: 1.5rem; }
  }
</style>
</head>
<body>

<!-- ── NAVIGATION ── -->
<nav>
  <div class="nav-logo">ibtasam.dev</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- ── HERO ── -->
<section id="hero">
  <div class="hero-grid"></div>
  <div class="orb1 hero-orb"></div>
  <div class="orb2 hero-orb"></div>

  <div class="hero-inner">
    <div class="hero-tag">Available · Open to opportunities</div>

    <h1 class="hero-name">
      Ibtasam<br><span>Shah</span>
    </h1>

    <p class="hero-title">
      Data Analyst · <em>Data Scientist</em>
    </p>

    <p class="hero-desc">
      Étudiant en BUT Sciences des Données à l'IUT de Vannes. Je transforme des données brutes en insights qui ont du sens, en combinant rigueur statistique et compréhension métier.
    </p>

    <div class="hero-ctas">
      <a href="#projects" class="btn-primary">
        <svg width="14" height="14" viewBox="0 0 14 14" fill="none"><path d="M1 7h12M7 1l6 6-6 6" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
        Voir mes projets
      </a>
      <a href="mailto:ibtasam.uhs8@gmail.com" class="btn-ghost">
        <svg width="14" height="14" viewBox="0 0 14 14" fill="none"><path d="M1.5 3.5h11v8h-11v-8zM1.5 3.5l5.5 4 5.5-4" stroke="currentColor" stroke-width="1.3" stroke-linecap="round" stroke-linejoin="round"/></svg>
        Me contacter
      </a>
    </div>

    <div class="hero-stats">
      <div class="stat-item">
        <div class="stat-num">980<span style="font-size:1rem;color:var(--text3)">/990</span></div>
        <div class="stat-label">TOEIC — C1</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">3</div>
        <div class="stat-label">Expériences</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">4</div>
        <div class="stat-label">Langues</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">2026</div>
        <div class="stat-label">Diplôme BUT</div>
      </div>
    </div>
  </div>
</section>

<!-- ── ABOUT ── -->
<section id="about">
  <div class="section-header">
    <span class="section-num">01</span>
    <h2 class="section-title">À propos</h2>
    <div class="section-line"></div>
  </div>

  <div class="about-grid">
    <div class="about-text">
      <p>
        Je suis <strong>Ibtasam Ul Hassan Shah</strong>, étudiant en BUT Sciences des Données à l'IUT de Vannes (2024–2026), après deux années de classe préparatoire ingénierie à <strong>l'ESILV Paris La Défense</strong>.
      </p>
      <p>
        Mon approche mêle analyse exploratoire, modélisation statistique et visualisation pour produire des décisions appuyées par la donnée. Actuellement en alternance chez <strong>Novo Nordisk</strong> sur des projets People Analytics.
      </p>
      <p>
        Mon objectif : devenir Data Scientist capable de connecter les solutions techniques aux enjeux business, en construisant des systèmes intelligents à partir de données.
      </p>

      <div style="margin-top:2rem;">
        <p style="font-family:var(--ff-mono);font-size:12px;color:var(--accent);letter-spacing:0.08em;text-transform:uppercase;margin-bottom:1rem;">Langues</p>
        <div class="langs-grid">
          <div class="lang-item">
            <span class="lang-flag">🇬🇧</span>
            <div>
              <div class="lang-name">Anglais</div>
              <div class="lang-level">TOEIC 980 · C1</div>
            </div>
          </div>
          <div class="lang-item">
            <span class="lang-flag">🇪🇸</span>
            <div>
              <div class="lang-name">Espagnol</div>
              <div class="lang-level">B2</div>
            </div>
          </div>
          <div class="lang-item">
            <span class="lang-flag">🇮🇳</span>
            <div>
              <div class="lang-name">Hindi</div>
              <div class="lang-level">Avancé</div>
            </div>
          </div>
          <div class="lang-item">
            <span class="lang-flag">🇵🇰</span>
            <div>
              <div class="lang-name">Ourdou</div>
              <div class="lang-level">Bilingue</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="about-education">
      <p style="font-family:var(--ff-mono);font-size:12px;color:var(--accent);letter-spacing:0.08em;text-transform:uppercase;margin-bottom:0.5rem;">Formation</p>

      <div class="edu-card">
        <div class="edu-school">IUT de Vannes</div>
        <div class="edu-degree">BUT Sciences des Données</div>
        <div style="font-size:13px;color:var(--text3);margin-top:8px;">
          Analyse de données · Machine Learning · BI · Statistiques · Bases de données
        </div>
        <div class="edu-year">2024 — 2026</div>
      </div>

      <div class="edu-card">
        <div class="edu-school">ESILV Paris La Défense</div>
        <div class="edu-degree">Classe préparatoire ingénierie</div>
        <div style="font-size:13px;color:var(--text3);margin-top:8px;">
          Mathématiques · Algorithmique · Programmation · Modélisation
        </div>
        <div class="edu-year">2022 — 2024</div>
      </div>

      <div style="background:var(--surface);border:1px solid var(--border2);border-radius:12px;padding:1.25rem;margin-top:0.5rem;">
        <div style="font-family:var(--ff-mono);font-size:11px;color:var(--accent);letter-spacing:0.08em;text-transform:uppercase;margin-bottom:8px;">Objectif</div>
        <p style="font-size:14px;color:var(--text2);font-style:italic;">
          "Devenir Data Scientist capable de connecter les solutions techniques aux défis business."
        </p>
      </div>
    </div>
  </div>
</section>

<!-- ── EXPERIENCE ── -->
<section id="experience">
  <div class="section-header">
    <span class="section-num">02</span>
    <h2 class="section-title">Expériences</h2>
    <div class="section-line"></div>
  </div>

  <div class="timeline">

    <div class="timeline-item">
      <div class="timeline-dot">💊</div>
      <div class="timeline-content">
        <div class="xp-header">
          <div>
            <div class="xp-company">Novo Nordisk</div>
            <div class="xp-role">Data Analyst RH — Alternance</div>
          </div>
          <span class="xp-period">2025 — 2026</span>
        </div>
        <div class="xp-tasks">
          <div class="xp-task">Analyse de datasets RH — People Analytics</div>
          <div class="xp-task">Indicateurs workforce, recrutement et turnover</div>
          <div class="xp-task">Monitoring de l'absentéisme</div>
          <div class="xp-task">Conception et déploiement de dashboards Power BI</div>
        </div>
        <div class="xp-tools">
          <span class="tool-tag">Power BI</span>
          <span class="tool-tag">SQL</span>
          <span class="tool-tag">Excel</span>
          <span class="tool-tag">Data Analysis</span>
        </div>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-dot">✈️</div>
      <div class="timeline-content">
        <div class="xp-header">
          <div>
            <div class="xp-company">Thales LAS France</div>
            <div class="xp-role">Data Analyst Obsolescence — Stage</div>
          </div>
          <span class="xp-period">Mars — Juin 2025</span>
        </div>
        <div class="xp-tasks">
          <div class="xp-task">Nettoyage et préparation de données industrielles</div>
          <div class="xp-task">Structuration de bases de données</div>
          <div class="xp-task">Analyse de stocks et BOM (Bill of Materials)</div>
          <div class="xp-task">Intégration de données SAP</div>
          <div class="xp-task">Prévision des besoins futurs en composants</div>
        </div>
        <div class="xp-tools">
          <span class="tool-tag">Python</span>
          <span class="tool-tag">Power BI</span>
          <span class="tool-tag">SQL</span>
          <span class="tool-tag">Excel</span>
          <span class="tool-tag">SAP</span>
        </div>
      </div>
    </div>

    <div class="timeline-item">
      <div class="timeline-dot">📰</div>
      <div class="timeline-content">
        <div class="xp-header">
          <div>
            <div class="xp-company">L'AGEFI</div>
            <div class="xp-role">Data Management</div>
          </div>
          <span class="xp-period">2024</span>
        </div>
        <div class="xp-tasks">
          <div class="xp-task">Contrôle qualité des données</div>
          <div class="xp-task">Validation d'informations financières</div>
          <div class="xp-task">Gestion de bases de données</div>
          <div class="xp-task">Traitement de flux numériques</div>
        </div>
        <div class="xp-tools">
          <span class="tool-tag">Excel</span>
          <span class="tool-tag">Data Quality</span>
          <span class="tool-tag">Databases</span>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- ── PROJECTS ── -->
<section id="projects">
  <div class="section-header">
    <span class="section-num">03</span>
    <h2 class="section-title">Projets</h2>
    <div class="section-line"></div>
  </div>

  <div class="projects-grid">

    <div class="project-card">
      <div class="project-icon icon-coral">🚗</div>
      <div class="project-type">Power BI · Data Viz</div>
      <div class="project-title">Accidents de la Route en France</div>
      <p class="project-desc">
        Dashboard interactif analysant les accidents routiers selon les conditions météo, la localisation, la gravité et l'évolution temporelle. Pipeline complet de cleaning à visualisation.
      </p>
      <div class="project-tags">
        <span class="project-tag">Power BI</span>
        <span class="project-tag">Data Cleaning</span>
        <span class="project-tag">Dashboard</span>
        <span class="project-tag">France</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-icon icon-blue">🏅</div>
      <div class="project-type">R · Statistiques</div>
      <div class="project-title">Analyse des Jeux Olympiques</div>
      <p class="project-desc">
        Étude statistique approfondie des données historiques des Jeux Olympiques. EDA, analyses multivariées, visualisations et interprétations des performances des nations.
      </p>
      <div class="project-tags">
        <span class="project-tag">R</span>
        <span class="project-tag">EDA</span>
        <span class="project-tag">Statistics</span>
        <span class="project-tag">ggplot2</span>
      </div>
    </div>

    <div class="project-card">
      <div class="project-icon icon-teal">🔧</div>
      <div class="project-type">BI · Industrie</div>
      <div class="project-title">Dashboard Obsolescence Industrielle</div>
      <p class="project-desc">
        Outil d'aide à la décision combinant données de stocks, cycles de vie des composants et prévisions. Aide les équipes à anticiper les risques liés aux composants obsolètes.
      </p>
      <div class="project-tags">
        <span class="project-tag">Python</span>
        <span class="project-tag">Power BI</span>
        <span class="project-tag">SAP</span>
        <span class="project-tag">Forecasting</span>
      </div>
    </div>

  </div>
</section>

<!-- ── SKILLS ── -->
<section id="skills">
  <div class="section-header">
    <span class="section-num">04</span>
    <h2 class="section-title">Compétences</h2>
    <div class="section-line"></div>
  </div>

  <div class="skills-wrapper">
    <div>
      <p class="skill-category-title">Analyse & Stats</p>
      <div class="skill-items">
        <div class="skill-item">
          <div class="skill-info"><span class="skill-name">Data Analysis & EDA</span><span class="skill-pct">92%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="92"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-info"><span class="skill-name">Modélisation statistique</span><span class="skill-pct">80%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="80"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-info"><span class="skill-name">Machine Learning</span><span class="skill-pct">72%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="72"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-info"><span class="skill-name">Data Visualization</span><span class="skill-pct">88%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="88"></div></div>
        </div>
      </div>

      <p class="skill-category-title" style="margin-top:2.5rem;">BI & Reporting</p>
      <div class="skill-items">
        <div class="skill-item">
          <div class="skill-info"><span class="skill-name">Power BI</span><span class="skill-pct">90%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="90"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-info"><span class="skill-name">Excel / VBA</span><span class="skill-pct">85%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="85"></div></div>
        </div>
        <div class="skill-item">
          <div class="skill-info"><span class="skill-name">Tableau</span><span class="skill-pct">70%</span></div>
          <div class="skill-bar"><div class="skill-fill" data-width="70"></div></div>
        </div>
      </div>
    </div>

    <div>
      <p class="skill-category-title">Stack technique</p>
      <div class="tech-grid">
        <div class="tech-item"><span class="tech-icon">🐍</span>Python</div>
        <div class="tech-item"><span class="tech-icon">📊</span>R</div>
        <div class="tech-item"><span class="tech-icon">🗄️</span>SQL</div>
        <div class="tech-item"><span class="tech-icon">📈</span>Power BI</div>
        <div class="tech-item"><span class="tech-icon">📗</span>Excel</div>
        <div class="tech-item"><span class="tech-icon">⚙️</span>VBA</div>
        <div class="tech-item"><span class="tech-icon">🔄</span>Talend</div>
        <div class="tech-item"><span class="tech-icon">💾</span>SAP</div>
        <div class="tech-item"><span class="tech-icon">🖥️</span>C++</div>
        <div class="tech-item"><span class="tech-icon">🌐</span>HTML/CSS</div>
        <div class="tech-item"><span class="tech-icon">🗃️</span>Access</div>
        <div class="tech-item"><span class="tech-icon">🔬</span>Tableau</div>
      </div>

      <p class="skill-category-title" style="margin-top:2.5rem;">Savoir-faire</p>
      <div style="display:flex;flex-wrap:wrap;gap:8px;">
        <span class="tool-tag">Hypothesis testing</span>
        <span class="tool-tag">Régression</span>
        <span class="tool-tag">ACP / AFC</span>
        <span class="tool-tag">Séries temporelles</span>
        <span class="tool-tag">KPI Design</span>
        <span class="tool-tag">Reporting</span>
        <span class="tool-tag">Data Quality</span>
        <span class="tool-tag">ETL</span>
        <span class="tool-tag">People Analytics</span>
        <span class="tool-tag">Forecasting</span>
      </div>
    </div>
  </div>
</section>

<!-- ── CONTACT ── -->
<section id="contact">
  <div class="contact-inner">
    <h2 class="contact-heading">
      Parlons<br><span>données</span>
    </h2>
    <p class="contact-sub">
      Je cherche des opportunités en Data Analytics, Business Intelligence ou Data Science. Alternance, stage, CDI — écrivez-moi !
    </p>

    <div class="contact-links">
      <a href="mailto:ibtasam.uhs8@gmail.com" class="contact-link">
        <svg viewBox="0 0 18 18" fill="none" stroke="currentColor" stroke-width="1.3" stroke-linecap="round" stroke-linejoin="round">
          <rect x="1.5" y="3.5" width="15" height="11" rx="2"/>
          <path d="M1.5 4.5l7.5 5.5 7.5-5.5"/>
        </svg>
        ibtasam.uhs8@gmail.com
      </a>
      <a href="https://linkedin.com" class="contact-link" target="_blank">
        <svg viewBox="0 0 18 18" fill="none" stroke="currentColor" stroke-width="1.3" stroke-linecap="round" stroke-linejoin="round">
          <rect x="1.5" y="1.5" width="15" height="15" rx="3"/>
          <path d="M5.5 8v5"/>
          <path d="M5.5 5.5v.01"/>
          <path d="M9 8v5"/>
          <path d="M9 10.5a2.5 2.5 0 0 1 5 0V13"/>
        </svg>
        LinkedIn
      </a>
      <a href="https://github.com" class="contact-link" target="_blank">
        <svg viewBox="0 0 18 18" fill="none" stroke="currentColor" stroke-width="1.3" stroke-linecap="round" stroke-linejoin="round">
          <path d="M9 2a7 7 0 0 0-2.213 13.635c.35.064.478-.152.478-.337 0-.166-.006-.605-.01-1.188-1.946.423-2.357-.938-2.357-.938-.318-.809-.777-1.025-.777-1.025-.636-.434.048-.425.048-.425.703.05 1.073.722 1.073.722.625 1.07 1.638.761 2.037.582.063-.453.244-.761.445-.937-1.554-.176-3.188-.777-3.188-3.46 0-.764.273-1.389.722-1.879-.073-.177-.313-.888.068-1.851 0 0 .589-.188 1.929.719A6.717 6.717 0 0 1 9 5.744c.597.003 1.198.08 1.758.236 1.338-.907 1.926-.719 1.926-.719.383.963.142 1.674.07 1.851.45.49.72 1.115.72 1.879 0 2.69-1.636 3.282-3.196 3.454.251.216.475.643.475 1.296 0 .936-.009 1.69-.009 1.92 0 .187.126.405.482.337A7.002 7.002 0 0 0 9 2z"/>
        </svg>
        GitHub
      </a>
    </div>
  </div>
</section>

<!-- ── FOOTER ── -->
<footer>
  <span class="footer-brand">ibtasam.dev</span>
  <span class="footer-copy">© 2025 Ibtasam Ul Hassan Shah — Data Analyst</span>
</footer>

<script>
  /* Intersection Observer for scroll reveals */
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
        if (e.target.classList.contains('skill-fill')) {
          e.target.style.width = e.target.dataset.width + '%';
        }
      }
    });
  }, { threshold: 0.15 });

  document.querySelectorAll('.timeline-item, .project-card').forEach(el => observer.observe(el));

  /* Skill bars */
  const skillObs = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.querySelectorAll('.skill-fill').forEach(bar => {
          bar.style.width = bar.dataset.width + '%';
        });
      }
    });
  }, { threshold: 0.3 });
  document.querySelectorAll('.skill-items').forEach(el => skillObs.observe(el));

  /* Stagger project cards */
  document.querySelectorAll('.project-card').forEach((el, i) => {
    el.style.transitionDelay = (i * 0.12) + 's';
  });

  /* Nav shrink on scroll */
  const nav = document.querySelector('nav');
  window.addEventListener('scroll', () => {
    nav.style.padding = window.scrollY > 60 ? '0.75rem 3rem' : '1.25rem 3rem';
  });

  /* Cursor glow effect */
  const glow = document.createElement('div');
  glow.style.cssText = 'position:fixed;width:400px;height:400px;border-radius:50%;background:radial-gradient(circle,rgba(0,229,176,0.04),transparent 70%);pointer-events:none;transition:transform 0.15s ease;z-index:0;top:0;left:0;transform:translate(-50%,-50%)';
  document.body.appendChild(glow);
  document.addEventListener('mousemove', e => {
    glow.style.transform = `translate(calc(${e.clientX}px - 50%), calc(${e.clientY}px - 50%))`;
  });
</script>
</body>
</html>

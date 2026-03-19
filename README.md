<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Harishchandra Prajapati — Pharma Sales Leader</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;0,700;0,900;1,400;1,600&family=DM+Sans:wght@300;400;500&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #0f1117;
    --paper: #faf8f3;
    --gold: #c8963e;
    --gold-light: #e8b85a;
    --rust: #b85c38;
    --sage: #4a6741;
    --mid: #6b6560;
    --border: rgba(200,150,62,0.2);
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--paper);
    color: var(--ink);
    font-family: 'DM Sans', sans-serif;
    font-weight: 300;
    overflow-x: hidden;
  }

  /* ─── NOISE TEXTURE OVERLAY ─── */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 9999;
    opacity: 0.4;
  }

  /* ─── NAV ─── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.4rem 4rem;
    background: rgba(250,248,243,0.88);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
  }

  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    font-weight: 700;
    letter-spacing: 0.05em;
    color: var(--ink);
    text-decoration: none;
  }

  .nav-links {
    display: flex;
    gap: 2.5rem;
    list-style: none;
  }

  .nav-links a {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--mid);
    text-decoration: none;
    transition: color 0.2s;
  }

  .nav-links a:hover { color: var(--gold); }

  /* ─── HERO ─── */
  #hero {
    min-height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    position: relative;
    overflow: hidden;
  }

  .hero-left {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 8rem 4rem 4rem 4rem;
    position: relative;
    z-index: 2;
  }

  .hero-tag {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1.5rem;
    display: flex;
    align-items: center;
    gap: 0.8rem;
  }

  .hero-tag::before {
    content: '';
    width: 32px;
    height: 1px;
    background: var(--gold);
  }

  .hero-name {
    font-family: 'Playfair Display', serif;
    font-size: clamp(3rem, 5vw, 5.5rem);
    font-weight: 900;
    line-height: 1.05;
    color: var(--ink);
    margin-bottom: 0.3rem;
  }

  .hero-name span {
    color: var(--gold);
    font-style: italic;
  }

  .hero-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1rem, 1.6vw, 1.4rem);
    font-weight: 400;
    font-style: italic;
    color: var(--mid);
    margin-bottom: 2.5rem;
    letter-spacing: 0.03em;
  }

  .hero-bio {
    font-size: 1rem;
    line-height: 1.75;
    color: var(--mid);
    max-width: 420px;
    margin-bottom: 3rem;
  }

  .hero-bio strong {
    color: var(--ink);
    font-weight: 500;
  }

  .hero-stats {
    display: flex;
    gap: 2.5rem;
    margin-bottom: 3rem;
  }

  .stat {
    display: flex;
    flex-direction: column;
    gap: 0.2rem;
  }

  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2.2rem;
    font-weight: 900;
    color: var(--ink);
    line-height: 1;
  }

  .stat-num sup {
    font-size: 1rem;
    color: var(--gold);
  }

  .stat-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--mid);
  }

  .hero-cta {
    display: inline-flex;
    align-items: center;
    gap: 0.75rem;
    padding: 0.9rem 2rem;
    background: var(--ink);
    color: var(--paper);
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    text-decoration: none;
    transition: background 0.25s, gap 0.25s;
    width: fit-content;
  }

  .hero-cta:hover {
    background: var(--gold);
    gap: 1.2rem;
  }

  .hero-cta svg { transition: transform 0.25s; }
  .hero-cta:hover svg { transform: translateX(4px); }

  .hero-right {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .hero-backdrop {
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, #1a1208 0%, #2d1e0a 40%, #3d2912 100%);
  }

  .hero-pattern {
    position: absolute;
    inset: 0;
    background-image:
      repeating-linear-gradient(45deg, rgba(200,150,62,0.06) 0, rgba(200,150,62,0.06) 1px, transparent 0, transparent 50%);
    background-size: 30px 30px;
  }

  .hero-circle {
    position: absolute;
    width: 420px;
    height: 420px;
    border-radius: 50%;
    border: 1px solid rgba(200,150,62,0.25);
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }

  .hero-circle::before {
    content: '';
    position: absolute;
    inset: 30px;
    border-radius: 50%;
    border: 1px solid rgba(200,150,62,0.15);
  }

  .hero-initials {
    font-family: 'Playfair Display', serif;
    font-size: 9rem;
    font-weight: 900;
    color: rgba(200,150,62,0.15);
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -52%);
    letter-spacing: -0.05em;
    user-select: none;
  }

  .hero-badge {
    position: absolute;
    bottom: 2.5rem;
    right: 2.5rem;
    width: 120px;
    height: 120px;
    border-radius: 50%;
    border: 1px solid rgba(200,150,62,0.4);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: var(--gold-light);
    text-align: center;
    animation: spin-slow 20s linear infinite;
  }

  @keyframes spin-slow {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
  }

  .hero-badge-text {
    font-family: 'DM Mono', monospace;
    font-size: 0.55rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    line-height: 2.2;
    color: rgba(200,150,62,0.7);
    position: absolute;
    width: 100%;
    top: 50%;
    transform: translateY(-50%);
    text-align: center;
    animation: counter-spin 20s linear infinite;
  }

  @keyframes counter-spin {
    from { transform: translateY(-50%) rotate(0deg); }
    to { transform: translateY(-50%) rotate(-360deg); }
  }

  .hero-scroll {
    position: absolute;
    bottom: 2rem;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;
    color: var(--mid);
    font-family: 'DM Mono', monospace;
    font-size: 0.6rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    z-index: 3;
  }

  .scroll-line {
    width: 1px;
    height: 40px;
    background: linear-gradient(to bottom, var(--gold), transparent);
    animation: scroll-pulse 2s ease-in-out infinite;
  }

  @keyframes scroll-pulse {
    0%, 100% { opacity: 0.4; transform: scaleY(1); }
    50% { opacity: 1; transform: scaleY(1.2); }
  }

  /* ─── SECTION BASE ─── */
  section { padding: 7rem 4rem; }

  .section-eyebrow {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1rem;
    display: flex;
    align-items: center;
    gap: 0.8rem;
  }

  .section-eyebrow::before {
    content: '';
    width: 24px;
    height: 1px;
    background: var(--gold);
  }

  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 3.5vw, 3rem);
    font-weight: 700;
    line-height: 1.15;
    color: var(--ink);
    margin-bottom: 1rem;
  }

  /* ─── EXPERIENCE ─── */
  #experience {
    background: var(--ink);
    color: var(--paper);
  }

  #experience .section-title { color: var(--paper); }

  .exp-grid {
    display: grid;
    grid-template-columns: 1fr 2fr;
    gap: 4rem;
    margin-top: 4rem;
  }

  .exp-left p {
    color: rgba(250,248,243,0.55);
    line-height: 1.75;
    font-size: 0.95rem;
    max-width: 280px;
  }

  .exp-timeline {
    display: flex;
    flex-direction: column;
    gap: 0;
  }

  .exp-item {
    display: grid;
    grid-template-columns: 120px 1fr;
    gap: 2rem;
    padding: 2.5rem 0;
    border-bottom: 1px solid rgba(200,150,62,0.15);
    position: relative;
    transition: background 0.3s;
  }

  .exp-item:first-child { border-top: 1px solid rgba(200,150,62,0.15); }

  .exp-item::before {
    content: '';
    position: absolute;
    left: -2px;
    top: 0;
    bottom: 0;
    width: 2px;
    background: var(--gold);
    transform: scaleY(0);
    transition: transform 0.4s;
    transform-origin: top;
  }

  .exp-item:hover::before { transform: scaleY(1); }

  .exp-period {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.1em;
    color: var(--gold);
    padding-top: 0.3rem;
  }

  .exp-company {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem;
    font-weight: 700;
    color: var(--paper);
    margin-bottom: 0.3rem;
  }

  .exp-role {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.1em;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 0.8rem;
  }

  .exp-desc {
    font-size: 0.92rem;
    color: rgba(250,248,243,0.6);
    line-height: 1.7;
  }

  .exp-tag {
    display: inline-block;
    margin-top: 1rem;
    padding: 0.3rem 0.9rem;
    border: 1px solid rgba(200,150,62,0.3);
    font-family: 'DM Mono', monospace;
    font-size: 0.62rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--gold);
  }

  /* ─── PHILOSOPHY ─── */
  #philosophy {
    background: var(--paper);
  }

  .phil-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2px;
    margin-top: 4rem;
  }

  .phil-card {
    background: #fff;
    padding: 2.5rem;
    border: 1px solid rgba(200,150,62,0.12);
    position: relative;
    overflow: hidden;
    transition: transform 0.3s, box-shadow 0.3s;
  }

  .phil-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 20px 60px rgba(200,150,62,0.12);
  }

  .phil-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--gold), var(--rust));
    transform: scaleX(0);
    transition: transform 0.4s;
    transform-origin: left;
  }

  .phil-card:hover::after { transform: scaleX(1); }

  .phil-icon {
    font-size: 2rem;
    margin-bottom: 1.2rem;
    display: block;
  }

  .phil-heading {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem;
    font-weight: 700;
    margin-bottom: 0.8rem;
    color: var(--ink);
  }

  .phil-text {
    font-size: 0.9rem;
    color: var(--mid);
    line-height: 1.75;
  }

  /* ─── EXPERTISE ─── */
  #expertise {
    background: #f0ece3;
  }

  .expertise-wrap {
    display: grid;
    grid-template-columns: 1.2fr 1fr;
    gap: 5rem;
    margin-top: 4rem;
    align-items: center;
  }

  .skill-list {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }

  .skill-row {}

  .skill-header {
    display: flex;
    justify-content: space-between;
    margin-bottom: 0.5rem;
  }

  .skill-name {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--ink);
  }

  .skill-pct {
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    color: var(--gold);
  }

  .skill-bar {
    height: 4px;
    background: rgba(0,0,0,0.08);
    position: relative;
    overflow: hidden;
  }

  .skill-fill {
    position: absolute;
    top: 0; left: 0; bottom: 0;
    background: linear-gradient(90deg, var(--gold), var(--rust));
    width: 0;
    transition: width 1.2s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  }

  .expertise-quote {
    padding: 3rem;
    background: var(--ink);
    color: var(--paper);
    position: relative;
  }

  .expertise-quote::before {
    content: '\201C';
    font-family: 'Playfair Display', serif;
    font-size: 8rem;
    font-weight: 900;
    color: var(--gold);
    opacity: 0.2;
    position: absolute;
    top: -1rem;
    left: 1.5rem;
    line-height: 1;
  }

  .quote-text {
    font-family: 'Playfair Display', serif;
    font-size: 1.25rem;
    font-style: italic;
    line-height: 1.65;
    color: var(--paper);
    position: relative;
    z-index: 1;
    margin-bottom: 1.5rem;
  }

  .quote-attr {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--gold);
  }

  /* ─── LEADERSHIP ─── */
  #leadership {
    background: var(--ink);
    color: var(--paper);
  }

  #leadership .section-title { color: var(--paper); }

  .lead-intro {
    color: rgba(250,248,243,0.55);
    max-width: 520px;
    line-height: 1.75;
    margin-bottom: 4rem;
  }

  .lead-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1.5rem;
  }

  .lead-card {
    padding: 2rem;
    border: 1px solid rgba(200,150,62,0.2);
    position: relative;
    transition: border-color 0.3s;
  }

  .lead-card:hover { border-color: var(--gold); }

  .lead-num {
    font-family: 'Playfair Display', serif;
    font-size: 3.5rem;
    font-weight: 900;
    color: rgba(200,150,62,0.12);
    position: absolute;
    top: 0.5rem;
    right: 1rem;
    line-height: 1;
  }

  .lead-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.15rem;
    font-weight: 700;
    color: var(--paper);
    margin-bottom: 0.7rem;
  }

  .lead-text {
    font-size: 0.88rem;
    color: rgba(250,248,243,0.55);
    line-height: 1.7;
  }

  /* ─── INTERESTS ─── */
  #interests {
    background: var(--paper);
  }

  .interests-row {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 2rem;
    margin-top: 4rem;
  }

  .interest-item {
    text-align: center;
    padding: 2.5rem 1.5rem;
    border: 1px solid var(--border);
    transition: border-color 0.3s, background 0.3s;
    cursor: default;
  }

  .interest-item:hover {
    border-color: var(--gold);
    background: rgba(200,150,62,0.04);
  }

  .interest-icon {
    font-size: 2.5rem;
    margin-bottom: 1rem;
    display: block;
  }

  .interest-name {
    font-family: 'Playfair Display', serif;
    font-size: 1rem;
    font-weight: 700;
    color: var(--ink);
    margin-bottom: 0.4rem;
  }

  .interest-sub {
    font-size: 0.8rem;
    color: var(--mid);
    line-height: 1.5;
  }

  /* ─── CONNECT ─── */
  #connect {
    background: linear-gradient(135deg, #1a1208 0%, #2d1e0a 100%);
    text-align: center;
    position: relative;
    overflow: hidden;
  }

  #connect::before {
    content: '';
    position: absolute;
    inset: 0;
    background-image: repeating-linear-gradient(45deg, rgba(200,150,62,0.05) 0, rgba(200,150,62,0.05) 1px, transparent 0, transparent 50%);
    background-size: 30px 30px;
  }

  .connect-inner { position: relative; z-index: 1; }

  #connect .section-eyebrow { justify-content: center; }
  #connect .section-eyebrow::before { display: none; }

  #connect .section-title {
    color: var(--paper);
    font-size: clamp(2.5rem, 4vw, 4rem);
    margin-bottom: 1.5rem;
  }

  .connect-sub {
    color: rgba(250,248,243,0.55);
    font-size: 1rem;
    max-width: 480px;
    margin: 0 auto 3.5rem;
    line-height: 1.75;
  }

  .connect-links {
    display: flex;
    gap: 1.5rem;
    justify-content: center;
    flex-wrap: wrap;
  }

  .connect-link {
    display: inline-flex;
    align-items: center;
    gap: 0.6rem;
    padding: 0.9rem 2rem;
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    text-decoration: none;
    transition: all 0.25s;
  }

  .connect-link.primary {
    background: var(--gold);
    color: var(--ink);
  }

  .connect-link.primary:hover { background: var(--gold-light); }

  .connect-link.secondary {
    border: 1px solid rgba(200,150,62,0.4);
    color: var(--gold);
  }

  .connect-link.secondary:hover {
    border-color: var(--gold);
    background: rgba(200,150,62,0.08);
  }

  /* ─── FOOTER ─── */
  footer {
    background: #0a0c10;
    padding: 2rem 4rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-top: 1px solid rgba(200,150,62,0.1);
  }

  .footer-name {
    font-family: 'Playfair Display', serif;
    font-size: 0.9rem;
    color: rgba(250,248,243,0.4);
  }

  .footer-note {
    font-family: 'DM Mono', monospace;
    font-size: 0.6rem;
    letter-spacing: 0.12em;
    color: rgba(250,248,243,0.25);
    text-transform: uppercase;
  }

  /* ─── ANIMATIONS ─── */
  .fade-up {
    opacity: 0;
    transform: translateY(28px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }

  .fade-up.visible {
    opacity: 1;
    transform: translateY(0);
  }

  .delay-1 { transition-delay: 0.1s; }
  .delay-2 { transition-delay: 0.2s; }
  .delay-3 { transition-delay: 0.3s; }
  .delay-4 { transition-delay: 0.4s; }
  .delay-5 { transition-delay: 0.5s; }

  /* ─── RESPONSIVE ─── */
  @media (max-width: 900px) {
    nav { padding: 1.2rem 2rem; }
    .nav-links { display: none; }
    #hero { grid-template-columns: 1fr; }
    .hero-right { display: none; }
    .hero-left { padding: 7rem 2rem 4rem; }
    section { padding: 5rem 2rem; }
    .exp-grid { grid-template-columns: 1fr; gap: 2rem; }
    .exp-item { grid-template-columns: 1fr; gap: 0.5rem; }
    .phil-grid { grid-template-columns: 1fr; }
    .expertise-wrap { grid-template-columns: 1fr; }
    .lead-grid { grid-template-columns: 1fr; }
    .interests-row { grid-template-columns: 1fr 1fr; }
    footer { flex-direction: column; gap: 0.5rem; text-align: center; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#hero" class="nav-logo">H.P.</a>
  <ul class="nav-links">
    <li><a href="#experience">Experience</a></li>
    <li><a href="#philosophy">Philosophy</a></li>
    <li><a href="#expertise">Expertise</a></li>
    <li><a href="#leadership">Leadership</a></li>
    <li><a href="#connect">Connect</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-left">
    <div class="hero-tag">Pharma Sales Leader · 18+ Years</div>
    <h1 class="hero-name">
      Harishchandra<br><span>Prajapati</span>
    </h1>
    <p class="hero-title">Sales & Marketing Professional · Derma & Cosmetic Segment</p>
    <p class="hero-bio">
      A <strong>disciplined, people-first leader</strong> who has spent nearly two decades building territories, developing high-performing teams, and growing brands across India's pharmaceutical landscape. Currently driving growth in the <strong>derma-cosmetic segment</strong> at Akumentis Healthcare.
    </p>
    <div class="hero-stats">
      <div class="stat">
        <span class="stat-num">18<sup>+</sup></span>
        <span class="stat-label">Years in Pharma</span>
      </div>
      <div class="stat">
        <span class="stat-num">10<sup>+</sup></span>
        <span class="stat-label">Years in Leadership</span>
      </div>
      <div class="stat">
        <span class="stat-num">3</span>
        <span class="stat-label">Iconic Companies</span>
      </div>
    </div>
    <a href="#experience" class="hero-cta">
      View My Journey
      <svg width="16" height="16" viewBox="0 0 16 16" fill="none">
        <path d="M3 8h10M9 4l4 4-4 4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>
    </a>
  </div>
  <div class="hero-right">
    <div class="hero-backdrop"></div>
    <div class="hero-pattern"></div>
    <div class="hero-circle"></div>
    <div class="hero-initials">HP</div>
    <div class="hero-badge">
      <div class="hero-badge-text">Pharma · Derma · Cosmetic · Leadership ·&nbsp;</div>
    </div>
  </div>
  <div class="hero-scroll">
    <div class="scroll-line"></div>
    Scroll
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="section-eyebrow">Career Journey</div>
  <h2 class="section-title">18 Years of<br>Pharma Excellence</h2>
  <div class="exp-grid">
    <div class="exp-left fade-up">
      <p>From frontline sales at Tablet India to national brands at Cipla, and now leading derma-cosmetic growth at Akumentis — a journey built on discipline, trust, and results.</p>
    </div>
    <div class="exp-timeline">
      <div class="exp-item fade-up delay-1">
        <div class="exp-period">Present<br>Current</div>
        <div>
          <div class="exp-company">Akumentis Healthcare</div>
          <div class="exp-role">Sales & Marketing Leader · Derma Cosmetic</div>
          <p class="exp-desc">Leading sales initiatives in the fast-growing dermatology and cosmeceutical segment. Building strong HCP relationships, territory expansion, and team excellence in a specialty-focused environment.</p>
          <span class="exp-tag">Derma · Cosmetic · Specialty</span>
        </div>
      </div>
      <div class="exp-item fade-up delay-2">
        <div class="exp-period">17 Years<br>Cipla Era</div>
        <div>
          <div class="exp-company">Cipla Ltd.</div>
          <div class="exp-role">Senior Sales Professional · Pharma</div>
          <p class="exp-desc">A landmark 17-year tenure at one of India's most respected pharmaceutical companies. Built deep institutional knowledge, long-standing customer relationships, and a reputation for consistent performance and team management.</p>
          <span class="exp-tag">Cipla · 17 Years · Multi-Therapy</span>
        </div>
      </div>
      <div class="exp-item fade-up delay-3">
        <div class="exp-period">2 Years<br>Foundation</div>
        <div>
          <div class="exp-company">Tablet India</div>
          <div class="exp-role">Sales Representative · Pharma</div>
          <p class="exp-desc">The formative years — learning the fundamentals of pharmaceutical sales, customer engagement, and territory management. The bedrock upon which an 18-year career was built.</p>
          <span class="exp-tag">Foundation · Sales · Field</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PHILOSOPHY -->
<section id="philosophy">
  <div class="section-eyebrow">Core Values</div>
  <h2 class="section-title fade-up">The Principles<br>I Work By</h2>
  <div class="phil-grid">
    <div class="phil-card fade-up delay-1">
      <span class="phil-icon">📐</span>
      <div class="phil-heading">Discipline Above All</div>
      <p class="phil-text">Discipline is the invisible architecture of every result. It means showing up consistently, keeping commitments, and maintaining standards — even when it's inconvenient.</p>
    </div>
    <div class="phil-card fade-up delay-2">
      <span class="phil-icon">🚀</span>
      <div class="phil-heading">Workaholic by Nature</div>
      <p class="phil-text">Hard work isn't a burden — it's a privilege. The willingness to put in the hours, go the extra mile, and outwork the competition has been a defining trait across every role.</p>
    </div>
    <div class="phil-card fade-up delay-3">
      <span class="phil-icon">😄</span>
      <div class="phil-heading">Light at Heart</div>
      <p class="phil-text">A positive, warm energy in the team is not a luxury — it's a strategy. Keeping the atmosphere light, encouraging laughter, and bringing humanity to the workplace drives genuine performance.</p>
    </div>
    <div class="phil-card fade-up delay-2">
      <span class="phil-icon">🤝</span>
      <div class="phil-heading">No Friction Leadership</div>
      <p class="phil-text">Smooth collaboration between teams, channels, and stakeholders is a competitive advantage. Minimising friction — in processes, communication, and culture — accelerates everything.</p>
    </div>
    <div class="phil-card fade-up delay-3">
      <span class="phil-icon">📚</span>
      <div class="phil-heading">Lifelong Reader</div>
      <p class="phil-text">Books are the mentors that never sleep. A deep love for reading has shaped perspectives on leadership, strategy, and human behaviour — bringing outside wisdom into everyday decisions.</p>
    </div>
    <div class="phil-card fade-up delay-4">
      <span class="phil-icon">🌟</span>
      <div class="phil-heading">Team First, Always</div>
      <p class="phil-text">Strong connect with the team isn't built through hierarchy — it's earned through genuine care, presence, and shared purpose. When the team wins, everyone wins.</p>
    </div>
  </div>
</section>

<!-- EXPERTISE -->
<section id="expertise">
  <div class="section-eyebrow">Skill Landscape</div>
  <h2 class="section-title fade-up">Built Over<br>18 Years of Action</h2>
  <div class="expertise-wrap">
    <div class="skill-list">
      <div class="skill-row fade-up delay-1">
        <div class="skill-header">
          <span class="skill-name">Pharma Sales & Territory Management</span>
          <span class="skill-pct">97%</span>
        </div>
        <div class="skill-bar"><div class="skill-fill" data-width="97"></div></div>
      </div>
      <div class="skill-row fade-up delay-2">
        <div class="skill-header">
          <span class="skill-name">Team Management & People Development</span>
          <span class="skill-pct">95%</span>
        </div>
        <div class="skill-bar"><div class="skill-fill" data-width="95"></div></div>
      </div>
      <div class="skill-row fade-up delay-3">
        <div class="skill-header">
          <span class="skill-name">Derma & Cosmeceutical Marketing</span>
          <span class="skill-pct">90%</span>
        </div>
        <div class="skill-bar"><div class="skill-fill" data-width="90"></div></div>
      </div>
      <div class="skill-row fade-up delay-4">
        <div class="skill-header">
          <span class="skill-name">HCP Relationship Building</span>
          <span class="skill-pct">98%</span>
        </div>
        <div class="skill-bar"><div class="skill-fill" data-width="98"></div></div>
      </div>
      <div class="skill-row fade-up delay-3">
        <div class="skill-header">
          <span class="skill-name">Sales Strategy & Forecasting</span>
          <span class="skill-pct">88%</span>
        </div>
        <div class="skill-bar"><div class="skill-fill" data-width="88"></div></div>
      </div>
      <div class="skill-row fade-up delay-4">
        <div class="skill-header">
          <span class="skill-name">Stakeholder Engagement & KOL Management</span>
          <span class="skill-pct">92%</span>
        </div>
        <div class="skill-bar"><div class="skill-fill" data-width="92"></div></div>
      </div>
    </div>
    <div class="expertise-quote fade-up delay-2">
      <p class="quote-text">"Discipline creates freedom. When your habits are strong, you stop making decisions about effort — you just show up and deliver."</p>
      <div class="quote-attr">— H.C. Prajapati · Personal Belief</div>
    </div>
  </div>
</section>

<!-- LEADERSHIP -->
<section id="leadership">
  <div class="section-eyebrow">Man Management</div>
  <h2 class="section-title">10 Years of<br>Building Leaders</h2>
  <p class="lead-intro fade-up">People management isn't about titles or authority — it's about trust, clarity, and helping people become the best version of themselves. 10+ years of leading teams has shaped a unique leadership DNA.</p>
  <div class="lead-grid">
    <div class="lead-card fade-up delay-1">
      <div class="lead-num">01</div>
      <div class="lead-title">Trust as Currency</div>
      <p class="lead-text">Building credibility with every interaction. A team that trusts their leader performs beyond targets — not out of compulsion, but out of commitment.</p>
    </div>
    <div class="lead-card fade-up delay-2">
      <div class="lead-num">02</div>
      <div class="lead-title">Strong Team Connect</div>
      <p class="lead-text">Regular touchpoints, genuine conversations, and understanding each person's motivation. A connected team is a resilient team that weathers any market headwind.</p>
    </div>
    <div class="lead-card fade-up delay-3">
      <div class="lead-num">03</div>
      <div class="lead-title">No Friction Culture</div>
      <p class="lead-text">Removing barriers to execution. When team members can focus on their work without navigating unnecessary conflict or process drag, performance soars naturally.</p>
    </div>
    <div class="lead-card fade-up delay-4">
      <div class="lead-num">04</div>
      <div class="lead-title">Coaching Over Commanding</div>
      <p class="lead-text">10 years of people management have proven one truth: you grow faster by growing others. The best managers are teachers, coaches, and cheerleaders rolled into one.</p>
    </div>
  </div>
</section>

<!-- INTERESTS -->
<section id="interests">
  <div class="section-eyebrow">Beyond Work</div>
  <h2 class="section-title fade-up">What Fuels<br>the Drive</h2>
  <div class="interests-row">
    <div class="interest-item fade-up delay-1">
      <span class="interest-icon">📖</span>
      <div class="interest-name">Avid Reader</div>
      <p class="interest-sub">Books on leadership, sales psychology, human behaviour, and self-improvement. Reading is the quiet discipline behind the public results.</p>
    </div>
    <div class="interest-item fade-up delay-2">
      <span class="interest-icon">🏃</span>
      <div class="interest-name">Workaholic Spirit</div>
      <p class="interest-sub">Finds energy in the work itself. Driven by purpose, not just targets — turning professional passion into consistent daily action.</p>
    </div>
    <div class="interest-item fade-up delay-3">
      <span class="interest-icon">😊</span>
      <div class="interest-name">People Person</div>
      <p class="interest-sub">A natural connector — warm, approachable, and genuine. Believes that real relationships are the greatest asset in any profession.</p>
    </div>
    <div class="interest-item fade-up delay-4">
      <span class="interest-icon">🌿</span>
      <div class="interest-name">Derma Enthusiast</div>
      <p class="interest-sub">Deeply passionate about the science of skin health and the art of cosmeceutical marketing — a segment that blends medicine with lifestyle.</p>
    </div>
  </div>
</section>

<!-- CONNECT -->
<section id="connect">
  <div class="connect-inner">
    <div class="section-eyebrow">Let's Connect</div>
    <h2 class="section-title">Open to Conversations<br>That Matter</h2>
    <p class="connect-sub">Whether it's about pharma sales strategy, team leadership, or the derma-cosmetic industry — reach out and let's have a meaningful conversation.</p>
    <div class="connect-links">
      <a href="mailto:harishchandra.prajapati@email.com" class="connect-link primary">
        ✉ Send an Email
      </a>
      <a href="https://linkedin.com/in/harishchandra-prajapati" class="connect-link secondary" target="_blank">
        in LinkedIn Profile
      </a>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <span class="footer-name">Harishchandra Prajapati</span>
  <span class="footer-note">Pharma Sales & Marketing · India · © 2025</span>
</footer>

<script>
  // Intersection Observer for fade-up animations
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
        // Animate skill bars
        const fill = e.target.querySelector('.skill-fill');
        if (fill) {
          fill.style.width = fill.dataset.width + '%';
        }
      }
    });
  }, { threshold: 0.15 });

  document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));

  // Also observe skill bars separately
  document.querySelectorAll('.skill-fill').forEach(el => {
    const rowObserver = new IntersectionObserver((entries) => {
      entries.forEach(e => {
        if (e.isIntersecting) {
          e.target.style.width = e.target.dataset.width + '%';
        }
      });
    }, { threshold: 0.5 });
    rowObserver.observe(el);
  });

  // Smooth active nav link highlighting
  const sections = document.querySelectorAll('section[id]');
  const navLinks = document.querySelectorAll('.nav-links a');

  window.addEventListener('scroll', () => {
    let current = '';
    sections.forEach(s => {
      if (window.scrollY >= s.offsetTop - 120) current = s.id;
    });
    navLinks.forEach(a => {
      a.style.color = a.getAttribute('href') === '#' + current ? 'var(--gold)' : '';
    });
  });
</script>
</body>
</html>

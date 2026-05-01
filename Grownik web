fullText:
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Shreyansh Srivastava | Sr. IT Recruiter</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght=0,400;0,700;0,900;1,400&family=DM+Mono:ital,wght=0,300;0,400;1,300&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --bg: #0d0d0d;
      --bg2: #141414;
      --bg3: #1c1c1c;
      --gold: #c9a84c;
      --gold-light: #e2c07a;
      --gold-dim: #7a6330;
      --white: #f0ebe0;
      --grey: #6b6b6b;
      --grey-light: #9a9a9a;
      --border: rgba(201,168,76,0.18);
      --font-display: 'Playfair Display', serif;
      --font-mono: 'DM Mono', monospace;
      --font-body: 'DM Sans', sans-serif;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    html { scroll-behavior: smooth; }

    body {
      background: var(--bg);
      color: var(--white);
      font-family: var(--font-body);
      font-weight: 300;
      overflow-x: hidden;
      cursor: default;
    }

    /* Grain overlay */
    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 512 512' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
      pointer-events: none;
      z-index: 9999;
      opacity: 0.35;
    }

    /* ── NAV ── */
    nav {
      position: fixed;
      top: 0; left: 0; right: 0;
      z-index: 100;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1.4rem 4rem;
      background: linear-gradient(to bottom, rgba(13,13,13,0.95), transparent);
      backdrop-filter: blur(2px);
    }
    .nav-logo {
      font-family: var(--font-display);
      font-size: 1.1rem;
      font-style: italic;
      color: var(--gold);
      letter-spacing: 0.02em;
    }
    .nav-links {
      display: flex;
      gap: 2.5rem;
      list-style: none;
    }
    .nav-links a {
      font-family: var(--font-mono);
      font-size: 0.72rem;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--grey-light);
      text-decoration: none;
      transition: color 0.3s;
    }
    .nav-links a:hover { color: var(--gold); }

    /* ── HERO ── */
    #hero {
      min-height: 100vh;
      display: grid;
      grid-template-columns: 1fr 1fr;
      align-items: center;
      padding: 8rem 4rem 4rem;
      position: relative;
      overflow: hidden;
    }

    .hero-bg-text {
      position: absolute;
      bottom: -2rem;
      right: -1rem;
      font-family: var(--font-display);
      font-size: clamp(6rem, 15vw, 18rem);
      font-weight: 900;
      color: rgba(201,168,76,0.04);
      line-height: 1;
      pointer-events: none;
      user-select: none;
      white-space: nowrap;
    }

    .hero-left { position: relative; z-index: 1; }

    .hero-tag {
      display: inline-flex;
      align-items: center;
      gap: 0.6rem;
      font-family: var(--font-mono);
      font-size: 0.7rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 1.8rem;
      opacity: 0;
      animation: fadeUp 0.8s ease 0.2s forwards;
    }
    .hero-tag::before {
      content: '';
      width: 2rem;
      height: 1px;
      background: var(--gold);
    }

    .hero-name {
      font-family: var(--font-display);
      font-size: clamp(2.8rem, 6vw, 5.5rem);
      font-weight: 900;
      line-height: 1.05;
      letter-spacing: -0.01em;
      margin-bottom: 1.2rem;
      opacity: 0;
      animation: fadeUp 0.8s ease 0.4s forwards;
    }
    .hero-name em {
      font-style: italic;
      color: var(--gold);
    }

    .hero-title {
      font-family: var(--font-mono);
      font-size: 0.85rem;
      color: var(--grey-light);
      letter-spacing: 0.08em;
      margin-bottom: 2rem;
      opacity: 0;
      animation: fadeUp 0.8s ease 0.55s forwards;
    }

    .typewriter-container {
      font-family: var(--font-mono);
      font-size: 0.9rem;
      color: var(--grey-light);
      margin-bottom: 3rem;
      min-height: 1.4em;
      opacity: 0;
      animation: fadeUp 0.8s ease 0.7s forwards;
    }
    #typewriter-text { color: var(--gold-light); }
    .cursor {
      display: inline-block;
      width: 2px;
      height: 1em;
      background: var(--gold);
      margin-left: 2px;
      vertical-align: middle;
      animation: blink 1s step-end infinite;
    }
    @keyframes blink { 50% { opacity: 0; } }

    .hero-ctas {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
      opacity: 0;
      animation: fadeUp 0.8s ease 0.85s forwards;
    }
    .btn-primary {
      padding: 0.85rem 2rem;
      background: var(--gold);
      color: #0d0d0d;
      font-family: var(--font-mono);
      font-size: 0.72rem;
      font-weight: 400;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      text-decoration: none;
      border: none;
      cursor: pointer;
      transition: background 0.3s, transform 0.2s;
    }
    .btn-primary:hover { background: var(--gold-light); transform: translateY(-2px); }
    .btn-secondary {
      padding: 0.85rem 2rem;
      background: transparent;
      color: var(--gold);
      font-family: var(--font-mono);
      font-size: 0.72rem;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      text-decoration: none;
      border: 1px solid var(--border);
      cursor: pointer;
      transition: border-color 0.3s, color 0.3s, transform 0.2s;
    }
    .btn-secondary:hover { border-color: var(--gold); color: var(--gold-light); transform: translateY(-2px); }

    .hero-right {
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      gap: 1.5rem;
      position: relative;
      z-index: 1;
      opacity: 0;
      animation: fadeIn 1s ease 1s forwards;
    }

    .stat-card {
      background: var(--bg2);
      border: 1px solid var(--border);
      padding: 1.5rem 2rem;
      width: 16rem;
      position: relative;
      overflow: hidden;
    }
    .stat-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0;
      width: 3px;
      height: 100%;
      background: var(--gold);
    }
    .stat-number {
      font-family: var(--font-display);
      font-size: 2.8rem;
      font-weight: 700;
      color: var(--gold);
      line-height: 1;
    }
    .stat-label {
      font-family: var(--font-mono);
      font-size: 0.65rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--grey);
      margin-top: 0.3rem;
    }

    /* ── SECTION COMMON ── */
    section {
      padding: 6rem 4rem;
    }
    .section-header {
      display: flex;
      align-items: center;
      gap: 1.5rem;
      margin-bottom: 4rem;
    }
    .section-num {
      font-family: var(--font-mono);
      font-size: 0.65rem;
      color: var(--gold-dim);
      letter-spacing: 0.2em;
    }
    .section-title {
      font-family: var(--font-display);
      font-size: clamp(2rem, 4vw, 3.2rem);
      font-weight: 700;
      line-height: 1;
    }
    .section-line {
      flex: 1;
      height: 1px;
      background: var(--border);
    }

    /* ── ABOUT ── */
    #about { background: var(--bg2); }
    .about-grid {
      display: grid;
      grid-template-columns: 2fr 1fr 1fr;
      gap: 5rem;
      align-items: start;
    }
    .about-bio {
      font-size: 1.05rem;
      line-height: 1.8;
      color: var(--grey-light);
    }
    .about-bio strong { color: var(--white); font-weight: 500; }
    .about-bio p + p { margin-top: 1.2rem; }

    /* NEW IMAGE STYLES */
    .about-image-container {
      background: var(--bg3);
      border: 1px solid var(--border);
      padding: 1.5rem;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
    }
    .about-image-container img {
      max-width: 100%;
      height: auto;
      object-fit: cover;
    }

    .about-details { display: flex; flex-direction: column; gap: 1rem; }
    .detail-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 0;
      border-bottom: 1px solid var(--border);
    }
    .detail-key {
      font-family: var(--font-mono);
      font-size: 0.65rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: var(--grey);
    }
    .detail-val {
      font-size: 0.9rem;
      color: var(--white);
      text-align: right;
    }
    .badge {
      display: inline-block;
      padding: 0.25rem 0.7rem;
      background: rgba(201,168,76,0.12);
      border: 1px solid var(--border);
      color: var(--gold);
      font-family: var(--font-mono);
      font-size: 0.62rem;
      letter-spacing: 0.15em;
      text-transform: uppercase;
    }

    /* ── EXPERIENCE ── */
    #experience { background: var(--bg); }
    .exp-timeline { position: relative; padding-left: 2rem; }
    .exp-timeline::before {
      content: '';
      position: absolute;
      left: 0; top: 0; bottom: 0;
      width: 1px;
      background: var(--border);
    }
    .exp-item {
      position: relative;
      padding: 0 0 3.5rem 2.5rem;
      opacity: 0;
      transform: translateX(-20px);
      transition: opacity 0.6s ease, transform 0.6s ease;
    }
    .exp-item.visible { opacity: 1; transform: translateX(0); }
    .exp-item::before {
      content: '';
      position: absolute;
      left: -4.5px; top: 0.4rem;
      width: 9px; height: 9px;
      background: var(--gold);
      border-radius: 50%;
      box-shadow: 0 0 10px rgba(201,168,76,0.5);
    }
    .exp-period {
      font-family: var(--font-mono);
      font-size: 0.65rem;
      letter-spacing: 0.18em;
      color: var(--gold-dim);
      text-transform: uppercase;
      margin-bottom: 0.5rem;
    }
    .exp-role {
      font-family: var(--font-display);
      font-size: 1.5rem;
      font-weight: 700;
      margin-bottom: 0.2rem;
    }
    .exp-company {
      font-family: var(--font-mono);
      font-size: 0.8rem;
      color: var(--gold);
      letter-spacing: 0.1em;
      margin-bottom: 1rem;
    }
    .exp-desc {
      font-size: 0.9rem;
      line-height: 1.7;
      color: var(--grey-light);
      max-width: 60rem;
    }
    .exp-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-top: 1rem;
    }
    .exp-tag {
      font-family: var(--font-mono);
      font-size: 0.6rem;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      padding: 0.25rem 0.65rem;
      border: 1px solid var(--border);
      color: var(--grey);
    }

    /* ── SKILLS ── */
    #skills { background: var(--bg2); }
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1.5rem;
    }
    .skill-block {
      background: var(--bg3);
      border: 1px solid var(--border);
      padding: 2rem;
      position: relative;
      overflow: hidden;
      transition: border-color 0.3s;
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 0.5s, transform 0.5s, border-color 0.3s;
    }
    .skill-block.visible { opacity: 1; transform: translateY(0); }
    .skill-block:hover { border-color: rgba(201,168,76,0.4); }
    .skill-block-icon {
      font-size: 1.5rem;
      margin-bottom: 1rem;
    }
    .skill-block-title {
      font-family: var(--font-display);
      font-size: 1.1rem;
      font-weight: 700;
      margin-bottom: 0.8rem;
    }
    .skill-list {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 0.4rem;
    }
    .skill-list li {
      font-family: var(--font-mono);
      font-size: 0.72rem;
      letter-spacing: 0.08em;
      color: var(--grey-light);
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }
    .skill-list li::before {
      content: '▸';
      color: var(--gold);
      font-size: 0.6rem;
    }

    /* ── MARKETS ── */
    #markets { background: var(--bg); }
    .markets-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 1.5rem;
    }
    .market-card {
      border: 1px solid var(--border);
      padding: 2.5rem 1.5rem;
      text-align: center;
      position: relative;
      overflow: hidden;
      cursor: default;
      transition: background 0.4s;
      opacity: 0;
      transform: scale(0.95);
      transition: opacity 0.5s, transform 0.5s, background 0.4s;
    }
    .market-card.visible { opacity: 1; transform: scale(1); }
    .market-card:hover { background: rgba(201,168,76,0.05); }
    .market-flag { font-size: 2.5rem; margin-bottom: 0.8rem; }
    .market-name {
      font-family: var(--font-display);
      font-size: 1.3rem;
      font-weight: 700;
      margin-bottom: 0.3rem;
    }
    .market-sub {
      font-family: var(--font-mono);
      font-size: 0.65rem;
      letter-spacing: 0.15em;
      text-transform: uppercase;
      color: var(--gold-dim);
    }

    /* ── CONTACT ── */
    #contact {
      background: var(--bg2);
      text-align: center;
    }
    .contact-inner {
      max-width: 50rem;
      margin: 0 auto;
    }
    .contact-heading {
      font-family: var(--font-display);
      font-size: clamp(2.5rem, 5vw, 4.5rem);
      font-weight: 900;
      line-height: 1.1;
      margin-bottom: 1.5rem;
    }
    .contact-heading em { font-style: italic; color: var(--gold); }
    .contact-sub {
      font-size: 1rem;
      line-height: 1.7;
      color: var(--grey-light);
      margin-bottom: 3rem;
    }
    .contact-links {
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      flex-wrap: wrap;
      margin-bottom: 3rem;
    }
    .contact-link {
      display: flex;
      align-items: center;
      gap: 0.6rem;
      font-family: var(--font-mono);
      font-size: 0.75rem;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--grey-light);
      text-decoration: none;
      padding: 0.8rem 1.5rem;
      border: 1px solid var(--border);
      transition: color 0.3s, border-color 0.3s;
    }
    .contact-link:hover { color: var(--gold); border-color: var(--gold); }
    .contact-email {
      font-family: var(--font-display);
      font-size: 1.2rem;
      font-style: italic;
      color: var(--gold);
    }

    /* ── FOOTER ── */
    footer {
      padding: 2rem 4rem;
      border-top: 1px solid var(--border);
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: var(--bg);
    }
    footer p {
      font-family: var(--font-mono);
      font-size: 0.65rem;
      letter-spacing: 0.15em;
      color: var(--grey);
    }

    /* ── SCROLL REVEAL ── */
    .reveal {
      opacity: 0;
      transform: translateY(30px);
      transition: opacity 0.7s ease, transform 0.7s ease;
    }
    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* ── ANIMATIONS ── */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(25px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    /* ── RESPONSIVE ── */
    @media (max-width: 900px) {
      nav { padding: 1.2rem 2rem; }
      #hero { grid-template-columns: 1fr; padding: 7rem 2rem 4rem; }
      .hero-right { align-items: flex-start; flex-direction: row; flex-wrap: wrap; }
      .stat-card { width: auto; flex: 1; min-width: 10rem; }
      section { padding: 4rem 2rem; }
      .about-grid { grid-template-columns: 1fr; gap: 3rem; }
      .skills-grid { grid-template-columns: 1fr 1fr; }
      .markets-grid { grid-template-columns: 1fr 1fr; }
      footer { flex-direction: column; gap: 1rem; text-align: center; }
    }
    @media (max-width: 560px) {
      .skills-grid { grid-template-columns: 1fr; }
      .markets-grid { grid-template-columns: 1fr 1fr; }
      .nav-links { display: none; }
    }
  </style>
</head>
<body>

  <nav>
    <div class="nav-logo">S. Srivastava</div>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#markets">Markets</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <section id="hero">
    <div class="hero-bg-text">Recruit</div>
    <div class="hero-left">
      <div class="hero-tag">Sr. IT Recruiter · Workday Certified</div>
      <h1 class="hero-name">
        Shreyansh<br><em>Srivastava</em>
      </h1>
      <p class="hero-title">// Full-Cycle Technical Recruitment · Global Markets</p>
      <div class="typewriter-container">
        &gt; <span id="typewriter-text"></span><span class="cursor"></span>
      </div>
      <div class="hero-ctas">
        <a href="#contact" class="btn-primary">Get in Touch</a>
        <a href="#experience" class="btn-secondary">View Experience</a>
      </div>
    </div>
    <div class="hero-right">
      <div class="stat-card">
        <div class="stat-number">4+</div>
        <div class="stat-label">Years of Experience</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">F500</div>
        <div class="stat-label">Client Portfolio</div>
      </div>
      <div class="stat-card">
        <div class="stat-number">4</div>
        <div class="stat-label">Global Markets</div>
      </div>
    </div>
  </section>

  <section id="about">
    <div class="section-header reveal">
      <span class="section-num">01</span>
      <h2 class="section-title">About</h2>
      <div class="section-line"></div>
    </div>
    <div class="about-grid">
      <div class="about-bio reveal">
        <p>
          Results-driven <strong>Senior Technical Recruiter</strong> with 4+ years of specialized experience in IT talent acquisition across <strong>global markets</strong> — UK, EU, US, and India.
        </p>
        <p>
          Proven track record delivering high-quality candidates for <strong>Fortune 500 clients</strong> in Investment Banking, Wealth Management, and Commercial Banking sectors. Expert in full-cycle recruitment, ATS/VMS platforms, and strategic sourcing methodologies.
        </p>
        <p>
          <strong>Workday Certified</strong> with demonstrated success in building high-performing technical teams and maintaining exceptional client satisfaction rates. My approach blends sharp technical intuition with a deep understanding of people — matching not just skills, but potential.
        </p>
      </div>

      <div class="about-image-container reveal" style="transition-delay: 0.1s;">
        <img src="image_0.png" alt="Shreyansh Srivastava | Professional Headshot">
      </div>

      <div class="about-details reveal">
        <div class="detail-row">
          <span class="detail-key">Location</span>
          <span class="detail-val">Noida, UP, India</span>
        </div>
        <div class="detail-row">
          <span class="detail-key">Current Role</span>
          <span class="detail-val">Sr. IT Recruiter @ iXceed Solutions</span>
        </div>
        <div class="detail-row">
          <span class="detail-key">Email</span>
          <span class="detail-val">Shreyanshcareer41@gmail.com</span>
        </div>
        <div class="detail-row">
          <span class="detail-key">Phone</span>
          <span class="detail-val">+91 7007997580</span>
        </div>
        <div class="detail-row">
          <span class="detail-key">Certification</span>
          <span class="detail-val"><span class="badge">Workday Certified</span></span>
        </div>
        <div class="detail-row">
          <span class="detail-key">Education</span>
          <span class="detail-val">BSc, PRSU Prayagraj</span>
        

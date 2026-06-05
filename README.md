      font-family: 'DM Sans', sans-serif;
      background: var(--bg);
      color: var(--text);
      min-height: 100vh;
      overflow-x: hidden;
    }

    /* ── BACKGROUND GRID ── */
    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background-image:
        linear-gradient(rgba(0,229,255,0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(0,229,255,0.03) 1px, transparent 1px);
      background-size: 40px 40px;
      pointer-events: none;
      z-index: 0;
    }

    /* ── NAVBAR ── */
    nav {
      position: fixed;
      top: 0; left: 0; right: 0;
      z-index: 100;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 18px 48px;
      background: rgba(10,10,15,0.85);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--border);
    }
    .nav-logo {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 1.5rem;
      letter-spacing: 3px;
      color: var(--accent);
    }
    .nav-links { display: flex; gap: 32px; list-style: none; }
    .nav-links a {
      font-size: 0.8rem;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: var(--muted);
      text-decoration: none;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--accent); }

    /* ── HERO ── */
    .hero {
      position: relative;
      z-index: 1;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding: 120px 48px 80px;
      max-width: 1100px;
      margin: 0 auto;
    }
    .hero-eyebrow {
      font-family: 'JetBrains Mono', monospace;
      font-size: 0.75rem;
      color: var(--accent);
      letter-spacing: 4px;
      text-transform: uppercase;
      margin-bottom: 24px;
      opacity: 0;
      animation: fadeUp 0.6s 0.2s forwards;
    }
    .hero-name {
      font-family: 'Bebas Neue', sans-serif;
      font-size: clamp(4rem, 12vw, 9rem);
      line-height: 0.92;
      letter-spacing: 2px;
      opacity: 0;
      animation: fadeUp 0.7s 0.4s forwards;
    }
    .hero-name span {
      -webkit-text-stroke: 1px var(--accent);
      color: transparent;
    }
    .hero-tagline {
      margin-top: 32px;
      font-size: 1.1rem;
      color: var(--muted);
      font-weight: 300;
      max-width: 480px;
      line-height: 1.7;
      opacity: 0;
      animation: fadeUp 0.7s 0.6s forwards;
    }
    .hero-cta {
      margin-top: 48px;
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
      opacity: 0;
      animation: fadeUp 0.7s 0.8s forwards;
    }
    .btn {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 14px 28px;
      font-size: 0.8rem;
      letter-spacing: 2px;
      text-transform: uppercase;
      text-decoration: none;
      border-radius: 3px;
      font-family: 'JetBrains Mono', monospace;
      transition: all 0.25s;
    }
    .btn-primary {
      background: var(--accent);
      color: var(--bg);
      font-weight: 600;
    }
    .btn-primary:hover { background: #fff; box-shadow: 0 0 30px rgba(0,229,255,0.4); }
    .btn-outline {
      border: 1px solid var(--border);
      color: var(--muted);
    }
    .btn-outline:hover { border-color: var(--accent); color: var(--accent); }

    /* ── SCROLL INDICATOR ── */
    .scroll-line {
      position: absolute;
      bottom: 40px;
      left: 48px;
      display: flex;
      align-items: center;
      gap: 12px;
      font-family: 'JetBrains Mono', monospace;
      font-size: 0.65rem;
      letter-spacing: 3px;
      color: var(--muted);
      text-transform: uppercase;
      opacity: 0;
      animation: fadeUp 0.7s 1.2s forwards;
    }
    .scroll-line::before {
      content: '';
      display: block;
      width: 40px;
      height: 1px;
      background: var(--accent);
      animation: lineGrow 1s 1.5s both;
    }

    /* ── SECTION COMMON ── */
    section {
      position: relative;
      z-index: 1;
      max-width: 1100px;
      margin: 0 auto;
      padding: 100px 48px;
    }
    .section-label {
      font-family: 'JetBrains Mono', monospace;
      font-size: 0.7rem;
      letter-spacing: 4px;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 16px;
    }
    .section-title {
      font-family: 'Bebas Neue', sans-serif;
      font-size: clamp(2.5rem, 6vw, 4.5rem);
      line-height: 1;
      margin-bottom: 56px;
    }
    .divider {
      width: 100%;
      height: 1px;
      background: var(--border);
      margin: 0;
    }

    /* ── ABOUT ── */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 64px;
      align-items: start;
    }
    .about-text p {
      color: var(--muted);
      line-height: 1.85;
      font-size: 1.05rem;
      margin-bottom: 16px;
    }
    .about-text p strong { color: var(--text); }
    .info-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 32px;
    }
    .info-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 14px 0;
      border-bottom: 1px solid var(--border);
      font-size: 0.9rem;
    }
    .info-row:last-child { border-bottom: none; }
    .info-row .label { color: var(--muted); font-size: 0.75rem; letter-spacing: 1.5px; text-transform: uppercase; }
    .info-row .value { color: var(--text); font-family: 'JetBrains Mono', monospace; font-size: 0.8rem; }

    /* ── SKILLS ── */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 20px;
    }
    .skill-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 28px;
      position: relative;
      overflow: hidden;
      transition: border-color 0.25s, transform 0.25s;
    }
    .skill-card:hover {
      border-color: var(--accent);
      transform: translateY(-4px);
    }
    .skill-card::after {
      content: '';
      position: absolute;
      top: 0; left: 0;
      width: 3px; height: 100%;
      background: var(--accent);
      transform: scaleY(0);
      transform-origin: bottom;
      transition: transform 0.3s;
    }
    .skill-card:hover::after { transform: scaleY(1); }
    .skill-icon { font-size: 1.8rem; margin-bottom: 16px; }
    .skill-name {
      font-size: 0.85rem;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: var(--text);
      font-weight: 500;
      margin-bottom: 8px;
    }
    .skill-desc { font-size: 0.85rem; color: var(--muted); line-height: 1.6; }
    .skill-tag {
      display: inline-block;
      margin-top: 14px;
      padding: 4px 10px;
      background: rgba(0,229,255,0.08);
      border: 1px solid rgba(0,229,255,0.2);
      border-radius: 20px;
      font-size: 0.7rem;
      color: var(--accent);
      font-family: 'JetBrains Mono', monospace;
    }

    /* ── EDUCATION ── */
    .timeline { position: relative; padding-left: 32px; }
    .timeline::before {
      content: '';
      position: absolute;
      left: 0; top: 8px; bottom: 8px;
      width: 1px;
      background: var(--border);
    }
    .timeline-item {
      position: relative;
      margin-bottom: 48px;
      padding-left: 28px;
    }
    .timeline-item::before {
      content: '';
      position: absolute;
      left: -36px; top: 6px;
      width: 10px; height: 10px;
      border-radius: 50%;
      background: var(--accent);
      box-shadow: 0 0 12px var(--accent);
    }
    .timeline-year {
      font-family: 'JetBrains Mono', monospace;
      font-size: 0.7rem;
      color: var(--accent);
      letter-spacing: 3px;
      text-transform: uppercase;
      margin-bottom: 8px;
    }
    .timeline-degree {
      font-size: 1.15rem;
      font-weight: 500;
      margin-bottom: 4px;
    }
    .timeline-school {
      font-size: 0.9rem;
      color: var(--muted);
    }

    /* ── PROJECTS ── */
    .project-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 40px;
      margin-bottom: 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 32px;
      transition: border-color 0.25s, transform 0.2s;
    }
    .project-card:hover { border-color: var(--accent2); transform: translateX(6px); }
    .project-num {
      font-family: 'Bebas Neue', sans-serif;
      font-size: 3.5rem;
      color: var(--border);
      min-width: 70px;
    }
    .project-info { flex: 1; }
    .project-title { font-size: 1.2rem; font-weight: 500; margin-bottom: 8px; }
    .project-desc { font-size: 0.9rem; color: var(--muted); line-height: 1.6; }
    .project-tags { display: flex; gap: 8px; margin-top: 14px; flex-wrap: wrap; }
    .project-tag {
      padding: 4px 12px;
      background: rgba(255,77,109,0.08);
      border: 1px solid rgba(255,77,109,0.2);
      border-radius: 20px;
      font-size: 0.7rem;
      color: var(--accent2);
      font-family: 'JetBrains Mono', monospace;
    }
    .project-arrow { font-size: 1.5rem; color: var(--muted); transition: color 0.2s; }
    .project-card:hover .project-arrow { color: var(--accent2); }

    /* ── CONTACT ── */
    .contact-wrap {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 64px;
      align-items: start;
    }
    .contact-blurb {
      font-size: 1.05rem;
      color: var(--muted);
      line-height: 1.85;
    }
    .contact-links { display: flex; flex-direction: column; gap: 16px; }
    .contact-link {
      display: flex;
      align-items: center;
      gap: 16px;
      padding: 20px 24px;
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 8px;
      text-decoration: none;
      color: var(--text);
      transition: border-color 0.25s, transform 0.2s;
    }
    .contact-link:hover { border-color: var(--accent); transform: translateX(6px); }
    .contact-link-icon { font-size: 1.2rem; }
    .contact-link-label { font-size: 0.7rem; color: var(--muted); letter-spacing: 2px; text-transform: uppercase; font-family: 'JetBrains Mono', monospace; }
    .contact-link-val { font-size: 0.9rem; margin-top: 2px; }

    /* ── FOOTER ── */
    footer {
      position: relative;
      z-index: 1;
      text-align: center;
      padding: 32px;
      border-top: 1px solid var(--border);
      font-family: 'JetBrains Mono', monospace;
      font-size: 0.7rem;
      color: var(--muted);
      letter-spacing: 2px;
    }
    footer span { color: var(--accent); }

    /* ── ANIMATIONS ── */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(24px); }
      to   { opacity: 1; transform: translateY(0); }
    }
    @keyframes lineGrow {
      from { transform: scaleX(0); transform-origin: left; }
      to   { transform: scaleX(1); transform-origin: left; }
    }

    /* ── RESPONSIVE ── */
    @media (max-width: 768px) {
      nav { padding: 16px 20px; }
      .nav-links { display: none; }
      section { padding: 80px 20px; }
      .hero { padding: 100px 20px 60px; }
      .about-grid, .contact-wrap { grid-template-columns: 1fr; gap: 40px; }
      .project-card { flex-direction: column; align-items: flex-start; }
    }
  </style>
</head>
<body>

  <!-- NAV -->
  <nav>
    <div class="nav-logo">MK</div>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#education">Education</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <div class="hero">
    <p class="hero-eyebrow">// Web Developer & CSE Student</p>
    <h1 class="hero-name">MANIRAJ<br/><span>KUMAR</span></h1>
    <p class="hero-tagline">
      Building real-world web experiences from Bihar.<br/>
      Currently pursuing Diploma in Computer Science Engineering at Govt. Polytechnic Khagaria.
    </p>
    <div class="hero-cta">
      <a href="#projects" class="btn btn-primary">View Projects →</a>
      <a href="#contact" class="btn btn-outline">Get in Touch</a>
    </div>
    <div class="scroll-line">Scroll to explore</div>
  </div>

  <div class="divider"></div>

  <!-- ABOUT -->
  <section id="about">
    <p class="section-label">// 01 — About Me</p>
    <h2 class="section-title">Who I Am</h2>
    <div class="about-grid">
      <div class="about-text">
        <p>I'm <strong>Maniraj Kumar</strong>, a passionate CSE diploma student with a love for building things on the web. I'm currently doing a <strong>Web Development Internship</strong>, where I work on real-world projects and grow my skills every day.</p>
        <p>My journey started with learning the foundations — HTML, CSS, and JavaScript — and I've been expanding my knowledge to include deployment, version control, and modern web tools.</p>
        <p>I believe in learning by doing, and every project I take on teaches me something new. I'm based in Bihar and proud to represent the next generation of tech talent from this region.</p>
      </div>
      <div class="info-card">
        <div class="info-row">
          <span class="label">Name</span>
          <span class="value">Maniraj Kumar</span>
        </div>
        <div class="info-row">
          <span class="label">Role</span>
          <span class="value">Diploma Student</span>
        </div>
        <div class="info-row">
          <span class="label">Internship</span>
          <span class="value">Web Development</span>
        </div>
        <div class="info-row">
          <span class="label">Location</span>
          <span class="value">Khagaria, Bihar</span>
        </div>
        <div class="info-row">
          <span class="label">Email</span>
          <span class="value">kmaniraj678@gmail.com</span>
        </div>
        <div class="info-row">
          <span class="label">Status</span>
          <span class="value" style="color:var(--accent)">● Available</span>
        </div>
      </div>
    </div>
  </section>

  <div class="divider"></div>

  <!-- SKILLS -->
  <section id="skills">
    <p class="section-label">// 02 — Skills</p>
    <h2 class="section-title">Competencies</h2>
    <div class="skills-grid">
      <div class="skill-card">
        <div class="skill-icon">🌐</div>
        <div class="skill-name">Web Development</div>
        <div class="skill-desc">Building structured, semantic web pages with proper layout and styling.</div>
        <span class="skill-tag">HTML · CSS</span>
      </div>
      <div class="skill-card">
        <div class="skill-icon">⚡</div>
        <div class="skill-name">JavaScript</div>
        <div class="skill-desc">Adding interactivity and dynamic behaviour to web interfaces.</div>
        <span class="skill-tag">JavaScript</span>
      </div>
      <div class="skill-card">
        <div class="skill-icon">💻</div>
        <div class="skill-name">Programming</div>
        <div class="skill-desc">Understanding core programming logic, loops, functions, and memory.</div>
        <span class="skill-tag">C Language</span>
      </div>
      <div class="skill-card">
        <div class="skill-icon">🚀</div>
        <div class="skill-name">Web Deployment</div>
        <div class="skill-desc">Hosting and publishing websites using modern free deployment platforms.</div>
        <span class="skill-tag">Netlify · GitHub Pages</span>
      </div>
      <div class="skill-card">
        <div class="skill-icon">🖥️</div>
        <div class="skill-name">Operating System</div>
        <div class="skill-desc">Working efficiently on Windows for development and productivity tasks.</div>
        <span class="skill-tag">Windows</span>
      </div>
      <div class="skill-card">
        <div class="skill-icon">📐</div>
        <div class="skill-name">Engineering Math</div>
        <div class="skill-desc">Linear algebra, calculus, eigenvalues, and numerical methods for engineering.</div>
        <span class="skill-tag">Linear Algebra · Calculus</span>
      </div>
    </div>
  </section>

  <div class="divider"></div>

  <!-- EDUCATION -->
  <section id="education">
    <p class="section-label">// 03 — Education</p>
    <h2 class="section-title">Academic Path</h2>
    <div class="timeline">
      <div class="timeline-item">
        <div class="timeline-year">2023 — Pursuing</div>
        <div class="timeline-degree">Diploma in Computer Science & Engineering</div>
        <div class="timeline-school">Government Polytechnic Khagaria, Bihar</div>
      </div>
      <div class="timeline-item">
        <div class="timeline-year">Completed</div>
        <div class="timeline-degree">10th (Secondary Education)</div>
        <div class="timeline-school">Uccha Madhyamik Vidyalaya, Pagara</div>
      </div>
    </div>
  </section>

  <div class="divider"></div>

  <!-- PROJECTS -->
  <section id="projects">
    <p class="section-label">// 04 — Projects</p>
    <h2 class="section-title">Work</h2>

    <div class="project-card">
      <div class="project-num">01</div>
      <div class="project-info">
        <div class="project-title">Personal Portfolio Website</div>
        <div class="project-desc">A fully responsive portfolio website built with pure HTML & CSS to showcase my skills, education, and projects. Deployed live using Netlify.</div>
        <div class="project-tags">
          <span class="project-tag">HTML</span>
          <span class="project-tag">CSS</span>
          <span class="project-tag">Netlify</span>
        </div>
      </div>
      <div class="project-arrow">↗</div>
    </div>

    <div class="project-card">
      <div class="project-num">02</div>
      <div class="project-info">
        <div class="project-title">Web Development Internship Project</div>
        <div class="project-desc">Real-world web project developed during internship — applying front-end skills in a professional environment with live deployment.</div>
        <div class="project-tags">
          <span class="project-tag">HTML</span>
          <span class="project-tag">CSS</span>
          <span class="project-tag">JavaScript</span>
        </div>
      </div>
      <div class="project-arrow">↗</div>
    </div>

    <div class="project-card">
      <div class="project-num">03</div>
      <div class="project-info">
        <div class="project-title">C Programming Projects</div>
        <div class="project-desc">Logic-building programs in C covering loops, arrays, functions, and problem-solving — part of core CSE curriculum.</div>
        <div class="project-tags">
          <span class="project-tag">C Language</span>
          <span class="project-tag">DSA Basics</span>
        </div>
      </div>
      <div class="project-arrow">↗</div>
    </div>
  </section>

  <div class="divider"></div>

  <!-- CONTACT -->
  <section id="contact">
    <p class="section-label">// 05 — Contact</p>
    <h2 class="section-title">Let's Connect</h2>
    <div class="contact-wrap">
      <div class="contact-blurb">
        I'm always open to new opportunities, collaborations, and learning from the community. Feel free to reach out — whether it's about a project, an internship, or just to say hi!
      </div>
      <div class="contact-links">
        <a href="mailto:kmaniraj67

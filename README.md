<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Siddharth Kumar — AI & ML Engineer</title>
  <link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg: #f9f8f5;
      --surface: #ffffff;
      --surface2: #f1f0ec;
      --border: #e2e1db;
      --text: #1a1a18;
      --muted: #6b6a65;
      --hint: #a09f9a;
      --teal-bg: #E1F5EE;
      --teal-text: #0F6E56;
      --teal-border: #9FE1CB;
      --purple-bg: #EEEDFE;
      --purple-text: #3C3489;
      --purple-border: #CECBF6;
      --blue-bg: #E6F1FB;
      --blue-text: #0C447C;
      --blue-border: #B5D4F4;
      --amber-bg: #FAEEDA;
      --amber-text: #633806;
      --amber-border: #FAC775;
      --green: #1D9E75;
    }

    body {
      font-family: 'Syne', sans-serif;
      background: var(--bg);
      color: var(--text);
      min-height: 100vh;
      display: flex;
      justify-content: center;
      padding: 3rem 1.5rem;
    }

    .card {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: 20px;
      max-width: 780px;
      width: 100%;
      padding: 2.5rem 2.5rem;
      box-shadow: 0 4px 32px rgba(0,0,0,0.06);
    }

    /* HERO */
    .hero {
      display: flex;
      align-items: center;
      gap: 1.75rem;
      margin-bottom: 2rem;
      flex-wrap: wrap;
    }

    .avatar-wrap { position: relative; flex-shrink: 0; }

    .avatar {
      width: 88px; height: 88px;
      border-radius: 50%;
      background: linear-gradient(135deg, #1D9E75, #378ADD, #7F77DD);
      display: flex; align-items: center; justify-content: center;
      font-size: 28px; font-weight: 800; color: white; letter-spacing: -1px;
    }

    .pulse-ring {
      position: absolute; inset: -7px; border-radius: 50%;
      border: 2px solid var(--green); opacity: 0.45;
      animation: pulse 2.5s ease-in-out infinite;
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); opacity: 0.45; }
      50% { transform: scale(1.09); opacity: 0.12; }
    }

    .hero-text h1 {
      font-size: 30px; font-weight: 800;
      letter-spacing: -0.5px; line-height: 1.15; margin-bottom: 5px;
    }

    .tagline {
      font-family: 'Space Mono', monospace;
      font-size: 12px; color: var(--muted); margin-bottom: 12px;
    }

    .status-badge {
      display: inline-flex; align-items: center; gap: 6px;
      background: #eaf7f2; color: #0c6646;
      font-size: 11px; font-weight: 700;
      padding: 4px 11px; border-radius: 999px;
      text-transform: uppercase; letter-spacing: 0.9px;
    }

    .dot {
      width: 6px; height: 6px; border-radius: 50%; background: currentColor;
      animation: blink 1.4s ease-in-out infinite;
    }
    @keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0.15; } }

    /* DIVIDER */
    .divider { height: 1px; background: var(--border); margin: 1.75rem 0; }

    /* SECTION LABEL */
    .section-label {
      font-family: 'Space Mono', monospace;
      font-size: 10px; font-weight: 700;
      letter-spacing: 2.5px; text-transform: uppercase;
      color: var(--hint); margin-bottom: 1rem;
    }

    /* BIO */
    .bio {
      font-size: 15px; line-height: 1.8; color: var(--muted);
      border-left: 2.5px solid var(--green); padding-left: 1rem;
      margin-bottom: 1.25rem;
    }

    /* MISSION CARD */
    .mission-card {
      background: var(--surface2); border: 1px solid var(--border);
      border-radius: 12px; padding: 1rem 1.25rem;
      font-size: 14px; color: var(--text); font-style: italic; line-height: 1.75;
      position: relative; overflow: hidden; margin-bottom: 1.75rem;
    }
    .mission-card::before {
      content: '';
      position: absolute; left: 0; top: 0; bottom: 0; width: 3px;
      background: linear-gradient(180deg, #1D9E75, #7F77DD);
      border-radius: 3px 0 0 3px;
    }

    /* FOCUS GRID */
    .focus-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 10px; margin-bottom: 1.75rem;
    }

    .focus-item {
      background: var(--surface2); border: 1px solid var(--border);
      border-radius: 10px; padding: 0.75rem 1rem;
      display: flex; align-items: flex-start; gap: 10px;
    }

    .focus-icon {
      width: 30px; height: 30px; border-radius: 7px;
      display: flex; align-items: center; justify-content: center; flex-shrink: 0;
    }
    .focus-icon.teal { background: var(--teal-bg); color: var(--teal-text); }
    .focus-icon.purple { background: var(--purple-bg); color: var(--purple-text); }
    .focus-icon.blue { background: var(--blue-bg); color: var(--blue-text); }

    .focus-icon svg { width: 15px; height: 15px; }
    .focus-label { font-size: 13px; font-weight: 700; color: var(--text); }
    .focus-sub { font-size: 11.5px; color: var(--muted); margin-top: 2px; line-height: 1.4; }

    /* SKILLS */
    .skills-grid { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 1.75rem; }

    .skill-tag {
      font-family: 'Space Mono', monospace;
      font-size: 11.5px; font-weight: 700;
      padding: 5px 13px; border-radius: 999px; border: 1px solid;
      transition: transform 0.15s, box-shadow 0.15s; cursor: default;
    }
    .skill-tag:hover { transform: translateY(-2px); box-shadow: 0 3px 10px rgba(0,0,0,0.08); }

    .tag-teal  { background: var(--teal-bg);   color: var(--teal-text);   border-color: var(--teal-border); }
    .tag-purple{ background: var(--purple-bg); color: var(--purple-text); border-color: var(--purple-border); }
    .tag-blue  { background: var(--blue-bg);   color: var(--blue-text);   border-color: var(--blue-border); }
    .tag-amber { background: var(--amber-bg);  color: var(--amber-text);  border-color: var(--amber-border); }
    .tag-gray  { background: var(--surface2);  color: var(--muted);       border-color: var(--border); }

    /* GOAL STRIP */
    .goal-strip {
      display: flex; align-items: flex-start; gap: 14px;
      background: var(--surface2); border: 1px solid var(--border);
      border-radius: 12px; padding: 1rem 1.25rem; margin-bottom: 1.75rem;
    }
    .goal-icon {
      width: 38px; height: 38px; border-radius: 9px;
      background: var(--purple-bg);
      display: flex; align-items: center; justify-content: center; flex-shrink: 0;
    }
    .goal-text { font-size: 14px; color: var(--text); line-height: 1.6; }
    .goal-text strong { font-weight: 800; }

    /* CONTACT */
    .contact-row { display: flex; flex-wrap: wrap; gap: 10px; }

    .contact-btn {
      display: inline-flex; align-items: center; gap: 7px;
      font-family: 'Syne', sans-serif;
      font-size: 13px; font-weight: 600;
      padding: 8px 16px; border-radius: 9px;
      border: 1px solid var(--border);
      background: var(--surface); color: var(--text);
      text-decoration: none;
      transition: background 0.15s, transform 0.15s, box-shadow 0.15s;
    }
    .contact-btn:hover {
      background: var(--surface2);
      transform: translateY(-1px);
      box-shadow: 0 3px 10px rgba(0,0,0,0.07);
    }

    /* FOOTER */
    .footer {
      margin-top: 2rem; text-align: center;
      font-family: 'Space Mono', monospace;
      font-size: 10px; color: var(--hint); letter-spacing: 1px;
    }
  </style>
</head>
<body>
<div class="card">

  <!-- HERO -->
  <div class="hero">
    <div class="avatar-wrap">
      <div class="pulse-ring"></div>
      <div class="avatar">SK</div>
    </div>
    <div class="hero-text">
      <h1>Siddharth Kumar</h1>
      <div class="tagline">// AI &amp; ML Engineer in the making · CSE 2nd Year</div>
      <span class="status-badge"><span class="dot"></span> Actively learning &amp; building</span>
    </div>
  </div>

  <!-- ABOUT -->
  <p class="section-label">About</p>
  <p class="bio">
    A passionate Computer Science student specializing in Artificial Intelligence and Machine Learning, driven by a singular belief: the future belongs to those who build it. I don't just study algorithms — I ask how they can transform the world.
  </p>

  <div class="mission-card">
    My mission is to contribute to humanity's peak development in AI and ML — building systems that are not just intelligent, but meaningful. From solving everyday problems to shaping the next wave of intelligent technology, I am here to learn, build, and grow — fast.
  </div>

  <div class="divider"></div>

  <!-- FOCUS -->
  <p class="section-label">Currently focused on</p>
  <div class="focus-grid">
    <div class="focus-item">
      <div class="focus-icon teal">
        <svg viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
          <circle cx="8" cy="8" r="6" stroke="currentColor" stroke-width="1.5"/>
          <path d="M5 8l2 2 4-4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </div>
      <div>
        <div class="focus-label">ML Algorithms</div>
        <div class="focus-sub">From linear models to deep neural architectures</div>
      </div>
    </div>
    <div class="focus-item">
      <div class="focus-icon purple">
        <svg viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
          <rect x="2" y="2" width="5" height="5" rx="1" stroke="currentColor" stroke-width="1.5"/>
          <rect x="9" y="2" width="5" height="5" rx="1" stroke="currentColor" stroke-width="1.5"/>
          <rect x="2" y="9" width="5" height="5" rx="1" stroke="currentColor" stroke-width="1.5"/>
          <rect x="9" y="9" width="5" height="5" rx="1" stroke="currentColor" stroke-width="1.5"/>
        </svg>
      </div>
      <div>
        <div class="focus-label">Python &amp; ML Projects</div>
        <div class="focus-sub">Portfolio-grade apps with real-world impact</div>
      </div>
    </div>
    <div class="focus-item">
      <div class="focus-icon blue">
        <svg viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M2 12L6 7l3 3 3-4 2 2" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </div>
      <div>
        <div class="focus-label">Data Analysis</div>
        <div class="focus-sub">Extracting signal from noise with Pandas &amp; NumPy</div>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- SKILLS -->
  <p class="section-label">Tech stack</p>
  <div class="skills-grid">
    <span class="skill-tag tag-teal">Python</span>
    <span class="skill-tag tag-teal">Scikit-learn</span>
    <span class="skill-tag tag-teal">NumPy</span>
    <span class="skill-tag tag-teal">Pandas</span>
    <span class="skill-tag tag-teal">Matplotlib</span>
    <span class="skill-tag tag-purple">Machine Learning</span>
    <span class="skill-tag tag-purple">Data Analysis</span>
    <span class="skill-tag tag-blue">HTML</span>
    <span class="skill-tag tag-blue">CSS</span>
    <span class="skill-tag tag-blue">JavaScript</span>
    <span class="skill-tag tag-amber">Jupyter Notebook</span>
    <span class="skill-tag tag-amber">VS Code</span>
    <span class="skill-tag tag-gray">Git &amp; GitHub</span>
    <span class="skill-tag tag-gray">Netlify</span>
  </div>

  <div class="divider"></div>

  <!-- GOAL -->
  <div class="goal-strip">
    <div class="goal-icon">
      <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="10" cy="10" r="8" stroke="#534AB7" stroke-width="1.5"/>
        <circle cx="10" cy="10" r="4" stroke="#534AB7" stroke-width="1.5"/>
        <circle cx="10" cy="10" r="1.5" fill="#534AB7"/>
      </svg>
    </div>
    <p class="goal-text"><strong>Long-term goal:</strong> Drive AI research and development that pushes the boundaries of what's possible — building intelligent systems that benefit all of humanity.</p>
  </div>

  <!-- CONTACT -->
  <p class="section-label">Connect</p>
  <div class="contact-row">
    <a class="contact-btn" href="mailto:siddharth9508.kumar@gmail.com">
      <svg width="14" height="14" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect x="1" y="3" width="14" height="10" rx="1.5" stroke="currentColor" stroke-width="1.3"/>
        <path d="M1 5l7 5 7-5" stroke="currentColor" stroke-width="1.3" stroke-linecap="round"/>
      </svg>
      siddharth9508.kumar@gmail.com
    </a>
    <a class="contact-btn" href="https://github.com/siddharth9508kumar" target="_blank" rel="noopener">
      <svg width="14" height="14" viewBox="0 0 16 16" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
        <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/>
      </svg>
      siddharth9508kumar
    </a>
  </div>

  <div class="footer" style="margin-top: 2rem;">⭐ Always learning · Always building · Always growing</div>

</div>
</body>
</html>

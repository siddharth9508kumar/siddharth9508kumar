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

    .divider { height: 1px; background: var(--border); margin: 1.75rem 0; }

    .section-label {
      font-family: 'Space Mono', monospace;
      font-size: 10px; font-weight: 700;
      letter-spacing: 2.5px; text-transform: uppercase;
      color: var(--hint); margin-bottom: 1rem;
    }

    .bio {
      font-size: 15px; line-height: 1.8; color: var(--muted);
      border-left: 2.5px solid var(--green); padding-left: 1rem;
      margin-bottom: 1.25rem;
    }

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
    }

    .footer {
      margin-top: 2rem; text-align: center;
      font-family: 'Space Mono', monospace;
      font-size: 10px; color: var(--hint); letter-spacing: 1px;
    }
  </style>
</head>
<body>
<div class="card">

  <div class="hero">
    <div class="avatar-wrap">
      <div class="pulse-ring"></div>
      <div class="avatar">SK</div>
    </div>
    <div class="hero-text">
      <h1>Siddharth Kumar</h1>
      <div class="tagline">// AI & ML Engineer in the making · CSE 2nd Year</div>
      <span class="status-badge"><span class="dot"></span> Actively learning & building</span>
    </div>
  </div>

  <p class="section-label">About</p>
  <p class="bio">
    A passionate Computer Science student specializing in Artificial Intelligence and Machine Learning, driven by a singular belief: the future belongs to those who build it.
  </p>

  <div class="mission-card">
    My mission is to contribute to humanity's peak development in AI and ML — building meaningful intelligent systems.
  </div>

  <div class="footer">⭐ Always learning · Always building · Always growing</div>

</div>
</body>
</html>

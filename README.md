<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Weekend Warriors — The Party Game App for Friends</title>
<meta name="description" content="Weekend Warriors is a mobile party game app with quizzes, challenges, card games, dice games and Truth or Dare — made for game nights with friends. Free on iOS and Android." />
<meta name="theme-color" content="#1F3358" />

<!-- Open Graph -->
<meta property="og:title" content="Weekend Warriors — The Party Game App for Friends" />
<meta property="og:description" content="Quizzes, challenges, cards, dice and Truth or Dare — one app for your whole friend group's game night." />
<meta property="og:type" content="website" />

<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@500;600;700&family=Manrope:wght@400;500;700;800&display=swap" rel="stylesheet" />

<style>
  :root {
    --cream: #FFF6E8;
    --surface: #FFFFFF;
    --ink: #26201A;
    --muted: #6B6157;
    --navy: #1F3358;
    --navy-light: #2E4876;
    --coral: #FF5A3C;
    --coral-dark: #E24726;
    --gold: #FFC145;
    --line: #EAE0D0;
    --radius-lg: 28px;
    --radius-md: 18px;
    --radius-sm: 12px;
    --maxw: 1200px;
    --shadow: 0 14px 34px rgba(38, 32, 26, 0.10);
    --shadow-sm: 0 6px 16px rgba(38, 32, 26, 0.08);
  }

  @media (min-width: 1560px) { :root { --maxw: 1320px; } }
  @media (min-width: 1900px) { :root { --maxw: 1440px; } }

  * { box-sizing: border-box; min-width: 0; }
  html { scroll-behavior: smooth; margin: 0; padding: 0; width: 100%; background: var(--navy); }
  html, body { overflow-x: hidden; }
  @media (prefers-reduced-motion: reduce) {
    html { scroll-behavior: auto; }
    *, *::before, *::after { animation-duration: 0.001ms !important; animation-iteration-count: 1 !important; transition-duration: 0.001ms !important; }
  }

  body {
    margin: 0;
    padding: 0;
    width: 100%;
    font-family: 'Manrope', Arial, sans-serif;
    color: var(--ink);
    background: var(--cream);
    line-height: 1.55;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }

  main { flex: 1 0 auto; }

  h1, h2, h3 {
    font-family: 'Fredoka', 'Manrope', Arial, sans-serif;
    font-weight: 600;
    line-height: 1.12;
    margin: 0;
    color: var(--navy);
  }

  p { margin: 0; }

  a { color: inherit; }

  img, svg { display: block; max-width: 100%; }

  .container {
    width: 100%;
    max-width: var(--maxw);
    margin: 0 auto;
    padding: 0 24px;
  }

  @media (min-width: 640px) {
    .container { padding: 0 32px; }
  }

  .skip-link {
    position: absolute;
    left: 12px;
    top: -60px;
    background: var(--navy);
    color: white;
    padding: 10px 16px;
    border-radius: 0 0 8px 8px;
    z-index: 100;
    transition: top 0.15s ease;
  }
  .skip-link:focus { top: 0; }

  a:focus-visible,
  button:focus-visible,
  summary:focus-visible {
    outline: 3px solid var(--coral);
    outline-offset: 3px;
    border-radius: 6px;
  }

  /* ---------- Header ---------- */
  header {
    position: sticky;
    top: 0;
    z-index: 20;
    background: rgba(255, 246, 232, 0.9);
    backdrop-filter: blur(8px);
    border-bottom: 1px solid var(--line);
  }

  .nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 16px 0;
    gap: 16px;
  }

  .brand {
    display: flex;
    align-items: center;
    gap: 10px;
    font-family: 'Fredoka', sans-serif;
    font-weight: 700;
    font-size: 1.15rem;
    color: var(--navy);
    text-decoration: none;
  }

  .brand-mark {
    width: 34px;
    height: 34px;
    border-radius: 10px;
    background: var(--coral);
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    flex-shrink: 0;
  }

  .menu {
    display: none;
    list-style: none;
    gap: 2px;
    padding: 0;
    margin: 0;
    flex-wrap: nowrap;
  }

  .menu a {
    text-decoration: none;
    font-weight: 700;
    font-size: 0.86rem;
    padding: 8px 12px;
    border-radius: 999px;
    color: var(--navy);
    white-space: nowrap;
    transition: background 0.15s ease, color 0.15s ease;
  }

  .menu a:hover { background: var(--navy); color: white; }

  .nav-cta {
    display: none;
  }

  @media (min-width: 1120px) {
    .menu { display: flex; }
    .nav-cta {
      display: inline-flex;
      align-items: center;
      background: var(--navy);
      color: white;
      font-weight: 700;
      font-size: 0.9rem;
      padding: 10px 20px;
      border-radius: 999px;
      text-decoration: none;
      white-space: nowrap;
      transition: background 0.15s ease;
    }
    .nav-cta:hover { background: var(--navy-light); }
  }

  /* ---------- Buttons ---------- */
  .btn-group {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
  }

  .store-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: var(--navy);
    color: white;
    text-decoration: none;
    padding: 13px 22px;
    border-radius: 999px;
    font-weight: 700;
    font-size: 0.98rem;
    box-shadow: var(--shadow-sm);
    transition: transform 0.15s ease, background 0.15s ease;
  }

  .store-btn:hover { background: var(--navy-light); transform: translateY(-2px); }

  .store-btn.alt {
    background: white;
    color: var(--navy);
    border: 2px solid var(--navy);
  }
  .store-btn.alt:hover { background: var(--navy); color: white; }

  .store-btn svg { flex-shrink: 0; }

  /* ---------- Hero ---------- */
  .hero {
    padding: 56px 0 40px;
    overflow: hidden;
  }

  .hero-grid {
    display: grid;
    gap: 40px;
    align-items: center;
  }

  @media (min-width: 900px) {
    .hero-grid { grid-template-columns: 1.05fr 0.95fr; gap: 24px; }
  }

  .hero h1 {
    font-size: clamp(2.3rem, 5.2vw, 3.4rem);
    letter-spacing: -0.01em;
  }

  .hero-sub {
    margin-top: 18px;
    font-size: 1.12rem;
    color: var(--muted);
    max-width: 46ch;
  }

  .hero .btn-group { margin-top: 28px; }

  .hero-note {
    margin-top: 16px;
    font-size: 0.88rem;
    color: var(--muted);
  }

  /* Fanned card visual */
  .card-fan {
    position: relative;
    height: 340px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .play-card {
    position: absolute;
    width: 148px;
    height: 208px;
    background: var(--surface);
    border-radius: 18px;
    box-shadow: var(--shadow);
    padding: 18px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    transition: transform 0.4s ease;
  }

  .play-card .tag {
    font-size: 0.72rem;
    font-weight: 800;
    color: var(--muted);
  }

  .play-card .icon-wrap {
    width: 44px;
    height: 44px;
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
  }

  .play-card .prompt {
    font-family: 'Fredoka', sans-serif;
    font-weight: 600;
    font-size: 1rem;
    color: var(--navy);
    line-height: 1.2;
  }

  .pc-1 { background: var(--coral); transform: rotate(-14deg) translate(-92px, 8px); z-index: 1; }
  .pc-1 .icon-wrap { background: rgba(255,255,255,0.22); }
  .pc-1 .tag, .pc-1 .prompt { color: white; }

  .pc-2 { transform: rotate(-4deg) translate(-18px, -6px); z-index: 2; }
  .pc-2 .icon-wrap { background: var(--gold); color: var(--navy); }

  .pc-3 { transform: rotate(7deg) translate(56px, 4px); z-index: 3; }
  .pc-3 .icon-wrap { background: var(--navy); color: white; }

  .pc-4 { background: var(--navy); transform: rotate(15deg) translate(122px, 20px); z-index: 1; }
  .pc-4 .icon-wrap { background: rgba(255,255,255,0.16); }
  .pc-4 .tag, .pc-4 .prompt { color: white; }

  @media (min-width: 900px) {
    .card-fan:hover .pc-1 { transform: rotate(-18deg) translate(-100px, 0px); }
    .card-fan:hover .pc-2 { transform: rotate(-5deg) translate(-20px, -14px); }
    .card-fan:hover .pc-3 { transform: rotate(9deg) translate(60px, -6px); }
    .card-fan:hover .pc-4 { transform: rotate(19deg) translate(130px, 12px); }
  }

  @media (max-width: 899px) {
    .card-fan { height: 260px; }
    .play-card { width: 118px; height: 166px; padding: 14px; }
    .play-card .prompt { font-size: 0.85rem; }
    .pc-1 { transform: rotate(-14deg) translate(-64px, 6px); }
    .pc-2 { transform: rotate(-4deg) translate(-12px, -4px); }
    .pc-3 { transform: rotate(7deg) translate(40px, 2px); }
    .pc-4 { transform: rotate(15deg) translate(86px, 14px); }
  }

  /* ---------- Section shell ---------- */
  section { padding: 64px 0; }
  section .eyebrow-free-heading { max-width: 60ch; }
  .section-head { margin-bottom: 36px; }
  .section-head h2 { font-size: clamp(1.6rem, 3.4vw, 2.15rem); }
  .section-head p {
    margin-top: 12px;
    color: var(--muted);
    max-width: 56ch;
    font-size: 1.02rem;
  }

  /* ---------- Features (asymmetric bento) ---------- */
  .bento {
    display: grid;
    gap: 18px;
  }

  @media (min-width: 860px) {
    .bento {
      grid-template-columns: 1.3fr 1fr;
      grid-template-rows: auto auto;
    }
    .bento .card-big { grid-row: 1 / 3; }
    .bento .card-wide { grid-column: 1 / 3; }
  }

  .feature-card {
    background: var(--surface);
    border-radius: var(--radius-md);
    padding: 30px;
    box-shadow: var(--shadow-sm);
    display: flex;
    flex-direction: column;
    gap: 14px;
  }

  .feature-card.dark {
    background: var(--navy);
    color: white;
  }
  .feature-card.dark h3 { color: white; }
  .feature-card.dark p { color: rgba(255,255,255,0.78); }

  .feature-card .icon-badge {
    width: 46px;
    height: 46px;
    border-radius: 12px;
    background: var(--cream);
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--coral);
  }
  .feature-card.dark .icon-badge { background: rgba(255,255,255,0.14); color: var(--gold); }

  .feature-card h3 { font-size: 1.2rem; }
  .feature-card p { color: var(--muted); font-size: 0.98rem; }

  .card-big .icon-badge { width: 54px; height: 54px; }
  .card-big h3 { font-size: 1.55rem; }
  .card-big p { font-size: 1.02rem; max-width: 40ch; }

  .card-wide {
    flex-direction: row;
    align-items: center;
    gap: 24px;
  }
  @media (max-width: 640px) {
    .card-wide { flex-direction: column; align-items: flex-start; }
  }

  /* ---------- Game categories ---------- */
  .cat-grid {
    display: grid;
    grid-template-columns: 1fr;
    gap: 16px;
  }

  @media (min-width: 640px) {
    .cat-grid { grid-template-columns: 1fr 1fr; }
  }
  @media (min-width: 980px) {
    .cat-grid { grid-template-columns: repeat(3, 1fr); }
  }

  .cat-card {
    background: var(--surface);
    border-top: 4px solid var(--coral);
    border-radius: var(--radius-sm);
    padding: 24px;
    box-shadow: var(--shadow-sm);
    display: flex;
    flex-direction: column;
    gap: 12px;
  }

  .cat-card:nth-child(2n) { border-top-color: var(--gold); }
  .cat-card:nth-child(3n) { border-top-color: var(--navy); }

  .cat-card .icon-wrap {
    width: 42px;
    height: 42px;
    border-radius: 10px;
    background: var(--cream);
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--navy);
  }

  .cat-card h3 { font-size: 1.08rem; }
  .cat-card p { color: var(--muted); font-size: 0.94rem; }

  /* ---------- How it works ---------- */
  .steps {
    list-style: none;
    margin: 0;
    padding: 0;
    display: grid;
    gap: 20px;
  }

  @media (min-width: 760px) {
    .steps {
      position: relative;
      padding-left: 0;
    }
    .steps::before {
      content: "";
      position: absolute;
      left: 27px;
      top: 12px;
      bottom: 12px;
      width: 2px;
      background: var(--line);
    }
  }

  .step {
    display: flex;
    gap: 20px;
    align-items: flex-start;
  }

  .step-num {
    flex-shrink: 0;
    width: 56px;
    height: 56px;
    border-radius: 50%;
    background: var(--navy);
    color: white;
    font-family: 'Fredoka', sans-serif;
    font-weight: 700;
    font-size: 1.3rem;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    z-index: 1;
  }

  .step:nth-child(2n) .step-num { background: var(--coral); }

  .step-body h3 { font-size: 1.08rem; margin-bottom: 4px; }
  .step-body p { color: var(--muted); font-size: 0.98rem; }

  /* ---------- Support panel ---------- */
  .support-panel {
    background: var(--surface);
    border-radius: var(--radius-lg);
    padding: 44px 32px;
    text-align: center;
    box-shadow: var(--shadow-sm);
    max-width: 640px;
    margin: 0 auto;
  }

  .support-panel .icon-badge {
    width: 52px;
    height: 52px;
    border-radius: 14px;
    background: var(--cream);
    color: var(--coral);
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 18px;
  }

  .support-panel h2 { font-size: clamp(1.4rem, 2.8vw, 1.7rem); }

  .support-panel p {
    margin-top: 12px;
    color: var(--muted);
    font-size: 1.02rem;
    max-width: 44ch;
    margin-left: auto;
    margin-right: auto;
  }

  .support-panel .store-btn { margin-top: 24px; background: var(--coral); }
  .support-panel .store-btn:hover { background: var(--coral-dark); }

  /* ---------- Download banner ---------- */
  .download-banner {
    background: linear-gradient(135deg, var(--coral), var(--gold));
    border-radius: var(--radius-lg);
    padding: 48px 32px;
    text-align: center;
    color: white;
    box-shadow: var(--shadow);
  }

  .download-banner h2 { color: white; font-size: clamp(1.6rem, 3.6vw, 2.2rem); }
  .download-banner p {
    margin-top: 10px;
    color: rgba(255,255,255,0.92);
    font-size: 1.05rem;
  }
  .download-banner .btn-group {
    justify-content: center;
    margin-top: 26px;
  }
  .download-banner .store-btn { background: var(--navy); }
  .download-banner .store-btn:hover { background: #16294a; }
  .download-banner .store-btn.alt { background: white; color: var(--navy); border-color: white; }
  .download-banner .store-btn.alt:hover { background: rgba(255,255,255,0.85); }

  /* ---------- FAQ / Support ---------- */
  .faq-list details {
    background: var(--surface);
    border: 1px solid var(--line);
    border-radius: var(--radius-sm);
    padding: 4px 20px;
    margin-bottom: 12px;
  }
  .faq-list summary {
    cursor: pointer;
    font-weight: 700;
    padding: 16px 0;
    color: var(--navy);
    font-family: 'Fredoka', sans-serif;
    list-style: none;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 12px;
  }
  .faq-list summary::-webkit-details-marker { display: none; }
  .faq-list summary::after {
    content: "+";
    font-size: 1.4rem;
    color: var(--coral);
    flex-shrink: 0;
  }
  .faq-list details[open] summary::after { content: "–"; }
  .faq-list p { padding-bottom: 18px; color: var(--muted); }

  /* ---------- Footer ---------- */
  footer {
    background: var(--navy);
    color: rgba(255,255,255,0.85);
    padding: 44px 0 28px;
    margin-top: 24px;
    flex-shrink: 0;
    width: 100vw;
    position: relative;
    left: 50%;
    right: 50%;
    margin-left: -50vw;
    margin-right: -50vw;
  }

  .footer-grid {
    display: grid;
    gap: 28px;
  }

  @media (min-width: 700px) {
    .footer-grid { grid-template-columns: 1.2fr 1fr 1fr; }
  }

  .footer-brand {
    display: flex;
    align-items: center;
    gap: 10px;
    font-family: 'Fredoka', sans-serif;
    font-weight: 700;
    color: white;
    font-size: 1.1rem;
  }
  .footer-brand .brand-mark { background: var(--coral); }

  footer h4 {
    color: white;
    font-family: 'Fredoka', sans-serif;
    font-size: 0.98rem;
    margin: 0 0 12px;
  }

  footer ul { list-style: none; margin: 0; padding: 0; display: grid; gap: 8px; }
  footer a { text-decoration: none; color: rgba(255,255,255,0.78); font-size: 0.94rem; }
  footer a:hover { color: white; text-decoration: underline; }

  .donate-btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    margin-top: 14px;
    background: var(--coral);
    color: white;
    text-decoration: none;
    font-weight: 700;
    font-size: 0.92rem;
    padding: 11px 20px;
    border-radius: 999px;
    transition: background 0.15s ease, transform 0.15s ease;
  }
  .donate-btn:hover { background: var(--coral-dark); transform: translateY(-2px); }

  .footer-bottom {
    margin-top: 36px;
    padding-top: 20px;
    border-top: 1px solid rgba(255,255,255,0.14);
    font-size: 0.82rem;
    color: rgba(255,255,255,0.6);
    display: flex;
    flex-direction: row;
    align-items: baseline;
    justify-content: space-between;
    gap: 16px;
  }

  .footer-bottom span:first-child { text-align: left; }
  .footer-bottom span:last-child { text-align: right; }

  @media (max-width: 420px) {
    .footer-bottom { font-size: 0.74rem; gap: 10px; }
  }
</style>
</head>

<body>

<a class="skip-link" href="#main">Skip to content</a>

<header>
  <nav class="container nav" aria-label="Main navigation">
    <a class="brand" href="#top">
      <span class="brand-mark" aria-hidden="true">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <rect x="3" y="3" width="7" height="7" rx="2"></rect>
          <rect x="14" y="3" width="7" height="7" rx="2"></rect>
          <rect x="3" y="14" width="7" height="7" rx="2"></rect>
          <rect x="14" y="14" width="7" height="7" rx="2"></rect>
        </svg>
      </span>
      Weekend Warriors
    </a>
    <ul class="menu">
      <li><a href="#features">Why you'll love it</a></li>
      <li><a href="#games">Games</a></li>
      <li><a href="#how">How it works</a></li>
      <li><a href="#support">Support us</a></li>
      <li><a href="#faq">FAQ</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <a class="nav-cta" href="#download">Get the app</a>
  </nav>
</header>

<main id="main">

  <div id="top" class="container hero">
    <div class="hero-grid">
      <div>
        <h1>Turn any hangout into a game night.</h1>
        <p class="hero-sub">
          Weekend Warriors packs quizzes, challenges, choices, card games, dice games and Truth or Dare into one app —
          no board, no setup, just you and your friends passing the phone around.
        </p>
        <div class="btn-group">
          <a class="store-btn" href="https://play.google.com/store/apps/details?id=com.weekendwarriors.app" target="_blank" rel="noopener noreferrer">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M3 2.6a1 1 0 0 1 1.5-.86l13.7 8.4a1 1 0 0 1 0 1.72L4.5 20.26A1 1 0 0 1 3 19.4V2.6z"/></svg>
            Get it on Google Play
          </a>
          <a class="store-btn alt" href="https://apps.apple.com/app/idXXXXXXXXXX" target="_blank" rel="noopener noreferrer">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M16.7 1.2c.1 1.1-.3 2.2-1 3-.7.8-1.8 1.4-2.9 1.3-.1-1.1.4-2.2 1.1-2.9.7-.8 1.9-1.4 2.8-1.4zM20.9 17c-.6 1.3-.9 1.9-1.6 3-1 1.5-2.5 3.4-4.3 3.4-1.6 0-2-1-4.1-1s-2.6 1-4.2 1c-1.8 0-3.2-1.7-4.2-3.2C.2 16.8-.5 12 1 8.9c1-2.1 2.9-3.5 4.9-3.5 1.6 0 2.7 1.1 4.1 1.1 1.3 0 2.2-1.1 4.1-1.1 1.5 0 3.2.9 4.2 2.4-3.7 2-3.1 7.3 1.6 9.2z"/></svg>
            Download on the App Store
          </a>
        </div>
        <p class="hero-note">Free to download · Made for friend groups of 2 and up</p>
      </div>

      <div class="card-fan" aria-hidden="true">
        <div class="play-card pc-1">
          <div class="icon-wrap">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"></circle><path d="M9.5 9.5a2.5 2.5 0 1 1 3.5 2.3c-1 .5-1.5 1-1.5 2.2"></path><circle cx="12" cy="17" r="0.5" fill="currentColor"></circle></svg>
          </div>
          <div>
            <div class="tag">QUIZ</div>
            <div class="prompt">Who's most likely to...?</div>
          </div>
        </div>
        <div class="play-card pc-2">
          <div class="icon-wrap">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="3" width="18" height="18" rx="4"></rect><circle cx="8.5" cy="8.5" r="1" fill="currentColor" stroke="none"></circle><circle cx="15.5" cy="15.5" r="1" fill="currentColor" stroke="none"></circle><circle cx="12" cy="12" r="1" fill="currentColor" stroke="none"></circle></svg>
          </div>
          <div>
            <div class="tag">DICE</div>
            <div class="prompt">Roll and act it out</div>
          </div>
        </div>
        <div class="play-card pc-3">
          <div class="icon-wrap">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M7 10a5 5 0 0 1 10 0c0 3-2.5 3.5-2.5 6H9.5c0-2.5-2.5-3-2.5-6z"></path><path d="M9.5 20h5"></path></svg>
          </div>
          <div>
            <div class="tag">CHALLENGE</div>
            <div class="prompt">Last one to laugh wins</div>
          </div>
        </div>
        <div class="play-card pc-4">
          <div class="icon-wrap">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 15a2 2 0 0 1-2 2H8l-4 4V5a2 2 0 0 1 2-2h13a2 2 0 0 1 2 2z"></path></svg>
          </div>
          <div>
            <div class="tag">TRUTH OR DARE</div>
            <div class="prompt">Pick your fate</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <section id="features">
    <div class="container">
      <div class="section-head">
        <h2>Built for the whole group, not just one player</h2>
        <p>Every part of Weekend Warriors is designed around playing together — same room, same table, phone in the middle.</p>
      </div>

      <div class="bento">
        <div class="feature-card card-big">
          <div class="icon-badge" aria-hidden="true">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"></path><circle cx="9" cy="7" r="4"></circle><path d="M23 21v-2a4 4 0 0 0-3-3.87"></path><path d="M16 3.13a4 4 0 0 1 0 7.75"></path></svg>
          </div>
          <h3>One app, endless game nights</h3>
          <p>Mix quizzes, challenges, choices, card games and dice rounds however you like. Play a quick five-minute round before dinner, or turn a whole evening into a tournament.</p>
        </div>

        <div class="feature-card">
          <div class="icon-badge" aria-hidden="true">
            <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M13 2 3 14h9l-1 8 10-12h-9l1-8z"></path></svg>
          </div>
          <h3>Zero setup</h3>
          <p>No boards, no cards to shuffle. Open the app and you're playing in under a minute.</p>
        </div>

        <div class="feature-card">
          <div class="icon-badge" aria-hidden="true">
            <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"></path><circle cx="9" cy="7" r="4"></circle><path d="M23 21v-2a4 4 0 0 0-3-3.87"></path><path d="M16 3.13a4 4 0 0 1 0 7.75"></path></svg>
          </div>
          <h3>Works for any group size</h3>
          <p>From a couple on the couch to a full houseparty — the games scale with how many of you show up.</p>
        </div>

        <div class="feature-card card-wide">
          <div class="icon-badge" aria-hidden="true">
            <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20.8 4.6a5.5 5.5 0 0 0-7.8 0L12 5.6l-1-1a5.5 5.5 0 1 0-7.8 7.8l1 1L12 21l7.8-7.6 1-1a5.5 5.5 0 0 0 0-7.8z"></path></svg>
          </div>
          <div>
            <h3>Real laughs, not screen time</h3>
            <p>Once you've picked a game, the phone becomes the referee, not the entertainment. The point is looking at each other, not your feed.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="games" style="background: var(--surface);">
    <div class="container">
      <div class="section-head">
        <h2>Six ways to play</h2>
        <p>Pick one category or shuffle them all together — every game is built to be quick to learn and fun with people you actually know.</p>
      </div>

      <div class="cat-grid">
        <div class="cat-card">
          <div class="icon-wrap" aria-hidden="true">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"></circle><path d="M9.5 9.5a2.5 2.5 0 1 1 3.5 2.3c-1 .5-1.5 1-1.5 2.2"></path><circle cx="12" cy="17" r="0.5" fill="currentColor"></circle></svg>
          </div>
          <h3>Quizzes</h3>
          <p>Trivia, pop culture and "who knows the group best" rounds that spark friendly bragging rights.</p>
        </div>

        <div class="cat-card">
          <div class="icon-wrap" aria-hidden="true">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M13 2 3 14h9l-1 8 10-12h-9l1-8z"></path></svg>
          </div>
          <h3>Challenges</h3>
          <p>Quick, silly, easy-to-judge challenges that get everyone off the couch for a minute.</p>
        </div>

        <div class="cat-card">
          <div class="icon-wrap" aria-hidden="true">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M6 3v18"></path><path d="M6 8h9a3 3 0 0 0 0-6"></path><path d="M6 16h9a3 3 0 0 1 0 6"></path></svg>
          </div>
          <h3>Choices</h3>
          <p>Would-you-rather style picks that always end in a group debate about who's right.</p>
        </div>

        <div class="cat-card">
          <div class="icon-wrap" aria-hidden="true">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="4" y="2" width="12" height="17" rx="2" transform="rotate(-8 10 10)"></rect></svg>
          </div>
          <h3>Card games</h3>
          <p>Classic card-game formats, reimagined so any group can pick them up in seconds.</p>
        </div>

        <div class="cat-card">
          <div class="icon-wrap" aria-hidden="true">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="3" width="18" height="18" rx="4"></rect><circle cx="8.5" cy="8.5" r="1" fill="currentColor" stroke="none"></circle><circle cx="15.5" cy="15.5" r="1" fill="currentColor" stroke="none"></circle><circle cx="12" cy="12" r="1" fill="currentColor" stroke="none"></circle></svg>
          </div>
          <h3>Dice games</h3>
          <p>Roll, react, and let chance pick who's up next — simple rules, unpredictable results.</p>
        </div>

        <div class="cat-card">
          <div class="icon-wrap" aria-hidden="true">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 15a2 2 0 0 1-2 2H8l-4 4V5a2 2 0 0 1 2-2h13a2 2 0 0 1 2 2z"></path></svg>
          </div>
          <h3>Truth or Dare</h3>
          <p>Lighthearted truths and playful, family-friendly dares — nothing you wouldn't do in front of your grandma.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="how">
    <div class="container">
      <div class="section-head">
        <h2>From download to game night in four steps</h2>
      </div>

      <ol class="steps">
        <li class="step">
          <div class="step-num" aria-hidden="true">1</div>
          <div class="step-body">
            <h3>Download the app</h3>
            <p>Free on both iOS and Android — no account needed to start playing.</p>
          </div>
        </li>
        <li class="step">
          <div class="step-num" aria-hidden="true">2</div>
          <div class="step-body">
            <h3>Pick your categories</h3>
            <p>Mix and match quizzes, dares, challenges, cards and dice to fit your group's mood.</p>
          </div>
        </li>
        <li class="step">
          <div class="step-num" aria-hidden="true">3</div>
          <div class="step-body">
            <h3>Gather your crew</h3>
            <p>Works for two people or a whole houseparty — settle in around one phone.</p>
          </div>
        </li>
        <li class="step">
          <div class="step-num" aria-hidden="true">4</div>
          <div class="step-body">
            <h3>Play, laugh, repeat</h3>
            <p>Pass the phone, take turns, and let the app keep score while you focus on each other.</p>
          </div>
        </li>
      </ol>
    </div>
  </section>

  <section id="support">
    <div class="container">
      <div class="support-panel">
        <div class="icon-badge" aria-hidden="true">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20.8 4.6a5.5 5.5 0 0 0-7.8 0L12 5.6l-1-1a5.5 5.5 0 1 0-7.8 7.8l1 1L12 21l7.8-7.6 1-1a5.5 5.5 0 0 0 0-7.8z"></path></svg>
        </div>
        <h2>Support the project</h2>
        <p>Weekend Warriors is a student passion project. If you enjoy it, consider supporting development.</p>
        <a class="store-btn" href="https://www.paypal.com/paypalme/JSmeerkaas" target="_blank" rel="noopener noreferrer">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M7.5 2.5h6.7c3 0 5 1.9 4.5 4.9-.6 3.7-3 5.6-6.6 5.6H9.8l-1 6.2H5.4L7.5 2.5zm2.7 8.2h1.9c1.9 0 3-.9 3.3-2.8.3-1.8-.6-2.6-2.4-2.6h-1.8l-1 5.4z"/></svg>
          Doneer via PayPal
        </a>
      </div>
    </div>
  </section>

  <section id="download">
    <div class="container">
      <div class="download-banner">
        <h2>Free to download. Built for weekends.</h2>
        <p>Grab your friends, pick a game, and see who's really the Weekend Warrior.</p>
        <div class="btn-group">
          <a class="store-btn" href="https://play.google.com/store/apps/details?id=com.weekendwarriors.app" target="_blank" rel="noopener noreferrer">
            <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M3 2.6a1 1 0 0 1 1.5-.86l13.7 8.4a1 1 0 0 1 0 1.72L4.5 20.26A1 1 0 0 1 3 19.4V2.6z"/></svg>
            Get it on Google Play
          </a>
          <a class="store-btn alt" href="https://apps.apple.com/app/idXXXXXXXXXX" target="_blank" rel="noopener noreferrer">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M16.7 1.2c.1 1.1-.3 2.2-1 3-.7.8-1.8 1.4-2.9 1.3-.1-1.1.4-2.2 1.1-2.9.7-.8 1.9-1.4 2.8-1.4zM20.9 17c-.6 1.3-.9 1.9-1.6 3-1 1.5-2.5 3.4-4.3 3.4-1.6 0-2-1-4.1-1s-2.6 1-4.2 1c-1.8 0-3.2-1.7-4.2-3.2C.2 16.8-.5 12 1 8.9c1-2.1 2.9-3.5 4.9-3.5 1.6 0 2.7 1.1 4.1 1.1 1.3 0 2.2-1.1 4.1-1.1 1.5 0 3.2.9 4.2 2.4-3.7 2-3.1 7.3 1.6 9.2z"/></svg>
            Download on the App Store
          </a>
        </div>
      </div>
    </div>
  </section>

  <section id="faq" style="background: var(--surface);">
    <div class="container">
      <div class="section-head">
        <h2>Frequently asked questions</h2>
      </div>

      <div class="faq-list">
        <details>
          <summary>Is Weekend Warriors free?</summary>
          <p>Yes, the app is free to download on both Google Play and the App Store.</p>
        </details>
        <details>
          <summary>How many people can play?</summary>
          <p>Weekend Warriors works with as few as two players and scales up to a full group — there's no fixed maximum.</p>
        </details>
        <details>
          <summary>Do I need an account to play?</summary>
          <p>No, you can open the app and start playing right away without signing up.</p>
        </details>
        <details>
          <summary>Is the content appropriate for everyone?</summary>
          <p>Weekend Warriors is designed to be light, family-friendly fun for friend groups. It doesn't include mature themes such as alcohol, gambling or adult content.</p>
        </details>
        <details>
          <summary>Can I choose which type of games we play?</summary>
          <p>Yes, you can pick and combine categories like quizzes, challenges, choices, card games, dice games and Truth or Dare.</p>
        </details>
        <details>
          <summary>Does the app need an internet connection?</summary>
          <p>Most game content works offline once downloaded, which makes it handy for game nights anywhere.</p>
        </details>
      </div>
    </div>
  </section>

</main>

<footer id="contact">
  <div class="container footer-grid">
    <div>
      <div class="footer-brand">
        <span class="brand-mark" aria-hidden="true">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <rect x="3" y="3" width="7" height="7" rx="2"></rect>
            <rect x="14" y="3" width="7" height="7" rx="2"></rect>
            <rect x="3" y="14" width="7" height="7" rx="2"></rect>
            <rect x="14" y="14" width="7" height="7" rx="2"></rect>
          </svg>
        </span>
        Weekend Warriors
      </div>
    </div>

    <div>
      <p style="margin-top: 14px; max-width: 34ch; color: rgba(255,255,255,0.72); font-size: 0.94rem;">
        The party game app that gets friend groups off their feeds and into the room.
      </p>
    </div>
    <div>
      <h4>Explore</h4>
      <ul>
        <li><a href="#features">Why you'll love it</a></li>
        <li><a href="#games">Games</a></li>
        <li><a href="#how">How it works</a></li>
        <li><a href="#faq">FAQ</a></li>
      </ul>
    </div>

    <div>
      <h4>Support</h4>
      <ul>
        <li><a href="https://docs.google.com/document/d/11vJCnAG37Z6YQKx41V-x_h5Abil_VlyKp0LTUG6FX0E/edit?usp=sharing">Privacy Policy</a></li>
        <li><a href="mailto:bwbbstudio@gmail.com">bwbbstudio@gmail.com</a></li>
      </ul>
      <a class="donate-btn" href="https://www.paypal.com/paypalme/JSmeerkaas" target="_blank" rel="noopener noreferrer">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M20.8 4.6a5.5 5.5 0 0 0-7.8 0L12 5.6l-1-1a5.5 5.5 0 1 0-7.8 7.8l1 1L12 21l7.8-7.6 1-1a5.5 5.5 0 0 0 0-7.8z"></path></svg>
        Doneer via PayPal
      </a>
    </div>
  </div>

  <div class="container footer-bottom">
    <span>© 2026 Weekend Warriors</span>
    <span>Made for friend groups everywhere</span>
  </div>
</footer>

</body>
</html>

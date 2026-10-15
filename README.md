<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>DigitalForgePro | Software built to take a hit</title>
<meta name="description" content="DigitalForgePro designs, builds and runs websites, mobile apps and cloud systems. Led by CEO Andrew Parker and Manager Daniel Wilson.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,500;12..96,700;12..96,800&family=Public+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
:root{
  --forge:#0F1B2E;      /* deep blue-slate */
  --forge-2:#17294A;
  --steel:#E8ECF1;
  --paper:#F7F8FA;
  --white:#FFFFFF;
  --cobalt:#2340E8;
  --cobalt-d:#1A31B8;
  --ember:#FF7A1A;
  --ink:#16202D;
  --muted:#5A6676;
  --line:#D5DBE3;
  --display:'Bricolage Grotesque','Segoe UI',system-ui,sans-serif;
  --body:'Public Sans','Segoe UI',system-ui,-apple-system,sans-serif;
  --wrap:1160px;
}
*,*::before,*::after{box-sizing:border-box}
html{scroll-behavior:smooth}
body{margin:0;font-family:var(--body);font-size:1.0625rem;line-height:1.65;color:var(--ink);background:var(--paper);-webkit-font-smoothing:antialiased}
img,svg,canvas{display:block;max-width:100%}
h1,h2,h3,h4{font-family:var(--display);line-height:1.1;margin:0 0 .5em;letter-spacing:-.02em;color:inherit}
h1{font-size:clamp(2.5rem,6.5vw,5rem);font-weight:800}
h2{font-size:clamp(1.8rem,3.6vw,2.75rem);font-weight:700}
h3{font-size:1.35rem;font-weight:700}
p{margin:0 0 1em;max-width:68ch}
a{color:var(--cobalt)}
:focus-visible{outline:3px solid var(--ember);outline-offset:3px;border-radius:4px}
.wrap{width:min(100% - 2.5rem,var(--wrap));margin-inline:auto}
.skip{position:absolute;left:-999px;top:0;background:var(--ember);color:#000;padding:.6rem 1rem;z-index:100}
.skip:focus{left:0}

/* ---------- Buttons ---------- */
.btn{display:inline-flex;align-items:center;justify-content:center;gap:.5rem;font:600 1rem var(--body);padding:.85rem 1.5rem;border-radius:999px;border:2px solid transparent;cursor:pointer;text-decoration:none;transition:background .2s,color .2s,border-color .2s,transform .15s}
.btn:active{transform:translateY(1px)}
.btn-primary{background:var(--ember);color:#1a0d00}
.btn-primary:hover{background:#ff8f3d}
.btn-blue{background:var(--cobalt);color:#fff}
.btn-blue:hover{background:var(--cobalt-d)}
.btn-ghost{border-color:rgba(255,255,255,.45);color:#fff}
.btn-ghost:hover{background:rgba(255,255,255,.12)}
.btn-line{border-color:var(--ink);color:var(--ink)}
.btn-line:hover{background:var(--ink);color:#fff}

/* ---------- Header ---------- */
header.site{position:sticky;top:0;z-index:50;background:rgba(15,27,46,.94);backdrop-filter:blur(10px);color:#fff;border-bottom:1px solid rgba(255,255,255,.08)}
.nav{display:flex;align-items:center;justify-content:space-between;height:68px}
.logo{display:flex;align-items:center;gap:.6rem;font:800 1.25rem var(--display);color:#fff;text-decoration:none;letter-spacing:-.02em}
.logo b{color:var(--ember);font-weight:800}
.logo svg{width:28px;height:28px}
.nav ul{display:flex;gap:.25rem;list-style:none;margin:0;padding:0;align-items:center}
.nav a.link{color:#D4DCEA;text-decoration:none;padding:.5rem .85rem;border-radius:8px;font-weight:500;font-size:.98rem}
.nav a.link:hover{color:#fff;background:rgba(255,255,255,.08)}
.nav a.link[aria-current="page"]{color:#fff;box-shadow:inset 0 -2px 0 var(--ember);border-radius:0}
.nav .cta{margin-left:.5rem;padding:.55rem 1.1rem}
.burger{display:none;background:none;border:0;color:#fff;width:44px;height:44px;cursor:pointer;border-radius:8px}
.burger span{display:block;width:22px;height:2px;background:#fff;margin:5px auto;transition:transform .25s,opacity .2s}
.burger[aria-expanded="true"] span:nth-child(1){transform:translateY(7px) rotate(45deg)}
.burger[aria-expanded="true"] span:nth-child(2){opacity:0}
.burger[aria-expanded="true"] span:nth-child(3){transform:translateY(-7px) rotate(-45deg)}

/* ---------- Pages ---------- */
.page{display:none}
.page.active{display:block}
section{padding:clamp(3.5rem,8vw,6.5rem) 0}
.tint{background:var(--steel)}
.dark{background:var(--forge);color:#fff}
.lead{font-size:1.2rem;color:var(--muted)}
.dark .lead{color:#B9C5D9}
.page-head{background:var(--forge);color:#fff;padding:clamp(3.5rem,8vw,6rem) 0 clamp(2.5rem,5vw,4rem);position:relative;overflow:hidden}
.page-head::after{content:"";position:absolute;right:-80px;top:-80px;width:340px;height:340px;border-radius:50%;background:radial-gradient(circle,rgba(255,122,26,.35),transparent 65%)}
.page-head h1{font-size:clamp(2.2rem,5vw,3.75rem);max-width:18ch}
.page-head p{color:#B9C5D9;font-size:1.2rem}

/* ---------- Hero ---------- */
.hero{position:relative;background:var(--forge);color:#fff;overflow:hidden;padding:clamp(4rem,10vw,8rem) 0 clamp(4rem,9vw,7rem);min-height:calc(100vh - 68px);display:flex;align-items:center}
.hero canvas{position:absolute;inset:0;width:100%;height:100%;touch-action:pan-y}
.hero .wrap{position:relative;pointer-events:none}
.hero .wrap a,.hero .wrap button{pointer-events:auto}
.hero h1{max-width:13ch;animation:strike .9s cubic-bezier(.2,.8,.2,1) both}
.hero p.lead{max-width:52ch;animation:strike .9s .12s cubic-bezier(.2,.8,.2,1) both}
.hero .actions{display:flex;flex-wrap:wrap;gap:.75rem;margin-top:1.75rem;animation:strike .9s .24s cubic-bezier(.2,.8,.2,1) both}
.hero .hint{margin-top:2.5rem;font-size:.92rem;color:#8FA0BC}
@keyframes strike{from{opacity:0;transform:translateY(24px)}to{opacity:1;transform:none}}

/* ---------- Services (list rows) ---------- */
.split{display:grid;grid-template-columns:1fr 1.5fr;gap:clamp(2rem,6vw,5rem);align-items:start}
.svc{list-style:none;margin:0;padding:0}
.svc li{display:grid;grid-template-columns:3rem 1fr;gap:1rem;padding:1.5rem 0;border-top:1px solid var(--line)}
.svc li:last-child{border-bottom:1px solid var(--line)}
.svc svg{width:36px;height:36px;color:var(--cobalt)}
.svc h3{margin-bottom:.25rem}
.svc p{margin:0;color:var(--muted)}

/* ---------- Process ---------- */
.steps{display:grid;grid-template-columns:repeat(4,1fr);gap:1.25rem;counter-reset:s;margin-top:2.5rem}
.step{border-top:3px solid var(--ember);padding-top:1rem;counter-increment:s}
.step::before{content:counter(s);display:block;font:800 2.5rem var(--display);color:var(--ember);line-height:1}
.step h3{margin:.4rem 0 .35rem;color:#fff}
.step p{color:#B9C5D9;font-size:.98rem;margin:0}

/* ---------- Project visuals / rows ---------- */
.filters{display:flex;flex-wrap:wrap;gap:.5rem;margin-bottom:2.5rem}
.chip{font:500 .95rem var(--body);padding:.5rem 1.1rem;border-radius:999px;border:1.5px solid var(--line);background:var(--white);color:var(--ink);cursor:pointer}
.chip:hover{border-color:var(--cobalt)}
.chip[aria-pressed="true"]{background:var(--ink);border-color:var(--ink);color:#fff}
.proj{display:grid;grid-template-columns:1.1fr 1fr;gap:clamp(1.5rem,5vw,4rem);align-items:center;padding:2.5rem 0;border-top:1px solid var(--line)}
.proj:nth-child(even) .proj-vis{order:2}
.proj-vis{border-radius:18px;overflow:hidden;box-shadow:0 18px 40px -22px rgba(15,27,46,.55)}
.proj-vis svg{width:100%;height:auto}
.meta{display:flex;flex-wrap:wrap;gap:.4rem;margin:.75rem 0 1rem;padding:0;list-style:none}
.meta li{font-size:.85rem;background:var(--steel);border-radius:6px;padding:.2rem .6rem;color:var(--ink)}
.proj .result{border-left:3px solid var(--ember);padding-left:1rem;color:var(--ink);font-weight:500}
.proj-mini{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem}
.proj-mini article{background:var(--white);border-radius:14px;overflow:hidden;border:1px solid var(--line)}
.proj-mini .body{padding:1.1rem 1.25rem 1.4rem}
.proj-mini h3{font-size:1.15rem;margin-bottom:.3rem}
.proj-mini p{color:var(--muted);font-size:.97rem;margin:0}

/* ---------- Testimonials ---------- */
.feature-quote{background:var(--forge);color:#fff;border-radius:24px;padding:clamp(1.75rem,5vw,3.5rem);position:relative}
.feature-quote blockquote{margin:0;font:600 clamp(1.4rem,3vw,2.2rem)/1.3 var(--display);letter-spacing:-.01em;max-width:30ch}
.feature-quote .who{margin-top:1.75rem}
.who{display:flex;align-items:center;gap:.9rem}
.av{width:46px;height:46px;border-radius:50%;display:grid;place-items:center;font:700 1rem var(--display);color:#fff;flex:none}
.who strong{display:block;line-height:1.2}
.who span{font-size:.9rem;color:var(--muted)}
.feature-quote .who span{color:#B9C5D9}
.quotes{columns:3 280px;column-gap:1.5rem;margin-top:1.5rem}
.quote{break-inside:avoid;background:var(--white);border:1px solid var(--line);border-radius:6px 22px 6px 22px;padding:1.5rem;margin-bottom:1.5rem}
.quote p{margin-bottom:1.25rem}
.stars{color:var(--ember);letter-spacing:2px;margin-bottom:.5rem;font-size:1.05rem}

/* ---------- About ---------- */
.people{display:grid;grid-template-columns:1fr 1fr;gap:1.5rem}
.person{background:var(--white);border:1px solid var(--line);border-radius:20px;padding:2rem}
.person .big-av{width:84px;height:84px;border-radius:22px;display:grid;place-items:center;font:800 1.9rem var(--display);color:#fff;margin-bottom:1.25rem}
.person h3{margin-bottom:.1rem}
.person .role{color:var(--cobalt);font-weight:600;margin-bottom:1rem}
.values{display:grid;grid-template-columns:repeat(3,1fr);gap:2rem;margin-top:2rem}
.values div{border-top:3px solid var(--cobalt);padding-top:1rem}
.values p{color:var(--muted);margin:0}
.facts{display:flex;flex-wrap:wrap;gap:2.5rem 4rem;margin-top:2rem}
.facts div{min-width:120px}
.facts strong{display:block;font:800 2.4rem var(--display);color:var(--ember);line-height:1}
.facts span{color:#B9C5D9;font-size:.95rem}

/* ---------- Blog ---------- */
.posts{display:grid;gap:1.5rem;max-width:820px}
.post{background:var(--white);border:1px solid var(--line);border-radius:16px;padding:clamp(1.25rem,3vw,2rem)}
.post time{font-size:.9rem;color:var(--muted)}
.post h2{font-size:1.6rem;margin:.3rem 0 .6rem}
.post .more{display:none;margin-top:1rem}
.post.open .more{display:block}
.post .toggle{background:none;border:0;color:var(--cobalt);font:600 1rem var(--body);padding:.25rem 0;cursor:pointer;text-decoration:underline;text-underline-offset:4px}

/* ---------- Contact ---------- */
.contact-grid{display:grid;grid-template-columns:1fr 1.2fr;gap:clamp(2rem,6vw,5rem)}
.info-list{list-style:none;padding:0;margin:1.5rem 0 0}
.info-list li{padding:1rem 0;border-top:1px solid var(--line)}
.info-list strong{display:block}
form.contact{background:var(--white);border:1px solid var(--line);border-radius:20px;padding:clamp(1.25rem,3vw,2.25rem)}
.field{margin-bottom:1.15rem}
label{display:block;font-weight:600;margin-bottom:.35rem;font-size:.97rem}
input,select,textarea{width:100%;font:inherit;padding:.8rem .9rem;border:1.5px solid #B8C1CD;border-radius:10px;background:#fff;color:var(--ink)}
textarea{min-height:140px;resize:vertical}
input:focus,select:focus,textarea:focus{outline:3px solid rgba(35,64,232,.3);border-color:var(--cobalt)}
.field.bad input,.field.bad select,.field.bad textarea{border-color:#C62828}
.err{display:none;color:#B71C1C;font-size:.9rem;margin-top:.3rem}
.field.bad .err{display:block}
.ok{display:none;background:#E6F4EA;border:1px solid #9BD0A9;color:#14532D;border-radius:10px;padding:1rem 1.1rem;margin-top:1rem}
.ok.show{display:block}

/* ---------- CTA band ---------- */
.band{background:var(--cobalt);color:#fff;text-align:center}
.band p{margin-inline:auto;color:#DDE3FF}
.band .btn-primary{margin-top:.5rem}

/* ---------- Footer ---------- */
footer.site{background:#0A1322;color:#A9B6CC;padding:3.5rem 0 1.5rem;font-size:.97rem}
.fgrid{display:grid;grid-template-columns:1.6fr 1fr 1fr;gap:2.5rem}
footer h4{color:#fff;font-size:1rem;margin-bottom:.8rem}
footer ul{list-style:none;margin:0;padding:0}
footer li{margin-bottom:.4rem}
footer a{color:#A9B6CC;text-decoration:none}
footer a:hover{color:#fff;text-decoration:underline}
.copy{border-top:1px solid rgba(255,255,255,.1);margin-top:2.5rem;padding-top:1.25rem;font-size:.9rem}

/* ---------- Responsive ---------- */
@media (max-width:900px){
  .split,.contact-grid,.proj,.people{grid-template-columns:1fr}
  .proj:nth-child(even) .proj-vis{order:0}
  .steps{grid-template-columns:1fr 1fr}
  .proj-mini,.values{grid-template-columns:1fr}
  .fgrid{grid-template-columns:1fr 1fr}
  .fgrid>div:first-child{grid-column:1/-1}
}
@media (max-width:860px){
  .burger{display:block}
  .nav ul{position:absolute;left:0;right:0;top:68px;background:var(--forge);flex-direction:column;align-items:stretch;padding:.75rem 1.25rem 1.25rem;border-bottom:1px solid rgba(255,255,255,.1);display:none}
  .nav ul.open{display:flex}
  .nav a.link{display:block;padding:.85rem .5rem;border-radius:0}
  .nav a.link[aria-current="page"]{box-shadow:inset 3px 0 0 var(--ember);padding-left:.9rem}
  .nav .cta{margin:.5rem 0 0}
}
@media (max-width:560px){
  .steps{grid-template-columns:1fr}
  .fgrid{grid-template-columns:1fr}
  .hero .actions .btn{width:100%}
  .hero{min-height:auto}
}
@media (prefers-reduced-motion:reduce){
  *{animation:none!important;transition:none!important}
  html{scroll-behavior:auto}
}
</style>
</head>
<body>
<a class="skip" href="#main">Skip to content</a>

<header class="site">
  <div class="wrap nav">
    <a class="logo" href="#home" aria-label="DigitalForgePro home">
      <svg viewBox="0 0 32 32" aria-hidden="true"><path d="M16 2l12 14-12 14L4 16z" fill="#2340E8"/><path d="M16 9l6 7-6 7-6-7z" fill="#FF7A1A"/></svg>
      <span>DigitalForge<b>Pro</b></span>
    </a>
    <button class="burger" id="burger" aria-label="Open menu" aria-expanded="false" aria-controls="menu"><span></span><span></span><span></span></button>
    <ul id="menu">
      <li><a class="link" href="#home" data-nav="home">Home</a></li>
      <li><a class="link" href="#projects" data-nav="projects">Projects</a></li>
      <li><a class="link" href="#testimonials" data-nav="testimonials">Testimonials</a></li>
      <li><a class="link" href="#about" data-nav="about">About</a></li>
      <li><a class="link" href="#blog" data-nav="blog">Blog</a></li>
      <li><a class="btn btn-primary cta" href="#contact" data-nav="contact">Contact us</a></li>
    </ul>
  </div>
</header>

<main id="main" tabindex="-1">

<!-- ================= HOME ================= -->
<div class="page" id="page-home" data-title="DigitalForgePro | Software built to take a hit">
  <div class="hero">
    <canvas id="sparks" aria-hidden="true"></canvas>
    <div class="wrap">
      <h1>We forge software built to take a hit.</h1>
      <p class="lead">DigitalForgePro designs, builds and runs websites, mobile apps and cloud systems for companies that can't afford downtime.</p>
      <div class="actions">
        <a class="btn btn-primary" href="#projects">See our projects</a>
        <a class="btn btn-ghost" href="#contact">Start a project</a>
      </div>
      <p class="hint">Move your cursor or tap the screen to strike sparks.</p>
    </div>
  </div>

  <section>
    <div class="wrap split">
      <div>
        <h2>One team for the whole build</h2>
        <p class="lead">From the first sketch to the 3&nbsp;a.m. alert, the same people stay on your product.</p>
        <a class="btn btn-line" href="#about">Meet the team</a>
      </div>
      <ul class="svc">
        <li>
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><rect x="3" y="4" width="18" height="14" rx="2"/><path d="M8 21h8M12 18v3"/></svg>
          <div><h3>Websites and web apps</h3><p>Fast, accessible sites and customer portals that work on every screen size.</p></div>
        </li>
        <li>
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><rect x="7" y="2" width="10" height="20" rx="2"/><path d="M11 18h2"/></svg>
          <div><h3>Mobile apps</h3><p>iOS and Android apps with offline support, clean design and steady release cycles.</p></div>
        </li>
        <li>
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M7 18a4 4 0 010-8 5.5 5.5 0 0110.5 1.5A3.3 3.3 0 0117 18z"/></svg>
          <div><h3>Cloud and DevOps</h3><p>Automated deployments, monitoring and hosting that scales when your traffic does.</p></div>
        </li>
        <li>
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M12 3l8 3v6c0 5-3.5 8-8 9-4.5-1-8-4-8-9V6z"/><path d="M9 12l2 2 4-4"/></svg>
          <div><h3>Security and maintenance</h3><p>Audits, updates and support plans so your software stays safe after launch.</p></div>
        </li>
      </ul>
    </div>
  </section>

  <section class="dark">
    <div class="wrap">
      <h2>How we work</h2>
      <p class="lead">Named after the forge, because good software gets shaped in stages.</p>
      <div class="steps">
        <div class="step"><h3>Heat</h3><p>We learn your goals, users and limits in a short discovery workshop.</p></div>
        <div class="step"><h3>Shape</h3><p>Designs and a clickable prototype take form. You review before we build.</p></div>
        <div class="step"><h3>Temper</h3><p>We build in two-week cycles, testing each release for speed and security.</p></div>
        <div class="step"><h3>Ship</h3><p>We launch, monitor and keep improving with a dedicated support plan.</p></div>
      </div>
    </div>
  </section>

  <section>
    <div class="wrap">
      <h2>Recent work</h2>
      <div class="proj-mini" id="home-projects"></div>
      <p style="margin-top:2rem"><a class="btn btn-line" href="#projects">View all projects</a></p>
    </div>
  </section>

  <section class="band">
    <div class="wrap">
      <h2>Have something to build?</h2>
      <p class="lead">Tell us what you need. We reply within one business day.</p>
      <a class="btn btn-primary" href="#contact">Contact us</a>
    </div>
  </section>
</div>

<!-- ================= PROJECTS ================= -->
<div class="page" id="page-projects" data-title="Projects | DigitalForgePro">
  <div class="page-head"><div class="wrap">
    <h1>Projects we've shipped</h1>
    <p>A selection of web, mobile and cloud work for clients in logistics, finance, retail, health and education.</p>
  </div></div>
  <section>
    <div class="wrap">
      <div class="filters" role="group" aria-label="Filter projects by type">
        <button class="chip" data-f="all" aria-pressed="true">All</button>
        <button class="chip" data-f="Web" aria-pressed="false">Web</button>
        <button class="chip" data-f="Mobile" aria-pressed="false">Mobile</button>
        <button class="chip" data-f="E-commerce" aria-pressed="false">E-commerce</button>
        <button class="chip" data-f="Cloud" aria-pressed="false">Cloud</button>
      </div>
      <div id="project-list"></div>
    </div>
  </section>
</div>

<!-- ================= TESTIMONIALS ================= -->
<div class="page" id="page-testimonials" data-title="Testimonials | DigitalForgePro">
  <div class="page-head"><div class="wrap">
    <h1>What our clients say</h1>
    <p>We measure success by how our clients' businesses grow after launch.</p>
  </div></div>
  <section>
    <div class="wrap">
      <div class="feature-quote" id="feature-quote"></div>
      <div class="quotes" id="quote-grid"></div>
    </div>
  </section>
  <section class="band">
    <div class="wrap">
      <h2>Join our list of happy clients</h2>
      <a class="btn btn-primary" href="#contact">Start your project</a>
    </div>
  </section>
</div>

<!-- ================= ABOUT ================= -->
<div class="page" id="page-about" data-title="About | DigitalForgePro">
  <div class="page-head"><div class="wrap">
    <h1>A small team with a forge mindset</h1>
    <p>We started DigitalForgePro to give growing companies the same engineering quality that large firms keep for themselves.</p>
  </div></div>

  <section>
    <div class="wrap split">
      <div>
        <h2>Our story</h2>
      </div>
      <div>
        <p class="lead">DigitalForgePro began with a simple frustration: too many good businesses were stuck with slow, fragile software built by agencies that disappeared after launch.</p>
        <p>We do it differently. We keep our team small, our code clean and our promises specific. Every project has a named lead, a clear schedule and a plan for life after launch.</p>
        <p>Today we build and support websites, apps and cloud platforms for clients across several industries, and our online home is <strong>digitalforgepro.online</strong>.</p>
      </div>
    </div>
  </section>

  <section class="tint">
    <div class="wrap">
      <h2>Leadership</h2>
      <div class="people">
        <article class="person">
          <div class="big-av" style="background:var(--cobalt)" aria-hidden="true">AP</div>
          <h3>Andrew Parker</h3>
          <p class="role">Chief Executive Officer</p>
          <p>Andrew founded DigitalForgePro and sets the company's direction. A software engineer by training, he stays close to architecture decisions and personally reviews every client proposal.</p>
        </article>
        <article class="person">
          <div class="big-av" style="background:var(--ember);color:#1a0d00" aria-hidden="true">DW</div>
          <h3>Daniel Wilson</h3>
          <p class="role">Manager</p>
          <p>Daniel runs delivery. He keeps schedules honest, budgets clear and communication steady, so every client knows what is happening and what comes next.</p>
        </article>
      </div>
    </div>
  </section>

  <section>
    <div class="wrap">
      <h2>What we stand for</h2>
      <div class="values">
        <div><h3>Plain talk</h3><p>No jargon and no surprise invoices. You always know where your project stands.</p></div>
        <div><h3>Built to last</h3><p>We write code the next developer can read, and we document what we build.</p></div>
        <div><h3>We stay</h3><p>Launch is the start of the relationship. Every project includes a support plan.</p></div>
      </div>
    </div>
  </section>

  <section class="dark">
    <div class="wrap">
      <h2>DigitalForgePro at a glance</h2>
      <div class="facts">
        <div><strong>60+</strong><span>Projects delivered</span></div>
        <div><strong>12</strong><span>Specialists on the team</span></div>
        <div><strong>98%</strong><span>Clients who return</span></div>
        <div><strong>24/7</strong><span>Monitoring on support plans</span></div>
      </div>
    </div>
  </section>
</div>

<!-- ================= BLOG ================= -->
<div class="page" id="page-blog" data-title="Blog | DigitalForgePro">
  <div class="page-head"><div class="wrap">
    <h1>Notes from the forge</h1>
    <p>Short, practical writing from the DigitalForgePro team.</p>
  </div></div>
  <section>
    <div class="wrap"><div class="posts" id="posts"></div></div>
  </section>
</div>

<!-- ================= CONTACT ================= -->
<div class="page" id="page-contact" data-title="Contact | DigitalForgePro">
  <div class="page-head"><div class="wrap">
    <h1>Let's build something solid</h1>
    <p>Share a few details and we'll reply within one business day.</p>
  </div></div>
  <section>
    <div class="wrap contact-grid">
      <div>
        <h2>Talk to us</h2>
        <p>Whether you have a full brief or only an idea, we're happy to help you shape it.</p>
        <ul class="info-list">
          <li><strong>Email</strong><a href="mailto:hello@digitalforgepro.online">hello@digitalforgepro.online</a></li>
          <li><strong>Website</strong>digitalforgepro.online</li>
          <li><strong>Chief Executive Officer</strong>Andrew Parker</li>
          <li><strong>Manager</strong>Daniel Wilson</li>
          <li><strong>Hours</strong>Monday to Friday, 9:00 to 17:00</li>
        </ul>
      </div>
      <form class="contact" id="contact-form" novalidate>
        <div class="field">
          <label for="name">Your name</label>
          <input id="name" name="name" type="text" autocomplete="name" required>
          <div class="err">Enter your name.</div>
        </div>
        <div class="field">
          <label for="email">Email address</label>
          <input id="email" name="email" type="email" autocomplete="email" required>
          <div class="err">Enter a valid email address, like name@company.com.</div>
        </div>
        <div class="field">
          <label for="type">What do you need?</label>
          <select id="type" name="type" required>
            <option value="">Choose one</option>
            <option>Website or web app</option>
            <option>Mobile app</option>
            <option>Cloud and DevOps</option>
            <option>Security or maintenance</option>
            <option>Something else</option>
          </select>
          <div class="err">Choose the type of project.</div>
        </div>
        <div class="field">
          <label for="message">Project details</label>
          <textarea id="message" name="message" required></textarea>
          <div class="err">Tell us a little about your project (at least 15 characters).</div>
        </div>
        <button class="btn btn-blue" type="submit">Send message</button>
        <div class="ok" id="ok" role="status"></div>
      </form>
    </div>
  </section>
</div>

</main>

<footer class="site">
  <div class="wrap">
    <div class="fgrid">
      <div>
        <a class="logo" href="#home"><svg viewBox="0 0 32 32" aria-hidden="true"><path d="M16 2l12 14-12 14L4 16z" fill="#2340E8"/><path d="M16 9l6 7-6 7-6-7z" fill="#FF7A1A"/></svg><span>DigitalForge<b>Pro</b></span></a>
        <p style="margin-top:1rem;max-width:36ch">Websites, apps and cloud systems built to last. Led by CEO Andrew Parker and Manager Daniel Wilson.</p>
      </div>
      <div>
        <h4>Pages</h4>
        <ul>
          <li><a href="#home">Home</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#testimonials">Testimonials</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#blog">Blog</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </div>
      <div>
        <h4>Get in touch</h4>
        <ul>
          <li><a href="mailto:hello@digitalforgepro.online">hello@digitalforgepro.online</a></li>
          <li>digitalforgepro.online</li>
        </ul>
      </div>
    </div>
    <div class="copy">&copy; <span id="yr">2026</span> DigitalForgePro. All rights reserved.</div>
  </div>
</footer>

<script>
/* ================= DATA ================= */
const projects = [
  {id:1,title:"Harbor Freight Tracker",client:"Northline Logistics",cat:"Web",tags:["React","Node.js","Maps API"],color:"#2340E8",kind:"dash",
   text:"A live dashboard that shows every shipment on a map, flags delays and sends customers automatic updates.",
   result:"Support calls about delivery status dropped by more than a third."},
  {id:2,title:"Mint & Ledger",client:"Mint Ledger Finance",cat:"Mobile",tags:["iOS","Android","React Native"],color:"#0E8F6E",kind:"phone",
   text:"A budgeting app that links to bank accounts, sorts spending automatically and sets savings goals.",
   result:"Reached 40,000 active users within the first six months."},
  {id:3,title:"Bloom Basket",client:"Bloom Basket Florals",cat:"E-commerce",tags:["Shopify","Custom theme","Payments"],color:"#C2367A",kind:"shop",
   text:"A fast online store for a flower delivery business, with same-day delivery slots and subscription bouquets.",
   result:"Online orders doubled during the first holiday season."},
  {id:4,title:"ClinicFlow",client:"Greenfield Health Group",cat:"Web",tags:["Next.js","PostgreSQL","Secure login"],color:"#0F7C9B",kind:"dash",
   text:"A booking and reminders platform for a group of clinics that cut missed appointments and front-desk workload.",
   result:"Missed appointments fell by 28% in the first quarter."},
  {id:5,title:"Pulse Sensor Cloud",client:"Aerowatt Energy",cat:"Cloud",tags:["AWS","IoT","Terraform"],color:"#6B3FD4",kind:"cloud",
   text:"A cloud platform that collects data from thousands of sensors and alerts engineers the moment readings drift.",
   result:"Handles 5 million readings a day with 99.95% uptime."},
  {id:6,title:"Atlas Learn",client:"Atlas Academy",cat:"Mobile",tags:["Flutter","Video","Offline mode"],color:"#D9541E",kind:"phone",
   text:"A learning app with video lessons, quizzes and offline downloads for students on slow connections.",
   result:"Course completion rates rose from 41% to 67%."}
];

const testimonials = [
  {n:"Sarah Mitchell",r:"Operations Director, Northline Logistics",c:"#2340E8",q:"DigitalForgePro replaced a tangle of spreadsheets with a tracker our whole team uses every day. They delivered on the date they promised."},
  {n:"James Okafor",r:"Founder, Mint Ledger Finance",c:"#0E8F6E",q:"Andrew and his team understood our product better than some of our own staff. The app launched smoothly and our users love it."},
  {n:"Priya Nair",r:"Owner, Bloom Basket Florals",c:"#C2367A",q:"Our old site crashed every Valentine's Day. This year it didn't even slow down, and sales hit a record."},
  {n:"Marcus Lindqvist",r:"CTO, Aerowatt Energy",c:"#6B3FD4",q:"Their cloud engineers are the real thing. Clear documentation, sensible architecture and no drama."},
  {n:"Elena Rossi",r:"Head of Digital, Atlas Academy",c:"#D9541E",q:"Daniel kept us informed at every step. We never had to chase an update, which is rare with software projects."},
  {n:"Dr. Thomas Reid",r:"Medical Director, Greenfield Health Group",c:"#0F7C9B",q:"Patients can now book in under a minute, and our reception team finally has time to focus on people instead of phones."}
];

const posts = [
  {id:"p1",date:"October 6, 2026",author:"Andrew Parker",title:"Five signs your website is costing you customers",
   intro:"Most slow, confusing sites never get a complaint. Visitors simply leave.",
   more:["Start with speed. If your page takes more than three seconds to show something useful on a phone, a large share of visitors are already gone. Compressing images and removing unused scripts usually gives the biggest win.","Next, check your mobile layout on a real phone, not just a resized browser window. Tiny buttons, text that needs zooming and forms that are painful to fill are all silent conversion killers.","Finally, look at your contact path. If a visitor needs more than two clicks to reach you, simplify it. A clear button and a short form beat a long menu every time."]},
  {id:"p2",date:"September 22, 2026",author:"Daniel Wilson",title:"How to brief a software team without writing a 50-page document",
   intro:"A good brief fits on one page. Here is what that page should say.",
   more:["Describe the problem, not the solution. Tell us who is struggling, what they do today and what would make it better. We'll propose the solution together.","Name your limits early: budget range, target launch date and any systems we must connect to. These details shape the plan more than any feature list.","Finally, tell us how you'll judge success. Faster checkouts, fewer support tickets, more bookings: one clear number gives the whole team something to aim at."]},
  {id:"p3",date:"September 9, 2026",author:"Andrew Parker",title:"Why launch day is only the beginning",
   intro:"Software ages the moment it goes live. Plan for that from the start.",
   more:["Libraries need updates, browsers change and customers ask for things you hadn't thought of. A product with no maintenance plan slowly becomes a liability.","We recommend setting aside a small monthly budget for updates, monitoring and improvements. It costs far less than a rebuild two years later.","That's why every DigitalForgePro project ends with a support plan, not just a handover."]}
];

/* ================= HELPERS ================= */
const $ = (s,el=document)=>el.querySelector(s);
const $$ = (s,el=document)=>[...el.querySelectorAll(s)];
const initials = n=>n.split(" ").map(w=>w[0]).slice(0,2).join("");

function visual(kind,color){
  const bg=color+"22";
  const w='<rect width="480" height="320" fill="'+bg+'"/>';
  let s='';
  if(kind==="dash"){
    s=w+'<rect x="40" y="36" width="400" height="248" rx="12" fill="#fff"/><rect x="40" y="36" width="400" height="30" rx="12" fill="'+color+'"/>'+
      '<rect x="58" y="84" width="84" height="54" rx="8" fill="'+color+'22"/><rect x="154" y="84" width="84" height="54" rx="8" fill="'+color+'22"/><rect x="250" y="84" width="84" height="54" rx="8" fill="'+color+'22"/><rect x="346" y="84" width="76" height="54" rx="8" fill="'+color+'22"/>'+
      [0,1,2,3,4,5,6].map(i=>'<rect x="'+(66+i*34)+'" y="'+(262-[40,70,55,95,80,110,90][i])+'" width="20" height="'+[40,70,55,95,80,110,90][i]+'" rx="4" fill="'+color+'"/>').join('')+
      '<circle cx="380" cy="215" r="38" fill="none" stroke="'+color+'33" stroke-width="14"/><path d="M380 177a38 38 0 0 1 33 57" fill="none" stroke="#FF7A1A" stroke-width="14" stroke-linecap="round"/>';
  }else if(kind==="phone"){
    s=w+'<rect x="165" y="20" width="150" height="285" rx="26" fill="#16202D"/><rect x="173" y="32" width="134" height="261" rx="18" fill="#fff"/>'+
      '<rect x="185" y="48" width="70" height="10" rx="5" fill="'+color+'"/><rect x="185" y="70" width="110" height="64" rx="12" fill="'+color+'"/>'+
      [0,1,2,3].map(i=>'<rect x="185" y="'+(148+i*34)+'" width="26" height="26" rx="8" fill="'+color+'33"/><rect x="220" y="'+(150+i*34)+'" width="75" height="8" rx="4" fill="#C9D0DA"/><rect x="220" y="'+(164+i*34)+'" width="45" height="6" rx="3" fill="#E1E5EB"/>').join('')+
      '<circle cx="95" cy="90" r="30" fill="#FF7A1A" opacity=".85"/><circle cx="395" cy="230" r="44" fill="'+color+'" opacity=".35"/>';
  }else if(kind==="shop"){
    s=w+'<rect x="36" y="30" width="408" height="260" rx="12" fill="#fff"/><rect x="36" y="30" width="408" height="30" rx="12" fill="'+color+'"/>'+
      [0,1,2].map(i=>'<rect x="'+(54+i*128)+'" y="80" width="112" height="100" rx="10" fill="'+color+'2b"/><circle cx="'+(110+i*128)+'" cy="128" r="'+(22+i*4)+'" fill="'+color+'"/><rect x="'+(54+i*128)+'" y="194" width="80" height="8" rx="4" fill="#C9D0DA"/><rect x="'+(54+i*128)+'" y="210" width="40" height="8" rx="4" fill="'+color+'"/>').join('')+
      '<rect x="54" y="244" width="130" height="30" rx="15" fill="#FF7A1A"/>';
  }else{
    s=w+'<circle cx="240" cy="160" r="46" fill="'+color+'"/><path d="M224 160h32M240 144v32" stroke="#fff" stroke-width="6" stroke-linecap="round"/>'+
      [[90,70],[390,70],[80,250],[400,250],[240,40],[240,285]].map(p=>'<line x1="240" y1="160" x2="'+p[0]+'" y2="'+p[1]+'" stroke="'+color+'55" stroke-width="3" stroke-dasharray="6 6"/><circle cx="'+p[0]+'" cy="'+p[1]+'" r="20" fill="#fff" stroke="'+color+'" stroke-width="4"/><circle cx="'+p[0]+'" cy="'+p[1]+'" r="6" fill="#FF7A1A"/>').join('');
  }
  return '<svg viewBox="0 0 480 320" role="img" aria-label="Preview illustration of the project" xmlns="http://www.w3.org/2000/svg">'+s+'</svg>';
}

/* ================= RENDER ================= */
function renderProjects(filter="all"){
  const list = projects.filter(p=>filter==="all"||p.cat===filter);
  $("#project-list").innerHTML = list.map(p=>`
    <article class="proj">
      <div class="proj-vis">${visual(p.kind,p.color)}</div>
      <div>
        <h2 style="font-size:clamp(1.5rem,3vw,2.1rem)">${p.title}</h2>
        <p style="color:var(--muted);margin-bottom:0">Client: ${p.client}</p>
        <ul class="meta"><li>${p.cat}</li>${p.tags.map(t=>`<li>${t}</li>`).join("")}</ul>
        <p>${p.text}</p>
        <p class="result">${p.result}</p>
      </div>
    </article>`).join("");
}
function renderHomeProjects(){
  $("#home-projects").innerHTML = projects.slice(0,3).map(p=>`
    <article>${visual(p.kind,p.color)}
      <div class="body"><h3>${p.title}</h3><p>${p.cat} project for ${p.client}</p></div>
    </article>`).join("");
}
function renderTestimonials(){
  const f=testimonials[0];
  $("#feature-quote").innerHTML = `<blockquote>&ldquo;${f.q}&rdquo;</blockquote>
    <div class="who"><div class="av" style="background:${f.c}" aria-hidden="true">${initials(f.n)}</div><div><strong>${f.n}</strong><span>${f.r}</span></div></div>`;
  $("#quote-grid").innerHTML = testimonials.slice(1).map(t=>`
    <figure class="quote" style="margin-inline:0">
      <div class="stars" aria-label="5 out of 5 stars">&#9733;&#9733;&#9733;&#9733;&#9733;</div>
      <p>&ldquo;${t.q}&rdquo;</p>
      <figcaption class="who"><div class="av" style="background:${t.c}" aria-hidden="true">${initials(t.n)}</div><div><strong>${t.n}</strong><span>${t.r}</span></div></figcaption>
    </figure>`).join("");
}
function renderPosts(){
  $("#posts").innerHTML = posts.map(p=>`
    <article class="post" id="${p.id}">
      <time>${p.date} &middot; by ${p.author}</time>
      <h2>${p.title}</h2>
      <p>${p.intro}</p>
      <div class="more" id="${p.id}-more">${p.more.map(m=>`<p>${m}</p>`).join("")}</div>
      <button class="toggle" aria-expanded="false" aria-controls="${p.id}-more">Read more</button>
    </article>`).join("");
  $$(".post .toggle").forEach(b=>b.addEventListener("click",()=>{
    const post=b.closest(".post"), open=post.classList.toggle("open");
    b.setAttribute("aria-expanded",open); b.textContent=open?"Show less":"Read more";
  }));
}

/* ================= ROUTER ================= */
const valid=["home","projects","testimonials","about","blog","contact"];
function route(){
  let page=(location.hash||"#home").slice(1);
  if(!valid.includes(page)) page="home";
  $$(".page").forEach(p=>p.classList.toggle("active",p.id==="page-"+page));
  $$("[data-nav]").forEach(a=>{ a.dataset.nav===page ? a.setAttribute("aria-current","page") : a.removeAttribute("aria-current"); });
  document.title=$("#page-"+page).dataset.title;
  menu.classList.remove("open"); burger.setAttribute("aria-expanded","false"); burger.setAttribute("aria-label","Open menu");
  window.scrollTo({top:0,behavior:"instant"});
  page==="home"?sparks.start():sparks.stop();
}

/* ================= NAV ================= */
const burger=$("#burger"), menu=$("#menu");
burger.addEventListener("click",()=>{
  const o=menu.classList.toggle("open");
  burger.setAttribute("aria-expanded",o);
  burger.setAttribute("aria-label",o?"Close menu":"Open menu");
});
document.addEventListener("keydown",e=>{ if(e.key==="Escape"&&menu.classList.contains("open")){menu.classList.remove("open");burger.setAttribute("aria-expanded","false");burger.focus();} });

/* ================= PROJECT FILTER ================= */
$$(".chip").forEach(c=>c.addEventListener("click",()=>{
  $$(".chip").forEach(x=>x.setAttribute("aria-pressed",x===c));
  renderProjects(c.dataset.f);
}));

/* ================= CONTACT FORM ================= */
const form=$("#contact-form");
function setBad(id,bad){ $("#"+id).closest(".field").classList.toggle("bad",bad); return !bad; }
form.addEventListener("submit",e=>{
  e.preventDefault();
  const v={name:$("#name").value.trim(),email:$("#email").value.trim(),type:$("#type").value,msg:$("#message").value.trim()};
  const checks=[
    setBad("name",v.name.length<2),
    setBad("email",!/^[^\s@]+@[^\s@]+\.[^\s@]{2,}$/.test(v.email)),
    setBad("type",!v.type),
    setBad("message",v.msg.length<15)
  ];
  if(checks.includes(false)){ const first=$(".field.bad input, .field.bad select, .field.bad textarea"); first&&first.focus(); return; }
  /* TODO: send to a real backend or form service (e.g. Formspree, Netlify Forms, your own API). */
  const ok=$("#ok");
  ok.textContent=`Thanks, ${v.name.split(" ")[0]}. We received your message and will reply to ${v.email} within one business day.`;
  ok.classList.add("show"); form.reset();
});
$$("#contact-form input,#contact-form select,#contact-form textarea").forEach(el=>el.addEventListener("input",()=>el.closest(".field").classList.remove("bad")));

/* ================= SPARKS (hero) ================= */
const sparks=(()=>{
  const cv=$("#sparks"), ctx=cv.getContext("2d");
  const reduce=matchMedia("(prefers-reduced-motion: reduce)").matches;
  let W=0,H=0,dpr=1,parts=[],raf=null,last=0,ambient=0,running=false;
  function size(){
    const r=cv.getBoundingClientRect(); dpr=Math.min(devicePixelRatio||1,2);
    W=r.width;H=r.height; cv.width=W*dpr; cv.height=H*dpr; ctx.setTransform(dpr,0,0,dpr,0,0);
  }
  function burst(x,y,n,power=1){
    for(let i=0;i<n;i++){
      const a=-Math.PI/2+(Math.random()-.5)*2.4, s=(1.5+Math.random()*5)*power;
      parts.push({x,y,vx:Math.cos(a)*s,vy:Math.sin(a)*s,life:1,decay:.008+Math.random()*.014,r:1+Math.random()*2});
    }
    if(parts.length>600) parts.splice(0,parts.length-600);
  }
  function frame(t){
    if(!running) return;
    const dt=Math.min((t-last)/16.7,3)||1; last=t;
    ctx.clearRect(0,0,W,H);
    ambient-=dt;
    if(ambient<=0 && !reduce){ burst(W*(W>700?.78:.5),H*.82,26,1.2); ambient=70+Math.random()*60; }
    for(let i=parts.length-1;i>=0;i--){
      const p=parts[i];
      p.vy+=.12*dt; p.x+=p.vx*dt; p.y+=p.vy*dt; p.life-=p.decay*dt;
      if(p.life<=0||p.y>H+10){parts.splice(i,1);continue;}
      const g=ctx.createRadialGradient(p.x,p.y,0,p.x,p.y,p.r*5);
      g.addColorStop(0,`rgba(255,${Math.round(150+p.life*80)},${Math.round(40+p.life*90)},${p.life})`);
      g.addColorStop(1,"rgba(255,122,26,0)");
      ctx.fillStyle=g; ctx.beginPath(); ctx.arc(p.x,p.y,p.r*5,0,6.283); ctx.fill();
    }
    raf=requestAnimationFrame(frame);
  }
  function pos(e){const r=cv.getBoundingClientRect();return [e.clientX-r.left,e.clientY-r.top];}
  let lastMove=0;
  cv.addEventListener("pointermove",e=>{ if(reduce)return; const n=performance.now(); if(n-lastMove<40)return; lastMove=n; const [x,y]=pos(e); burst(x,y,3,.6); });
  cv.addEventListener("pointerdown",e=>{ const [x,y]=pos(e); burst(x,y,40,1.3); if(reduce&&!running){frame(performance.now());setTimeout(()=>{running=false;},1500);running=true;} });
  addEventListener("resize",size);
  return{
    start(){ if(running)return; size(); running=true; last=performance.now(); raf=requestAnimationFrame(frame); },
    stop(){ running=false; cancelAnimationFrame(raf); parts=[]; }
  };
})();

/* ================= INIT ================= */
$("#yr").textContent=new Date().getFullYear();
renderProjects(); renderHomeProjects(); renderTestimonials(); renderPosts();
addEventListener("hashchange",route);
route();
</script>
</body>
</html>

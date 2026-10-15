# My-JavaScript-code-

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>DigitalForgePro | Custom software, built and managed</title>
  <meta name="description" content="DigitalForgePro builds custom web apps, mobile apps and cloud platforms, then hosts, monitors and maintains them.">
  <meta name="theme-color" content="#0e2a3b">
  <link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Crect width='32' height='32' rx='8' fill='%2312202b'/%3E%3Cpath d='M9 7h14v4H13v4h8v4h-8v6H9z' fill='%23fff'/%3E%3Crect x='19' y='21' width='4' height='4' fill='%23ff7a4d'/%3E%3C/svg%3E">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,500;12..96,700;12..96,800&family=IBM+Plex+Mono:wght@400;500&family=Public+Sans:wght@400;500;600&display=swap" rel="stylesheet">
  <style>
/* DigitalForgePro v2
   Palette: slate paper, ink, quench (deep blue-teal), ember (accent), gold, mint, sky */
:root {
  --paper: #eef2f5;
  --surface: #ffffff;
  --ink: #12202b;
  --steel: #4a5a67;
  --line: #cfd8de;
  --ember: #c93a12;
  --ember-dark: #a62d0a;
  --ember-bright: #ff7a4d;
  --gold: #f4b942;
  --mint: #5fd1a8;
  --sky: #7cc4f5;
  --quench: #0e2a3b;
  --quench-2: #163d55;
  --error: #b3261e;
  --display: "Bricolage Grotesque", "Public Sans", system-ui, sans-serif;
  --body: "Public Sans", system-ui, -apple-system, "Segoe UI", sans-serif;
  --mono: "IBM Plex Mono", ui-monospace, "SFMono-Regular", Menlo, monospace;
  --shadow: 0 1px 2px rgba(14, 42, 59, 0.06), 0 14px 32px -14px rgba(14, 42, 59, 0.25);
}

*, *::before, *::after { box-sizing: border-box; }
html { scroll-behavior: smooth; }
body { margin: 0; background: var(--paper); color: var(--ink); font: 400 1.0625rem/1.65 var(--body); -webkit-font-smoothing: antialiased; }
h1, h2, h3, h4 { font-family: var(--display); font-weight: 700; line-height: 1.08; letter-spacing: -0.02em; margin: 0 0 0.5em; }
h1 { font-size: clamp(2.5rem, 6vw, 4.8rem); letter-spacing: -0.035em; font-weight: 800; }
h2 { font-size: clamp(1.9rem, 3.8vw, 3rem); }
h3 { font-size: 1.3rem; letter-spacing: -0.01em; }
p { margin: 0 0 1em; max-width: 62ch; }
a { color: inherit; }
svg, img { display: block; max-width: 100%; }
ul, ol { margin: 0; padding: 0; list-style: none; }
:focus-visible { outline: 3px solid var(--ember); outline-offset: 3px; }

.skip { position: absolute; left: 1rem; top: -4rem; z-index: 100; background: var(--ink); color: #fff; padding: 0.6rem 1rem; border-radius: 6px; }
.skip:focus { top: 1rem; }
.wrap { width: min(1180px, 100% - 2.5rem); margin-inline: auto; }
.section { padding: clamp(3.5rem, 8vw, 6.5rem) 0; }
.section-white { background: var(--surface); }
.section-head { max-width: 46rem; margin-bottom: 2.75rem; }
.lede { font-size: 1.2rem; color: var(--steel); max-width: 56ch; }
.page[hidden] { display: none; }

/* Dark sections: deep blue-teal with warm and cool glows plus a dot grid */
.dark {
  position: relative; isolation: isolate; color: #fff;
  background:
    radial-gradient(52rem 28rem at 88% -10%, rgba(61, 139, 217, 0.38), transparent 62%),
    radial-gradient(38rem 24rem at -6% 112%, rgba(255, 122, 77, 0.3), transparent 62%),
    var(--quench);
}
.dark::before {
  content: ""; position: absolute; inset: 0; z-index: -1; pointer-events: none;
  background-image: radial-gradient(rgba(255, 255, 255, 0.13) 1px, transparent 1.3px);
  background-size: 26px 26px;
  -webkit-mask-image: linear-gradient(180deg, #000, transparent 90%);
  mask-image: linear-gradient(180deg, #000, transparent 90%);
}
.dark .lede, .dark p { color: #c9d8e2; }
.dark h1, .dark h2, .dark h3 { color: #fff; }

/* Buttons */
.btn { display: inline-flex; align-items: center; justify-content: center; padding: 0.85rem 1.5rem; border-radius: 8px; font: 600 1rem/1.2 var(--body); text-decoration: none; border: 2px solid transparent; cursor: pointer; transition: background-color 0.15s, color 0.15s, border-color 0.15s, transform 0.15s; }
.btn:active { transform: translateY(1px); }
.btn-primary { background: var(--ember); color: #fff; box-shadow: 0 10px 22px -10px rgba(201, 58, 18, 0.8); }
.btn-primary:hover { background: var(--ember-dark); }
.btn-ghost { border-color: var(--ink); color: var(--ink); background: transparent; }
.btn-ghost:hover { background: var(--ink); color: #fff; }
.dark .btn-ghost, .on-dark .btn-ghost { border-color: rgba(255, 255, 255, 0.7); color: #fff; }
.dark .btn-ghost:hover, .on-dark .btn-ghost:hover { background: #fff; color: var(--ink); }
.btn-small { padding: 0.55rem 1rem; font-size: 0.95rem; }
.btn-row { display: flex; flex-wrap: wrap; gap: 0.9rem; margin-top: 1.75rem; }
.text-link { font-weight: 600; text-decoration-thickness: 2px; text-underline-offset: 4px; text-decoration-color: var(--ember); }
.text-link:hover { color: var(--ember); }

/* Header */
.site-header { position: sticky; top: 0; z-index: 50; background: rgba(238, 242, 245, 0.92); -webkit-backdrop-filter: blur(10px); backdrop-filter: blur(10px); border-bottom: 1px solid transparent; transition: border-color 0.2s; }
.site-header.scrolled { border-bottom-color: var(--line); }
.header-inner { display: flex; align-items: center; justify-content: space-between; gap: 1.5rem; min-height: 4.5rem; }
.brand { display: inline-flex; align-items: center; gap: 0.65rem; text-decoration: none; font: 700 1.3rem/1 var(--display); letter-spacing: -0.02em; }
.brand svg { width: 2.1rem; height: 2.1rem; }
.brand span { font-weight: 500; color: var(--steel); }
.nav { display: flex; align-items: center; gap: 2rem; }
.nav-links { display: flex; gap: clamp(1rem, 1.7vw, 1.75rem); }
.nav-links a { text-decoration: none; font-weight: 500; padding: 0.4rem 0; border-bottom: 2px solid transparent; }
.nav-links a:hover { border-bottom-color: var(--line); }
.nav-links a[aria-current="page"] { border-bottom-color: var(--ember); font-weight: 600; }
.nav-toggle { display: none; background: none; border: 2px solid var(--ink); border-radius: 8px; padding: 0.5rem 0.8rem; font: 600 0.95rem var(--body); color: var(--ink); cursor: pointer; }

/* Hero */
.hero { padding: clamp(3rem, 6vw, 5rem) 0 clamp(3.5rem, 7vw, 6rem); }
.hero-grid { display: grid; grid-template-columns: 1fr 1.05fr; gap: clamp(2rem, 4vw, 3.5rem); align-items: center; }
.hero h1 { margin-bottom: 0.4em; }
.hero-note { margin-top: 1.5rem; font-size: 0.95rem; color: #9db6c6; }
.hero-art { position: relative; padding-bottom: 3.5rem; }
.hero-art .art-main { width: 100%; height: auto; }
.chip { position: absolute; right: 0; top: 0.5rem; display: flex; align-items: center; gap: 0.65rem; background: #fff; color: var(--ink); border-radius: 14px; padding: 0.65rem 1rem; font-size: 0.92rem; font-weight: 600; box-shadow: 0 18px 30px -14px rgba(0, 0, 0, 0.5); }
.chip i { width: 0.65rem; height: 0.65rem; border-radius: 50%; background: #1faa72; box-shadow: 0 0 0 4px rgba(31, 170, 114, 0.2); }
.log { background: #0a1e2b; color: #d3e0e8; border: 1px solid rgba(255, 255, 255, 0.14); border-radius: 14px; font: 400 0.84rem/1.7 var(--mono); box-shadow: 0 26px 46px -18px rgba(0, 0, 0, 0.65); }
.log-card { position: absolute; left: -1.5rem; bottom: 0; width: min(21.5rem, 78%); }
.log-bar { display: flex; justify-content: space-between; align-items: center; padding: 0.55rem 0.9rem; border-bottom: 1px solid rgba(255, 255, 255, 0.12); font-size: 0.74rem; color: #93abba; }
.log-replay { background: none; border: 1px solid rgba(255, 255, 255, 0.3); color: #d3e0e8; border-radius: 5px; padding: 0.1rem 0.55rem; font: 500 0.72rem var(--mono); cursor: pointer; }
.log-replay:hover { background: rgba(255, 255, 255, 0.12); }
.log-body { padding: 0.8rem 0.95rem 1rem; }
.log-line { display: flex; gap: 0.6rem; transition: opacity 0.25s, transform 0.25s; }
.log-line.pending { opacity: 0; transform: translateY(5px); }
.log-line .ok { color: #6fe3a5; }
.log-line .cmd { color: var(--ember-bright); }
.log-line.final { color: #fff; font-weight: 600; margin-top: 0.4rem; }
@keyframes rise { from { opacity: 0; transform: translateY(22px); } to { opacity: 1; transform: none; } }
.hero-art .art-main { animation: rise 0.9s cubic-bezier(0.2, 0.7, 0.2, 1) both; }
.hero-art .log-card { animation: rise 0.9s 0.25s cubic-bezier(0.2, 0.7, 0.2, 1) both; }
.hero-art .chip { animation: rise 0.9s 0.45s cubic-bezier(0.2, 0.7, 0.2, 1) both; }

/* Trusted row */
.trusted-band { background: var(--surface); border-bottom: 1px solid var(--line); }
.trusted { display: flex; flex-wrap: wrap; align-items: center; justify-content: space-between; gap: 1rem 2.5rem; padding: 1.7rem 0; }
.trusted p { margin: 0; font-size: 0.95rem; color: var(--steel); max-width: 16rem; }
.trusted ul { display: flex; flex-wrap: wrap; gap: 0.8rem 2.5rem; align-items: center; }
.trusted li { font: 700 1.25rem var(--display); color: #7a8995; letter-spacing: -0.02em; }
.trusted li:nth-child(2) { font-style: italic; font-weight: 500; }
.trusted li:nth-child(3) { letter-spacing: 0.02em; font-weight: 500; }
.trusted li:nth-child(5) { font-weight: 800; letter-spacing: -0.05em; }

/* Service panels */
.panels { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; }
.panel { border-radius: 22px; padding: clamp(1.6rem, 3vw, 2.4rem); }
.panel-light { background: var(--surface); border: 1px solid var(--line); box-shadow: var(--shadow); }
.panel-dark { background: linear-gradient(160deg, var(--quench-2), var(--quench)); color: #fff; box-shadow: var(--shadow); }
.panel-dark p, .panel-dark .icon-row span { color: #c9d8e2; }
.panel h3 { font-size: 1.7rem; }
.icon-row { display: flex; gap: 1rem; padding: 1rem 0; border-top: 1px solid var(--line); }
.panel-dark .icon-row { border-top-color: rgba(255, 255, 255, 0.16); }
.icon-row strong { display: block; font-weight: 600; }
.icon-row span { color: var(--steel); font-size: 0.97rem; }
.icon { flex: none; width: 2.9rem; height: 2.9rem; border-radius: 13px; display: grid; place-items: center; background: rgba(201, 58, 18, 0.1); color: var(--ember); }
.panel-dark .icon { background: rgba(255, 255, 255, 0.1); color: var(--ember-bright); }
.icon svg { width: 1.45rem; height: 1.45rem; fill: none; stroke: currentColor; stroke-width: 1.8; stroke-linecap: round; stroke-linejoin: round; }

/* Process */
.steps { display: grid; grid-template-columns: repeat(5, 1fr); gap: 1.5rem; }
.step { position: relative; }
.step-n { width: 2.8rem; height: 2.8rem; border-radius: 50%; background: var(--ink); color: #fff; display: grid; place-items: center; font: 700 1.15rem var(--display); margin-bottom: 1rem; position: relative; z-index: 1; }
.step:first-child .step-n { background: var(--ember); }
.step:not(:last-child)::after { content: ""; position: absolute; top: 1.4rem; left: 3.4rem; right: -1.5rem; border-top: 2px dashed #aebbc4; }
.step h3 { font-size: 1.15rem; margin-bottom: 0.3rem; }
.step p { font-size: 0.97rem; color: var(--steel); }

/* Why us */
.why { display: grid; grid-template-columns: 1fr 1fr; gap: clamp(2rem, 5vw, 4.5rem); align-items: center; }
.why-art { background: radial-gradient(circle at 30% 20%, #ffffff, #dfe8ee); border-radius: 26px; padding: 1.5rem; box-shadow: var(--shadow); }
.points li { position: relative; padding: 0.9rem 0 0.9rem 1.9rem; border-top: 1px solid var(--line); }
.points li::before { content: ""; position: absolute; left: 0; top: 1.4rem; width: 0.7rem; height: 0.7rem; background: var(--ember); border-radius: 2px; transform: rotate(45deg); }
.points strong { display: block; font: 700 1.15rem var(--display); }
.points span { color: var(--steel); }

/* Projects */
.feature-grid { display: grid; grid-template-columns: 1.3fr 1fr; gap: 1.5rem; }
.feature-grid .project:first-child { grid-row: span 2; }
.project-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 1.75rem; }
.project { background: var(--surface); border: 1px solid var(--line); border-radius: 20px; overflow: hidden; display: flex; flex-direction: column; box-shadow: var(--shadow); transition: transform 0.2s, box-shadow 0.2s; }
.project:hover { transform: translateY(-4px); box-shadow: 0 2px 4px rgba(14, 42, 59, 0.06), 0 26px 40px -18px rgba(14, 42, 59, 0.38); }
.project[hidden] { display: none; }
.shot { width: 100%; height: auto; aspect-ratio: 400 / 260; }
.project-body { padding: 1.3rem 1.5rem 1.6rem; display: flex; flex-direction: column; flex: 1; }
.project-kind { font-size: 0.92rem; color: var(--steel); margin-bottom: 0.2rem; }
.project h3 { margin-bottom: 0.5rem; }
.project p { font-size: 1rem; }
.outcome { font-weight: 600; border-left: 3px solid var(--ember); padding-left: 0.8rem; margin: 0.4rem 0 1.1rem; }
.tags { display: flex; flex-wrap: wrap; gap: 0.5rem; margin-bottom: 1.2rem; }
.tags li { font-size: 0.82rem; padding: 0.15rem 0.7rem; border: 1px solid var(--line); border-radius: 999px; color: var(--steel); background: var(--paper); }
.project-body .btn { margin-top: auto; align-self: flex-start; }
.filters { display: flex; flex-wrap: wrap; gap: 0.6rem; margin-bottom: 1.5rem; }
.filter { background: var(--surface); border: 2px solid var(--ink); color: var(--ink); border-radius: 999px; padding: 0.45rem 1.15rem; font: 600 0.95rem var(--body); cursor: pointer; transition: background-color 0.15s, color 0.15s; }
.filter:hover { background: #dfe7ec; }
.filter[aria-pressed="true"] { background: var(--ink); color: #fff; }
.result-count { color: var(--steel); font-size: 0.95rem; margin-bottom: 1.25rem; }

/* Case study dialog */
dialog.case { border: 0; padding: 0; border-radius: 22px; width: min(780px, calc(100% - 2rem)); max-height: calc(100vh - 2rem); overflow: auto; box-shadow: 0 40px 80px -20px rgba(0, 0, 0, 0.6); color: var(--ink); background: var(--surface); }
dialog.case::backdrop { background: rgba(8, 24, 35, 0.7); -webkit-backdrop-filter: blur(4px); backdrop-filter: blur(4px); }
.case-close { position: absolute; top: 0.9rem; right: 0.9rem; z-index: 2; width: 2.5rem; height: 2.5rem; border-radius: 50%; border: 0; background: rgba(255, 255, 255, 0.92); color: var(--ink); font: 500 1.5rem/1 var(--body); cursor: pointer; box-shadow: 0 4px 12px rgba(0, 0, 0, 0.25); }
.case-close:hover { background: #fff; }
.case-art .shot { border-radius: 0; }
.case-body { padding: 1.75rem 2rem 2.2rem; }
.case-body h2 { font-size: 2rem; margin-bottom: 0.2rem; }
.case-cols { display: grid; grid-template-columns: 1fr 1fr; gap: 0 2rem; margin-top: 1.25rem; }
.case-cols h3 { font-size: 1.05rem; margin-bottom: 0.3rem; }
.case-results { border-top: 1px solid var(--line); margin-top: 0.5rem; padding-top: 1rem; }
.case-results li { position: relative; padding: 0.25rem 0 0.25rem 1.6rem; }
.case-results li::before { content: ""; position: absolute; left: 0.2rem; top: 0.75rem; width: 0.55rem; height: 0.55rem; background: var(--ember); border-radius: 2px; transform: rotate(45deg); }

/* Portraits and quotes */
.portrait { border-radius: 50%; overflow: hidden; flex: none; }
.portrait svg { width: 100%; height: 100%; }
.slider { position: relative; }
.slide { display: grid; grid-template-columns: auto 1fr; gap: clamp(1.25rem, 3vw, 2.5rem); align-items: center; }
.slide[hidden] { display: none; }
.slide .portrait { width: clamp(6rem, 14vw, 10rem); height: clamp(6rem, 14vw, 10rem); box-shadow: 0 0 0 6px var(--paper), 0 0 0 8px var(--ember); }
.quote-big { font: 600 clamp(1.4rem, 3vw, 2.2rem)/1.28 var(--display); letter-spacing: -0.02em; margin: 0; max-width: 42ch; }
.who { margin-top: 1rem; font-size: 0.98rem; color: var(--steel); }
.who strong { color: var(--ink); display: block; font-weight: 600; }
.slider-controls { display: flex; align-items: center; gap: 0.75rem; margin-top: 2rem; }
.slider-btn { width: 2.75rem; height: 2.75rem; border-radius: 50%; border: 2px solid var(--ink); background: transparent; color: var(--ink); font: 600 1.15rem var(--body); cursor: pointer; transition: background-color 0.15s, color 0.15s; }
.slider-btn:hover { background: var(--ink); color: #fff; }
.slider-count { font-size: 0.95rem; color: var(--steel); min-width: 4rem; text-align: center; }
.slide .result, .feature-quote .result { display: block; width: fit-content; margin-top: 0.6rem; }
.quotes { columns: 2 22rem; column-gap: 2.5rem; }
.q { break-inside: avoid; margin: 0 0 1.75rem; padding: 1.5rem; background: var(--surface); border: 1px solid var(--line); border-radius: 18px; box-shadow: var(--shadow); }
.q blockquote { margin: 0 0 1.1rem; font-size: 1.1rem; line-height: 1.55; }
.q figcaption { display: flex; gap: 0.9rem; align-items: center; }
.q .portrait { width: 3.4rem; height: 3.4rem; }
.q .who { margin: 0; line-height: 1.4; }
.result { display: inline-block; margin-top: 0.3rem; font-weight: 600; font-size: 0.88rem; color: var(--ember-dark); background: rgba(201, 58, 18, 0.09); padding: 0.1rem 0.6rem; border-radius: 999px; }
.feature-quote { display: grid; grid-template-columns: auto 1fr; gap: clamp(1.25rem, 3vw, 2.5rem); align-items: center; }
.feature-quote .portrait { width: clamp(7rem, 16vw, 12rem); height: clamp(7rem, 16vw, 12rem); box-shadow: 0 0 0 6px var(--paper), 0 0 0 8px var(--ember); }

/* Inner page heads */
h1[tabindex="-1"]:focus { outline: none; }
.page-head { padding: clamp(3.2rem, 7vw, 5.5rem) 0 clamp(2.5rem, 5vw, 4rem); }
.page-head h1 { font-size: clamp(2.4rem, 5.5vw, 4.2rem); max-width: 18ch; }

/* Services page */
.service-group { display: grid; grid-template-columns: 0.8fr 1.4fr; gap: clamp(2rem, 5vw, 4.5rem); padding: clamp(2.5rem, 5vw, 4rem) 0; border-top: 2px solid var(--ink); }
.service-group:first-of-type { border-top: 0; }
.service-intro { align-self: start; position: sticky; top: 6.5rem; }
.service { display: flex; gap: 1.1rem; border-top: 1px solid var(--line); padding: 1.5rem 0; }
.service:first-child { border-top: 0; padding-top: 0; }
.service h3 { margin-bottom: 0.3rem; }
.service p { margin-bottom: 0.5rem; }
.stack { font-size: 0.92rem; color: var(--steel); }
.stack b { color: var(--ink); font-weight: 600; }
.table-wrap { overflow-x: auto; border: 1px solid var(--line); border-radius: 18px; background: var(--surface); box-shadow: var(--shadow); }
table { width: 100%; border-collapse: collapse; min-width: 640px; }
th, td { text-align: left; vertical-align: top; padding: 1rem 1.25rem; border-bottom: 1px solid var(--line); font-size: 1rem; }
thead th { font: 700 1.1rem var(--display); background: #e3eaef; }
tbody th { font-weight: 600; width: 16%; color: var(--steel); }
tbody tr:last-child th, tbody tr:last-child td { border-bottom: 0; }
.faq { max-width: 46rem; border-top: 2px solid var(--ink); }
.faq details { border-bottom: 1px solid var(--line); }
.faq summary { cursor: pointer; list-style: none; font: 600 1.1rem var(--display); padding: 1.1rem 2.5rem 1.1rem 0; position: relative; }
.faq summary::-webkit-details-marker { display: none; }
.faq summary::after { content: "+"; position: absolute; right: 0.4rem; top: 0.9rem; font: 500 1.6rem/1 var(--body); color: var(--ember); }
.faq details[open] summary::after { content: "\2212"; }
.faq details p { padding-bottom: 1.1rem; color: var(--steel); }

/* About */
.story { display: grid; grid-template-columns: 1fr 1fr; gap: clamp(2rem, 5vw, 4.5rem); }
.story p { max-width: none; }
.values { display: grid; grid-template-columns: repeat(2, 1fr); gap: 1.25rem; }
.values > div { display: flex; gap: 1rem; background: var(--surface); border: 1px solid var(--line); border-radius: 18px; padding: 1.4rem; box-shadow: var(--shadow); }
.values dt { font: 700 1.2rem var(--display); margin-bottom: 0.3rem; }
.values dd { margin: 0; color: var(--steel); }
.team { display: grid; grid-template-columns: repeat(auto-fit, minmax(210px, 1fr)); gap: 2rem 1.75rem; }
.person .portrait { width: 100%; height: auto; aspect-ratio: 1; border-radius: 22px; margin-bottom: 0.9rem; }
.person strong { display: block; font: 700 1.15rem var(--display); }
.person span { color: var(--steel); font-size: 0.96rem; }
.leaders { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; }
.leader { display: flex; gap: 1.4rem; align-items: flex-start; background: var(--surface); border: 1px solid var(--line); border-radius: 22px; padding: 1.5rem; box-shadow: var(--shadow); }
.section-white .leader { background: var(--paper); box-shadow: none; }
.leader .portrait { width: 8rem; height: 8rem; border-radius: 20px; }
.leader h3 { font-size: 1.5rem; margin-bottom: 0.1rem; }
.leader-role { color: var(--steel); margin-bottom: 0.5rem; }
.leader .result { margin: 0 0 0.8rem; }
.leader p:last-child { margin-bottom: 0; }
.timeline { border-left: 2px solid var(--ink); margin-left: 0.4rem; max-width: 40rem; }
.timeline li { position: relative; padding: 0 0 1.75rem 1.75rem; }
.timeline li::before { content: ""; position: absolute; left: -0.55rem; top: 0.45rem; width: 0.9rem; height: 0.9rem; background: var(--ember); border-radius: 50%; border: 3px solid var(--paper); box-sizing: content-box; margin-left: -3px; }
.timeline b { font: 700 1.15rem var(--display); display: block; }
.timeline span { color: var(--steel); }

/* Contact */
.contact-grid { display: grid; grid-template-columns: 1.25fr 0.75fr; gap: clamp(2rem, 5vw, 4.5rem); align-items: start; }
.form { background: var(--surface); border: 1px solid var(--line); border-radius: 22px; padding: clamp(1.4rem, 3vw, 2.25rem); box-shadow: var(--shadow); }
.form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1.25rem; }
.field { margin-bottom: 1.25rem; }
.field label { display: block; font-weight: 600; font-size: 0.95rem; margin-bottom: 0.35rem; }
.field input, .field select, .field textarea { width: 100%; padding: 0.8rem 0.9rem; font: 400 1rem var(--body); color: var(--ink); background: #fff; border: 1.5px solid #8795a0; border-radius: 8px; }
.field textarea { min-height: 9rem; resize: vertical; }
.field input:focus, .field select:focus, .field textarea:focus { outline: 3px solid var(--ember); outline-offset: 1px; border-color: var(--ink); }
.field [aria-invalid="true"] { border-color: var(--error); }
.error { color: var(--error); font-size: 0.9rem; margin: 0.3rem 0 0; }
.hint { color: var(--steel); font-size: 0.9rem; font-weight: 400; }
.notice { border-radius: 22px; padding: 2rem; }
.notice h2 { font-size: 1.8rem; }
.person-card { display: flex; gap: 1rem; align-items: center; background: var(--surface); border: 1px solid var(--line); border-radius: 18px; padding: 1.1rem; margin-bottom: 2rem; box-shadow: var(--shadow); }
.person-card .portrait { width: 4.5rem; height: 4.5rem; }
.person-card p { margin: 0; font-size: 0.97rem; line-height: 1.45; }
.contact-side h2 { font-size: 1.5rem; }
.contact-list { margin-bottom: 2.25rem; }
.contact-list li { border-top: 1px solid var(--line); padding: 0.9rem 0; }
.contact-list strong { display: block; font-weight: 600; }
.next-steps { counter-reset: n; }
.next-steps li { counter-increment: n; position: relative; padding: 0.7rem 0 0.7rem 2.6rem; border-top: 1px solid var(--line); }
.next-steps li::before { content: counter(n); position: absolute; left: 0; top: 0.6rem; width: 1.8rem; height: 1.8rem; border-radius: 50%; background: var(--ink); color: #fff; display: grid; place-items: center; font: 700 0.9rem var(--display); }

/* CTA + footer */
.cta-band { padding: clamp(3.5rem, 7vw, 5.5rem) 0; }
.cta-band h2 { max-width: 20ch; }
.site-footer { background: #0a1e2b; color: #c2d2dd; padding: 3.5rem 0 2rem; font-size: 0.98rem; }
.footer-grid { display: grid; grid-template-columns: 1.4fr 1fr 1.3fr 1fr 1.1fr; gap: 2.25rem; }
.site-footer .brand { color: #fff; margin-bottom: 0.9rem; }
.site-footer .brand span { color: #93abba; }
.site-footer h3 { font-size: 1rem; color: #fff; margin-bottom: 0.8rem; }
.site-footer li { margin-bottom: 0.45rem; }
.site-footer a { text-decoration: none; }
.site-footer a:hover { color: #fff; text-decoration: underline; text-underline-offset: 3px; }
.site-footer :focus-visible { outline-color: var(--ember-bright); }
.footer-base { border-top: 1px solid rgba(255, 255, 255, 0.14); margin-top: 2.5rem; padding-top: 1.5rem; font-size: 0.9rem; color: #93abba; }

/* Responsive */
@media (max-width: 960px) {
  .hero-grid, .story, .contact-grid, .service-group, .why { grid-template-columns: 1fr; }
  .service-intro { position: static; }
  .steps { grid-template-columns: repeat(2, 1fr); }
  .step::after { display: none; }
  .feature-grid, .panels, .leaders { grid-template-columns: 1fr; }
  .feature-grid .project:first-child { grid-row: auto; }
  .footer-grid { grid-template-columns: 1fr 1fr; }
  .log-card { position: static; width: 100%; margin-top: 1rem; }
  .hero-art { padding-bottom: 0; }
  .chip { top: -0.5rem; right: 0.5rem; }
}
@media (max-width: 980px) {
  .nav-toggle { display: inline-block; }
  .nav { display: none; position: absolute; left: 0; right: 0; top: 4.5rem; background: var(--paper); border-bottom: 1px solid var(--line); flex-direction: column; align-items: flex-start; padding: 1.25rem 1.25rem 1.75rem; gap: 1.25rem; }
  .site-header.nav-open .nav { display: flex; }
  .nav-links { flex-direction: column; gap: 0.6rem; }
}
@media (max-width: 680px) {
  .project-grid, .form-row, .values, .case-cols { grid-template-columns: 1fr; }
  .steps { grid-template-columns: 1fr; }
  .leader { flex-direction: column; }
  .footer-grid { grid-template-columns: 1fr; }
  .slide, .feature-quote { grid-template-columns: 1fr; }
  .case-body { padding: 1.4rem 1.25rem 1.8rem; }
}
@media (prefers-reduced-motion: reduce) {
  html { scroll-behavior: auto; }
  *, *::before, *::after { transition: none !important; animation: none !important; }
}

/* ---------- Navigation helpers ---------- */
.progress { position: fixed; top: 0; left: 0; height: 3px; width: 0; background: var(--ember); z-index: 80; }
.to-top { position: fixed; right: 1.25rem; bottom: 1.25rem; z-index: 60; width: 3rem; height: 3rem; border-radius: 50%; border: 0; background: var(--ink); color: #fff; cursor: pointer; display: grid; place-items: center; box-shadow: 0 10px 24px -8px rgba(0, 0, 0, 0.5); transition: background-color 0.15s; }
.to-top[hidden] { display: none; }
.to-top:hover { background: var(--ember); }
.to-top svg { width: 1.3rem; height: 1.3rem; fill: none; stroke: currentColor; stroke-width: 2.2; stroke-linecap: round; stroke-linejoin: round; }
.crumbs { display: flex; flex-wrap: wrap; gap: 0.5rem; font-size: 0.92rem; color: #9db6c6; margin-bottom: 1.25rem; }
.crumbs a { color: #c9d8e2; text-underline-offset: 3px; }
.crumbs a:hover { color: #fff; }
.crumbs [aria-current] { color: #fff; }
.subnav { position: sticky; top: 4.5rem; z-index: 40; background: rgba(255, 255, 255, 0.95); -webkit-backdrop-filter: blur(8px); backdrop-filter: blur(8px); border-bottom: 1px solid var(--line); }
.subnav .wrap { display: flex; flex-wrap: wrap; align-items: center; gap: 0.5rem 0.75rem; padding: 0.7rem 0; }
.subnav span { font-size: 0.9rem; color: var(--steel); margin-right: 0.5rem; }
.subnav a { font-weight: 600; font-size: 0.95rem; text-decoration: none; padding: 0.3rem 0.95rem; border-radius: 999px; border: 1.5px solid var(--line); }
.subnav a:hover { border-color: var(--ink); background: var(--paper); }
.service-group, #models, #faq { scroll-margin-top: 8rem; }

/* ---------- Blog ---------- */
.blog-filter { background: var(--surface); border: 2px solid var(--ink); color: var(--ink); border-radius: 999px; padding: 0.45rem 1.15rem; font: 600 0.95rem var(--body); cursor: pointer; transition: background-color 0.15s, color 0.15s; }
.blog-filter:hover { background: #dfe7ec; }
.blog-filter[aria-pressed="true"] { background: var(--ink); color: #fff; }
.blog-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.75rem; }
.post-card { position: relative; background: var(--surface); border: 1px solid var(--line); border-radius: 20px; overflow: hidden; display: flex; flex-direction: column; box-shadow: var(--shadow); transition: transform 0.2s, box-shadow 0.2s; }
.post-card:hover { transform: translateY(-4px); box-shadow: 0 2px 4px rgba(14, 42, 59, 0.06), 0 26px 40px -18px rgba(14, 42, 59, 0.38); }
.post-card[hidden] { display: none; }
.cover { width: 100%; height: auto; aspect-ratio: 16 / 9; }
.post-card.featured { grid-column: 1 / -1; flex-direction: row; }
.post-card.featured .cover { width: 52%; height: auto; aspect-ratio: auto; align-self: stretch; }
.post-card.featured h3 { font-size: clamp(1.5rem, 2.6vw, 2rem); }
.post-card.featured .post-body { justify-content: center; padding: 2rem; }
.post-body { padding: 1.3rem 1.5rem 1.5rem; display: flex; flex-direction: column; flex: 1; }
.post-meta { display: flex; flex-wrap: wrap; gap: 0.4rem 0.9rem; align-items: center; font-size: 0.9rem; color: var(--steel); margin-bottom: 0.6rem; }
.cat { font-weight: 600; color: var(--ember-dark); background: rgba(201, 58, 18, 0.09); padding: 0.1rem 0.7rem; border-radius: 999px; font-size: 0.85rem; }
.post-card h3 { margin-bottom: 0.5rem; }
.post-card h3 a { text-decoration: none; }
.post-card h3 a::after { content: ""; position: absolute; inset: 0; }
.post-card p { font-size: 1rem; color: var(--steel); }
.byline { display: flex; gap: 0.7rem; align-items: center; margin-top: auto; padding-top: 0.9rem; font-size: 0.92rem; }
.byline .portrait { width: 2.5rem; height: 2.5rem; }
.byline strong { display: block; font-weight: 600; line-height: 1.2; }
.byline span { color: var(--steel); font-size: 0.85rem; }

.narrow { width: min(860px, 100% - 2.5rem); margin-inline: auto; }
.post-head { padding: clamp(3rem, 6vw, 5rem) 0 clamp(4rem, 7vw, 6rem); }
.post-head h1 { font-size: clamp(2.1rem, 4.6vw, 3.6rem); max-width: 22ch; }
.post-head .post-meta { color: #c9d8e2; margin-bottom: 1rem; }
.post-head .cat { background: rgba(255, 255, 255, 0.14); color: #fff; }
.post-byline { display: flex; flex-wrap: wrap; gap: 1rem 1.5rem; align-items: center; margin-top: 1.5rem; color: #c9d8e2; font-size: 0.97rem; }
.post-byline .portrait { width: 3rem; height: 3rem; }
.post-byline strong { color: #fff; display: block; font-weight: 600; line-height: 1.2; }
.post-cover { margin-top: -3.2rem; position: relative; z-index: 1; }
.post-cover .cover { border-radius: 22px; box-shadow: 0 30px 50px -24px rgba(14, 42, 59, 0.55); aspect-ratio: 2 / 1; }
.prose { font-size: 1.125rem; padding-top: 2.5rem; }
.prose p { max-width: none; }
.prose h2 { font-size: 1.6rem; margin: 2.2rem 0 0.5rem; }
.prose ul, .prose ol { margin: 0 0 1.2em; }
.prose li { position: relative; padding: 0.5rem 0 0.5rem 1.8rem; border-top: 1px solid var(--line); }
.prose li:last-child { border-bottom: 1px solid var(--line); }
.prose li::before { content: ""; position: absolute; left: 0.2rem; top: 1.15rem; width: 0.6rem; height: 0.6rem; background: var(--ember); border-radius: 2px; transform: rotate(45deg); }
.callout { background: var(--surface); border: 1px solid var(--line); border-left: 5px solid var(--ember); border-radius: 12px; padding: 1.1rem 1.4rem; margin: 2rem 0; font-weight: 500; }
.callout b { display: block; font: 700 0.95rem var(--display); color: var(--ember-dark); margin-bottom: 0.2rem; }
.prose .table-wrap { margin: 1.5rem 0; }
.prose th, .prose td { font-size: 1rem; }
.post-actions { display: flex; flex-wrap: wrap; gap: 0.75rem; margin: 2rem 0 0; }
.author-box { display: flex; gap: 1.1rem; align-items: center; background: var(--surface); border: 1px solid var(--line); border-radius: 18px; padding: 1.2rem; margin-top: 2.5rem; box-shadow: var(--shadow); }
.author-box .portrait { width: 4.5rem; height: 4.5rem; }
.author-box p { margin: 0; font-size: 0.97rem; line-height: 1.5; }
.post-nav { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; margin: 2rem 0 4rem; }
.post-nav a { display: block; border: 1px solid var(--line); border-radius: 16px; padding: 1rem 1.2rem; text-decoration: none; background: var(--surface); transition: border-color 0.15s; }
.post-nav a:hover { border-color: var(--ink); }
.post-nav small { display: block; color: var(--steel); font-size: 0.85rem; }
.post-nav strong { font: 700 1.05rem/1.25 var(--display); }
.post-nav .next { text-align: right; grid-column: 2; }

@media (max-width: 960px) {
  .blog-grid { grid-template-columns: repeat(2, 1fr); }
  .post-card.featured { flex-direction: column; }
  .post-card.featured .cover { width: 100%; aspect-ratio: 16 / 9; }
}
@media (max-width: 680px) {
  .blog-grid, .post-nav { grid-template-columns: 1fr; }
  .post-nav .next { grid-column: auto; text-align: left; }
  .author-box { flex-direction: column; align-items: flex-start; }
}

/* ---------- Navbar responsiveness ---------- */
.nav-links a { transition: border-color 0.15s, color 0.15s; }
.nav-links a:active, .nav > .btn:active { opacity: 0.7; }
.nav-links a:hover { color: var(--ember-dark); }
.nav-toggle { min-height: 2.75rem; }
.page:not([hidden]) { animation: pageIn 0.28s ease both; }
@keyframes pageIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: none; } }
@media (max-width: 980px) {
  .nav { max-height: calc(100vh - 4.5rem); overflow-y: auto; box-shadow: 0 24px 40px -20px rgba(14, 42, 59, 0.35); }
  .nav-links { width: 100%; gap: 0; }
  .nav-links li { border-top: 1px solid var(--line); }
  .nav-links li:first-child { border-top: 0; }
  .nav-links a { display: block; padding: 0.9rem 0; font-size: 1.1rem; border-bottom: 0; }
  .nav-links a[aria-current="page"] { color: var(--ember-dark); box-shadow: inset 3px 0 0 var(--ember); padding-left: 0.9rem; }
  .nav > .btn { width: 100%; padding: 0.95rem 1.5rem; }
}

  </style>
</head>
<body>

<div class="progress" id="progress" aria-hidden="true"></div>
<a class="skip" href="#main">Skip to content</a>
<header class="site-header">
  <div class="wrap header-inner">
    <a class="brand" href="#home" aria-label="DigitalForgePro home"><svg viewBox="0 0 32 32" aria-hidden="true"><rect width="32" height="32" rx="8" fill="#12202b"/><path d="M9 7h14v4H13v4h8v4h-8v6H9z" fill="#fff"/><rect x="19" y="21" width="4" height="4" fill="#ff7a4d"/></svg><div>DigitalForge<span>Pro</span></div></a>
    <button class="nav-toggle" id="nav-toggle" aria-expanded="false" aria-controls="site-nav">Menu</button>
    <nav class="nav" id="site-nav" aria-label="Main">
      <ul class="nav-links"><li><a href="#home">Home</a></li><li><a href="#services">Services</a></li><li><a href="#projects">Projects</a></li><li><a href="#testimonials">Testimonials</a></li><li><a href="#about">About</a></li><li><a href="#blog">Blog</a></li></ul>
      <a class="btn btn-primary" href="#contact">Contact us</a>
    </nav>
  </div>
</header>
<main id="main">

<div class="page" id="page-home">
<section class="hero dark">
  <div class="wrap hero-grid">
    <div>
      <h1>We build your software, then keep it running.</h1>
      <p class="lede">DigitalForgePro designs and builds web apps, mobile apps and cloud platforms for growing companies. After launch we host, monitor and maintain them, so one team stays accountable from the first sketch to the 3 a.m. alert.</p>
      <div class="btn-row">
        <a class="btn btn-primary" href="#contact">Contact us</a>
        <a class="btn btn-ghost" href="#projects">See our projects</a>
      </div>
      <p class="hero-note">Led by CEO Andrew Parker, with 10 years of experience. Free 30-minute discovery call.</p>
    </div>
    <div class="hero-art">
      
<svg class="art-main" viewBox="0 0 560 470" role="img" aria-label="Illustration of a web dashboard and a mobile banking app">
  <defs>
    <linearGradient id="gWin" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="#ffffff"/><stop offset="1" stop-color="#e9eff3"/></linearGradient>
    <linearGradient id="gEmber" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#ff9a6b"/><stop offset="1" stop-color="#c93a12"/></linearGradient>
    <linearGradient id="gArea" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="#ff7a4d" stop-opacity=".35"/><stop offset="1" stop-color="#ff7a4d" stop-opacity="0"/></linearGradient>
    <filter id="shadow" x="-20%" y="-20%" width="140%" height="160%"><feDropShadow dx="0" dy="20" stdDeviation="18" flood-color="#000" flood-opacity=".4"/></filter>
  </defs>
  <circle cx="300" cy="230" r="205" fill="none" stroke="#fff" stroke-opacity=".08" stroke-width="2"/>
  <circle cx="300" cy="230" r="150" fill="none" stroke="#fff" stroke-opacity=".06" stroke-width="2"/>
  <g filter="url(#shadow)"><rect x="24" y="48" width="410" height="300" rx="18" fill="url(#gWin)"/></g>
  <path d="M24 66a18 18 0 0 1 18-18h374a18 18 0 0 1 18 18v20H24z" fill="#dce5ea"/>
  <circle cx="46" cy="67" r="4.5" fill="#ff7a4d"/><circle cx="61" cy="67" r="4.5" fill="#f4b942"/><circle cx="76" cy="67" r="4.5" fill="#5fd1a8"/>
  <rect x="112" y="58" width="210" height="18" rx="9" fill="#fff"/>
  <path d="M24 86H112V348H42A18 18 0 0 1 24 330Z" fill="#12202b"/>
  <rect x="38" y="100" width="22" height="22" rx="6" fill="#ff7a4d"/>
  <rect x="38" y="140" width="60" height="9" rx="4.5" fill="#fff" fill-opacity=".9"/>
  <rect x="38" y="168" width="48" height="9" rx="4.5" fill="#fff" fill-opacity=".28"/>
  <rect x="38" y="196" width="56" height="9" rx="4.5" fill="#fff" fill-opacity=".28"/>
  <rect x="38" y="224" width="40" height="9" rx="4.5" fill="#fff" fill-opacity=".28"/>
  <rect x="132" y="102" width="130" height="13" rx="6.5" fill="#12202b" fill-opacity=".85"/>
  <rect x="132" y="122" width="84" height="8" rx="4" fill="#12202b" fill-opacity=".28"/>
  <g>
    <rect x="132" y="144" width="92" height="56" rx="10" fill="#fff" stroke="#d3dde4"/><rect x="142" y="154" width="38" height="6" rx="3" fill="#12202b" fill-opacity=".35"/><rect x="142" y="170" width="56" height="12" rx="5" fill="#12202b"/>
    <rect x="232" y="144" width="92" height="56" rx="10" fill="#fff" stroke="#d3dde4"/><rect x="242" y="154" width="38" height="6" rx="3" fill="#12202b" fill-opacity=".35"/><rect x="242" y="170" width="46" height="12" rx="5" fill="#1faa72"/>
    <rect x="332" y="144" width="92" height="56" rx="10" fill="#fff" stroke="#d3dde4"/><rect x="342" y="154" width="38" height="6" rx="3" fill="#12202b" fill-opacity=".35"/><rect x="342" y="170" width="62" height="12" rx="5" fill="#c93a12"/>
  </g>
  <rect x="132" y="212" width="292" height="124" rx="12" fill="#fff" stroke="#d3dde4"/>
  <path d="M148 306L180 286L212 292L244 266L276 274L308 246L340 254L372 228L404 236V322H148Z" fill="url(#gArea)"/>
  <g fill="#cfe0ea">
    <rect x="152" y="296" width="18" height="26" rx="3"/><rect x="184" y="284" width="18" height="38" rx="3"/><rect x="216" y="290" width="18" height="32" rx="3"/><rect x="248" y="268" width="18" height="54" rx="3"/><rect x="280" y="276" width="18" height="46" rx="3"/><rect x="312" y="250" width="18" height="72" rx="3"/><rect x="344" y="258" width="18" height="64" rx="3"/><rect x="376" y="236" width="18" height="86" rx="3" fill="#12202b"/>
  </g>
  <polyline points="161,284 193,266 225,272 257,246 289,254 321,226 353,234 385,208" fill="none" stroke="#ff7a4d" stroke-width="3.5" stroke-linecap="round" stroke-linejoin="round"/>
  <circle cx="385" cy="208" r="6" fill="#fff" stroke="#ff7a4d" stroke-width="3.5"/>
  <g filter="url(#shadow)"><rect x="394" y="150" width="150" height="292" rx="30" fill="#12202b"/></g>
  <rect x="404" y="162" width="130" height="268" rx="22" fill="#f7f9fa"/>
  <rect x="446" y="168" width="46" height="8" rx="4" fill="#12202b"/>
  <circle cx="430" cy="204" r="14" fill="url(#gEmber)"/>
  <rect x="452" y="194" width="52" height="7" rx="3.5" fill="#12202b" fill-opacity=".8"/><rect x="452" y="207" width="34" height="5" rx="2.5" fill="#12202b" fill-opacity=".3"/>
  <rect x="416" y="230" width="106" height="68" rx="14" fill="url(#gEmber)"/>
  <rect x="428" y="242" width="40" height="6" rx="3" fill="#fff" fill-opacity=".8"/><rect x="428" y="256" width="72" height="14" rx="5" fill="#fff"/><rect x="428" y="278" width="30" height="6" rx="3" fill="#fff" fill-opacity=".6"/>
  <g>
    <circle cx="430" cy="326" r="9" fill="#cfe0ea"/><rect x="446" y="319" width="56" height="7" rx="3.5" fill="#12202b" fill-opacity=".75"/><rect x="446" y="331" width="34" height="5" rx="2.5" fill="#12202b" fill-opacity=".3"/>
    <circle cx="430" cy="362" r="9" fill="#cfe0ea"/><rect x="446" y="355" width="48" height="7" rx="3.5" fill="#12202b" fill-opacity=".75"/><rect x="446" y="367" width="30" height="5" rx="2.5" fill="#12202b" fill-opacity=".3"/>
    <circle cx="430" cy="398" r="9" fill="#cfe0ea"/><rect x="446" y="391" width="56" height="7" rx="3.5" fill="#12202b" fill-opacity=".75"/><rect x="446" y="403" width="38" height="5" rx="2.5" fill="#12202b" fill-opacity=".3"/>
  </g>
  <g fill="#f4b942"><rect x="470" y="80" width="9" height="9" transform="rotate(45 474 84)"/><rect x="500" y="112" width="6" height="6" transform="rotate(45 503 115)" fill="#ff7a4d"/><rect x="40" y="28" width="7" height="7" transform="rotate(45 43 31)" fill="#ff7a4d"/><rect x="346" y="28" width="6" height="6" transform="rotate(45 349 31)"/></g>
</svg>
      <div class="chip"><i></i>99.98% uptime, last 12 months</div>
      <div class="log log-card" id="deploy-log" role="img" aria-label="Animated example of a software release going live with zero downtime">
        <div class="log-bar"><span>customer-portal / production</span><button class="log-replay" id="log-replay" type="button">Replay</button></div>
        <div class="log-body" aria-hidden="true">
          <div class="log-line"><span class="cmd">$</span><span>forge release customer-portal</span></div>
          <div class="log-line"><span class="ok">ok</span><span>1,284 tests passed</span></div>
          <div class="log-line"><span class="ok">ok</span><span>Security scan: no issues</span></div>
          <div class="log-line"><span class="ok">ok</span><span>Rolled out to 3 regions</span></div>
          <div class="log-line final"><span>Live. Zero downtime.</span></div>
        </div>
      </div>
    </div>
  </div>
</section>

<div class="trusted-band">
  <div class="wrap trusted">
    <p>Teams that run on software we built and look after</p>
    <ul><li>Harborline</li><li>LedgerLeaf</li><li>ClinicFlow</li><li>Marketly</li><li>FieldNotes</li></ul>
  </div>
</div>

<section class="section">
  <div class="wrap">
    <div class="section-head">
      <h2>Two jobs, done by the same people.</h2>
      <p class="lede">Most software problems start at the handoff between the team that built it and the team that runs it. We removed the handoff.</p>
    </div>
    <div class="panels">
      <div class="panel panel-light">
        <h3>Build</h3>
        <p>Software made to fit how your business actually works.</p>
        <ul>
          <li class="icon-row"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><rect x="3" y="4" width="18" height="16" rx="2"/><path d="M3 9h18M7 6.5h.01M10 6.5h.01"/></svg></span><div><strong>Custom web applications</strong><span>Portals, dashboards, internal tools and SaaS products.</span></div></li>
          <li class="icon-row"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><rect x="7" y="2.5" width="10" height="19" rx="2.5"/><path d="M11 18.5h2"/></svg></span><div><strong>Mobile apps</strong><span>iOS and Android, native or cross-platform.</span></div></li>
          <li class="icon-row"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><circle cx="6" cy="12" r="2.5"/><circle cx="18" cy="6" r="2.5"/><circle cx="18" cy="18" r="2.5"/><path d="M8.3 11l7.4-4M8.3 13l7.4 4"/></svg></span><div><strong>APIs and integrations</strong><span>Connect payments, CRMs and older systems.</span></div></li>
          <li class="icon-row"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M4 20l4-1 11-11-3-3L5 16z"/><path d="M14 7l3 3"/></svg></span><div><strong>Product design</strong><span>Research, prototypes and design systems.</span></div></li>
        </ul>
      </div>
      <div class="panel panel-dark">
        <h3>Manage</h3>
        <p>Ongoing care so your software stays fast, secure and current.</p>
        <ul>
          <li class="icon-row"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M7 18h10.5a4 4 0 0 0 .5-7.97A6 6 0 0 0 6.6 9.2 4.4 4.4 0 0 0 7 18z"/></svg></span><div><strong>Hosting and monitoring</strong><span>Cloud infrastructure we run and watch for you.</span></div></li>
          <li class="icon-row"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M14.5 6.5a4 4 0 0 0-5 5L4 17l3 3 5.5-5.5a4 4 0 0 0 5-5l-2.5 2.5-2.5-.5-.5-2.5z"/></svg></span><div><strong>Maintenance and updates</strong><span>Patches, upgrades and bug fixes on a schedule.</span></div></li>
          <li class="icon-row"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M12 3l8 3v6c0 4.5-3.2 8-8 9-4.8-1-8-4.5-8-9V6z"/><path d="M9 12l2 2 4-4"/></svg></span><div><strong>Security and compliance</strong><span>Backups, access reviews and audit preparation.</span></div></li>
          <li class="icon-row"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M4 14v-2a8 8 0 0 1 16 0v2"/><rect x="3" y="14" width="4" height="6" rx="1.5"/><rect x="17" y="14" width="4" height="6" rx="1.5"/></svg></span><div><strong>Support and on-call</strong><span>A real person answers, with response times in writing.</span></div></li>
        </ul>
      </div>
    </div>
    <p style="margin-top:2rem"><a class="text-link" href="#services">Explore all services</a></p>
  </div>
</section>

<section class="section section-white">
  <div class="wrap">
    <div class="section-head"><h2>How a project moves from idea to live.</h2></div>
    <ol class="steps">
      <li class="step"><span class="step-n">1</span><h3>Discover</h3><p>We learn your users, goals and constraints, then agree on what to build first.</p></li>
      <li class="step"><span class="step-n">2</span><h3>Design</h3><p>Clickable prototypes you can test with real people before any code is written.</p></li>
      <li class="step"><span class="step-n">3</span><h3>Build</h3><p>Two-week cycles, with working software you can use at the end of each one.</p></li>
      <li class="step"><span class="step-n">4</span><h3>Launch</h3><p>Staged rollout, load testing and a rehearsed rollback plan.</p></li>
      <li class="step"><span class="step-n">5</span><h3>Run</h3><p>Monitoring, updates and support continue, with a monthly report you can read.</p></li>
    </ol>
  </div>
</section>

<section class="section">
  <div class="wrap why">
    <div class="why-art">
<svg viewBox="0 0 520 380" role="img" aria-label="Diagram: Build and Run overlap as one team" style="width:100%;height:auto">
  <defs><clipPath id="clipBuild"><circle cx="205" cy="190" r="125"/></clipPath></defs>
  <circle cx="260" cy="190" r="178" fill="none" stroke="#12202b" stroke-opacity=".12" stroke-width="2" stroke-dasharray="4 8"/>
  <circle cx="205" cy="190" r="125" fill="#0e2a3b"/>
  <circle cx="315" cy="190" r="125" fill="#c93a12"/>
  <circle cx="315" cy="190" r="125" fill="#f4b942" clip-path="url(#clipBuild)"/>
  <g font-family="Bricolage Grotesque, Public Sans, sans-serif" text-anchor="middle">
    <text x="148" y="200" font-size="36" font-weight="800" fill="#fff">Build</text>
    <text x="372" y="200" font-size="36" font-weight="800" fill="#fff">Run</text>
    <text x="260" y="186" font-size="17" font-weight="700" fill="#12202b">One</text>
    <text x="260" y="206" font-size="17" font-weight="700" fill="#12202b">team</text>
  </g>
  <g font-family="Public Sans, sans-serif" font-size="14" font-weight="600" text-anchor="middle">
    <rect x="46" y="62" width="92" height="30" rx="15" fill="#fff"/><text x="92" y="82" fill="#12202b">Design</text>
    <rect x="20" y="228" width="80" height="30" rx="15" fill="#fff"/><text x="60" y="248" fill="#12202b">Code</text>
    <rect x="98" y="312" width="80" height="30" rx="15" fill="#fff"/><text x="138" y="332" fill="#12202b">Test</text>
    <rect x="382" y="58" width="96" height="30" rx="15" fill="#fff"/><text x="430" y="78" fill="#12202b">Monitor</text>
    <rect x="428" y="236" width="76" height="30" rx="15" fill="#fff"/><text x="466" y="256" fill="#12202b">Patch</text>
    <rect x="350" y="316" width="96" height="30" rx="15" fill="#fff"/><text x="398" y="336" fill="#12202b">Support</text>
  </g>
</svg></div>
    <div>
      <h2>Build and run, under one roof.</h2>
      <p class="lede">When the same people build and operate your software, they make better decisions at every step.</p>
      <ul class="points">
        <li><strong>One team, one agreement</strong><span>No finger-pointing between the people who built it and the people who run it.</span></li>
        <li><strong>Designed to be operated</strong><span>Monitoring, backups and recovery plans are part of the build, not an afterthought.</span></li>
        <li><strong>No surprises</strong><span>A plain-language report every month: what changed, what it cost, what we recommend.</span></li>
      </ul>
    </div>
  </div>
</section>

<section class="section section-white">
  <div class="wrap">
    <div class="section-head">
      <h2>Recent work.</h2>
      <p class="lede">A few of the products we built and still look after. Open a case study to see what we did and what changed.</p>
    </div>
    <div class="feature-grid">
      
<article class="project" data-cat="web">
  <svg class="shot" viewBox="0 0 400 260" aria-hidden="true" focusable="false"><rect width="400" height="260" fill="#12202b"/><circle cx="370" cy="20" r="120" fill="#ffffff" opacity=".08"/><circle cx="10" cy="260" r="100" fill="#ff7a4d" opacity=".2"/><rect x="38" y="44" width="344" height="204" rx="12" fill="#000" opacity=".2"/><rect x="28" y="30" width="344" height="204" rx="12" fill="#ffffff"/><rect x="28" y="30" width="344" height="26" rx="12" fill="#12202b" opacity=".18"/><rect x="28" y="44" width="344" height="12" fill="#12202b" opacity=".18"/><rect x="44" y="68" width="98" height="40" rx="8" fill="#12202b" opacity=".12"/><rect x="52" y="76" width="36" height="6" rx="3" fill="#12202b" opacity=".5"/><rect x="52" y="90" width="56" height="10" rx="4" fill="#12202b"/><rect x="152" y="68" width="98" height="40" rx="8" fill="#12202b" opacity=".12"/><rect x="160" y="76" width="36" height="6" rx="3" fill="#12202b" opacity=".5"/><rect x="160" y="90" width="56" height="10" rx="4" fill="#12202b"/><rect x="260" y="68" width="98" height="40" rx="8" fill="#12202b" opacity=".12"/><rect x="268" y="76" width="36" height="6" rx="3" fill="#12202b" opacity=".5"/><rect x="268" y="90" width="56" height="10" rx="4" fill="#ff7a4d"/><rect x="54" y="180" width="24" height="34" rx="4" fill="#12202b" opacity="0.8"/><rect x="94" y="160" width="24" height="54" rx="4" fill="#12202b" opacity="0.8"/><rect x="134" y="170" width="24" height="44" rx="4" fill="#12202b" opacity="0.8"/><rect x="174" y="146" width="24" height="68" rx="4" fill="#12202b" opacity="0.8"/><rect x="214" y="158" width="24" height="56" rx="4" fill="#12202b" opacity="0.8"/><rect x="254" y="134" width="24" height="80" rx="4" fill="#12202b" opacity="0.8"/><rect x="294" y="152" width="24" height="62" rx="4" fill="#ff7a4d" opacity="1"/><polyline points="66,160 106,142 146,150 186,124 226,134 266,108 306,118" fill="none" stroke="#ff7a4d" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/></svg>
  <div class="project-body">
    <p class="project-kind">Web application</p>
    <h3>Harborline Freight Tracker</h3>
    <p>A live dispatch dashboard for a regional freight company, replacing three spreadsheets and a phone tree.</p>
    <p class="outcome">Dispatch calls fell by 38% in the first quarter.</p>
    <ul class="tags"><li>React</li><li>Node.js</li><li>PostgreSQL</li></ul>
    <button class="btn btn-ghost btn-small open-case" type="button">View case study</button>
  </div>
  <template>
    <h2>Harborline Freight Tracker</h2>
    <p class="project-kind">Web application</p>
    <div class="case-cols">
      <div><h3>The challenge</h3><p>Dispatchers tracked more than 200 trucks across three spreadsheets and constant phone calls, so delays surfaced hours late.</p></div>
      <div><h3>What we built</h3><p>A live map and exception board that flags late loads automatically, driver check-ins by text message, and a tracking link for customers.</p></div>
    </div>
    <div class="case-results"><h3>Results</h3><ul><li>38% fewer dispatch calls in the first quarter</li><li>Late-load alerts reach dispatch in under 2 minutes</li><li>Customers track their own shipments, so status calls dropped</li></ul></div>
    <div class="btn-row"><a class="btn btn-primary" href="#contact" data-close-and-go>Start a similar project</a></div>
  </template>
</article>
      
<article class="project" data-cat="mobile">
  <svg class="shot" viewBox="0 0 400 260" aria-hidden="true" focusable="false"><rect width="400" height="260" fill="#1d5c63"/><circle cx="370" cy="20" r="120" fill="#f4f7f8" opacity=".08"/><circle cx="10" cy="260" r="100" fill="#ffb347" opacity=".2"/><rect x="40" y="70" width="76" height="130" rx="12" fill="#f4f7f8" opacity=".22"/><rect x="284" y="70" width="76" height="130" rx="12" fill="#f4f7f8" opacity=".22"/><rect x="146" y="26" width="128" height="228" rx="22" fill="#000" opacity=".22"/><rect x="136" y="14" width="128" height="228" rx="22" fill="#f4f7f8"/><rect x="170" y="24" width="60" height="6" rx="3" fill="#1d5c63" opacity=".4"/><rect x="148" y="44" width="104" height="58" rx="12" fill="#ffb347"/><rect x="158" y="56" width="40" height="7" rx="3.5" fill="#f4f7f8" opacity=".8"/><rect x="158" y="72" width="70" height="12" rx="4" fill="#f4f7f8"/><circle cx="160" cy="128" r="9" fill="#1d5c63" opacity=".85"/><rect x="176" y="121" width="60" height="7" rx="3" fill="#1d5c63" opacity=".8"/><rect x="176" y="133" width="34" height="5" rx="2.5" fill="#1d5c63" opacity=".35"/><circle cx="160" cy="156" r="9" fill="#1d5c63" opacity=".85"/><rect x="176" y="149" width="54" height="7" rx="3" fill="#1d5c63" opacity=".8"/><rect x="176" y="161" width="34" height="5" rx="2.5" fill="#1d5c63" opacity=".35"/><circle cx="160" cy="184" r="9" fill="#1d5c63" opacity=".85"/><rect x="176" y="177" width="48" height="7" rx="3" fill="#1d5c63" opacity=".8"/><rect x="176" y="189" width="34" height="5" rx="2.5" fill="#1d5c63" opacity=".35"/><circle cx="160" cy="212" r="9" fill="#1d5c63" opacity=".85"/><rect x="176" y="205" width="42" height="7" rx="3" fill="#1d5c63" opacity=".8"/><rect x="176" y="217" width="34" height="5" rx="2.5" fill="#1d5c63" opacity=".35"/></svg>
  <div class="project-body">
    <p class="project-kind">Mobile app</p>
    <h3>LedgerLeaf Mobile Banking</h3>
    <p>An iOS and Android money-management app built for a credit union's everyday members.</p>
    <p class="outcome">42,000 members onboarded in six months.</p>
    <ul class="tags"><li>Swift</li><li>Kotlin</li><li>Open banking APIs</li></ul>
    <button class="btn btn-ghost btn-small open-case" type="button">View case study</button>
  </div>
  <template>
    <h2>LedgerLeaf Mobile Banking</h2>
    <p class="project-kind">Mobile app</p>
    <div class="case-cols">
      <div><h3>The challenge</h3><p>Members relied on branch visits and a dated web banking site, and younger members were leaving for fintech apps.</p></div>
      <div><h3>What we built</h3><p>A mobile-first app for budgeting, instant transfers and card controls, connected to the credit union's existing core banking system through secure APIs.</p></div>
    </div>
    <div class="case-results"><h3>Results</h3><ul><li>42,000 members onboarded in six months</li><li>Mobile logins now outnumber web logins four to one</li><li>4.8-star rating in the app stores after launch</li></ul></div>
    <div class="btn-row"><a class="btn btn-primary" href="#contact" data-close-and-go>Start a similar project</a></div>
  </template>
</article>
      
<article class="project" data-cat="cloud">
  <svg class="shot" viewBox="0 0 400 260" aria-hidden="true" focusable="false"><rect width="400" height="260" fill="#5a2a3c"/><circle cx="370" cy="20" r="120" fill="#fbeff1" opacity=".08"/><circle cx="10" cy="260" r="100" fill="#ffb347" opacity=".2"/><rect x="34" y="40" width="72" height="92" rx="10" fill="#fbeff1"/><rect x="42" y="48" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="44" y="102" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="44" y="114" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/><rect x="118" y="40" width="72" height="92" rx="10" fill="#fbeff1"/><rect x="126" y="48" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="128" y="102" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="128" y="114" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/><rect x="202" y="40" width="72" height="92" rx="10" fill="#ffb347"/><rect x="210" y="48" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="212" y="102" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="212" y="114" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/><rect x="286" y="40" width="72" height="92" rx="10" fill="#fbeff1"/><rect x="294" y="48" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="296" y="102" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="296" y="114" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/><rect x="34" y="144" width="72" height="92" rx="10" fill="#fbeff1"/><rect x="42" y="152" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="44" y="206" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="44" y="218" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/><rect x="118" y="144" width="72" height="92" rx="10" fill="#fbeff1"/><rect x="126" y="152" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="128" y="206" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="128" y="218" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/><rect x="202" y="144" width="72" height="92" rx="10" fill="#fbeff1"/><rect x="210" y="152" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="212" y="206" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="212" y="218" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/><rect x="286" y="144" width="72" height="92" rx="10" fill="#fbeff1"/><rect x="294" y="152" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="296" y="206" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="296" y="218" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/></svg>
  <div class="project-body">
    <p class="project-kind">Cloud and managed services</p>
    <h3>Marketly Cloud Migration</h3>
    <p>Moved an online store from a single aging server to a scalable cloud setup, over one weekend.</p>
    <p class="outcome">Checkout is 2.4 times faster, and Black Friday ran with zero downtime.</p>
    <ul class="tags"><li>AWS</li><li>Terraform</li><li>24/7 monitoring</li></ul>
    <button class="btn btn-ghost btn-small open-case" type="button">View case study</button>
  </div>
  <template>
    <h2>Marketly Cloud Migration</h2>
    <p class="project-kind">Cloud and managed services</p>
    <div class="case-cols">
      <div><h3>The challenge</h3><p>A single aging server buckled during sales events, and every release risked taking the store offline.</p></div>
      <div><h3>What we built</h3><p>We rebuilt hosting on auto-scaling cloud infrastructure, automated the deployments, and moved the database with no customer-facing outage.</p></div>
    </div>
    <div class="case-results"><h3>Results</h3><ul><li>Checkout 2.4 times faster</li><li>Black Friday ran with zero downtime</li><li>Peak-season hosting costs 18% lower than before</li></ul></div>
    <div class="btn-row"><a class="btn btn-primary" href="#contact" data-close-and-go>Start a similar project</a></div>
  </template>
</article>
    </div>
    <p style="margin-top:2rem"><a class="text-link" href="#projects">View all projects</a></p>
  </div>
</section>

<section class="section">
  <div class="wrap">
    <div class="section-head"><h2>What clients say.</h2></div>
    <div class="slider" id="slider" aria-live="polite"><figure class="slide" style="margin:0"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#cfe3ea"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#1d5c63"/><rect x="52" y="76" width="16" height="16" fill="#c68642"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#c68642"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#c68642"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#2b1b12"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><blockquote class="quote-big">They pushed back on our feature list and they were right. The app we launched did less than we first asked for, and our members liked it far more.</blockquote><figcaption class="who"><strong>Daniel Reyes</strong>Product Lead, LedgerLeaf<span class="result">42,000 members onboarded in six months</span></figcaption></div></figure><figure class="slide" hidden style="margin:0"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#fbe0d3"/><circle cx="40" cy="44" r="10" fill="#14100d"/><circle cx="50" cy="34" r="11" fill="#14100d"/><circle cx="62" cy="30" r="11" fill="#14100d"/><circle cx="74" cy="34" r="11" fill="#14100d"/><circle cx="83" cy="44" r="10" fill="#14100d"/><circle cx="36" cy="58" r="8" fill="#14100d"/><circle cx="84" cy="58" r="8" fill="#14100d"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#c93a12"/><rect x="52" y="76" width="16" height="16" fill="#7a4a2a"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#7a4a2a"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#7a4a2a"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#14100d"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><blockquote class="quote-big">DigitalForgePro replaced three spreadsheets and a phone tree with one dashboard. Dispatchers adopted it in a week, and the team still answers when we call at 6 a.m.</blockquote><figcaption class="who"><strong>Amara Okafor</strong>Chief Operating Officer, Harborline Freight<span class="result">38% fewer dispatch calls</span></figcaption></div></figure><figure class="slide" hidden style="margin:0"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#e3e6f8"/><path d="M34 66C30 34 44 22 60 22C76 22 90 34 86 66L88 100H32Z" fill="#14100d"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#3a4a8c"/><rect x="52" y="76" width="16" height="16" fill="#c48a5a"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#c48a5a"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#c48a5a"/><path d="M37 56C34 30 50 24 62 25C76 26 85 36 83 56C78 44 70 38 56 40C48 42 41 46 37 56Z" fill="#14100d"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="51" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><circle cx="69" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><path d="M58 56h4" stroke="#1b1b1b" stroke-width="2"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><blockquote class="quote-big">Our scheduling system hasn't gone down once since launch. The monthly report tells us what changed, in language our front desk understands.</blockquote><figcaption class="who"><strong>Dr. Priya Nair</strong>Practice Director, ClinicFlow<span class="result">27% fewer missed appointments</span></figcaption></div></figure><figure class="slide" hidden style="margin:0"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#f3dfe4"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#5a2a3c"/><rect x="52" y="76" width="16" height="16" fill="#f0c8a0"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#f0c8a0"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#f0c8a0"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#7a4a22"/><path d="M39 60C39 80 48 88 60 88C72 88 81 80 81 60C77 70 70 74 60 74C50 74 43 70 39 60Z" fill="#7a4a22"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#f4e9e4" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><blockquote class="quote-big">They moved our store to the cloud over a single weekend. Black Friday was the quietest on-call week our team has ever had.</blockquote><figcaption class="who"><strong>Tom Whitfield</strong>Chief Technology Officer, Marketly<span class="result">Zero downtime on peak sales day</span></figcaption></div></figure><figure class="slide" hidden style="margin:0"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#e0efd9"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#2f5d3a"/><rect x="52" y="76" width="16" height="16" fill="#f6d6b8"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#f6d6b8"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#f6d6b8"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#b5562b"/><circle cx="60" cy="21" r="10" fill="#b5562b"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><blockquote class="quote-big">Our crews work where there is no signal. DigitalForgePro designed for that from the first sprint, not as an afterthought.</blockquote><figcaption class="who"><strong>Lena Hoffmann</strong>Head of Programs, FieldNotes<span class="result">Fully offline data capture</span></figcaption></div></figure><figure class="slide" hidden style="margin:0"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#d9e3ea"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#12202b"/><rect x="52" y="76" width="16" height="16" fill="#6b4423"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#6b4423"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#6b4423"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#0f0b09"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="51" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><circle cx="69" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><path d="M58 56h4" stroke="#1b1b1b" stroke-width="2"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><blockquote class="quote-big">Parents stopped emailing us about login problems, and we stopped worrying about patches and security updates. That used to take half my week.</blockquote><figcaption class="who"><strong>Marcus Bell</strong>IT Director, SchoolBridge<span class="result">81% fewer login tickets</span></figcaption></div></figure></div>
    <div class="slider-controls">
      <button class="slider-btn" id="slider-prev" type="button" aria-label="Previous testimonial">&lsaquo;</button>
      <span class="slider-count" id="slider-count">1 of 6</span>
      <button class="slider-btn" id="slider-next" type="button" aria-label="Next testimonial">&rsaquo;</button>
    </div>
    <p style="margin-top:1.5rem"><a class="text-link" href="#testimonials">Read all client stories</a></p>
  </div>
</section>

<section class="section section-white">
  <div class="wrap">
    <div class="section-head">
      <h2>Led by people you can call.</h2>
      <p class="lede">Our CEO and our manager are involved in every client relationship, from the first call to the monthly report.</p>
    </div>
    
<div class="leaders">
  <article class="leader"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#f4b942"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#12202b"/><rect x="52" y="76" width="16" height="16" fill="#e3b58a"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#e3b58a"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#e3b58a"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#3b2a20"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><h3>Andrew Parker</h3><p class="leader-role">Chief Executive Officer</p><span class="result">10 years of experience</span><p>Andrew founded DigitalForgePro after a decade of building and running software for companies in logistics, healthcare and retail. He sets our engineering standards, leads strategy, and stays close to every client relationship.</p></div></article>
  <article class="leader"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#cfe3ea"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#3a4a8c"/><rect x="52" y="76" width="16" height="16" fill="#f0c8a0"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#f0c8a0"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#f0c8a0"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#8a5a2b"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><h3>Daniel Wilson</h3><p class="leader-role">Manager</p><p>Daniel manages day-to-day delivery, making sure every project has a clear plan, an honest status and a team with what it needs. Once work begins, he is your main point of contact.</p></div></article>
</div>
    <p style="margin-top:2rem"><a class="text-link" href="#about">Meet the whole team</a></p>
  </div>
</section>

<section class="section">
  <div class="wrap">
    <div class="section-head">
      <h2>Latest from the blog.</h2>
      <p class="lede">Plain-language writing about building, running and securing software.</p>
    </div>
    <div class="blog-grid">
<article class="post-card" data-cat="Strategy">
  <svg class="cover" viewBox="0 0 640 360" preserveAspectRatio="xMidYMid slice" aria-hidden="true" focusable="false"><rect width="640" height="360" fill="#12202b"/><circle cx="590" cy="30" r="190" fill="#ffffff" opacity=".07"/><circle cx="30" cy="350" r="150" fill="#ff7a4d" opacity=".22"/><circle cx="40" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><rect x="150" y="255" width="42" height="60" rx="6" fill="#ffffff" opacity="0.85"/><rect x="214" y="225" width="42" height="90" rx="6" fill="#ffffff" opacity="0.85"/><rect x="278" y="195" width="42" height="120" rx="6" fill="#ffffff" opacity="0.85"/><rect x="342" y="155" width="42" height="160" rx="6" fill="#ffffff" opacity="0.85"/><rect x="406" y="110" width="42" height="205" rx="6" fill="#ffffff" opacity="0.85"/><rect x="470" y="60" width="42" height="255" rx="6" fill="#ff7a4d" opacity="1"/><polyline points="171,235 235,205 299,175 363,135 427,95 491,62" fill="none" stroke="#ff7a4d" stroke-width="5" stroke-linecap="round" stroke-linejoin="round" opacity=".9"/><circle cx="491" cy="62" r="9" fill="#ffffff" stroke="#ff7a4d" stroke-width="5"/></svg>
  <div class="post-body">
    <div class="post-meta"><span class="cat">Strategy</span><span>October 8, 2026</span><span>4 min read</span></div>
    <h3><a href="#blog/old-software-replace-or-rescue">Five signs your old software now costs more than it saves</a></h3>
    <p>Old software isn't automatically bad software. These five warning signs tell you when keeping it alive has stopped making sense.</p>
    <div class="byline"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#f4b942"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#12202b"/><rect x="52" y="76" width="16" height="16" fill="#e3b58a"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#e3b58a"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#e3b58a"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#3b2a20"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><strong>Andrew Parker</strong><span>Chief Executive Officer</span></div></div>
  </div>
</article>
<article class="post-card" data-cat="Cloud">
  <svg class="cover" viewBox="0 0 640 360" preserveAspectRatio="xMidYMid slice" aria-hidden="true" focusable="false"><rect width="640" height="360" fill="#1d5c63"/><circle cx="590" cy="30" r="190" fill="#ffffff" opacity=".07"/><circle cx="30" cy="350" r="150" fill="#ffb347" opacity=".22"/><circle cx="40" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="262" cy="150" r="52" fill="#ffffff"/><circle cx="332" cy="120" r="70" fill="#ffffff"/><circle cx="404" cy="152" r="50" fill="#ffffff"/><rect x="212" y="150" width="242" height="56" rx="28" fill="#ffffff"/><line x1="332" y1="206" x2="190" y2="270" stroke="#ffffff" stroke-width="3" stroke-dasharray="7 7" opacity=".7"/><rect x="154" y="270" width="72" height="40" rx="8" fill="#ffffff"/><circle cx="170" cy="290" r="5" fill="#ffb347"/><rect x="182" y="286" width="32" height="8" rx="4" fill="#1d5c63" opacity=".5"/><line x1="332" y1="206" x2="332" y2="270" stroke="#ffffff" stroke-width="3" stroke-dasharray="7 7" opacity=".7"/><rect x="296" y="270" width="72" height="40" rx="8" fill="#ffffff"/><circle cx="312" cy="290" r="5" fill="#ffb347"/><rect x="324" y="286" width="32" height="8" rx="4" fill="#1d5c63" opacity=".5"/><line x1="332" y1="206" x2="474" y2="270" stroke="#ffffff" stroke-width="3" stroke-dasharray="7 7" opacity=".7"/><rect x="438" y="270" width="72" height="40" rx="8" fill="#ffffff"/><circle cx="454" cy="290" r="5" fill="#ffb347"/><rect x="466" y="286" width="32" height="8" rx="4" fill="#1d5c63" opacity=".5"/></svg>
  <div class="post-body">
    <div class="post-meta"><span class="cat">Cloud</span><span>September 24, 2026</span><span>4 min read</span></div>
    <h3><a href="#blog/cloud-migration-without-panic">Cloud migration without the weekend panic</a></h3>
    <p>Moving to the cloud is a series of small, reversible steps. The calm migrations are the ones that planned the boring parts.</p>
    <div class="byline"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#cfe9dd"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#1d5c63"/><rect x="52" y="76" width="16" height="16" fill="#b97a4b"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#b97a4b"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#b97a4b"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#1a1210"/><path d="M39 60C39 80 48 88 60 88C72 88 81 80 81 60C77 70 70 74 60 74C50 74 43 70 39 60Z" fill="#1a1210"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#f4e9e4" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><strong>Ibrahim Yusuf</strong><span>Engineering Lead</span></div></div>
  </div>
</article>
<article class="post-card" data-cat="Reliability">
  <svg class="cover" viewBox="0 0 640 360" preserveAspectRatio="xMidYMid slice" aria-hidden="true" focusable="false"><rect width="640" height="360" fill="#3a4a8c"/><circle cx="590" cy="30" r="190" fill="#ffffff" opacity=".07"/><circle cx="30" cy="350" r="150" fill="#ffb347" opacity=".22"/><circle cx="40" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="320" cy="180" r="112" fill="none" stroke="#ffffff" stroke-opacity=".2" stroke-width="26"/><circle cx="320" cy="180" r="112" fill="none" stroke="#ffb347" stroke-width="26" stroke-linecap="round" stroke-dasharray="672 32" transform="rotate(-90 320 180)"/><text x="320" y="196" text-anchor="middle" font-family="Bricolage Grotesque, Public Sans, sans-serif" font-size="58" font-weight="800" fill="#ffffff">99.9%</text><text x="320" y="228" text-anchor="middle" font-family="Public Sans, sans-serif" font-size="20" font-weight="600" fill="#ffffff" opacity=".75">uptime</text></svg>
  <div class="post-body">
    <div class="post-meta"><span class="cat">Reliability</span><span>September 10, 2026</span><span>4 min read</span></div>
    <h3><a href="#blog/what-99-9-uptime-means">What 99.9% uptime actually means</a></h3>
    <p>Three nines sounds close to perfect. Here is what each level of uptime allows in real hours and minutes of downtime.</p>
    <div class="byline"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#dfe7ff"/><path d="M34 66C30 34 44 22 60 22C76 22 90 34 86 66L88 100H32Z" fill="#d8a657"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#2f5d3a"/><rect x="52" y="76" width="16" height="16" fill="#f6d1b1"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#f6d1b1"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#f6d1b1"/><path d="M37 56C34 30 50 24 62 25C76 26 85 36 83 56C78 44 70 38 56 40C48 42 41 46 37 56Z" fill="#d8a657"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><strong>Hannah Müller</strong><span>Head of Managed Services</span></div></div>
  </div>
</article></div>
    <p style="margin-top:2rem"><a class="text-link" href="#blog">Read all articles</a></p>
  </div>
</section>

<section class="cta-band dark">
  <div class="wrap">
    <h2>Tell us what you need built or kept running.</h2>
    <p>Share a few details and a senior engineer will reply within one business day.</p>
    <div class="btn-row"><a class="btn btn-primary" href="#contact">Contact us</a>
    <a class="btn btn-ghost" href="#projects">See our projects</a></div>
  </div>
</section>
</div>

<div class="page" id="page-services" hidden>

<section class="page-head dark">
  <div class="wrap">
    <nav class="crumbs" aria-label="Breadcrumb"><a href="#home">Home</a><span aria-hidden="true">/</span><span aria-current="page">Services</span></nav>
    <h1>Software built for you. Care that doesn't stop at launch.</h1>
    <p class="lede">Hire us to build something new, to look after what you already have, or both. Every engagement has a named lead and a written scope.</p>
  </div>
</section>
<nav class="subnav" aria-label="On this page"><div class="wrap"><span>Jump to</span>
  <a href="#services/build">Build</a><a href="#services/manage">Manage</a><a href="#services/models">Ways to work with us</a><a href="#services/faq">Questions</a>
</div></nav>

<section class="section">
  <div class="wrap">
    <div class="service-group" id="build">
      <div class="service-intro">
        <h2>Build</h2>
        <p>From first prototype to production, we design and engineer software your team and customers will actually use.</p>
        <a class="btn btn-primary" href="#contact">Start a project</a>
      </div>
      <div>
        <div class="service"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><rect x="3" y="4" width="18" height="16" rx="2"/><path d="M3 9h18M7 6.5h.01M10 6.5h.01"/></svg></span><div><h3>Custom web applications</h3><p>Customer portals, internal tools, dashboards and SaaS products, designed around your workflows and built to scale with your business.</p><p class="stack"><b>Typical tools:</b> React, Next.js, Node.js, Python, PostgreSQL</p></div></div>
        <div class="service"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><rect x="7" y="2.5" width="10" height="19" rx="2.5"/><path d="M11 18.5h2"/></svg></span><div><h3>Mobile apps</h3><p>iOS and Android apps that feel at home on each phone. We help you choose between native and cross-platform based on your needs, not our preferences.</p><p class="stack"><b>Typical tools:</b> Swift, Kotlin, React Native, Flutter</p></div></div>
        <div class="service"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><circle cx="6" cy="12" r="2.5"/><circle cx="18" cy="6" r="2.5"/><circle cx="18" cy="18" r="2.5"/><path d="M8.3 11l7.4-4M8.3 13l7.4 4"/></svg></span><div><h3>APIs and integrations</h3><p>Connect your systems so data moves on its own: payment providers, CRMs, accounting tools, and databases that predate everyone on your team.</p><p class="stack"><b>Typical tools:</b> REST, GraphQL, webhooks, message queues</p></div></div>
        <div class="service"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M7 18h10.5a4 4 0 0 0 .5-7.97A6 6 0 0 0 6.6 9.2 4.4 4.4 0 0 0 7 18z"/></svg></span><div><h3>Cloud setup and migration</h3><p>Move from a single server to a cloud setup that scales, with automated deployments so releases become routine instead of risky.</p><p class="stack"><b>Typical tools:</b> AWS, Azure, Google Cloud, Docker, Terraform</p></div></div>
        <div class="service"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M4 20l4-1 11-11-3-3L5 16z"/><path d="M14 7l3 3"/></svg></span><div><h3>Product design</h3><p>User research, flows, prototypes and design systems. We test with real users early, when changes are cheap.</p><p class="stack"><b>Typical tools:</b> Figma, usability testing, accessibility reviews</p></div></div>
      </div>
    </div>

    <div class="service-group" id="manage">
      <div class="service-intro">
        <h2>Manage</h2>
        <p>Software needs ongoing care. We take over the hosting, updates and on-call, whether we built it or not.</p>
        <a class="btn btn-primary" href="#contact">Ask about managed services</a>
      </div>
      <div>
        <div class="service"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M3 12h4l2-6 4 12 2-6h6"/></svg></span><div><h3>Managed hosting and monitoring</h3><p>We run your infrastructure and watch it continuously. Alerts reach an engineer, not an inbox nobody reads, and uptime targets are written into your agreement.</p><p class="stack"><b>Typical tools:</b> Datadog, Grafana, PagerDuty, cloud-native monitoring</p></div></div>
        <div class="service"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M14.5 6.5a4 4 0 0 0-5 5L4 17l3 3 5.5-5.5a4 4 0 0 0 5-5l-2.5 2.5-2.5-.5-.5-2.5z"/></svg></span><div><h3>Maintenance and updates</h3><p>Dependency patches, framework upgrades and bug fixes on a regular schedule, so small issues never grow into emergency rewrites.</p><p class="stack"><b>Typical tools:</b> Automated testing, staged releases</p></div></div>
        <div class="service"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M12 3l8 3v6c0 4.5-3.2 8-8 9-4.8-1-8-4.5-8-9V6z"/><path d="M9 12l2 2 4-4"/></svg></span><div><h3>Security and compliance</h3><p>Backups you can restore from, access reviews, vulnerability scanning and help preparing for GDPR, HIPAA or SOC 2 audits.</p><p class="stack"><b>Typical tools:</b> Encrypted backups, SSO, penetration-testing partners</p></div></div>
        <div class="service"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M4 14v-2a8 8 0 0 1 16 0v2"/><rect x="3" y="14" width="4" height="6" rx="1.5"/><rect x="17" y="14" width="4" height="6" rx="1.5"/></svg></span><div><h3>Support and on-call</h3><p>A named contact and agreed response times by severity. When something breaks, you reach a person who already knows your system.</p><p class="stack"><b>Typical tools:</b> Ticketing, shared chat channel, runbooks</p></div></div>
        <div class="service"><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M4 17a8 8 0 1 1 16 0"/><path d="M12 17l4-5"/></svg></span><div><h3>Performance and cost review</h3><p>A monthly look at speed, errors and cloud spend, with plain-language recommendations and the savings we found.</p><p class="stack"><b>Typical tools:</b> Load testing, cost dashboards</p></div></div>
      </div>
    </div>
  </div>
</section>

<section class="section section-white" id="models">
  <div class="wrap">
    <div class="section-head">
      <h2>Three ways to work with us.</h2>
      <p class="lede">Pick the one that matches where your product is today. You can switch as it grows.</p>
    </div>
    <div class="table-wrap">
      <table>
        <thead><tr><th scope="col"></th><th scope="col">Fixed project</th><th scope="col">Dedicated team</th><th scope="col">Managed retainer</th></tr></thead>
        <tbody>
          <tr><th scope="row">Best for</th><td>A clearly defined product or feature with a known outcome.</td><td>A larger product that will keep changing for a year or more.</td><td>Software that is live and needs dependable care.</td></tr>
          <tr><th scope="row">How it's priced</th><td>One price agreed after discovery, paid in milestones.</td><td>Monthly fee for a team of engineers and a designer.</td><td>Monthly fee based on the size of the system and response times.</td></tr>
          <tr><th scope="row">Typical length</th><td>6 to 16 weeks</td><td>6 months and up</td><td>12-month agreements, renewable</td></tr>
          <tr><th scope="row">What you get</th><td>Designed, tested software, handed over with documentation.</td><td>An embedded team that plans and ships with your staff.</td><td>Hosting, monitoring, updates and support under one agreement.</td></tr>
        </tbody>
      </table>
    </div>
  </div>
</section>

<section class="section" id="faq">
  <div class="wrap">
    <div class="section-head"><h2>Questions we hear often.</h2></div>
    <div class="faq">
      <details><summary>How long does a typical project take?</summary><p>Most first releases take 8 to 16 weeks. After discovery, you receive a written plan with milestones, so you know what arrives and when.</p></details>
      <details><summary>Who owns the code?</summary><p>You do. Source code, designs and cloud accounts are registered in your name from the start, so you are never locked in to working with us.</p></details>
      <details><summary>Can you take over software someone else built?</summary><p>Yes. We begin with a two-week review covering code quality, security and hosting, then give you a straightforward report and a plan to stabilize it.</p></details>
      <details><summary>Which technologies do you use?</summary><p>We choose tools to suit your problem and your team. Our most common stack is React, Node.js, Python and PostgreSQL on AWS, Azure or Google Cloud, with Swift, Kotlin or React Native for mobile.</p></details>
      <details><summary>What happens if something breaks after launch?</summary><p>Under a managed retainer, monitoring alerts our on-call engineer immediately. Your agreement lists response times by severity, and every incident ends with a written summary of the cause and the fix.</p></details>
    </div>
  </div>
</section>

<section class="cta-band dark">
  <div class="wrap">
    <h2>Tell us what you need built or kept running.</h2>
    <p>Share a few details and a senior engineer will reply within one business day.</p>
    <div class="btn-row"><a class="btn btn-primary" href="#contact">Contact us</a>
    <a class="btn btn-ghost" href="#projects">See our projects</a></div>
  </div>
</section>
</div>

<div class="page" id="page-projects" hidden>

<section class="page-head dark">
  <div class="wrap">
    <nav class="crumbs" aria-label="Breadcrumb"><a href="#home">Home</a><span aria-hidden="true">/</span><span aria-current="page">Projects</span></nav>
    <h1>Products we built, and still look after.</h1>
    <p class="lede">A selection of recent work across web, mobile and cloud. Each one has a measurable result, and most are still in our care.</p>
  </div>
</section>

<section class="section">
  <div class="wrap">
    <div class="filters" role="group" aria-label="Filter projects by type">
      <button class="filter" type="button" data-filter="all" aria-pressed="true">All projects</button>
      <button class="filter" type="button" data-filter="web" aria-pressed="false">Web applications</button>
      <button class="filter" type="button" data-filter="mobile" aria-pressed="false">Mobile apps</button>
      <button class="filter" type="button" data-filter="cloud" aria-pressed="false">Cloud and managed</button>
    </div>
    <p class="result-count" id="result-count" role="status">Showing 6 projects</p>
    <div class="project-grid" id="project-grid">
<article class="project" data-cat="web">
  <svg class="shot" viewBox="0 0 400 260" aria-hidden="true" focusable="false"><rect width="400" height="260" fill="#12202b"/><circle cx="370" cy="20" r="120" fill="#ffffff" opacity=".08"/><circle cx="10" cy="260" r="100" fill="#ff7a4d" opacity=".2"/><rect x="38" y="44" width="344" height="204" rx="12" fill="#000" opacity=".2"/><rect x="28" y="30" width="344" height="204" rx="12" fill="#ffffff"/><rect x="28" y="30" width="344" height="26" rx="12" fill="#12202b" opacity=".18"/><rect x="28" y="44" width="344" height="12" fill="#12202b" opacity=".18"/><rect x="44" y="68" width="98" height="40" rx="8" fill="#12202b" opacity=".12"/><rect x="52" y="76" width="36" height="6" rx="3" fill="#12202b" opacity=".5"/><rect x="52" y="90" width="56" height="10" rx="4" fill="#12202b"/><rect x="152" y="68" width="98" height="40" rx="8" fill="#12202b" opacity=".12"/><rect x="160" y="76" width="36" height="6" rx="3" fill="#12202b" opacity=".5"/><rect x="160" y="90" width="56" height="10" rx="4" fill="#12202b"/><rect x="260" y="68" width="98" height="40" rx="8" fill="#12202b" opacity=".12"/><rect x="268" y="76" width="36" height="6" rx="3" fill="#12202b" opacity=".5"/><rect x="268" y="90" width="56" height="10" rx="4" fill="#ff7a4d"/><rect x="54" y="180" width="24" height="34" rx="4" fill="#12202b" opacity="0.8"/><rect x="94" y="160" width="24" height="54" rx="4" fill="#12202b" opacity="0.8"/><rect x="134" y="170" width="24" height="44" rx="4" fill="#12202b" opacity="0.8"/><rect x="174" y="146" width="24" height="68" rx="4" fill="#12202b" opacity="0.8"/><rect x="214" y="158" width="24" height="56" rx="4" fill="#12202b" opacity="0.8"/><rect x="254" y="134" width="24" height="80" rx="4" fill="#12202b" opacity="0.8"/><rect x="294" y="152" width="24" height="62" rx="4" fill="#ff7a4d" opacity="1"/><polyline points="66,160 106,142 146,150 186,124 226,134 266,108 306,118" fill="none" stroke="#ff7a4d" stroke-width="4" stroke-linecap="round" stroke-linejoin="round"/></svg>
  <div class="project-body">
    <p class="project-kind">Web application</p>
    <h3>Harborline Freight Tracker</h3>
    <p>A live dispatch dashboard for a regional freight company, replacing three spreadsheets and a phone tree.</p>
    <p class="outcome">Dispatch calls fell by 38% in the first quarter.</p>
    <ul class="tags"><li>React</li><li>Node.js</li><li>PostgreSQL</li></ul>
    <button class="btn btn-ghost btn-small open-case" type="button">View case study</button>
  </div>
  <template>
    <h2>Harborline Freight Tracker</h2>
    <p class="project-kind">Web application</p>
    <div class="case-cols">
      <div><h3>The challenge</h3><p>Dispatchers tracked more than 200 trucks across three spreadsheets and constant phone calls, so delays surfaced hours late.</p></div>
      <div><h3>What we built</h3><p>A live map and exception board that flags late loads automatically, driver check-ins by text message, and a tracking link for customers.</p></div>
    </div>
    <div class="case-results"><h3>Results</h3><ul><li>38% fewer dispatch calls in the first quarter</li><li>Late-load alerts reach dispatch in under 2 minutes</li><li>Customers track their own shipments, so status calls dropped</li></ul></div>
    <div class="btn-row"><a class="btn btn-primary" href="#contact" data-close-and-go>Start a similar project</a></div>
  </template>
</article>
<article class="project" data-cat="mobile">
  <svg class="shot" viewBox="0 0 400 260" aria-hidden="true" focusable="false"><rect width="400" height="260" fill="#1d5c63"/><circle cx="370" cy="20" r="120" fill="#f4f7f8" opacity=".08"/><circle cx="10" cy="260" r="100" fill="#ffb347" opacity=".2"/><rect x="40" y="70" width="76" height="130" rx="12" fill="#f4f7f8" opacity=".22"/><rect x="284" y="70" width="76" height="130" rx="12" fill="#f4f7f8" opacity=".22"/><rect x="146" y="26" width="128" height="228" rx="22" fill="#000" opacity=".22"/><rect x="136" y="14" width="128" height="228" rx="22" fill="#f4f7f8"/><rect x="170" y="24" width="60" height="6" rx="3" fill="#1d5c63" opacity=".4"/><rect x="148" y="44" width="104" height="58" rx="12" fill="#ffb347"/><rect x="158" y="56" width="40" height="7" rx="3.5" fill="#f4f7f8" opacity=".8"/><rect x="158" y="72" width="70" height="12" rx="4" fill="#f4f7f8"/><circle cx="160" cy="128" r="9" fill="#1d5c63" opacity=".85"/><rect x="176" y="121" width="60" height="7" rx="3" fill="#1d5c63" opacity=".8"/><rect x="176" y="133" width="34" height="5" rx="2.5" fill="#1d5c63" opacity=".35"/><circle cx="160" cy="156" r="9" fill="#1d5c63" opacity=".85"/><rect x="176" y="149" width="54" height="7" rx="3" fill="#1d5c63" opacity=".8"/><rect x="176" y="161" width="34" height="5" rx="2.5" fill="#1d5c63" opacity=".35"/><circle cx="160" cy="184" r="9" fill="#1d5c63" opacity=".85"/><rect x="176" y="177" width="48" height="7" rx="3" fill="#1d5c63" opacity=".8"/><rect x="176" y="189" width="34" height="5" rx="2.5" fill="#1d5c63" opacity=".35"/><circle cx="160" cy="212" r="9" fill="#1d5c63" opacity=".85"/><rect x="176" y="205" width="42" height="7" rx="3" fill="#1d5c63" opacity=".8"/><rect x="176" y="217" width="34" height="5" rx="2.5" fill="#1d5c63" opacity=".35"/></svg>
  <div class="project-body">
    <p class="project-kind">Mobile app</p>
    <h3>LedgerLeaf Mobile Banking</h3>
    <p>An iOS and Android money-management app built for a credit union's everyday members.</p>
    <p class="outcome">42,000 members onboarded in six months.</p>
    <ul class="tags"><li>Swift</li><li>Kotlin</li><li>Open banking APIs</li></ul>
    <button class="btn btn-ghost btn-small open-case" type="button">View case study</button>
  </div>
  <template>
    <h2>LedgerLeaf Mobile Banking</h2>
    <p class="project-kind">Mobile app</p>
    <div class="case-cols">
      <div><h3>The challenge</h3><p>Members relied on branch visits and a dated web banking site, and younger members were leaving for fintech apps.</p></div>
      <div><h3>What we built</h3><p>A mobile-first app for budgeting, instant transfers and card controls, connected to the credit union's existing core banking system through secure APIs.</p></div>
    </div>
    <div class="case-results"><h3>Results</h3><ul><li>42,000 members onboarded in six months</li><li>Mobile logins now outnumber web logins four to one</li><li>4.8-star rating in the app stores after launch</li></ul></div>
    <div class="btn-row"><a class="btn btn-primary" href="#contact" data-close-and-go>Start a similar project</a></div>
  </template>
</article>
<article class="project" data-cat="web">
  <svg class="shot" viewBox="0 0 400 260" aria-hidden="true" focusable="false"><rect width="400" height="260" fill="#3a4a8c"/><circle cx="370" cy="20" r="120" fill="#ffffff" opacity=".08"/><circle cx="10" cy="260" r="100" fill="#ff7a4d" opacity=".2"/><rect x="38" y="44" width="344" height="204" rx="12" fill="#000" opacity=".2"/><rect x="28" y="30" width="344" height="204" rx="12" fill="#ffffff"/><path d="M28 42a12 12 0 0 1 12-12h58v204H40a12 12 0 0 1-12-12z" fill="#3a4a8c" opacity=".9"/><rect x="42" y="54" width="44" height="8" rx="4" fill="#ffffff" opacity="0.55"/><rect x="42" y="80" width="44" height="8" rx="4" fill="#ffffff" opacity="1"/><rect x="42" y="106" width="44" height="8" rx="4" fill="#ffffff" opacity="0.55"/><rect x="42" y="132" width="44" height="8" rx="4" fill="#ffffff" opacity="0.55"/><rect x="42" y="158" width="44" height="8" rx="4" fill="#ffffff" opacity="0.55"/><rect x="116" y="48" width="130" height="12" rx="6" fill="#3a4a8c" opacity=".85"/><rect x="116" y="76" width="240" height="28" rx="7" fill="#3a4a8c" opacity=".12"/><circle cx="132" cy="90" r="7" fill="#3a4a8c" opacity=".9"/><rect x="148" y="86" width="80" height="8" rx="4" fill="#3a4a8c" opacity=".7"/><rect x="116" y="112" width="240" height="28" rx="7" fill="#3a4a8c" opacity=".12"/><circle cx="132" cy="126" r="7" fill="#ff7a4d" opacity=".9"/><rect x="148" y="122" width="117" height="8" rx="4" fill="#3a4a8c" opacity=".7"/><rect x="116" y="148" width="240" height="28" rx="7" fill="#3a4a8c" opacity=".12"/><circle cx="132" cy="162" r="7" fill="#3a4a8c" opacity=".9"/><rect x="148" y="158" width="84" height="8" rx="4" fill="#3a4a8c" opacity=".7"/><rect x="116" y="184" width="240" height="28" rx="7" fill="#3a4a8c" opacity=".12"/><circle cx="132" cy="198" r="7" fill="#3a4a8c" opacity=".9"/><rect x="148" y="194" width="121" height="8" rx="4" fill="#3a4a8c" opacity=".7"/></svg>
  <div class="project-body">
    <p class="project-kind">Web application</p>
    <h3>ClinicFlow Scheduling</h3>
    <p>Online booking, reminders and waiting-room tools for a group of family clinics.</p>
    <p class="outcome">No-shows down 27%, and front-desk staff save about 11 hours a week.</p>
    <ul class="tags"><li>TypeScript</li><li>AWS</li><li>SMS reminders</li></ul>
    <button class="btn btn-ghost btn-small open-case" type="button">View case study</button>
  </div>
  <template>
    <h2>ClinicFlow Scheduling</h2>
    <p class="project-kind">Web application</p>
    <div class="case-cols">
      <div><h3>The challenge</h3><p>Phone-only booking overwhelmed front desks, and about one in five appointments was missed.</p></div>
      <div><h3>What we built</h3><p>Online booking, automatic reminders by text and email, and a waiting-room screen, with encrypted storage designed for health data rules.</p></div>
    </div>
    <div class="case-results"><h3>Results</h3><ul><li>No-shows down 27%</li><li>About 11 staff hours saved each week</li><li>No unplanned downtime since launch</li></ul></div>
    <div class="btn-row"><a class="btn btn-primary" href="#contact" data-close-and-go>Start a similar project</a></div>
  </template>
</article>
<article class="project" data-cat="cloud">
  <svg class="shot" viewBox="0 0 400 260" aria-hidden="true" focusable="false"><rect width="400" height="260" fill="#5a2a3c"/><circle cx="370" cy="20" r="120" fill="#fbeff1" opacity=".08"/><circle cx="10" cy="260" r="100" fill="#ffb347" opacity=".2"/><rect x="34" y="40" width="72" height="92" rx="10" fill="#fbeff1"/><rect x="42" y="48" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="44" y="102" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="44" y="114" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/><rect x="118" y="40" width="72" height="92" rx="10" fill="#fbeff1"/><rect x="126" y="48" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="128" y="102" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="128" y="114" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/><rect x="202" y="40" width="72" height="92" rx="10" fill="#ffb347"/><rect x="210" y="48" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="212" y="102" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="212" y="114" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/><rect x="286" y="40" width="72" height="92" rx="10" fill="#fbeff1"/><rect x="294" y="48" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="296" y="102" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="296" y="114" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/><rect x="34" y="144" width="72" height="92" rx="10" fill="#fbeff1"/><rect x="42" y="152" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="44" y="206" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="44" y="218" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/><rect x="118" y="144" width="72" height="92" rx="10" fill="#fbeff1"/><rect x="126" y="152" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="128" y="206" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="128" y="218" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/><rect x="202" y="144" width="72" height="92" rx="10" fill="#fbeff1"/><rect x="210" y="152" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="212" y="206" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="212" y="218" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/><rect x="286" y="144" width="72" height="92" rx="10" fill="#fbeff1"/><rect x="294" y="152" width="56" height="44" rx="6" fill="#5a2a3c" opacity=".25"/><rect x="296" y="206" width="40" height="7" rx="3" fill="#5a2a3c" opacity=".7"/><rect x="296" y="218" width="24" height="6" rx="3" fill="#5a2a3c" opacity=".4"/></svg>
  <div class="project-body">
    <p class="project-kind">Cloud and managed services</p>
    <h3>Marketly Cloud Migration</h3>
    <p>Moved an online store from a single aging server to a scalable cloud setup, over one weekend.</p>
    <p class="outcome">Checkout is 2.4 times faster, and Black Friday ran with zero downtime.</p>
    <ul class="tags"><li>AWS</li><li>Terraform</li><li>24/7 monitoring</li></ul>
    <button class="btn btn-ghost btn-small open-case" type="button">View case study</button>
  </div>
  <template>
    <h2>Marketly Cloud Migration</h2>
    <p class="project-kind">Cloud and managed services</p>
    <div class="case-cols">
      <div><h3>The challenge</h3><p>A single aging server buckled during sales events, and every release risked taking the store offline.</p></div>
      <div><h3>What we built</h3><p>We rebuilt hosting on auto-scaling cloud infrastructure, automated the deployments, and moved the database with no customer-facing outage.</p></div>
    </div>
    <div class="case-results"><h3>Results</h3><ul><li>Checkout 2.4 times faster</li><li>Black Friday ran with zero downtime</li><li>Peak-season hosting costs 18% lower than before</li></ul></div>
    <div class="btn-row"><a class="btn btn-primary" href="#contact" data-close-and-go>Start a similar project</a></div>
  </template>
</article>
<article class="project" data-cat="mobile">
  <svg class="shot" viewBox="0 0 400 260" aria-hidden="true" focusable="false"><rect width="400" height="260" fill="#2f5d3a"/><circle cx="370" cy="20" r="120" fill="#f3f8f2" opacity=".08"/><circle cx="10" cy="260" r="100" fill="#ffd166" opacity=".2"/><rect x="40" y="70" width="76" height="130" rx="12" fill="#f3f8f2" opacity=".22"/><rect x="284" y="70" width="76" height="130" rx="12" fill="#f3f8f2" opacity=".22"/><rect x="146" y="26" width="128" height="228" rx="22" fill="#000" opacity=".22"/><rect x="136" y="14" width="128" height="228" rx="22" fill="#f3f8f2"/><rect x="170" y="24" width="60" height="6" rx="3" fill="#2f5d3a" opacity=".4"/><rect x="148" y="44" width="104" height="58" rx="12" fill="#ffd166"/><rect x="158" y="56" width="40" height="7" rx="3.5" fill="#f3f8f2" opacity=".8"/><rect x="158" y="72" width="70" height="12" rx="4" fill="#f3f8f2"/><circle cx="160" cy="128" r="9" fill="#2f5d3a" opacity=".85"/><rect x="176" y="121" width="60" height="7" rx="3" fill="#2f5d3a" opacity=".8"/><rect x="176" y="133" width="34" height="5" rx="2.5" fill="#2f5d3a" opacity=".35"/><circle cx="160" cy="156" r="9" fill="#2f5d3a" opacity=".85"/><rect x="176" y="149" width="54" height="7" rx="3" fill="#2f5d3a" opacity=".8"/><rect x="176" y="161" width="34" height="5" rx="2.5" fill="#2f5d3a" opacity=".35"/><circle cx="160" cy="184" r="9" fill="#2f5d3a" opacity=".85"/><rect x="176" y="177" width="48" height="7" rx="3" fill="#2f5d3a" opacity=".8"/><rect x="176" y="189" width="34" height="5" rx="2.5" fill="#2f5d3a" opacity=".35"/><circle cx="160" cy="212" r="9" fill="#2f5d3a" opacity=".85"/><rect x="176" y="205" width="42" height="7" rx="3" fill="#2f5d3a" opacity=".8"/><rect x="176" y="217" width="34" height="5" rx="2.5" fill="#2f5d3a" opacity=".35"/></svg>
  <div class="project-body">
    <p class="project-kind">Mobile app</p>
    <h3>FieldNotes Offline App</h3>
    <p>A data-capture app for agronomists who work in fields with no signal, syncing when they return.</p>
    <p class="outcome">Crews log up to two weeks of readings offline, with no lost records.</p>
    <ul class="tags"><li>React Native</li><li>SQLite</li><li>Background sync</li></ul>
    <button class="btn btn-ghost btn-small open-case" type="button">View case study</button>
  </div>
  <template>
    <h2>FieldNotes Offline App</h2>
    <p class="project-kind">Mobile app</p>
    <div class="case-cols">
      <div><h3>The challenge</h3><p>Agronomists work in fields without coverage and were re-typing paper notes at night.</p></div>
      <div><h3>What we built</h3><p>An offline-first app that stores readings, photos and GPS points on the phone and syncs safely whenever a signal returns.</p></div>
    </div>
    <div class="case-results"><h3>Results</h3><ul><li>Up to two weeks of work offline</li><li>No lost records in the first season</li><li>Report preparation cut from days to hours</li></ul></div>
    <div class="btn-row"><a class="btn btn-primary" href="#contact" data-close-and-go>Start a similar project</a></div>
  </template>
</article>
<article class="project" data-cat="cloud">
  <svg class="shot" viewBox="0 0 400 260" aria-hidden="true" focusable="false"><rect width="400" height="260" fill="#12202b"/><circle cx="370" cy="20" r="120" fill="#dfe7ec" opacity=".08"/><circle cx="10" cy="260" r="100" fill="#ff7a4d" opacity=".2"/><line x1="200" y1="130" x2="86" y2="66" stroke="#dfe7ec" stroke-width="3" opacity=".5"/><line x1="200" y1="130" x2="200" y2="36" stroke="#dfe7ec" stroke-width="3" opacity=".5"/><line x1="200" y1="130" x2="318" y2="74" stroke="#dfe7ec" stroke-width="3" opacity=".5"/><line x1="200" y1="130" x2="68" y2="188" stroke="#dfe7ec" stroke-width="3" opacity=".5"/><line x1="200" y1="130" x2="200" y2="220" stroke="#dfe7ec" stroke-width="3" opacity=".5"/><line x1="200" y1="130" x2="336" y2="186" stroke="#dfe7ec" stroke-width="3" opacity=".5"/><circle cx="86" cy="66" r="20" fill="#dfe7ec"/><rect x="78" y="60" width="16" height="12" rx="3" fill="#12202b" opacity=".7"/><circle cx="200" cy="36" r="20" fill="#dfe7ec"/><rect x="192" y="30" width="16" height="12" rx="3" fill="#12202b" opacity=".7"/><circle cx="318" cy="74" r="20" fill="#dfe7ec"/><rect x="310" y="68" width="16" height="12" rx="3" fill="#12202b" opacity=".7"/><circle cx="68" cy="188" r="20" fill="#dfe7ec"/><rect x="60" y="182" width="16" height="12" rx="3" fill="#12202b" opacity=".7"/><circle cx="200" cy="220" r="20" fill="#dfe7ec"/><rect x="192" y="214" width="16" height="12" rx="3" fill="#12202b" opacity=".7"/><circle cx="336" cy="186" r="20" fill="#dfe7ec"/><rect x="328" y="180" width="16" height="12" rx="3" fill="#12202b" opacity=".7"/><circle cx="200" cy="130" r="42" fill="#ff7a4d"/><circle cx="200" cy="130" r="16" fill="#12202b"/></svg>
  <div class="project-body">
    <p class="project-kind">Cloud and managed services</p>
    <h3>SchoolBridge Parent Portal</h3>
    <p>A single sign-on portal connecting a school district's grading, attendance and messaging systems.</p>
    <p class="outcome">Login support tickets dropped by 81%, and we now run it under a managed retainer.</p>
    <ul class="tags"><li>Single sign-on</li><li>Azure</li><li>Managed hosting</li></ul>
    <button class="btn btn-ghost btn-small open-case" type="button">View case study</button>
  </div>
  <template>
    <h2>SchoolBridge Parent Portal</h2>
    <p class="project-kind">Cloud and managed services</p>
    <div class="case-cols">
      <div><h3>The challenge</h3><p>Parents needed five separate logins for grades, attendance and messaging, and the help desk was swamped with reset requests.</p></div>
      <div><h3>What we built</h3><p>One single sign-on portal in front of the district's existing systems, hosted, patched and monitored by us.</p></div>
    </div>
    <div class="case-results"><h3>Results</h3><ul><li>81% fewer login tickets</li><li>Parent logins tripled in the first term</li><li>Patched and monitored under our managed retainer</li></ul></div>
    <div class="btn-row"><a class="btn btn-primary" href="#contact" data-close-and-go>Start a similar project</a></div>
  </template>
</article></div>
  </div>
</section>

<section class="cta-band dark">
  <div class="wrap">
    <h2>Tell us what you need built or kept running.</h2>
    <p>Share a few details and a senior engineer will reply within one business day.</p>
    <div class="btn-row"><a class="btn btn-primary" href="#contact">Contact us</a>
    <a class="btn btn-ghost" href="#projects">See our projects</a></div>
  </div>
</section>
</div>

<div class="page" id="page-testimonials" hidden>

<section class="page-head dark">
  <div class="wrap">
    <nav class="crumbs" aria-label="Breadcrumb"><a href="#home">Home</a><span aria-hidden="true">/</span><span aria-current="page">Testimonials</span></nav>
    <h1>What clients say after launch.</h1>
    <p class="lede">The real test of software is how it runs six months later. Here is how our clients describe working with us.</p>
  </div>
</section>

<section class="section">
  <div class="wrap">
    <figure class="feature-quote" style="margin:0">
      <span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#cfe3ea"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#1d5c63"/><rect x="52" y="76" width="16" height="16" fill="#c68642"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#c68642"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#c68642"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#2b1b12"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span>
      <div>
        <blockquote class="quote-big">They pushed back on our feature list and they were right. The app we launched did less than we first asked for, and our members liked it far more.</blockquote>
        <figcaption class="who"><strong>Daniel Reyes</strong>Product Lead, LedgerLeaf<span class="result">42,000 members onboarded in six months</span></figcaption>
      </div>
    </figure>
  </div>
</section>

<section class="section section-white">
  <div class="wrap"><div class="quotes"><figure class="q"><blockquote><p>DigitalForgePro replaced three spreadsheets and a phone tree with one dashboard. Dispatchers adopted it in a week, and the team still answers when we call at 6 a.m.</p></blockquote><figcaption><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#fbe0d3"/><circle cx="40" cy="44" r="10" fill="#14100d"/><circle cx="50" cy="34" r="11" fill="#14100d"/><circle cx="62" cy="30" r="11" fill="#14100d"/><circle cx="74" cy="34" r="11" fill="#14100d"/><circle cx="83" cy="44" r="10" fill="#14100d"/><circle cx="36" cy="58" r="8" fill="#14100d"/><circle cx="84" cy="58" r="8" fill="#14100d"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#c93a12"/><rect x="52" y="76" width="16" height="16" fill="#7a4a2a"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#7a4a2a"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#7a4a2a"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#14100d"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div class="who"><strong>Amara Okafor</strong>Chief Operating Officer, Harborline Freight<br><span class="result">38% fewer dispatch calls</span></div></figcaption></figure><figure class="q"><blockquote><p>Our scheduling system hasn't gone down once since launch. The monthly report tells us what changed, in language our front desk understands.</p></blockquote><figcaption><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#e3e6f8"/><path d="M34 66C30 34 44 22 60 22C76 22 90 34 86 66L88 100H32Z" fill="#14100d"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#3a4a8c"/><rect x="52" y="76" width="16" height="16" fill="#c48a5a"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#c48a5a"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#c48a5a"/><path d="M37 56C34 30 50 24 62 25C76 26 85 36 83 56C78 44 70 38 56 40C48 42 41 46 37 56Z" fill="#14100d"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="51" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><circle cx="69" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><path d="M58 56h4" stroke="#1b1b1b" stroke-width="2"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div class="who"><strong>Dr. Priya Nair</strong>Practice Director, ClinicFlow<br><span class="result">27% fewer missed appointments</span></div></figcaption></figure><figure class="q"><blockquote><p>They moved our store to the cloud over a single weekend. Black Friday was the quietest on-call week our team has ever had.</p></blockquote><figcaption><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#f3dfe4"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#5a2a3c"/><rect x="52" y="76" width="16" height="16" fill="#f0c8a0"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#f0c8a0"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#f0c8a0"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#7a4a22"/><path d="M39 60C39 80 48 88 60 88C72 88 81 80 81 60C77 70 70 74 60 74C50 74 43 70 39 60Z" fill="#7a4a22"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#f4e9e4" stroke-width="2.2" stroke-linecap="round"/></svg></span><div class="who"><strong>Tom Whitfield</strong>Chief Technology Officer, Marketly<br><span class="result">Zero downtime on peak sales day</span></div></figcaption></figure><figure class="q"><blockquote><p>Our crews work where there is no signal. DigitalForgePro designed for that from the first sprint, not as an afterthought.</p></blockquote><figcaption><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#e0efd9"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#2f5d3a"/><rect x="52" y="76" width="16" height="16" fill="#f6d6b8"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#f6d6b8"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#f6d6b8"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#b5562b"/><circle cx="60" cy="21" r="10" fill="#b5562b"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div class="who"><strong>Lena Hoffmann</strong>Head of Programs, FieldNotes<br><span class="result">Fully offline data capture</span></div></figcaption></figure><figure class="q"><blockquote><p>Parents stopped emailing us about login problems, and we stopped worrying about patches and security updates. That used to take half my week.</p></blockquote><figcaption><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#d9e3ea"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#12202b"/><rect x="52" y="76" width="16" height="16" fill="#6b4423"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#6b4423"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#6b4423"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#0f0b09"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="51" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><circle cx="69" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><path d="M58 56h4" stroke="#1b1b1b" stroke-width="2"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div class="who"><strong>Marcus Bell</strong>IT Director, SchoolBridge<br><span class="result">81% fewer login tickets</span></div></figcaption></figure></div></div>
</section>

<section class="cta-band dark">
  <div class="wrap">
    <h2>Tell us what you need built or kept running.</h2>
    <p>Share a few details and a senior engineer will reply within one business day.</p>
    <div class="btn-row"><a class="btn btn-primary" href="#contact">Contact us</a>
    <a class="btn btn-ghost" href="#projects">See our projects</a></div>
  </div>
</section>
</div>

<div class="page" id="page-about" hidden>

<section class="page-head dark">
  <div class="wrap">
    <nav class="crumbs" aria-label="Breadcrumb"><a href="#home">Home</a><span aria-hidden="true">/</span><span aria-current="page">About</span></nav>
    <h1>A software studio that stays after launch.</h1>
    <p class="lede">DigitalForgePro is a team of engineers, designers and operations specialists who build software and then run it.</p>
  </div>
</section>

<section class="section">
  <div class="wrap story">
    <div><h2>Why we exist.</h2></div>
    <div>
      <p>Our CEO, Andrew Parker, started DigitalForgePro after ten years of watching too many software projects ship late and then slowly fall apart in production. The team that built the product moved on, and nobody was left who understood it.</p>
      <p>So we set up a different kind of studio. The people who design and build your software are the same people who host it, monitor it and answer the phone when something goes wrong. That makes us more careful about what we build, because we are the ones who live with it.</p>
      <p>Today we work with startups, clinics, schools, logistics firms and retailers. Our clients are rarely technology companies. They are businesses that need software to work, every day, without drama.</p>
    </div>
  </div>
</section>

<section class="section section-white">
  <div class="wrap">
    <div class="section-head">
      <h2>Leadership.</h2>
      <p class="lede">The two people accountable for every project we deliver.</p>
    </div>
    
<div class="leaders">
  <article class="leader"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#f4b942"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#12202b"/><rect x="52" y="76" width="16" height="16" fill="#e3b58a"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#e3b58a"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#e3b58a"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#3b2a20"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><h3>Andrew Parker</h3><p class="leader-role">Chief Executive Officer</p><span class="result">10 years of experience</span><p>Andrew founded DigitalForgePro after a decade of building and running software for companies in logistics, healthcare and retail. He sets our engineering standards, leads strategy, and stays close to every client relationship.</p></div></article>
  <article class="leader"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#cfe3ea"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#3a4a8c"/><rect x="52" y="76" width="16" height="16" fill="#f0c8a0"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#f0c8a0"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#f0c8a0"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#8a5a2b"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><h3>Daniel Wilson</h3><p class="leader-role">Manager</p><p>Daniel manages day-to-day delivery, making sure every project has a clear plan, an honest status and a team with what it needs. Once work begins, he is your main point of contact.</p></div></article>
</div>
  </div>
</section>

<section class="section">
  <div class="wrap">
    <div class="section-head"><h2>How we work.</h2></div>
    <dl class="values">
      <div><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><circle cx="12" cy="12" r="8"/><circle cx="12" cy="12" r="3"/></svg></span><div><dt>We say what we would cut.</dt><dd>Smaller scope ships sooner and teaches you more. We will tell you which features can wait.</dd></div></div>
      <div><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M12 3l8 3v6c0 4.5-3.2 8-8 9-4.8-1-8-4.5-8-9V6z"/><path d="M9 12l2 2 4-4"/></svg></span><div><dt>We own what we ship.</dt><dd>If our work fails, we fix it, and we write up what happened and how we will prevent it.</dd></div></div>
      <div><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M4 5h16v11H9l-5 4z"/></svg></span><div><dt>Plain language, always.</dt><dd>Reports, estimates and incident notes are written for the person who has to decide, not for other engineers.</dd></div></div>
      <div><span class="icon"><svg viewBox="0 0 24 24" aria-hidden="true" focusable="false"><path d="M5 12a7 7 0 0 1 12-5l2 2M19 12a7 7 0 0 1-12 5l-2-2"/><path d="M19 4v5h-5M5 20v-5h5"/></svg></span><div><dt>Small steps, shipped often.</dt><dd>Working software every two weeks keeps risk low and lets you change direction early.</dd></div></div>
    </dl>
  </div>
</section>

<section class="section section-white">
  <div class="wrap">
    <div class="section-head"><h2>The wider team.</h2>
    <p class="lede">A small, senior team. You will know who is working on your product by name.</p></div>
    <ul class="team"><li class="person"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#7cc4f5"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#12202b"/><rect x="52" y="76" width="16" height="16" fill="#8d5524"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#8d5524"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#8d5524"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#1a1210"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="51" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><circle cx="69" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><path d="M58 56h4" stroke="#1b1b1b" stroke-width="2"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><strong>Kwame Mensah</strong><span>Chief Technology Officer</span></li><li class="person"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#ffd1c2"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#c93a12"/><rect x="52" y="76" width="16" height="16" fill="#f1c27d"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#f1c27d"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#f1c27d"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#5a2a1c"/><circle cx="60" cy="21" r="10" fill="#5a2a1c"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><strong>Sofia Alvarez</strong><span>Head of Design</span></li><li class="person"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#cfe9dd"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#1d5c63"/><rect x="52" y="76" width="16" height="16" fill="#b97a4b"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#b97a4b"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#b97a4b"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#1a1210"/><path d="M39 60C39 80 48 88 60 88C72 88 81 80 81 60C77 70 70 74 60 74C50 74 43 70 39 60Z" fill="#1a1210"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#f4e9e4" stroke-width="2.2" stroke-linecap="round"/></svg></span><strong>Ibrahim Yusuf</strong><span>Engineering Lead</span></li><li class="person"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#dfe7ff"/><path d="M34 66C30 34 44 22 60 22C76 22 90 34 86 66L88 100H32Z" fill="#d8a657"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#2f5d3a"/><rect x="52" y="76" width="16" height="16" fill="#f6d1b1"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#f6d1b1"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#f6d1b1"/><path d="M37 56C34 30 50 24 62 25C76 26 85 36 83 56C78 44 70 38 56 40C48 42 41 46 37 56Z" fill="#d8a657"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><strong>Hannah Müller</strong><span>Head of Managed Services</span></li></ul>
  </div>
</section>

<section class="section">
  <div class="wrap">
    <div class="section-head"><h2>Our story so far.</h2></div>
    <ol class="timeline">
      <li><b>2019</b><span>Andrew Parker founds DigitalForgePro and ships the first client project, a booking system for a local clinic.</span></li>
      <li><b>2021</b><span>We add managed hosting and on-call after clients ask us to keep running what we built.</span></li>
      <li><b>2023</b><span>The team grows to 20 across design, engineering and operations, and we open our first mobile practice.</span></li>
      <li><b>2025</b><span>We reach 60 products under management, with a median of under four minutes to respond to a critical alert.</span></li>
      <li><b>Today</b><span>We are choosing our next few partners carefully. If your project looks like a fit, we would like to hear about it.</span></li>
    </ol>
  </div>
</section>

<section class="cta-band dark">
  <div class="wrap">
    <h2>Tell us what you need built or kept running.</h2>
    <p>Share a few details and a senior engineer will reply within one business day.</p>
    <div class="btn-row"><a class="btn btn-primary" href="#contact">Contact us</a>
    <a class="btn btn-ghost" href="#projects">See our projects</a></div>
  </div>
</section>
</div>

<div class="page" id="page-blog" hidden>
<div id="blog-list">

<section class="page-head dark">
  <div class="wrap">
    <nav class="crumbs" aria-label="Breadcrumb"><a href="#home">Home</a><span aria-hidden="true">/</span><span aria-current="page">Blog</span></nav>
    <h1>Notes from the forge.</h1>
    <p class="lede">Plain-language writing about building, running and securing software, from the people who do it every day.</p>
  </div>
</section>
<section class="section">
  <div class="wrap">
    <div class="filters" role="group" aria-label="Filter articles by topic">
      <button class="blog-filter" type="button" data-cat="all" aria-pressed="true">All topics</button>
      <button class="blog-filter" type="button" data-cat="Strategy" aria-pressed="false">Strategy</button><button class="blog-filter" type="button" data-cat="Cloud" aria-pressed="false">Cloud</button><button class="blog-filter" type="button" data-cat="Reliability" aria-pressed="false">Reliability</button><button class="blog-filter" type="button" data-cat="Security" aria-pressed="false">Security</button>
    </div>
    <p class="result-count" id="blog-count" role="status">Showing 4 articles</p>
    <div class="blog-grid" id="blog-grid">
<article class="post-card featured" data-cat="Strategy">
  <svg class="cover" viewBox="0 0 640 360" preserveAspectRatio="xMidYMid slice" aria-hidden="true" focusable="false"><rect width="640" height="360" fill="#12202b"/><circle cx="590" cy="30" r="190" fill="#ffffff" opacity=".07"/><circle cx="30" cy="350" r="150" fill="#ff7a4d" opacity=".22"/><circle cx="40" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><rect x="150" y="255" width="42" height="60" rx="6" fill="#ffffff" opacity="0.85"/><rect x="214" y="225" width="42" height="90" rx="6" fill="#ffffff" opacity="0.85"/><rect x="278" y="195" width="42" height="120" rx="6" fill="#ffffff" opacity="0.85"/><rect x="342" y="155" width="42" height="160" rx="6" fill="#ffffff" opacity="0.85"/><rect x="406" y="110" width="42" height="205" rx="6" fill="#ffffff" opacity="0.85"/><rect x="470" y="60" width="42" height="255" rx="6" fill="#ff7a4d" opacity="1"/><polyline points="171,235 235,205 299,175 363,135 427,95 491,62" fill="none" stroke="#ff7a4d" stroke-width="5" stroke-linecap="round" stroke-linejoin="round" opacity=".9"/><circle cx="491" cy="62" r="9" fill="#ffffff" stroke="#ff7a4d" stroke-width="5"/></svg>
  <div class="post-body">
    <div class="post-meta"><span class="cat">Strategy</span><span>October 8, 2026</span><span>4 min read</span></div>
    <h3><a href="#blog/old-software-replace-or-rescue">Five signs your old software now costs more than it saves</a></h3>
    <p>Old software isn't automatically bad software. These five warning signs tell you when keeping it alive has stopped making sense.</p>
    <div class="byline"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#f4b942"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#12202b"/><rect x="52" y="76" width="16" height="16" fill="#e3b58a"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#e3b58a"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#e3b58a"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#3b2a20"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><strong>Andrew Parker</strong><span>Chief Executive Officer</span></div></div>
  </div>
</article>
<article class="post-card" data-cat="Cloud">
  <svg class="cover" viewBox="0 0 640 360" preserveAspectRatio="xMidYMid slice" aria-hidden="true" focusable="false"><rect width="640" height="360" fill="#1d5c63"/><circle cx="590" cy="30" r="190" fill="#ffffff" opacity=".07"/><circle cx="30" cy="350" r="150" fill="#ffb347" opacity=".22"/><circle cx="40" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="262" cy="150" r="52" fill="#ffffff"/><circle cx="332" cy="120" r="70" fill="#ffffff"/><circle cx="404" cy="152" r="50" fill="#ffffff"/><rect x="212" y="150" width="242" height="56" rx="28" fill="#ffffff"/><line x1="332" y1="206" x2="190" y2="270" stroke="#ffffff" stroke-width="3" stroke-dasharray="7 7" opacity=".7"/><rect x="154" y="270" width="72" height="40" rx="8" fill="#ffffff"/><circle cx="170" cy="290" r="5" fill="#ffb347"/><rect x="182" y="286" width="32" height="8" rx="4" fill="#1d5c63" opacity=".5"/><line x1="332" y1="206" x2="332" y2="270" stroke="#ffffff" stroke-width="3" stroke-dasharray="7 7" opacity=".7"/><rect x="296" y="270" width="72" height="40" rx="8" fill="#ffffff"/><circle cx="312" cy="290" r="5" fill="#ffb347"/><rect x="324" y="286" width="32" height="8" rx="4" fill="#1d5c63" opacity=".5"/><line x1="332" y1="206" x2="474" y2="270" stroke="#ffffff" stroke-width="3" stroke-dasharray="7 7" opacity=".7"/><rect x="438" y="270" width="72" height="40" rx="8" fill="#ffffff"/><circle cx="454" cy="290" r="5" fill="#ffb347"/><rect x="466" y="286" width="32" height="8" rx="4" fill="#1d5c63" opacity=".5"/></svg>
  <div class="post-body">
    <div class="post-meta"><span class="cat">Cloud</span><span>September 24, 2026</span><span>4 min read</span></div>
    <h3><a href="#blog/cloud-migration-without-panic">Cloud migration without the weekend panic</a></h3>
    <p>Moving to the cloud is a series of small, reversible steps. The calm migrations are the ones that planned the boring parts.</p>
    <div class="byline"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#cfe9dd"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#1d5c63"/><rect x="52" y="76" width="16" height="16" fill="#b97a4b"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#b97a4b"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#b97a4b"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#1a1210"/><path d="M39 60C39 80 48 88 60 88C72 88 81 80 81 60C77 70 70 74 60 74C50 74 43 70 39 60Z" fill="#1a1210"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#f4e9e4" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><strong>Ibrahim Yusuf</strong><span>Engineering Lead</span></div></div>
  </div>
</article>
<article class="post-card" data-cat="Reliability">
  <svg class="cover" viewBox="0 0 640 360" preserveAspectRatio="xMidYMid slice" aria-hidden="true" focusable="false"><rect width="640" height="360" fill="#3a4a8c"/><circle cx="590" cy="30" r="190" fill="#ffffff" opacity=".07"/><circle cx="30" cy="350" r="150" fill="#ffb347" opacity=".22"/><circle cx="40" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="320" cy="180" r="112" fill="none" stroke="#ffffff" stroke-opacity=".2" stroke-width="26"/><circle cx="320" cy="180" r="112" fill="none" stroke="#ffb347" stroke-width="26" stroke-linecap="round" stroke-dasharray="672 32" transform="rotate(-90 320 180)"/><text x="320" y="196" text-anchor="middle" font-family="Bricolage Grotesque, Public Sans, sans-serif" font-size="58" font-weight="800" fill="#ffffff">99.9%</text><text x="320" y="228" text-anchor="middle" font-family="Public Sans, sans-serif" font-size="20" font-weight="600" fill="#ffffff" opacity=".75">uptime</text></svg>
  <div class="post-body">
    <div class="post-meta"><span class="cat">Reliability</span><span>September 10, 2026</span><span>4 min read</span></div>
    <h3><a href="#blog/what-99-9-uptime-means">What 99.9% uptime actually means</a></h3>
    <p>Three nines sounds close to perfect. Here is what each level of uptime allows in real hours and minutes of downtime.</p>
    <div class="byline"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#dfe7ff"/><path d="M34 66C30 34 44 22 60 22C76 22 90 34 86 66L88 100H32Z" fill="#d8a657"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#2f5d3a"/><rect x="52" y="76" width="16" height="16" fill="#f6d1b1"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#f6d1b1"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#f6d1b1"/><path d="M37 56C34 30 50 24 62 25C76 26 85 36 83 56C78 44 70 38 56 40C48 42 41 46 37 56Z" fill="#d8a657"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><strong>Hannah Müller</strong><span>Head of Managed Services</span></div></div>
  </div>
</article>
<article class="post-card" data-cat="Security">
  <svg class="cover" viewBox="0 0 640 360" preserveAspectRatio="xMidYMid slice" aria-hidden="true" focusable="false"><rect width="640" height="360" fill="#5a2a3c"/><circle cx="590" cy="30" r="190" fill="#fbeff1" opacity=".07"/><circle cx="30" cy="350" r="150" fill="#ffb347" opacity=".22"/><circle cx="40" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="40" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="40" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="40" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="40" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="120" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="120" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="120" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="120" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="120" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="200" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="200" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="200" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="200" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="200" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="280" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="280" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="280" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="280" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="280" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="360" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="360" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="360" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="360" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="360" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="440" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="440" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="440" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="440" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="440" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="520" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="520" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="520" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="520" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="520" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="600" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="600" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="600" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="600" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="600" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><path d="M320 62L436 106V192C436 256 388 296 320 318C252 296 204 256 204 192V106Z" fill="#fbeff1"/><path d="M320 82L418 118V192C418 244 380 278 320 298C260 278 222 244 222 192V118Z" fill="#5a2a3c" opacity=".12"/><path d="M268 190L304 226L376 148" fill="none" stroke="#ffb347" stroke-width="20" stroke-linecap="round" stroke-linejoin="round"/></svg>
  <div class="post-body">
    <div class="post-meta"><span class="cat">Security</span><span>August 27, 2026</span><span>5 min read</span></div>
    <h3><a href="#blog/security-basics-small-teams">Six security basics any team can do this month</a></h3>
    <p>You do not need a security department to avoid the most common breaches. Start with these six habits.</p>
    <div class="byline"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#7cc4f5"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#12202b"/><rect x="52" y="76" width="16" height="16" fill="#8d5524"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#8d5524"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#8d5524"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#1a1210"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="51" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><circle cx="69" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><path d="M58 56h4" stroke="#1b1b1b" stroke-width="2"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><strong>Kwame Mensah</strong><span>Chief Technology Officer</span></div></div>
  </div>
</article></div>
  </div>
</section>

<section class="cta-band dark">
  <div class="wrap">
    <h2>Tell us what you need built or kept running.</h2>
    <p>Share a few details and a senior engineer will reply within one business day.</p>
    <div class="btn-row"><a class="btn btn-primary" href="#contact">Contact us</a>
    <a class="btn btn-ghost" href="#projects">See our projects</a></div>
  </div>
</section>
</div>

<article class="post" id="post-old-software-replace-or-rescue" data-title="Five signs your old software now costs more than it saves" hidden>
  <section class="post-head dark">
    <div class="narrow">
      <nav class="crumbs" aria-label="Breadcrumb"><a href="#home">Home</a><span aria-hidden="true">/</span><a href="#blog">Blog</a><span aria-hidden="true">/</span><span aria-current="page">Strategy</span></nav>
      <div class="post-meta"><span class="cat">Strategy</span><span>October 8, 2026</span><span>4 min read</span></div>
      <h1>Five signs your old software now costs more than it saves</h1>
      <div class="post-byline"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#f4b942"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#12202b"/><rect x="52" y="76" width="16" height="16" fill="#e3b58a"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#e3b58a"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#e3b58a"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#3b2a20"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><strong>Andrew Parker</strong>Chief Executive Officer</div></div>
    </div>
  </section>
  <div class="narrow post-cover"><svg class="cover" viewBox="0 0 640 360" preserveAspectRatio="xMidYMid slice" aria-hidden="true" focusable="false"><rect width="640" height="360" fill="#12202b"/><circle cx="590" cy="30" r="190" fill="#ffffff" opacity=".07"/><circle cx="30" cy="350" r="150" fill="#ff7a4d" opacity=".22"/><circle cx="40" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><rect x="150" y="255" width="42" height="60" rx="6" fill="#ffffff" opacity="0.85"/><rect x="214" y="225" width="42" height="90" rx="6" fill="#ffffff" opacity="0.85"/><rect x="278" y="195" width="42" height="120" rx="6" fill="#ffffff" opacity="0.85"/><rect x="342" y="155" width="42" height="160" rx="6" fill="#ffffff" opacity="0.85"/><rect x="406" y="110" width="42" height="205" rx="6" fill="#ffffff" opacity="0.85"/><rect x="470" y="60" width="42" height="255" rx="6" fill="#ff7a4d" opacity="1"/><polyline points="171,235 235,205 299,175 363,135 427,95 491,62" fill="none" stroke="#ff7a4d" stroke-width="5" stroke-linecap="round" stroke-linejoin="round" opacity=".9"/><circle cx="491" cy="62" r="9" fill="#ffffff" stroke="#ff7a4d" stroke-width="5"/></svg></div>
  <div class="narrow prose">
    
<p>Old software is not automatically bad software. Plenty of ten-year-old systems run a business perfectly well. The trouble starts when keeping a system alive takes more money and attention than the system is worth. These five signs suggest you have reached that point.</p>
<h2>1. Small changes take weeks</h2>
<p>If adding a field to a form or changing a pricing rule needs a month of planning, the code has become tangled. Every change risks breaking something unrelated, so everyone moves slowly and carefully.</p>
<h2>2. Only one person understands it</h2>
<p>When a single developer holds the knowledge in their head, you carry a hidden risk. Holidays, resignations and illness all become business problems.</p>
<h2>3. Updates keep getting postponed</h2>
<p>Security patches and framework upgrades pile up because nobody trusts the system to survive them. Unpatched software is also the easiest kind to attack.</p>
<h2>4. Workarounds are everywhere</h2>
<p>Spreadsheets that copy data in and out, manual steps before month-end, a colleague who just knows which button to avoid. Each workaround is a sign the software no longer fits the work.</p>
<h2>5. It cannot talk to anything new</h2>
<p>Modern payment providers, CRMs and analytics tools expect clean APIs. If connecting a new tool means a custom project every time, the old system is holding you back.</p>
<div class="callout"><b>Before you rewrite</b>Ask for a short technical review first. Many systems need stabilizing and tidying, not replacing, and a review costs a fraction of a rebuild.</div>
    <div class="post-actions">
      <button class="btn btn-ghost btn-small copy-link" type="button">Copy link</button>
      <a class="btn btn-ghost btn-small" href="#blog">All articles</a>
    </div>
    <div class="author-box"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#f4b942"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#12202b"/><rect x="52" y="76" width="16" height="16" fill="#e3b58a"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#e3b58a"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#e3b58a"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#3b2a20"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><p><strong>Written by Andrew Parker</strong><br>Chief Executive Officer at DigitalForgePro. Questions about this article? <a class="text-link" href="#contact">Get in touch</a>.</p></div>
    <nav class="post-nav" aria-label="More articles"><a class="next" href="#blog/cloud-migration-without-panic"><small>Next article</small><strong>Cloud migration without the weekend panic</strong></a></nav>
  </div>
  
<section class="cta-band dark">
  <div class="wrap">
    <h2>Tell us what you need built or kept running.</h2>
    <p>Share a few details and a senior engineer will reply within one business day.</p>
    <div class="btn-row"><a class="btn btn-primary" href="#contact">Contact us</a>
    <a class="btn btn-ghost" href="#projects">See our projects</a></div>
  </div>
</section>
</article>
<article class="post" id="post-cloud-migration-without-panic" data-title="Cloud migration without the weekend panic" hidden>
  <section class="post-head dark">
    <div class="narrow">
      <nav class="crumbs" aria-label="Breadcrumb"><a href="#home">Home</a><span aria-hidden="true">/</span><a href="#blog">Blog</a><span aria-hidden="true">/</span><span aria-current="page">Cloud</span></nav>
      <div class="post-meta"><span class="cat">Cloud</span><span>September 24, 2026</span><span>4 min read</span></div>
      <h1>Cloud migration without the weekend panic</h1>
      <div class="post-byline"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#cfe9dd"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#1d5c63"/><rect x="52" y="76" width="16" height="16" fill="#b97a4b"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#b97a4b"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#b97a4b"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#1a1210"/><path d="M39 60C39 80 48 88 60 88C72 88 81 80 81 60C77 70 70 74 60 74C50 74 43 70 39 60Z" fill="#1a1210"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#f4e9e4" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><strong>Ibrahim Yusuf</strong>Engineering Lead</div></div>
    </div>
  </section>
  <div class="narrow post-cover"><svg class="cover" viewBox="0 0 640 360" preserveAspectRatio="xMidYMid slice" aria-hidden="true" focusable="false"><rect width="640" height="360" fill="#1d5c63"/><circle cx="590" cy="30" r="190" fill="#ffffff" opacity=".07"/><circle cx="30" cy="350" r="150" fill="#ffb347" opacity=".22"/><circle cx="40" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="262" cy="150" r="52" fill="#ffffff"/><circle cx="332" cy="120" r="70" fill="#ffffff"/><circle cx="404" cy="152" r="50" fill="#ffffff"/><rect x="212" y="150" width="242" height="56" rx="28" fill="#ffffff"/><line x1="332" y1="206" x2="190" y2="270" stroke="#ffffff" stroke-width="3" stroke-dasharray="7 7" opacity=".7"/><rect x="154" y="270" width="72" height="40" rx="8" fill="#ffffff"/><circle cx="170" cy="290" r="5" fill="#ffb347"/><rect x="182" y="286" width="32" height="8" rx="4" fill="#1d5c63" opacity=".5"/><line x1="332" y1="206" x2="332" y2="270" stroke="#ffffff" stroke-width="3" stroke-dasharray="7 7" opacity=".7"/><rect x="296" y="270" width="72" height="40" rx="8" fill="#ffffff"/><circle cx="312" cy="290" r="5" fill="#ffb347"/><rect x="324" y="286" width="32" height="8" rx="4" fill="#1d5c63" opacity=".5"/><line x1="332" y1="206" x2="474" y2="270" stroke="#ffffff" stroke-width="3" stroke-dasharray="7 7" opacity=".7"/><rect x="438" y="270" width="72" height="40" rx="8" fill="#ffffff"/><circle cx="454" cy="290" r="5" fill="#ffb347"/><rect x="466" y="286" width="32" height="8" rx="4" fill="#1d5c63" opacity=".5"/></svg></div>
  <div class="narrow prose">
    
<p>Moving to the cloud sounds like a single event. In practice it is a series of small, reversible steps, and the calm migrations are the ones that planned the boring parts in advance.</p>
<h2>Start with an inventory</h2>
<p>List every server, database, scheduled job and integration. The surprise is usually a forgotten job that quietly sends invoices every Friday. If it is not on the list, it will not be on the new system.</p>
<h2>Copy first, then switch</h2>
<p>Run the new environment alongside the old one and keep the data in sync. Test with copies of real traffic before any customer touches it. Switching becomes a small final step rather than a leap.</p>
<h2>Describe your setup in code</h2>
<p>Tools like Terraform let you rebuild the whole environment from a file. That makes it repeatable, reviewable and easy to recreate if something goes wrong.</p>
<h2>Rehearse the cutover</h2>
<p>Practice the switch on a copy at least twice, and time every step. The rehearsal that goes badly is the best one, because you fix the problem on a Tuesday instead of at 2 a.m.</p>
<h2>Keep a way back</h2>
<p>Decide in advance what would trigger a rollback and how long it would take. Teams that know they can undo the move make calmer decisions during it.</p>
<div class="callout"><b>Rule of thumb</b>A migration plan is only finished when it explains how to go back.</div>
    <div class="post-actions">
      <button class="btn btn-ghost btn-small copy-link" type="button">Copy link</button>
      <a class="btn btn-ghost btn-small" href="#blog">All articles</a>
    </div>
    <div class="author-box"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#cfe9dd"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#1d5c63"/><rect x="52" y="76" width="16" height="16" fill="#b97a4b"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#b97a4b"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#b97a4b"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#1a1210"/><path d="M39 60C39 80 48 88 60 88C72 88 81 80 81 60C77 70 70 74 60 74C50 74 43 70 39 60Z" fill="#1a1210"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#f4e9e4" stroke-width="2.2" stroke-linecap="round"/></svg></span><p><strong>Written by Ibrahim Yusuf</strong><br>Engineering Lead at DigitalForgePro. Questions about this article? <a class="text-link" href="#contact">Get in touch</a>.</p></div>
    <nav class="post-nav" aria-label="More articles"><a class="prev" href="#blog/old-software-replace-or-rescue"><small>Previous article</small><strong>Five signs your old software now costs more than it saves</strong></a><a class="next" href="#blog/what-99-9-uptime-means"><small>Next article</small><strong>What 99.9% uptime actually means</strong></a></nav>
  </div>
  
<section class="cta-band dark">
  <div class="wrap">
    <h2>Tell us what you need built or kept running.</h2>
    <p>Share a few details and a senior engineer will reply within one business day.</p>
    <div class="btn-row"><a class="btn btn-primary" href="#contact">Contact us</a>
    <a class="btn btn-ghost" href="#projects">See our projects</a></div>
  </div>
</section>
</article>
<article class="post" id="post-what-99-9-uptime-means" data-title="What 99.9% uptime actually means" hidden>
  <section class="post-head dark">
    <div class="narrow">
      <nav class="crumbs" aria-label="Breadcrumb"><a href="#home">Home</a><span aria-hidden="true">/</span><a href="#blog">Blog</a><span aria-hidden="true">/</span><span aria-current="page">Reliability</span></nav>
      <div class="post-meta"><span class="cat">Reliability</span><span>September 10, 2026</span><span>4 min read</span></div>
      <h1>What 99.9% uptime actually means</h1>
      <div class="post-byline"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#dfe7ff"/><path d="M34 66C30 34 44 22 60 22C76 22 90 34 86 66L88 100H32Z" fill="#d8a657"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#2f5d3a"/><rect x="52" y="76" width="16" height="16" fill="#f6d1b1"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#f6d1b1"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#f6d1b1"/><path d="M37 56C34 30 50 24 62 25C76 26 85 36 83 56C78 44 70 38 56 40C48 42 41 46 37 56Z" fill="#d8a657"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><strong>Hannah Müller</strong>Head of Managed Services</div></div>
    </div>
  </section>
  <div class="narrow post-cover"><svg class="cover" viewBox="0 0 640 360" preserveAspectRatio="xMidYMid slice" aria-hidden="true" focusable="false"><rect width="640" height="360" fill="#3a4a8c"/><circle cx="590" cy="30" r="190" fill="#ffffff" opacity=".07"/><circle cx="30" cy="350" r="150" fill="#ffb347" opacity=".22"/><circle cx="40" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="40" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="120" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="200" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="280" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="360" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="440" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="520" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="50" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="115" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="180" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="245" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="600" cy="310" r="1.8" fill="#ffffff" opacity=".25"/><circle cx="320" cy="180" r="112" fill="none" stroke="#ffffff" stroke-opacity=".2" stroke-width="26"/><circle cx="320" cy="180" r="112" fill="none" stroke="#ffb347" stroke-width="26" stroke-linecap="round" stroke-dasharray="672 32" transform="rotate(-90 320 180)"/><text x="320" y="196" text-anchor="middle" font-family="Bricolage Grotesque, Public Sans, sans-serif" font-size="58" font-weight="800" fill="#ffffff">99.9%</text><text x="320" y="228" text-anchor="middle" font-family="Public Sans, sans-serif" font-size="20" font-weight="600" fill="#ffffff" opacity=".75">uptime</text></svg></div>
  <div class="narrow prose">
    
<p>When a hosting provider promises 99.9% uptime, it sounds almost perfect. The numbers behind it are more useful than the percentage, so here they are.</p>
<div class="table-wrap"><table>
<thead><tr><th scope="col">Uptime target</th><th scope="col">Downtime per year</th><th scope="col">Downtime per month</th></tr></thead>
<tbody>
<tr><td>99%</td><td>About 3 days 16 hours</td><td>About 7 hours 18 minutes</td></tr>
<tr><td>99.9%</td><td>About 8 hours 46 minutes</td><td>About 44 minutes</td></tr>
<tr><td>99.99%</td><td>About 53 minutes</td><td>About 4 minutes 23 seconds</td></tr>
</tbody></table></div>
<h2>Ask what is being measured</h2>
<p>Does the figure cover the whole application or only the server it runs on? Does planned maintenance count as downtime? Two providers can quote the same number and mean very different things.</p>
<h2>Each extra nine costs more</h2>
<p>Going from 99.9% to 99.99% usually means duplicate infrastructure in separate locations, automatic failover and an on-call engineer awake around the clock. That is worth it for a payment system. It may not be for an internal reporting tool.</p>
<h2>Recovery time matters as much</h2>
<p>A brief outage you fix in two minutes is very different from a long one. Ask how quickly problems are detected, and how quickly service is restored.</p>
<div class="callout"><b>The takeaway</b>Choose the target that matches what downtime actually costs your business, not the biggest number on the brochure.</div>
    <div class="post-actions">
      <button class="btn btn-ghost btn-small copy-link" type="button">Copy link</button>
      <a class="btn btn-ghost btn-small" href="#blog">All articles</a>
    </div>
    <div class="author-box"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#dfe7ff"/><path d="M34 66C30 34 44 22 60 22C76 22 90 34 86 66L88 100H32Z" fill="#d8a657"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#2f5d3a"/><rect x="52" y="76" width="16" height="16" fill="#f6d1b1"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#f6d1b1"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#f6d1b1"/><path d="M37 56C34 30 50 24 62 25C76 26 85 36 83 56C78 44 70 38 56 40C48 42 41 46 37 56Z" fill="#d8a657"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><p><strong>Written by Hannah Müller</strong><br>Head of Managed Services at DigitalForgePro. Questions about this article? <a class="text-link" href="#contact">Get in touch</a>.</p></div>
    <nav class="post-nav" aria-label="More articles"><a class="prev" href="#blog/cloud-migration-without-panic"><small>Previous article</small><strong>Cloud migration without the weekend panic</strong></a><a class="next" href="#blog/security-basics-small-teams"><small>Next article</small><strong>Six security basics any team can do this month</strong></a></nav>
  </div>
  
<section class="cta-band dark">
  <div class="wrap">
    <h2>Tell us what you need built or kept running.</h2>
    <p>Share a few details and a senior engineer will reply within one business day.</p>
    <div class="btn-row"><a class="btn btn-primary" href="#contact">Contact us</a>
    <a class="btn btn-ghost" href="#projects">See our projects</a></div>
  </div>
</section>
</article>
<article class="post" id="post-security-basics-small-teams" data-title="Six security basics any team can do this month" hidden>
  <section class="post-head dark">
    <div class="narrow">
      <nav class="crumbs" aria-label="Breadcrumb"><a href="#home">Home</a><span aria-hidden="true">/</span><a href="#blog">Blog</a><span aria-hidden="true">/</span><span aria-current="page">Security</span></nav>
      <div class="post-meta"><span class="cat">Security</span><span>August 27, 2026</span><span>5 min read</span></div>
      <h1>Six security basics any team can do this month</h1>
      <div class="post-byline"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#7cc4f5"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#12202b"/><rect x="52" y="76" width="16" height="16" fill="#8d5524"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#8d5524"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#8d5524"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#1a1210"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="51" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><circle cx="69" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><path d="M58 56h4" stroke="#1b1b1b" stroke-width="2"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><div><strong>Kwame Mensah</strong>Chief Technology Officer</div></div>
    </div>
  </section>
  <div class="narrow post-cover"><svg class="cover" viewBox="0 0 640 360" preserveAspectRatio="xMidYMid slice" aria-hidden="true" focusable="false"><rect width="640" height="360" fill="#5a2a3c"/><circle cx="590" cy="30" r="190" fill="#fbeff1" opacity=".07"/><circle cx="30" cy="350" r="150" fill="#ffb347" opacity=".22"/><circle cx="40" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="40" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="40" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="40" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="40" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="120" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="120" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="120" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="120" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="120" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="200" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="200" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="200" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="200" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="200" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="280" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="280" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="280" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="280" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="280" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="360" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="360" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="360" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="360" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="360" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="440" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="440" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="440" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="440" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="440" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="520" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="520" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="520" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="520" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="520" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="600" cy="50" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="600" cy="115" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="600" cy="180" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="600" cy="245" r="1.8" fill="#fbeff1" opacity=".25"/><circle cx="600" cy="310" r="1.8" fill="#fbeff1" opacity=".25"/><path d="M320 62L436 106V192C436 256 388 296 320 318C252 296 204 256 204 192V106Z" fill="#fbeff1"/><path d="M320 82L418 118V192C418 244 380 278 320 298C260 278 222 244 222 192V118Z" fill="#5a2a3c" opacity=".12"/><path d="M268 190L304 226L376 148" fill="none" stroke="#ffb347" stroke-width="20" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
  <div class="narrow prose">
    
<p>Most breaches are not clever. They exploit a reused password, an unpatched server or a backup that never worked. You do not need a security department to close those doors. Start here.</p>
<ul>
<li><strong>Turn on multi-factor authentication.</strong> Do it for email, cloud accounts and code repositories first. It blocks most stolen-password attacks on its own.</li>
<li><strong>Patch on a schedule.</strong> Pick one day each week to apply updates, so patching is routine instead of a worry.</li>
<li><strong>Restore a backup.</strong> Actually restore one, to a test system, and time it. A backup you have never restored is a hope, not a backup.</li>
<li><strong>Give people only the access they need.</strong> Most staff do not need admin rights, and fewer admins means fewer accounts to protect.</li>
<li><strong>Remove leavers promptly.</strong> Keep a list of who has access to what, and review it every quarter.</li>
<li><strong>Write a one-page incident plan.</strong> Who to call, what to switch off, and who speaks to customers. Decide it calmly now rather than in the middle of a crisis.</li>
</ul>
<div class="callout"><b>Where to begin</b>If you only do one thing this week, turn on multi-factor authentication for your email. Everything else flows from that account.</div>
    <div class="post-actions">
      <button class="btn btn-ghost btn-small copy-link" type="button">Copy link</button>
      <a class="btn btn-ghost btn-small" href="#blog">All articles</a>
    </div>
    <div class="author-box"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#7cc4f5"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#12202b"/><rect x="52" y="76" width="16" height="16" fill="#8d5524"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#8d5524"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#8d5524"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#1a1210"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="51" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><circle cx="69" cy="56" r="7" fill="none" stroke="#1b1b1b" stroke-width="2"/><path d="M58 56h4" stroke="#1b1b1b" stroke-width="2"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><p><strong>Written by Kwame Mensah</strong><br>Chief Technology Officer at DigitalForgePro. Questions about this article? <a class="text-link" href="#contact">Get in touch</a>.</p></div>
    <nav class="post-nav" aria-label="More articles"><a class="prev" href="#blog/what-99-9-uptime-means"><small>Previous article</small><strong>What 99.9% uptime actually means</strong></a></nav>
  </div>
  
<section class="cta-band dark">
  <div class="wrap">
    <h2>Tell us what you need built or kept running.</h2>
    <p>Share a few details and a senior engineer will reply within one business day.</p>
    <div class="btn-row"><a class="btn btn-primary" href="#contact">Contact us</a>
    <a class="btn btn-ghost" href="#projects">See our projects</a></div>
  </div>
</section>
</article>
</div>

<div class="page" id="page-contact" hidden>

<section class="page-head dark">
  <div class="wrap">
    <nav class="crumbs" aria-label="Breadcrumb"><a href="#home">Home</a><span aria-hidden="true">/</span><span aria-current="page">Contact</span></nav>
    <h1>Tell us what you're building.</h1>
    <p class="lede">A few details are enough to start. A senior engineer, not a salesperson, will reply within one business day.</p>
  </div>
</section>

<section class="section">
  <div class="wrap contact-grid">
    <div>
      <form class="form" id="contact-form" novalidate>
        <div class="form-row">
          <div class="field">
            <label for="name">Your name</label>
            <input id="name" name="name" type="text" autocomplete="name" required aria-describedby="name-error">
            <p class="error" id="name-error" aria-live="polite"></p>
          </div>
          <div class="field">
            <label for="email">Work email</label>
            <input id="email" name="email" type="email" autocomplete="email" required aria-describedby="email-error">
            <p class="error" id="email-error" aria-live="polite"></p>
          </div>
        </div>
        <div class="form-row">
          <div class="field">
            <label for="company">Company <span class="hint">(optional)</span></label>
            <input id="company" name="company" type="text" autocomplete="organization">
          </div>
          <div class="field">
            <label for="budget">Budget range <span class="hint">(optional)</span></label>
            <select id="budget" name="budget">
              <option value="">Not sure yet</option>
              <option>Under $15,000</option>
              <option>$15,000 to $50,000</option>
              <option>$50,000 to $150,000</option>
              <option>Over $150,000</option>
            </select>
          </div>
        </div>
        <div class="field">
          <label for="service">What do you need help with?</label>
          <select id="service" name="service" required aria-describedby="service-error">
            <option value="">Choose one</option>
            <option>Build a new web application</option>
            <option>Build a mobile app</option>
            <option>Connect or integrate systems</option>
            <option>Move to the cloud</option>
            <option>Take over and manage existing software</option>
            <option>Something else</option>
          </select>
          <p class="error" id="service-error" aria-live="polite"></p>
        </div>
        <div class="field">
          <label for="message">Tell us about your project</label>
          <textarea id="message" name="message" required aria-describedby="message-error"></textarea>
          <p class="error" id="message-error" aria-live="polite"></p>
        </div>
        <button class="btn btn-primary" type="submit">Send message</button>
      </form>
      <div class="notice dark" id="form-success" tabindex="-1" hidden>
        <h2>Thanks, <span id="success-name"></span>. We have your message.</h2>
        <p>A senior engineer will reply within one business day. If your matter is urgent, email us directly at hello@digitalforgepro.website.</p>
        <a class="btn btn-ghost" href="#projects">See our projects while you wait</a>
      </div>
    </div>

    <aside class="contact-side">
      <div class="person-card"><span class="portrait"><svg viewBox="0 0 120 120" aria-hidden="true" focusable="false"><rect width="120" height="120" fill="#cfe3ea"/><path d="M14 120C14 96 34 86 60 86C86 86 106 96 106 120Z" fill="#3a4a8c"/><rect x="52" y="76" width="16" height="16" fill="#f0c8a0"/><rect x="52" y="76" width="16" height="16" fill="#000" opacity=".12"/><path d="M48 88L60 102L72 88Z" fill="#f0c8a0"/><ellipse cx="60" cy="56" rx="22" ry="26" fill="#f0c8a0"/><path d="M37 54C35 32 48 26 60 26C72 26 85 32 83 54C79 44 72 40 60 40C48 40 41 44 37 54Z" fill="#8a5a2b"/><circle cx="51" cy="56" r="2.4" fill="#1b1b1b"/><circle cx="69" cy="56" r="2.4" fill="#1b1b1b"/><path d="M52 67Q60 73 68 67" fill="none" stroke="#7a3b2e" stroke-width="2.2" stroke-linecap="round"/></svg></span><p><strong>Daniel Wilson, Manager</strong><br>I read every message myself and reply within one business day.</p></div>
      <h2>Reach us directly</h2>
      <ul class="contact-list">
        <li><strong>Email</strong><a href="mailto:hello@digitalforgepro.website">hello@digitalforgepro.website</a></li>
        <li><strong>Phone</strong><a href="tel:+15550100199">+1 (555) 010-0199</a></li>
        <li><strong>Hours</strong>Monday to Friday, 8:00 to 18:00 UTC</li>
        <li><strong>Where we are</strong>Remote-first, working with clients worldwide</li>
      </ul>
      <h2>What happens next</h2>
      <ol class="next-steps">
        <li>We read your message and reply within one business day.</li>
        <li>We book a free 30-minute call to understand your goals.</li>
        <li>You receive a written proposal with scope, timeline and price.</li>
      </ol>
    </aside>
  </div>
</section>
</div>

</main>

<footer class="site-footer">
  <div class="wrap">
    <div class="footer-grid">
      <div>
        <a class="brand" href="#home"><svg viewBox="0 0 32 32" aria-hidden="true"><rect width="32" height="32" rx="8" fill="#12202b"/><path d="M9 7h14v4H13v4h8v4h-8v6H9z" fill="#fff"/><rect x="19" y="21" width="4" height="4" fill="#ff7a4d"/></svg><div>DigitalForge<span>Pro</span></div></a>
        <p>We build custom software for growing companies, then host, monitor and maintain it so it keeps working.</p>
      </div>
      <div>
        <h3>Company</h3>
        <ul>
          <li><a href="#about">About us</a></li>
          <li><a href="#projects">Projects</a></li>
          <li><a href="#testimonials">Testimonials</a></li>
          <li><a href="#blog">Blog</a></li>
          <li><a href="#contact">Contact us</a></li>
        </ul>
      </div>
      <div>
        <h3>Latest articles</h3>
        <ul>
          <li><a href="#blog/old-software-replace-or-rescue">Five signs your old software now costs more than it saves</a></li><li><a href="#blog/cloud-migration-without-panic">Cloud migration without the weekend panic</a></li><li><a href="#blog/what-99-9-uptime-means">What 99.9% uptime actually means</a></li>
        </ul>
      </div>
      <div>
        <h3>Services</h3>
        <ul>
          <li><a href="#services/build">Software development</a></li>
          <li><a href="#services/manage">Managed services</a></li>
          <li><a href="#services/models">Ways to work with us</a></li>
          <li><a href="#services/faq">Questions we hear</a></li>
        </ul>
      </div>
      <div>
        <h3>Get in touch</h3>
        <ul>
          <li><a href="mailto:hello@digitalforgepro.website">hello@digitalforgepro.website</a></li>
          <li>Mon to Fri, 8:00 to 18:00 UTC</li>
          <li>Remote-first, serving clients worldwide</li>
        </ul>
      </div>
    </div>
    <p class="footer-base">&copy; <span id="year">2026</span> DigitalForgePro. All rights reserved. digitalforgepro.website</p>
  </div>
</footer>


<button class="to-top" id="to-top" type="button" aria-label="Back to top" hidden><svg viewBox="0 0 24 24" aria-hidden="true"><path d="M12 19V5M5 12l7-7 7 7"/></svg></button>
<dialog class="case" id="case-dialog" aria-label="Project case study">
  <button class="case-close" type="button" aria-label="Close case study">&times;</button>
  <div class="case-art"></div>
  <div class="case-body"></div>
</dialog>
<script>
/* DigitalForgePro v2 — scripts */
(function () {
  "use strict";

  var reduceMotion = window.matchMedia("(prefers-reduced-motion: reduce)").matches;
  var playLog = null;

  /* Footer year */
  var year = document.getElementById("year");
  if (year) year.textContent = new Date().getFullYear();

  /* Header: border on scroll + mobile menu */
  var header = document.querySelector(".site-header");
  var toggle = document.getElementById("nav-toggle");
  function closeMenu() {
    if (!header || !toggle) return;
    header.classList.remove("nav-open");
    toggle.setAttribute("aria-expanded", "false");
    toggle.textContent = "Menu";
  }
  if (header) {
    var onScroll = function () { header.classList.toggle("scrolled", window.scrollY > 8); };
    onScroll();
    window.addEventListener("scroll", onScroll, { passive: true });
  }
  if (toggle) {
    toggle.addEventListener("click", function () {
      var open = header.classList.toggle("nav-open");
      toggle.setAttribute("aria-expanded", String(open));
      toggle.textContent = open ? "Close" : "Menu";
    });
    document.addEventListener("keydown", function (e) {
      if (e.key === "Escape" && header.classList.contains("nav-open")) { closeMenu(); toggle.focus(); }
    });
  }

  /* Hero deploy log: plays on load and on request */
  var log = document.getElementById("deploy-log");
  if (log) {
    var lines = Array.prototype.slice.call(log.querySelectorAll(".log-line"));
    var replay = document.getElementById("log-replay");
    var timers = [];
    var play = function () {
      timers.forEach(clearTimeout);
      timers = [];
      if (reduceMotion) { lines.forEach(function (l) { l.classList.remove("pending"); }); return; }
      lines.forEach(function (l) { l.classList.add("pending"); });
      lines.forEach(function (l, i) {
        timers.push(setTimeout(function () { l.classList.remove("pending"); }, 600 + i * 520));
      });
    };
    playLog = play;
    play();
    if (replay) replay.addEventListener("click", play);
  }

  /* Project filter */
  var filters = document.querySelectorAll(".filter");
  if (filters.length) {
    var gridProjects = document.querySelectorAll("#project-grid .project");
    var count = document.getElementById("result-count");
    filters.forEach(function (btn) {
      btn.addEventListener("click", function () {
        var cat = btn.getAttribute("data-filter");
        var shown = 0;
        filters.forEach(function (b) { b.setAttribute("aria-pressed", String(b === btn)); });
        gridProjects.forEach(function (p) {
          var match = cat === "all" || p.getAttribute("data-cat") === cat;
          p.hidden = !match;
          if (match) shown++;
        });
        if (count) count.textContent = "Showing " + shown + (shown === 1 ? " project" : " projects");
      });
    });
  }

  /* Case study dialog */
  var dialog = document.getElementById("case-dialog");
  if (dialog) {
    var dBody = dialog.querySelector(".case-body");
    var dArt = dialog.querySelector(".case-art");
    document.addEventListener("click", function (e) {
      var btn = e.target.closest(".open-case");
      if (!btn) return;
      var card = btn.closest(".project");
      dArt.innerHTML = "";
      dArt.appendChild(card.querySelector(".shot").cloneNode(true));
      dBody.innerHTML = card.querySelector("template").innerHTML;
      if (typeof dialog.showModal === "function") dialog.showModal();
      else dialog.setAttribute("open", "");
    });
    dialog.querySelector(".case-close").addEventListener("click", function () { dialog.close(); });
    dialog.addEventListener("click", function (e) { if (e.target === dialog) dialog.close(); });
    dialog.addEventListener("click", function (e) {
      if (e.target.closest("[data-close-and-go]")) dialog.close();
    });
  }

  /* Testimonial slider */
  var slider = document.getElementById("slider");
  if (slider) {
    var slides = slider.querySelectorAll(".slide");
    var counter = document.getElementById("slider-count");
    var current = 0;
    var show = function (i) {
      current = (i + slides.length) % slides.length;
      slides.forEach(function (s, n) { s.hidden = n !== current; });
      counter.textContent = (current + 1) + " of " + slides.length;
    };
    document.getElementById("slider-prev").addEventListener("click", function () { show(current - 1); });
    document.getElementById("slider-next").addEventListener("click", function () { show(current + 1); });
    show(0);
  }

  /* Contact form: validation and confirmation.
     Front-end only. To receive messages, send the form data to a service
     (Formspree, Netlify Forms, your own API) with fetch() in the valid branch. */
  var form = document.getElementById("contact-form");
  if (form) {
    var rules = {
      name: function (v) { return v.trim().length >= 2 ? "" : "Enter your name."; },
      email: function (v) { return /^[^\s@]+@[^\s@]+\.[^\s@]{2,}$/.test(v.trim()) ? "" : "Enter a valid email address, like name@company.com."; },
      service: function (v) { return v ? "" : "Choose what you need help with."; },
      message: function (v) { return v.trim().length >= 20 ? "" : "Tell us a little more. A couple of sentences is enough (20 characters minimum)."; }
    };
    var check = function (field) {
      var input = form.elements[field];
      var msg = rules[field](input.value);
      document.getElementById(field + "-error").textContent = msg;
      input.setAttribute("aria-invalid", msg ? "true" : "false");
      return !msg;
    };
    Object.keys(rules).forEach(function (field) {
      form.elements[field].addEventListener("blur", function () { check(field); });
      form.elements[field].addEventListener("input", function () {
        if (form.elements[field].getAttribute("aria-invalid") === "true") check(field);
      });
    });
    form.addEventListener("submit", function (e) {
      e.preventDefault();
      var firstBad = null;
      Object.keys(rules).forEach(function (field) { if (!check(field) && !firstBad) firstBad = form.elements[field]; });
      if (firstBad) { firstBad.focus(); return; }
      var panel = document.getElementById("form-success");
      document.getElementById("success-name").textContent = form.elements.name.value.trim().split(" ")[0];
      form.hidden = true;
      panel.hidden = false;
      panel.focus();
    });
  }

  /* Reading progress bar + back-to-top button */
  var progress = document.getElementById("progress");
  var toTop = document.getElementById("to-top");
  function onScrollExtras() {
    var h = document.documentElement;
    var max = h.scrollHeight - h.clientHeight;
    if (progress) progress.style.width = (max > 0 ? Math.min(100, (window.scrollY / max) * 100) : 0) + "%";
    if (toTop) toTop.hidden = window.scrollY < 700;
  }
  window.addEventListener("scroll", onScrollExtras, { passive: true });
  window.addEventListener("resize", onScrollExtras);
  if (toTop) {
    toTop.addEventListener("click", function () {
      window.scrollTo({ top: 0, behavior: reduceMotion ? "auto" : "smooth" });
    });
  }

  /* Blog category filter */
  var bFilters = document.querySelectorAll(".blog-filter");
  if (bFilters.length) {
    var bCards = document.querySelectorAll("#blog-grid .post-card");
    var bCount = document.getElementById("blog-count");
    bFilters.forEach(function (btn) {
      btn.addEventListener("click", function () {
        var cat = btn.getAttribute("data-cat");
        var shown = 0;
        bFilters.forEach(function (b) { b.setAttribute("aria-pressed", String(b === btn)); });
        bCards.forEach(function (card) {
          var match = cat === "all" || card.getAttribute("data-cat") === cat;
          card.hidden = !match;
          if (match) shown++;
        });
        if (bCount) bCount.textContent = "Showing " + shown + (shown === 1 ? " article" : " articles");
      });
    });
  }

  /* Copy article link */
  document.addEventListener("click", function (e) {
    var b = e.target.closest(".copy-link");
    if (!b) return;
    var done = function () {
      b.textContent = "Link copied";
      setTimeout(function () { b.textContent = "Copy link"; }, 2000);
    };
    if (navigator.clipboard && navigator.clipboard.writeText) navigator.clipboard.writeText(location.href).then(done, done);
    else done();
  });

  /* Page router: seven pages in one file, switched by URL hash.
     #blog/<slug> opens an article; other second segments scroll to a section (e.g. #services/faq) */
  var pageNames = ["home", "services", "projects", "testimonials", "about", "blog", "contact"];
  var pageTitles = {
    home: "DigitalForgePro | Custom software, built and managed",
    services: "Services | DigitalForgePro",
    projects: "Projects | DigitalForgePro",
    testimonials: "Testimonials | DigitalForgePro",
    about: "About us | DigitalForgePro",
    blog: "Blog | DigitalForgePro",
    contact: "Contact us | DigitalForgePro"
  };
  var firstRoute = true;
  var current = null; /* in-memory location, used when the browser blocks URL changes */
  function getHash() { return current !== null ? current : (location.hash || ""); }

  function visibleHeading(name) {
    var hs = document.querySelectorAll("#page-" + name + " h1");
    for (var i = 0; i < hs.length; i++) { if (hs[i].offsetParent !== null) return hs[i]; }
    return null;
  }

  function route() {
    var raw = getHash().replace(/^#/, "");
    var parts = raw.split("/");
    var name = raw ? parts[0] : "home";
    if (pageNames.indexOf(name) === -1) { name = "home"; parts = ["home"]; }

    pageNames.forEach(function (p) { document.getElementById("page-" + p).hidden = (p !== name); });
    document.querySelectorAll(".nav-links a, .nav > .btn").forEach(function (a) {
      if (a.getAttribute("href") === "#" + name) a.setAttribute("aria-current", "page");
      else a.removeAttribute("aria-current");
    });

    var title = pageTitles[name];
    var target = null;
    if (name === "blog") {
      var post = parts[1] ? document.getElementById("post-" + parts[1]) : null;
      document.getElementById("blog-list").hidden = !!post;
      document.querySelectorAll("#page-blog .post").forEach(function (p) { p.hidden = (p !== post); });
      if (post) title = post.getAttribute("data-title") + " | DigitalForgePro Blog";
    } else if (parts[1]) {
      target = document.getElementById(parts[1]);
    }
    document.title = title;
    closeMenu();

    if (target) {
      target.scrollIntoView();
    } else {
      window.scrollTo({ top: 0, behavior: "auto" });
      if (!firstRoute) {
        var h1 = visibleHeading(name);
        if (h1) { h1.setAttribute("tabindex", "-1"); h1.focus({ preventScroll: true }); }
      }
    }
    if (name === "home" && playLog) playLog();
    firstRoute = false;
    onScrollExtras();
  }

  /* Go to a page: updates the address when the browser allows it, and always shows the page */
  function go(hash) {
    current = hash;
    try { if (window.history && history.pushState) history.pushState(null, "", hash); } catch (err) { /* address bar locked: fine */ }
    route();
  }

  /* Every in-site link (navbar, logo, buttons, footer, article links) is handled here */
  document.addEventListener("click", function (e) {
    var a = e.target.closest && e.target.closest('a[href^="#"]');
    if (!a || e.defaultPrevented || e.button > 0 || e.metaKey || e.ctrlKey || e.shiftKey) return;
    var href = a.getAttribute("href");
    if (href === "#main") {
      e.preventDefault();
      var m = document.getElementById("main");
      m.setAttribute("tabindex", "-1");
      m.focus();
      return;
    }
    var name = href.replace(/^#/, "").split("/")[0];
    if (pageNames.indexOf(name) === -1) return;
    e.preventDefault();
    go(href);
  });

  /* Browser back/forward and typed addresses */
  window.addEventListener("hashchange", function () { current = null; route(); });
  window.addEventListener("popstate", function () { current = null; route(); });

  /* Close the mobile menu when tapping outside it */
  document.addEventListener("click", function (e) {
    if (header && header.classList.contains("nav-open") && !header.contains(e.target)) closeMenu();
  });

  route();
})();

</script>
</body>
</html>

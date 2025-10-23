
<!-- index.html (minimal skeleton) -->
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Project Landing</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="site-header">
    <div class="container header-inner">
      <h1 class="brand">Prospector <span class="muted">— Quality for Python</span></h1>
      <nav class="nav">
        <a href="#">Docs</a>
        <a href="#">Profiles</a>
        <a href="#">Contribute</a>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero">
      <div class="container">
        <h2 class="hero-title">Static analysis, simplified</h2>
        <p class="hero-sub">Run multiple linters and formatters in one go. Configure with profiles and get meaningful reports.</p>
        <div class="hero-cta">
          <a class="btn primary" href="#">Get Started</a>
          <a class="btn outline" href="#">View Docs</a>
        </div>
      </div>
    </section>

    <section class="features container">
      <article class="card">
        <h3>Profiles</h3>
        <p>Prebuilt profiles for frameworks and styles so you get useful results immediately.</p>
      </article>
      <article class="card">
        <h3>Plugins</h3>
        <p>Easily enable additional tools like mypy or bandit as optional extras.</p>
      </article>
      <article class="card">
        <h3>CI Friendly</h3>
        <p>Integrates with pre-commit and CI pipelines for automated checks.</p>
      </article>
    </section>

    <section class="container code-sample">
      <h3>Example</h3>
      <pre><code>prospector --profile flask_rest_api --output-format json</code></pre>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container">
      <small>© 2025 Prospector — Contribute on GitHub</small>
    </div>
  </footer>
</body>
</html>
/* styles.css - modern, responsive styles for a project page */

/* ---------- Variables & Reset ---------- */
:root{
  --bg: #0f1724;            /* dark background for hero */
  --card-bg: #ffffff;
  --muted: #6b7280;
  --accent: #2563eb;
  --accent-2: #06b6d4;
  --text: #0b1220;
  --glass: rgba(255,255,255,0.06);
  --radius: 14px;
  --container-max: 1100px;
  --flow: 1.2rem;
}

*{box-sizing:border-box}
html,body{height:100%}
body{
  margin:0;
  font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
  background: linear-gradient(180deg,#fbfdff 0%,#f7f9fc 100%);
  color:var(--text);
  -webkit-font-smoothing:antialiased;
  -moz-osx-font-smoothing:grayscale;
  line-height:1.45;
  font-size:16px;
}

/* ---------- Utility ---------- */
.container{
  width:calc(100% - 2rem);
  max-width:var(--container-max);
  margin:0 auto;
  padding:2rem 1rem;
}

.header-inner{display:flex;align-items:center;justify-content:space-between;gap:1rem}

/* ---------- Header ---------- */
.site-header{
  position:sticky;
  top:0;
  z-index:40;
  backdrop-filter: blur(6px);
  background: linear-gradient(180deg, rgba(255,255,255,0.7), rgba(255,255,255,0.55));
  border-bottom:1px solid rgba(11,18,32,0.06);
}
.brand{
  margin:0;
  font-size:1.15rem;
  letter-spacing:0.2px;
  color:var(--text);
}
.brand .muted{color:var(--muted);font-weight:600;margin-left:8px;font-size:0.9rem}

.nav a{
  text-decoration:none;
  color:var(--text);
  padding:8px 12px;
  border-radius:8px;
  font-weight:600;
  opacity:0.9;
}
.nav a:hover{background:var(--glass)}

/* ---------- Hero ---------- */
.hero{
  background: linear-gradient(180deg, var(--bg), #0b1220);
  color:white;
  padding:4.5rem 0;
  border-bottom-left-radius:36px;
  border-bottom-right-radius:36px;
  box-shadow: 0 8px 40px rgba(2,6,23,0.4);
}
.hero .container{display:flex;flex-direction:column;align-items:flex-start;gap:1rem}
.hero-title{
  margin:0 0 0.25rem 0;
  font-size:2rem;
  line-height:1.04;
  font-weight:700;
}
.hero-sub{margin:0 0 1rem 0;color:rgba(255,255,255,0.88);max-width:60ch}

.hero-cta{display:flex;gap:0.75rem;align-items:center}
.btn{
  display:inline-block;
  padding:0.55rem 1rem;
  border-radius:12px;
  text-decoration:none;
  font-weight:700;
  font-size:0.95rem;
  transition:transform .12s ease, box-shadow .12s ease;
}
.btn:active{transform:translateY(1px)}
.btn.primary{
  background:linear-gradient(90deg,var(--accent),var(--accent-2));
  color:#fff;
  box-shadow: 0 6px 18px rgba(37,99,235,0.18);
}
.btn.outline{
  background:transparent;
  border:1px solid rgba(255,255,255,0.12);
  color:rgba(255,255,255,0.95);
}

/* ---------- Features grid ---------- */
.features{
  display:grid;
  grid-template-columns: repeat(3, 1fr);
  gap:1.25rem;
  margin-top:-2.5rem; /* lift cards up into hero */
  position:relative;
  z-index:30;
}
.card{
  background:var(--card-bg);
  border-radius:14px;
  padding:1.25rem;
  box-shadow: 0 8px 30px rgba(11,18,32,0.06);
  transition:transform .14s ease, box-shadow .14s ease;
}
.card:hover{transform:translateY(-6px);box-shadow:0 18px 40px rgba(11,18,32,0.08)}
.card h3{margin:0 0 0.5rem 0}
.card p{margin:0;color:var(--muted)}

/* ---------- Code sample ---------- */
.code-sample pre{
  background:#0b1220;
  color:#e6eef8;
  padding:1rem;
  border-radius:10px;
  overflow:auto;
  box-shadow: 0 6px 24px rgba(2,6,23,0.28);
  margin-top:0.75rem;
  border:1px solid rgba(255,255,255,0.04);
  font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, "Roboto Mono", monospace;
  font-size:0.95rem;
}

/* ---------- Footer ---------- */
.site-footer{
  padding:1.5rem 0;
  color:var(--muted);
  border-top:1px solid rgba(11,18,32,0.04);
  background:transparent;
}

/* ---------- Responsive ---------- */
@media (max-width:900px){
  .features{grid-template-columns:repeat(2,1fr)}
  .hero-title{font-size:1.6rem}
  .hero-sub{max-width:44ch}
}
@media (max-width:600px){
  .header-inner{flex-direction:column;align-items:flex-start;gap:0.5rem;padding:0.75rem 0}
  .features{grid-template-columns: 1fr}
  .hero{padding:3rem 0;border-radius:0 0 20px 20px}
  .hero .container{align-items:flex-start}
  .nav{display:flex;gap:0.5rem;flex-wrap:wrap}
}

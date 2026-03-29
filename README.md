:root {
  --bg: #0b0b0f;
  --bg-soft: #11131b;
  --panel: rgba(255, 255, 255, 0.06);
  --panel-border: rgba(255, 255, 255, 0.12);
  --text: #edf2ff;
  --muted: #a8b0c7;
  --blue: #00d1ff;
  --purple: #7a5cff;
  --glow: 0 0 24px rgba(0, 209, 255, 0.18);
  --radius: 22px;
  --container: 1180px;
}

* { box-sizing: border-box; }
html { scroll-behavior: smooth; }
body {
  margin: 0;
  font-family: Inter, system-ui, sans-serif;
  background:
    radial-gradient(circle at 20% 10%, rgba(122,92,255,.16), transparent 28%),
    radial-gradient(circle at 80% 15%, rgba(0,209,255,.14), transparent 25%),
    linear-gradient(180deg, #07080c 0%, #0b0b0f 100%);
  color: var(--text);
}

a { color: inherit; text-decoration: none; }
img { max-width: 100%; display: block; }

.site-shell {
  min-height: 100vh;
  overflow-x: hidden;
}

.topbar {
  position: sticky;
  top: 0;
  z-index: 30;
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: min(var(--container), calc(100% - 2rem));
  margin: 0 auto;
  padding: 1rem 0;
  backdrop-filter: blur(14px);
}

.brand {
  display: inline-flex;
  align-items: center;
  gap: .8rem;
  font-weight: 800;
  letter-spacing: .14em;
  font-size: .92rem;
}
.brand-mark {
  width: 38px;
  height: 38px;
  display: grid;
  place-items: center;
  border-radius: 12px;
  background: linear-gradient(135deg, var(--blue), var(--purple));
  color: #061018;
  box-shadow: var(--glow);
}
.brand-text { white-space: nowrap; }

.nav {
  display: flex;
  align-items: center;
  gap: 1.2rem;
}
.nav a {
  color: var(--muted);
  transition: .25s ease;
}
.nav a:hover { color: var(--text); }

.nav-cta, .btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 999px;
  font-weight: 700;
  transition: transform .25s ease, box-shadow .25s ease, background .25s ease;
}
.nav-cta {
  padding: .85rem 1.15rem;
  background: linear-gradient(135deg, rgba(0,209,255,.2), rgba(122,92,255,.22));
  color: var(--text) !important;
  border: 1px solid rgba(255,255,255,.12);
}
.nav-cta:hover, .btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 12px 32px rgba(0, 209, 255, .18);
}

.nav-toggle {
  display: none;
  background: transparent;
  border: 0;
  padding: 0;
}
.nav-toggle span {
  display: block;
  width: 24px;
  height: 2px;
  margin: 5px 0;
  background: var(--text);
}

.hero,
.section,
.footer {
  width: min(var(--container), calc(100% - 2rem));
  margin: 0 auto;
}

.hero {
  display: grid;
  grid-template-columns: 1.05fr .95fr;
  align-items: center;
  gap: 3rem;
  min-height: calc(100vh - 88px);
  padding: 3rem 0 5rem;
}

.eyebrow {
  display: inline-block;
  margin-bottom: 1rem;
  font-size: .85rem;
  font-weight: 700;
  letter-spacing: .18em;
  text-transform: uppercase;
  color: var(--blue);
}

h1, h2, h3, p { margin-top: 0; }
h1 {
  font-size: clamp(2.7rem, 6vw, 5rem);
  line-height: .96;
  letter-spacing: -.04em;
  margin-bottom: 1.25rem;
}
h2 {
  font-size: clamp(2rem, 4vw, 3.2rem);
  line-height: 1.05;
  letter-spacing: -.03em;
  margin-bottom: 1rem;
}
h3 {
  font-size: 1.2rem;
  margin-bottom: .6rem;
}
.lead, .section-heading p, .feature-copy p, .contact-copy p, .solution-card p, .industry-card p, .footer p {
  color: var(--muted);
  line-height: 1.7;
}

.hero-actions {
  display: flex;
  gap: 1rem;
  margin: 1.8rem 0 2rem;
  flex-wrap: wrap;
}

.btn {
  padding: 1rem 1.35rem;
  border: 1px solid rgba(255,255,255,.12);
}
.btn-primary {
  color: #071019;
  background: linear-gradient(135deg, var(--blue), #6af0ff);
}
.btn-secondary {
  background: rgba(255,255,255,.04);
  color: var(--text);
}

.hero-stats {
  display: flex;
  flex-wrap: wrap;
  gap: 1.25rem;
}
.hero-stats div {
  min-width: 120px;
}
.hero-stats strong {
  display: block;
  font-size: 1.45rem;
  margin-bottom: .25rem;
}
.hero-stats span {
  color: var(--muted);
  font-size: .95rem;
}

.glass {
  background: var(--panel);
  border: 1px solid var(--panel-border);
  box-shadow: inset 0 1px 0 rgba(255,255,255,.06), 0 18px 40px rgba(0,0,0,.35);
  backdrop-filter: blur(18px);
}

.hero-visual { position: relative; }
.hero-visual::before {
  content: "";
  position: absolute;
  inset: 8% 10% auto auto;
  width: 190px;
  height: 190px;
  border-radius: 999px;
  background: radial-gradient(circle, rgba(122,92,255,.35), transparent 65%);
  filter: blur(20px);
}
.visual-card {
  border-radius: 28px;
  padding: 1rem;
}
.visual-header {
  display: flex;
  gap: .35rem;
  padding: .2rem 0 .9rem;
}
.dot {
  width: 10px;
  height: 10px;
  border-radius: 999px;
  background: rgba(255,255,255,.22);
}
.dashboard {
  display: grid;
  gap: .9rem;
}
.dashboard-row {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: .9rem;
}
.dashboard-panel {
  border-radius: 20px;
  padding: 1rem;
  background: rgba(10, 14, 22, .78);
  border: 1px solid rgba(255,255,255,.06);
}
.panel-lg { min-height: 180px; }
.panel-title {
  color: var(--muted);
  margin-bottom: 1rem;
}
.signal-grid {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: .6rem;
}
.signal-grid span {
  height: 62px;
  border-radius: 14px;
  background: linear-gradient(180deg, rgba(0,209,255,.65), rgba(122,92,255,.25));
  animation: pulse 2.4s infinite ease-in-out;
}
.signal-grid span:nth-child(odd) { animation-delay: .15s; }
.kpi {
  font-size: 2rem;
  font-weight: 800;
  margin-bottom: .35rem;
}
.kpi-label {
  color: var(--muted);
  font-size: .92rem;
}
.chart-panel { padding: 1.25rem; }
.chart {
  height: 90px;
  border-radius: 14px;
  background:
    linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,0)),
    linear-gradient(90deg,
      rgba(0,209,255,.1) 0%,
      rgba(122,92,255,.36) 50%,
      rgba(0,209,255,.1) 100%);
  position: relative;
  overflow: hidden;
}
.chart::after {
  content: "";
  position: absolute;
  inset: 0;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,.22), transparent);
  transform: translateX(-100%);
  animation: sweep 2.8s linear infinite;
}

.section {
  padding: 5.5rem 0;
}
.section-dark {
  border-top: 1px solid rgba(255,255,255,.05);
  border-bottom: 1px solid rgba(255,255,255,.05);
  background: rgba(255,255,255,.015);
}
.section-heading {
  max-width: 800px;
  margin-bottom: 2rem;
}

.card-grid,
.industry-grid {
  display: grid;
  gap: 1.2rem;
}
.card-grid {
  grid-template-columns: repeat(4, 1fr);
}
.solution-card {
  border-radius: var(--radius);
  padding: 1.4rem;
  transition: transform .25s ease, border-color .25s ease;
}
.solution-card:hover,
.industry-card:hover {
  transform: translateY(-4px);
  border-color: rgba(0,209,255,.34);
}
.icon-wrap {
  width: 52px;
  height: 52px;
  display: grid;
  place-items: center;
  border-radius: 16px;
  font-size: 1.4rem;
  margin-bottom: 1rem;
  background: linear-gradient(135deg, rgba(0,209,255,.18), rgba(122,92,255,.18));
  box-shadow: var(--glow);
}

.two-col {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  align-items: center;
}
.feature-list {
  list-style: none;
  padding: 0;
  margin: 1.5rem 0 0;
}
.feature-list li {
  padding: .95rem 0;
  border-bottom: 1px solid rgba(255,255,255,.08);
  color: var(--muted);
}
.feature-panel {
  border-radius: 26px;
  padding: 1.2rem;
  display: grid;
  gap: 1rem;
}
.mini-card {
  padding: 1rem 1.15rem;
  border-radius: 18px;
  background: rgba(10,14,22,.72);
  border: 1px solid rgba(255,255,255,.06);
}
.mini-card span {
  display: block;
  color: var(--muted);
  font-size: .9rem;
  margin-bottom: .35rem;
}
.mini-card strong {
  font-size: 1.1rem;
}

.industry-grid {
  grid-template-columns: repeat(3, 1fr);
}
.industry-card {
  padding: 1.4rem;
  border-radius: var(--radius);
  border: 1px solid rgba(255,255,255,.08);
  background: rgba(255,255,255,.02);
  transition: transform .25s ease, border-color .25s ease;
}

.contact-wrap { align-items: start; }
.contact-links {
  display: grid;
  gap: .9rem;
  margin-top: 1.5rem;
}
.contact-links a {
  color: var(--text);
  font-weight: 600;
}
.contact-form {
  border-radius: 26px;
  padding: 1.4rem;
  display: grid;
  gap: 1rem;
}
.contact-form label {
  display: grid;
  gap: .45rem;
}
.contact-form span {
  color: var(--muted);
  font-size: .92rem;
}
input, textarea {
  width: 100%;
  border: 1px solid rgba(255,255,255,.12);
  background: rgba(10,14,22,.75);
  color: var(--text);
  border-radius: 16px;
  padding: 1rem 1rem;
  font: inherit;
  outline: none;
}
input:focus, textarea:focus {
  border-color: rgba(0,209,255,.44);
  box-shadow: 0 0 0 3px rgba(0,209,255,.08);
}

.footer {
  display: flex;
  justify-content: space-between;
  gap: 2rem;
  padding: 2rem 0 5rem;
  color: var(--muted);
}
.footer-brand {
  color: var(--text);
  font-weight: 800;
  letter-spacing: .14em;
  margin-bottom: .5rem;
}
.footer-links {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

.floating-call {
  position: fixed;
  right: 1rem;
  bottom: 1rem;
  z-index: 40;
  padding: 1rem 1.2rem;
  border-radius: 999px;
  background: linear-gradient(135deg, var(--blue), var(--purple));
  color: #071019;
  font-weight: 800;
  box-shadow: 0 12px 32px rgba(0,209,255,.26);
}

.reveal {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity .65s ease, transform .65s ease;
}
.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

@keyframes pulse {
  0%, 100% { transform: scaleY(.78); opacity: .72; }
  50% { transform: scaleY(1); opacity: 1; }
}
@keyframes sweep {
  to { transform: translateX(100%); }
}

@media (max-width: 980px) {
  .hero,
  .two-col,
  .card-grid,
  .industry-grid {
    grid-template-columns: 1fr;
  }

  .hero {
    padding-top: 2rem;
  }

  .nav-toggle { display: block; z-index: 31; }
  .nav {
    position: absolute;
    top: calc(100% + .5rem);
    right: 0;
    display: none;
    flex-direction: column;
    align-items: stretch;
    width: min(320px, calc(100vw - 2rem));
    padding: 1rem;
    border-radius: 20px;
    background: rgba(8,10,16,.95);
    border: 1px solid rgba(255,255,255,.08);
    box-shadow: 0 16px 40px rgba(0,0,0,.35);
  }
  .nav.open { display: flex; }
  .nav a { padding: .6rem .3rem; }

  .topbar {
    position: sticky;
  }
}

@media (max-width: 640px) {
  .topbar, .hero, .section, .footer {
    width: min(var(--container), calc(100% - 1.2rem));
  }
  h1 { font-size: 2.5rem; }
  .footer {
    flex-direction: column;
    padding-bottom: 6rem;
  }
  .floating-call {
    left: .8rem;
    right: .8rem;
    text-align: center;
  }
}

# ff-sens-pro<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FF SENS PRO — Configurações Profissionais Free Fire</title>
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&family=Orbitron:wght@400;600;700;900&family=Exo+2:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #050608;
  --dark: #0a0c10;
  --card: #0e1118;
  --card2: #12151f;
  --border: #1e2333;
  --orange: #FF6B00;
  --orange2: #FF9A3C;
  --orange-glow: rgba(255,107,0,0.18);
  --red: #FF2D2D;
  --yellow: #FFD600;
  --cyan: #00E5FF;
  --white: #EEF0F5;
  --gray: #6B7280;
  --gray2: #9CA3AF;
}
* { margin:0; padding:0; box-sizing:border-box; }
html { scroll-behavior:smooth; }
body {
  font-family:'Exo 2', sans-serif;
  background:var(--bg);
  color:var(--white);
  overflow-x:hidden;
  cursor:crosshair;
}

/* ===== ANIMATED BG ===== */
.bg-layer {
  position:fixed; inset:0; pointer-events:none; z-index:0;
  background:
    radial-gradient(ellipse 70% 50% at 20% 20%, rgba(255,107,0,0.06) 0%, transparent 60%),
    radial-gradient(ellipse 60% 40% at 80% 80%, rgba(0,229,255,0.04) 0%, transparent 60%);
}
.bg-grid {
  position:fixed; inset:0; pointer-events:none; z-index:0; opacity:0.025;
  background-image:
    linear-gradient(rgba(255,107,0,0.8) 1px, transparent 1px),
    linear-gradient(90deg, rgba(255,107,0,0.8) 1px, transparent 1px);
  background-size:40px 40px;
}
.scanline {
  position:fixed; inset:0; pointer-events:none; z-index:0;
  background:repeating-linear-gradient(0deg, transparent, transparent 2px, rgba(0,0,0,0.03) 2px, rgba(0,0,0,0.03) 4px);
}

/* ===== HEADER ===== */
header {
  position:sticky; top:0; z-index:200;
  background:rgba(5,6,8,0.92);
  backdrop-filter:blur(16px);
  border-bottom:1px solid var(--border);
  padding:0 2rem;
  height:60px;
  display:flex; align-items:center; justify-content:space-between;
}
.logo {
  font-family:'Orbitron',monospace;
  font-weight:900; font-size:1.1rem;
  letter-spacing:0.08em;
  color:var(--white);
}
.logo span { color:var(--orange); text-shadow:0 0 20px var(--orange); }
.header-right { display:flex; gap:0.5rem; align-items:center; }
.nav-btn {
  background:transparent; border:1px solid var(--border);
  color:var(--gray2); padding:0.35rem 0.9rem;
  border-radius:4px; cursor:pointer; font-family:'Exo 2',sans-serif;
  font-size:0.8rem; font-weight:600; letter-spacing:0.05em;
  transition:all 0.2s; text-transform:uppercase;
}
.nav-btn:hover, .nav-btn.active { border-color:var(--orange); color:var(--orange); background:rgba(255,107,0,0.08); }
.live-badge {
  display:flex; align-items:center; gap:5px;
  background:rgba(255,45,45,0.12); border:1px solid rgba(255,45,45,0.4);
  color:#FF6B6B; padding:4px 10px; border-radius:20px; font-size:0.72rem; font-weight:700;
}
.live-dot { width:6px; height:6px; border-radius:50%; background:#FF2D2D; animation:blink 1s infinite; }
@keyframes blink { 0%,100%{opacity:1} 50%{opacity:0.2} }

/* ===== HERO ===== */
.hero {
  min-height:100vh;
  display:flex; align-items:center; justify-content:center;
  flex-direction:column; text-align:center;
  padding:5rem 1.5rem 3rem;
  position:relative; z-index:1;
}

/* Crosshair animation */
.crosshair-anim {
  position:relative; width:120px; height:120px; margin:0 auto 2.5rem;
}
.ch-ring {
  position:absolute; inset:0; border-radius:50%;
  border:2px solid rgba(255,107,0,0.2);
  animation:pulse-ring 2s ease-out infinite;
}
.ch-ring:nth-child(2) { animation-delay:0.7s; }
.ch-ring:nth-child(3) { animation-delay:1.4s; }
@keyframes pulse-ring {
  0%{transform:scale(0.5);opacity:0.8;} 100%{transform:scale(1.8);opacity:0;}
}
.ch-center {
  position:absolute; inset:30px;
  border-radius:50%; border:2px solid var(--orange);
  box-shadow:0 0 20px var(--orange-glow), inset 0 0 15px rgba(255,107,0,0.1);
  animation:spin 8s linear infinite;
}
@keyframes spin { to{transform:rotate(360deg);} }
.ch-dot {
  position:absolute; inset:0; display:flex; align-items:center; justify-content:center;
}
.ch-dot::before {
  content:'';
  width:8px; height:8px; border-radius:50%;
  background:var(--orange);
  box-shadow:0 0 12px var(--orange), 0 0 24px var(--orange-glow);
}
.ch-lines {
  position:absolute; inset:0;
  background:
    linear-gradient(var(--orange) 1px, transparent 1px) center/2px 100%,
    linear-gradient(90deg, var(--orange) 1px, transparent 1px) center/100% 2px;
  opacity:0.6;
}

.hero-eyebrow {
  font-family:'Orbitron',monospace; font-size:0.7rem;
  letter-spacing:0.25em; text-transform:uppercase; color:var(--orange);
  border:1px solid rgba(255,107,0,0.3); padding:4px 14px; border-radius:2px;
  margin-bottom:1.5rem; display:inline-block;
  animation:fadeIn 0.6s ease both;
}

.hero h1 {
  font-family:'Orbitron',monospace;
  font-size:clamp(2.5rem, 8vw, 6rem);
  font-weight:900; line-height:0.95;
  letter-spacing:-0.01em;
  animation:fadeIn 0.7s ease 0.1s both;
}
.hero h1 .line1 { display:block; color:var(--white); }
.hero h1 .line2 {
  display:block; color:transparent;
  -webkit-text-stroke:1px var(--orange);
  text-shadow:0 0 40px rgba(255,107,0,0.3);
}
.hero h1 .line3 { display:block; color:var(--orange); text-shadow:0 0 40px rgba(255,107,0,0.5); }

.hero-sub {
  max-width:560px; margin:1.5rem auto;
  font-size:1rem; color:var(--gray2); line-height:1.7;
  animation:fadeIn 0.7s ease 0.2s both;
}
.hero-sub strong { color:var(--white); }

.hero-stats {
  display:flex; gap:2rem; justify-content:center; margin:2rem 0;
  animation:fadeIn 0.7s ease 0.3s both; flex-wrap:wrap;
}
.hstat { text-align:center; }
.hstat-num {
  font-family:'Orbitron',monospace; font-size:1.8rem; font-weight:900;
  color:var(--orange); text-shadow:0 0 20px var(--orange-glow);
}
.hstat-label { font-size:0.72rem; color:var(--gray); text-transform:uppercase; letter-spacing:0.1em; }

.hero-btns { display:flex; gap:1rem; justify-content:center; flex-wrap:wrap; animation:fadeIn 0.7s ease 0.4s both; }

.btn-primary {
  background:var(--orange); color:#000;
  font-family:'Orbitron',monospace; font-size:0.85rem; font-weight:700;
  padding:0.8rem 2.2rem; border-radius:4px; border:none; cursor:pointer;
  letter-spacing:0.08em; text-transform:uppercase; text-decoration:none;
  transition:all 0.25s; position:relative; overflow:hidden;
  box-shadow:0 4px 20px rgba(255,107,0,0.4);
  display:inline-flex; align-items:center; gap:0.5rem;
}
.btn-primary::before {
  content:''; position:absolute; top:0; left:-100%; width:60%; height:100%;
  background:linear-gradient(90deg,transparent,rgba(255,255,255,0.3),transparent);
  transform:skewX(-20deg); animation:shine 2.5s infinite 1s;
}
@keyframes shine { to{left:200%;} }
.btn-primary:hover { background:#FF8C33; transform:translateY(-2px); box-shadow:0 8px 30px rgba(255,107,0,0.5); }

.btn-secondary {
  background:transparent; color:var(--orange);
  font-family:'Orbitron',monospace; font-size:0.85rem; font-weight:700;
  padding:0.8rem 2.2rem; border-radius:4px; border:1px solid var(--orange);
  cursor:pointer; letter-spacing:0.08em; text-transform:uppercase; text-decoration:none;
  transition:all 0.25s; display:inline-flex; align-items:center; gap:0.5rem;
}
.btn-secondary:hover { background:rgba(255,107,0,0.1); transform:translateY(-2px); }

@keyframes fadeIn { from{opacity:0;transform:translateY(18px);} to{opacity:1;transform:translateY(0);} }

/* ===== SECTION BASE ===== */
.section { padding:5rem 1.5rem; position:relative; z-index:1; }
.container { max-width:960px; margin:0 auto; }
.section-tag {
  font-family:'Orbitron',monospace; font-size:0.65rem;
  letter-spacing:0.2em; text-transform:uppercase;
  color:var(--orange); margin-bottom:0.75rem;
  display:flex; align-items:center; gap:0.5rem;
}
.section-tag::before { content:''; width:24px; height:1px; background:var(--orange); }
.section h2 {
  font-family:'Orbitron',monospace;
  font-size:clamp(1.6rem, 4vw, 2.8rem);
  font-weight:900; line-height:1.1; margin-bottom:1.2rem;
}
.section h2 .acc { color:var(--orange); }

/* ===== SENSITIVITY CALCULATOR ===== */
.calc-section {
  background:var(--dark);
  border-top:1px solid var(--border);
  border-bottom:1px solid var(--border);
}
.calc-grid {
  display:grid; grid-template-columns:1fr 1fr; gap:2rem; margin-top:2.5rem;
}
@media(max-width:700px){ .calc-grid{grid-template-columns:1fr;} }

.calc-panel {
  background:var(--card);
  border:1px solid var(--border);
  border-radius:8px; padding:1.8rem;
}
.calc-panel h3 {
  font-family:'Orbitron',monospace; font-size:0.9rem; font-weight:700;
  color:var(--orange); margin-bottom:1.5rem;
  display:flex; align-items:center; gap:0.5rem;
}

.field-group { margin-bottom:1.2rem; }
.field-label {
  display:flex; justify-content:space-between; align-items:center;
  font-size:0.8rem; font-weight:600; color:var(--gray2);
  text-transform:uppercase; letter-spacing:0.08em; margin-bottom:0.5rem;
}
.field-value {
  font-family:'Orbitron',monospace; font-weight:700;
  color:var(--orange); font-size:0.9rem;
}

.slider-wrap { position:relative; }
input[type=range] {
  width:100%; -webkit-appearance:none; appearance:none;
  height:4px; border-radius:2px; outline:none;
  background:linear-gradient(90deg, var(--orange) var(--pct,50%), var(--border) var(--pct,50%));
  cursor:pointer;
}
input[type=range]::-webkit-slider-thumb {
  -webkit-appearance:none; width:18px; height:18px; border-radius:50%;
  background:var(--orange); border:3px solid var(--bg);
  box-shadow:0 0 8px rgba(255,107,0,0.6);
  transition:transform 0.15s;
}
input[type=range]::-webkit-slider-thumb:hover { transform:scale(1.3); }

.select-field {
  width:100%; background:var(--dark); border:1px solid var(--border);
  color:var(--white); padding:0.6rem 0.9rem; border-radius:6px;
  font-family:'Exo 2',sans-serif; font-size:0.9rem; outline:none;
  cursor:pointer; transition:border 0.2s;
}
.select-field:focus { border-color:var(--orange); }

/* Results panel */
.result-panel {
  background:var(--card2);
  border:1px solid rgba(255,107,0,0.25);
  border-radius:8px; padding:1.5rem;
  box-shadow:0 0 30px rgba(255,107,0,0.06);
}
.result-panel h3 {
  font-family:'Orbitron',monospace; font-size:0.85rem;
  color:var(--orange); margin-bottom:1.2rem;
  display:flex; align-items:center; gap:0.5rem;
}
.result-row {
  display:flex; justify-content:space-between; align-items:center;
  padding:0.7rem 0; border-bottom:1px solid var(--border);
}
.result-row:last-child { border-bottom:none; }
.result-name { font-size:0.82rem; color:var(--gray2); }
.result-val {
  font-family:'Orbitron',monospace; font-weight:700;
  font-size:1rem; color:var(--white);
  background:rgba(255,107,0,0.1); border:1px solid rgba(255,107,0,0.3);
  padding:3px 12px; border-radius:4px;
  transition:all 0.3s;
}
.result-val.updated {
  color:var(--orange);
  box-shadow:0 0 12px rgba(255,107,0,0.4);
}

.copy-btn {
  width:100%; margin-top:1rem;
  background:rgba(255,107,0,0.1); border:1px solid rgba(255,107,0,0.4);
  color:var(--orange); padding:0.7rem;
  border-radius:6px; cursor:pointer; font-family:'Orbitron',monospace;
  font-size:0.75rem; font-weight:700; letter-spacing:0.1em; text-transform:uppercase;
  transition:all 0.2s; display:flex; align-items:center; justify-content:center; gap:0.5rem;
}
.copy-btn:hover { background:rgba(255,107,0,0.2); border-color:var(--orange); }
.copy-btn.copied { background:rgba(0,229,255,0.1); border-color:var(--cyan); color:var(--cyan); }

/* Accuracy meter */
.accuracy-meter {
  margin-top:1.5rem; padding-top:1.5rem; border-top:1px solid var(--border);
}
.acc-label { font-size:0.75rem; color:var(--gray); text-transform:uppercase; letter-spacing:0.1em; margin-bottom:0.5rem; }
.acc-bar-wrap { height:8px; background:var(--border); border-radius:4px; overflow:hidden; }
.acc-bar {
  height:100%; border-radius:4px;
  background:linear-gradient(90deg, var(--red), var(--yellow), #00C853);
  transition:width 0.5s cubic-bezier(0.34,1.56,0.64,1);
}
.acc-score {
  font-family:'Orbitron',monospace; font-size:1.8rem; font-weight:900;
  margin-top:0.5rem;
  transition:color 0.3s;
}

/* ===== PRESETS ===== */
.presets-section { padding:5rem 1.5rem; }
.presets-grid {
  display:grid; grid-template-columns:repeat(auto-fill,minmax(280px,1fr));
  gap:1.2rem; margin-top:2rem;
}
.preset-card {
  background:var(--card); border:1px solid var(--border); border-radius:8px;
  overflow:hidden; transition:all 0.25s; cursor:pointer;
  position:relative;
}
.preset-card::before {
  content:''; position:absolute; top:0; left:0; right:0; height:3px;
  background:linear-gradient(90deg, var(--orange), transparent); opacity:0;
  transition:opacity 0.25s;
}
.preset-card:hover { border-color:rgba(255,107,0,0.4); transform:translateY(-4px); box-shadow:0 8px 30px rgba(255,107,0,0.1); }
.preset-card:hover::before { opacity:1; }
.preset-card.active { border-color:var(--orange); box-shadow:0 0 20px rgba(255,107,0,0.15); }
.preset-card.active::before { opacity:1; }

.preset-head {
  padding:1.2rem 1.4rem;
  display:flex; align-items:center; justify-content:space-between;
  border-bottom:1px solid var(--border);
}
.preset-name { font-family:'Rajdhani',sans-serif; font-size:1.1rem; font-weight:700; }
.preset-badge {
  font-size:0.65rem; font-weight:800; letter-spacing:0.1em; text-transform:uppercase;
  padding:3px 8px; border-radius:3px;
}
.badge-pro { background:rgba(255,107,0,0.15); color:var(--orange); border:1px solid rgba(255,107,0,0.4); }
.badge-easy { background:rgba(0,229,255,0.1); color:var(--cyan); border:1px solid rgba(0,229,255,0.3); }
.badge-med { background:rgba(255,214,0,0.1); color:var(--yellow); border:1px solid rgba(255,214,0,0.3); }
.badge-sniper { background:rgba(255,45,45,0.1); color:#FF6B6B; border:1px solid rgba(255,45,45,0.3); }

.preset-body { padding:1.2rem 1.4rem; }
.preset-stat {
  display:flex; justify-content:space-between; align-items:center;
  padding:0.35rem 0; font-size:0.82rem;
}
.preset-stat-name { color:var(--gray2); }
.preset-stat-val {
  font-family:'Orbitron',monospace; font-size:0.78rem; font-weight:700; color:var(--white);
  background:var(--dark); padding:2px 8px; border-radius:3px;
}
.preset-desc { font-size:0.78rem; color:var(--gray); margin-top:0.75rem; line-height:1.5; border-top:1px solid var(--border); padding-top:0.75rem; }

.apply-btn {
  width:100%; margin-top:1rem;
  background:transparent; border:1px solid var(--border);
  color:var(--gray2); padding:0.6rem;
  border-radius:5px; cursor:pointer; font-family:'Orbitron',monospace;
  font-size:0.7rem; font-weight:700; letter-spacing:0.1em; text-transform:uppercase;
  transition:all 0.2s;
}
.apply-btn:hover { border-color:var(--orange); color:var(--orange); background:rgba(255,107,0,0.08); }
.preset-card.active .apply-btn { background:var(--orange); border-color:var(--orange); color:#000; }

/* ===== TIPS SECTION ===== */
.tips-section {
  background:var(--dark);
  border-top:1px solid var(--border);
  border-bottom:1px solid var(--border);
  padding:5rem 1.5rem;
}
.tips-grid {
  display:grid; grid-template-columns:repeat(auto-fill,minmax(240px,1fr));
  gap:1rem; margin-top:2rem;
}
.tip-card {
  background:var(--card); border:1px solid var(--border);
  border-radius:8px; padding:1.4rem;
  transition:all 0.25s;
  position:relative; overflow:hidden;
}
.tip-card::after {
  content:''; position:absolute; bottom:0; left:0; right:0; height:2px;
  background:linear-gradient(90deg, var(--orange), var(--orange2));
  transform:scaleX(0); transform-origin:left; transition:transform 0.3s;
}
.tip-card:hover { border-color:rgba(255,107,0,0.3); }
.tip-card:hover::after { transform:scaleX(1); }

.tip-icon { font-size:2rem; margin-bottom:0.75rem; }
.tip-title { font-family:'Rajdhani',sans-serif; font-size:1rem; font-weight:700; margin-bottom:0.4rem; }
.tip-text { font-size:0.82rem; color:var(--gray2); line-height:1.6; }

/* ===== SENSITIVITY GUIDE ===== */
.guide-section { padding:5rem 1.5rem; }
.guide-table {
  width:100%; border-collapse:collapse; margin-top:2rem;
  font-size:0.85rem;
}
.guide-table th {
  font-family:'Orbitron',monospace; font-size:0.7rem; font-weight:700;
  color:var(--orange); text-transform:uppercase; letter-spacing:0.1em;
  padding:0.75rem 1rem; border-bottom:2px solid var(--orange);
  text-align:left; background:var(--card);
}
.guide-table td {
  padding:0.75rem 1rem; border-bottom:1px solid var(--border);
  color:var(--gray2); vertical-align:middle;
}
.guide-table tr:hover td { background:rgba(255,107,0,0.04); color:var(--white); }
.guide-table td:first-child { font-weight:700; color:var(--white); }
.guide-table td:last-child { font-family:'Orbitron',monospace; font-size:0.8rem; }
.range-pill {
  display:inline-block;
  background:rgba(255,107,0,0.1); border:1px solid rgba(255,107,0,0.3);
  color:var(--orange); padding:2px 10px; border-radius:20px; font-size:0.75rem;
}

/* ===== DEVICE PROFILES ===== */
.device-section { padding:5rem 1.5rem; }
.device-tabs { display:flex; gap:0.5rem; flex-wrap:wrap; margin-bottom:2rem; }
.dtab {
  background:var(--card); border:1px solid var(--border);
  color:var(--gray2); padding:0.5rem 1.2rem; border-radius:4px;
  cursor:pointer; font-size:0.8rem; font-weight:600; font-family:'Exo 2',sans-serif;
  transition:all 0.2s; text-transform:uppercase; letter-spacing:0.05em;
}
.dtab.active, .dtab:hover { background:rgba(255,107,0,0.1); border-color:var(--orange); color:var(--orange); }
.device-content { display:none; }
.device-content.active { display:grid; grid-template-columns:repeat(auto-fill,minmax(200px,1fr)); gap:1rem; }
.dstat-card {
  background:var(--card); border:1px solid var(--border); border-radius:8px;
  padding:1.2rem; text-align:center; transition:border-color 0.2s;
}
.dstat-card:hover { border-color:rgba(255,107,0,0.3); }
.dstat-name { font-size:0.75rem; color:var(--gray); text-transform:uppercase; letter-spacing:0.08em; margin-bottom:0.5rem; }
.dstat-val {
  font-family:'Orbitron',monospace; font-size:1.6rem; font-weight:900; color:var(--orange);
  text-shadow:0 0 20px rgba(255,107,0,0.3);
}

/* ===== CTA SECTION ===== */
.cta-section {
  padding:6rem 1.5rem;
  text-align:center;
  background:radial-gradient(ellipse 70% 50% at 50% 50%, rgba(255,107,0,0.06) 0%, transparent 70%);
  position:relative; z-index:1;
}
.cta-box {
  background:var(--card); border:1px solid rgba(255,107,0,0.3);
  border-radius:12px; padding:3.5rem 2rem;
  max-width:680px; margin:0 auto;
  box-shadow:0 0 60px rgba(255,107,0,0.08);
  position:relative; overflow:hidden;
}
.cta-box::before {
  content:''; position:absolute; top:0; left:0; right:0; height:2px;
  background:linear-gradient(90deg, transparent, var(--orange), transparent);
}
.cta-box h2 {
  font-family:'Orbitron',monospace; font-size:clamp(1.5rem,5vw,2.5rem);
  font-weight:900; margin-bottom:1rem;
}
.cta-box p { color:var(--gray2); margin-bottom:2rem; line-height:1.7; font-size:0.95rem; }
.cta-features {
  display:flex; gap:1.5rem; justify-content:center; flex-wrap:wrap;
  margin-bottom:2rem;
}
.cta-feat { display:flex; align-items:center; gap:0.4rem; font-size:0.82rem; color:var(--gray2); }
.cta-feat span { color:var(--orange); }

/* ===== TOAST ===== */
.toast {
  position:fixed; bottom:2rem; left:50%; transform:translateX(-50%) translateY(80px);
  background:var(--card2); border:1px solid var(--orange);
  color:var(--orange); padding:0.75rem 1.5rem; border-radius:6px;
  font-family:'Orbitron',monospace; font-size:0.78rem; font-weight:700;
  z-index:999; transition:transform 0.4s cubic-bezier(0.34,1.56,0.64,1);
  box-shadow:0 4px 30px rgba(255,107,0,0.3);
  white-space:nowrap;
}
.toast.show { transform:translateX(-50%) translateY(0); }

/* ===== FOOTER ===== */
footer {
  background:var(--dark); border-top:1px solid var(--border);
  padding:2rem 1.5rem; text-align:center;
  color:var(--gray); font-size:0.78rem; line-height:1.8; position:relative; z-index:1;
}
footer strong { color:var(--orange); font-family:'Orbitron',monospace; }

/* Reveal */
.reveal { opacity:0; transform:translateY(24px); transition:all 0.6s ease; }
.reveal.visible { opacity:1; transform:translateY(0); }

/* Mobile tweaks */
@media(max-width:600px){
  .hero-stats { gap:1.2rem; }
  .hstat-num { font-size:1.4rem; }
  header { padding:0 1rem; }
  .logo { font-size:0.9rem; }
}
</style>
</head>
<body>

<div class="bg-layer"></div>
<div class="bg-grid"></div>
<div class="scanline"></div>

<!-- HEADER -->
<header>
  <div class="logo">FF<span>SENS</span>PRO</div>
  <div class="header-right">
    <button class="nav-btn active" onclick="scrollTo('#calculadora')">CALC</button>
    <button class="nav-btn" onclick="scrollTo('#presets')">PRESETS</button>
    <button class="nav-btn" onclick="scrollTo('#guia')">GUIA</button>
    <div class="live-badge"><div class="live-dot"></div> ONLINE</div>
  </div>
</header>

<!-- ===== HERO ===== -->
<section class="hero">
  <div class="crosshair-anim">
    <div class="ch-ring"></div>
    <div class="ch-ring"></div>
    <div class="ch-ring"></div>
    <div class="ch-center">
      <div class="ch-lines"></div>
    </div>
    <div class="ch-dot"></div>
  </div>

  <div class="hero-eyebrow">🎯 Configurações Profissionais Free Fire</div>

  <h1>
    <span class="line1">DOMINE A</span>
    <span class="line2">MIRA</span>
    <span class="line3">PERFEITA</span>
  </h1>

  <p class="hero-sub">
    Calcule sua <strong>sensibilidade ideal</strong>, aplique presets de jogadores profissionais e eleve seu nível com configurações otimizadas para seu dispositivo e estilo de jogo.
  </p>

  <div class="hero-stats">
    <div class="hstat">
      <div class="hstat-num">50K+</div>
      <div class="hstat-label">Jogadores</div>
    </div>
    <div class="hstat">
      <div class="hstat-num">98%</div>
      <div class="hstat-label">Aprovação</div>
    </div>
    <div class="hstat">
      <div class="hstat-num">12</div>
      <div class="hstat-label">Presets Pro</div>
    </div>
    <div class="hstat">
      <div class="hstat-num">3x</div>
      <div class="hstat-label">Mais Precisão</div>
    </div>
  </div>

  <div class="hero-btns">
    <a href="#calculadora" class="btn-primary" onclick="smoothScroll(event,'calculadora')">
      ⚡ CALCULAR MINHA SENS
    </a>
    <a href="#presets" class="btn-secondary" onclick="smoothScroll(event,'presets')">
      🏆 VER PRESETS PRO
    </a>
  </div>
</section>

<!-- ===== CALCULATOR ===== -->
<section class="section calc-section reveal" id="calculadora">
  <div class="container">
    <div class="section-tag">Sistema de Otimização</div>
    <h2>CALCULADORA DE <span class="acc">SENSIBILIDADE</span></h2>
    <p style="color:var(--gray2);max-width:560px;line-height:1.7;">Ajuste os parâmetros do seu setup e receba suas configurações personalizadas instantaneamente.</p>

    <div class="calc-grid">
      <!-- INPUTS -->
      <div class="calc-panel">
        <h3>⚙️ SEU PERFIL</h3>

        <div class="field-group">
          <div class="field-label">
            <span>Tamanho da Tela</span>
            <span class="field-value" id="screenVal">6.0"</span>
          </div>
          <input type="range" min="5" max="8" step="0.1" value="6" id="screenSize" oninput="updateCalc()">
        </div>

        <div class="field-group">
          <div class="field-label">
            <span>Sensibilidade Atual (Geral)</span>
            <span class="field-value" id="generalVal">80</span>
          </div>
          <input type="range" min="1" max="100" value="80" id="generalSens" oninput="updateCalc()">
        </div>

        <div class="field-group">
          <div class="field-label">
            <span>Estilo de Jogo</span>
          </div>
          <select class="select-field" id="playStyle" onchange="updateCalc()">
            <option value="rush">Rush / Agressivo</option>
            <option value="sniper">Sniper / Distância</option>
            <option value="balanced" selected>Equilibrado</option>
            <option value="camper">Defensor / Camper</option>
          </select>
        </div>

        <div class="field-group">
          <div class="field-label">
            <span>Tipo de Controle</span>
          </div>
          <select class="select-field" id="control" onchange="updateCalc()">
            <option value="2" selected>2 Dedos</option>
            <option value="3">3 Dedos</option>
            <option value="4">4 Dedos</option>
            <option value="claw">Claw / Garra</option>
          </select>
        </div>

        <div class="field-group">
          <div class="field-label">
            <span>DPI do Dispositivo</span>
            <span class="field-value" id="dpiVal">400</span>
          </div>
          <input type="range" min="200" max="800" step="50" value="400" id="dpiRange" oninput="updateCalc()">
        </div>
      </div>

      <!-- RESULTS -->
      <div>
        <div class="result-panel">
          <h3>🎯 CONFIGURAÇÕES OTIMIZADAS</h3>

          <div class="result-row">
            <span class="result-name">Sensibilidade Geral</span>
            <span class="result-val" id="r_geral">—</span>
          </div>
          <div class="result-row">
            <span class="result-name">Visão do Mapa</span>
            <span class="result-val" id="r_mapa">—</span>
          </div>
          <div class="result-row">
            <span class="result-name">Mira (vermelho)</span>
            <span class="result-val" id="r_mira">—</span>
          </div>
          <div class="result-row">
            <span class="result-name">Scope 2x</span>
            <span class="result-val" id="r_2x">—</span>
          </div>
          <div class="result-row">
            <span class="result-name">Scope 4x</span>
            <span class="result-val" id="r_4x">—</span>
          </div>
          <div class="result-row">
            <span class="result-name">AWM Scope</span>
            <span class="result-val" id="r_awm">—</span>
          </div>
          <div class="result-row">
            <span class="result-name">Sensitivity Free</span>
            <span class="result-val" id="r_free">—</span>
          </div>

          <button class="copy-btn" id="copyBtn" onclick="copySettings()">
            📋 COPIAR CONFIGURAÇÕES
          </button>
        </div>

        <!-- Accuracy -->
        <div style="background:var(--card);border:1px solid var(--border);border-radius:8px;padding:1.4rem;margin-top:1rem;">
          <div class="acc-label">Score de Precisão Estimado</div>
          <div class="acc-bar-wrap">
            <div class="acc-bar" id="accBar" style="width:0%"></div>
          </div>
          <div class="acc-score" id="accScore" style="color:var(--orange);">—</div>
          <div style="font-size:0.75rem;color:var(--gray);margin-top:0.25rem;" id="accMsg">Ajuste os parâmetros acima</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== PRESETS ===== -->
<section class="section presets-section reveal" id="presets">
  <div class="container">
    <div class="section-tag">Configurações Prontas</div>
    <h2>PRESETS <span class="acc">PROFISSIONAIS</span></h2>
    <p style="color:var(--gray2);max-width:560px;line-height:1.7;margin-bottom:0.5rem;">Configurações testadas e validadas por jogadores de alto nível. Clique para aplicar no calculador.</p>

    <div class="presets-grid" id="presetsGrid"></div>
  </div>
</section>

<!-- ===== TIPS ===== -->
<section class="section tips-section reveal">
  <div class="container">
    <div class="section-tag">Melhore Seu Jogo</div>
    <h2>DICAS DE <span class="acc">OTIMIZAÇÃO</span></h2>
    <div class="tips-grid">
      <div class="tip-card">
        <div class="tip-icon">📱</div>
        <div class="tip-title">Temperatura do Celular</div>
        <div class="tip-text">Mantenha o dispositivo fresco. Celular quente reduz o responsivo do touch em até 30%, prejudicando a precisão da mira diretamente.</div>
      </div>
      <div class="tip-card">
        <div class="tip-icon">🔋</div>
        <div class="tip-title">Modo de Desempenho</div>
        <div class="tip-text">Ative o modo de desempenho nas configurações do celular e dentro do Free Fire defina gráficos para Suave + Taxa de quadros Alta.</div>
      </div>
      <div class="tip-card">
        <div class="tip-icon">👆</div>
        <div class="tip-title">Treine a Consistência</div>
        <div class="tip-text">Use o modo treinamento por 15 min antes de ranked. Mantenha a mesma sensibilidade por ao menos 3 dias antes de alterar.</div>
      </div>
      <div class="tip-card">
        <div class="tip-icon">🎯</div>
        <div class="tip-title">Scope vs Mira Livre</div>
        <div class="tip-text">Para médio alcance, mira vermelha com sens 40-60 é mais eficaz que 4x. Reserve o scope para alvos acima de 50m de distância.</div>
      </div>
      <div class="tip-card">
        <div class="tip-icon">🖐️</div>
        <div class="tip-title">Posição dos Dedos</div>
        <div class="tip-text">Com 4 dedos, mantenha os dois polegares nos lados e os indicadores no shoot e mira. Reduz o tempo de reação em 0.3s.</div>
      </div>
      <div class="tip-card">
        <div class="tip-icon">⚡</div>
        <div class="tip-title">Recuo e Controle</div>
        <div class="tip-text">Pratique o controle de recuo no modo treinamento. A sens geral alta ajuda no rush, mas prejudica o controle de armas automáticas.</div>
      </div>
    </div>
  </div>
</section>

<!-- ===== GUIDE TABLE ===== -->
<section class="section guide-section reveal" id="guia">
  <div class="container">
    <div class="section-tag">Referência Rápida</div>
    <h2>GUIA DE <span class="acc">SENSIBILIDADES</span></h2>
    <p style="color:var(--gray2);margin-bottom:0.5rem;line-height:1.7;">Referência com as faixas recomendadas para cada tipo de jogador e situação de combate.</p>

    <table class="guide-table">
      <thead>
        <tr>
          <th>Configuração</th>
          <th>Rush / Agressivo</th>
          <th>Equilibrado</th>
          <th>Sniper / Distância</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Geral</td>
          <td><span class="range-pill">80–100</span></td>
          <td><span class="range-pill">60–80</span></td>
          <td><span class="range-pill">40–60</span></td>
        </tr>
        <tr>
          <td>Visão do Mapa</td>
          <td><span class="range-pill">85–100</span></td>
          <td><span class="range-pill">70–85</span></td>
          <td><span class="range-pill">60–75</span></td>
        </tr>
        <tr>
          <td>Mira (Vermelha)</td>
          <td><span class="range-pill">70–90</span></td>
          <td><span class="range-pill">50–70</span></td>
          <td><span class="range-pill">30–55</span></td>
        </tr>
        <tr>
          <td>Scope 2x</td>
          <td><span class="range-pill">50–70</span></td>
          <td><span class="range-pill">35–55</span></td>
          <td><span class="range-pill">25–45</span></td>
        </tr>
        <tr>
          <td>Scope 4x</td>
          <td><span class="range-pill">30–50</span></td>
          <td><span class="range-pill">20–35</span></td>
          <td><span class="range-pill">10–25</span></td>
        </tr>
        <tr>
          <td>AWM / Sniper</td>
          <td><span class="range-pill">20–35</span></td>
          <td><span class="range-pill">10–20</span></td>
          <td><span class="range-pill">5–15</span></td>
        </tr>
        <tr>
          <td>Sens. Livre</td>
          <td><span class="range-pill">80–100</span></td>
          <td><span class="range-pill">60–80</span></td>
          <td><span class="range-pill">50–70</span></td>
        </tr>
      </tbody>
    </table>
  </div>
</section>

<!-- ===== DEVICE PROFILES ===== -->
<section class="section device-section reveal">
  <div class="container">
    <div class="section-tag">Por Dispositivo</div>
    <h2>CONFIGS POR <span class="acc">CELULAR</span></h2>
    <p style="color:var(--gray2);margin-bottom:1.5rem;line-height:1.7;">Configurações otimizadas para as linhas de celular mais populares no Free Fire Brasil.</p>

    <div class="device-tabs">
      <div class="dtab active" onclick="switchDevice('samsung')">Samsung</div>
      <div class="dtab" onclick="switchDevice('redmi')">Redmi / Xiaomi</div>
      <div class="dtab" onclick="switchDevice('moto')">Motorola</div>
      <div class="dtab" onclick="switchDevice('iphone')">iPhone</div>
      <div class="dtab" onclick="switchDevice('realme')">Realme / POCO</div>
    </div>

    <div class="device-content active" id="dev_samsung">
      <div class="dstat-card"><div class="dstat-name">Geral</div><div class="dstat-val">78</div></div>
      <div class="dstat-card"><div class="dstat-name">Mapa</div><div class="dstat-val">80</div></div>
      <div class="dstat-card"><div class="dstat-name">Mira</div><div class="dstat-val">65</div></div>
      <div class="dstat-card"><div class="dstat-name">Scope 2x</div><div class="dstat-val">48</div></div>
      <div class="dstat-card"><div class="dstat-name">Scope 4x</div><div class="dstat-val">28</div></div>
      <div class="dstat-card"><div class="dstat-name">AWM</div><div class="dstat-val">12</div></div>
    </div>
    <div class="device-content" id="dev_redmi">
      <div class="dstat-card"><div class="dstat-name">Geral</div><div class="dstat-val">85</div></div>
      <div class="dstat-card"><div class="dstat-name">Mapa</div><div class="dstat-val">88</div></div>
      <div class="dstat-card"><div class="dstat-name">Mira</div><div class="dstat-val">70</div></div>
      <div class="dstat-card"><div class="dstat-name">Scope 2x</div><div class="dstat-val">52</div></div>
      <div class="dstat-card"><div class="dstat-name">Scope 4x</div><div class="dstat-val">32</div></div>
      <div class="dstat-card"><div class="dstat-name">AWM</div><div class="dstat-val">15</div></div>
    </div>
    <div class="device-content" id="dev_moto">
      <div class="dstat-card"><div class="dstat-name">Geral</div><div class="dstat-val">75</div></div>
      <div class="dstat-card"><div class="dstat-name">Mapa</div><div class="dstat-val">78</div></div>
      <div class="dstat-card"><div class="dstat-name">Mira</div><div class="dstat-val">62</div></div>
      <div class="dstat-card"><div class="dstat-name">Scope 2x</div><div class="dstat-val">45</div></div>
      <div class="dstat-card"><div class="dstat-name">Scope 4x</div><div class="dstat-val">25</div></div>
      <div class="dstat-card"><div class="dstat-name">AWM</div><div class="dstat-val">10</div></div>
    </div>
    <div class="device-content" id="dev_iphone">
      <div class="dstat-card"><div class="dstat-name">Geral</div><div class="dstat-val">72</div></div>
      <div class="dstat-card"><div class="dstat-name">Mapa</div><div class="dstat-val">75</div></div>
      <div class="dstat-card"><div class="dstat-name">Mira</div><div class="dstat-val">58</div></div>
      <div class="dstat-card"><div class="dstat-name">Scope 2x</div><div class="dstat-val">42</div></div>
      <div class="dstat-card"><div class="dstat-name">Scope 4x</div><div class="dstat-val">22</div></div>
      <div class="dstat-card"><div class="dstat-name">AWM</div><div class="dstat-val">8</div></div>
    </div>
    <div class="device-content" id="dev_realme">
      <div class="dstat-card"><div class="dstat-name">Geral</div><div class="dstat-val">90</div></div>
      <div class="dstat-card"><div class="dstat-name">Mapa</div><div class="dstat-val">92</div></div>
      <div class="dstat-card"><div class="dstat-name">Mira</div><div class="dstat-val">75</div></div>
      <div class="dstat-card"><div class="dstat-name">Scope 2x</div><div class="dstat-val">55</div></div>
      <div class="dstat-card"><div class="dstat-name">Scope 4x</div><div class="dstat-val">35</div></div>
      <div class="dstat-card"><div class="dstat-name">AWM</div><div class="dstat-val">18</div></div>
    </div>
  </div>
</section>

<!-- ===== CTA ===== -->
<section class="cta-section reveal">
  <div class="cta-box">
    <div class="section-tag" style="justify-content:center;">Pronto Para Evoluir?</div>
    <h2>CALCULE SUA SENS <span style="color:var(--orange)">AGORA</span></h2>
    <p>Use o calculador acima gratuitamente. Ajuste, teste nos modos de treino do Free Fire e domine cada partida com configurações feitas para o seu estilo.</p>
    <div class="cta-features">
      <div class="cta-feat"><span>✔</span> 100% Gratuito</div>
      <div class="cta-feat"><span>✔</span> Personalizado</div>
      <div class="cta-feat"><span>✔</span> Atualizado 2025</div>
      <div class="cta-feat"><span>✔</span> 12 Presets Pro</div>
    </div>
    <a href="#calculadora" class="btn-primary" onclick="smoothScroll(event,'calculadora')" style="font-size:0.9rem;padding:0.9rem 2.5rem;">
      ⚡ IR PARA O CALCULADOR
    </a>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <strong>FF SENS PRO</strong> — Configurações Profissionais Free Fire
  <br>
  Este site é um guia independente de configurações. Não é afiliado à Garena ou Free Fire.
  <br>
  © 2025 FF Sens Pro. Todos os direitos reservados.
</footer>

<!-- TOAST -->
<div class="toast" id="toast">✅ CONFIGURAÇÕES COPIADAS!</div>

<script>
// ===== PRESETS DATA =====
const presets = [
  { name:'Rush Master', badge:'PRO', badgeClass:'badge-pro', style:'rush', control:'4', geral:95, mapa:100, mira:85, s2x:60, s4x:38, awm:20, free:98, desc:'Ideal para quem joga agressivo e precisa de resposta ultra-rápida no curto alcance.' },
  { name:'Iniciante+', badge:'FÁCIL', badgeClass:'badge-easy', style:'balanced', control:'2', geral:65, mapa:70, mira:55, s2x:40, s4x:22, awm:10, free:70, desc:'Configuração suave, ideal para quem está começando e quer melhorar a consistência.' },
  { name:'Equilibrado FF', badge:'MED', badgeClass:'badge-med', style:'balanced', control:'3', geral:78, mapa:82, mira:65, s2x:48, s4x:28, awm:13, free:80, desc:'O ponto de equilíbrio entre velocidade e precisão. Funciona bem em qualquer mapa.' },
  { name:'Sniper Elite', badge:'SNP', badgeClass:'badge-sniper', style:'sniper', control:'2', geral:50, mapa:60, mira:40, s2x:30, s4x:15, awm:7, free:55, desc:'Sensibilidades baixas para máxima precisão em longas distâncias com AWM e M82B.' },
  { name:'Claw 4 Dedos', badge:'PRO', badgeClass:'badge-pro', style:'rush', control:'claw', geral:88, mapa:90, mira:75, s2x:55, s4x:33, awm:18, free:92, desc:'Configuração claw otimizada para máximo controle e agilidade com 4 dedos.' },
  { name:'Mid Range', badge:'MED', badgeClass:'badge-med', style:'balanced', control:'3', geral:70, mapa:75, mira:58, s2x:42, s4x:25, awm:11, free:72, desc:'Perfeito para combates de médio alcance com AR e SMG em zonas urbanas.' },
];

function buildPresets() {
  const grid = document.getElementById('presetsGrid');
  grid.innerHTML = presets.map((p,i) => `
    <div class="preset-card" id="pc${i}" onclick="applyPreset(${i})">
      <div class="preset-head">
        <div class="preset-name">${p.name}</div>
        <div class="preset-badge ${p.badgeClass}">${p.badge}</div>
      </div>
      <div class="preset-body">
        <div class="preset-stat"><span class="preset-stat-name">Geral</span><span class="preset-stat-val">${p.geral}</span></div>
        <div class="preset-stat"><span class="preset-stat-name">Mira</span><span class="preset-stat-val">${p.mira}</span></div>
        <div class="preset-stat"><span class="preset-stat-name">Scope 2x</span><span class="preset-stat-val">${p.s2x}</span></div>
        <div class="preset-stat"><span class="preset-stat-name">Scope 4x</span><span class="preset-stat-val">${p.s4x}</span></div>
        <div class="preset-stat"><span class="preset-stat-name">AWM</span><span class="preset-stat-val">${p.awm}</span></div>
        <div class="preset-desc">${p.desc}</div>
        <button class="apply-btn" id="apb${i}">APLICAR PRESET</button>
      </div>
    </div>
  `).join('');
}

function applyPreset(i) {
  const p = presets[i];
  // Update sliders
  document.getElementById('generalSens').value = p.geral;
  document.getElementById('playStyle').value = p.style;
  document.getElementById('control').value = p.control;
  // Mark active
  document.querySelectorAll('.preset-card').forEach((c,j) => {
    c.classList.toggle('active', j===i);
  });
  // Calc
  updateCalc(p);
  showToast('🎯 PRESET "' + p.name.toUpperCase() + '" APLICADO!');
  document.getElementById('calculadora').scrollIntoView({behavior:'smooth'});
}

// ===== CALCULATOR =====
let lastResults = {};

function clamp(v,min,max) { return Math.round(Math.max(min, Math.min(max, v))); }

function updateCalc(preset) {
  const screen = parseFloat(document.getElementById('screenSize').value);
  const general = parseInt(document.getElementById('generalSens').value);
  const style = document.getElementById('playStyle').value;
  const control = document.getElementById('control').value;
  const dpi = parseInt(document.getElementById('dpiRange').value);

  document.getElementById('screenVal').textContent = screen.toFixed(1) + '"';
  document.getElementById('generalVal').textContent = general;
  document.getElementById('dpiVal').textContent = dpi;

  // Update slider bg
  document.querySelectorAll('input[type=range]').forEach(r => {
    const pct = ((r.value - r.min) / (r.max - r.min) * 100).toFixed(1) + '%';
    r.style.setProperty('--pct', pct);
  });

  // Style multipliers
  const mult = { rush:1.15, sniper:0.65, balanced:1.0, camper:0.8 };
  const cm = { '2':1.0, '3':1.05, '4':1.1, 'claw':1.12 };
  const screenFactor = 1 - (screen - 6) * 0.04;
  const dpiFactor = 400 / dpi;
  const m = (mult[style]||1) * (cm[control]||1) * screenFactor * dpiFactor;

  const use = preset ? null : null;
  let r_geral, r_mapa, r_mira, r_2x, r_4x, r_awm, r_free;

  if (preset) {
    r_geral = preset.geral; r_mapa = preset.mapa; r_mira = preset.mira;
    r_2x = preset.s2x; r_4x = preset.s4x; r_awm = preset.awm; r_free = preset.free;
  } else {
    r_geral = clamp(general * m, 5, 100);
    r_mapa  = clamp(r_geral * 1.05, 5, 100);
    r_mira  = clamp(r_geral * 0.82, 5, 100);
    r_2x    = clamp(r_geral * 0.62, 5, 80);
    r_4x    = clamp(r_geral * 0.36, 5, 60);
    r_awm   = clamp(r_geral * 0.16, 3, 30);
    r_free  = clamp(r_geral * 1.02, 5, 100);
  }

  // Update UI with flash
  const fields = { r_geral, r_mapa, r_mira, r_2x, r_4x, r_awm, r_free };
  for (const [id, val] of Object.entries(fields)) {
    const el = document.getElementById(id);
    el.textContent = val;
    el.classList.remove('updated');
    void el.offsetWidth;
    el.classList.add('updated');
    setTimeout(()=>el.classList.remove('updated'), 600);
  }
  lastResults = { r_geral, r_mapa, r_mira, r_2x, r_4x, r_awm, r_free };

  // Accuracy score
  const styleScores = { rush:82, sniper:90, balanced:88, camper:75 };
  const controlBonus = { '2':0, '3':3, '4':6, 'claw':8 };
  const base = styleScores[style] || 80;
  const bonus = controlBonus[control] || 0;
  const screenBonus = screen >= 6 && screen <= 7 ? 2 : -1;
  const score = Math.min(99, base + bonus + screenBonus);

  const bar = document.getElementById('accBar');
  const scoreEl = document.getElementById('accScore');
  const msgEl = document.getElementById('accMsg');
  bar.style.width = score + '%';

  const color = score >= 85 ? '#00C853' : score >= 70 ? var_css('--yellow') : var_css('--red');
  scoreEl.style.color = score >= 85 ? '#00C853' : score >= 70 ? '#FFD600' : '#FF2D2D';
  scoreEl.textContent = score + '/100';
  msgEl.textContent = score >= 90 ? '🔥 Configuração Excelente!' : score >= 80 ? '✅ Boa Configuração' : score >= 70 ? '⚠️ Aceitável — ajuste o controle' : '❌ Ajuste o estilo de jogo';
}

function var_css(name) {
  return getComputedStyle(document.documentElement).getPropertyValue(name).trim();
}

function copySettings() {
  const { r_geral, r_mapa, r_mira, r_2x, r_4x, r_awm, r_free } = lastResults;
  if (!r_geral) { showToast('⚠️ CALCULE PRIMEIRO!'); return; }
  const text =
`━━━━━ FF SENS PRO ━━━━━
Geral:        ${r_geral}
Visão Mapa:   ${r_mapa}
Mira (red):   ${r_mira}
Scope 2x:     ${r_2x}
Scope 4x:     ${r_4x}
AWM Scope:    ${r_awm}
Sens. Livre:  ${r_free}
━━━━━━━━━━━━━━━━━━━━━`;
  navigator.clipboard.writeText(text).then(() => {
    const btn = document.getElementById('copyBtn');
    btn.textContent = '✅ COPIADO!';
    btn.classList.add('copied');
    setTimeout(() => { btn.textContent = '📋 COPIAR CONFIGURAÇÕES'; btn.classList.remove('copied'); }, 2000);
    showToast('✅ CONFIGURAÇÕES COPIADAS!');
  });
}

// ===== DEVICE TABS =====
function switchDevice(id) {
  document.querySelectorAll('.device-content').forEach(el => el.classList.remove('active'));
  document.querySelectorAll('.dtab').forEach(el => el.classList.remove('active'));
  document.getElementById('dev_' + id).classList.add('active');
  event.target.classList.add('active');
}

// ===== TOAST =====
function showToast(msg) {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('show');
  setTimeout(() => t.classList.remove('show'), 2800);
}

// ===== SCROLL =====
function smoothScroll(e, id) {
  e.preventDefault();
  document.getElementById(id).scrollIntoView({ behavior:'smooth' });
}
function scrollTo(id) {
  document.querySelector(id).scrollIntoView({ behavior:'smooth' });
}

// ===== SCROLL REVEAL =====
const obs = new IntersectionObserver(entries => {
  entries.forEach(e => { if(e.isIntersecting) e.target.classList.add('visible'); });
}, { threshold:0.08 });
document.querySelectorAll('.reveal').forEach(el => obs.observe(el));

// ===== INIT =====
buildPresets();
updateCalc();
</script>
</body>
</html>

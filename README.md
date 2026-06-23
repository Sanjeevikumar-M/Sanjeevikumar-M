<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sanjeevikumar M — AI Engineer & Systems Builder</title>
<meta name="description" content="Sanjeevikumar M — AI Engineer building intelligent systems across Artificial Intelligence, IoT and Embedded Engineering.">
<meta property="og:title" content="Sanjeevikumar M — AI Engineer & Systems Builder">
<meta property="og:description" content="Building intelligent systems with AI, IoT & Embedded Engineering.">
<meta property="og:type" content="website">
<meta name="theme-color" content="#050505">
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Ccircle cx='8' cy='24' r='3' fill='%23ff003c'/%3E%3Ccircle cx='24' cy='24' r='3' fill='%23ff003c'/%3E%3Ccircle cx='16' cy='8' r='3' fill='%23ff003c'/%3E%3Cpath d='M8 24L16 8L24 24' stroke='%23ff003c' stroke-width='1.5' fill='none'/%3E%3C/svg%3E">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;600;700&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
/* ============================================================
   TOKENS
============================================================ */
:root{
  --void:#050505;
  --panel:#0b0b0e;
  --signal:#ff003c;
  --signal-soft:rgba(255,0,60,.5);
  --ember:#8a0a1f;
  --bone:#f3f2f0;
  --mist:#9a9aa3;
  --mist-dim:#65656d;
  --glass:rgba(255,255,255,.035);
  --glass-hover:rgba(255,255,255,.06);
  --border:rgba(255,255,255,.09);
  --border-hover:rgba(255,0,60,.4);
  --font-display:'Space Grotesk',sans-serif;
  --font-body:'Inter',sans-serif;
  --font-mono:'JetBrains Mono',monospace;
  --container:1180px;
  --radius:18px;
  --radius-sm:10px;
  --ease:cubic-bezier(.22,1,.36,1);
  --nav-h:76px;
}

*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
html{scroll-behavior:smooth;}
html.reduced-motion{scroll-behavior:auto;}
body{
  background:var(--void);
  color:var(--bone);
  font-family:var(--font-body);
  font-size:16px;
  line-height:1.7;
  overflow-x:hidden;
  -webkit-font-smoothing:antialiased;
}
img,svg{display:block;max-width:100%;}
a{color:inherit;text-decoration:none;}
ul{list-style:none;}
button{font-family:inherit;cursor:pointer;background:none;border:none;color:inherit;}
::selection{background:var(--signal);color:#fff;}

:focus-visible{outline:2px solid var(--signal);outline-offset:3px;border-radius:4px;}

.skip-link{
  position:absolute;left:-9999px;top:0;background:var(--signal);color:#fff;
  padding:10px 16px;z-index:999;font-family:var(--font-mono);font-size:.85rem;
}
.skip-link:focus{left:12px;top:12px;}

.container{
  max-width:var(--container);
  margin-inline:auto;
  padding-inline:clamp(20px,5vw,40px);
}

section{position:relative;padding-block:clamp(80px,12vw,140px);}

/* grain overlay */
.grain{
  position:fixed;inset:0;z-index:2;pointer-events:none;opacity:.05;mix-blend-mode:overlay;
  background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='2' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
}

#bg-particles{position:fixed;inset:0;z-index:0;pointer-events:none;}

.cursor-glow{
  position:fixed;width:420px;height:420px;border-radius:50%;
  background:radial-gradient(circle,rgba(255,0,60,.16),transparent 70%);
  pointer-events:none;z-index:1;transform:translate(-50%,-50%);
  will-change:transform;transition:opacity .3s;
}
@media (hover:none){.cursor-glow{display:none;}}
html.reduced-motion .cursor-glow{display:none;}

main{position:relative;z-index:1;}

/* ============================================================
   TYPE
============================================================ */
.eyebrow{
  font-family:var(--font-mono);
  font-size:.78rem;
  letter-spacing:.06em;
  color:var(--signal);
  display:inline-flex;
  align-items:center;
  gap:8px;
  margin-bottom:18px;
}
.eyebrow::before{content:'';width:7px;height:7px;border-radius:50%;background:var(--signal);box-shadow:0 0 10px var(--signal);}

h1,h2,h3{font-family:var(--font-display);font-weight:600;letter-spacing:-.01em;color:var(--bone);}
.section-title{font-size:clamp(2rem,4vw,2.9rem);margin-bottom:18px;}
.section-head{max-width:680px;margin-bottom:56px;}
.section-head p{color:var(--mist);font-size:1.05rem;max-width:560px;}
.muted{color:var(--mist);}

/* ============================================================
   NAV
============================================================ */
.nav{
  position:fixed;top:0;left:0;right:0;z-index:50;
  height:var(--nav-h);
  display:flex;align-items:center;
  background:rgba(5,5,5,.55);
  border-bottom:1px solid transparent;
  backdrop-filter:blur(18px) saturate(140%);
  -webkit-backdrop-filter:blur(18px) saturate(140%);
  transition:border-color .4s,background .4s;
}
.nav.scrolled{background:rgba(5,5,5,.82);border-bottom-color:var(--border);}
.nav .container{display:flex;align-items:center;justify-content:space-between;width:100%;}
.logo{font-family:var(--font-display);font-weight:700;font-size:1.25rem;letter-spacing:-.02em;}
.logo span{color:var(--signal);}
.nav-links{display:flex;gap:34px;font-family:var(--font-mono);font-size:.85rem;}
.nav-links a{color:var(--mist);position:relative;padding-bottom:4px;transition:color .3s;}
.nav-links a:hover{color:var(--bone);}
.nav-links a::after{
  content:'';position:absolute;left:0;bottom:0;width:0;height:1px;background:var(--signal);
  transition:width .3s var(--ease);
}
.nav-links a:hover::after{width:100%;}
.nav-actions{display:flex;align-items:center;gap:16px;}
.nav-cta{
  display:flex;align-items:center;gap:8px;
  font-family:var(--font-mono);font-size:.8rem;
  border:1px solid var(--border);padding:9px 16px;border-radius:999px;
  transition:border-color .3s,background .3s,transform .3s;
}
.nav-cta:hover{border-color:var(--border-hover);background:var(--glass-hover);transform:translateY(-1px);}
.nav-cta svg{width:14px;height:14px;}
.nav-toggle{display:none;width:40px;height:40px;align-items:center;justify-content:center;}
.nav-toggle svg{width:22px;height:22px;}

.mobile-panel{
  position:fixed;top:var(--nav-h);left:0;right:0;z-index:49;
  background:rgba(5,5,5,.97);border-bottom:1px solid var(--border);
  display:flex;flex-direction:column;padding:24px clamp(20px,5vw,40px) 32px;gap:20px;
  transform:translateY(-110%);transition:transform .45s var(--ease);
}
.mobile-panel.open{transform:translateY(0);}
.mobile-panel a{font-family:var(--font-mono);font-size:1rem;color:var(--mist);}
.mobile-panel a:hover{color:var(--bone);}

@media (max-width:860px){
  .nav-links{display:none;}
  .nav-toggle{display:flex;}
  .nav-cta span.label{display:none;}
}

/* ============================================================
   BUTTONS
============================================================ */
.btn-row{display:flex;flex-wrap:wrap;gap:14px;}
.btn{
  display:inline-flex;align-items:center;gap:10px;
  font-family:var(--font-mono);font-size:.85rem;font-weight:500;
  padding:14px 24px;border-radius:999px;
  transition:transform .35s var(--ease),box-shadow .35s var(--ease),border-color .35s,background .35s;
  white-space:nowrap;
}
.btn svg{width:15px;height:15px;}
.btn-primary{
  background:linear-gradient(135deg,var(--signal),var(--ember));
  color:#fff;border:1px solid transparent;
}
.btn-primary:hover{transform:translateY(-3px);box-shadow:0 16px 40px -12px rgba(255,0,60,.55);}
.btn-outline{
  background:var(--glass);border:1px solid var(--border);color:var(--bone);
  backdrop-filter:blur(10px);
}
.btn-outline:hover{border-color:var(--border-hover);background:var(--glass-hover);transform:translateY(-3px);}

/* ============================================================
   HERO
============================================================ */
#hero{
  min-height:100vh;
  display:flex;align-items:center;
  padding-top:calc(var(--nav-h) + 40px);
  overflow:hidden;
}
#neural-canvas{position:absolute;inset:0;z-index:0;}
.hero-inner{position:relative;z-index:1;width:100%;text-align:center;}
.hero-kicker{
  font-family:var(--font-mono);color:var(--mist);font-size:.85rem;
  letter-spacing:.06em;margin-bottom:22px;
}
.hero-kicker .blink{color:var(--signal);animation:blink 1.1s steps(1) infinite;}
.hero-name{
  font-size:clamp(2.6rem,9vw,6.4rem);
  line-height:.96;font-weight:700;
  background:linear-gradient(180deg,#ffffff 0%,#cfcfd2 60%,#8d8d92 100%);
  -webkit-background-clip:text;background-clip:text;color:transparent;
  margin-bottom:22px;
}
.hero-headline{
  font-family:var(--font-display);font-weight:500;color:var(--bone);
  font-size:clamp(1.1rem,2.6vw,1.6rem);max-width:760px;margin:0 auto 26px;line-height:1.35;
}
.hero-roles{
  font-family:var(--font-mono);font-size:clamp(1rem,2vw,1.15rem);color:var(--signal);
  margin-bottom:26px;height:1.6em;
}
.hero-roles .cursor{display:inline-block;width:2px;background:var(--signal);margin-left:2px;animation:blink 1s steps(1) infinite;}
.hero-desc{
  max-width:620px;margin:0 auto 40px;color:var(--mist);font-size:1.02rem;
}
.hero .btn-row{justify-content:center;margin-bottom:64px;}
.float-tags{display:flex;flex-wrap:wrap;justify-content:center;gap:12px;max-width:760px;margin-inline:auto;}
.float-tag{
  font-family:var(--font-mono);font-size:.78rem;color:var(--mist);
  border:1px solid var(--border);padding:8px 16px;border-radius:999px;
  background:var(--glass);backdrop-filter:blur(8px);
  animation:floatTag 4s ease-in-out infinite;
}
html.reduced-motion .float-tag{animation:none;}
@keyframes floatTag{0%,100%{transform:translateY(0);}50%{transform:translateY(-7px);}}
@keyframes blink{0%,50%{opacity:1;}51%,100%{opacity:0;}}

.scroll-cue{
  position:absolute;bottom:32px;left:50%;transform:translateX(-50%);
  display:flex;flex-direction:column;align-items:center;gap:8px;z-index:1;
  font-family:var(--font-mono);font-size:.7rem;color:var(--mist-dim);letter-spacing:.1em;
}
.scroll-cue .line{width:1px;height:36px;background:linear-gradient(var(--mist-dim),transparent);animation:scrollLine 2s ease-in-out infinite;}
html.reduced-motion .scroll-cue .line{animation:none;}
@keyframes scrollLine{0%{transform:scaleY(0);transform-origin:top;}50%{transform:scaleY(1);transform-origin:top;}50.01%{transform-origin:bottom;}100%{transform:scaleY(0);transform-origin:bottom;}}

/* ============================================================
   REVEAL
============================================================ */
.reveal{opacity:0;transform:translateY(28px);transition:opacity .8s var(--ease),transform .8s var(--ease);}
.reveal.is-visible{opacity:1;transform:none;}
html.reduced-motion .reveal{opacity:1;transform:none;transition:none;}

/* ============================================================
   ABOUT
============================================================ */
#about .about-grid{display:grid;grid-template-columns:1.2fr .8fr;gap:64px;align-items:start;}
.about-list{margin-top:26px;display:flex;flex-direction:column;gap:12px;}
.about-list li{
  font-family:var(--font-mono);font-size:.92rem;color:var(--bone);
  display:flex;align-items:center;gap:10px;
}
.about-list li::before{content:'›';color:var(--signal);font-weight:700;}
.pull{
  margin-top:30px;padding-left:20px;border-left:2px solid var(--signal);
  font-family:var(--font-display);font-size:1.15rem;color:var(--bone);font-weight:500;
}
.orbit-wrap{display:flex;align-items:center;justify-content:center;min-height:320px;}
.orbit{width:280px;height:280px;position:relative;}
.orbit svg{width:100%;height:100%;}
.orbit-ring{animation:spin 22s linear infinite;transform-origin:center;}
.orbit-ring.rev{animation-direction:reverse;animation-duration:30s;}
html.reduced-motion .orbit-ring{animation:none;}
@keyframes spin{to{transform:rotate(360deg);}}

@media (max-width:860px){
  #about .about-grid{grid-template-columns:1fr;gap:40px;}
  .orbit-wrap{order:-1;min-height:220px;}
  .orbit{width:200px;height:200px;}
}

/* ============================================================
   GLASS CARD BASE
============================================================ */
.glass{
  background:var(--glass);border:1px solid var(--border);border-radius:var(--radius);
  backdrop-filter:blur(20px) saturate(140%);-webkit-backdrop-filter:blur(20px) saturate(140%);
  transition:border-color .4s var(--ease),transform .4s var(--ease),box-shadow .4s var(--ease),background .4s var(--ease);
}
.glass:hover{
  border-color:var(--border-hover);background:var(--glass-hover);
  transform:translateY(-6px);box-shadow:0 24px 60px -24px rgba(255,0,60,.3);
}

/* ============================================================
   EXPERTISE
============================================================ */
.expertise-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:22px;}
.expertise-card{padding:34px 28px;}
.expertise-card .icon-box{
  width:48px;height:48px;border-radius:12px;
  background:rgba(255,0,60,.08);border:1px solid rgba(255,0,60,.18);
  display:flex;align-items:center;justify-content:center;margin-bottom:22px;
  transition:background .4s,transform .4s;
}
.expertise-card svg{width:22px;height:22px;color:var(--signal);}
.expertise-card:hover .icon-box{background:rgba(255,0,60,.16);transform:scale(1.08) rotate(-4deg);}
.expertise-card h3{font-size:1.15rem;margin-bottom:10px;}
.expertise-card p{color:var(--mist);font-size:.92rem;}

@media (max-width:900px){.expertise-grid{grid-template-columns:repeat(2,1fr);}}
@media (max-width:560px){.expertise-grid{grid-template-columns:1fr;}}

/* ============================================================
   PROJECTS
============================================================ */
.project-list{display:flex;flex-direction:column;gap:28px;}
.project-card{
  display:grid;grid-template-columns:.85fr 1.15fr;gap:0;overflow:hidden;
}
.project-card:nth-child(even){grid-template-columns:1.15fr .85fr;}
.project-card:nth-child(even) .project-visual{order:2;}
.project-visual{
  position:relative;min-height:260px;background:radial-gradient(circle at 30% 20%,rgba(255,0,60,.12),transparent 60%),#0a0a0c;
  display:flex;align-items:center;justify-content:center;border-right:1px solid var(--border);
}
.project-card:nth-child(even) .project-visual{border-right:none;border-left:1px solid var(--border);}
.project-visual svg{width:90%;height:90%;max-width:280px;}
.project-body{padding:38px;display:flex;flex-direction:column;gap:14px;}
.project-index{font-family:var(--font-mono);color:var(--signal);font-size:.8rem;}
.project-body h3{font-size:1.5rem;}
.project-body p{color:var(--mist);font-size:.96rem;}
.project-tags{display:flex;flex-wrap:wrap;gap:8px;margin-top:6px;}
.project-tags span{
  font-family:var(--font-mono);font-size:.72rem;color:var(--mist);
  border:1px solid var(--border);padding:5px 12px;border-radius:999px;
}
.project-link{
  margin-top:10px;display:inline-flex;align-items:center;gap:8px;
  font-family:var(--font-mono);font-size:.82rem;color:var(--bone);
  border-bottom:1px solid transparent;transition:border-color .3s,color .3s,gap .3s;
}
.project-link svg{width:14px;height:14px;transition:transform .3s;}
.project-link:hover{color:var(--signal);border-color:var(--signal);}
.project-link:hover svg{transform:translate(3px,-3px);}

@media (max-width:760px){
  .project-card,.project-card:nth-child(even){grid-template-columns:1fr;}
  .project-visual,.project-card:nth-child(even) .project-visual{order:0;border:none;border-bottom:1px solid var(--border);}
  .project-body{padding:28px;}
}

/* ============================================================
   JOURNEY
============================================================ */
.timeline{position:relative;max-width:760px;margin-inline:auto;}
.timeline-track{
  position:absolute;left:50%;top:0;bottom:0;width:2px;background:var(--border);
  transform:translateX(-50%);
}
.timeline-fill{
  position:absolute;left:0;top:0;width:100%;height:0%;
  background:linear-gradient(var(--signal),var(--ember));
  transition:height .1s linear;
}
.tnode{
  position:relative;width:50%;padding:0 44px 64px;
}
.tnode:nth-child(odd){left:0;text-align:right;}
.tnode:nth-child(even){left:50%;text-align:left;}
.tnode:last-child{padding-bottom:0;}
.tnode .dot{
  position:absolute;top:2px;width:14px;height:14px;border-radius:50%;
  background:var(--void);border:2px solid var(--mist-dim);transition:border-color .4s,box-shadow .4s,background .4s;
}
.tnode:nth-child(odd) .dot{right:-7px;}
.tnode:nth-child(even) .dot{left:-7px;}
.tnode.is-visible .dot{border-color:var(--signal);background:var(--signal);box-shadow:0 0 16px var(--signal-soft);}
.tnode h3{font-size:1.1rem;margin-bottom:6px;}
.tnode .tlabel{font-family:var(--font-mono);font-size:.72rem;color:var(--mist-dim);text-transform:uppercase;letter-spacing:.08em;}

@media (max-width:700px){
  .timeline-track{left:6px;}
  .timeline-fill{left:0;}
  .tnode,.tnode:nth-child(odd),.tnode:nth-child(even){
    width:100%;left:0;text-align:left;padding-left:34px;padding-right:0;
  }
  .tnode:nth-child(odd) .dot,.tnode:nth-child(even) .dot{left:0;right:auto;}
}

/* ============================================================
   ACHIEVEMENTS
============================================================ */
.ach-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:20px;}
.ach-card{padding:30px 24px;text-align:left;}
.ach-card .icon-box{
  width:44px;height:44px;border-radius:12px;background:rgba(255,0,60,.08);
  border:1px solid rgba(255,0,60,.18);display:flex;align-items:center;justify-content:center;margin-bottom:18px;
}
.ach-card svg{width:20px;height:20px;color:var(--signal);}
.ach-card h3{font-size:1rem;margin-bottom:6px;line-height:1.4;}
.ach-card p{color:var(--mist);font-size:.85rem;}

@media (max-width:900px){.ach-grid{grid-template-columns:repeat(2,1fr);}}
@media (max-width:520px){.ach-grid{grid-template-columns:1fr;}}

/* ============================================================
   STACK
============================================================ */
.stack-groups{display:flex;flex-direction:column;gap:30px;}
.stack-group-label{
  font-family:var(--font-mono);font-size:.78rem;color:var(--mist-dim);
  text-transform:uppercase;letter-spacing:.1em;width:160px;flex-shrink:0;
}
.stack-row{display:flex;gap:28px;align-items:flex-start;padding-block:18px;border-bottom:1px solid var(--border);}
.stack-row:last-child{border-bottom:none;}
.chip-row{display:flex;flex-wrap:wrap;gap:10px;flex:1;}
.chip{
  font-family:var(--font-mono);font-size:.82rem;color:var(--bone);
  border:1px solid var(--border);padding:8px 16px;border-radius:999px;
  background:var(--glass);transition:border-color .3s,transform .3s,background .3s;
}
.chip:hover{border-color:var(--border-hover);background:var(--glass-hover);transform:translateY(-2px);}

@media (max-width:640px){
  .stack-row{flex-direction:column;gap:10px;}
  .stack-group-label{width:auto;}
}

/* ============================================================
   VISION
============================================================ */
#vision{text-align:center;position:relative;}
.vision-glow{
  position:absolute;top:50%;left:50%;width:600px;height:600px;
  background:radial-gradient(circle,rgba(255,0,60,.14),transparent 70%);
  transform:translate(-50%,-50%);z-index:0;pointer-events:none;
}
.vision-text{
  position:relative;z-index:1;font-family:var(--font-display);font-weight:500;
  font-size:clamp(1.4rem,3.4vw,2.3rem);line-height:1.45;max-width:880px;margin-inline:auto;color:var(--bone);
}
.vision-text .accent{color:var(--signal);}

/* ============================================================
   CONTACT
============================================================ */
#contact{text-align:center;}
.contact-status{
  display:inline-flex;align-items:center;gap:8px;font-family:var(--font-mono);font-size:.8rem;
  color:var(--mist);border:1px solid var(--border);padding:8px 16px;border-radius:999px;margin-bottom:30px;
}
.contact-status .dot{width:7px;height:7px;border-radius:50%;background:var(--signal);box-shadow:0 0 10px var(--signal);animation:blink 1.6s ease-in-out infinite;}
html.reduced-motion .contact-status .dot{animation:none;}
.contact-heading{font-size:clamp(2rem,5.5vw,3.6rem);max-width:820px;margin-inline:auto 32px;margin-bottom:32px;}
#contact .btn-row{justify-content:center;}

/* ============================================================
   FOOTER
============================================================ */
footer{
  border-top:1px solid var(--border);padding-block:36px;
  display:flex;flex-wrap:wrap;gap:16px;align-items:center;justify-content:space-between;
}
footer .container{display:flex;flex-wrap:wrap;gap:16px;align-items:center;justify-content:space-between;width:100%;}
footer p{font-family:var(--font-mono);font-size:.78rem;color:var(--mist-dim);}
.back-top{font-family:var(--font-mono);font-size:.78rem;color:var(--mist);display:inline-flex;align-items:center;gap:6px;transition:color .3s;}
.back-top:hover{color:var(--signal);}
.back-top svg{width:13px;height:13px;}
</style>
</head>
<body>

<a href="#main" class="skip-link">Skip to content</a>
<canvas id="bg-particles"></canvas>
<div class="grain"></div>
<div class="cursor-glow" id="cursorGlow"></div>

<header class="nav" id="nav">
  <div class="container">
    <a href="#hero" class="logo">S<span>/</span>M</a>
    <nav class="nav-links" aria-label="Section navigation">
      <a href="#about">About</a>
      <a href="#expertise">Expertise</a>
      <a href="#work">Work</a>
      <a href="#journey">Journey</a>
      <a href="#stack">Stack</a>
      <a href="#contact">Contact</a>
    </nav>
    <div class="nav-actions">
      <a class="nav-cta" href="resume.pdf" download>
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M12 3v12m0 0l-4-4m4 4l4-4M5 21h14"/></svg>
        <span class="label">Resume</span>
      </a>
      <button class="nav-toggle" id="navToggle" aria-label="Open menu" aria-expanded="false">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M4 6h16M4 12h16M4 18h16"/></svg>
      </button>
    </div>
  </div>
</header>

<div class="mobile-panel" id="mobilePanel">
  <a href="#about">About</a>
  <a href="#expertise">Expertise</a>
  <a href="#work">Work</a>
  <a href="#journey">Journey</a>
  <a href="#stack">Stack</a>
  <a href="#contact">Contact</a>
</div>

<main id="main">

  <!-- ===================== HERO ===================== -->
  <section id="hero">
    <canvas id="neural-canvas"></canvas>
    <div class="container hero-inner">
      <p class="hero-kicker">$ whoami<span class="blink">_</span></p>
      <h1 class="hero-name">SANJEEVIKUMAR M</h1>
      <p class="hero-headline">Building Intelligent Systems with AI, IoT &amp; Embedded Engineering</p>
      <p class="hero-roles">$ <span id="typewriter"></span><span class="cursor"></span></p>
      <p class="hero-desc">I design and build intelligent systems that connect Artificial Intelligence, Embedded Hardware, IoT Devices, Cloud Infrastructure, and Modern Web Applications to solve real-world challenges.</p>

      <div class="btn-row">
        <a href="#work" class="btn btn-primary">
          Explore Projects
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M5 12h14m-6-6l6 6-6 6"/></svg>
        </a>
        <a href="https://github.com/your-username" target="_blank" rel="noopener" class="btn btn-outline">
          <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 .5C5.73.5.98 5.24.98 11.5c0 4.86 3.16 8.98 7.54 10.43.55.1.75-.24.75-.53 0-.26-.01-1.13-.02-2.05-3.07.67-3.72-1.31-3.72-1.31-.5-1.28-1.23-1.62-1.23-1.62-1-.69.08-.67.08-.67 1.1.08 1.68 1.14 1.68 1.14.98 1.68 2.58 1.2 3.21.91.1-.71.38-1.2.69-1.47-2.45-.28-5.02-1.23-5.02-5.47 0-1.21.43-2.2 1.14-2.98-.11-.28-.5-1.42.11-2.96 0 0 .94-.3 3.07 1.14a10.6 10.6 0 0 1 5.59 0c2.13-1.44 3.07-1.14 3.07-1.14.61 1.54.22 2.68.11 2.96.71.78 1.14 1.77 1.14 2.98 0 4.25-2.58 5.19-5.04 5.46.39.34.74 1.02.74 2.05 0 1.48-.01 2.67-.01 3.03 0 .29.2.64.76.53C19.86 20.47 23 16.36 23 11.5 23 5.24 18.27.5 12 .5Z"/></svg>
          View GitHub
        </a>
        <a href="https://linkedin.com/in/your-username" target="_blank" rel="noopener" class="btn btn-outline">
          <svg viewBox="0 0 24 24" fill="currentColor"><path d="M4.98 3.5a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5ZM3 9h4v12H3zM9.5 9H13v1.7h.05c.5-.9 1.7-1.85 3.5-1.85 3.75 0 4.45 2.47 4.45 5.67V21h-4v-5.9c0-1.4-.03-3.2-1.95-3.2-1.95 0-2.25 1.52-2.25 3.1V21h-4z"/></svg>
          LinkedIn
        </a>
        <a href="resume.pdf" download class="btn btn-outline">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M12 3v12m0 0l-4-4m4 4l4-4M5 21h14"/></svg>
          Download Resume
        </a>
      </div>

      <div class="float-tags" id="floatTags">
        <span class="float-tag">Python</span>
        <span class="float-tag">FastAPI</span>
        <span class="float-tag">TensorFlow</span>
        <span class="float-tag">ESP32</span>
        <span class="float-tag">React</span>
        <span class="float-tag">Machine Learning</span>
        <span class="float-tag">Computer Vision</span>
        <span class="float-tag">IoT</span>
        <span class="float-tag">Embedded Systems</span>
      </div>
    </div>
    <div class="scroll-cue"><span>SCROLL</span><span class="line"></span></div>
  </section>

  <!-- ===================== ABOUT ===================== -->
  <section id="about">
    <div class="container">
      <p class="eyebrow reveal">$ cat about.md</p>
      <div class="about-grid">
        <div>
          <h2 class="section-title reveal">Engineering the Future</h2>
          <p class="reveal">I am an AI &amp; Data Science Engineer passionate about creating intelligent solutions that bridge the gap between software and hardware.</p>
          <p class="reveal" style="margin-top:16px;">My work spans:</p>
          <ul class="about-list reveal-group">
            <li class="reveal">Artificial Intelligence</li>
            <li class="reveal">Machine Learning</li>
            <li class="reveal">Computer Vision</li>
            <li class="reveal">Full Stack Development</li>
            <li class="reveal">IoT Systems</li>
            <li class="reveal">Embedded Engineering</li>
            <li class="reveal">Cloud Technologies</li>
          </ul>
          <p class="pull reveal">Focus on innovation, scalability, and real-world impact.</p>
        </div>
        <div class="orbit-wrap reveal">
          <div class="orbit">
            <svg viewBox="0 0 200 200">
              <g class="orbit-ring">
                <circle cx="100" cy="100" r="92" fill="none" stroke="rgba(255,0,60,.25)" stroke-width="1"/>
                <circle cx="100" cy="8" r="4" fill="#ff003c"/>
              </g>
              <g class="orbit-ring rev">
                <circle cx="100" cy="100" r="64" fill="none" stroke="rgba(255,255,255,.12)" stroke-width="1"/>
                <circle cx="164" cy="100" r="3" fill="#f3f2f0"/>
              </g>
              <circle cx="100" cy="100" r="34" fill="none" stroke="rgba(255,0,60,.45)" stroke-width="1.4"/>
              <circle cx="100" cy="100" r="5" fill="#ff003c"/>
            </svg>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ===================== EXPERTISE ===================== -->
  <section id="expertise">
    <div class="container">
      <p class="eyebrow reveal">$ ls expertise/</p>
      <div class="section-head">
        <h2 class="section-title reveal">Core Expertise</h2>
        <p class="reveal">Six disciplines, one system: where intelligence meets infrastructure.</p>
      </div>
      <div class="expertise-grid reveal-group">

        <div class="glass expertise-card reveal">
          <div class="icon-box"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><rect x="7" y="7" width="10" height="10" rx="1.5"/><path d="M9 2v3M15 2v3M9 19v3M15 19v3M2 9h3M2 15h3M19 9h3M19 15h3"/></svg></div>
          <h3>Artificial Intelligence</h3>
          <p>Build predictive models, intelligent agents, and AI-powered applications.</p>
        </div>

        <div class="glass expertise-card reveal">
          <div class="icon-box"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><circle cx="5" cy="18" r="1.8"/><circle cx="11" cy="11" r="1.8"/><circle cx="17" cy="14" r="1.8"/><circle cx="20" cy="6" r="1.8"/><path d="M6.5 16.8L9.5 12.4M12.5 12L15.5 13.5M18.3 12.6L19 7.8"/></svg></div>
          <h3>Machine Learning</h3>
          <p>Data-driven systems that learn and adapt.</p>
        </div>

        <div class="glass expertise-card reveal">
          <div class="icon-box"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M2 12c2.5-5 7-7 10-7s7.5 2 10 7c-2.5 5-7 7-10 7s-7.5-2-10-7Z"/><circle cx="12" cy="12" r="3"/></svg></div>
          <h3>Computer Vision</h3>
          <p>Object detection, image understanding, and visual intelligence.</p>
        </div>

        <div class="glass expertise-card reveal">
          <div class="icon-box"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M8 17l-5-5 5-5M16 7l5 5-5 5M13 4l-3 16"/></svg></div>
          <h3>Full Stack Development</h3>
          <p>Scalable web platforms using React, FastAPI, and modern technologies.</p>
        </div>

        <div class="glass expertise-card reveal">
          <div class="icon-box"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><circle cx="12" cy="12" r="2"/><path d="M12 2a10 10 0 0 1 7.07 17.07M12 6a8 8 0 0 1 5.66 13.66M12 2A10 10 0 0 0 4.93 19.07M12 6a8 8 0 0 0-5.66 13.66"/></svg></div>
          <h3>IoT Systems</h3>
          <p>Connected devices, sensors, and intelligent automation.</p>
        </div>

        <div class="glass expertise-card reveal">
          <div class="icon-box"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><rect x="6" y="6" width="12" height="12" rx="1.5"/><path d="M9 1v3M15 1v3M9 20v3M15 20v3M1 9h3M1 15h3M20 9h3M20 15h3"/><circle cx="12" cy="12" r="2.5"/></svg></div>
          <h3>Embedded Engineering</h3>
          <p>ESP32, Raspberry Pi, STM32, and hardware-software integration.</p>
        </div>

      </div>
    </div>
  </section>

  <!-- ===================== WORK ===================== -->
  <section id="work">
    <div class="container">
      <p class="eyebrow reveal">$ git log --projects</p>
      <div class="section-head">
        <h2 class="section-title reveal">Featured Work</h2>
        <p class="reveal">Systems built end-to-end — from sensor to satellite to screen.</p>
      </div>

      <div class="project-list reveal-group">

        <article class="glass project-card reveal">
          <div class="project-visual">
            <svg viewBox="0 0 300 220">
              <defs><linearGradient id="g1" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#ff003c" stop-opacity=".7"/><stop offset="1" stop-color="#ff003c" stop-opacity="0"/></linearGradient></defs>
              <rect x="20" y="20" width="260" height="180" rx="10" fill="none" stroke="rgba(255,255,255,.15)"/>
              <g stroke="rgba(255,0,60,.45)" stroke-width="1">
                <line x1="20" y1="60" x2="280" y2="60"/><line x1="20" y1="100" x2="280" y2="100"/><line x1="20" y1="140" x2="280" y2="140"/><line x1="20" y1="180" x2="280" y2="180"/>
                <line x1="80" y1="20" x2="80" y2="200"/><line x1="150" y1="20" x2="150" y2="200"/><line x1="220" y1="20" x2="220" y2="200"/>
              </g>
              <circle cx="150" cy="100" r="38" fill="url(#g1)"/>
              <circle cx="150" cy="100" r="38" fill="none" stroke="#ff003c" stroke-width="1.6"/>
              <circle cx="150" cy="100" r="4" fill="#ff003c"/>
            </svg>
          </div>
          <div class="project-body">
            <span class="project-index">01 — Environmental Intelligence</span>
            <h3>Methane Shadow Hunter</h3>
            <p>An AI-powered environmental intelligence platform that detects methane super-emitters from satellite imagery, estimates emissions, and generates compliance reports.</p>
            <div class="project-tags">
              <span>FastAPI</span><span>React</span><span>Google Earth Engine</span><span>Machine Learning</span><span>GIS</span>
            </div>
            <a href="#" class="project-link">View Project <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M7 17L17 7M9 7h8v8"/></svg></a>
          </div>
        </article>

        <article class="glass project-card reveal">
          <div class="project-visual">
            <svg viewBox="0 0 300 220">
              <circle cx="80" cy="110" r="6" fill="#ff003c"/><circle cx="150" cy="60" r="6" fill="#ff003c"/><circle cx="220" cy="110" r="6" fill="#ff003c"/><circle cx="150" cy="160" r="6" fill="#ff003c"/>
              <g stroke="rgba(255,0,60,.4)" stroke-width="1.4">
                <line x1="80" y1="110" x2="150" y2="60"/><line x1="150" y1="60" x2="220" y2="110"/>
                <line x1="220" y1="110" x2="150" y2="160"/><line x1="150" y1="160" x2="80" y2="110"/>
                <line x1="80" y1="110" x2="220" y2="110"/>
              </g>
              <circle cx="150" cy="110" r="3" fill="#fff"><animate attributeName="r" values="3;7;3" dur="2s" repeatCount="indefinite"/></circle>
            </svg>
          </div>
          <div class="project-body">
            <span class="project-index">02 — Smart City</span>
            <h3>Smart Waste Management System</h3>
            <p>IoT-enabled smart city solution for real-time waste monitoring, predictive collection scheduling, and route optimization.</p>
            <div class="project-tags">
              <span>ESP32</span><span>IoT</span><span>Flask</span><span>MySQL</span><span>Analytics</span>
            </div>
            <a href="#" class="project-link">View Project <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M7 17L17 7M9 7h8v8"/></svg></a>
          </div>
        </article>

        <article class="glass project-card reveal">
          <div class="project-visual">
            <svg viewBox="0 0 300 220">
              <path d="M30 170 C 90 60, 210 60, 270 170" fill="none" stroke="rgba(255,0,60,.5)" stroke-width="2"/>
              <circle cx="30" cy="170" r="6" fill="#ff003c"/><circle cx="270" cy="170" r="6" fill="#ff003c"/>
              <circle cx="150" cy="70" r="5" fill="#fff"/>
              <path d="M30 170 C 90 60, 210 60, 270 170" fill="none" stroke="#fff" stroke-width="1" stroke-dasharray="4 6" opacity=".5"/>
            </svg>
          </div>
          <div class="project-body">
            <span class="project-index">03 — AgriTech</span>
            <h3>AgroLink</h3>
            <p>AI-powered farmer-to-consumer marketplace improving agricultural supply chain efficiency.</p>
            <div class="project-tags">
              <span>AI</span><span>Web Development</span><span>Database Systems</span>
            </div>
            <a href="#" class="project-link">View Project <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M7 17L17 7M9 7h8v8"/></svg></a>
          </div>
        </article>

        <article class="glass project-card reveal">
          <div class="project-visual">
            <svg viewBox="0 0 300 220">
              <polyline points="20,110 60,110 75,60 95,160 115,90 135,130 155,110 300,110" fill="none" stroke="#ff003c" stroke-width="1.8"/>
              <line x1="20" y1="110" x2="300" y2="110" stroke="rgba(255,255,255,.15)" stroke-width="1"/>
            </svg>
          </div>
          <div class="project-body">
            <span class="project-index">04 — Environmental Monitoring</span>
            <h3>IoT Weather Monitoring Station</h3>
            <p>Real-time environmental monitoring platform using sensor networks and cloud dashboards.</p>
            <div class="project-tags">
              <span>ESP8266</span><span>IoT</span><span>Cloud Integration</span>
            </div>
            <a href="#" class="project-link">View Project <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M7 17L17 7M9 7h8v8"/></svg></a>
          </div>
        </article>

      </div>
    </div>
  </section>

  <!-- ===================== JOURNEY ===================== -->
  <section id="journey">
    <div class="container">
      <p class="eyebrow reveal">$ git log --reverse --oneline</p>
      <div class="section-head" style="margin-inline:auto;text-align:center;">
        <h2 class="section-title reveal">The Journey</h2>
      </div>
      <div class="timeline" id="timeline">
        <div class="timeline-track"><div class="timeline-fill" id="timelineFill"></div></div>

        <div class="tnode reveal" data-tnode>
          <span class="tlabel">Origin</span>
          <h3>Student Engineer</h3>
          <span class="dot"></span>
        </div>
        <div class="tnode reveal" data-tnode>
          <span class="tlabel">Foundation</span>
          <h3>AI &amp; Data Science Learner</h3>
          <span class="dot"></span>
        </div>
        <div class="tnode reveal" data-tnode>
          <span class="tlabel">Competition</span>
          <h3>Hackathon Competitor</h3>
          <span class="dot"></span>
        </div>
        <div class="tnode reveal" data-tnode>
          <span class="tlabel">Execution</span>
          <h3>Systems Builder</h3>
          <span class="dot"></span>
        </div>
        <div class="tnode reveal" data-tnode>
          <span class="tlabel">Present</span>
          <h3>AI Engineer</h3>
          <span class="dot"></span>
        </div>
      </div>
    </div>
  </section>

  <!-- ===================== ACHIEVEMENTS ===================== -->
  <section id="achievements">
    <div class="container">
      <p class="eyebrow reveal">$ cat achievements.log</p>
      <div class="section-head">
        <h2 class="section-title reveal">Milestones</h2>
      </div>
      <div class="ach-grid reveal-group">
        <div class="glass ach-card reveal">
          <div class="icon-box"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M8 4h8v4a4 4 0 0 1-8 0V4Z"/><path d="M8 6H5a3 3 0 0 0 3 4M16 6h3a3 3 0 0 1-3 4"/><path d="M10 14h4l1 6H9l1-6Z"/></svg></div>
          <h3>TEXPERIA Hackathon</h3>
          <p>2nd Prize Winner</p>
        </div>
        <div class="glass ach-card reveal">
          <div class="icon-box"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><circle cx="12" cy="8" r="5"/><path d="M9 12.5L7 21l5-3 5 3-2-8.5"/></svg></div>
          <h3>ZYPH Global Summit Hackathon</h3>
          <p>Top 10 Finalist</p>
        </div>
        <div class="glass ach-card reveal">
          <div class="icon-box"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M12 2c2 2 3 5 3 8 0 2-1 3-1 3h-4s-1-1-1-3c0-3 1-6 3-8Z"/><path d="M9 13l-3 3 1 4 4-3M15 13l3 3-1 4-4-3"/><circle cx="12" cy="9" r="1.4"/></svg></div>
          <h3>AI &amp; Full Stack Internships</h3>
          <p>Multiple roles across product teams</p>
        </div>
        <div class="glass ach-card reveal">
          <div class="icon-box"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M9 18h6M10 22h4M12 2a6 6 0 0 0-3 11c.6.4 1 1 1 1.7V16h4v-1.3c0-.7.4-1.3 1-1.7A6 6 0 0 0 12 2Z"/></svg></div>
          <h3>Open Source Contributor</h3>
          <p>Building in public, shipping in the open</p>
        </div>
      </div>
    </div>
  </section>

  <!-- ===================== STACK ===================== -->
  <section id="stack">
    <div class="container">
      <p class="eyebrow reveal">$ pip list --stack</p>
      <div class="section-head">
        <h2 class="section-title reveal">Tech Stack</h2>
      </div>
      <div class="stack-groups reveal-group">

        <div class="stack-row reveal">
          <span class="stack-group-label">Languages</span>
          <div class="chip-row">
            <span class="chip">Python</span><span class="chip">Java</span><span class="chip">JavaScript</span><span class="chip">C</span><span class="chip">C++</span>
          </div>
        </div>

        <div class="stack-row reveal">
          <span class="stack-group-label">AI</span>
          <div class="chip-row">
            <span class="chip">TensorFlow</span><span class="chip">Scikit-Learn</span><span class="chip">Pandas</span><span class="chip">NumPy</span>
          </div>
        </div>

        <div class="stack-row reveal">
          <span class="stack-group-label">Backend</span>
          <div class="chip-row">
            <span class="chip">FastAPI</span><span class="chip">Flask</span>
          </div>
        </div>

        <div class="stack-row reveal">
          <span class="stack-group-label">Frontend</span>
          <div class="chip-row">
            <span class="chip">React</span><span class="chip">HTML</span><span class="chip">CSS</span>
          </div>
        </div>

        <div class="stack-row reveal">
          <span class="stack-group-label">Database</span>
          <div class="chip-row">
            <span class="chip">MySQL</span><span class="chip">MongoDB</span><span class="chip">Supabase</span>
          </div>
        </div>

        <div class="stack-row reveal">
          <span class="stack-group-label">Embedded</span>
          <div class="chip-row">
            <span class="chip">ESP32</span><span class="chip">ESP8266</span><span class="chip">STM32</span><span class="chip">Arduino</span><span class="chip">Raspberry Pi</span>
          </div>
        </div>

        <div class="stack-row reveal">
          <span class="stack-group-label">Tools</span>
          <div class="chip-row">
            <span class="chip">Git</span><span class="chip">GitHub</span><span class="chip">Linux</span><span class="chip">Docker</span><span class="chip">VS Code</span>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- ===================== VISION ===================== -->
  <section id="vision">
    <div class="vision-glow"></div>
    <div class="container">
      <p class="eyebrow reveal" style="justify-content:center;">$ cat vision.md</p>
      <h2 class="section-title reveal" style="margin-bottom:24px;">My Vision</h2>
      <p class="vision-text reveal">To build <span class="accent">intelligent technologies</span> that make industries smarter, cities more sustainable, and everyday life more connected through the power of <span class="accent">Artificial Intelligence</span> and <span class="accent">Embedded Systems</span>.</p>
    </div>
  </section>

  <!-- ===================== CONTACT ===================== -->
  <section id="contact">
    <div class="container">
      <span class="contact-status reveal"><span class="dot"></span> Open to opportunities</span>
      <h2 class="contact-heading reveal">Let's Build Something Intelligent Together</h2>
      <div class="btn-row reveal">
        <a href="https://github.com/your-username" target="_blank" rel="noopener" class="btn btn-outline">
          <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 .5C5.73.5.98 5.24.98 11.5c0 4.86 3.16 8.98 7.54 10.43.55.1.75-.24.75-.53 0-.26-.01-1.13-.02-2.05-3.07.67-3.72-1.31-3.72-1.31-.5-1.28-1.23-1.62-1.23-1.62-1-.69.08-.67.08-.67 1.1.08 1.68 1.14 1.68 1.14.98 1.68 2.58 1.2 3.21.91.1-.71.38-1.2.69-1.47-2.45-.28-5.02-1.23-5.02-5.47 0-1.21.43-2.2 1.14-2.98-.11-.28-.5-1.42.11-2.96 0 0 .94-.3 3.07 1.14a10.6 10.6 0 0 1 5.59 0c2.13-1.44 3.07-1.14 3.07-1.14.61 1.54.22 2.68.11 2.96.71.78 1.14 1.77 1.14 2.98 0 4.25-2.58 5.19-5.04 5.46.39.34.74 1.02.74 2.05 0 1.48-.01 2.67-.01 3.03 0 .29.2.64.76.53C19.86 20.47 23 16.36 23 11.5 23 5.24 18.27.5 12 .5Z"/></svg>
          GitHub
        </a>
        <a href="https://linkedin.com/in/your-username" target="_blank" rel="noopener" class="btn btn-outline">
          <svg viewBox="0 0 24 24" fill="currentColor"><path d="M4.98 3.5a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5ZM3 9h4v12H3zM9.5 9H13v1.7h.05c.5-.9 1.7-1.85 3.5-1.85 3.75 0 4.45 2.47 4.45 5.67V21h-4v-5.9c0-1.4-.03-3.2-1.95-3.2-1.95 0-2.25 1.52-2.25 3.1V21h-4z"/></svg>
          LinkedIn
        </a>
        <a href="mailto:your.email@example.com" class="btn btn-primary">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M3 6h18v12H3z"/><path d="M3 7l9 6 9-6"/></svg>
          Email
        </a>
      </div>
    </div>
  </section>

</main>

<footer>
  <div class="container">
    <p>© <span id="year"></span> Sanjeevikumar M — Building the future through AI, Engineering, and Innovation.</p>
    <a href="#hero" class="back-top">Back to top <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M12 19V5M5 12l7-7 7 7"/></svg></a>
  </div>
</footer>

<script>
(function(){
  "use strict";
  var reduced = window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  if(reduced){ document.documentElement.classList.add('reduced-motion'); }

  /* ---------- year ---------- */
  document.getElementById('year').textContent = new Date().getFullYear();

  /* ---------- nav scroll state ---------- */
  var nav = document.getElementById('nav');
  function onScroll(){
    if(window.scrollY > 30){ nav.classList.add('scrolled'); } else { nav.classList.remove('scrolled'); }
  }
  document.addEventListener('scroll', onScroll, {passive:true});
  onScroll();

  /* ---------- mobile menu ---------- */
  var toggle = document.getElementById('navToggle');
  var panel = document.getElementById('mobilePanel');
  toggle.addEventListener('click', function(){
    var open = panel.classList.toggle('open');
    toggle.setAttribute('aria-expanded', open ? 'true' : 'false');
  });
  panel.querySelectorAll('a').forEach(function(a){
    a.addEventListener('click', function(){ panel.classList.remove('open'); toggle.setAttribute('aria-expanded','false'); });
  });

  /* ---------- cursor glow ---------- */
  var glow = document.getElementById('cursorGlow');
  if(!reduced && matchMedia('(hover:hover)').matches){
    var gx=0, gy=0, cx=0, cy=0;
    window.addEventListener('mousemove', function(e){ gx=e.clientX; gy=e.clientY; });
    function glowLoop(){
      cx += (gx-cx)*0.12; cy += (gy-cy)*0.12;
      glow.style.transform = 'translate('+cx+'px,'+cy+'px) translate(-50%,-50%)';
      requestAnimationFrame(glowLoop);
    }
    glowLoop();
  } else {
    glow.style.display = 'none';
  }

  /* ---------- scroll reveal ---------- */
  document.querySelectorAll('.reveal-group').forEach(function(group){
    var kids = group.querySelectorAll(':scope > .reveal');
    kids.forEach(function(el, i){ el.style.transitionDelay = Math.min(i*70,560)+'ms'; });
  });
  if('IntersectionObserver' in window){
    var io = new IntersectionObserver(function(entries){
      entries.forEach(function(entry){
        if(entry.isIntersecting){
          entry.target.classList.add('is-visible');
          io.unobserve(entry.target);
        }
      });
    }, {threshold:0.15, rootMargin:'0px 0px -40px 0px'});
    document.querySelectorAll('.reveal').forEach(function(el){ io.observe(el); });
  } else {
    document.querySelectorAll('.reveal').forEach(function(el){ el.classList.add('is-visible'); });
  }

  /* ---------- floating tag stagger ---------- */
  document.querySelectorAll('.float-tag').forEach(function(tag, i){
    tag.style.animationDelay = (i*0.3)+'s';
    tag.style.animationDuration = (3.4 + (i%3)*0.6)+'s';
  });

  /* ---------- typewriter ---------- */
  var roles = ['AI Engineer','Full Stack Developer','Systems Builder'];
  var twEl = document.getElementById('typewriter');
  if(reduced){
    twEl.textContent = roles.join(' • ');
  } else {
    var ri=0, ci=0, deleting=false;
    function tick(){
      var word = roles[ri];
      if(!deleting){
        ci++; twEl.textContent = word.slice(0,ci);
        if(ci === word.length){ deleting = true; setTimeout(tick, 1700); return; }
        setTimeout(tick, 65 + Math.random()*40);
      } else {
        ci--; twEl.textContent = word.slice(0,ci);
        if(ci === 0){ deleting = false; ri = (ri+1) % roles.length; setTimeout(tick, 300); return; }
        setTimeout(tick, 32);
      }
    }
    tick();
  }

  /* ---------- timeline fill ---------- */
  var timeline = document.getElementById('timeline');
  var fill = document.getElementById('timelineFill');
  var tnodes = document.querySelectorAll('[data-tnode]');
  function updateTimeline(){
    var rect = timeline.getBoundingClientRect();
    var vh = window.innerHeight;
    var total = rect.height;
    var visible = vh*0.5 - rect.top;
    var progress = Math.max(0, Math.min(1, visible/total));
    fill.style.height = (progress*100)+'%';
    var thresholdPx = progress*total;
    tnodes.forEach(function(node){
      var topWithin = node.offsetTop;
      if(thresholdPx >= topWithin + 10){ node.classList.add('is-visible'); }
    });
  }
  var ticking=false;
  document.addEventListener('scroll', function(){
    if(!ticking){ ticking=true; requestAnimationFrame(function(){ updateTimeline(); ticking=false; }); }
  }, {passive:true});
  window.addEventListener('resize', updateTimeline);
  updateTimeline();

  /* ---------- ambient background particles (global, fixed) ---------- */
  var bgCanvas = document.getElementById('bg-particles');
  var bgCtx = bgCanvas.getContext('2d');
  var bgParticles = [];
  function sizeBg(){
    bgCanvas.width = window.innerWidth * Math.min(devicePixelRatio||1, 2);
    bgCanvas.height = window.innerHeight * Math.min(devicePixelRatio||1, 2);
    bgCanvas.style.width = window.innerWidth+'px';
    bgCanvas.style.height = window.innerHeight+'px';
  }
  function initBg(){
    sizeBg();
    var count = Math.min(46, Math.floor((window.innerWidth*window.innerHeight)/34000));
    bgParticles = [];
    for(var i=0;i<count;i++){
      bgParticles.push({
        x: Math.random()*bgCanvas.width,
        y: Math.random()*bgCanvas.height,
        vx: (Math.random()-0.5)*0.15,
        vy: (Math.random()-0.5)*0.15,
        r: Math.random()*1.4+0.4
      });
    }
  }
  function drawBg(){
    bgCtx.clearRect(0,0,bgCanvas.width,bgCanvas.height);
    bgCtx.fillStyle = 'rgba(255,255,255,0.5)';
    for(var i=0;i<bgParticles.length;i++){
      var p = bgParticles[i];
      p.x += p.vx; p.y += p.vy;
      if(p.x<0) p.x=bgCanvas.width; if(p.x>bgCanvas.width) p.x=0;
      if(p.y<0) p.y=bgCanvas.height; if(p.y>bgCanvas.height) p.y=0;
      bgCtx.globalAlpha = 0.22;
      bgCtx.beginPath();
      bgCtx.arc(p.x,p.y,p.r*2,0,Math.PI*2);
      bgCtx.fill();
    }
    bgCtx.globalAlpha = 1;
  }
  var bgVisible = true;
  document.addEventListener('visibilitychange', function(){ bgVisible = !document.hidden; });
  function bgLoop(){
    if(!reduced && bgVisible){ drawBg(); }
    requestAnimationFrame(bgLoop);
  }
  initBg();
  window.addEventListener('resize', initBg);
  if(!reduced){ bgLoop(); } else { drawBg(); }

  /* ---------- hero neural network canvas ---------- */
  var hero = document.getElementById('hero');
  var nCanvas = document.getElementById('neural-canvas');
  var nCtx = nCanvas.getContext('2d');
  var nodes = [], pulses = [];
  var mouse = {x:-9999, y:-9999};
  var DPR = Math.min(devicePixelRatio||1, 2);

  function sizeHero(){
    var w = hero.offsetWidth, h = hero.offsetHeight;
    nCanvas.width = w*DPR; nCanvas.height = h*DPR;
    nCanvas.style.width = w+'px'; nCanvas.style.height = h+'px';
  }
  function initNeural(){
    sizeHero();
    var w = nCanvas.width, h = nCanvas.height;
    var count = Math.min(64, Math.floor((w*h)/55000));
    nodes = [];
    for(var i=0;i<count;i++){
      nodes.push({
        x: Math.random()*w, y: Math.random()*h,
        vx:(Math.random()-0.5)*0.35, vy:(Math.random()-0.5)*0.35
      });
    }
    pulses = [];
  }
  function maybeSpawnPulse(){
    if(pulses.length > 6) return;
    if(Math.random() > 0.04) return;
    var a = nodes[Math.floor(Math.random()*nodes.length)];
    var best=null, bestD=99999;
    for(var i=0;i<nodes.length;i++){
      var b = nodes[i]; if(b===a) continue;
      var d = Math.hypot(a.x-b.x, a.y-b.y);
      if(d < 160*DPR && d < bestD){ bestD=d; best=b; }
    }
    if(best){ pulses.push({a:a,b:best,t:0}); }
  }
  function drawNeural(){
    var w = nCanvas.width, h = nCanvas.height;
    nCtx.clearRect(0,0,w,h);
    var linkDist = 150*DPR;

    for(var i=0;i<nodes.length;i++){
      var n = nodes[i];
      n.x += n.vx; n.y += n.vy;
      var dxm = n.x-mouse.x, dym = n.y-mouse.y;
      var dm = Math.hypot(dxm,dym);
      if(dm < 110*DPR){
        var f = (110*DPR-dm)/(110*DPR)*0.04;
        n.vx += (dxm/dm)*f; n.vy += (dym/dm)*f;
      }
      n.vx *= 0.98; n.vy *= 0.98;
      if(n.x<0||n.x>w) n.vx*=-1;
      if(n.y<0||n.y>h) n.vy*=-1;
      n.x = Math.max(0,Math.min(w,n.x));
      n.y = Math.max(0,Math.min(h,n.y));
    }

    for(var i=0;i<nodes.length;i++){
      for(var j=i+1;j<nodes.length;j++){
        var a=nodes[i], b=nodes[j];
        var d = Math.hypot(a.x-b.x, a.y-b.y);
        if(d < linkDist){
          var alpha = (1-d/linkDist)*0.35;
          nCtx.strokeStyle = 'rgba(255,0,60,'+alpha+')';
          nCtx.lineWidth = 1*DPR;
          nCtx.beginPath(); nCtx.moveTo(a.x,a.y); nCtx.lineTo(b.x,b.y); nCtx.stroke();
        }
      }
    }

    nCtx.fillStyle = 'rgba(255,40,80,0.85)';
    for(var i=0;i<nodes.length;i++){
      var n = nodes[i];
      nCtx.beginPath(); nCtx.arc(n.x,n.y,1.6*DPR,0,Math.PI*2); nCtx.fill();
    }

    maybeSpawnPulse();
    for(var p=pulses.length-1;p>=0;p--){
      var pu = pulses[p];
      pu.t += 0.018;
      if(pu.t >= 1){ pulses.splice(p,1); continue; }
      var px = pu.a.x + (pu.b.x-pu.a.x)*pu.t;
      var py = pu.a.y + (pu.b.y-pu.a.y)*pu.t;
      nCtx.beginPath();
      nCtx.arc(px,py,2.4*DPR,0,Math.PI*2);
      nCtx.fillStyle = 'rgba(255,255,255,0.95)';
      nCtx.shadowColor = '#ff003c';
      nCtx.shadowBlur = 8*DPR;
      nCtx.fill();
      nCtx.shadowBlur = 0;
    }
  }
  var heroVisible = true;
  if('IntersectionObserver' in window){
    new IntersectionObserver(function(entries){
      heroVisible = entries[0].isIntersecting;
    }, {threshold:0}).observe(hero);
  }
  function neuralLoop(){
    if(!reduced && bgVisible && heroVisible){ drawNeural(); }
    requestAnimationFrame(neuralLoop);
  }
  initNeural();
  window.addEventListener('resize', initNeural);
  hero.addEventListener('mousemove', function(e){
    var r = hero.getBoundingClientRect();
    mouse.x = (e.clientX - r.left)*DPR; mouse.y = (e.clientY - r.top)*DPR;
  });
  hero.addEventListener('mouseleave', function(){ mouse.x=-9999; mouse.y=-9999; });
  if(!reduced){ neuralLoop(); } else { drawNeural(); }

})();
</script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nirmal Koswatta — Junior DevOps Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;600;700&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #12151C;
    --panel: #181C26;
    --border: #262B36;
    --text: #E7EAF0;
    --muted: #8891A3;
    --teal: #4FD1C5;
    --amber: #F0A857;
    --radius: 6px;
  }

  *{ box-sizing: border-box; }

  html{ scroll-behavior: smooth; }

  body{
    margin: 0;
    background: var(--bg);
    color: var(--text);
    font-family: 'Inter', sans-serif;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }

  a{ color: var(--teal); }
  a:focus-visible, button:focus-visible{
    outline: 2px solid var(--teal);
    outline-offset: 3px;
  }

  .wrap{
    max-width: 760px;
    margin: 0 auto;
    padding: 0 24px;
  }

  /* ---------- header ---------- */
  header{
    border-bottom: 1px solid var(--border);
    padding: 18px 0;
  }
  .header-row{
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: 760px;
    margin: 0 auto;
    padding: 0 24px;
  }
  .brand{
    font-family: 'Space Grotesk', sans-serif;
    font-weight: 600;
    font-size: 16px;
    letter-spacing: 0.01em;
  }
  .status-pill{
    display: inline-flex;
    align-items: center;
    gap: 7px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    color: var(--muted);
  }
  .dot{
    width: 7px; height: 7px; border-radius: 50%;
    background: var(--teal);
    box-shadow: 0 0 0 3px rgba(79,209,197,0.15);
  }

  /* ---------- hero / terminal ---------- */
  .hero{ padding: 72px 0 56px; }

  .terminal{
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    overflow: hidden;
  }
  .terminal-bar{
    display: flex;
    align-items: center;
    padding: 10px 14px;
    border-bottom: 1px solid var(--border);
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    color: var(--muted);
  }
  .terminal-body{
    padding: 22px 20px 26px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 14px;
    min-height: 168px;
  }
  .terminal-body .line{ white-space: pre-wrap; }
  .prompt{ color: var(--teal); }
  .output{ color: var(--text); }
  .comment{ color: var(--muted); }
  .cursor{
    display: inline-block;
    width: 8px; height: 16px;
    background: var(--teal);
    margin-left: 2px;
    vertical-align: -3px;
    animation: blink 1s steps(1) infinite;
  }
  @keyframes blink{ 50%{ opacity: 0; } }

  h1.title{
    font-family: 'Space Grotesk', sans-serif;
    font-size: 30px;
    font-weight: 700;
    margin: 28px 0 6px;
  }
  .subtitle{
    color: var(--muted);
    font-size: 16px;
    margin: 0 0 0;
  }

  /* ---------- sections ---------- */
  section{ padding: 44px 0; border-top: 1px solid var(--border); }
  section > h2{
    font-family: 'Space Grotesk', sans-serif;
    font-size: 13px;
    font-weight: 600;
    color: var(--muted);
    letter-spacing: 0.06em;
    margin: 0 0 20px;
  }

  .about p{ max-width: 66ch; margin: 0 0 14px; font-size: 15.5px; }
  .about p:last-child{ margin-bottom: 0; }

  /* status board */
  .board-row{
    display: flex;
    gap: 16px;
    padding: 14px 0;
    border-bottom: 1px solid var(--border);
    align-items: flex-start;
  }
  .board-row:last-child{ border-bottom: none; }
  .board-label{
    flex: 0 0 108px;
    display: flex;
    align-items: center;
    gap: 8px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 12px;
    padding-top: 3px;
  }
  .board-label .dot.production{ background: var(--teal); box-shadow: 0 0 0 3px rgba(79,209,197,0.15); }
  .board-label .dot.staging{ background: var(--amber); box-shadow: 0 0 0 3px rgba(240,168,87,0.15); }
  .board-label .dot.planned{ background: transparent; border: 1.5px solid var(--muted); }
  .board-items{
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }
  .chip{
    font-family: 'JetBrains Mono', monospace;
    font-size: 12.5px;
    padding: 4px 10px;
    border: 1px solid var(--border);
    border-radius: 4px;
    color: var(--text);
  }

  /* projects */
  .projects{
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }
  .card{
    background: var(--panel);
    border: 1px solid var(--border);
    border-top: 2px solid var(--teal);
    border-radius: var(--radius);
    padding: 18px 18px 16px;
  }
  .card h3{
    font-family: 'Space Grotesk', sans-serif;
    font-size: 16px;
    margin: 0 0 8px;
  }
  .card p{
    font-size: 14px;
    color: var(--muted);
    margin: 0 0 12px;
  }
  .card .tags{ display: flex; flex-wrap: wrap; gap: 6px; }
  .card .tags span{
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px;
    color: var(--muted);
    border: 1px solid var(--border);
    padding: 2px 7px;
    border-radius: 3px;
  }

  /* pipeline log */
  .log-row{
    display: flex;
    align-items: flex-start;
    gap: 10px;
    padding: 9px 0;
    font-size: 14.5px;
  }
  .log-icon{
    flex: 0 0 18px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 13px;
    padding-top: 1px;
  }
  .log-row.done .log-icon{ color: var(--teal); }
  .log-row.pending .log-icon{ color: var(--amber); }
  .log-row.done span.label{ color: var(--muted); }
  .log-note{
    color: var(--muted);
    font-size: 13px;
  }

  /* connect */
  .connect-list{
    display: flex;
    flex-direction: column;
    gap: 10px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 14.5px;
  }
  .connect-list a{
    color: var(--text);
    text-decoration: none;
    border-bottom: 1px solid var(--border);
    padding-bottom: 2px;
    transition: border-color 0.15s ease, color 0.15s ease;
  }
  .connect-list a:hover{
    color: var(--teal);
    border-color: var(--teal);
  }

  footer{
    border-top: 1px solid var(--border);
    padding: 24px 0 40px;
    color: var(--muted);
    font-size: 12.5px;
    font-family: 'JetBrains Mono', monospace;
  }

  @media (max-width: 600px){
    .projects{ grid-template-columns: 1fr; }
    .board-row{ flex-direction: column; gap: 8px; }
    .board-label{ flex: none; }
    h1.title{ font-size: 24px; }
  }

  @media (prefers-reduced-motion: reduce){
    .cursor{ animation: none; }
    html{ scroll-behavior: auto; }
  }
</style>
</head>
<body>

<header>
  <div class="header-row">
    <span class="brand">N. Koswatta</span>
    <span class="status-pill"><span class="dot"></span>open to junior DevOps roles</span>
  </div>
</header>

<main class="wrap">

  <section class="hero">
    <div class="terminal">
      <div class="terminal-bar">~/nirmal-koswatta — zsh</div>
      <div class="terminal-body" id="termBody"></div>
    </div>
    <h1 class="title">Nirmal Koswatta</h1>
    <p class="subtitle">Junior DevOps Engineer — CI/CD, containers, cloud infrastructure</p>
  </section>

  <section class="about">
    <h2>WHOAMI</h2>
    <p>I work on deployment pipelines, containerized environments, and cloud infrastructure day-to-day at <strong>Zuse Technologies</strong>, and build full-stack and applied-AI side projects in my own time. Previously a DevOps intern at Fortude.</p>
    <p>Final-year BSc (Hons) Computer Science student at the University of Bedfordshire, expected 2027. HND in IT from SLIIT City University, 2025.</p>
  </section>

  <section class="stack">
    <h2>DEPLOY STATUS — SKILLS</h2>
    <div class="board-row">
      <div class="board-label"><span class="dot production"></span>production</div>
      <div class="board-items">
        <span class="chip">Docker</span><span class="chip">Git</span><span class="chip">Linux</span>
        <span class="chip">Nginx</span><span class="chip">Node.js</span><span class="chip">MongoDB</span>
        <span class="chip">GitHub Actions</span>
      </div>
    </div>
    <div class="board-row">
      <div class="board-label"><span class="dot staging"></span>staging</div>
      <div class="board-items">
        <span class="chip">React</span><span class="chip">Python</span>
        <span class="chip">AWS</span><span class="chip">Three.js</span>
      </div>
    </div>
    <div class="board-row">
      <div class="board-label"><span class="dot planned"></span>planned</div>
      <div class="board-items">
        <span class="chip">Terraform</span><span class="chip">Jenkins</span>
        <span class="chip">Kubernetes</span><span class="chip">ELK Stack</span>
      </div>
    </div>
  </section>

  <section class="builds">
    <h2>BUILDS</h2>
    <div class="projects">
      <div class="card">
        <h3>GarageVR</h3>
        <p>Final-year project — WebXR/WebGL 3D vehicle configurator with a computer-vision brand classifier (EfficientNetB3, ~24k images) and a geospatial parts marketplace on MongoDB Atlas.</p>
        <div class="tags"><span>WebXR</span><span>Computer Vision</span><span>MongoDB</span></div>
      </div>
      <div class="card">
        <h3>Tea Lives</h3>
        <p>Tea estate management system with a RAG-based AI assistant and a deep-learning disease classification model.</p>
        <div class="tags"><span>React</span><span>Node.js</span><span>RAG</span></div>
      </div>
    </div>
  </section>

  <section class="pipeline">
    <h2>PIPELINE — CURRENTLY BUILDING TOWARD</h2>
    <div class="log-row done"><span class="log-icon">✓</span><span><span class="label">Dockerized every side project</span> — shipped across GarageVR & Tea Lives</span></div>
    <div class="log-row done"><span class="log-icon">✓</span><span><span class="label">CI pipelines with GitHub Actions</span> — used for automated builds/deploys at Zuse</span></div>
    <div class="log-row pending"><span class="log-icon">○</span><span>Terraform — working through infrastructure-as-code fundamentals</span></div>
    <div class="log-row pending"><span class="log-icon">○</span><span>Jenkins — building pipelines outside of GitHub Actions</span></div>
    <div class="log-row pending"><span class="log-icon">○</span><span>ELK Stack — log aggregation and monitoring</span></div>
  </section>

  <section class="connect">
    <h2>CONNECT</h2>
    <div class="connect-list">
      <a href="mailto:nirmalkoza@gmail.com">nirmalkoza@gmail.com</a>
      <a href="https://linkedin.com/in/nirmal-koswatta-a7889b281">linkedin.com/in/nirmal-koswatta-a7889b281</a>
      <a href="https://github.com/Open-Source-DevOps">github.com/Open-Source-DevOps</a>
    </div>
  </section>

</main>

<footer>
  <div class="wrap">© 2026 Nirmal Koswatta</div>
</footer>

<script>
  const lines = [
    { type: 'prompt', text: '$ whoami' },
    { type: 'output', text: 'nirmal-koswatta — junior devops engineer' },
    { type: 'prompt', text: '$ cat current_focus.txt' },
    { type: 'output', text: 'automating deploys @ zuse technologies' },
    { type: 'prompt', text: '$ echo $LEVELING_UP' },
    { type: 'output', text: 'terraform, jenkins, kubernetes' }
  ];

  const body = document.getElementById('termBody');
  const reduceMotion = window.matchMedia('(prefers-reduced-motion: reduce)').matches;

  function render(){
    body.innerHTML = lines.map(l =>
      `<div class="line ${l.type === 'prompt' ? 'prompt' : 'output'}">${l.text}</div>`
    ).join('') + '<span class="cursor"></span>';
  }

  if (reduceMotion) {
    render();
  } else {
    let i = 0;
    let charIndex = 0;
    let html = '';

    function typeNext(){
      if (i >= lines.length){
        body.innerHTML = html + '<span class="cursor"></span>';
        return;
      }
      const current = lines[i];
      if (charIndex === 0) html += `<div class="line ${current.type === 'prompt' ? 'prompt' : 'output'}">`;
      charIndex++;
      const partial = current.text.slice(0, charIndex);
      body.innerHTML = html + partial + '</div><span class="cursor"></span>';

      if (charIndex >= current.text.length){
        html += current.text + '</div>';
        charIndex = 0;
        i++;
        setTimeout(typeNext, current.type === 'prompt' ? 260 : 160);
      } else {
        setTimeout(typeNext, 18);
      }
    }
    typeNext();
  }
</script>

</body>
</html>

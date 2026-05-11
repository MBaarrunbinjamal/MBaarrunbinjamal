
<style>
@import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Syne:wght@400;700;800&display=swap');
*{box-sizing:border-box;margin:0;padding:0}
:root{
  --brand:#00FFA3;
  --brand2:#00C8FF;
  --dark:#0D1117;
  --surface:#161B22;
  --surface2:#21262D;
  --border:#30363D;
  --text:#E6EDF3;
  --muted:#8B949E;
  --accent:#FF7B72;
}
body{background:var(--dark);color:var(--text);font-family:'Syne',sans-serif;min-height:100vh}
.mono{font-family:'JetBrains Mono',monospace}
.container{max-width:860px;margin:0 auto;padding:2rem 1.5rem}

/* HERO */
.hero{display:grid;grid-template-columns:1fr auto;gap:2rem;align-items:center;padding:2.5rem;background:var(--surface);border:1px solid var(--border);border-radius:16px;position:relative;overflow:hidden;margin-bottom:1.5rem}
.hero::before{content:'';position:absolute;top:-60px;right:-60px;width:220px;height:220px;border-radius:50%;background:radial-gradient(circle,rgba(0,255,163,0.12),transparent 70%);pointer-events:none}
.hero::after{content:'';position:absolute;bottom:-40px;left:30%;width:180px;height:180px;border-radius:50%;background:radial-gradient(circle,rgba(0,200,255,0.09),transparent 70%);pointer-events:none}
.badge-row{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:1rem}
.badge{font-size:11px;padding:4px 10px;border-radius:20px;font-family:'JetBrains Mono',monospace;font-weight:700;letter-spacing:.5px}
.badge-green{background:rgba(0,255,163,0.15);color:var(--brand);border:1px solid rgba(0,255,163,0.3)}
.badge-blue{background:rgba(0,200,255,0.12);color:var(--brand2);border:1px solid rgba(0,200,255,0.25)}
.badge-red{background:rgba(255,123,114,0.12);color:var(--accent);border:1px solid rgba(255,123,114,0.25)}
h1.name{font-size:2rem;font-weight:800;line-height:1.1;margin-bottom:.4rem;letter-spacing:-1px}
h1.name span{background:linear-gradient(135deg,var(--brand),var(--brand2));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text}
.tagline{color:var(--muted);font-size:14px;margin-bottom:1.2rem;font-family:'JetBrains Mono',monospace}
.tagline strong{color:var(--text)}
.contact-row{display:flex;flex-wrap:wrap;gap:10px}
.contact-btn{display:inline-flex;align-items:center;gap:6px;padding:7px 14px;border-radius:8px;font-size:13px;text-decoration:none;font-weight:600;border:1px solid var(--border);color:var(--text);background:var(--surface2);transition:all .2s;cursor:pointer}
.contact-btn:hover{border-color:var(--brand);color:var(--brand)}
.avatar-wrap{position:relative}
.avatar{width:100px;height:100px;border-radius:50%;background:linear-gradient(135deg,var(--brand),var(--brand2));display:flex;align-items:center;justify-content:center;font-size:2.2rem;font-weight:800;color:#0D1117;flex-shrink:0}
.online-dot{position:absolute;bottom:6px;right:6px;width:14px;height:14px;background:var(--brand);border-radius:50%;border:2px solid var(--dark)}

/* GRID CARDS */
.grid2{display:grid;grid-template-columns:1fr 1fr;gap:1rem;margin-bottom:1.5rem}
.grid3{display:grid;grid-template-columns:repeat(3,1fr);gap:1rem;margin-bottom:1.5rem}
.card{background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:1.25rem}
.card-label{font-size:11px;color:var(--muted);text-transform:uppercase;letter-spacing:1px;margin-bottom:.5rem;font-family:'JetBrains Mono',monospace}
.card-val{font-size:1.9rem;font-weight:800;font-family:'JetBrains Mono',monospace;color:var(--brand)}
.card-sub{font-size:12px;color:var(--muted);margin-top:2px}

/* ABOUT */
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:.75rem;margin-bottom:1.5rem}
.about-item{display:flex;align-items:flex-start;gap:10px;background:var(--surface);border:1px solid var(--border);border-radius:10px;padding:.9rem 1rem}
.about-icon{font-size:1.1rem;flex-shrink:0;margin-top:1px}
.about-text{font-size:13px;color:var(--muted);line-height:1.5}
.about-text strong{color:var(--text);display:block;font-size:13px;margin-bottom:1px}

/* SKILLS */
.skills-section{background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:1.25rem;margin-bottom:1.5rem}
.section-title{font-size:13px;color:var(--muted);text-transform:uppercase;letter-spacing:1px;margin-bottom:1rem;font-family:'JetBrains Mono',monospace;display:flex;align-items:center;gap:8px}
.section-title::before{content:'//';color:var(--brand);font-weight:700}
.skills-grid{display:flex;flex-wrap:wrap;gap:8px}
.skill-tag{display:inline-flex;align-items:center;gap:6px;padding:6px 12px;border-radius:6px;font-size:12px;font-family:'JetBrains Mono',monospace;font-weight:600;background:var(--surface2);border:1px solid var(--border);color:var(--text);transition:all .2s}
.skill-tag:hover{border-color:var(--brand);color:var(--brand)}
.skill-dot{width:6px;height:6px;border-radius:50%}

/* ACTIVITY BAR */
.bar-row{margin-bottom:1.5rem;background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:1.25rem}
.bar-list{display:flex;flex-direction:column;gap:.75rem;margin-top:.75rem}
.bar-item{display:grid;grid-template-columns:90px 1fr 40px;align-items:center;gap:10px}
.bar-name{font-size:12px;font-family:'JetBrains Mono',monospace;color:var(--muted)}
.bar-track{height:6px;background:var(--surface2);border-radius:4px;overflow:hidden}
.bar-fill{height:100%;border-radius:4px;transition:width 1s ease}
.bar-pct{font-size:11px;font-family:'JetBrains Mono',monospace;color:var(--muted);text-align:right}

/* STREAK */
.streak-section{background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:1.25rem;margin-bottom:1.5rem}
.heatmap{display:grid;grid-template-columns:repeat(52,1fr);gap:2px;margin-top:.75rem}
.hm-cell{aspect-ratio:1;border-radius:2px;background:var(--surface2)}

/* STATS GRID */
.stats-embed{display:grid;grid-template-columns:1fr 1fr;gap:1rem;margin-bottom:1.5rem}
.stat-card{background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:1.25rem;position:relative;overflow:hidden}
.stat-card img{width:100%;border-radius:6px;opacity:.9}
.stat-card::after{content:'';position:absolute;inset:0;border-radius:12px;border:1px solid var(--border);pointer-events:none}

/* TROPHIES */
.trophy-row{background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:1.25rem;margin-bottom:1.5rem}
.trophy-row img{width:100%;border-radius:6px}

/* FOOTER */
.footer{text-align:center;font-size:12px;color:var(--muted);font-family:'JetBrains Mono',monospace;padding:1.5rem 0 .5rem}
.footer span{color:var(--brand)}

/* ACTIVITY CHART */
.mini-chart{display:flex;align-items:flex-end;gap:3px;height:60px;margin-top:.75rem}
.mini-bar{flex:1;border-radius:3px 3px 0 0;background:var(--surface2);min-width:8px;transition:background .2s}
.mini-bar:hover{background:var(--brand)}
</style>

<div class="container">

  <!-- HERO -->
  <div class="hero">
    <div>
      <div class="badge-row">
        <span class="badge badge-green">🟢 Available for collab</span>
        <span class="badge badge-blue">Pakistan 🇵🇰</span>
        <span class="badge badge-red">ML + DevOps learner</span>
      </div>
      <h1 class="name">Muhammad <span>Baarrun</span><br>bin Jamal</h1>
      <p class="tagline"><strong>Web Developer</strong> · AI Enthusiast · Open Source Contributor</p>
      <div class="contact-row">
        <a class="contact-btn" href="mailto:mbaarrun2008@gmail.com">
          <i class="ti ti-mail" aria-hidden="true"></i> mbaarrun2008@gmail.com
        </a>
        <a class="contact-btn" href="https://linkedin.com/in/M-Baarrun-bin-Jamal">
          <i class="ti ti-brand-linkedin" aria-hidden="true"></i> LinkedIn
        </a>
        <a class="contact-btn" href="https://ehsan.dev">
          <i class="ti ti-world" aria-hidden="true"></i> ehsan.dev
        </a>
      </div>
    </div>
    <div class="avatar-wrap">
      <div class="avatar">MB</div>
      <div class="online-dot"></div>
    </div>
  </div>

  <!-- STAT COUNTERS -->
  <div class="grid3" id="counters">
    <div class="card">
      <div class="card-label">Total commits</div>
      <div class="card-val mono" id="c1">0</div>
      <div class="card-sub">↑ 38 this month</div>
    </div>
    <div class="card">
      <div class="card-label">Repositories</div>
      <div class="card-val mono" id="c2">0</div>
      <div class="card-sub">Public + private</div>
    </div>
    <div class="card">
      <div class="card-label">Streak (days)</div>
      <div class="card-val mono" id="c3">0</div>
      <div class="card-sub">Personal best 🔥</div>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="about-grid">
    <div class="about-item">
      <span class="about-icon">🔭</span>
      <div class="about-text"><strong>Currently building</strong>AI-driven solutions to real-world problems</div>
    </div>
    <div class="about-item">
      <span class="about-icon">🌱</span>
      <div class="about-text"><strong>Currently learning</strong>Advanced Machine Learning &amp; DevOps</div>
    </div>
    <div class="about-item">
      <span class="about-icon">👯</span>
      <div class="about-text"><strong>Looking to collaborate</strong>Open-source projects</div>
    </div>
    <div class="about-item">
      <span class="about-icon">💬</span>
      <div class="about-text"><strong>Ask me about</strong>Python · Django · ML · Git · Docker</div>
    </div>
    <div class="about-item">
      <span class="about-icon">👨‍💻</span>
      <div class="about-text"><strong>All projects at</strong><a href="https://ehsan.dev" style="color:var(--brand)">ehsan.dev</a></div>
    </div>
    <div class="about-item">
      <span class="about-icon">⚡</span>
      <div class="about-text"><strong>Fun fact</strong>Explores new tech every single week</div>
    </div>
  </div>

  <!-- SKILLS -->
  <div class="skills-section">
    <div class="section-title">Languages &amp; Tools</div>
    <div class="skills-grid">
      <span class="skill-tag"><span class="skill-dot" style="background:#3776AB"></span>Python</span>
      <span class="skill-tag"><span class="skill-dot" style="background:#092E20"></span>Django</span>
      <span class="skill-tag"><span class="skill-dot" style="background:#61DAFB"></span>React</span>
      <span class="skill-tag"><span class="skill-dot" style="background:#E34F26"></span>HTML5</span>
      <span class="skill-tag"><span class="skill-dot" style="background:#1572B6"></span>CSS3</span>
      <span class="skill-tag"><span class="skill-dot" style="background:#F7DF1E"></span>JavaScript</span>
      <span class="skill-tag"><span class="skill-dot" style="background:#F05032"></span>Git</span>
      <span class="skill-tag"><span class="skill-dot" style="background:#2496ED"></span>Docker</span>
      <span class="skill-tag"><span class="skill-dot" style="background:#FCC624"></span>Linux</span>
      <span class="skill-tag"><span class="skill-dot" style="background:#FF6C37"></span>Postman</span>
      <span class="skill-tag"><span class="skill-dot" style="background:#430098"></span>Heroku</span>
      <span class="skill-tag"><span class="skill-dot" style="background:#007ACC"></span>VS Code</span>
    </div>
  </div>

  <!-- LANGUAGE BARS -->
  <div class="bar-row">
    <div class="section-title">Top languages</div>
    <div class="bar-list" id="bars"></div>
  </div>

  <!-- COMMIT ACTIVITY -->
  <div class="bar-row">
    <div class="section-title">Commit activity — last 12 months</div>
    <div class="mini-chart" id="activity"></div>
  </div>

  <!-- CONTRIBUTION HEATMAP -->
  <div class="streak-section">
    <div class="section-title">Contribution heatmap</div>
    <div class="heatmap" id="heatmap"></div>
  </div>

  <!-- GITHUB STATS -->
  <div class="stats-embed">
    <div class="stat-card">
      <img src="https://github-readme-stats.vercel.app/api?username=md-ehsanulhaque&show_icons=true&theme=github_dark&hide_border=true&bg_color=161B22&title_color=00FFA3&icon_color=00C8FF&text_color=8B949E" alt="GitHub Stats" loading="lazy"/>
    </div>
    <div class="stat-card">
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=md-ehsanulhaque&theme=github-dark-blue&hide_border=true&background=161B22&stroke=30363D&ring=00FFA3&fire=FF7B72&currStreakLabel=00FFA3" alt="Streak Stats" loading="lazy"/>
    </div>
  </div>

  <!-- TROPHIES -->
  <div class="trophy-row">
    <div class="section-title">GitHub Trophies</div>
    <img src="https://github-profile-trophy.vercel.app/?username=md-ehsanulhaque&theme=darkhub&no-frame=true&row=1&column=7&margin-w=8" alt="GitHub Trophies" loading="lazy" style="margin-top:.75rem"/>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <span>// built with passion from Karachi, Pakistan 🇵🇰</span><br>
    <span style="opacity:.5;font-size:11px">profile generated · 2025</span>
  </div>

</div>

<script>
function animCount(id, target, dur){
  const el = document.getElementById(id);
  if(!el) return;
  const start = performance.now();
  function step(now){
    const p = Math.min((now - start)/dur, 1);
    el.textContent = Math.round(p * target);
    if(p < 1) requestAnimationFrame(step);
  }
  requestAnimationFrame(step);
}
animCount('c1', 847, 1800);
animCount('c2', 34, 1400);
animCount('c3', 21, 1200);

const langs = [
  {name:'Python', pct:48, color:'#3776AB'},
  {name:'JavaScript', pct:27, color:'#F7DF1E'},
  {name:'HTML/CSS', pct:14, color:'#E34F26'},
  {name:'Shell/Bash', pct:7, color:'#89E051'},
  {name:'Dockerfile', pct:4, color:'#2496ED'},
];
const barList = document.getElementById('bars');
langs.forEach(l => {
  barList.innerHTML += `<div class="bar-item">
    <span class="bar-name">${l.name}</span>
    <div class="bar-track"><div class="bar-fill" style="width:0%;background:${l.color}" data-w="${l.pct}"></div></div>
    <span class="bar-pct">${l.pct}%</span>
  </div>`;
});
setTimeout(()=>{
  document.querySelectorAll('.bar-fill').forEach(b=>{
    b.style.width = b.dataset.w + '%';
  });
},200);

const months = [12,19,8,24,31,15,22,41,18,29,35,27];
const actEl = document.getElementById('activity');
const maxM = Math.max(...months);
months.forEach(v => {
  const d = document.createElement('div');
  d.className = 'mini-bar';
  d.style.height = Math.round((v/maxM)*100) + '%';
  d.title = v + ' commits';
  actEl.appendChild(d);
});

const hm = document.getElementById('heatmap');
const intensities = ['#161B22','#0E4429','#006D32','#26A641','#39D353'];
for(let i=0;i<52*7;i++){
  const c = document.createElement('div');
  c.className = 'hm-cell';
  const r = Math.random();
  const idx = r < .5 ? 0 : r < .65 ? 1 : r < .8 ? 2 : r < .92 ? 3 : 4;
  c.style.background = intensities[idx];
  c.title = Math.round(r*8) + ' contributions';
  hm.appendChild(c);
}
</script>

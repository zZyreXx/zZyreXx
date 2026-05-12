[taifyu_github_readme_preview.html](https://github.com/user-attachments/files/27652994/taifyu_github_readme_preview.html)

<style>
  @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600&family=Space+Mono:wght@400;700&display=swap');

  * { box-sizing: border-box; margin: 0; padding: 0; }

  .readme-wrap {
    background: #0d1117;
    color: #e6edf3;
    font-family: 'Fira Code', monospace;
    padding: 2rem 1.5rem;
    min-height: 600px;
    position: relative;
    overflow: hidden;
    border-radius: 12px;
  }

  .grid-bg {
    position: absolute;
    inset: 0;
    background-image:
      linear-gradient(rgba(88,166,255,0.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(88,166,255,0.04) 1px, transparent 1px);
    background-size: 32px 32px;
    pointer-events: none;
  }

  .scanline {
    position: absolute;
    top: -100%;
    left: 0;
    width: 100%;
    height: 40%;
    background: linear-gradient(transparent, rgba(88,166,255,0.03), transparent);
    animation: scan 6s linear infinite;
    pointer-events: none;
  }

  @keyframes scan {
    0% { top: -40%; }
    100% { top: 100%; }
  }

  .content { position: relative; z-index: 1; }

  /* Header */
  .header { text-align: center; margin-bottom: 2rem; }

  .typing-title {
    font-family: 'Space Mono', monospace;
    font-size: 1.1rem;
    color: #58a6ff;
    overflow: hidden;
    white-space: nowrap;
    border-right: 2px solid #58a6ff;
    width: 0;
    animation: typeTitle 2.5s steps(38) 0.3s forwards, blink 0.75s step-end infinite;
    display: inline-block;
  }

  @keyframes typeTitle {
    to { width: 100%; }
  }
  @keyframes blink {
    50% { border-color: transparent; }
  }

  .subtitle {
    font-size: 0.72rem;
    color: #8b949e;
    margin-top: 0.5rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    opacity: 0;
    animation: fadeUp 0.6s ease 2.8s forwards;
  }

  /* Badge row */
  .badges {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    justify-content: center;
    margin: 1rem 0 1.5rem;
    opacity: 0;
    animation: fadeUp 0.6s ease 3.2s forwards;
  }

  .badge {
    background: #161b22;
    border: 1px solid #30363d;
    border-radius: 20px;
    padding: 4px 12px;
    font-size: 0.65rem;
    color: #8b949e;
    display: flex;
    align-items: center;
    gap: 5px;
    transition: border-color 0.2s, color 0.2s;
  }

  .badge:hover { border-color: #58a6ff; color: #58a6ff; }

  .badge-dot {
    width: 7px; height: 7px;
    border-radius: 50%;
    background: #3fb950;
    animation: pulse 2s ease infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(0.8); }
  }

  /* About section */
  .section-header {
    font-size: 0.7rem;
    color: #58a6ff;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    margin-bottom: 0.75rem;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .section-header::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, #30363d, transparent);
  }

  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 10px;
    margin-bottom: 1.5rem;
    opacity: 0;
    animation: fadeUp 0.6s ease 3.5s forwards;
  }

  .about-card {
    background: #161b22;
    border: 1px solid #30363d;
    border-radius: 8px;
    padding: 0.8rem;
    font-size: 0.65rem;
    color: #8b949e;
    line-height: 1.6;
    transition: border-color 0.2s, transform 0.2s;
    text-align: center;
  }

  .about-card:hover {
    border-color: #58a6ff;
    transform: translateY(-2px);
  }

  .about-card .icon { font-size: 1.2rem; display: block; margin-bottom: 4px; }
  .about-card .label { color: #e6edf3; font-size: 0.68rem; }

  /* Skills */
  .skills-section {
    margin-bottom: 1.5rem;
    opacity: 0;
    animation: fadeUp 0.6s ease 3.8s forwards;
  }

  .skill-bar-wrap {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 8px;
  }

  .skill-name {
    font-size: 0.63rem;
    color: #e6edf3;
    width: 90px;
    flex-shrink: 0;
  }

  .skill-bar-bg {
    flex: 1;
    height: 5px;
    background: #21262d;
    border-radius: 10px;
    overflow: hidden;
  }

  .skill-bar-fill {
    height: 100%;
    border-radius: 10px;
    width: 0;
    transition: width 1.2s ease;
  }

  .skill-pct {
    font-size: 0.58rem;
    color: #58a6ff;
    width: 28px;
    text-align: right;
  }

  /* Skill icons */
  .skill-icons {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 1.5rem;
    opacity: 0;
    animation: fadeUp 0.6s ease 4s forwards;
  }

  .skill-icon-pill {
    background: #161b22;
    border: 1px solid #30363d;
    border-radius: 6px;
    padding: 5px 10px;
    font-size: 0.6rem;
    color: #8b949e;
    display: flex;
    align-items: center;
    gap: 5px;
    transition: all 0.2s;
    cursor: default;
  }

  .skill-icon-pill:hover { border-color: var(--c); color: var(--c); }
  .skill-icon-pill img { width: 14px; height: 14px; }

  /* Stats */
  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
    margin-bottom: 1.5rem;
    opacity: 0;
    animation: fadeUp 0.6s ease 4.2s forwards;
  }

  .stats-card {
    background: #161b22;
    border: 1px solid #30363d;
    border-radius: 8px;
    padding: 0.8rem 1rem;
    font-size: 0.63rem;
    color: #8b949e;
    overflow: hidden;
  }

  .stats-card img {
    width: 100%;
    height: auto;
    display: block;
    opacity: 0.9;
  }

  /* Terminal block */
  .terminal {
    background: #010409;
    border: 1px solid #30363d;
    border-radius: 8px;
    overflow: hidden;
    margin-bottom: 1.5rem;
    opacity: 0;
    animation: fadeUp 0.6s ease 4.5s forwards;
  }

  .terminal-bar {
    background: #161b22;
    padding: 8px 12px;
    display: flex;
    align-items: center;
    gap: 6px;
    border-bottom: 1px solid #30363d;
  }

  .terminal-dot {
    width: 8px; height: 8px;
    border-radius: 50%;
  }

  .terminal-body {
    padding: 1rem;
    font-size: 0.63rem;
    line-height: 1.9;
  }

  .t-prompt { color: #3fb950; }
  .t-cmd { color: #e6edf3; }
  .t-out { color: #8b949e; }
  .t-hi { color: #58a6ff; }
  .t-warn { color: #d29922; }

  /* Support */
  .support-section {
    text-align: center;
    opacity: 0;
    animation: fadeUp 0.6s ease 4.8s forwards;
  }

  .support-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: #21262d;
    border: 1px solid #30363d;
    border-radius: 8px;
    padding: 10px 20px;
    color: #e6edf3;
    font-family: 'Fira Code', monospace;
    font-size: 0.68rem;
    cursor: pointer;
    transition: all 0.2s;
    margin-top: 0.5rem;
  }

  .support-btn:hover { background: #f6c90e22; border-color: #f6c90e; color: #f6c90e; }

  .footer-text {
    font-size: 0.58rem;
    color: #484f58;
    text-align: center;
    margin-top: 1.5rem;
    opacity: 0;
    animation: fadeUp 0.6s ease 5s forwards;
  }

  /* Snake animation strip */
  .snake-strip {
    background: #161b22;
    border: 1px solid #30363d;
    border-radius: 8px;
    padding: 0.5rem;
    margin-bottom: 1.5rem;
    overflow: hidden;
    opacity: 0;
    animation: fadeUp 0.6s ease 4s forwards;
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .snake-canvas { display: block; width: 100%; height: 28px; }

  /* Copy button */
  .copy-btn {
    position: absolute;
    top: 1rem;
    right: 1rem;
    background: #21262d;
    border: 1px solid #30363d;
    border-radius: 6px;
    padding: 5px 10px;
    color: #8b949e;
    font-family: 'Fira Code', monospace;
    font-size: 0.58rem;
    cursor: pointer;
    z-index: 10;
    transition: all 0.2s;
  }
  .copy-btn:hover { border-color: #58a6ff; color: #58a6ff; }

  .view-raw-btn {
    display: inline-block;
    margin-top: 1rem;
    background: #21262d;
    border: 1px solid #30363d;
    border-radius: 6px;
    padding: 6px 14px;
    color: #8b949e;
    font-family: 'Fira Code', monospace;
    font-size: 0.62rem;
    cursor: pointer;
    transition: all 0.2s;
  }
  .view-raw-btn:hover { border-color: #3fb950; color: #3fb950; }
</style>

<div class="readme-wrap">
  <div class="grid-bg"></div>
  <div class="scanline"></div>

  <button class="copy-btn" onclick="copyReadme()">⎘ copy README</button>

  <div class="content">

    <!-- Header -->
    <div class="header" style="opacity:0;animation:fadeUp 0.6s ease 0.1s forwards;">
      <div style="font-size:0.65rem;color:#484f58;margin-bottom:0.5rem;">// TAIFYU · github.com/zZyreXx</div>
      <div class="typing-title">Hi there! &nbsp;I'm TAIFYU 👋</div>
      <div class="subtitle">Fullstack Developer &nbsp;·&nbsp; Discord Bot Architect &nbsp;·&nbsp; Gamer</div>
    </div>

    <!-- Badges -->
    <div class="badges">
      <span class="badge"><span class="badge-dot"></span> Open to collaborate</span>
      <span class="badge">⚡ Fullstack Dev</span>
      <span class="badge">🤖 Bot Builder</span>
      <span class="badge">🎮 Gamer</span>
      <span class="badge">🌱 Learning LLMs</span>
    </div>

    <!-- Terminal -->
    <div class="terminal" style="animation-delay:1.5s">
      <div class="terminal-bar">
        <span class="terminal-dot" style="background:#ff5f57"></span>
        <span class="terminal-dot" style="background:#febc2e"></span>
        <span class="terminal-dot" style="background:#28c840"></span>
        <span style="font-size:0.6rem;color:#484f58;margin-left:6px;">zsh — ~</span>
      </div>
      <div class="terminal-body">
        <div><span class="t-prompt">taifyu@dev</span><span style="color:#484f58">:</span><span style="color:#58a6ff">~</span><span style="color:#484f58">$ </span><span class="t-cmd">cat about_me.json</span></div>
        <div class="t-out">{</div>
        <div class="t-out">&nbsp;&nbsp;"name": <span class="t-hi">"TAIFYU"</span>,</div>
        <div class="t-out">&nbsp;&nbsp;"role": <span class="t-hi">"Fullstack Developer"</span>,</div>
        <div class="t-out">&nbsp;&nbsp;"loves": [<span class="t-warn">"Discord Bots"</span>, <span class="t-warn">"Web Dev"</span>, <span class="t-warn">"Gaming"</span>],</div>
        <div class="t-out">&nbsp;&nbsp;"learning": <span class="t-hi">"Large Language Models"</span>,</div>
        <div class="t-out">&nbsp;&nbsp;"github": <span class="t-hi">"@zZyreXx"</span>,</div>
        <div class="t-out">&nbsp;&nbsp;"coffee_link": <span class="t-hi">"buymeacoffee.com/zZyreXxSer"</span></div>
        <div class="t-out">}</div>
        <div style="margin-top:4px;"><span class="t-prompt">taifyu@dev</span><span style="color:#484f58">:</span><span style="color:#58a6ff">~</span><span style="color:#484f58">$ </span><span class="t-cmd" id="cursor-line"></span><span style="animation:blink 1s step-end infinite;color:#58a6ff">█</span></div>
      </div>
    </div>

    <!-- About cards -->
    <div style="opacity:0;animation:fadeUp 0.6s ease 2s forwards;">
      <div class="section-header">// about.me</div>
    </div>
    <div class="about-grid" style="animation-delay:2.2s">
      <div class="about-card">
        <span class="icon">🤖</span>
        <span class="label">Discord Bots</span><br>
        I love building powerful, scalable bots
      </div>
      <div class="about-card">
        <span class="icon">🧠</span>
        <span class="label">LLM Explorer</span><br>
        Currently diving deep into large language models
      </div>
      <div class="about-card">
        <span class="icon">🎮</span>
        <span class="label">Gamer</span><br>
        When I'm not coding, I'm gaming
      </div>
    </div>

    <!-- Skills bars -->
    <div class="skills-section" style="animation-delay:2.5s">
      <div class="section-header">// skill.stack</div>
      <div id="skill-bars"></div>
    </div>

    <!-- Skill pills -->
    <div class="skill-icons">
      <span class="skill-icon-pill" style="--c:#3776ab">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg"> Python
      </span>
      <span class="skill-icon-pill" style="--c:#f7df1e">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg"> JavaScript
      </span>
      <span class="skill-icon-pill" style="--c:#e44d26">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg"> HTML5
      </span>
      <span class="skill-icon-pill" style="--c:#1572b6">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg"> CSS3
      </span>
      <span class="skill-icon-pill" style="--c:#68a063">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg"> Node.js
      </span>
      <span class="skill-icon-pill" style="--c:#61dafb">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg"> React
      </span>
      <span class="skill-icon-pill" style="--c:#3178c6">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg"> TypeScript
      </span>
      <span class="skill-icon-pill" style="--c:#47a248">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg"> MongoDB
      </span>
    </div>

    <!-- Stats -->
    <div class="stats-grid">
      <div class="stats-card">
        <img src="https://github-readme-stats.vercel.app/api?username=zZyreXx&theme=transparent&show_icons=true&hide_border=true&count_private=false&text_color=58a6ff&title_color=e6edf3&icon_color=3fb950" />
      </div>
      <div class="stats-card">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=zZyreXx&theme=transparent&show_icons=true&hide_border=true&layout=compact&text_color=58a6ff&title_color=e6edf3" />
      </div>
    </div>

    <!-- Snake strip (contribution style) -->
    <div class="snake-strip">
      <canvas class="snake-canvas" id="snakeCanvas" height="28"></canvas>
    </div>

    <!-- Support -->
    <div class="support-section">
      <div class="section-header">// support.me</div>
      <div style="font-size:0.62rem;color:#8b949e;margin-bottom:0.5rem;">If you like my work, buy me a coffee ☕</div>
      <button class="support-btn" onclick="openLink('https://www.buymeacoffee.com/zZyreXxSer')">
        ☕ buymeacoffee.com/zZyreXxSer
      </button>
      <div style="margin-top:1rem;font-size:0.62rem;color:#8b949e;">Check the repos for code → <span style="color:#58a6ff">github.com/zZyreXx</span></div>
    </div>

    <div class="footer-text">
      ─── Made with ❤️ by TAIFYU · Fullstack Dev · Discord Bot Architect ───
    </div>

    <div style="text-align:center;opacity:0;animation:fadeUp 0.6s ease 5.2s forwards;">
      <button class="view-raw-btn" onclick="showMarkdown()">📄 View README.md source</button>
    </div>

  </div>
</div>

<div id="markdown-output" style="display:none;margin-top:1rem;background:#010409;border:1px solid #30363d;border-radius:8px;padding:1rem;font-family:'Fira Code',monospace;font-size:0.62rem;color:#8b949e;white-space:pre-wrap;line-height:1.8;max-height:400px;overflow-y:auto;"></div>

<script>
const skills = [
  { name: 'Python',      pct: 88, color: '#3776ab' },
  { name: 'JavaScript',  pct: 80, color: '#f7df1e' },
  { name: 'Node.js',     pct: 75, color: '#68a063' },
  { name: 'HTML/CSS',    pct: 85, color: '#e44d26' },
  { name: 'TypeScript',  pct: 60, color: '#3178c6' },
  { name: 'Discord.js',  pct: 92, color: '#5865f2' },
];

const container = document.getElementById('skill-bars');
skills.forEach(s => {
  const row = document.createElement('div');
  row.className = 'skill-bar-wrap';
  row.innerHTML = `
    <span class="skill-name">${s.name}</span>
    <div class="skill-bar-bg"><div class="skill-bar-fill" data-pct="${s.pct}" style="background:${s.color}"></div></div>
    <span class="skill-pct">${s.pct}%</span>
  `;
  container.appendChild(row);
});

setTimeout(() => {
  document.querySelectorAll('.skill-bar-fill').forEach(el => {
    el.style.width = el.dataset.pct + '%';
  });
}, 3800);

const canvas = document.getElementById('snakeCanvas');
const ctx = canvas.getContext('2d');
canvas.width = canvas.offsetWidth;
canvas.height = 28;

const cellSize = 8;
const cols = Math.floor(canvas.width / cellSize);
const rows = Math.floor(canvas.height / cellSize);

let snake = [{x: 2, y: 1}];
let dir = {x: 1, y: 0};
let food = {x: Math.floor(cols/2), y: 1};
let contributions = [];

for (let i = 0; i < cols; i++) {
  contributions.push(Math.floor(Math.random() * 4));
}

function contribColor(lvl) {
  return ['#161b22','#0e4429','#006d32','#26a641','#39d353'][lvl];
}

function drawSnake() {
  ctx.clearRect(0, 0, canvas.width, canvas.height);

  for (let x = 0; x < cols; x++) {
    const lvl = contributions[x];
    ctx.fillStyle = contribColor(lvl);
    ctx.beginPath();
    ctx.roundRect(x * cellSize + 1, 1, cellSize - 2, canvas.height - 2, 2);
    ctx.fill();
  }

  ctx.fillStyle = '#ff5f57';
  ctx.beginPath();
  ctx.arc(food.x * cellSize + cellSize/2, food.y * cellSize + cellSize/2, 3, 0, Math.PI*2);
  ctx.fill();

  snake.forEach((seg, i) => {
    ctx.fillStyle = i === 0 ? '#58a6ff' : `rgba(88,166,255,${0.7 - i*0.06})`;
    ctx.beginPath();
    ctx.roundRect(seg.x * cellSize + 1, seg.y * cellSize + 1, cellSize-2, cellSize-2, 2);
    ctx.fill();
  });
}

function moveSnake() {
  const head = {x: snake[0].x + dir.x, y: snake[0].y + dir.y};
  if (head.x < 0) head.x = cols - 1;
  if (head.x >= cols) head.x = 0;
  if (head.y < 0) head.y = rows - 1;
  if (head.y >= rows) head.y = 0;

  if (head.x === food.x && head.y === food.y) {
    snake.unshift(head);
    contributions[food.x] = Math.min(4, contributions[food.x] + 1);
    food = {x: Math.floor(Math.random()*cols), y: Math.floor(Math.random()*rows)};
  } else {
    snake = [head, ...snake.slice(0, 6)];
  }

  if (Math.random() < 0.3) {
    const choices = [{x:1,y:0},{x:-1,y:0}];
    if (rows > 1) choices.push({x:0,y:1},{x:0,y:-1});
    const newDir = choices[Math.floor(Math.random()*choices.length)];
    if (!(newDir.x === -dir.x && newDir.y === -dir.y)) dir = newDir;
  }
  drawSnake();
}

setInterval(moveSnake, 80);
drawSnake();

const rawMD = `<!--
  ╔══════════════════════════════════════════════════╗
  ║   TAIFYU · zZyreXx · Fullstack Dev              ║
  ╚══════════════════════════════════════════════════╝
-->

<div align="center">

\`\`\`
 ████████╗ █████╗ ██╗███████╗██╗   ██╗██╗   ██╗
    ██╔══╝██╔══██╗██║██╔════╝╚██╗ ██╔╝██║   ██║
    ██║   ███████║██║█████╗   ╚████╔╝ ██║   ██║
    ██║   ██╔══██║██║██╔══╝   ╚██╔╝  ██║   ██║
    ██║   ██║  ██║██║██║       ██║   ╚██████╔╝
    ╚═╝   ╚═╝  ╚═╝╚═╝╚═╝       ╚═╝    ╚═════╝
\`\`\`

### Hi there! I'm TAIFYU 👋
#### Fullstack Developer · Discord Bot Architect · Gamer

![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=58A6FF&center=true&vCenter=true&width=500&lines=Fullstack+Developer;Discord+Bot+Architect;LLM+Explorer;Always+Building+Something+Cool)

[![Open to Collaborate](https://img.shields.io/badge/-Open%20to%20Collaborate-3fb950?style=flat-square&logo=github&logoColor=white)](https://github.com/zZyreXx)
[![Discord Bots](https://img.shields.io/badge/-Discord%20Bot%20Builder-5865F2?style=flat-square&logo=discord&logoColor=white)](#)
[![LLM Explorer](https://img.shields.io/badge/-Learning%20LLMs-ff6b6b?style=flat-square&logo=openai&logoColor=white)](#)

</div>

---

### 👾 About Me

\`\`\`json
{
  "name": "TAIFYU",
  "role": "Fullstack Developer",
  "loves": ["Discord Bots", "Web Dev", "Gaming"],
  "learning": "Large Language Models",
  "github": "@zZyreXx",
  "support": "buymeacoffee.com/zZyreXxSer"
}
\`\`\`

- 🤖 I love creating **Discord bots** that are powerful and scalable
- 🧠 Currently learning **Large Language Models** & AI integration
- 🎮 Gamer at heart — when I'm not coding, I'm gaming
- 📦 Check my repos for source code!

---

### 🛠️ Tech Stack

<div align="left">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Discord.js](https://img.shields.io/badge/Discord.js-5865F2?style=for-the-badge&logo=discord&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)

</div>

---

### 📊 GitHub Stats

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=zZyreXx&theme=transparent&show_icons=true&hide_border=true&count_private=false&text_color=58a6ff&title_color=e6edf3&icon_color=3fb950" height="150" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=zZyreXx&theme=transparent&show_icons=true&hide_border=true&layout=compact&text_color=58a6ff&title_color=e6edf3" height="150" />
</div>

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=zZyreXx&theme=dark&hide_border=true&stroke=58a6ff&ring=58a6ff&fire=3fb950&currStreakLabel=e6edf3" />
</div>

---

### 🐍 My Contributions

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/zZyreXx/zZyreXx/output/github-contribution-grid-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/zZyreXx/zZyreXx/output/github-contribution-grid-snake.svg" />
  <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/zZyreXx/zZyreXx/output/github-contribution-grid-snake.svg" />
</picture>

---

### ☕ Support Me

<div align="center">
  <a href="https://www.buymeacoffee.com/zZyreXxSer">
    <img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" height="50" width="210" />
  </a>
</div>

---

<div align="center">
  <sub>Made with ❤️ by TAIFYU · check repos for code!</sub>
</div>
`;

function showMarkdown() {
  const el = document.getElementById('markdown-output');
  if (el.style.display === 'none') {
    el.style.display = 'block';
    el.textContent = rawMD;
  } else {
    el.style.display = 'none';
  }
}

function copyReadme() {
  navigator.clipboard.writeText(rawMD).then(() => {
    const btn = document.querySelector('.copy-btn');
    btn.textContent = '✓ copied!';
    btn.style.color = '#3fb950';
    setTimeout(() => { btn.textContent = '⎘ copy README'; btn.style.color = ''; }, 2000);
  });
}
</script>

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Manu Bharadwaj — GitHub README</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:ital,wght@0,300;0,400;0,500;0,700;1,400&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --bg: #060a0f;
    --s1: #0d1117;
    --s2: #161b22;
    --s3: #21262d;
    --border: #30363d;
    --accent: #58a6ff;
    --green: #3fb950;
    --orange: #f0883e;
    --purple: #d2a8ff;
    --red: #f85149;
    --yellow: #e3b341;
    --text: #e6edf3;
    --muted: #8b949e;
    --dim: #484f58;
    --fmono: 'JetBrains Mono', monospace;
    --fhead: 'Syne', sans-serif;
  }
  html { scroll-behavior: smooth; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--fmono);
    min-height: 100vh;
  }
  body::before {
    content: '';
    position: fixed; inset: 0;
    background-image:
      linear-gradient(rgba(88,166,255,0.025) 1px, transparent 1px),
      linear-gradient(90deg, rgba(88,166,255,0.025) 1px, transparent 1px);
    background-size: 48px 48px;
    pointer-events: none; z-index: 0;
  }
  .wrap { position: relative; z-index: 1; max-width: 960px; margin: 0 auto; padding: 36px 20px 60px; }

  /* HERO */
  .hero {
    display: grid;
    grid-template-columns: auto 1fr auto;
    align-items: center;
    gap: 20px;
    padding: 28px 32px;
    background: var(--s1);
    border: 1px solid var(--border);
    border-radius: 16px;
    margin-bottom: 20px;
    animation: fadeUp .4s ease both;
  }
  .avatar {
    width: 76px; height: 76px;
    border-radius: 50%;
    border: 2px solid var(--accent);
    padding: 2px;
    flex-shrink: 0;
  }
  .avatar img { width: 100%; height: 100%; border-radius: 50%; object-fit: cover; }
  .hero-name { font-family: var(--fhead); font-size: 28px; font-weight: 800; letter-spacing: -0.5px; }
  .hero-sub { font-size: 11px; color: var(--muted); letter-spacing: 2.5px; text-transform: uppercase; margin: 4px 0 10px; }
  .badge-row { display: flex; flex-wrap: wrap; gap: 6px; }
  .badge {
    display: inline-flex; align-items: center; gap: 5px;
    font-size: 10px; font-weight: 600; padding: 3px 10px;
    border-radius: 20px; border: 1px solid; text-decoration: none;
    letter-spacing: .5px; transition: opacity .15s;
  }
  .badge:hover { opacity: .8; }
  .ba { background: rgba(88,166,255,.1); border-color: rgba(88,166,255,.35); color: #79c0ff; }
  .bg { background: rgba(63,185,80,.1); border-color: rgba(63,185,80,.35); color: #56d364; }
  .bp { background: rgba(210,168,255,.1); border-color: rgba(210,168,255,.35); color: var(--purple); }
  .bo { background: rgba(240,136,62,.1); border-color: rgba(240,136,62,.35); color: var(--orange); }
  .hero-ranks { text-align: right; }
  .rank-item { margin-bottom: 10px; }
  .rank-platform { font-size: 9px; letter-spacing: 2px; text-transform: uppercase; color: var(--dim); }
  .rank-num { font-size: 22px; font-weight: 700; font-family: var(--fhead); }
  .rank-num.gold { color: var(--yellow); }
  .rank-num.silver { color: #a8b2c0; }
  .rank-label { font-size: 10px; color: var(--muted); }

  /* GRID LAYOUT */
  .grid2 { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 16px; }
  .grid3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 16px; margin-bottom: 16px; }
  .full { grid-column: 1 / -1; }

  /* PANEL */
  .panel {
    background: var(--s1); border: 1px solid var(--border);
    border-radius: 12px; overflow: hidden;
    animation: fadeUp .4s ease both;
  }
  .ph {
    display: flex; align-items: center; justify-content: space-between;
    padding: 12px 18px; border-bottom: 1px solid var(--border);
    background: var(--s2);
  }
  .pt {
    font-size: 10px; font-weight: 600; letter-spacing: 2.5px;
    text-transform: uppercase; color: var(--muted);
    display: flex; align-items: center; gap: 8px;
  }
  .pt::before { content: ''; width: 7px; height: 7px; border-radius: 50%; background: var(--accent); display: inline-block; }
  .pb { padding: 16px 18px; }

  /* README OUTPUT */
  .readme-box {
    font-family: var(--fmono); font-size: 11.5px; line-height: 1.75;
    color: #a8d8a8; white-space: pre-wrap; word-break: break-all;
    max-height: 600px; overflow-y: auto;
    scrollbar-width: thin; scrollbar-color: var(--border) transparent;
    background: #070b10; padding: 18px;
  }
  .readme-box::-webkit-scrollbar { width: 4px; }
  .readme-box::-webkit-scrollbar-thumb { background: var(--border); border-radius: 4px; }

  /* COPY BTN */
  .copy-btn {
    display: flex; align-items: center; gap: 7px;
    background: var(--accent); color: #060a0f;
    border: none; border-radius: 8px; padding: 8px 18px;
    font-family: var(--fmono); font-size: 12px; font-weight: 700;
    cursor: pointer; transition: all .15s; letter-spacing: .5px; white-space: nowrap;
  }
  .copy-btn:hover { background: #79c0ff; transform: translateY(-1px); }
  .copy-btn.ok { background: var(--green); }

  /* EXP CARDS */
  .exp-item { padding: 14px 0; border-bottom: 1px solid var(--border); }
  .exp-item:last-child { border-bottom: none; padding-bottom: 0; }
  .exp-top { display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 4px; }
  .exp-co { font-size: 13px; font-weight: 600; color: var(--text); }
  .exp-period { font-size: 10px; color: var(--dim); background: var(--s3); padding: 2px 8px; border-radius: 4px; white-space: nowrap; }
  .exp-role { font-size: 11px; color: var(--accent); margin-bottom: 6px; }
  .exp-bullets { list-style: none; }
  .exp-bullets li { font-size: 11px; color: var(--muted); line-height: 1.6; padding-left: 14px; position: relative; margin-bottom: 3px; }
  .exp-bullets li::before { content: '›'; position: absolute; left: 0; color: var(--green); font-size: 13px; }
  .highlight { color: var(--green); font-weight: 600; }

  /* STACK */
  .stack-group { margin-bottom: 14px; }
  .stack-group:last-child { margin-bottom: 0; }
  .stack-lbl { font-size: 9px; letter-spacing: 2.5px; text-transform: uppercase; color: var(--dim); margin-bottom: 7px; }
  .pills { display: flex; flex-wrap: wrap; gap: 5px; }
  .pill {
    font-size: 10px; padding: 3px 9px; border-radius: 4px;
    border: 1px solid; font-weight: 500;
  }
  .pa { background: rgba(88,166,255,.08); border-color: rgba(88,166,255,.25); color: #79c0ff; }
  .pg { background: rgba(63,185,80,.08); border-color: rgba(63,185,80,.25); color: #56d364; }
  .pp { background: rgba(210,168,255,.08); border-color: rgba(210,168,255,.25); color: var(--purple); }
  .py { background: rgba(227,179,65,.08); border-color: rgba(227,179,65,.25); color: var(--yellow); }
  .pr { background: rgba(248,81,73,.08); border-color: rgba(248,81,73,.25); color: var(--red); }

  /* PROJECTS */
  .proj { padding: 14px 0; border-bottom: 1px solid var(--border); }
  .proj:last-child { border-bottom: none; padding-bottom: 0; }
  .proj-title { font-size: 13px; font-weight: 600; color: var(--text); margin-bottom: 4px; display: flex; align-items: center; gap: 8px; }
  .proj-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--green); flex-shrink: 0; }
  .proj-desc { font-size: 11px; color: var(--muted); line-height: 1.65; margin-bottom: 8px; }

  /* CP CARDS */
  .cp-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .cp-card { background: var(--s2); border: 1px solid var(--border); border-radius: 10px; padding: 14px 16px; }
  .cp-plat { font-size: 9px; letter-spacing: 2.5px; text-transform: uppercase; color: var(--dim); margin-bottom: 6px; }
  .cp-rank { font-size: 26px; font-weight: 800; font-family: var(--fhead); line-height: 1; margin-bottom: 4px; }
  .cp-rank.gold { color: var(--yellow); }
  .cp-rank.silver { color: #a8b2c0; }
  .cp-sub { font-size: 11px; color: var(--muted); }
  .cp-imgs { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-top: 12px; }
  .cp-img-box { background: var(--s2); border: 1px solid var(--border); border-radius: 8px; overflow: hidden; display: flex; flex-direction: column; align-items: center; justify-content: center; min-height: 160px; }
  .cp-img-box img { width: 100%; max-width: 340px; display: block; border-radius: 6px; }
  .cp-img-label { font-size: 10px; color: var(--dim); padding: 8px; text-align: center; }

  /* STEPS */
  .steps {
    background: var(--s1); border: 1px solid var(--border);
    border-radius: 12px; padding: 18px 24px;
    display: flex; gap: 0; align-items: stretch; flex-wrap: wrap;
    margin-top: 16px;
  }
  .step { display: flex; align-items: center; gap: 12px; flex: 1; min-width: 160px; padding: 4px 16px; }
  .step:first-child { padding-left: 0; }
  .step:not(:first-child) { border-left: 1px solid var(--border); }
  .snum {
    width: 30px; height: 30px; border-radius: 50%;
    background: var(--s3); border: 1px solid var(--border);
    display: flex; align-items: center; justify-content: center;
    font-size: 12px; font-weight: 700; color: var(--accent); flex-shrink: 0;
  }
  .stxt strong { display: block; font-size: 12px; color: var(--text); margin-bottom: 2px; }
  .stxt span { font-size: 11px; color: var(--muted); line-height: 1.5; }

  /* AVAIL STRIP */
  .avail {
    display: flex; align-items: center; gap: 10px;
    background: rgba(63,185,80,.07); border: 1px solid rgba(63,185,80,.25);
    border-radius: 10px; padding: 10px 16px; margin-bottom: 16px;
  }
  .avail-dot { width: 8px; height: 8px; border-radius: 50%; background: var(--green); animation: pulse 2s ease-in-out infinite; flex-shrink: 0; }
  .avail-txt { font-size: 12px; color: #56d364; font-weight: 500; }

  @keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:.5;transform:scale(.8)} }
  @keyframes fadeUp { from{opacity:0;transform:translateY(14px)} to{opacity:1;transform:translateY(0)} }

  .panel:nth-child(1){animation-delay:.05s}
  .panel:nth-child(2){animation-delay:.1s}
  .panel:nth-child(3){animation-delay:.15s}
  .panel:nth-child(4){animation-delay:.2s}
  .panel:nth-child(5){animation-delay:.25s}

  @media(max-width:680px){
    .hero{grid-template-columns:1fr; gap:12px;}
    .hero-ranks{text-align:left; display:flex; gap:24px;}
    .grid2,.grid3,.cp-grid,.cp-imgs{grid-template-columns:1fr;}
    .steps{flex-direction:column; gap:12px;}
    .step{border-left:none!important; padding:4px 0!important; border-top:1px solid var(--border);}
    .step:first-child{border-top:none;}
  }
</style>
</head>
<body>
<div class="wrap">

  <!-- HERO -->
  <div class="hero">
    <div class="avatar">
      <img src="https://i.postimg.cc/SKBNcms1/Bharadwaj-removebg-preview.png" alt="Manu" onerror="this.style.display='none'"/>
    </div>
    <div>
      <div class="hero-name">Manu Bharadwaj</div>
      <div class="hero-sub">Full-Stack Engineer · Competitive Programmer · Scalable Systems</div>
      <div class="badge-row">
        <a class="badge ba" href="https://www.linkedin.com/in/manu-bharadwaj-3507a345" target="_blank">LinkedIn</a>
        <a class="badge ba" href="https://github.com/Manu577228" target="_blank">GitHub</a>
        <a class="badge bo" href="https://leetcode.com/u/mbbn/" target="_blank">LeetCode</a>
        <a class="badge ba" href="https://codeforces.com/profile/MBBN" target="_blank">Codeforces</a>
        <a class="badge bg" href="https://manu-bharadwaj-portfolio.vercel.app/" target="_blank">Portfolio</a>
        <span class="badge bg">● Open to Work</span>
      </div>
    </div>
    <div class="hero-ranks">
      <div class="rank-item">
        <div class="rank-platform">LeetCode</div>
        <div class="rank-num gold">#49</div>
        <div class="rank-label">Best Global Rank</div>
      </div>
      <div class="rank-item">
        <div class="rank-platform">Codeforces</div>
        <div class="rank-num silver">#113</div>
        <div class="rank-label">Best Rank</div>
      </div>
    </div>
  </div>

  <div class="avail">
    <div class="avail-dot"></div>
    <div class="avail-txt">Available for full-time roles · Software Engineering · Backend / Full-stack · Bangalore, India</div>
  </div>

  <!-- ROW 1 -->
  <div class="grid2">

    <!-- README panel -->
    <div class="panel" style="grid-column:1/2">
      <div class="ph">
        <div class="pt">README.md — Full Output</div>
        <button class="copy-btn" id="copyBtn" onclick="doCopy()">
          <svg width="13" height="13" viewBox="0 0 16 16" fill="currentColor"><path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"/><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"/></svg>
          Copy README
        </button>
      </div>
      <div class="readme-box" id="readmeOut"></div>
    </div>

    <!-- Right col -->
    <div style="display:flex;flex-direction:column;gap:16px;">

      <!-- CP Ranks -->
      <div class="panel">
        <div class="ph"><div class="pt">Competitive Programming</div></div>
        <div class="pb">
          <div class="cp-grid">
            <div class="cp-card">
              <div class="cp-plat">LeetCode · mbbn</div>
              <div class="cp-rank gold">#49</div>
              <div class="cp-sub">Best Global Rank</div>
              <div style="margin-top:8px;font-size:11px;color:var(--muted)">Graphs · DP · Trees · Greedy · String algorithms</div>
            </div>
            <div class="cp-card">
              <div class="cp-plat">Codeforces · MBBN</div>
              <div class="cp-rank silver">#113</div>
              <div class="cp-sub">Best Contest Rank</div>
              <div style="margin-top:8px;font-size:11px;color:var(--muted)">Rated · High-perf Java implementations</div>
            </div>
          </div>
          <div class="cp-imgs">
            <div class="cp-img-box">
              <img src="https://leetcard.jacoblin.cool/mbbn?theme=dark&font=Courier&ext=contest" alt="LeetCode stats" loading="lazy"/>
              <div class="cp-img-label">LeetCode Card · live data</div>
            </div>
            <div class="cp-img-box">
              <img src="https://codeforces-readme-stats.vercel.app/api/card?username=MBBN" alt="Codeforces stats" loading="lazy"/>
              <div class="cp-img-label">Codeforces Card · live data</div>
            </div>
          </div>
        </div>
      </div>

      <!-- Stack -->
      <div class="panel">
        <div class="ph"><div class="pt">Tech Stack</div></div>
        <div class="pb">
          <div class="stack-group">
            <div class="stack-lbl">Frontend</div>
            <div class="pills">
              <span class="pill pa">React</span><span class="pill pa">Next.js</span><span class="pill pa">Angular</span>
              <span class="pill pa">TypeScript</span><span class="pill pa">Redux</span><span class="pill pa">Micro Frontends</span>
            </div>
          </div>
          <div class="stack-group">
            <div class="stack-lbl">Backend</div>
            <div class="pills">
              <span class="pill pp">Spring Boot</span><span class="pill pp">Express.js</span>
              <span class="pill pp">Django</span><span class="pill pp">GraphQL</span><span class="pill pp">Kafka</span><span class="pill pp">JWT</span>
            </div>
          </div>
          <div class="stack-group">
            <div class="stack-lbl">Data</div>
            <div class="pills">
              <span class="pill pg">PostgreSQL</span><span class="pill pg">MySQL</span>
              <span class="pill pg">MongoDB</span><span class="pill pg">SQLite</span><span class="pill pg">Redis</span>
            </div>
          </div>
          <div class="stack-group">
            <div class="stack-lbl">Infra & Languages</div>
            <div class="pills">
              <span class="pill py">Docker</span><span class="pill py">Jenkins</span><span class="pill py">AWS EC2</span><span class="pill py">CI/CD</span>
              <span class="pill pr">Java</span><span class="pill pr">Python</span><span class="pill pr">JavaScript</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Experience -->
  <div class="panel" style="margin-bottom:16px">
    <div class="ph"><div class="pt">Experience</div></div>
    <div class="pb">
      <div class="exp-item">
        <div class="exp-top">
          <div class="exp-co">Fractal Analytics</div>
          <div class="exp-period">Jun 2024 – Sep 2024 · Jun 2025 – Sep 2025</div>
        </div>
        <div class="exp-role">Full Stack Engineering Intern · Rehired 2 Cycles</div>
        <ul class="exp-bullets">
          <li>Designed multi-tenant expense management platform with cross-functional financial workflows, real-time dashboards — adopted in production by multiple internal teams.</li>
          <li>Reduced API <span class="highlight">p99 latency by 40%</span> by profiling endpoints, eliminating N+1 queries, and introducing composite DB indexing.</li>
          <li>Implemented JWT authentication with role-based access control across all platform endpoints.</li>
          <li>Competitively rehired for a second cycle based on demonstrated engineering ownership and cross-team impact.</li>
        </ul>
      </div>
      <div class="exp-item">
        <div class="exp-top">
          <div class="exp-co">Allstate India</div>
          <div class="exp-period">Nov 2022 – Mar 2023</div>
        </div>
        <div class="exp-role">Software Engineer</div>
        <ul class="exp-bullets">
          <li>Engineered enterprise React reporting platforms consolidating analytics for global stakeholders — eliminated duplicate data pipelines.</li>
          <li>Improved CI/CD stability with pre-merge validation gates, cutting rollback frequency and accelerating release cadence.</li>
        </ul>
      </div>
      <div class="exp-item">
        <div class="exp-top">
          <div class="exp-co">TechChef's Software <span style="font-size:10px;color:var(--dim)">· Dell, Intuit, JPMC</span></div>
          <div class="exp-period">Sep 2021 – Nov 2022</div>
        </div>
        <div class="exp-role">Consultant · Client-facing Engineering</div>
        <ul class="exp-bullets">
          <li>Architected React Micro Frontend system enabling fully independent per-team deployments — eliminated cross-team release coupling.</li>
          <li>Built QuickBooks-integrated modules in React + GraphQL, replacing over-fetching REST calls and <span class="highlight">cutting data transfer 35%</span>.</li>
          <li>Delivered Jest + Enzyme testing framework from zero — <span class="highlight">90%+ test coverage</span> and WCAG-compliant, cross-browser UIs.</li>
        </ul>
      </div>
      <div class="exp-item">
        <div class="exp-top">
          <div class="exp-co">Fidelitus Corp</div>
          <div class="exp-period">Jan 2021 – Jul 2021</div>
        </div>
        <div class="exp-role">Executive IT</div>
        <ul class="exp-bullets">
          <li>Built reusable React components and secure auth flows for enterprise platforms, enforcing design system conventions across 5+ views.</li>
        </ul>
      </div>
    </div>
  </div>

  <!-- Projects -->
  <div class="panel" style="margin-bottom:16px">
    <div class="ph"><div class="pt">Projects</div></div>
    <div class="pb">
      <div class="proj">
        <div class="proj-title"><span class="proj-dot"></span> URL Shortener · High-Throughput Link Management</div>
        <div class="proj-desc">
          Sub-10ms p99 URL resolution using Base62 encoding with collision-resistant ID generation and composite DB indexing. Horizontally scalable API with token-bucket rate limiting and idempotent write handling — modeled on production link-shortening infrastructure at scale.
        </div>
        <div class="pills"><span class="pill pp">Spring Boot</span><span class="pill pg">MySQL</span><span class="pill pa">React</span><span class="pill py">Docker</span></div>
      </div>
      <div class="proj" style="border-bottom:none;padding-bottom:0">
        <div class="proj-title"><span class="proj-dot"></span> Expense Splitter · Distributed Group Settlement</div>
        <div class="proj-desc">
          Multi-user expense splitting engine with real-time balance tracking, unequal shares, partial payments and group settlements. Optimistic UI updates with server-side reconciliation backed by atomic Django transactions — zero inconsistency under concurrent load.
        </div>
        <div class="pills"><span class="pill pp">Django</span><span class="pill pg">SQLite</span><span class="pill pa">React</span></div>
      </div>
    </div>
  </div>

  <!-- Instructions -->
  <div class="steps">
    <div class="step">
      <div class="snum">1</div>
      <div class="stxt"><strong>Click "Copy README"</strong><span>Full markdown copied to clipboard</span></div>
    </div>
    <div class="step">
      <div class="snum">2</div>
      <div class="stxt"><strong>Create repo on GitHub</strong><span>Name it exactly <code style="color:var(--accent)">Manu577228</code></span></div>
    </div>
    <div class="step">
      <div class="snum">3</div>
      <div class="stxt"><strong>Paste into README.md</strong><span>Edit → Paste → Commit → Live</span></div>
    </div>
  </div>

</div>

<script>
const README = `<div align="center">

<img src="https://i.postimg.cc/SKBNcms1/Bharadwaj-removebg-preview.png" width="110" style="border-radius:50%;" />

# Manu Bharadwaj

**Full-Stack Software Engineer · Competitive Programmer · Scalable Systems**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0D1117?style=for-the-badge&logo=linkedin&logoColor=58A6FF)](https://www.linkedin.com/in/manu-bharadwaj-3507a345)
[![GitHub](https://img.shields.io/badge/GitHub-0D1117?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Manu577228)
[![LeetCode](https://img.shields.io/badge/LeetCode-0D1117?style=for-the-badge&logo=leetcode&logoColor=FFA116)](https://leetcode.com/u/mbbn/)
[![Codeforces](https://img.shields.io/badge/Codeforces-0D1117?style=for-the-badge&logo=codeforces&logoColor=1F8ACB)](https://codeforces.com/profile/MBBN)
[![Portfolio](https://img.shields.io/badge/Portfolio-0D1117?style=for-the-badge&logo=vercel&logoColor=white)](https://manu-bharadwaj-portfolio.vercel.app/)

![](https://img.shields.io/badge/Status-Open%20to%20Work-2ea44f?style=flat-square)
![](https://img.shields.io/badge/Experience-2.8%2B%20Years-58a6ff?style=flat-square)
![](https://img.shields.io/badge/LeetCode%20Best%20Rank-%2349%20Global-FFA116?style=flat-square)
![](https://img.shields.io/badge/Codeforces%20Best%20Rank-%23113-1F8ACB?style=flat-square)

</div>

---

## About

Full-Stack Software Engineer with **2.8 years** of production experience — equally fluent in backend engineering (distributed systems, high-throughput APIs, microservices) and frontend development (React, Angular, modern JavaScript). Proven track record owning features from database to UI and delivering measurable performance improvements.

**LeetCode Best Global Rank #49** · **Codeforces Best Rank #113** · Exceptionally strong in algorithms, system design, and competitive programming.

---

## Competitive Programming

| Platform | Handle | Best Rank | Strengths |
|----------|--------|-----------|-----------|
| 🟡 LeetCode | [mbbn](https://leetcode.com/u/mbbn/) | **#49 Global** | Graphs, DP, trees, greedy, string algorithms |
| 🔵 Codeforces | [MBBN](https://codeforces.com/profile/MBBN) | **#113** | Rated contests · High-performance Java |

<div align="center">

<img src="https://leetcard.jacoblin.cool/mbbn?theme=dark&font=Courier&ext=contest" />

<br/><br/>

<img src="https://codeforces-readme-stats.vercel.app/api/card?username=MBBN" />

</div>

---

## Experience

**Fractal Analytics** · Full Stack Engineering Intern *(Rehired — 2 Cycles)*
\`Jun 2024 – Sep 2024\` · \`Jun 2025 – Sep 2025\`

- Designed multi-tenant expense management platform with cross-functional financial workflows and real-time dashboards — adopted by multiple internal teams in production.
- Reduced API **p99 latency by 40%** by profiling endpoints, eliminating N+1 query patterns, and introducing composite DB indexing.
- Implemented JWT authentication with RBAC securing all platform endpoints.
- Competitively rehired for a second cycle based on demonstrated impact and engineering ownership.

---

**Allstate India** · Software Engineer
\`Nov 2022 – Mar 2023\`

- Engineered enterprise React reporting platforms consolidating analytics for global stakeholders — eliminated duplicate data pipelines.
- Improved CI/CD stability with pre-merge validation gates, cutting rollback frequency and accelerating release cadence.

---

**TechChef's Software** · Consultant *(Dell, Intuit, JPMC)*
\`Sep 2021 – Nov 2022\`

- Architected React Micro Frontend system enabling fully independent per-team deployments — eliminated cross-team release coupling.
- Built QuickBooks-integrated GraphQL modules, replacing over-fetching REST calls and **cutting data transfer by 35%**.
- Delivered Jest + Enzyme testing framework from zero — **90%+ test coverage**, WCAG-compliant, cross-browser UIs.

---

**Fidelitus Corp** · Executive IT
\`Jan 2021 – Jul 2021\`

- Built reusable React components and secure authentication flows for enterprise internal platforms across 5+ views.

---

## Tech Stack

**Frontend**
![React](https://img.shields.io/badge/React-0D1117?style=flat-square&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-0D1117?style=flat-square&logo=next.js&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-0D1117?style=flat-square&logo=angular&logoColor=DD0031)
![TypeScript](https://img.shields.io/badge/TypeScript-0D1117?style=flat-square&logo=typescript&logoColor=3178C6)
![Redux](https://img.shields.io/badge/Redux-0D1117?style=flat-square&logo=redux&logoColor=764ABC)

**Backend**
![Spring Boot](https://img.shields.io/badge/Spring_Boot-0D1117?style=flat-square&logo=springboot&logoColor=6DB33F)
![Express](https://img.shields.io/badge/Express.js-0D1117?style=flat-square&logo=express&logoColor=white)
![Django](https://img.shields.io/badge/Django-0D1117?style=flat-square&logo=django&logoColor=092E20)
![GraphQL](https://img.shields.io/badge/GraphQL-0D1117?style=flat-square&logo=graphql&logoColor=E10098)
![Kafka](https://img.shields.io/badge/Kafka-0D1117?style=flat-square&logo=apachekafka&logoColor=white)

**Data**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0D1117?style=flat-square&logo=postgresql&logoColor=336791)
![MySQL](https://img.shields.io/badge/MySQL-0D1117?style=flat-square&logo=mysql&logoColor=4479A1)
![MongoDB](https://img.shields.io/badge/MongoDB-0D1117?style=flat-square&logo=mongodb&logoColor=47A248)
![Redis](https://img.shields.io/badge/Redis-0D1117?style=flat-square&logo=redis&logoColor=DC382D)

**Infrastructure**
![Docker](https://img.shields.io/badge/Docker-0D1117?style=flat-square&logo=docker&logoColor=2496ED)
![Jenkins](https://img.shields.io/badge/Jenkins-0D1117?style=flat-square&logo=jenkins&logoColor=D24939)
![AWS](https://img.shields.io/badge/AWS_EC2-0D1117?style=flat-square&logo=amazonaws&logoColor=FF9900)
![CI/CD](https://img.shields.io/badge/CI%2FCD-0D1117?style=flat-square&logo=githubactions&logoColor=2088FF)

---

## Projects

### URL Shortener · High-Throughput Link Management
Sub-10ms p99 URL resolution using Base62 encoding with collision-resistant ID generation and composite DB indexing. Horizontally scalable API with token-bucket rate limiting and idempotent write handling — modeled on production link-shortening infrastructure at scale.

\`Spring Boot\` \`MySQL\` \`React\` \`Docker\`

### Expense Splitter · Distributed Group Settlement
Multi-user expense splitting engine with real-time balance tracking, unequal shares, partial payments and group settlements. Optimistic UI updates backed by atomic Django transactions — zero inconsistency under concurrent load.

\`Django\` \`SQLite\` \`React\`

---

## Engineering Principles

> Algorithmic clarity over clever hacks.  
> Measure before optimizing.  
> Design for scale from day one.  
> Own outcomes end-to-end.

---

<div align="center">

📧 bnmanubharadwaj@gmail.com &nbsp;·&nbsp; 🌐 [manu-bharadwaj-portfolio.vercel.app](https://manu-bharadwaj-portfolio.vercel.app/)

*Competitive precision. Scalable engineering. Measurable results.*

</div>`;

document.getElementById('readmeOut').textContent = README;

function doCopy() {
  navigator.clipboard.writeText(README).then(() => {
    const btn = document.getElementById('copyBtn');
    btn.classList.add('ok');
    btn.innerHTML = `<svg width="13" height="13" viewBox="0 0 16 16" fill="currentColor"><path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.75.75 0 0 1 1.06-1.06L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"/></svg> Copied!`;
    setTimeout(() => {
      btn.classList.remove('ok');
      btn.innerHTML = `<svg width="13" height="13" viewBox="0 0 16 16" fill="currentColor"><path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"/><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"/></svg> Copy README`;
    }, 2500);
  }).catch(() => {
    const ta = document.createElement('textarea');
    ta.value = README; ta.style.cssText = 'position:fixed;opacity:0;top:0;left:0';
    document.body.appendChild(ta); ta.select();
    document.execCommand('copy'); document.body.removeChild(ta);
  });
}
</script>
</body>
</html>

<div align="center">

<img src="https://i.postimg.cc/SKBNcms1/Bharadwaj-removebg-preview.png" width="110" style="border-radius:50%;" />

# Manu Bharadwaj

**Full-Stack Software Engineer · Competitive Programmer · Scalable Systems**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0D1117?style=for-the-badge&logo=linkedin&logoColor=58A6FF)](https://www.linkedin.com/in/manu-bharadwaj-3507a345)
[![GitHub](https://img.shields.io/badge/GitHub-0D1117?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Manu577228)
[![LeetCode](https://img.shields.io/badge/LeetCode-0D1117?style=for-the-badge&logo=leetcode&logoColor=FFA116)](https://leetcode.com/u/mbbn/)
[![Codeforces](https://img.shields.io/badge/Codeforces-0D1117?style=for-the-badge&logo=codeforces&logoColor=1F8ACB)](https://codeforces.com/profile/MBBN)
[![Portfolio](https://img.shields.io/badge/Portfolio-0D1117?style=for-the-badge&logo=vercel&logoColor=white)](https://manu-bharadwaj-portfolio.vercel.app/)

![](https://img.shields.io/badge/Status-Open%20to%20Work-2ea44f?style=flat-square)
![](https://img.shields.io/badge/Experience-2.8%2B%20Years-58a6ff?style=flat-square)
![](https://img.shields.io/badge/LeetCode%20Best%20Rank-%2349%20Global-FFA116?style=flat-square)
![](https://img.shields.io/badge/Codeforces%20Best%20Rank-%23113-1F8ACB?style=flat-square)

</div>

---

## About

Full-Stack Software Engineer with **2.8 years** of production experience — equally fluent in backend engineering (distributed systems, high-throughput APIs, microservices) and frontend development (React, Angular, modern JavaScript). Proven track record owning features from database to UI and delivering measurable performance improvements.

**LeetCode Best Global Rank #49** · **Codeforces Best Rank #113** · Exceptionally strong in algorithms, system design, and competitive programming.

---

## Competitive Programming

| Platform | Handle | Best Rank | Strengths |
|----------|--------|-----------|-----------|
| 🟡 LeetCode | [mbbn](https://leetcode.com/u/mbbn/) | **#49 Global** | Graphs, DP, trees, greedy, string algorithms |
| 🔵 Codeforces | [MBBN](https://codeforces.com/profile/MBBN) | **#113** | Rated contests · High-performance Java |

<div align="center">

<img src="https://leetcard.jacoblin.cool/mbbn?theme=dark&font=Courier&ext=contest" />

<br/><br/>

<img src="https://codeforces-readme-stats.vercel.app/api/card?username=MBBN" />

</div>

---

## Experience

**Fractal Analytics** · Full Stack Engineering Intern *(Rehired — 2 Cycles)*
`Jun 2024 – Sep 2024` · `Jun 2025 – Sep 2025`

- Designed multi-tenant expense management platform with cross-functional financial workflows and real-time dashboards — adopted by multiple internal teams in production.
- Reduced API **p99 latency by 40%** by profiling endpoints, eliminating N+1 query patterns, and introducing composite DB indexing.
- Implemented JWT authentication with RBAC securing all platform endpoints.
- Competitively rehired for a second cycle based on demonstrated impact and engineering ownership.

---

**Allstate India** · Software Engineer
`Nov 2022 – Mar 2023`

- Engineered enterprise React reporting platforms consolidating analytics for global stakeholders — eliminated duplicate data pipelines.
- Improved CI/CD stability with pre-merge validation gates, cutting rollback frequency and accelerating release cadence.

---

**TechChef's Software** · Consultant *(Dell, Intuit, JPMC)*
`Sep 2021 – Nov 2022`

- Architected React Micro Frontend system enabling fully independent per-team deployments — eliminated cross-team release coupling.
- Built QuickBooks-integrated GraphQL modules, replacing over-fetching REST calls and **cutting data transfer by 35%**.
- Delivered Jest + Enzyme testing framework from zero — **90%+ test coverage**, WCAG-compliant, cross-browser UIs.

---

**Fidelitus Corp** · Executive IT
`Jan 2021 – Jul 2021`

- Built reusable React components and secure authentication flows for enterprise internal platforms across 5+ views.

---

## Tech Stack

**Frontend**
![React](https://img.shields.io/badge/React-0D1117?style=flat-square&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-0D1117?style=flat-square&logo=next.js&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-0D1117?style=flat-square&logo=angular&logoColor=DD0031)
![TypeScript](https://img.shields.io/badge/TypeScript-0D1117?style=flat-square&logo=typescript&logoColor=3178C6)
![Redux](https://img.shields.io/badge/Redux-0D1117?style=flat-square&logo=redux&logoColor=764ABC)

**Backend**
![Spring Boot](https://img.shields.io/badge/Spring_Boot-0D1117?style=flat-square&logo=springboot&logoColor=6DB33F)
![Express](https://img.shields.io/badge/Express.js-0D1117?style=flat-square&logo=express&logoColor=white)
![Django](https://img.shields.io/badge/Django-0D1117?style=flat-square&logo=django&logoColor=092E20)
![GraphQL](https://img.shields.io/badge/GraphQL-0D1117?style=flat-square&logo=graphql&logoColor=E10098)
![Kafka](https://img.shields.io/badge/Kafka-0D1117?style=flat-square&logo=apachekafka&logoColor=white)

**Data**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0D1117?style=flat-square&logo=postgresql&logoColor=336791)
![MySQL](https://img.shields.io/badge/MySQL-0D1117?style=flat-square&logo=mysql&logoColor=4479A1)
![MongoDB](https://img.shields.io/badge/MongoDB-0D1117?style=flat-square&logo=mongodb&logoColor=47A248)
![Redis](https://img.shields.io/badge/Redis-0D1117?style=flat-square&logo=redis&logoColor=DC382D)

**Infrastructure**
![Docker](https://img.shields.io/badge/Docker-0D1117?style=flat-square&logo=docker&logoColor=2496ED)
![Jenkins](https://img.shields.io/badge/Jenkins-0D1117?style=flat-square&logo=jenkins&logoColor=D24939)
![AWS](https://img.shields.io/badge/AWS_EC2-0D1117?style=flat-square&logo=amazonaws&logoColor=FF9900)
![CI/CD](https://img.shields.io/badge/CI%2FCD-0D1117?style=flat-square&logo=githubactions&logoColor=2088FF)

---

## Projects

### URL Shortener · High-Throughput Link Management
Sub-10ms p99 URL resolution using Base62 encoding with collision-resistant ID generation and composite DB indexing. Horizontally scalable API with token-bucket rate limiting and idempotent write handling — modeled on production link-shortening infrastructure at scale.

`Spring Boot` `MySQL` `React` `Docker`

### Expense Splitter · Distributed Group Settlement
Multi-user expense splitting engine with real-time balance tracking, unequal shares, partial payments and group settlements. Optimistic UI updates backed by atomic Django transactions — zero inconsistency under concurrent load.

`Django` `SQLite` `React`

---

## Engineering Principles

> Algorithmic clarity over clever hacks.  
> Measure before optimizing.  
> Design for scale from day one.  
> Own outcomes end-to-end.

---

<div align="center">

📧 bnmanubharadwaj@gmail.com &nbsp;·&nbsp; 🌐 [manu-bharadwaj-portfolio.vercel.app](https://manu-bharadwaj-portfolio.vercel.app/)

*Competitive precision. Scalable engineering. Measurable results.*

</div>

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bharadwaj BN - GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Creepster&family=Nosifer&family=Eater&family=Orbitron:wght@700;900&family=Rajdhani:wght@400;600;700&family=Russo+One&display=swap" rel="stylesheet">
<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    font-family: 'Rajdhani', sans-serif;
    background: #000;
    color: #fff;
    overflow-x: hidden;
    position: relative;
    padding: 0;
    margin: 0;
  }

  /* Animated Neon Background */
  body::before {
    content: '';
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: 
      radial-gradient(circle at 20% 30%, rgba(255,255,255,0.15) 0%, #000 100%),
      repeating-linear-gradient(
         135deg,
         rgba(0,0,0,0.90) 0px,
         rgba(0,0,0,0.90) 16px,
         rgba(255,255,255,0.05) 16px,
         rgba(255,255,255,0.05) 32px
      );
    background-attachment: fixed;
    z-index: -2;
  }

  /* Animated Grid Lines */
  body::after {
    content: '';
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: 
      linear-gradient(rgba(255,255,255,0.02) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255,255,255,0.02) 1px, transparent 1px);
    background-size: 50px 50px;
    z-index: -1;
    animation: gridMove 20s linear infinite;
  }

  @keyframes gridMove {
    0% { transform: translateY(0); }
    100% { transform: translateY(50px); }
  }

  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 60px 40px;
    text-align: center;
  }

  /* Profile Image */
  .profile-img {
    width: 250px;
    height: auto;
    border-radius: 30px;
    box-shadow: 
      18px 18px 30px #cfcfcf,
      -18px -18px 30px #ffffff,
      0 0 30px rgba(255,255,255,0.3);
    margin-bottom: 30px;
    animation: float 3s ease-in-out infinite;
  }

  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-10px); }
  }

  /* Main Name - Epic Funky Style */
  h1 {
    font-family: 'Creepster', cursive;
    font-size: 70px;
    font-weight: 900;
    margin-bottom: 5px;
    background: linear-gradient(90deg, #fff, #ccc, #fff);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-shadow: 0 0 12px #ffffff99;
    letter-spacing: 3px;
    animation: shimmer 3s linear infinite, glitchText 4s infinite;
    background-size: 200% auto;
  }

  @keyframes shimmer {
    to { background-position: 200% center; }
  }

  @keyframes glitchText {
    0%, 90%, 100% { transform: translate(0); }
    92% { transform: translate(-2px, 2px); }
    94% { transform: translate(2px, -2px); }
    96% { transform: translate(-2px, -2px); }
    98% { transform: translate(2px, 2px); }
  }

  /* Subtitle */
  .subtitle {
    font-size: 22px;
    color: #f0f0f0;
    font-style: italic;
    margin-bottom: 30px;
    letter-spacing: 1px;
  }

  /* Typing Effect Container */
  .typing-container {
    margin: 30px 0;
  }

  .typing-container img {
    max-width: 100%;
    height: auto;
  }

  /* About Me Box - Gothic Style */
  .about-box {
    max-width: 780px;
    padding: 30px;
    border-radius: 25px;
    background: rgba(255,255,255,0.08);
    backdrop-filter: blur(12px);
    box-shadow: 0 0 25px #ffffff33, inset 0 0 20px #000000aa;
    margin: 40px auto;
    font-size: 17px;
    line-height: 1.7;
  }

  h2 {
    font-family: 'Nosifer', cursive;
    font-size: 40px;
    color: #fff;
    font-weight: 900;
    text-shadow: 0 0 10px #fff;
    margin-bottom: 20px;
    animation: flicker 3s infinite;
  }

  @keyframes flicker {
    0%, 100% { opacity: 1; }
    41% { opacity: 1; }
    42% { opacity: 0.8; }
    43% { opacity: 1; }
    45% { opacity: 0.9; }
    46% { opacity: 1; }
  }

  .about-text {
    color: #e5e5e5;
    font-size: 18px;
    margin-bottom: 20px;
  }

  h3 {
    font-size: 25px;
    font-style: italic;
    color: #fff;
    margin: 20px 0 15px 0;
  }

  .building-list {
    font-size: 19px;
    line-height: 1.8;
    color: #e5e5e5;
    text-align: left;
    max-width: 600px;
    margin: 0 auto;
  }

  .motto {
    font-weight: bold;
    font-size: 19px;
    margin-top: 20px;
    color: #fff;
  }

  /* Tech Stack Section */
  .tech-section {
    margin: 60px 0;
  }

  .tech-section h2 {
    font-size: 50px;
    font-family: 'Eater', cursive;
    text-shadow: 0 0 12px #ffffff99;
  }

  .tech-icons {
    margin-top: 30px;
  }

  .tech-icons img {
    height: 90px;
    filter: drop-shadow(0 0 8px #ffffff88);
  }

  /* LeetCode Section */
  .leetcode-section {
    margin: 60px 0;
  }

  .leetcode-section h2 {
    font-size: 42px;
    font-family: 'Nosifer', cursive;
  }

  .leetcode-badge {
    display: inline-block;
    margin: 20px 10px;
    border-radius: 12px;
    box-shadow: 0 0 12px #ffffff99;
    transition: transform 0.3s ease;
  }

  .leetcode-badge:hover {
    transform: scale(1.05);
  }

  .banned-note {
    font-size: 16px;
    margin-top: 10px;
    color: #aaa;
    margin-bottom: 15px;
  }

  .banned-badges {
    display: flex;
    gap: 15px;
    justify-content: center;
    flex-wrap: wrap;
  }

  /* Connect Section */
  .connect-section {
    margin: 60px 0;
  }

  .connect-section h2 {
    font-size: 50px;
    font-family: 'Creepster', cursive;
  }

  .social-buttons {
    display: flex;
    gap: 20px;
    justify-content: center;
    flex-wrap: wrap;
    margin-top: 30px;
  }

  .social-buttons img {
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    cursor: pointer;
  }

  .social-buttons img:hover {
    transform: translateY(-3px);
    box-shadow: 0 5px 20px rgba(255,255,255,0.4);
  }

  /* Current Focus Section */
  .focus-section {
    margin: 60px 0;
  }

  .focus-section h2 {
    font-size: 45px;
    font-family: 'Georgia', serif;
    font-style: italic;
  }

  .focus-list {
    max-width: 650px;
    margin: 30px auto;
    font-size: 20px;
    font-family: 'Georgia', serif;
    color: #eaeaea;
    line-height: 2;
  }

  /* Footer Typing */
  .footer-typing {
    margin: 40px 0;
  }

  @media (max-width: 768px) {
    h1 { font-size: 45px; }
    h2 { font-size: 32px; }
    .about-box { padding: 20px; }
    .container { padding: 40px 20px; }
    .profile-img { width: 200px; }
    .tech-icons img { height: 70px; }
  }
</style>
</head>
<body>

<div class="container">
  
  <!-- Profile Image -->
  <img src="https://i.postimg.cc/SKBNcms1/Bharadwaj-removebg-preview.png" alt="Bharadwaj BN" class="profile-img">
  
  <!-- Main Name -->
  <h1>𝓑𝓱𝓪𝓻𝓪𝓭𝔀𝓪𝓳 𝓑𝓝</h1>
  
  <!-- Subtitle -->
  <p class="subtitle">𝓢𝓸𝓯𝓽𝔀𝓪𝓻𝓮 𝓔𝓷𝓰𝓲𝓷𝓮𝓮𝓻 • 𝓢𝔂𝓼𝓽𝓮𝓶 𝓓𝓮𝓼𝓲𝓰𝓷 • 𝓢𝓬𝓪𝓵𝓪𝓫𝓵𝓮 𝓑𝓪𝓬𝓴𝓮𝓷𝓭</p>
  
  <!-- Typing Effect -->
  <div class="typing-container">
    <img src="https://readme-typing-svg.herokuapp.com?color=FFFFFF&center=true&vCenter=true&width=900&height=45&lines=⚡+Backend+Architect+⚡;👁️‍🗨️+System+Design+Specialist+👁️‍🗨️;🔥+Full+Stack+Developer+🔥;💀+Clean+Architecture+Mindset+💀;⚔️+Competitive+Programmer+⚔️" alt="Typing Animation">
  </div>
  
  <!-- About Me Section -->
  <div class="about-box">
    <h2>𝕬𝖇𝖔𝖚𝖙 𝕸𝖊 👁️</h2>
    <p class="about-text">
      I build <strong>high-performance backend systems</strong>,<br>
      design <strong>clean engineering architectures</strong>,<br>
      and craft <strong>future-ready software</strong> with a blend of<br>
      <strong style="color:#fff;">elegance, logic, and pure engineering energy</strong>.
    </p>
    
    <h3>𝓘 𝓮𝓷𝓳𝓸𝔂 𝓫𝓾𝓲𝓵𝓭𝓲𝓷𝓰:</h3>
    
    <div class="building-list">
      ✨ 𝓢𝔂𝓼𝓽𝓮𝓶-𝓵𝓮𝓿𝓮𝓵 𝓑𝓪𝓬𝓴𝓮𝓷𝓭 𝓐𝓻𝓬𝓱𝓲𝓽𝓮𝓬𝓽𝓾𝓻𝓮𝓼<br>
      ✨ 𝓕𝓾𝓵𝓵-𝓼𝓽𝓪𝓬𝓴 𝓜𝓸𝓭𝓮𝓻𝓷 𝓤𝓘𝓼<br>
      ✨ 𝓝𝓮𝓸𝓶𝓸𝓻𝓹𝓱𝓲𝓬 𝓕𝓾𝓽𝓾𝓻𝓲𝓼𝓽𝓲𝓬 𝓤𝓧<br>
      ✨ 𝓒𝓵𝓮𝓪𝓷, 𝓞𝓹𝓽𝓲𝓶𝓲𝔃𝓮𝓭 & 𝓣𝓮𝓼𝓽𝓪𝓫𝓵𝓮 𝓒𝓸𝓭𝓮
    </div>
    
    <div class="motto">
      💫 𝓐𝓵𝔀𝓪𝔂𝓼 𝓲𝓶𝓹𝓻𝓸𝓿𝓲𝓷𝓰.<br>
      💫 𝓐𝓵𝔀𝓪𝔂𝓼 𝓵𝓮𝓪𝓻𝓷𝓲𝓷𝓰.<br>
      💫 𝓐𝓵𝔀𝓪𝔂𝓼 𝓫𝓾𝓲𝓵𝓭𝓲𝓷𝓰.
    </div>
  </div>
  
  <!-- Tech Stack Section -->
  <div class="tech-section">
    <h2>🌀 𝕿𝖊𝖈𝖍 𝕾𝖙𝖆𝖈𝖐 🌀</h2>
    <div class="tech-icons">
      <img src="https://skillicons.dev/icons?i=java,python,js,ts,react,angular,spring,django,fastapi,postgres,mysql,mongodb,docker,git,githubactions,vercel" alt="Tech Stack">
    </div>
  </div>
  
  <!-- LeetCode Section -->
  <div class="leetcode-section">
    <h2>💀 𝕷𝖊𝖊𝖙𝕮𝖔𝖉𝖊 𝕻𝖗𝖔𝖋𝖎𝖑𝖊𝖘 💀</h2>
    
    <a href="https://leetcode.com/u/mbbn/" class="leetcode-badge">
      <img src="https://img.shields.io/badge/ACTIVE_PROFILE-000?style=for-the-badge&logo=leetcode&logoColor=white" alt="Active LeetCode Profile">
    </a>
    
    <p class="banned-note">Past accounts (banned for AI usage — transparency 🩶)</p>
    
    <div class="banned-badges">
      <a href="https://leetcode.com/u/Manu-Bharadwaj-BN/">
        <img src="https://img.shields.io/badge/Account_1-111?style=for-the-badge&logo=leetcode&logoColor=white" alt="Account 1">
      </a>
      <a href="https://leetcode.com/u/manubn/">
        <img src="https://img.shields.io/badge/Account_2-111?style=for-the-badge&logo=leetcode&logoColor=white" alt="Account 2">
      </a>
      <a href="https://leetcode.com/u/the_bharadwaj/">
        <img src="https://img.shields.io/badge/Account_3-111?style=for-the-badge&logo=leetcode&logoColor=white" alt="Account 3">
      </a>
    </div>
  </div>
  
  <!-- Connect Section -->
  <div class="connect-section">
    <h2>🌐 𝓒𝓸𝓷𝓷𝓮𝓬𝓽 𝓦𝓲𝓽𝓱 𝓜𝓮</h2>
    <div class="social-buttons">
      <a href="https://www.linkedin.com/in/manu-bharadwaj-3507a345/">
        <img src="https://img.shields.io/badge/LinkedIn-000?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
      </a>
      <a href="https://youtube.com/@code-with-Bharadwaj">
        <img src="https://img.shields.io/badge/YouTube-000?style=for-the-badge&logo=youtube&logoColor=white" alt="YouTube">
      </a>
      <a href="https://manu-bharadwaj-portfolio.vercel.app/portfolio">
        <img src="https://img.shields.io/badge/Portfolio-000?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio">
      </a>
      <a href="https://github.com/Manu577228">
        <img src="https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
      </a>
    </div>
  </div>
  
  <!-- Current Focus Section -->
  <div class="focus-section">
    <h2>✨ 𝓒𝓾𝓻𝓻𝓮𝓷𝓽 𝓕𝓸𝓬𝓾𝓼</h2>
    <div class="focus-list">
      💠 𝓢𝓬𝓪𝓵𝓪𝓫𝓵𝓮 𝓑𝓪𝓬𝓴𝓮𝓷𝓭 𝓢𝔂𝓼𝓽𝓮𝓶𝓼<br>
      💠 𝓒𝓵𝓮𝓪𝓷 𝓐𝓻𝓬𝓱𝓲𝓽𝓮𝓬𝓽𝓾𝓻𝓮<br>
      💠 𝓗𝓛𝓓 + 𝓛𝓛𝓓<br>
      💠 𝓕𝓾𝓵𝓵 𝓢𝓽𝓪𝓬𝓴<br>
      💠 𝓢𝔂𝓼𝓽𝓮𝓶 𝓓𝓮𝓼𝓲𝓰𝓷
    </div>
  </div>
  
  <!-- Footer Typing -->
  <div class="footer-typing">
    <img src="https://readme-typing-svg.herokuapp.com?color=FFFFFF&center=true&vCenter=true&width=850&height=45&lines=⚡+𝙁𝙪𝙩𝙪𝙧𝙚-𝙍𝙚𝙖𝙙𝙮+•+𝙉𝙚𝙤𝙣+𝙀𝙣𝙜𝙞𝙣𝙚𝙚𝙧𝙞𝙣𝙜+⚡" alt="Footer Animation">
  </div>
  
</div>

</body>
</html>


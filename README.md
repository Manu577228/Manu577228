<div align="center">

<img src="assets/banner.svg" width="100%" alt="Manu Bharadwaj - Full-Stack Engineer, LeetCode Global Rank 41"/>

<a href="https://github.com/Manu577228">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=21&pause=1200&color=FF4F8B&center=true&vCenter=true&width=820&lines=Protagonist+class%3A+Full-Stack+Engineer;I+ship+React+%2B+Spring+Boot+apps+that+survive+200+users;Power+level%3A+LeetCode+Global+Rank+41;Training+arc%3A+teaching+DSA+to+3.32K+students;Next+quest%3A+joining+YOUR+team" alt="Typing animation"/>
</a>

<br/>

[![Portfolio](https://img.shields.io/badge/PORTFOLIO-Live%20Projects-ff4f8b?style=for-the-badge&logo=vercel&logoColor=white)](https://manu-bharadwaj-portfolio.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LINKEDIN-Let's%20Talk-4de1ff?style=for-the-badge&logo=linkedin&logoColor=black)](https://www.linkedin.com/in/manu-bharadwaj-3507a345)
[![Email](https://img.shields.io/badge/EMAIL-Hire%20Me-ff4f8b?style=for-the-badge&logo=gmail&logoColor=white)](mailto:bnmanubharadwaj@gmail.com)
[![YouTube](https://img.shields.io/badge/YOUTUBE-@code--with--Bharadwaj-4de1ff?style=for-the-badge&logo=youtube&logoColor=black)](https://www.youtube.com/@code-with-Bharadwaj)

[![LeetCode](https://img.shields.io/badge/LEETCODE-Rank%2041-ffa116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/mbbn/)
[![LeetCode JS](https://img.shields.io/badge/LEETCODE%20JS-Previous%20Account-555555?style=for-the-badge&logo=leetcode&logoColor=ffa116)](https://leetcode.com/u/Manu-Bharadwaj-BN/)
[![Codeforces](https://img.shields.io/badge/CODEFORCES-MBBN--AC-1f8acb?style=for-the-badge&logo=codeforces&logoColor=white)](https://codeforces.com/profile/MBBN-AC)

<img src="assets/divider.svg" width="100%" alt=""/>

</div>

## Prologue: The 10-Second Pitch

> **Recruiters: if you only read one section, read this one.**

| You need someone who... | Here's the proof |
|:--|:--|
| **Ships real products** | 30 full-stack projects built, the best 12 live on my [portfolio](https://manu-bharadwaj-portfolio.vercel.app) |
| **Builds things that don't fall over** | k6 tested on live deployments: **0% failures up to 200 concurrent users**, p95 latency **427 ms** |
| **Has real industry experience** | **2.5 years** across Fractal Analytics, Allstate India and TechChef's Software |
| **Has delivered for big-name clients** | Built for **Dell, Intuit and JPMC** at TechChef's Software, and enterprise reporting platforms at **Allstate India** |
| **Is technically elite** | LeetCode **Best Global Rank 41**, **800+** problems solved |
| **Communicates and mentors** | **3.32K** YouTube subscribers, **~2,000** videos on DSA, CP and System Design |
| **Speaks your team's language** | English · हिन्दी · ಕನ್ನಡ |
| **Thinks in systems** | **50** LLD + **10** HLD designs open-sourced, each with a video walkthrough |

<div align="center">

### 📬 **[bnmanubharadwaj@gmail.com](mailto:bnmanubharadwaj@gmail.com)**
*Replies fast. Interviews gladly.*

<img src="assets/divider.svg" width="100%" alt=""/>

</div>

## Chapter 1: Character Sheet

<div align="center">

<img src="assets/character-sheet.svg" width="100%" alt="Character sheet showing problem solving, system design, full-stack build, performance and teaching stats"/>

<sub>Bars are a stylised view of the real numbers beside them. The numbers are what count.</sub>

<img src="assets/divider.svg" width="100%" alt=""/>

</div>

## Chapter 2: Passive Skills (Why Teams Hire Me and Keep Me)

<table>
<tr>
<td width="33%" valign="top">

### ⚔️ Full-Stack Combo
Frontend, backend, database, auth, deployment and load testing. I deliver a working, deployed, measured result, not a half-built feature.

</td>
<td width="33%" valign="top">

### 🧠 Strategist Mind
Years of explaining algorithms and design problems on camera taught me to split big problems into clean parts. I design first, weigh trade-offs, then build.

</td>
<td width="33%" valign="top">

### 🤝 Party Support
I write things down, explain things clearly and help people get unstuck. Teaching about 2,000 videos' worth of material is a habit I bring to code reviews and onboarding.

</td>
</tr>
</table>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Chapter 3: Boss Fights (Projects That Run in Production)

> Not demos that live on my laptop. Deployed, load-tested and documented.

### 👹 Boss 1: Expense Splitter (Group Expense Platform)
`React 19` `Django REST Framework` `PostgreSQL` `JWT` `RBAC` `Material UI` `k6` `Vercel` `Render` `Neon`

Splits bills so friendships survive dinner. Built during my **Fractal Analytics** internship.

- **13 REST endpoints** (9 for groups, members, expenses and summaries, plus 4 for auth), deployed across **3 cloud services**
- **Equal and custom split modes** with server-side validation (minimum 2 members, valid membership, full coverage, amounts summing within INR 0.01)
- **JWT auth** (SimpleJWT login, registration, refresh) with **RBAC** on every route
- Responsive Material UI frontend with 4 views: dashboard, expense form, expense list, balance summary

<details>
<summary><b>⚔️ Battle log: k6 results (click to expand)</b></summary>

<br/>

| Test | Setup | Result |
|:--|:--|:--|
| **Load test** | 5 min, 50 concurrent users, 5 read endpoints | 41,127 requests, **0% failures**, 137 req/s, 17 ms average, **48 ms p95** |
| **Stress test** | 6 min, ramp to 200 users (+300%) | 101,002 requests, **0% failures**, throughput up 105% to 280 req/s, **p95 427 ms** (14% under the 500 ms target) |

Result: gradual degradation under pressure, never failure.

</details>

### 👹 Boss 2: URL Shortener (Bharadwaj.ly)
`Spring Boot` `React + Vite` `PostgreSQL` `JWT` `Docker` `Tailwind` `Material UI` `k6`

Because long URLs are a cry for help.

- Clean **Controller → Service → Repository** backend (Spring Data JPA, Hibernate) with **stateless JWT auth** via a custom Spring Security filter, role claim and 48-hour expiry
- **Dockerized**, 7 environment variables, **zero hardcoded secrets**, CORS restricted to 1 origin
- REST APIs for registration, login, **8-character short codes**, link listing and public **HTTP 302 redirects**
- Deployed across Vercel, Render and Neon

<details>
<summary><b>⚔️ Battle log: k6 results (click to expand)</b></summary>

<br/>

Load tested on the **live deployment** (Render free tier, from India, 3 runs, about 9 minutes):

- **6,329 requests, 99.95% success**, 12,013 of 12,013 checks passed
- All **5,693 redirects** returned 3xx with a Location header
- Saturation point identified and documented: from 20 to 50 users, throughput rose 63% while p95 rose 158% (2.71 s at 50 users), with 0 errors
- k6 script with 5 test profiles, a 90/10 redirect-to-list mix, free-tier warm-up, p95 and error-rate thresholds, and a setup step that logs in, seeds a short URL and verifies its redirect

</details>

### 🗡️ Side Quests: 30 Full-Stack Projects
JWT and OTP auth systems (MrAuthy), an E-Shop with Stripe payments, AI apps and more, built mainly in React with Next.js, Angular, Spring Boot, Django, MERN and MEAN. The 12 best are on my [**portfolio**](https://manu-bharadwaj-portfolio.vercel.app).

<details>
<summary><b>🔍 My checklist for every project (click to expand)</b></summary>

<br/>

1. **Design first:** layered architecture, clear boundaries, no spaghetti.
2. **Secure by default:** JWT, RBAC, server-side validation, no secrets in code.
3. **Ship it:** every project is deployed so you can click it, not just read about it.
4. **Measure it:** k6 load and stress tests with real numbers and documented limits.
5. **Document it:** README, resume-ready write-up and live links.

</details>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Chapter 4: Story Arcs (Career Timeline)

```mermaid
timeline
    title Manu Bharadwaj: The Story So Far
    2018 : Graduated, BE from VTU
    2021 : Arc 1 at Fidelitus Corp
         : Reusable React components and secure auth flows
    2021-2022 : Arc 2 at TechChef's Software
              : React Micro Frontends, QuickBooks GraphQL modules
              : Clients: Dell, Intuit, JPMC
    2022-2023 : Arc 3 at Allstate India
              : Enterprise React reporting platforms, CI/CD gates
    2025 : Arc 4 at Fractal Analytics
         : Shipped a load-tested expense platform end to end
    2026 : Expense Splitter and URL Shortener load-tested live
```

### 🏯 Guild History

**🔹 Full Stack Engineering Intern · Fractal Analytics** · Jul 2025 – Oct 2025
Delivered the Expense Splitter platform from design to deployment: 13 REST endpoints, JWT and RBAC, 3 cloud services, stress tested to 200 concurrent users with 0% failures.

**🔹 Software Engineer · Allstate India** · Nov 2022 – Mar 2023
Built enterprise React reporting platforms for global stakeholders, bringing analytics and data-visualization workflows into one place and removing manual reporting and duplicate data pipelines. Strengthened CI/CD with pre-merge validation gates and deployment health checks, which cut rollbacks and sped up releases.

**🔹 Consultant · TechChef's Software** · Sep 2021 – Nov 2022 · *Clients: Dell, Intuit, JPMC*
Architected a React Micro Frontend system so teams could deploy independently, removing release coupling and cutting deploy times. Built QuickBooks-integrated React and GraphQL modules, replacing over-fetching REST calls with schema-driven queries. Set up Jest and Enzyme from scratch and shipped WCAG-compliant, cross-browser UIs.

**🔹 Executive IT · Fidelitus Corp** · Jan 2021 – Jul 2021
Built reusable React components that enforced design-system conventions across internal enterprise platforms, and secure authentication flows.

**🎓 Education:** Bachelor of Engineering, Visvesvaraya Technological University (2018)

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Chapter 5: Skill Scrolls (Tech Arsenal)

<table>
<tr><td><b>⚡ Languages</b></td><td>

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)

</td></tr>
<tr><td><b>🎨 Frontend</b></td><td>

![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat-square&logo=angular&logoColor=white)
![Jest](https://img.shields.io/badge/Jest-C21325?style=flat-square&logo=jest&logoColor=white)
![Micro Frontends](https://img.shields.io/badge/Micro%20Frontends-555555?style=flat-square)

</td></tr>
<tr><td><b>⚙️ Backend</b></td><td>

![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=flat-square&logo=graphql&logoColor=white)

</td></tr>
<tr><td><b>🗄️ Databases & DevOps</b></td><td>

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![MS SQL](https://img.shields.io/badge/MS%20SQL-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
![AWS](https://img.shields.io/badge/AWS%20EC2-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![k6](https://img.shields.io/badge/k6-7D64FF?style=flat-square&logo=k6&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

</td></tr>
<tr><td><b>📜 Core Concepts</b></td><td>Data Structures · Algorithms · Low-Level Design · High-Level Design · System Design · OOP · REST APIs · Microservices · CI/CD · Performance Testing</td></tr>
</table>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Chapter 6: Rival Board (Competitive Programming)

> Strong fundamentals aren't a slogan here. They're ranked.

<div align="center">

### 🥇 Main account: [mbbn](https://leetcode.com/u/mbbn/) · Java, Python · Best Global Rank 41

[![LeetCode stats mbbn](https://leetcard.jacoblin.cool/mbbn?theme=dark&font=Karma&ext=contest)](https://leetcode.com/u/mbbn/)

[![LeetCode heatmap mbbn](https://leetcard.jacoblin.cool/mbbn?theme=dark&font=Karma&ext=heatmap)](https://leetcode.com/u/mbbn/)

### 🥈 Previous account: [Manu-Bharadwaj-BN](https://leetcode.com/u/Manu-Bharadwaj-BN/) · JavaScript

[![LeetCode stats Manu-Bharadwaj-BN](https://leetcard.jacoblin.cool/Manu-Bharadwaj-BN?theme=dark&font=Karma&ext=contest)](https://leetcode.com/u/Manu-Bharadwaj-BN/)

[![LeetCode heatmap Manu-Bharadwaj-BN](https://leetcard.jacoblin.cool/Manu-Bharadwaj-BN?theme=dark&font=Karma&ext=heatmap)](https://leetcode.com/u/Manu-Bharadwaj-BN/)

<sub>Cards refresh automatically after every contest.</sub>

</div>

**What this means for your team:** I can break down unfamiliar problems under time pressure, choose the right data structure and write clean, correct code on the first pass.

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Chapter 7: Sacred Scrolls (Open Source)

| Repo | What's inside | Languages |
|:--|:--|:--|
| 🏗️ [**50 LLD Problems Solved**](https://github.com/Manu577228/50-LLD-Problems-Solved) | 50 low-level design problems, each explained on YouTube | Java, Python |
| 🌐 [**Important HLD Problems**](https://github.com/Manu577228/Important-HLD-Problems) | 10 system design classics: WhatsApp, Uber, TinyURL, Dream11, Zomato and more | Design docs |
| 🧠 [**CP Core Algorithms 150**](https://github.com/Manu577228/CP-Core-Algorithms-150) | 150 advanced algorithms, plus 25+ extreme ones on niche topics | Java, Python |

Every repo ships with a video walkthrough, because code that teaches is worth more than code that merely exists.

## Chapter 8: Training Arc (I Teach This Stuff Too)

<div align="center">

[![YouTube](https://img.shields.io/badge/WATCH-@code--with--Bharadwaj-ff4f8b?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/@code-with-Bharadwaj)

**3.32K subscribers · ~2,000 videos · Java, Python and JavaScript series**

</div>

DSA, competitive programming, advanced algorithms and system design, explained in plain language for beginners and interview candidates.

**Why that matters to an employer:** explaining Dijkstra without anyone crying is the same skill as explaining your codebase to a new teammate, writing a clear design doc or mentoring a junior engineer.

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Chapter 9: Status Window (GitHub Activity)

<div align="center">

![Manu's GitHub stats](https://github-readme-stats.vercel.app/api?username=Manu577228&show_icons=true&theme=radical&hide_border=true)
![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Manu577228&layout=compact&theme=radical&hide_border=true)

![Streak](https://streak-stats.demolab.com?user=Manu577228&theme=radical&hide_border=true)

![Activity graph](https://github-readme-activity-graph.vercel.app/graph?username=Manu577228&theme=react-dark&hide_border=true&area=true&color=ff4f8b&line=4de1ff&point=ffffff)

</div>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Chapter 10: The Hiring Quest Route

```mermaid
flowchart LR
    A([You: Hiring Manager]) --> B[Email me]
    B --> C{Interview rounds}
    C -->|DSA round| D[Solve it live]
    C -->|System design| E[LLD and HLD ready]
    C -->|Project deep dive| F[Live demos and k6 reports]
    D --> G([Offer])
    E --> G
    F --> G
    style A fill:#ff4f8b,stroke:#ffffff,color:#ffffff
    style G fill:#4de1ff,stroke:#ffffff,color:#000000
```

## 📜 Scroll of Answers (Recruiter FAQ)

<details>
<summary><b>What roles am I looking for?</b></summary>
<br/>
Software Engineer / SDE roles where I can build scalable full-stack products, own features end to end and keep growing in system design.
</details>

<details>
<summary><b>Can I work across the stack?</b></summary>
<br/>
Yes. React, Next.js and Angular on the frontend. Spring Boot, Django, FastAPI and Node.js on the backend. PostgreSQL, MySQL, MongoDB and MS SQL for data. Docker, Jenkins and AWS EC2 for delivery.
</details>

<details>
<summary><b>Do I have experience with large clients and enterprise codebases?</b></summary>
<br/>
Yes. I built enterprise React platforms at Allstate India and delivered work for Dell, Intuit and JPMC through TechChef's Software.
</details>

<details>
<summary><b>How do I handle quality and performance?</b></summary>
<br/>
I test, then measure. My recent projects were load and stress tested with k6 on live deployments, with results and limits documented.
</details>

<details>
<summary><b>Will I be good in a team?</b></summary>
<br/>
I've worked with teams at Fractal Analytics, Allstate India and TechChef's Software, delivering for clients like Dell, Intuit and JPMC. I also spend my free time teaching thousands of developers, so clear communication and helping others is second nature.
</details>

<details>
<summary><b>What's the fastest way to reach me?</b></summary>
<br/>
Email <b>bnmanubharadwaj@gmail.com</b> or message me on <a href="https://www.linkedin.com/in/manu-bharadwaj-3507a345">LinkedIn</a>.
</details>

<div align="center">

<br/>

## ⚔️ Join My Party

### I'm open to SDE roles. Send me a problem. I'll send back a solution, a deployment and a load test.

**ನಮಸ್ಕಾರ · नमस्ते · Hello**

*ನಿಮ್ಮ ಸಂದೇಶಕ್ಕಾಗಿ ಕಾಯುತ್ತಿದ್ದೇನೆ · आपके संदेश की प्रतीक्षा रहेगी · Write to me in any of the three.*

[![Email me](https://img.shields.io/badge/EMAIL-bnmanubharadwaj@gmail.com-ff4f8b?style=for-the-badge&logo=gmail&logoColor=white)](mailto:bnmanubharadwaj@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LINKEDIN-Connect%20with%20me-4de1ff?style=for-the-badge&logo=linkedin&logoColor=black)](https://www.linkedin.com/in/manu-bharadwaj-3507a345)
[![Portfolio](https://img.shields.io/badge/PORTFOLIO-See%20my%20work-ff4f8b?style=for-the-badge&logo=vercel&logoColor=white)](https://manu-bharadwaj-portfolio.vercel.app)

<sub>*Time complexity of replying to recruiters: O(1). Space complexity of my coffee consumption: unbounded.* ☕</sub>

<br/>

<img src="assets/footer.svg" width="100%" alt="Contact Manu Bharadwaj"/>

</div>
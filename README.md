<div align="center">

<img src="assets/banner.svg" width="100%" alt="Manu Bharadwaj, Full-Stack Engineer, problem solver and teacher"/>

<a href="https://github.com/Manu577228"><img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=18&duration=3200&pause=1100&color=A5B4FC&center=true&vCenter=true&width=640&lines=I+build+full-stack+things.;I+load-test+them+for+fun.;I+solve+problems+on+LeetCode.;Then+I+teach+them+on+YouTube." alt="Typing animation"/></a>

<br/>

[![Email](https://img.shields.io/badge/Email-14182a?style=for-the-badge&logo=gmail&logoColor=c4b5fd)](mailto:bnmanubharadwaj@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-14182a?style=for-the-badge&logo=linkedin&logoColor=67e8f9)](https://www.linkedin.com/in/manu-bharadwaj-3507a345)
[![Portfolio](https://img.shields.io/badge/Portfolio-14182a?style=for-the-badge&logo=vercel&logoColor=f9a8d4)](https://manu-bharadwaj-portfolio.vercel.app)
[![YouTube](https://img.shields.io/badge/YouTube-14182a?style=for-the-badge&logo=youtube&logoColor=fda4af)](https://www.youtube.com/@code-with-Bharadwaj)
[![LeetCode](https://img.shields.io/badge/LeetCode-14182a?style=for-the-badge&logo=leetcode&logoColor=fcd34d)](https://leetcode.com/u/mbbn/)

<br/>

<a href="#about">About</a> &nbsp;·&nbsp;
<a href="#journey">Journey</a> &nbsp;·&nbsp;
<a href="#built-and-broken">Projects</a> &nbsp;·&nbsp;
<a href="#toolkit">Toolkit</a> &nbsp;·&nbsp;
<a href="#leetcode">LeetCode</a> &nbsp;·&nbsp;
<a href="#open-source">Open Source</a> &nbsp;·&nbsp;
<a href="#youtube">YouTube</a> &nbsp;·&nbsp;
<a href="#contact">Contact</a>

<br/><br/>

<img src="assets/snapshot.svg" width="100%" alt="Key numbers: LeetCode global rank 41, 800+ problems solved, 30 projects shipped, 0% failures at 200 users, 3K+ subscribers"/>

</div>

<!-- Subscriber and video counts are rounded down on purpose. They change faster than this file does. -->

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<a id="about"></a>

## ✦ About

I'm a full-stack engineer with 2.5 years of experience, a soft spot for hard problems, and a habit of explaining everything I learn out loud. Mostly on camera. Sometimes to a rubber duck.

```java
public class Manu implements Engineer, Teacher {

    String  role     = "Full-Stack Engineer";
    String  frontend = "React, TypeScript, Micro Frontends";
    String  backend  = "Spring Boot, Django";
    String  leetcode = "Best global rank 41, 800+ solved";
    String  youtube  = "3K+ subscribers, 1.9K+ videos";
    boolean loadTestsEverything = true;
    boolean worksOnMyMachine    = false;   // it works on Render's machine

    public void today() {
        build();
        breakIt();      // k6 does the honest part
        fix();
        teachIt();      // the best code review there is
    }
}
```

> *This page is not a resume. The resume behaves itself. This is the version of me that tells you what I actually like building.*

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<a id="journey"></a>

## ✦ Journey

| | Chapter | The short story |
|:--:|:--|:--|
| **01** | **React, a lot of it** | Started in 2021 at Fidelitus building reusable components for internal enterprise platforms. Then TechChef's Software, with projects for **Dell, Intuit and JPMC**: a Micro Frontend architecture so teams could deploy independently, QuickBooks-integrated modules on GraphQL, and Jest and Enzyme testing from scratch. |
| **02** | **Enterprise scale** | At **Allstate India** I built React reporting platforms for global stakeholders and tightened CI/CD with pre-merge validation gates and deployment health checks. Fewer rollbacks, calmer Fridays. |
| **03** | **The deep end** | Stepped back from frontend-heavy work and went full-stack on purpose: personal projects in Java and Python, LeetCode in Java, and everything I learned turned into YouTube videos. |
| **04** | **Shipping for real** | As a Full Stack Engineering Intern at **Fractal Analytics**, I took Expense Splitter from design to deployment: 13 REST endpoints, JWT with role-based access control, three cloud services and a stress test that never blinked. |

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<a id="built-and-broken"></a>

## ✦ Built and Broken

I build things, then I try to break them with k6. The numbers below are from live deployments, not localhost.

<table>
<tr>
<td width="50%" valign="top">

### Expense Splitter
*Because "I'll pay you back" needs a database.*

`React 19` `Django REST` `PostgreSQL` `JWT` `RBAC` `Material UI` `k6`

Built during my Fractal Analytics internship, deployed across Vercel, Render and Neon.

- 13 REST endpoints: 9 for groups, members, expenses and summaries, 4 for auth
- Equal and custom splits with server-side validation: minimum 2 members, valid membership, full coverage, amounts within INR 0.01
- JWT (SimpleJWT login, registration, refresh) and RBAC on every route
- Four views: dashboard, expense form, expense list, balance summary

</td>
<td width="50%" valign="top">

### Bharadwaj.ly
*A URL shortener with opinions.*

`Spring Boot` `React + Vite` `PostgreSQL` `JWT` `Docker` `Tailwind` `k6`

Deployed across Vercel, Render and Neon.

- Controller, Service, Repository layers with stateless JWT through a custom Spring Security filter, role claim and 48-hour expiry
- Dockerized, 7 environment variables, zero hardcoded secrets, CORS locked to one origin
- 8-character short codes and public HTTP 302 redirects
- k6 script with 5 profiles, a 90/10 redirect-to-list mix, free-tier warm-up and thresholds

</td>
</tr>
</table>

<details>
<summary><b>Show me the load tests</b></summary>

<br/>

**Expense Splitter**

| Test | Setup | Result |
|:--|:--|:--|
| Load | 5 min, 50 concurrent users, 5 read endpoints | 41,127 requests, 0% failures, 137 req/s, 17 ms average, 48 ms p95 |
| Stress | 6 min, ramp to 200 users (+300%) | 101,002 requests, 0% failures, throughput up 105% to 280 req/s, p95 427 ms (14% under the 500 ms target) |

Verdict: gradual degradation under pressure, never failure. Like a good friend splitting a dinner bill.

**Bharadwaj.ly** (live on the Render free tier, tested from India, 3 runs, about 9 minutes)

| Metric | Result |
|:--|:--|
| Requests | 6,329 at 99.95% success |
| Checks | 12,013 of 12,013 passed, including all 5,693 redirects returning 3xx with a Location header |
| Saturation | From 20 to 50 users, throughput rose 63% while p95 rose 158% (2.71 s at 50 users), with 0 errors |

Verdict: I found the saturation point and wrote it down instead of hiding it. The free tier asked politely for a break. It never crashed.

</details>

<br/>

**And 30 full-stack projects in total.** JWT and OTP authentication systems (MrAuthy), an E-Shop with Stripe payments, AI apps and more, built across React, Next.js, Spring Boot, Django, MERN and MEAN, with Angular in personal projects. The 12 best live on my [portfolio](https://manu-bharadwaj-portfolio.vercel.app). The other 18 are on GitHub, quietly judging me.

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<a id="toolkit"></a>

## ✦ Toolkit

**Languages**
&nbsp;![Java](https://img.shields.io/badge/Java-14182a?style=flat-square&logo=openjdk&logoColor=fda4af)
![Python](https://img.shields.io/badge/Python-14182a?style=flat-square&logo=python&logoColor=fcd34d)
![JavaScript](https://img.shields.io/badge/JavaScript-14182a?style=flat-square&logo=javascript&logoColor=fcd34d)
![TypeScript](https://img.shields.io/badge/TypeScript-14182a?style=flat-square&logo=typescript&logoColor=67e8f9)
![HTML](https://img.shields.io/badge/HTML-14182a?style=flat-square&logo=html5&logoColor=fda4af)
![CSS](https://img.shields.io/badge/CSS-14182a?style=flat-square&logo=css3&logoColor=67e8f9)

**Frontend**
&nbsp;![React](https://img.shields.io/badge/React-14182a?style=flat-square&logo=react&logoColor=67e8f9)
![Next.js](https://img.shields.io/badge/Next.js-14182a?style=flat-square&logo=nextdotjs&logoColor=white)
![Micro Frontends](https://img.shields.io/badge/Micro_Frontends-14182a?style=flat-square&logoColor=white)
![Jest](https://img.shields.io/badge/Jest-14182a?style=flat-square&logo=jest&logoColor=f9a8d4)
![Enzyme](https://img.shields.io/badge/Enzyme-14182a?style=flat-square&logoColor=white)
![Angular](https://img.shields.io/badge/Angular_(personal_projects)-14182a?style=flat-square&logo=angular&logoColor=fda4af)

**Backend**
&nbsp;![Spring Boot](https://img.shields.io/badge/Spring_Boot-14182a?style=flat-square&logo=springboot&logoColor=6ee7b7)
![Django](https://img.shields.io/badge/Django-14182a?style=flat-square&logo=django&logoColor=6ee7b7)
![FastAPI](https://img.shields.io/badge/FastAPI-14182a?style=flat-square&logo=fastapi&logoColor=6ee7b7)
![Node.js](https://img.shields.io/badge/Node.js-14182a?style=flat-square&logo=nodedotjs&logoColor=6ee7b7)
![Express](https://img.shields.io/badge/Express.js-14182a?style=flat-square&logo=express&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-14182a?style=flat-square&logo=graphql&logoColor=f9a8d4)
![REST](https://img.shields.io/badge/REST_APIs-14182a?style=flat-square&logoColor=white)
![Microservices](https://img.shields.io/badge/Microservices-14182a?style=flat-square&logoColor=white)

**Databases**
&nbsp;![PostgreSQL](https://img.shields.io/badge/PostgreSQL-14182a?style=flat-square&logo=postgresql&logoColor=67e8f9)
![MySQL](https://img.shields.io/badge/MySQL-14182a?style=flat-square&logo=mysql&logoColor=67e8f9)
![MS SQL](https://img.shields.io/badge/MS_SQL-14182a?style=flat-square&logo=microsoftsqlserver&logoColor=fda4af)
![MongoDB](https://img.shields.io/badge/MongoDB-14182a?style=flat-square&logo=mongodb&logoColor=6ee7b7)

**DevOps and Testing**
&nbsp;![Docker](https://img.shields.io/badge/Docker-14182a?style=flat-square&logo=docker&logoColor=67e8f9)
![Jenkins](https://img.shields.io/badge/Jenkins-14182a?style=flat-square&logo=jenkins&logoColor=fda4af)
![AWS EC2](https://img.shields.io/badge/AWS_EC2-14182a?style=flat-square&logo=amazonwebservices&logoColor=fcd34d)
![Git](https://img.shields.io/badge/Git-14182a?style=flat-square&logo=git&logoColor=fda4af)
![CI/CD](https://img.shields.io/badge/CI%2FCD-14182a?style=flat-square&logoColor=white)
![k6](https://img.shields.io/badge/k6-14182a?style=flat-square&logo=k6&logoColor=c4b5fd)

**Core Concepts**
&nbsp;![DSA](https://img.shields.io/badge/Data_Structures_%26_Algorithms-14182a?style=flat-square&logoColor=white)
![LLD](https://img.shields.io/badge/Low--Level_Design-14182a?style=flat-square&logoColor=white)
![HLD](https://img.shields.io/badge/High--Level_Design-14182a?style=flat-square&logoColor=white)
![OOP](https://img.shields.io/badge/OOP-14182a?style=flat-square&logoColor=white)

**AI-Assisted Development**
&nbsp;![ChatGPT](https://img.shields.io/badge/ChatGPT-14182a?style=flat-square&logo=openai&logoColor=6ee7b7)
![Gemini](https://img.shields.io/badge/Gemini-14182a?style=flat-square&logo=googlegemini&logoColor=c4b5fd)
![Claude](https://img.shields.io/badge/Claude-14182a?style=flat-square&logo=anthropic&logoColor=fcd34d)
![Copilot](https://img.shields.io/badge/Copilot-14182a?style=flat-square&logo=githubcopilot&logoColor=white)
![Pieces](https://img.shields.io/badge/Pieces-14182a?style=flat-square&logoColor=white)
![Gamma](https://img.shields.io/badge/Gamma-14182a?style=flat-square&logoColor=white)

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<a id="leetcode"></a>

## ✦ LeetCode

Two accounts, one slightly obsessive habit. The main account is where Java and Python live. The previous one preserves my JavaScript days.

<table align="center">
<tr>
<td align="center"><b>Main</b> · <a href="https://leetcode.com/u/mbbn/">mbbn</a><br/><sub>Java, Python · Best Global Rank 41</sub></td>
<td align="center"><b>Previous</b> · <a href="https://leetcode.com/u/Manu-Bharadwaj-BN/">Manu-Bharadwaj-BN</a><br/><sub>JavaScript</sub></td>
</tr>
<tr>
<td><a href="https://leetcode.com/u/mbbn/"><img src="https://leetcard.jacoblin.cool/mbbn?theme=dark&ext=contest" width="100%" alt="LeetCode stats for mbbn"/></a></td>
<td><a href="https://leetcode.com/u/Manu-Bharadwaj-BN/"><img src="https://leetcard.jacoblin.cool/Manu-Bharadwaj-BN?theme=dark&ext=contest" width="100%" alt="LeetCode stats for Manu-Bharadwaj-BN"/></a></td>
</tr>
<tr>
<td><a href="https://leetcode.com/u/mbbn/"><img src="https://leetcard.jacoblin.cool/mbbn?theme=dark&ext=heatmap" width="100%" alt="LeetCode heatmap for mbbn"/></a></td>
<td><a href="https://leetcode.com/u/Manu-Bharadwaj-BN/"><img src="https://leetcard.jacoblin.cool/Manu-Bharadwaj-BN?theme=dark&ext=heatmap" width="100%" alt="LeetCode heatmap for Manu-Bharadwaj-BN"/></a></td>
</tr>
</table>

<p align="center"><sub>Cards refresh automatically after every contest. The green squares are not decorative.</sub></p>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<a id="open-source"></a>

## ✦ Open Source

Design and algorithms, out loud. Every repo below is explained on YouTube, so you can read the code, watch the walkthrough, or do both and pretend it was easy.

| Repository | What's inside | Languages |
|:--|:--|:--|
| **[50 LLD Problems Solved](https://github.com/Manu577228/50-LLD-Problems-Solved)** | 50 low-level design problems, each explained on YouTube | Java, Python |
| **[Important HLD Problems](https://github.com/Manu577228/Important-HLD-Problems)** | 10 system design classics: WhatsApp, Uber, TinyURL, Dream11, Zomato and more | Design docs |
| **[CP Core Algorithms 150](https://github.com/Manu577228/CP-Core-Algorithms-150)** | 150 advanced algorithms and 25+ extreme algorithms on niche topics | Java, Python |

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<a id="youtube"></a>

## ✦ YouTube

[**@code-with-Bharadwaj**](https://www.youtube.com/@code-with-Bharadwaj) is where I explain DSA, competitive programming, advanced algorithms and system design, with series in Java, Python and JavaScript. That's **3K+ subscribers** and **1.9K+ videos**, and I still can't pick a favorite.

> If I can't explain it simply on camera, I don't understand it yet.

It's the same skill I bring to design docs, code reviews and onboarding.

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## ✦ GitHub Stats

<p align="center">
<img src="https://github-readme-stats.vercel.app/api?username=Manu577228&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0b0c18" height="170" alt="GitHub stats"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Manu577228&layout=compact&theme=tokyonight&hide_border=true&bg_color=0b0c18" height="170" alt="Top languages"/>
</p>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<a id="contact"></a>

## ✦ Contact

Open to Software Engineer and SDE roles, full-stack or backend. Send me a problem and I'll send back a solution, a deployment and a load test. If the problem is a bug, I'll also send back a slightly smug commit message.

<div align="center">

**[bnmanubharadwaj@gmail.com](mailto:bnmanubharadwaj@gmail.com)** &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/manu-bharadwaj-3507a345) &nbsp;·&nbsp; [Portfolio](https://manu-bharadwaj-portfolio.vercel.app) &nbsp;·&nbsp; [YouTube](https://www.youtube.com/@code-with-Bharadwaj)

<sub>Fine print: Bachelor of Engineering, Visvesvaraya Technological University, 2018.</sub>

<br/>

<img src="assets/footer.svg" width="100%" alt="Open to SDE roles. Let's build something that stays up. bnmanubharadwaj@gmail.com"/>

</div>
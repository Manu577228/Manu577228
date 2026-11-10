<div align="center">

<img src="assets/banner.svg" width="100%" alt="Manu Bharadwaj, Full-Stack Software Engineer"/>

[![Email](https://img.shields.io/badge/Email-111111?style=flat-square&logo=gmail&logoColor=white)](mailto:bnmanubharadwaj@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-111111?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/manu-bharadwaj-3507a345)
[![Portfolio](https://img.shields.io/badge/Portfolio-111111?style=flat-square&logo=vercel&logoColor=white)](https://manu-bharadwaj-portfolio.vercel.app)
[![YouTube](https://img.shields.io/badge/YouTube-111111?style=flat-square&logo=youtube&logoColor=white)](https://www.youtube.com/@code-with-Bharadwaj)
[![LeetCode](https://img.shields.io/badge/LeetCode-111111?style=flat-square&logo=leetcode&logoColor=white)](https://leetcode.com/u/mbbn/)

<img src="assets/snapshot.svg" width="100%" alt="Key numbers: LeetCode global rank 41, 800+ problems solved, 30 projects shipped, 0% failures at 200 users, 3.32K subscribers"/>

</div>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Summary

Software Engineer with 2.5 years of experience building enterprise React applications and full-stack products with React, Angular, Spring Boot, Django and the MERN stack. I have delivered work for Dell, Intuit and JPMC, and I load-test what I ship: my recent projects ran with zero failures under stress on live deployments. Outside work, I solve problems at LeetCode Global Rank 41 and teach DSA and system design to a 3.32K-subscriber YouTube audience.

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## At a Glance

| | |
|:--|:--|
| **Experience** | 2.5 years across Fractal Analytics, Allstate India, TechChef's Software and Fidelitus Corp |
| **Clients delivered for** | Dell, Intuit, JPMC |
| **Competitive coding** | LeetCode Best Global Rank 41, 800+ problems solved |
| **Performance** | k6 tested on live deployments: 0% failures up to 200 concurrent users, p95 latency 427 ms |
| **Projects** | 30 full-stack projects built, the best 12 live on my [portfolio](https://manu-bharadwaj-portfolio.vercel.app) |
| **System design** | 50 LLD and 10 HLD problems solved and open-sourced |
| **Teaching** | 3.32K subscribers, around 2,000 videos on DSA, CP and system design |
| **Looking for** | Software Engineer / SDE roles, full-stack or backend |

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Experience

**Full Stack Engineering Intern** · Fractal Analytics · *Jul 2025 – Oct 2025*
Delivered the Expense Splitter platform from design to deployment: 13 REST endpoints, JWT with role-based access control, three cloud services, stress tested to 200 concurrent users with 0% failures.

**Software Engineer** · Allstate India · *Nov 2022 – Mar 2023*
Built enterprise React reporting platforms for global stakeholders, bringing analytics and data-visualization workflows into one place and removing manual reporting and duplicate data pipelines. Strengthened CI/CD with pre-merge validation gates and deployment health checks, which cut rollbacks and sped up releases.

**Consultant** · TechChef's Software · *Sep 2021 – Nov 2022* · Clients: Dell, Intuit, JPMC
Architected a React Micro Frontend system so teams could deploy independently, removing release coupling and cutting deploy times. Built QuickBooks-integrated React and GraphQL modules, replacing over-fetching REST calls with schema-driven queries. Set up Jest and Enzyme testing from scratch and shipped WCAG-compliant, cross-browser UIs.

**Executive IT** · Fidelitus Corp · *Jan 2021 – Jul 2021*
Built reusable React components that enforced design-system conventions across internal enterprise platforms, and built secure authentication flows.

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Projects

### Expense Splitter: Group Expense Platform
`React 19` `Django REST Framework` `PostgreSQL` `JWT` `RBAC` `Material UI` `k6`

Built during my Fractal Analytics internship and deployed across Vercel, Render and Neon.

- 13 REST endpoints (9 for groups, members, expenses and summaries, 4 for auth)
- Equal and custom split modes with server-side validation: minimum 2 members, valid membership, full coverage, amounts summing within INR 0.01
- JWT authentication (SimpleJWT login, registration, refresh) and RBAC on every route
- Responsive Material UI frontend with four views: dashboard, expense form, expense list and balance summary

| Test | Setup | Result |
|:--|:--|:--|
| Load | 5 min, 50 concurrent users, 5 read endpoints | 41,127 requests, 0% failures, 137 req/s, 17 ms average, 48 ms p95 |
| Stress | 6 min, ramp to 200 users (+300%) | 101,002 requests, 0% failures, throughput up 105% to 280 req/s, p95 427 ms (14% under the 500 ms target) |

Result: gradual degradation under pressure, never failure.

### URL Shortener (Bharadwaj.ly): Full-Stack Platform
`Spring Boot` `React + Vite` `PostgreSQL` `JWT` `Docker` `Tailwind` `Material UI` `k6`

Deployed across Vercel, Render and Neon.

- Layered Controller, Service and Repository backend (Spring Data JPA, Hibernate) with stateless JWT authentication through a custom Spring Security filter, a role claim and 48-hour expiry
- Dockerized backend with 7 environment variables, zero hardcoded secrets and CORS restricted to one origin
- REST APIs for registration, login, 8-character short codes, link listing and public HTTP 302 redirects
- Load tested on the live deployment (Render free tier, from India, 3 runs, about 9 minutes): 6,329 requests, 99.95% success, 12,013 of 12,013 checks passed, including all 5,693 redirects returning 3xx with a Location header
- Saturation identified and documented: from 20 to 50 users, throughput rose 63% while p95 rose 158% (2.71 s at 50 users), with 0 errors
- k6 script with 5 test profiles, a 90/10 redirect-to-list mix, free-tier warm-up, p95 and error-rate thresholds, and a setup step that logs in, seeds a short URL and verifies its redirect

### 30 Full-Stack Projects
JWT and OTP authentication systems (MrAuthy), an E-Shop with Stripe payments, AI apps and more, built mainly in React with Next.js, Angular, Spring Boot, Django, MERN and MEAN. The 12 best are on my [portfolio](https://manu-bharadwaj-portfolio.vercel.app).

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Technical Skills

| | |
|:--|:--|
| **Languages** | Java, Python, JavaScript, TypeScript, HTML, CSS |
| **Frontend** | React, Next.js, Angular, Micro Frontends, Jest, Enzyme |
| **Backend** | Spring Boot, Django, FastAPI, Node.js, Express.js, REST APIs, GraphQL, Microservices |
| **Databases** | PostgreSQL, MySQL, MS SQL, MongoDB |
| **DevOps and Testing** | Docker, Jenkins, AWS EC2, Git, CI/CD, k6 |
| **Core Concepts** | Data Structures, Algorithms, Low-Level Design, High-Level Design, OOP |

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Competitive Programming

<table align="center">
<tr>
<td align="center"><b>Main account</b> · <a href="https://leetcode.com/u/mbbn/">mbbn</a><br/>Java, Python · Best Global Rank 41</td>
<td align="center"><b>Previous account</b> · <a href="https://leetcode.com/u/Manu-Bharadwaj-BN/">Manu-Bharadwaj-BN</a><br/>JavaScript</td>
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

<p align="center"><sub>Cards refresh automatically after every contest.</sub></p>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Open Source

| Repository | Contents | Languages |
|:--|:--|:--|
| [50 LLD Problems Solved](https://github.com/Manu577228/50-LLD-Problems-Solved) | 50 low-level design problems, each explained on YouTube | Java, Python |
| [Important HLD Problems](https://github.com/Manu577228/Important-HLD-Problems) | 10 system design classics: WhatsApp, Uber, TinyURL, Dream11, Zomato and more | Design docs |
| [CP Core Algorithms 150](https://github.com/Manu577228/CP-Core-Algorithms-150) | 150 advanced algorithms and 25+ extreme algorithms on niche topics | Java, Python |

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Teaching

[**@code-with-Bharadwaj**](https://www.youtube.com/@code-with-Bharadwaj) on YouTube: 3.32K subscribers and around 2,000 videos covering DSA, competitive programming, advanced algorithms and system design, with series in Java, Python and JavaScript. Explaining hard problems clearly on camera is the same skill I bring to design docs, code reviews and onboarding.

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## GitHub Stats

<p align="center">
<img src="https://github-readme-stats.vercel.app/api?username=Manu577228&show_icons=true&theme=github_dark&hide_border=true" height="170" alt="GitHub stats"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Manu577228&layout=compact&theme=github_dark&hide_border=true" height="170" alt="Top languages"/>
</p>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Education

Bachelor of Engineering · Visvesvaraya Technological University · 2018

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

## Contact

<div align="center">

I'm open to Software Engineer and SDE roles. Send me a problem and I'll send back a solution, a deployment and a load test.

**[bnmanubharadwaj@gmail.com](mailto:bnmanubharadwaj@gmail.com)** &nbsp;|&nbsp; [LinkedIn](https://www.linkedin.com/in/manu-bharadwaj-3507a345) &nbsp;|&nbsp; [Portfolio](https://manu-bharadwaj-portfolio.vercel.app)

</div>

<div align="center"><img src="assets/divider.svg" width="100%" alt=""/></div>

<div align="center">

<img src="assets/footer.svg" width="100%" alt="Open to SDE roles. Contact bnmanubharadwaj@gmail.com"/>

</div>

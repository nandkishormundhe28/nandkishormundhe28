# Super-Premium Developer Package for Nandkishor Mundhe

This single-file package contains all assets and code for your requested deliverables:

- `logo.svg` — Minimal premium NM logo (SVG, editable)
- `banner.html` — Animated GitHub banner (HTML + CSS) you can convert to GIF via ezgif.com or use as an HTML banner in a website
- `portfolio/` — A single-file React portfolio (`App.jsx`) and supporting CSS (`styles.css`) ready to drop into a Create React App / Vite project
- `resume.html` — Print-ready HTML resume with a modern, ATS-friendly layout
- `resume.md` — ATS-friendly Markdown resume you can paste into job portals
- `README-INSTALL.md` — Instructions for using these assets (how to add to README, convert banner to GIF, host portfolio, edit logo, etc.)

---

## File: logo.svg
```svg
<!-- logo.svg - Minimal premium NM monogram -->
<svg xmlns="http://www.w3.org/2000/svg" width="800" height="800" viewBox="0 0 200 200">
  <defs>
    <linearGradient id="g" x1="0" x2="1" y1="0" y2="1">
      <stop offset="0%" stop-color="#F7A81B"/>
      <stop offset="100%" stop-color="#FF6B6B"/>
    </linearGradient>
    <filter id="f" x="-20%" y="-20%" width="140%" height="140%">
      <feDropShadow dx="0" dy="6" stdDeviation="8" flood-color="#000" flood-opacity="0.18"/>
    </filter>
  </defs>

  <rect x="0" y="0" width="200" height="200" rx="24" fill="#0f1724" />
  <g transform="translate(20,20)" filter="url(#f)">
    <path d="M20 140 L20 40 L90 40 L90 80 L60 80 L60 140 Z" fill="url(#g)" />
    <path d="M100 140 L100 20 L180 20 L180 60 L140 60 L140 140 Z" fill="#ffffff" opacity="0.95" />
    <!-- Cutout to form N and M as negative space -->
    <path d="M28 48 L80 48 L80 76 L56 76 L56 140 L36 140 L36 76 L28 76 Z" fill="#0f1724" />
  </g>

</svg>
```

---

## File: banner.html
```html
<!-- banner.html - animated banner you can display at top of README (as an HTML page) or convert to GIF -->
<!doctype html>
<html>
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Nandkishor Mundhe - Banner</title>
  <style>
    :root{--bg:#071028;--accent:#F7A81B;--muted:#9AA6B2}
    html,body{height:100%;margin:0;font-family:Inter,Segoe UI,Roboto,Helvetica,Arial}
    .banner{display:flex;align-items:center;justify-content:center;height:40vh;background:linear-gradient(135deg,#071028 0%,#0b1630 60%);color:white}
    .card{width:92%;max-width:1100px;background:linear-gradient(180deg,rgba(255,255,255,0.03),rgba(255,255,255,0.01));border-radius:14px;padding:28px;box-shadow:0 10px 30px rgba(2,6,23,0.6);display:flex;gap:24px;align-items:center}
    .logo{width:110px;height:110px;border-radius:12px;background:linear-gradient(135deg,var(--accent),#FF6B6B);display:flex;align-items:center;justify-content:center;flex-shrink:0;box-shadow:0 8px 30px rgba(247,168,27,0.08);transform:translateY(0);animation:float 4s ease-in-out infinite}
    .logo svg{width:72px;height:72px}
    @keyframes float{0%{transform:translateY(0)}50%{transform:translateY(-8px)}100%{transform:translateY(0)}}
    .meta{flex:1}
    .title{font-size:28px;font-weight:700;letter-spacing:0.2px}
    .subtitle{color:var(--muted);margin-top:6px}
    .tags{margin-top:14px;display:flex;gap:10px;flex-wrap:wrap}
    .tag{background:rgba(255,255,255,0.03);padding:8px 12px;border-radius:999px;font-size:13px;color:var(--muted);border:1px solid rgba(255,255,255,0.03)}
    .marquee{margin-top:18px;overflow:hidden;white-space:nowrap}
    .marquee .items{display:inline-block;padding-left:100%;animation:slide 14s linear infinite}
    .items span{display:inline-block;margin-right:28px;font-weight:600;color:#e6eef9}
    @keyframes slide{0%{transform:translateX(0)}100%{transform:translateX(-100%)}}
  </style>
</head>
<body>
  <div class="banner">
    <div class="card">
      <div class="logo">
        <!-- simple monogram -->
        <svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <linearGradient id="lg" x1="0" x2="1"><stop offset="0%" stop-color="#F7A81B" /><stop offset="100%" stop-color="#FF6B6B" /></linearGradient>
          </defs>
          <rect width="100" height="100" rx="18" fill="url(#lg)" />
          <text x="50" y="60" text-anchor="middle" font-family="Segoe UI" font-weight="700" font-size="46" fill="#071028">NM</text>
        </svg>
      </div>
      <div class="meta">
        <div class="title">Nandkishor Mundhe — Full Stack Developer</div>
        <div class="subtitle">Java • Python • React • Machine Learning • Building polished web apps</div>
        <div class="tags">
          <div class="tag">Pune, India</div>
          <div class="tag">Open to opportunities</div>
          <div class="tag">Available for freelance</div>
        </div>
        <div class="marquee" aria-hidden="true">
          <div class="items">
            <span>Java • Python • React</span>
            <span>Spring Boot • Firebase • SQL</span>
            <span>Data Visualization • ML • Azure</span>
            <span>Clean Code • Testing • SDLC</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</body>
</html>
```

---

## File: portfolio/App.jsx
```jsx
// App.jsx - single-file React portfolio (drop into src/ of CRA or Vite)
import React from 'react';
import './styles.css';

export default function App(){
  return (
    <div className="site">
      <header className="hero">
        <div className="hero-inner">
          <div className="hero-left">
            <h1>Hey 👋, I'm <span className="accent">Nandkishor Mundhe</span></h1>
            <p className="lead">Full Stack Developer • Java • Python • React • ML Enthusiast</p>
            <div className="buttons">
              <a className="btn" href="#projects">See Projects</a>
              <a className="btn ghost" href="#contact">Contact</a>
            </div>
          </div>
          <div className="hero-right">
            <div className="card">
              <img src="/logo.svg" alt="NM Logo" />
              <h4>Nandkishor Mundhe</h4>
              <p>Full Stack Developer — building modern, responsive web apps</p>
            </div>
          </div>
        </div>
      </header>

      <main className="container">
        <section id="projects" className="section">
          <h2>Featured Projects</h2>
          <div className="grid">
            <article className="project">
              <img src="https://i.imgur.com/aZRQ5gN.png" alt="stocks"/>
              <h3>Stock Market Forecasting</h3>
              <p>Time-series forecasting using Linear Regression & LSTM with visual dashboards.</p>
            </article>
            <article className="project">
              <img src="https://i.imgur.com/OuNwSbn.png" alt="medicine"/>
              <h3>Medicine Reminder App</h3>
              <p>Android app with Firebase sync, notifications & scheduling.</p>
            </article>
            <article className="project">
              <img src="https://i.imgur.com/sKdY8Ih.png" alt="epass"/>
              <h3>E-Pass Generator</h3>
              <p>Role-based access system with Spring Boot backend & React frontend.</p>
            </article>
          </div>
        </section>

        <section className="section" id="skills">
          <h2>Skills & Tools</h2>
          <div className="chips">
            {['Java','Python','React','Spring Boot','SQL','Firebase','TensorFlow','Tableau'].map(s=> (
              <div key={s} className="chip">{s}</div>
            ))}
          </div>
        </section>

        <section className="section" id="contact">
          <h2>Contact</h2>
          <p>Mail: <a href="mailto:nandkishormundhe631@gmail.com">nandkishormundhe631@gmail.com</a></p>
          <p>LinkedIn: <a href="https://www.linkedin.com/in/nandkishor-mundhe-" target="_blank" rel="noreferrer">/in/nandkishor-mundhe-</a></p>
        </section>
      </main>

      <footer className="footer">
        <small>© {new Date().getFullYear()} Nandkishor Mundhe — Code. Learn. Build. Repeat.</small>
      </footer>
    </div>
  )
}
```

## File: portfolio/styles.css
```css
/* styles.css - minimal modern styles for the portfolio */
:root{--bg:#0b1220;--card:#071428;--accent:#F7A81B;--muted:#9aa6b2}
*{box-sizing:border-box}
body{margin:0;font-family:Inter,Segoe UI,Helvetica,Arial;background:linear-gradient(180deg,var(--bg),#061025);color:#e6eef9}
.site{min-height:100vh;display:flex;flex-direction:column}
.hero{padding:60px 24px}
.hero-inner{max-width:1100px;margin:0 auto;display:flex;gap:32px;align-items:center}
.hero-left{flex:1}
.accent{color:var(--accent)}
.lead{color:var(--muted);margin-top:8px}
.buttons{margin-top:16px}
.btn{background:var(--accent);color:#071428;padding:10px 16px;border-radius:8px;text-decoration:none;font-weight:600;margin-right:10px}
.btn.ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:#e6eef9}
.hero-right{width:260px}
.card{background:rgba(255,255,255,0.03);padding:18px;border-radius:12px;text-align:center}
.card img{width:78px}
.container{max-width:1100px;margin:40px auto;padding:0 20px}
.section{margin-bottom:32px}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:18px}
.project{background:linear-gradient(180deg,rgba(255,255,255,0.02),transparent);padding:16px;border-radius:10px}
.project img{width:100%;height:140px;object-fit:cover;border-radius:8px}
.chips{display:flex;gap:8px;flex-wrap:wrap}
.chip{background:rgba(255,255,255,0.03);padding:8px 12px;border-radius:999px}
.footer{text-align:center;padding:20px 0;color:var(--muted)}
@media(max-width:760px){.hero-inner{flex-direction:column-reverse}.hero-right{width:100%}}
```

---

## File: resume.html
```html
<!-- resume.html - modern, print-friendly resume. Save as resume.html and open in browser -> Print -> Save as PDF -->
<!doctype html>
<html>
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Nandkishor Mundhe - Resume</title>
<style>
  :root{--accent:#F7A81B;--text:#0b1220}
  body{font-family:Inter, Arial, sans-serif;margin:0;padding:32px;color:var(--text);background:#fff}
  .sheet{max-width:820px;margin:0 auto;border-radius:8px;padding:28px;border:1px solid #eee}
  header{display:flex;justify-content:space-between;align-items:center}
  h1{margin:0;font-size:22px}
  .contact{font-size:13px;color:#3b3b3b}
  .section{margin-top:18px}
  .section h3{margin-bottom:8px;color:var(--accent)}
  .two{display:flex;gap:18px}
  .left{flex:2}
  .right{flex:1}
  .skill{display:flex;align-items:center;justify-content:space-between}
  .bar{height:8px;background:#eee;border-radius:6px;overflow:hidden}
  .bar > i{display:block;height:100%;background:linear-gradient(90deg,var(--accent),#ff6b6b)}
  ul{margin:0;padding-left:18px}
  @media print{body{padding:0}.sheet{border:none}}
</style>
</head>
<body>
  <div class="sheet">
    <header>
      <div>
        <h1>Nandkishor Mundhe</h1>
        <div class="contact">Pune, Maharashtra • nandkishormundhe631@gmail.com • +91 8669526787</div>
      </div>
      <div>
        <div style="text-align:right">
          <div style="font-weight:700;color:var(--accent)">Full Stack Developer</div>
          <div style="font-size:13px;color:#666">Java • Python • React • Spring Boot • ML</div>
        </div>
      </div>
    </header>

    <div class="section two">
      <div class="left">
        <h3>Summary</h3>
        <p>A passionate Computer Engineering graduate focused on building scalable web applications and practical machine learning solutions. Proven experience in front-end and back-end development, with strong problem-solving skills and quick learning ability.</p>

        <h3>Experience</h3>
        <div>
          <strong>Frontend Developer Intern — Prodfitsols Infotech (OPC) Pvt Ltd</strong>
          <div style="font-size:13px;color:#666">Feb 2025 – Aug 2025</div>
          <ul>
            <li>Developed responsive UI using React.js and Angular; integrated RESTful APIs.</li>
            <li>Improved performance, resolved cross-browser issues and followed SDLC practices.</li>
          </ul>
        </div>

        <div style="margin-top:8px">
          <strong>Infosys — Virtual Internship & Training (Power Programmer)</strong>
          <div style="font-size:13px;color:#666">Training & Hands-on Labs</div>
          <ul>
            <li>Completed modules in OOP, scalable software development, and problem-solving.</li>
          </ul>
        </div>

        <h3>Projects</h3>
        <ul>
          <li><strong>Stock Forecasting:</strong> Time-series forecasting using Linear Regression and LSTM, dashboard for visualization.</li>
          <li><strong>Medicine Reminder App:</strong> Android app with Firebase for scheduling and push notifications.</li>
          <li><strong>E-Pass Generator:</strong> React frontend + Spring Boot backend with role-based authentication.</li>
        </ul>

      </div>

      <aside class="right">
        <h3>Education</h3>
        <div><strong>PICT — ME Computer Engineering</strong><div style="font-size:13px;color:#666">Graduated 2025 — CGPA 8.59</div></div>
        <div style="margin-top:8px"><strong>Anantrao Pawar College of Engineering</strong><div style="font-size:13px;color:#666">BE Computer Engineering — CGPA 8.79</div></div>

        <h3 style="margin-top:12px">Skills</h3>
        <div class="skill">Java <div style="width:56%" class="bar"><i style="width:86%"></i></div></div>
        <div class="skill">Python <div style="width:56%" class="bar"><i style="width:82%"></i></div></div>
        <div class="skill">React <div style="width:56%" class="bar"><i style="width:76%"></i></div></div>
        <div class="skill">SQL <div style="width:56%" class="bar"><i style="width:72%"></i></div></div>

        <h3 style="margin-top:12px">Certifications</h3>
        <ul>
          <li>Python Programming – Scalar Topics</li>
          <li>Java: Beginner to Advanced – LinkedIn Learning</li>
          <li>Data Visualization with Tableau – Great Learning</li>
        </ul>

      </aside>
    </div>

    <div class="section">
      <h3>Additional</h3>
      <p>Languages: English, Hindi, Marathi • Tools: Git, GitHub, VSCode, Android Studio • Cloud: GCP basics</p>
    </div>

  </div>
</body>
</html>
```

---

## File: resume.md
```md
# NANDKISHOR MUNDHE
Pune, Maharashtra • nandkishormundhe631@gmail.com • +91 8669526787

## SUMMARY
A passionate Computer Engineering graduate focused on building scalable web applications and practical machine learning solutions. Skilled in Java, Python, React, Spring Boot and data visualization.

## EXPERIENCE
**Frontend Developer Intern — Prodfitsols Infotech (OPC) Pvt Ltd** (Feb 2025 – Aug 2025)
- Built responsive UIs with React.js and Angular and integrated RESTful APIs.
- Improved performance and cross-browser compatibility; used Git for version control.

**Infosys — Virtual Internship & Training (Power Programmer)**
- Completed modules in OOP, scalable software development, and hands-on labs.

## PROJECTS
- **Stock Forecasting:** Time-series forecasting (Linear Regression, LSTM) + visualization dashboards.
- **Medicine Reminder App:** Android app using Firebase for scheduling and push notifications.
- **E-Pass Generator:** React frontend + Spring Boot backend with role-based auth.

## EDUCATION
**ME Computer Engineering** — Pune Institute of Computer Technology (2025) — CGPA 8.59

**BE Computer Engineering** — Anantrao Pawar College of Engineering (2023) — CGPA 8.79

## SKILLS
Java, Python, React, Spring Boot, SQL, Firebase, TensorFlow, Tableau

## CERTIFICATIONS
- Python Programming – Scalar Topics
- Java: Beginner to Advanced – LinkedIn Learning
- Data Visualization with Tableau – Great Learning

## CONTACT
- Email: nandkishormundhe631@gmail.com
- LinkedIn: https://www.linkedin.com/in/nandkishor-mundhe-
```

---

## File: README-INSTALL.md
```md
# How to use the assets

## 1) logo.svg
- Replace the `/logo.svg` path in the portfolio App.jsx with the provided logo.svg file in your `public/` folder.
- Open the SVG with any editor (Figma, Illustrator, VSCode) to fine-tune colors or sizes.

## 2) banner.html
- To use the banner on your README: convert the animated HTML to a GIF using a screen-record to GIF tool (e.g., record the page at 1280x360 then use ezgif.com to convert & optimize).
- Alternatively, host `banner.html` as a small landing page and link to it from your README.

## 3) Portfolio (React)
- Create a new React app (Vite or CRA) and drop `App.jsx` into `src/` and `styles.css` into `src/`.
- Place `logo.svg` in the `public/` folder. Replace placeholder images with your project screenshots.
- Run `npm start` or `pnpm dev`.

## 4) Resume
- Open `resume.html` in a browser and print to PDF using "Save as PDF" for a clean, printable resume.
- Use `resume.md` for easy copy-paste into job portals.

## 5) Converting Banner to GIF
- Open `banner.html` in Chrome at 1280x360 viewport (press F12 → Toggle Device Toolbar → set 1280x360)
- Use a screen recorder or "Capture screenshot" to record a 6–10s clip.
- Upload the clip to ezgif.com/video-to-gif, crop and optimize (reduce fps to 12, scale to 900px width)

## 6) Need changes?
- Reply here with specific edit requests (colors, copy, images, layout) and I'll update the files.
```

---

# Notes
- All images in the portfolio are placeholder images hosted on imgur. Replace them with your own screenshots for best effect.
- I intentionally removed repo links. When you're ready, I can add live links/cards that point to your repos.

Good work — everything is bundled and ready. Open the canvas file to copy any item you want to use.

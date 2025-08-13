# NAME : NAVEEN KUMAR T
# REG NO : 212223220067
# Ex01 Portfolio
## Date : 13:08:2025 

## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
```

<!doctype html>
<html lang="en">
<head>
  <!-- ====== META ====== -->
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Naveen Kumar — Portfolio</title>
  <meta name="description" content="Naveen Kumar — B.Tech IT | Data Analytics • Machine Learning • Web Development" />
  <meta name="theme-color" content="#0f1724" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap" rel="stylesheet">

  <!-- ====== STYLES ====== -->
  <style>
    :root{
      --bg:#0b1220;
      --panel:#0f172a;
      --text:#e5e7eb;
      --muted:#9aa4b2;
      --border:rgba(255,255,255,0.08);
      --glass:rgba(255,255,255,0.06);
      --glass-2:rgba(255,255,255,0.04);
      --accent:#6EE7B7; /* mint */
      --accent2:#60A5FA; /* blue */
      --ring: 0 0 0 8px rgba(110,231,183,.08);
      --shadow: 0 12px 40px rgba(2, 6, 23, .55);
      --radius: 16px;
    }

    *{box-sizing:border-box;margin:0;padding:0}
    html,body{height:100%}
    body{
      font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,'Helvetica Neue',Arial;
      color:var(--text);
      background:
        radial-gradient(900px 600px at 10% 5%, rgba(96,165,250,.12), transparent),
        radial-gradient(800px 500px at 90% 95%, rgba(110,231,183,.10), transparent),
        var(--bg);
      line-height:1.55;
    }
    img{max-width:100%;display:block}
    a{color:inherit;text-decoration:none}
    .container{max-width:1120px;margin:0 auto;padding:28px}

    /* ====== NAVBAR ====== */
    header{position:sticky;top:16px;z-index:40}
    .nav{
      backdrop-filter: blur(8px);
      background: linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.02));
      border:1px solid var(--border);
      border-radius:14px;
      padding:10px 16px;
      display:flex;align-items:center;justify-content:space-between;
      box-shadow:var(--shadow);
    }
    .brand{display:flex;gap:12px;align-items:center}
    .mark{
      width:44px;height:44px;border-radius:12px;
      background:linear-gradient(135deg,var(--accent),var(--accent2));
      display:grid;place-items:center;font-weight:800;color:#062132;
      box-shadow: inset 0 0 18px rgba(255,255,255,.25);
    }
    nav ul{display:flex;gap:12px;list-style:none}
    nav a{
      padding:8px 12px;border-radius:10px;font-weight:600;
      color:var(--muted);font-size:14px
    }
    nav a:hover{color:white;background:rgba(255,255,255,.06)}

    .cta{
      background: linear-gradient(90deg, var(--accent), var(--accent2));
      padding:8px 12px;border-radius:10px;
      color:#062132;font-weight:800
    }

    /* ====== HERO ====== */
    .hero{min-height:78vh;display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center;padding-top:20px}
    .intro h1{font-size:40px;line-height:1.02}
    .intro p{color:var(--muted);margin-top:12px;font-size:16px}
    .gradient-text{
      background:linear-gradient(90deg,var(--accent),var(--accent2));
      -webkit-background-clip:text;background-clip:text;color:transparent
    }
    .btns{margin-top:18px;display:flex;gap:12px;flex-wrap:wrap}
    .btn{
      padding:12px 16px;border-radius:12px;font-weight:800;
      background:transparent;border:1px solid var(--border);color:var(--text);
      transition:transform .2s ease, box-shadow .2s ease, background .2s ease;
    }
    .btn:hover{transform:translateY(-2px);box-shadow:var(--ring);background:rgba(255,255,255,.02)}
    .btn.primary{
      background:linear-gradient(90deg,var(--accent),var(--accent2));
      color:#062132;border:none;box-shadow:0 12px 28px rgba(96,165,250,.25)
    }

    /* Right profile card */
    .card{
      background:linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.02));
      border:1px solid var(--border);
      padding:18px;border-radius:var(--radius);box-shadow:var(--shadow)
    }
    .avatar-wrap{
      display:grid;place-items:center;position:relative;margin-bottom:12px;
    }
    .avatar-ring{
      --s:172px;
      width:var(--s);height:var(--s);
      border-radius:999px;padding:3px;
      background:conic-gradient(from 120deg, var(--accent), var(--accent2), var(--accent));
      animation:spin 8s linear infinite paused;
    }
    .avatar-ring:hover{animation-play-state:running}
    .avatar{
      width:100%;height:100%;border-radius:999px;
      display:grid;place-items:center;
      background:linear-gradient(135deg, rgba(96,165,250,.18), rgba(110,231,183,.14));
      color:var(--muted);font-weight:700
    }
    @keyframes spin{to{transform:rotate(360deg)}}

    .meta{display:flex;justify-content:space-between;color:var(--muted);margin-top:12px}
    .skills-inline{margin-top:14px;display:flex;gap:8px;flex-wrap:wrap}
    .chip{
      padding:8px 10px;border-radius:10px;
      border:1px solid rgba(255,255,255,.06);
      background:linear-gradient(180deg, rgba(255,255,255,.05), transparent);
      color:var(--muted);font-weight:700;font-size:12px
    }

    /* ====== SECTIONS ====== */
    section{padding:62px 0}
    h2.section-title{font-size:22px;margin-bottom:18px}
    .grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
    .project{
      position:relative;overflow:hidden;
      background:var(--glass-2);border:1px solid var(--border);
      padding:16px;border-radius:14px;transition:transform .35s, box-shadow .35s, border-color .35s;
    }
    .project:hover{transform:translateY(-8px);box-shadow:0 20px 60px rgba(2,6,23,.6);border-color:rgba(255,255,255,.18)}
    .thumb{height:140px;border-radius:10px;display:grid;place-items:center;
      font-weight:800;color:var(--muted);
      background:linear-gradient(135deg, rgba(96,165,250,.12), rgba(110,231,183,.10));
      border:1px dashed rgba(255,255,255,.08)
    }
    .project p{color:var(--muted);margin-top:10px;font-size:14px}

    .skills-wrap{display:flex;gap:10px;flex-wrap:wrap}
    .skill{
      padding:10px 12px;border-radius:10px;border:1px solid rgba(255,255,255,.06);
      background:linear-gradient(180deg, rgba(255,255,255,.02), transparent);
      color:var(--text);font-weight:700;font-size:13px;
      transform:translateY(8px);opacity:0;
      transition:transform .5s ease, opacity .5s ease;
    }
    .skill.visible{transform:none;opacity:1}

    .info-card{
      background:linear-gradient(180deg, rgba(255,255,255,.05), rgba(255,255,255,.02));
      border:1px solid var(--border);padding:16px;border-radius:14px
    }
    ul.clean{list-style: none;padding-left:0}
    ul.clean li{margin:8px 0;color:var(--muted)}

    /* ====== CONTACT ====== */
    .contact-grid{display:grid;grid-template-columns:1fr 380px;gap:18px}
    .form input,.form textarea{
      width:100%;padding:12px;border-radius:12px;border:1px solid rgba(255,255,255,.08);
      background:rgba(255,255,255,.02);color:var(--text);resize:none;outline:none
    }
    .form input:focus,.form textarea:focus{box-shadow:var(--ring);border-color:rgba(255,255,255,.22)}
    .form button{
      margin-top:10px;padding:12px;border-radius:12px;border:none;cursor:pointer;
      background:linear-gradient(90deg,var(--accent),var(--accent2));
      font-weight:800;color:#062132
    }

    /* ====== FOOTER ====== */
    footer{padding:26px 0;color:var(--muted);text-align:center;border-top:1px solid rgba(255,255,255,.06)}

    /* ====== SMALL SCREENS ====== */
    @media (max-width:1000px){.hero{grid-template-columns:1fr}}
    @media (max-width:860px){
      nav ul{display:none}
      .grid-3{grid-template-columns:1fr 1fr}
      .contact-grid{grid-template-columns:1fr}
    }
    @media (max-width:520px){.grid-3{grid-template-columns:1fr}}

    /* ====== MICRO ANIMS ====== */
    .reveal{opacity:0;transform:translateY(10px);transition:opacity .6s ease, transform .6s ease}
    .reveal.visible{opacity:1;transform:none}
    .pulse{animation:pulse 2.2s ease-in-out infinite}
    @keyframes pulse{0%,100%{transform:translateY(0)}50%{transform:translateY(-2px)}}

    /* Background blobs */
    .blobs{position:fixed;inset:auto auto 0 0;pointer-events:none;z-index:0}
    .blob{width:320px;height:320px;border-radius:50%;filter:blur(60px);opacity:.55}
    .b1{background:radial-gradient(circle at 30% 30%, rgba(96,165,250,.45), rgba(96,165,250,.12) 40%, transparent);position:absolute;right:-60px;bottom:-80px;animation:float1 9s infinite}
    .b2{background:radial-gradient(circle at 70% 70%, rgba(110,231,183,.45), rgba(110,231,183,.12) 40%, transparent);position:absolute;right:120px;bottom:-120px;animation:float2 10s infinite}
    @keyframes float1{0%{transform:translateY(0) rotate(0)}50%{transform:translateY(-18px) rotate(12deg)}100%{transform:translateY(0) rotate(0)}}
    @keyframes float2{0%{transform:translateY(0) rotate(0)}50%{transform:translateY(22px) rotate(-8deg)}100%{transform:translateY(0) rotate(0)}}
  </style>
</head>
<body>

  <!-- Background blobs -->
  <div class="blobs" aria-hidden="true">
    <div class="blob b1"></div>
    <div class="blob b2"></div>
  </div>

  <!-- ====== NAV ====== -->
  <header>
    <div class="container">
      <div class="nav">
        <div class="brand">
          <div class="mark">NK</div>
          <div>
            <div style="font-weight:800">Naveen Kumar</div>
            <div style="font-size:12px;color:var(--muted)">Data Analytics • Machine Learning • Web Dev</div>
          </div>
        </div>
        <nav aria-label="Primary">
          <ul>
            <li><a class="pulse" href="#home">Home</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#certifications">Certifications</a></li>
            <li><a href="#education">Education</a></li>
            <li><a class="cta" href="#contact">Contact</a></li>
          </ul>
        </nav>
      </div>
    </div>
  </header>

  <!-- ====== HERO ====== -->
  <main class="container" id="home">
    <section class="hero" aria-label="Intro">
      <div class="intro">
        <h1 class="reveal">
          Hi — I’m <span class="gradient-text">Naveen Kumar</span><br>
          <small style="font-weight:600;color:var(--muted)">B.Tech IT • Saveetha Engineering College</small>
        </h1>
        <p class="reveal" style="--delay:200ms">
          I specialize in <b>Data Analytics, Machine Learning, and Web Development</b>. I build insightful dashboards,
          predictive models, and interactive web tools with <b>Python, SQL, Power BI, and React</b>.
        </p>
        <div class="btns reveal" style="--delay:400ms">
          <a class="btn primary" href="#projects">See Projects</a>
          <a class="btn" href="#contact">Hire / Contact</a>
        </div>
        <div style="margin-top:18px" class="reveal">
          <div class="info-card" style="font-family:ui-monospace,Menlo,Consolas,monospace;font-size:13px">
            &lt;stack&gt; Python • SQL • Power BI • React • ML • Git &lt;/stack&gt;
          </div>
        </div>
      </div>

      <!-- Profile card -->
      <aside class="card" aria-label="Profile summary">
        <div class="avatar-wrap">
          <div class="avatar-ring" aria-hidden="true">
            <!-- Replace inner DIV with your <img src="me.jpg" alt="Naveen Kumar" class="avatar"> -->
             <img src="me.jpg" alt="Naveen Kumar" class="avatar">
          </div>
        </div>

        <div class="meta">
          <div>
            <div style="font-weight:800">Projects</div>
            <div style="font-size:12px;color:var(--muted)">15 completed</div>
          </div>
          <div style="text-align:right">
            <div style="font-weight:800">Location</div>
            <div style="font-size:12px;color:var(--muted)">Chennai, India</div>
          </div>
        </div>

        <div class="skills-inline" aria-label="Highlights">
          <span class="chip">Python</span>
          <span class="chip">SQL</span>
          <span class="chip">Power BI</span>
          <span class="chip">React</span>
          <span class="chip">Machine Learning</span>
          <span class="chip">Git</span>
        </div>
      </aside>
    </section>

    <!-- ====== PROJECTS ====== -->
    <section id="projects" aria-labelledby="proj-title">
      <h2 id="proj-title" class="section-title">Selected Projects</h2>

      <div class="grid-3">
        <article class="project reveal">
          <div class="thumb">Healthcare Data Insights</div>
          <h3 style="margin-top:10px">Power BI Dashboard</h3>
          <p>Built 5 interactive dashboards over 50K+ healthcare records. Integrated SQL queries, DAX measures, and drill-through for patient outcomes & resource utilization.</p>
          <div class="skills-inline" style="margin-top:10px">
            <span class="chip">Power BI</span><span class="chip">SQL</span><span class="chip">DAX</span>
          </div>
        </article>

        <article class="project reveal">
          <div class="thumb">Merck Market Access</div>
          <h3 style="margin-top:10px">Market Analysis Dashboard</h3>
          <p>Developed a business insights dashboard for pricing trends, competitive positioning, and product performance; enabled data-driven market strategies.</p>
          <div class="skills-inline" style="margin-top:10px">
            <span class="chip">Power BI</span><span class="chip">Data Modeling</span><span class="chip">ETL</span>
          </div>
        </article>

        <article class="project reveal">
          <div class="thumb">Generative AI Lab</div>
          <h3 style="margin-top:10px">Prompt Engineering</h3>
          <p>Compared LLM outputs across prompt patterns to improve accuracy, structure, and creativity; documented best practices for task types.</p>
          <div class="skills-inline" style="margin-top:10px">
            <span class="chip">LLMs</span><span class="chip">Python</span><span class="chip">Evaluation</span>
          </div>
        </article>
      </div>
    </section>

    <!-- ====== SKILLS ====== -->
    <section id="skills" aria-labelledby="skills-title">
      <h2 id="skills-title" class="section-title">Skills</h2>
      <div class="skills-wrap">
        <span class="skill">Python</span>
        <span class="skill">SQL</span>
        <span class="skill">Power BI</span>
        <span class="skill">Machine Learning</span>
        <span class="skill">React JS</span>
        <span class="skill">HTML & CSS</span>
        <span class="skill">Statistical Analysis</span>
        <span class="skill">Data Modeling</span>
        <span class="skill">Git & GitHub</span>
        <span class="skill">Google Cloud</span>
      </div>
    </section>

    <!-- ====== CERTIFICATIONS ====== -->
    <section id="certifications" aria-labelledby="cert-title">
      <h2 id="cert-title" class="section-title">Certifications</h2>
      <div class="grid-3">
        <div class="info-card reveal">
          <h3>Google Cloud Skill Boost</h3>
          <ul class="clean">
            <li>Hands-on labs & quests on cloud services</li>
            <li>Focus: data analytics & infra basics</li>
          </ul>
        </div>
        <div class="info-card reveal">
          <h3>Data Analytics with Python</h3>
          <ul class="clean">
            <li>Numpy, Pandas, Matplotlib workflows</li>
            <li>EDA & basic ML pipelines</li>
          </ul>
        </div>
        <div class="info-card reveal">
          <h3>Implant Training Certificate</h3>
          <ul class="clean">
            <li>Industry practices, SDLC and deployment</li>
            <li>Version control & collaboration</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- ====== EDUCATION ====== -->
    <section id="education" aria-labelledby="edu-title">
      <h2 id="edu-title" class="section-title">Education</h2>
      <div class="grid-3">
        <div class="info-card reveal">
          <h3>B.Tech — Information Technology</h3>
          <ul class="clean">
            <li>Saveetha Engineering College (2023–2027)</li>
            <li>Current: ~86%</li>
          </ul>
        </div>
        <div class="info-card reveal">
          <h3>Class XII</h3>
          <ul class="clean">
            <li>Assisi Matriculation Higher Secondary School</li>
            <li>Score: 82%</li>
          </ul>
        </div>
        <div class="info-card reveal">
          <h3>Interests</h3>
          <ul class="clean">
            <li>Data Engineering & BI</li>
            <li>Ethical Hacking & Linux</li>
            <li>Generative AI</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- ====== CONTACT ====== -->
    <section id="contact" aria-labelledby="contact-title">
      <h2 id="contact-title" class="section-title">Contact</h2>
      <div class="contact-grid">
        <div>
          <p style="color:var(--muted)">
            Want to collaborate on analytics, ML, or web projects? Send a message or email me.
          </p>
          <div style="margin-top:12px">
            <a href="mailto:nk.sec123@gmail.com" class="cta" style="display:inline-block;padding:12px 14px;border-radius:12px">Email: nk.sec123@gmail.com</a>
          </div>
          <div style="margin-top:12px;color:var(--muted)">
            <b style="color:var(--text)">Availability
              

        <!-- Demo form - replace with your backend or service like Formspree -->
        <form class="card form" onsubmit="event.preventDefault(); alert('Message sent (demo). Connect a backend or Formspree to enable.');">
          <label style="font-size:12px;color:var(--muted)">Your Name</label>
          <input placeholder="Your name" required />
          <label style="font-size:12px;color:var(--muted);margin-top:8px;display:block">Email</label>
          <input type="email" placeholder="nk,sec123@gmail.com" required />
          <label style="font-size:12px;color:var(--muted);margin-top:8px;display:block">Message</label>
          <textarea rows="5" placeholder="How can I help?" required></textarea>
          <button type="submit">Send Message</button>
        </form>
      </div>
    </section>

    <footer>
      <div>© 2025 Naveen Kumar — Built with ❤️ • Saveetha Engineering College</div>
    </footer>
  </main>

  <!-- ====== SCRIPTS ====== -->
  <script>
    // Reveal on scroll
    const observeReveal = (selector, opts={threshold:0.12}) => {
      const io = new IntersectionObserver(entries=>{
        entries.forEach(e=>{
          if(e.isIntersecting){ e.target.classList.add('visible'); io.unobserve(e.target); }
        })
      }, opts);
      document.querySelectorAll(selector).forEach(el=> io.observe(el));
    };
    observeReveal('.reveal');

    // Staggered skill animation
    const skills = document.querySelectorAll('.skill');
    const io2 = new IntersectionObserver(entries=>{
      entries.forEach(e=>{
        if(e.isIntersecting){
          skills.forEach((s, i)=> setTimeout(()=> s.classList.add('visible'), i*90));
          io2.disconnect();
        }
      })
    }, {threshold:.2});
    if(skills.length) io2.observe(skills[0]);

    // Smooth internal links
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', e=>{
        const id = a.getAttribute('href');
        if(id === '#') return;
        const el = document.querySelector(id);
        if(!el) return;
        e.preventDefault();
        el.scrollIntoView({behavior:'smooth', block:'start'});
        history.replaceState(null, '', id);
      })
    });
  </script>
<!-- Code injected by live-server -->
<script>
	// <![CDATA[  <-- For SVG support
	if ('WebSocket' in window) {
		(function () {
			function refreshCSS() {
				var sheets = [].slice.call(document.getElementsByTagName("link"));
				var head = document.getElementsByTagName("head")[0];
				for (var i = 0; i < sheets.length; ++i) {
					var elem = sheets[i];
					var parent = elem.parentElement || head;
					parent.removeChild(elem);
					var rel = elem.rel;
					if (elem.href && typeof rel != "string" || rel.length == 0 || rel.toLowerCase() == "stylesheet") {
						var url = elem.href.replace(/(&|\?)_cacheOverride=\d+/, '');
						elem.href = url + (url.indexOf('?') >= 0 ? '&' : '?') + '_cacheOverride=' + (new Date().valueOf());
					}
					parent.appendChild(elem);
				}
			}
			var protocol = window.location.protocol === 'http:' ? 'ws://' : 'wss://';
			var address = protocol + window.location.host + window.location.pathname + '/ws';
			var socket = new WebSocket(address);
			socket.onmessage = function (msg) {
				if (msg.data == 'reload') window.location.reload();
				else if (msg.data == 'refreshcss') refreshCSS();
			};
			if (sessionStorage && !sessionStorage.getItem('IsThisFirstTime_Log_From_LiveServer')) {
				console.log('Live reload enabled.');
				sessionStorage.setItem('IsThisFirstTime_Log_From_LiveServer', true);
			}
		})();
	}
	else {
		console.error('Upgrade your browser. This Browser is NOT supported WebSocket for Live-Reloading.');
	}
	// ]]>
</script>
</body>
</html>
```


## OUTPUT :
## Home Page 
<img width="1230" height="708" alt="Screenshot 2025-08-13 094507" src="https://github.com/user-attachments/assets/726c9f8e-f3e2-4145-a66e-9a59d0d12b01" />

## Project 
<img width="1869" height="897" alt="Screenshot 2025-08-13 093228" src="https://github.com/user-attachments/assets/dc105e03-3362-423a-9703-450b013c21fc" />

## Skill
<img width="1885" height="960" alt="Screenshot 2025-08-13 101518" src="https://github.com/user-attachments/assets/f13d9e01-4242-435a-9614-3b086e1040dd" />

## Certificate & Education
<img width="1458" height="791" alt="Screenshot 2025-08-13 100936" src="https://github.com/user-attachments/assets/1ef5eaaa-ab24-4f16-981e-eeb2df1fb144" />

## Contact 
<img width="1881" height="898" alt="Screenshot 2025-08-13 092854" src="https://github.com/user-attachments/assets/7e6750e1-2c89-4e15-b83b-ede82f6a0516" />






## RESULT :
The program for creating Portfolio using HTML and CSS is executed successfully.

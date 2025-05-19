<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vinita Sachdev | Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet" />
  <style>
    :root{--accent:#22d3ee;--bg:#000;--fg:#f1f5f9;--gray:#94a3b8;}
    *{margin:0;padding:0;box-sizing:border-box;font-family:"Poppins",sans-serif;scroll-behavior:smooth;}
    body{background:var(--bg);color:var(--fg);}
    header{position:fixed;top:0;left:0;width:100%;background:rgba(0,0,0,.6);backdrop-filter:blur(12px);border-bottom:1px solid #1e293b;z-index:100;}
    nav{max-width:1100px;margin:auto;display:flex;justify-content:space-between;align-items:center;padding:1rem 2rem;}
    .logo{font-size:1.5rem;font-weight:700;color:var(--accent);}
    .nav-links{display:flex;gap:1.5rem;}
    .nav-links a{text-decoration:none;color:var(--fg);font-weight:500;transition:color .2s ease;}
    .nav-links a:hover{color:var(--accent);}
    section{padding:6rem 2rem;max-width:1100px;margin:auto;}

    /* ---------- content blocks ---------- */
    .hero{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));align-items:center;gap:3rem;min-height:100vh;}
    .hero img{width:100%;border-radius:1.5rem;box-shadow:0 10px 25px rgba(34,211,238,.2);}
    .hero-content h1{font-size:2.7rem;line-height:1.2;margin-bottom:1rem;}
    .hero-content p{font-size:1.1rem;color:var(--gray);margin-bottom:2rem;}

    .about,.projects-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:2rem;align-items:center;}
    .about img{width:100%;border-radius:1.5rem;}
    .about-content h2,.projects-title{font-size:2rem;margin-bottom:1rem;}
    .about-content p{color:var(--gray);line-height:1.6;}

    .card{background:#0f172a;border:1px solid #1e293b;border-radius:1rem;overflow:hidden;transition:transform .5s ease,box-shadow .5s ease;}
    .card:hover{transform:translateY(-5px);box-shadow:0 12px 25px rgba(34,211,238,.12);}
    .card img{width:100%;height:160px;object-fit:cover;}
    .card-body{padding:1.25rem;}
    .card-body h3{margin-bottom:.5rem;color:var(--accent);}
    .card-body p{color:var(--gray);font-size:.9rem;}
    .card-body a{display:inline-block;margin-top:1rem;color:var(--accent);text-decoration:none;font-weight:600;}

    .email-box{background:#0f172a;border:1px solid #1e293b;border-radius:.75rem;padding:2rem;text-align:center;}
    .email-box h3{margin-bottom:.75rem;}
    .email-link{font-size:1.1rem;color:var(--accent);text-decoration:none;font-weight:600;word-break:break-all;}
    .email-link:hover{text-decoration:underline;}

    footer{text-align:center;padding:2rem 0;font-size:.9rem;color:var(--gray);}

    /* ---------- slide‑in animation ---------- */
    .section{opacity:0;transform:translateX(80px);transition:opacity .5s ease,transform .5s ease;}
    .section.left-start{transform:translateX(-80px);}
    .section.show{opacity:1;transform:translateX(0);}
  </style>
</head>
<body>
  <!-- ===== Header ===== -->
  <header>
    <nav>
      <div class="logo">Vinita</div>
      <div class="nav-links">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
      </div>
    </nav>
  </header>

  <!-- ===== Hero ===== -->
  <section id="home" class="hero section"><!-- slides from right -->
    <div class="hero-content">
      <h1>Hello, I'm <span style="color:var(--accent);">Vinita Sachdev</span></h1>
      <p>Entry‑Level Web Developer skilled in Python, SQL & modern web tech.</p>
    </div>
    <img src="formals.jpg" alt="Vinita photo" />
  </section>

  <!-- ===== About ===== -->
  <section id="about" class="about section left-start"><!-- slides from left -->
    <img src="formals.jpg" alt="About image" />
    <div class="about-content">
      <h2>About Me</h2>
      <p>Computer Science graduate passionate about web and software development with hands‑on experience in Python, Java, and SQL. Strong in backend development, database management, and SDLC practices. Excellent communication and problem‑solving skills with a collaborative mindset and eagerness to grow in an Agile environment.</p>
    </div>
  </section>

  <!-- ===== Projects ===== -->
  <section id="projects" class="section"><!-- slides from right -->
    <h2 class="projects-title" style="text-align:center;margin-bottom:2rem;">Projects</h2>
    <div class="projects-grid" id="projectsGrid"></div>
  </section>

  <!-- ===== Contact ===== -->
  <section id="contact" class="section left-start"><!-- slides from left -->
    <div class="email-box">
      <h3>Reach Me Directly</h3>
      <a href="mailto:vinitasachdev21@gmail.com" class="email-link">vinitasachdev21@gmail.com</a>
      <p style="color:var(--gray);margin-top:.5rem;">(Click to open your email client or copy the address)</p>
    </div>
  </section>

  <footer>© <span id="year"></span> Vinita Sachdev. All rights reserved.</footer>

<script>
  document.getElementById("year").textContent = new Date().getFullYear();

  /* ------- Populate projects grid ------- */
  const projects=[
    {title:"Personal Portfolio Website",description:"Responsive portfolio using HTML & CSS.",image:"potfolio.png",link:"https://github.com/Vinita-21/CodSoft"},
    {title:"To‑Do List App",description:"GUI task manager in Python & Tkinter.",link:"https://github.com/Vinita-21/CodSoft/blob/main/CodSoft_task001.mp4"},
    {title:"Calculator",description:"Basic arithmetic calculator in Python & Tkinter.",link:"https://github.com/Vinita-21/CodSoft"},
    {title:"Password Generator",description:"Secure password tool in Python.",link:"https://github.com/Vinita-21/CodSoft"},
    {title:"Employee Mgmt System",description:"Java desktop app with barcode integration.",image:"employee.png"}
  ];
  const grid=document.getElementById("projectsGrid");
  projects.forEach(p=>{
    const c=document.createElement("div");
    c.className="card";
    c.innerHTML=`<img src="${p.image||'placeholder.png'}" alt="${p.title}"/><div class="card-body"><h3>${p.title}</h3><p>${p.description}</p><a href="${p.link}" target="_blank">View →</a></div>`;
    grid.appendChild(c);
  });

  /* ---------- slide‑in observer ---------- */
  const observer=new IntersectionObserver(entries=>{
    entries.forEach(entry=>{
      if(entry.isIntersecting){
        entry.target.classList.add('show');
        observer.unobserve(entry.target);
      }
    });
 },{threshold:0.15});

  document.querySelectorAll('.section').forEach(sec=>observer.observe(sec));
</script>
</body>
</html>

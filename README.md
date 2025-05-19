# Portfolio

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Vinita Sachdev | Web Developer</title>
  <style>
    :root {
      --primary: #3f51b5;
      --accent: #f5f5f5;
      --text-dark: #333;
      --text-light: #fff;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      background: var(--accent);
      color: var(--text-dark);
      line-height: 1.6;
    }

    header {
      background: var(--primary);
      color: var(--text-light);
      text-align: center;
      padding: 3rem 1rem;
    }

    header h1 {
      font-size: 2.5rem;
    }

    nav {
      margin-top: 1rem;
    }

    nav a {
      color: var(--text-light);
      margin: 0 1rem;
      text-decoration: none;
      font-weight: 500;
    }

    section {
      padding: 2rem 1rem;
      max-width: 1000px;
      margin: auto;
    }

    h2 {
      color: var(--primary);
      margin-bottom: 1rem;
    }

    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1.5rem;
    }

    .project {
      background: #fff;
      padding: 1rem;
      border-radius: 8px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      transition: transform 0.3s ease;
    }

    .project:hover {
      transform: scale(1.02);
    }

    .project h3 {
      margin-bottom: 0.5rem;
    }

    .project p {
      font-size: 0.95rem;
      margin-bottom: 0.5rem;
    }

    .project a {
      color: var(--primary);
      font-weight: bold;
      text-decoration: none;
    }

    .contact-info p,
    .contact-info a {
      margin: 0.5rem 0;
      color: var(--text-dark);
      text-decoration: none;
    }

    footer {
      text-align: center;
      padding: 1.5rem;
      background-color: #eee;
      margin-top: 2rem;
      font-size: 0.9rem;
    }

    @media (max-width: 600px) {
      nav a {
        display: block;
        margin: 0.5rem 0;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>Vinita Sachdev</h1>
    <p>Entry-Level Web Developer</p>
    <nav>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section id="about">
    <h2>About Me</h2>
    <p>
      I’m a Computer Science graduate with hands-on experience in Python, Java, SQL, and Web Development. 
      I build user-focused applications with clean code and responsive design principles.
    </p>
  </section>

  <section id="projects">
    <h2>Projects</h2>
    <div class="projects-grid">
      <div class="project">
        <h3>To-Do List App</h3>
        <p>Python + Tkinter GUI application for task tracking with add/edit/delete functionality.</p>
        <a href="https://github.com/Vinita-21">View on GitHub</a>
      </div>
      <div class="project">
        <h3>Password Generator</h3>
        <p>Python app for generating secure passwords with customizable options and random logic.</p>
        <a href="https://github.com/Vinita-21">View on GitHub</a>
      </div>
      <div class="project">
        <h3>Employee Management System</h3>
        <p>Java application with JDBC and barcode generation for managing employee records.</p>
        <a href="https://github.com/Vinita-21">View on GitHub</a>
      </div>
      <div class="project">
        <h3>Tic Tac Toe with AI</h3>
        <p>Python game with Minimax algorithm to play against an intelligent AI opponent.</p>
        <a href="https://github.com/Vinita-21">View on GitHub</a>
      </div>
    </div>
  </section>

  <section id="contact">
    <h2>Contact</h2>
    <div class="contact-info">
      <p>Email: <a href="mailto:vinitasachdev21@gmail.com">vinitasachdev21@gmail.com</a></p>
      <p>LinkedIn: <a href="https://www.linkedin.com/in/vinita-sachdev-626860251/" target="_blank">Vinita Sachdev</a></p>
      <p>GitHub: <a href="https://github.com/Vinita-21" target="_blank">Vinita-21</a></p>
    </div>
  </section>

  <footer>
    &copy; 2025 Vinita Sachdev. Built with HTML & CSS.
  </footer>

</body>
</html>


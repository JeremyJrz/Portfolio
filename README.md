<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Portfolio - Jérémy Jerez</title>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css"/>
<style>
/* ROOT */
:root{
  --primary: #4da6ff;
  --dark: #000000;
  --lighttext: #f2f2f2;
  --card: #111;
  --card2: #0d0d0d;
}
*{margin:0;padding:0;box-sizing:border-box;}
body{
  font-family:"Montserrat", sans-serif;
  background:var(--dark);
  color:var(--lighttext);
  overflow-x:hidden;
}
html{scroll-behavior:smooth;}

/* HEADER */
header{
  width:100%;
  padding:1.2rem 2rem;
  position:sticky;top:0;z-index:100;
  background:rgba(0,0,0,0.7);
  backdrop-filter:blur(8px);
  animation:fadeDown 1s ease;
}
@keyframes fadeDown {
  from{opacity:0; transform:translateY(-20px);} 
  to{opacity:1; transform:translateY(0);} 
}
header .container{
  max-width:1200px;margin:auto;
  display:flex;justify-content:space-between;align-items:center;
}
header h1{color:var(--primary);font-weight:700;font-size:1.6rem;}
header nav ul{display:flex;list-style:none;gap:2rem;}
header nav a{
  color:var(--lighttext);
  text-decoration:none;
  font-weight:500;
  transition:0.3s;
}
header nav a:hover{color:var(--primary);} 

/* HERO */
.hero{
  height:80vh;
  display:flex;justify-content:center;align-items:center;
  text-align:center;
  position:relative;
  overflow:hidden;
}
/* Background animation */
.hero::before{
  content:"";
  position:absolute;inset:0;
  background:radial-gradient(circle at center, #111 0%, #000 100%);
  animation:pulse 6s infinite alternate ease-in-out;
  z-index:-1;
}
@keyframes pulse{
  from{transform:scale(1);} to{transform:scale(1.07);} }

.profile{
  width:170px;height:170px;
  border-radius:50%;background:#333;
  border:4px solid var(--primary);
  margin:auto;margin-bottom:1.4rem;
  box-shadow:0 0 25px rgba(77,166,255,0.3);
  animation:fadeUp 1.2s ease;
}
.hero h2{
  font-size:1.9rem;
  opacity:0;
  animation:slideUp 1.5s 0.3s forwards ease-out;
}
@keyframes slideUp{
  from{opacity:0; transform:translateY(40px);} to{opacity:1; transform:translateY(0);} }
@keyframes fadeUp{
  from{opacity:0; transform:translateY(20px);} to{opacity:1; transform:translateY(0);} }

/* COMPETENCES */
section{
  padding:4rem 0;
}
h2{text-align:center;font-size:2.3rem;margin-bottom:3rem;color:var(--primary);} 
.skills-grid{
  max-width:1100px;margin:auto;
  display:grid;grid-template-columns:repeat(auto-fit, minmax(230px,1fr));
  gap:2rem;
}
.skill-card{
  background:var(--card);
  padding:2rem;border-radius:10px;
  text-align:center;
  box-shadow:0 0 10px rgba(0,0,0,0.5);
  transition:0.4s;
  animation:fadeSlide 1s ease;
}
.skill-card:hover{
  transform:translateY(-10px) scale(1.05);
  box-shadow:0 0 20px rgba(77,166,255,0.6);
}
.skill-card i{
  font-size:3rem;color:var(--primary);margin-bottom:1rem;
  animation:float 3s infinite ease-in-out;
}
@keyframes float{
  0%{transform:translateY(0);} 50%{transform:translateY(-8px);} 100%{transform:translateY(0);} }
@keyframes fadeSlide{
  from{opacity:0; transform:translateY(25px);} to{opacity:1; transform:translateY(0);} }

/* PROJETS */
.projects-grid{
  max-width:1100px;margin:auto;
  display:grid;grid-template-columns:repeat(auto-fit, minmax(300px,1fr));
  gap:2rem;
}
.project-card{
  background:var(--card2);
  padding:2rem;border-radius:10px;
  border-left:4px solid var(--primary);
  opacity:0;
  animation:appear 1s forwards ease;
  box-shadow:0 0 12px rgba(0,0,0,0.6);
}
/* ----- MODIFICATION ICI ----- */
/* J'ai ajouté les délais pour les nouvelles cartes */
.project-card:nth-child(1){animation-delay:0.2s;}
.project-card:nth-child(2){animation-delay:0.4s;}
.project-card:nth-child(3){animation-delay:0.6s;}
.project-card:nth-child(4){animation-delay:0.8s;}
.project-card:nth-child(5){animation-delay:1.0s;}
.project-card:nth-child(6){animation-delay:1.2s;}
/* ----------------------------- */

@keyframes appear{
  from{opacity:0; transform:translateY(25px);} to{opacity:1; transform:translateY(0);} }
.project-card:hover{
  transform:scale(1.03);
  box-shadow:0 0 25px rgba(77,166,255,0.5);
  transition:0.4s;
}

/* CONTACT */
.contact-links{
  margin-top:2rem;
  display:flex;justify-content:center;gap:2rem;
}
.contact-icon i{
  font-size:2.5rem;color:var(--primary);
  transition:0.3s;
}
.contact-icon:hover i{
  transform:scale(1.3);
  color:white;
}

/* FOOTER */
footer{
  text-align:center;padding:1.5rem;background:#0a0a0a;color:#999;margin-top:3rem;
}
</style>
</head>
<body>

<header>
  <div class="container">
  <h1>Jérémy Jerez</h1>
  <nav>
  <ul>
  <li><a href="#accueil">Accueil</a></li>
  <li><a href="#competences">Compétences</a></li>
  <li><a href="#projets">Projets</a></li>
  <li><a href="#contact">Contact</a></li>
  </ul>
  </nav>
  </div>
</header>

<section id="accueil" class="hero">
  <div>
  <div class="profile"></div>
  <h2>Étudiant en école d'ingénieur au CESI de Rouen</h2>
  </div>
</section>

<section id="competences">
  <h2>Compétences</h2>
  <div class="skills-grid">
  <div class="skill-card"><i class="fa-brands fa-c"></i><h3>C++</h3></div>
  <div class="skill-card"><i class="fa-brands fa-python"></i><h3>Python</h3></div>
  <div class="skill-card"><i class="fa-solid fa-file-excel"></i><h3>Suite Office</h3></div>
  <div class="skill-card"><i class="fa-solid fa-palette"></i><h3>Canva</h3></div>
  <div class="skill-card"><i class="fa-solid fa-music"></i><h3>Ableton</h3></div>
  </div>
</section>

<section id="projets">
  <h2>Projets</h2>
  <div class="projects-grid">
  <div class="project-card">
  <h3>Capteur météo – 2025</h3>
  <p>Projet Arduino complet : température, humidité, pression, luminosité, GPS…</p>
  <p>Programmation en C / ATmega328 + carte SD + écran LED.</p>
  </div>
  <div class="project-card">
  <h3>Base de données qualité de l’air – 2025</h3>
  <p>Création, structuration et alimentation d'une base de données complète.</p>
  </div>
  <div class="project-card">
  <h3>Job Étudiant Sanofi – 2025</h3>
  <p>Numérisation, mise à jour d'indications internes, gestion documentaire.</p>
  </div>
  
  <div class="project-card">
  <h3>Nouveau Projet – Année</h3>
  <p>Description courte de ce projet et de ses objectifs principaux.</p>
  <p>Technologies utilisées : Ex: JavaScript, React, Node.js</p>
  </div>
  <div class="project-card">
  <h3>Autre Projet – Année</h3>
  <p>Description courte de ce projet et de ses objectifs principaux.</p>
  <p>Technologies utilisées : Ex: Python, Django, SQL</p>
  </div>
  <div class="project-card">
  <h3>Projet Personnel – Année</h3>
  <p>Description courte de ce projet et de ses objectifs principaux.</p>
  <p>Technologies utilisées : Ex: Figma, HTML, CSS</p>
  </div>
  
  </div>
</section>

<section id="contact" style="text-align:center;">
  <h2>Contact</h2>
  <p>Vous pouvez me contacter via :</p>
  <div class="contact-links">
  <a class="contact-icon" href="mailto:test@example.com"><i class="fas fa-envelope"></i></a>
  <a class="contact-icon" href="#"><i class="fab fa-linkedin"></i></a>
  <a class="contact-icon" href="#"><i class="fab fa-github"></i></a>
  </div>
</section>

<footer>
  <p>© 2025 Jérémy Jerez</p>
</footer>

</body>
</html>

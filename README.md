<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Portfolio - Jérémy Jerez</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css"/>
<style>
:root{
  --primary:#1e1e1e;
  --accent:#6c8aa8;
  --bg:#faf8f6;
  --text:#1a1a1a;
  --card:#ffffff;
  --soft:#e8e4df;
}
*{margin:0;padding:0;box-sizing:border-box;}
body{
  font-family:"Poppins", sans-serif;
  background:var(--dark);
  color:var(--text);
  overflow-x:hidden;
  line-height:1.6;
}
html{scroll-behavior:smooth;}

header{ width:100%; padding:0.6rem 2rem;
  background:var(--bg);
  position:sticky;top:0;z-index:100;
  border-bottom:1px solid var(--soft);
}
header .container{
  max-width:1200px;margin:auto;
  display:flex;justify-content:space-between;align-items:center;
}
header h1{
  font-family:'Didot', serif;
  color:var(--text);
  font-size:3rem;
  font-weight:300;
  letter-spacing:4px;
}
header nav ul{display:flex;list-style:none;gap:2rem;}
header nav a{
  color:var(--text);
  text-decoration:none;
  font-weight:400;
  transition:0.3s;
}
header nav a:hover{color:var(--primary);} 

.hero{
  height:50vh;
  display:flex;justify-content:center;align-items:center;
  text-align:center;
  padding:2rem;
}
.hero h2{
  font-size:2.2rem;
  max-width:700px;
  margin:auto;
  font-weight:600;
}

section{padding:4rem 0;}
h2{text-align:center;font-size:2.2rem;margin-bottom:3rem;color:var(--primary);} 

.skills-grid{
  max-width:1100px;margin:auto;
  display:grid;grid-template-columns:repeat(auto-fit,minmax(230px,1fr));
  gap:2rem;
}
.skill-card{
  background:var(--card);
  padding:2rem;border-radius:12px;
  text-align:center;
  border:1px solid #222;
  transition:0.3s;
}
.skill-card:hover{
  transform:translateY(-6px);
  border-color:var(--primary);
}
.skill-card i{font-size:2.7rem;color:var(--primary);margin-bottom:1rem;}
.skill-card h3{font-weight:500;}

.projects-grid{
  max-width:1100px;margin:auto;
  display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
  gap:2rem;
}
.project-card{
  background:var(--card2);
  padding:2rem;border-radius:12px;
  border-left:4px solid var(--primary);
  transition:0.3s;
}
.project-card:hover{
  transform:translateY(-6px);
  box-shadow:0 0 18px rgba(77,166,255,0.4);
}
.project-card h3{margin-bottom:0.8rem;font-weight:600;}
.project-card p{opacity:0.85;margin-bottom:0.5rem;}

.contact-links{
  margin-top:2rem;
  display:flex;justify-content:center;gap:2rem;
}
.contact-icon i{
  font-size:2.3rem;color:var(--primary);
  transition:0.3s;
}
.contact-icon:hover i{
  transform:scale(1.2);
  color:white;
}

footer{
  text-align:center;padding:1.5rem;background:#050505;color:#aaa;margin-top:3rem;
  font-size:0.9rem;
}
</style>
</head>
<body>

<header>
  <div class="container" style="padding:0.5rem 0;">
    <h1 style="font-size:2rem;">Portfolio</h1>
    <nav>
      <ul>
        <li><a href="#accueil">Accueil</a></li>
        <li><a href="#competences">Compétences</a></li>
        <li><a href="#projets">Projets</a></li>
      </ul>
    </nav>
  </div>
</header>

<section id="accueil" class="hero" style="position:relative; overflow:hidden;">
  <div style="position:absolute; top:-40px; left:-40px; width:180px; height:180px; background:#e5e7eb; border-radius:40px; opacity:0.5; z-index:-1;"></div>
  <div style="position:absolute; bottom:-50px; right:-30px; width:220px; height:220px; background:#dbeafe; border-radius:50%; opacity:0.4; z-index:-1;"></div>
  <div>
    <h2 style="font-size:2.5rem; font-weight:600;">Jérémy Jerez — Étudiant en école d'ingénieur au CESI</h2>
  </div>
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
      <p>Projet Arduino : température, humidité, pression, luminosité, GPS…</p>
      <p>Programmation en C / ATmega328 + carte SD + écran LED.</p>
    </div>

    <div class="project-card">
      <h3>Base de données qualité de l’air – 2025</h3>
      <p>Conception, structuration et alimentation d'une base complète.</p>
    </div>

    <div class="project-card">
      <h3>Job Étudiant Sanofi – 2025</h3>
      <p>Numérisation, mise à jour d'indications internes, gestion documentaire.</p>
    </div>

    <div class="project-card">
      <h3>Nouveau Projet – Année</h3>
      <p>Description courte du projet et de ses objectifs.</p>
    </div>

    <div class="project-card">
      <h3>Autre Projet – Année</h3>
      <p>Description courte du projet et de ses objectifs.</p>
    </div>

    <div class="project-card">
      <h3>Projet Personnel – Année</h3>
      <p>Description du projet personnel.</p>
    </div>

  </div>
</section>



<footer>
  <p>© 2025 Jérémy Jerez</p>
</footer>

</body>
</html>

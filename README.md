<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jérémy Jerez - Portfolio Étudiant</title>
    
    <link rel="stylesheet" href="style.css">
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;700&display=swap" rel="stylesheet">
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
</head>
<body>

    <header class="header-fade-in">
        <div class="container">
            <h1 class="logo">Jérémy Jerez</h1>
            <nav>
                <ul>
                    <li><a href="#accueil">Accueil</a></li>
                    <li><a href="#competences">Compétences</a></li>
                    <li><a href="#projets">Projets CESI</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>

        <section id="accueil" class="hero">
            <div class="container hero-content">
                <div class="profile-placeholder"></div>
                <h2 class="subtitle slide-up">Étudiant en école d'ingénieur au CESI de Rouen</h2>
            </div>
        </section>

        <section id="competences">
            <div class="container">
                <h2>Compétences</h2>
                <div class="skills-grid">
                    <div class="skill-card">
                        <i class="fa-brands fa-c-plus-plus"></i>
                        <h3>C++</h3>
                    </div>
                    <div class="skill-card">
                        <i class="fa-brands fa-python"></i>
                        <h3>Python</h3>
                    </div>
                    <div class="skill-card">
                        <i class="fa-solid fa-language"></i>
                        <h3>Anglais niveau B1</h3>
                    </div>
                    <div class="skill-card">
                        <i class="fa-solid fa-file-excel"></i>
                        <h3>Suite Office</h3>
                        <p>(Excel, Word, PowerPoint)</p>
                    </div>
                    <div class="skill-card">
                        <i class="fa-solid fa-palette"></i>
                        <h3>Canva</h3>
                    </div>
                    <div class="skill-card">
                        <i class="fa-solid fa-music"></i>
                        <h3>Ableton</h3>
                    </div>
                </div>
            </div>
        </section>

        <section id="projets" class="projects-bg">
            <div class="container">
                <h2>Projets CESI</h2>
                <div class="projects-grid">
                    
                    <div class="project-card animate-card">
                        <h3>Projet CESI – 2025 (Capteur météo)</h3>
                        <p>Réalisation d’un capteur météo (Arduino, température, humidité, GPS, pression, luminosité…)</p>
                        <p>Programmation en C avec ATmega328, écran LED, carte SD, horloge RTC.</p>
                    </div>
                    
                    <div class="project-card animate-card">
                        <h3>Projet base de données qualité de l’air – 2025</h3>
                        <p>Création et peuplement d’une base de données sur la qualité de l’air.</p>
                    </div>
                    
                    <div class="project-card animate-card">
                        <h3>Job étudiant Sanofi – 2025</h3>
                        <p>Mise en condition réelle en entreprise, numérisation de documents, mise à jour d’indications internes.</p>
                    </div>

                </div>
            </div>
        </section>

        <section id="contact">
            <div class="container">
                <h2>Contact</h2>
                <p>N'hésitez pas à me contacter par email ou via mes réseaux sociaux.</p>
                <div class="contact-links">
                    <a href="mailto:votre.email@example.com" class="contact-icon">
                        <i class="fas fa-envelope"></i>
                    </a>
                    <a href="tel:+33000000000" class="contact-icon">
                        <i class="fas fa-phone"></i>
                    </a>
                    <a href="#" class="contact-icon">
                        <i class="fab fa-linkedin"></i>
                    </a>
                    <a href="#" class="contact-icon">
                        <i class="fab fa-github"></i>
                    </a>
                </div>
            </div>
        </section>

    </main>

    <footer>
        <div class="container">
            <p>&copy; 2025 Jérémy Jerez. Tous droits réservés.</p>
        </div>
    </footer>

</body>
</html>


/* --- VARIABLES ET RESET GLOBAL --- */
:root {
    --primary-color: #4da6ff; /* Bleu clair demandé */
    --dark-color: #222;       /* Noir (légèrement adouci) */
    --light-color: #f4f4f4;   /* Fond clair pour les sections */
    --white-color: #ffffff;
    --shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth; /* Permet un défilement fluide lors du clic sur le menu */
}

body {
    font-family: 'Montserrat', sans-serif;
    line-height: 1.7;
    background-color: var(--white-color);
    color: var(--dark-color);
}

.container {
    max-width: 1100px;
    margin: auto;
    padding: 0 2rem;
    overflow: hidden; /* Empêche les dépassements */
}

h1, h2, h3 {
    font-weight: 500;
    margin-bottom: 1rem;
}

h2 {
    font-size: 2.2rem;
    text-align: center;
    margin-bottom: 2.5rem;
    color: var(--dark-color);
}

section {
    padding: 4rem 0;
}

/* --- 1. HEADER & NAVIGATION --- */
header {
    background: var(--white-color);
    padding: 1.2rem 0;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

/* Animation Fade-in Header */
@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}
.header-fade-in {
    animation: fadeIn 1s ease-in-out;
}

header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

header .logo {
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--primary-color);
    margin: 0;
}

header nav ul {
    display: flex;
    list-style: none;
}

header nav li {
    margin-left: 2rem;
}

header nav a {
    text-decoration: none;
    color: var(--dark-color);
    font-weight: 500;
    transition: color 0.3s ease;
}

header nav a:hover {
    color: var(--primary-color);
}

/* --- 2. SECTION ACCUEIL (HERO) --- */
.hero {
    background: var(--light-color);
    min-height: 60vh;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
}

.profile-placeholder {
    width: 150px;
    height: 150px;
    background-color: #ccc;
    border-radius: 50%;
    margin: 0 auto 1.5rem auto;
    border: 6px solid var(--white-color);
    box-shadow: var(--shadow);
}

.hero .subtitle {
    font-size: 1.8rem;
    font-weight: 300;
    opacity: 0; /* Caché par défaut pour l'animation */
}

/* Animation Slide-up Texte Accueil */
@keyframes slideUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}
.slide-up {
    animation: slideUp 1s ease-out 0.5s; /* Délai de 0.5s */
    animation-fill-mode: forwards; /* Garde l'état final */
}

/* --- 3. SECTION COMPÉTENCES --- */
.skills-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
}

.skill-card {
    background: var(--white-color);
    padding: 2rem;
    border-radius: 8px;
    box-shadow: var(--shadow);
    text-align: center;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.skill-card i {
    font-size: 2.5rem;
    color: var(--primary-color);
    margin-bottom: 1rem;
}

.skill-card h3 {
    font-size: 1.2rem;
    font-weight: 600;
    margin-bottom: 0.25rem;
}
.skill-card p {
    font-size: 0.9rem;
    font-weight: 300;
}

/* Animation Hover Compétences */
.skill-card:hover {
    transform: translateY(-5px) scale(1.03);
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
}

/* --- 4. SECTION PROJETS CESI --- */
.projects-bg {
    background: var(--light-color);
}

.projects-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
}

.project-card {
    background: var(--white-color);
    padding: 2rem;
    border-radius: 8px;
    box-shadow: var(--shadow);
    border-left: 5px solid var(--primary-color);
    opacity: 0; /* Caché pour animation */
}

.project-card h3 {
    color: var(--primary-color);
    font-weight: 700;
    font-size: 1.2rem;
}

.project-card p {
    font-size: 0.95rem;
    margin-bottom: 0.5rem;
}

/* Animation Apparition Projets */
@keyframes fadeSlideIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.animate-card {
    animation: fadeSlideIn 0.8s ease-out;
    animation-fill-mode: forwards;
}

/* Délai d'animation pour un effet décalé */
.project-card:nth-child(2) {
    animation-delay: 0.2s;
}
.project-card:nth-child(3) {
    animation-delay: 0.4s;
}

/* --- 5. SECTION CONTACT --- */
#contact {
    text-align: center;
}

.contact-links {
    display: flex;
    justify-content: center;
    gap: 2.5rem;
    margin-top: 2rem;
}

.contact-icon i {
    font-size: 2.5rem;
    color: var(--primary-color);
    transition: transform 0.3s ease, color 0.3s ease;
}

/* Animation Hover Contact */
.contact-icon:hover i {
    transform: scale(1.2);
    color: var(--dark-color);
}

/* --- 6. FOOTER --- */
footer {
    background: var(--dark-color);
    color: var(--white-color);
    text-align: center;
    padding: 1.5rem 0;
    margin-top: 2rem;
}

/* --- 7. RESPONSIVE DESIGN (Mobile) --- */
@media (max-width: 768px) {
    h2 {
        font-size: 1.8rem;
    }

    /* Header responsive */
    header .container {
        flex-direction: column;
    }
    header .logo {
        margin-bottom: 0.5rem;
    }
    header nav li {
        margin: 0 0.75rem;
    }

    /* Accueil responsive */
    .hero {
        min-height: 50vh;
    }
    .hero .subtitle {
        font-size: 1.4rem;
    }

    /* Compétences responsive */
    .skills-grid {
        grid-template-columns: repeat(2, 1fr);
    }

    /* Projets responsive */
    .projects-grid {
        grid-template-columns: 1fr;
    }
    
    /* Contact responsive */
    .contact-links {
        gap: 1.5rem;
    }
}

@media (max-width: 480px) {
    /* Compétences responsive (très petit écran) */
    .skills-grid {
        grid-template-columns: 1fr;
    }
}

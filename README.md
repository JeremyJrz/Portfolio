<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Portfolio — Systèmes embarqués (CESI)</title>
  <style>
    :root{
      --bg:#081126; --card:#0e1724; --accent:#00d4ff; --muted:#9fb3c8; --glass: rgba(255,255,255,0.04);
      --radius:16px; --glass-2: rgba(255,255,255,0.02);
    }
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;font-family:Inter,ui-sans-serif,system-ui,-apple-system,'Segoe UI',Roboto,'Helvetica Neue',Arial; background: radial-gradient(1200px 600px at 10% 10%, rgba(0,212,255,0.04), transparent), linear-gradient(180deg,#041226 0%, #071227 60%); color:#e6f2fb}
    a{color:var(--accent); text-decoration:none}

    /* Layout */
    .container{max-width:1100px;margin:48px auto;padding:24px}
    header{display:flex;gap:20px;align-items:center;margin-bottom:24px}
    .logo{width:64px;height:64px;border-radius:12px;background:linear-gradient(135deg,var(--accent),#6effc1);display:grid;place-items:center;font-weight:700;color:#021124;box-shadow:0 8px 30px rgba(0,0,0,0.6)}
    h1{margin:0;font-size:1.6rem}
    p.lead{margin:6px 0 0;color:var(--muted)}

    /* two column */
    .main{display:grid;grid-template-columns:260px 1fr;gap:20px}
    nav.toc{position:sticky;top:28px;padding:18px;background:linear-gradient(180deg,var(--glass),transparent);border-radius:12px;border:1px solid rgba(255,255,255,0.03);height:calc(100vh - 120px);overflow:auto}
    .toc h3{margin:0 0 12px 0;font-size:0.95rem}
    .toc ul{list-style:none;padding:0;margin:0}
    .toc li{margin:8px 0}
    .toc a{display:inline-block;padding:8px 10px;border-radius:10px;color:var(--muted);font-size:0.95rem}
    .toc a.active, .toc a:hover{background:linear-gradient(90deg, rgba(0,212,255,0.06), rgba(110,255,193,0.02));color:var(--accent);box-shadow:0 6px 18px rgba(0,212,255,0.03)}

    /* content cards */
    .content{padding:18px}
    .card{background:linear-gradient(180deg,var(--card), rgba(255,255,255,0.02));padding:18px;border-radius:var(--radius);margin-bottom:18px;border:1px solid rgba(255,255,255,0.03);box-shadow:0 8px 40px rgba(2,8,16,0.6)}
    h2{margin:0 0 8px 0}
    .meta{color:var(--muted);font-size:0.9rem;margin-bottom:12px}
    .project-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:12px}

    /* animated card */
    .proj{position:relative;overflow:hidden;padding:14px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.02));border:1px solid rgba(0,0,0,0.3);backdrop-filter: blur(4px)}
    .proj h3{margin:0 0 6px 0}
    .proj .chip{display:inline-block;padding:6px 8px;border-radius:999px;background:var(--glass-2);font-size:0.8rem;color:var(--muted)}
    .proj p{font-size:0.9rem;color:var(--muted);line-height:1.45}
    .float-glow{position:absolute;right:-30%;top:-40%;width:320px;height:320px;border-radius:50%;background:radial-gradient(circle at 30% 30%, rgba(0,212,255,0.12), transparent 40%), radial-gradient(circle at 70% 70%, rgba(110,255,193,0.06), transparent 30%);filter:blur(18px);transform:rotate(12deg);pointer-events:none}

    /* accordion */
    .accordion{border-radius:10px;overflow:hidden}
    .acc-item{border-bottom:1px solid rgba(255,255,255,0.03)}
    .acc-head{display:flex;justify-content:space-between;align-items:center;padding:12px;cursor:pointer}
    .acc-body{padding:12px 16px;background:linear-gradient(180deg,transparent, rgba(255,255,255,0.01));max-height:0;overflow:hidden;transition:max-height .36s cubic-bezier(.2,.9,.2,1)}
    .acc-item.open .acc-body{max-height:800px}

    /* footer */
    footer{margin-top:18px;text-align:center;color:var(--muted);font-size:0.9rem}

    /* small screens */
    @media (max-width:900px){.main{grid-template-columns:1fr}.toc{display:flex;gap:8px;height:auto;overflow:auto;padding:8px;border-radius:12px}.toc a{white-space:nowrap}}

    /* animations */
    @keyframes floatY{0%{transform:translateY(0)}50%{transform:translateY(-8px)}100%{transform:translateY(0)}}
    header .logo{animation:floatY 5s ease-in-out infinite}
    .proj{transition:transform .26s ease, box-shadow .26s ease}
    .proj:hover{transform:translateY(-8px) scale(1.01);box-shadow:0 20px 50px rgba(2,12,30,0.7)}

    /* smooth scroll */
    html{scroll-behavior:smooth}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="logo">S</div>
      <div>
        <h1>Portfolio — Projet Systèmes embarqués (CESI)</h1>
        <p class="lead">Prototype : Worldwide Weather Watcher — station météo embarquée pour navires</p>
      </div>
    </header>

    <div class="main">
      <nav class="toc" aria-label="Sommaire">
        <div class="toc-inner">
          <h3>Sommaire</h3>
          <ul>
            <li><a href="#intro">Introduction & Sujet</a></li>
            <li><a href="#materiel">Matériel & Capteurs</a></li>
            <li><a href="#modes">Modes de fonctionnement</a></li>
            <li><a href="#livrables">Livrables attendus</a></li>
            <li><a href="#organisation">Organisation / UML</a></li>
            <li><a href="#ressources">Ressources</a></li>
            <li><a href="#contact">Contact / A propos</a></li>
          </ul>

          <hr style="margin:12px 0;border:none;border-top:1px dashed rgba(255,255,255,0.03)">
          <div style="font-size:0.85rem;color:var(--muted)">Quick links</div>
          <ul style="margin-top:8px">
            <li><a href="#pbl">Boucles PBL</a></li>
            <li><a href="#maquette">Maquette / Démo</a></li>
          </ul>
        </div>
      </nav>

      <main class="content">
        <!-- Intro -->
        <section id="intro" class="card">
          <div class="float-glow" aria-hidden="true"></div>
          <h2>Introduction</h2>
          <div class="meta">Projet réalisé au CESI — Station météo embarquée pour navires</div>
          <p>Le projet "Worldwide Weather Watcher" vise à développer une station météo embarquée simple et robuste destinée à équiper des navires. L'objectif est de mesurer des paramètres (pression, température, hygrométrie, luminosité, position GPS...) pour fournir des informations instantanées et enregistrer les données sur carte SD afin d'alimenter des analyses à long terme (prévision de phénomènes extrêmes).</p>
        </section>

        <!-- Matériel -->
        <section id="materiel" class="card">
          <h2>Matériel et capteurs</h2>
          <p class="meta">Plateforme : Arduino (ATmega328) + modules</p>
          <div class="project-grid">
            <div class="proj">
              <h3>Microcontrôleur</h3>
              <div class="chip">AVR ATmega328 (Arduino)</div>
              <p>Le prototype est basé sur une carte Arduino (ATmega328) pour faciliter le prototypage et la mise au point.</p>
            </div>

            <div class="proj">
              <h3>Stockage</h3>
              <div class="chip">Lecteur SD (SPI)</div>
              <p>Enregistrement des données sur carte SD via interface SPI pour logs horodatés.</p>
            </div>

            <div class="proj">
              <h3>Temps</h3>
              <div class="chip">Horloge RTC (I2C)</div>
              <p>RTC pour horodatage fiable des mesures.</p>
            </div>

            <div class="proj">
              <h3>Interface</h3>
              <div class="chip">LED RGB, boutons</div>
              <p>LED RGB pour indiquer l'état système, 2 boutons poussoirs pour interaction simple à bord.</p>
            </div>

            <div class="proj">
              <h3>Capteurs</h3>
              <div class="chip">Pression, Température, Hygrométrie, GPS, Luminosité</div>
              <p>Mix I2C/SPI/analogique/UART selon le capteur (ex: GPS via UART, luminosité analogique).</p>
            </div>
          </div>
        </section>

        <!-- Modes -->
        <section id="modes" class="card">
          <h2>Modes de fonctionnement</h2>
          <p class="meta">Principes</p>
          <div class="accordion">
            <div class="acc-item open">
              <div class="acc-head">Lecture périodique & sauvegarde <span>▶</span></div>
              <div class="acc-body">
                <p>Le système lit périodiquement les capteurs, affiche un état via la LED RGB, et sauvegarde des trames horodatées sur la carte SD. Le protocole de sauvegarde garantit résilience en cas de perte d'alimentation.</p>
              </div>
            </div>
            <div class="acc-item">
              <div class="acc-head">Mode démonstration</div>
              <div class="acc-body"><p>Mode maquette pour la démonstration: envoie d'une série de mesures prédéfinies et présentation du flux via console / démonstration physique.</p></div>
            </div>
            <div class="acc-item">
              <div class="acc-head">Mode interactif</div>
              <div class="acc-body"><p>Interaction via deux boutons : navigation de menus simples (état, export, réinitialisation) et confirmations par LED.</p></div>
            </div>
          </div>
        </section>

        <!-- PBL loops -->
        <section id="pbl" class="card">
          <h2>Boucles PBL (sujets techniques)</h2>
          <p class="meta">Enchaînement pédagogique — tâches attendues</p>
          <ol>
            <li>Boucle PBL Analyse fonctionnelle</li>
            <li>Boucle PBL Assembleur et instructions</li>
            <li>Boucle PBL Assemblage Automates</li>
            <li>Boucle PBL Assemblage Mémoire</li>
            <li>Boucle PBL Pile</li>
            <li>Boucle PBL Interruptions</li>
            <li>Boucle PBL Système de fichiers</li>
          </ol>
          <p>Chaque "prosit" correspond à une demande fonctionnelle à implémenter d'ici la fin du projet — les fonctionnalités demandées s'intègrent donc au produit final.</p>
        </section>

        <!-- Livrables -->
        <section id="livrables" class="card">
          <h2>Livrables attendus</h2>
          <div class="project-grid">
            <div class="proj">
              <h3>Livrable 1 — Analyse du système</h3>
              <p>Diagrammes UML/SysML, algorithmes, schémas et explications. Format : rapport d'analyse.</p>
            </div>
            <div class="proj">
              <h3>Livrable 2 — Architecture du programme</h3>
              <p>Structure générale du logiciel (fonctions, modules, variables). Livrable non évolutif.</p>
            </div>
            <div class="proj">
              <h3>Livrable 3 — Maquette</h3>
              <p>Programme complet, script de compilation/téléversement, montage minimal et scénario de démonstration.</p>
            </div>
            <div class="proj">
              <h3>Livrable 4 — Documentation</h3>
              <p>Documentation technique et guide utilisateur (fonctionnement, performances, schémas).</p>
            </div>
          </div>
        </section>

        <!-- Architecture / UML -->
        <section id="organization" class="card" aria-labelledby="organization">
          <h2 id="organization">Organisation & UML</h2>
          <p class="meta">Recommandation</p>
          <p>Proposez des diagrammes de cas d'utilisation (utilisateurs : équipage, maintenance), diagrammes de classes/modules (DataLogger, SensorManager, Comm, UI), et séquences pour le scénario de démarrage, lecture capteur, sauvegarde SD et gestion d'interruption (ex: GPS reçu ou bouton pressé).</p>
        </section>

        <!-- Maquette -->
        <section id="maquette" class="card">
          <h2>Maquette / Démo</h2>
          <p class="meta">Attendus pour la démonstration</p>
          <ul>
            <li>Code complet et script de téléversement (Makefile ou script .bat/.sh)</li>
            <li>Montage minimal centré sur la carte Arduino</li>
            <li>Scénario de démonstration et questions-réponses</li>
          </ul>
        </section>

        <!-- Resources -->
        <section id="ressources" class="card">
          <h2>Ressources pour les étudiants</h2>
          <p class="meta">Fichiers et matériels</p>
          <p>Inclure : schémas de câblage, références de capteurs, datasheets (RTC, SD, capteurs I2C/SPI), et tableur de grille d'auto-évaluation.</p>
        </section>

        <section id="contact" class="card">
          <h2>À propos / Contact</h2>
          <p class="meta">Auteur : Jérémy Jerez — CESI</p>
          <p>Ce portfolio présente le projet réalisé dans le cadre du cursus. Pour modifications, amélioration d'animations ou génération d'une version imprimable, dis-moi ce que tu veux changer.</p>
        </section>

        <footer>
          <div>Version interactive — Animation CSS + JS minimale</div>
        </footer>
      </main>
    </div>
  </div>

  <script>
    // Smooth TOC active tracking
    const tocLinks = Array.from(document.querySelectorAll('.toc a'));
    const sections = tocLinks.map(a => document.querySelector(a.getAttribute('href')));
    function onScroll(){
      const middle = window.scrollY + window.innerHeight/3;
      let activeIndex = 0;
      for(let i=0;i<sections.length;i++){
        if(sections[i] && sections[i].offsetTop <= middle) activeIndex = i;
      }
      tocLinks.forEach((a,i)=> a.classList.toggle('active', i===activeIndex));
    }
    window.addEventListener('scroll', onScroll);
    onScroll();

    // Accordion
    document.querySelectorAll('.acc-head').forEach(h=>{
      h.addEventListener('click', ()=>{
        const item = h.parentElement;
        item.classList.toggle('open');
      });
    });

    // Mobile toc touch: prevent losing focus
    document.querySelectorAll('.toc a').forEach(a=>a.addEventListener('click', ()=>{if(window.innerWidth<900) window.scrollBy(0,-12)}));
  </script>
</body>
</html>

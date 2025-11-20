:root {
  --primary:#1e1e1e;
  --accent:#6c8aa8;
  --bg:#faf8f6;
  --text:#1a1a1a;
  --card:#ffffff;
  --soft:#e8e4df;
  --skill-blue:#faf7f2;
}

body {
  font-family: 'Roboto', sans-serif; /* Uniformité */
}

.project-card {
  background: var(--card); /* Correction */
}

.contact-icon:hover i {
  transform: scale(1.2);
  color: white;
  background-color: var(--accent); /* Meilleure visibilité */
  border-radius: 50%;
  padding: 0.5rem;
}


<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Baby Girl Coach — Programme Nutrition & Sport</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Fraunces:ital,wght@0,300;0,500;1,400&family=Manrope:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #1c0a14;
    --bg-soft: #2a0f1c;
    --card: #33131f;
    --pink: #ff4d76;
    --pink-soft: #ffb0c2;
    --gold: #f0c14b;
    --cream: #fff3ec;
    --cream-dim: #e8cfd0;
    --line: rgba(255,243,236,0.14);
  }
  *{margin:0;padding:0;box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--bg);
    color:var(--cream);
    font-family:'Manrope', sans-serif;
    overflow-x:hidden;
  }
  .display{font-family:'Bebas Neue', sans-serif; letter-spacing:0.03em;}
  .script{font-family:'Fraunces', serif; font-style:italic; font-weight:300;}

  /* subtle noise/glow background */
  body::before{
    content:"";
    position:fixed; inset:0;
    background:
      radial-gradient(ellipse 60% 40% at 15% 0%, rgba(255,77,118,0.16), transparent 60%),
      radial-gradient(ellipse 50% 40% at 100% 20%, rgba(240,193,75,0.10), transparent 60%);
    pointer-events:none;
    z-index:0;
  }

  .wrap{max-width:1080px; margin:0 auto; padding:0 24px; position:relative; z-index:1;}

  /* NAV */
  nav{
    display:flex; align-items:center; justify-content:space-between;
    padding:22px 24px; max-width:1080px; margin:0 auto; position:relative; z-index:5;
  }
  .brand{display:flex; align-items:baseline; gap:6px;}
  .brand-mark{font-family:'Bebas Neue'; font-size:1.5rem; letter-spacing:0.06em;}
  .brand-mark .accent{color:var(--pink);}
  nav a.cta{
    border:1px solid var(--pink); color:var(--cream);
    padding:9px 18px; border-radius:100px; text-decoration:none;
    font-size:0.82rem; font-weight:700; letter-spacing:0.02em;
    transition:background 0.25s ease, transform 0.2s ease;
  }
  nav a.cta:hover{background:var(--pink); transform:translateY(-1px);}

  /* HERO */
  .hero{
    padding:60px 24px 90px;
    max-width:1080px; margin:0 auto;
    position:relative; z-index:1;
  }
  .eyebrow{
    display:inline-flex; align-items:center; gap:8px;
    font-size:0.75rem; letter-spacing:0.14em; text-transform:uppercase;
    color:var(--pink-soft); font-weight:700; margin-bottom:22px;
  }
  .eyebrow::before{
    content:""; width:26px; height:1px; background:var(--pink-soft);
  }
  h1.hero-title{
    font-size:clamp(2.8rem, 8vw, 5.6rem);
    line-height:0.94;
    text-transform:uppercase;
  }
  h1.hero-title .line2{color:var(--pink);}
  h1.hero-title .amp{
    font-family:'Fraunces'; font-style:italic; font-weight:300;
    text-transform:none; color:var(--gold); font-size:0.6em;
  }
  .hero-sub{
    margin-top:26px; max-width:480px;
    font-size:1.05rem; line-height:1.65; color:var(--cream-dim);
  }
  .hero-actions{margin-top:38px; display:flex; gap:16px; flex-wrap:wrap; align-items:center;}
  .btn-primary{
    background:var(--pink); color:#1c0a14; text-decoration:none;
    padding:15px 30px; border-radius:100px; font-weight:800; font-size:0.95rem;
    display:inline-flex; align-items:center; gap:10px;
    transition:transform 0.2s ease, box-shadow 0.2s ease;
    box-shadow:0 8px 24px rgba(255,77,118,0.25);
  }
  .btn-primary:hover{transform:translateY(-2px); box-shadow:0 12px 28px rgba(255,77,118,0.35);}
  .btn-ghost{
    color:var(--cream-dim); text-decoration:none; font-size:0.9rem; font-weight:600;
    border-bottom:1px solid var(--line); padding-bottom:2px;
  }

  /* signature pulse-heart */
  .signature{
    margin-top:70px; display:flex; align-items:center; gap:22px;
  }
  .pulse-wrap{width:190px; height:70px; flex-shrink:0;}
  .pulse-wrap svg{width:100%; height:100%; overflow:visible;}
  .pulse-line{
    fill:none; stroke:var(--pink); stroke-width:2.5; stroke-linecap:round; stroke-linejoin:round;
    stroke-dasharray:300; stroke-dashoffset:300;
    animation:draw 2.6s ease-in-out infinite;
  }
  @keyframes draw{
    0%{stroke-dashoffset:300;}
    45%{stroke-dashoffset:0;}
    100%{stroke-dashoffset:-300;}
  }
  .signature-text{font-size:0.85rem; color:var(--cream-dim); line-height:1.5; max-width:260px;}
  .signature-text b{color:var(--cream); font-weight:700;}

  /* SECTION LABELS */
  .section{padding:70px 24px; max-width:1080px; margin:0 auto; position:relative; z-index:1;}
  .section-head{margin-bottom:44px;}
  .section-num{
    font-size:0.78rem; color:var(--pink-soft); font-weight:700;
    letter-spacing:0.14em; text-transform:uppercase; margin-bottom:12px;
  }
  h2.section-title{
    font-family:'Bebas Neue'; font-size:clamp(2.1rem, 5vw, 3.2rem);
    text-transform:uppercase; line-height:1;
  }
  h2.section-title .script{text-transform:none; color:var(--gold); font-size:0.9em;}
  .section-desc{margin-top:16px; color:var(--cream-dim); max-width:520px; line-height:1.6;}

  /* SERVICES */
  .services{
    display:grid; grid-template-columns:repeat(3, 1fr); gap:20px;
  }
  .service-card{
    background:var(--card);
    border:1px solid var(--line);
    border-radius:20px;
    padding:32px 26px;
    position:relative;
    overflow:hidden;
    transition:transform 0.25s ease, border-color 0.25s ease;
  }
  .service-card:hover{transform:translateY(-4px); border-color:rgba(255,77,118,0.4);}
  .service-card::after{
    content:""; position:absolute; top:-40px; right:-40px;
    width:120px; height:120px; border-radius:50%;
    background:radial-gradient(circle, rgba(255,77,118,0.14), transparent 70%);
  }
  .service-icon{
    width:46px; height:46px; border-radius:12px;
    background:rgba(255,77,118,0.14);
    display:flex; align-items:center; justify-content:center;
    margin-bottom:22px;
  }
  .service-icon svg{width:22px; height:22px; stroke:var(--pink); fill:none; stroke-width:1.8;}
  .service-card h3{
    font-family:'Bebas Neue'; font-size:1.5rem; text-transform:uppercase; letter-spacing:0.02em;
    margin-bottom:12px;
  }
  .service-card p{color:var(--cream-dim); font-size:0.92rem; line-height:1.6;}
  .service-tag{
    display:inline-block; margin-top:18px;
    font-size:0.72rem; letter-spacing:0.06em; text-transform:uppercase;
    color:var(--gold); font-weight:700;
  }

  /* PROCESS / TIMELINE (abonnement duration) */
  .timeline{
    display:flex; flex-direction:column; gap:0;
    border-top:1px solid var(--line);
  }
  .timeline-row{
    display:grid; grid-template-columns:70px 1fr;
    gap:22px; padding:26px 0;
    border-bottom:1px solid var(--line);
    align-items:start;
  }
  .timeline-week{font-family:'Bebas Neue'; font-size:1.1rem; color:var(--pink-soft);}
  .timeline-row h4{font-size:1.05rem; font-weight:700; margin-bottom:6px;}
  .timeline-row p{color:var(--cream-dim); font-size:0.9rem; line-height:1.6; max-width:520px;}

  /* FORM SECTION */
  .form-section{
    background:var(--bg-soft);
    border-radius:28px;
    padding:56px 40px;
    margin:70px 24px 0;
    position:relative; z-index:1;
    border:1px solid var(--line);
  }
  .form-inner{max-width:640px; margin:0 auto;}
  .form-head{text-align:center; margin-bottom:38px;}
  .form-head h2{font-family:'Bebas Neue'; font-size:clamp(2rem,5vw,2.8rem); text-transform:uppercase;}
  .form-head p{color:var(--cream-dim); margin-top:12px; font-size:0.95rem;}
  form{display:grid; grid-template-columns:1fr 1fr; gap:18px;}
  .field{display:flex; flex-direction:column; gap:8px;}
  .field.full{grid-column:1 / -1;}
  label{font-size:0.78rem; text-transform:uppercase; letter-spacing:0.06em; color:var(--pink-soft); font-weight:700;}
  input, select{
    background:rgba(255,243,236,0.05);
    border:1px solid var(--line);
    border-radius:12px;
    padding:14px 16px;
    color:var(--cream);
    font-family:'Manrope';
    font-size:0.95rem;
    outline:none;
    transition:border-color 0.2s ease, background 0.2s ease;
  }
  input::placeholder{color:rgba(255,243,236,0.35);}
  input:focus, select:focus{border-color:var(--pink); background:rgba(255,243,236,0.08);}
  select{appearance:none; -webkit-appearance:none;}
  .field.select-wrap{position:relative;}
  .field.select-wrap::after{
    content:"▾"; position:absolute; right:16px; top:41px; color:var(--pink-soft); pointer-events:none; font-size:0.8rem;
  }
  .submit-row{grid-column:1 / -1; margin-top:10px;}
  button.whatsapp-btn{
    width:100%;
    background:var(--pink);
    color:#1c0a14;
    border:none;
    border-radius:100px;
    padding:17px 24px;
    font-family:'Manrope';
    font-weight:800;
    font-size:1rem;
    cursor:pointer;
    display:flex; align-items:center; justify-content:center; gap:10px;
    transition:transform 0.2s ease, box-shadow 0.2s ease;
    box-shadow:0 8px 24px rgba(255,77,118,0.25);
  }
  button.whatsapp-btn:hover{transform:translateY(-2px); box-shadow:0 12px 30px rgba(255,77,118,0.35);}
  button.whatsapp-btn svg{width:20px; height:20px; fill:#1c0a14;}
  .form-note{
    text-align:center; margin-top:16px; font-size:0.78rem; color:var(--cream-dim); opacity:0.8;
  }

  footer{
    text-align:center; padding:50px 24px 34px; color:var(--cream-dim); font-size:0.82rem;
    position:relative; z-index:1;
  }
  footer .brand-mark{justify-content:center; display:flex; margin-bottom:10px;}

  @media (max-width: 780px){
    .services{grid-template-columns:1fr;}
    form{grid-template-columns:1fr;}
    .field.select-wrap::after{top:41px;}
    .form-section{padding:40px 22px; margin:60px 14px 0;}
    .signature{flex-direction:column; align-items:flex-start; gap:14px;}
  }

  @media (prefers-reduced-motion: reduce){
    .pulse-line{animation:none; stroke-dashoffset:0;}
  }
</style>
</head>
<body>

<nav>
  <div class="brand">
    <span class="brand-mark">BABY GIRL <span class="accent">COACH</span></span>
  </div>
  <a class="cta" href="#reserver">Réserver</a>
</nav>

<header class="hero">
  <div class="eyebrow">Coaching nutrition & sport</div>
  <h1 class="hero-title">
    TON CORPS,<br>
    <span class="line2">TA RÈGLE.</span>
  </h1>
  <p class="hero-sub">
    Un programme d'alimentation fait pour toi, des séances d'entraînement adaptées à ton niveau,
    et un suivi réel jusqu'au bout de ton abonnement. Pas de plan générique — que du sur-mesure.
  </p>
  <div class="hero-actions">
    <a href="#reserver" class="btn-primary">
      Démarrer mon programme
    </a>
    <a href="#services" class="btn-ghost">Voir comment ça marche</a>
  </div>

  <div class="signature">
    <div class="pulse-wrap">
      <svg viewBox="0 0 190 70" preserveAspectRatio="none">
        <path class="pulse-line" d="M0,35 L35,35 L48,10 L60,60 L72,35 L84,35 L92,20 L100,48 L108,35 L190,35"/>
      </svg>
    </div>
    <div class="signature-text">
      <b>Un seul rythme à suivre : le tien.</b> Chaque programme est ajusté semaine après semaine selon tes résultats.
    </div>
  </div>
</header>

<section class="section" id="services">
  <div class="section-head">
    <div class="section-num">01 — Ce qui est inclus</div>
    <h2 class="section-title">Trois piliers, <span class="script">un seul objectif</span></h2>
    <p class="section-desc">Ton abonnement combine ces trois services, pensés pour avancer ensemble et non séparément.</p>
  </div>

  <div class="services">
    <div class="service-card">
      <div class="service-icon">
        <svg viewBox="0 0 24 24"><path d="M12 3c-3 3-6 6-6 10a6 6 0 0012 0c0-4-3-7-6-10z"/></svg>
      </div>
      <h3>Programme de repas</h3>
      <p>Un plan alimentaire personnalisé selon ton poids, ta taille, tes goûts et ton objectif — perte de poids, prise de masse ou maintien.</p>
      <span class="service-tag">Nutrition</span>
    </div>

    <div class="service-card">
      <div class="service-icon">
        <svg viewBox="0 0 24 24"><path d="M6.5 6.5l11 11M4 9l3-3M9 4l-3 3M15 20l3-3M20 15l-3 3M2 6l4 4M18 14l4 4"/></svg>
      </div>
      <h3>Programme d'entraînement</h3>
      <p>Des séances d'exercices adaptées à ton niveau et ton matériel disponible, à la salle ou à la maison.</p>
      <span class="service-tag">Sport</span>
    </div>

    <div class="service-card">
      <div class="service-icon">
        <svg viewBox="0 0 24 24"><path d="M3 17l5-5 4 4 8-8M14 8h6v6"/></svg>
      </div>
      <h3>Suivi continu</h3>
      <p>Un accompagnement tout au long de ton abonnement : ajustements, réponses à tes questions, motivation constante.</p>
      <span class="service-tag">Suivi</span>
    </div>
  </div>
</section>

<section class="section">
  <div class="section-head">
    <div class="section-num">02 — Le déroulé</div>
    <h2 class="section-title">De la <span class="script">réservation</span> au résultat</h2>
  </div>

  <div class="timeline">
    <div class="timeline-row">
      <div class="timeline-week">Étape 1</div>
      <div>
        <h4>Tu remplis le formulaire</h4>
        <p>Nom, ville, poids et taille — les infos de base pour construire ton profil.</p>
      </div>
    </div>
    <div class="timeline-row">
      <div class="timeline-week">Étape 2</div>
      <div>
        <h4>On discute sur WhatsApp</h4>
        <p>Le formulaire t'envoie directement sur WhatsApp avec tes infos déjà prêtes — on ajuste les détails ensemble.</p>
      </div>
    </div>
    <div class="timeline-row">
      <div class="timeline-week">Étape 3</div>
      <div>
        <h4>Tu reçois ton programme</h4>
        <p>Plan de repas + programme d'entraînement personnalisés, prêts à suivre dès le premier jour.</p>
      </div>
    </div>
    <div class="timeline-row">
      <div class="timeline-week">Étape 4</div>
      <div>
        <h4>Suivi jusqu'au bout</h4>
        <p>Tout au long de ton abonnement, ajustements et accompagnement selon ton évolution.</p>
      </div>
    </div>
  </div>
</section>

<section class="form-section" id="reserver">
  <div class="form-inner">
    <div class="form-head">
      <h2>Réserve ta place</h2>
      <p>Remplis ce formulaire, il t'enverra directement sur WhatsApp avec tes infos.</p>
    </div>
    <form id="bookingForm">
      <div class="field full">
        <label for="name">Nom complet</label>
        <input type="text" id="name" placeholder="Ton nom" required>
      </div>
      <div class="field">
        <label for="city">Ville</label>
        <input type="text" id="city" placeholder="Ta ville" required>
      </div>
      <div class="field select-wrap">
        <label for="goal">Objectif</label>
        <select id="goal">
          <option value="Perte de poids">Perte de poids</option>
          <option value="Prise de masse">Prise de masse</option>
          <option value="Maintien / tonification">Maintien / tonification</option>
        </select>
      </div>
      <div class="field">
        <label for="weight">Poids (kg)</label>
        <input type="number" id="weight" placeholder="ex: 65" min="20" max="250" required>
      </div>
      <div class="field">
        <label for="height">Taille (cm)</label>
        <input type="number" id="height" placeholder="ex: 165" min="100" max="230" required>
      </div>
      <div class="submit-row">
        <button type="submit" class="whatsapp-btn">
          <svg viewBox="0 0 24 24"><path d="M17.6 6.3A8.8 8.8 0 0012 4a8.9 8.9 0 00-7.7 13.4L3 21l3.7-1.2A8.9 8.9 0 0012 21a8.9 8.9 0 006.3-15.2c-.2-.2-.5-.4-.7-.5zM12 19.3a7.3 7.3 0 01-3.7-1l-.3-.2-2.7.9.9-2.6-.2-.3A7.4 7.4 0 1112 19.3zm4-5.5c-.2-.1-1.3-.6-1.5-.7s-.4-.1-.5.1-.6.7-.7.8-.3.2-.5.1a6 6 0 01-1.8-1.1 6.6 6.6 0 01-1.2-1.5c-.1-.2 0-.4.1-.5l.3-.4.2-.3a.4.4 0 000-.4c0-.1-.5-1.3-.7-1.7s-.4-.4-.5-.4h-.5a.9.9 0 00-.6.3 2.7 2.7 0 00-.9 2 4.7 4.7 0 001 2.5 10.7 10.7 0 004.1 3.6c.6.2 1 .4 1.4.5a3.4 3.4 0 001.5.1 2.5 2.5 0 001.6-1.1 1.9 1.9 0 00.1-1.1c-.1-.1-.2-.2-.4-.3z"/></svg>
          Envoyer sur WhatsApp
        </button>
      </div>
    </form>
    <p class="form-note">En envoyant, tu seras redirigée vers WhatsApp avec tes informations déjà remplies.</p>
  </div>
</section>

<footer>
  <div class="brand-mark">BABY GIRL <span style="color:var(--pink)">&nbsp;COACH</span></div>
  Coaching nutrition & sport — sur mesure, du premier jour au dernier.
</footer>

<script>
document.getElementById('bookingForm').addEventListener('submit', function(e){
  e.preventDefault();
  const name = document.getElementById('name').value.trim();
  const city = document.getElementById('city').value.trim();
  const goal = document.getElementById('goal').value;
  const weight = document.getElementById('weight').value.trim();
  const height = document.getElementById('height').value.trim();

  const message =
    `Salam, je m'appelle ${name}.\n` +
    `Ville: ${city}\n` +
    `Objectif: ${goal}\n` +
    `Poids: ${weight} kg\n` +
    `Taille: ${height} cm\n` +
    `Je veux démarrer mon programme avec Baby Girl Coach.`;

  const phone = "212675451136";
  const url = `https://wa.me/${phone}?text=${encodeURIComponent(message)}`;
  window.open(url, '_blank');
});
</script>

</body>
</html>

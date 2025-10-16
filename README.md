<html lang="fr">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<meta name="description" content="StaynB - Conciergerie Airbnb en Île-de-France. Gestion complète, accueil voyageurs, ménage, optimisation, estimation de revenus." />
<title>StaynB — Conciergerie Airbnb (Île-de-France)</title>

<!-- Fonts & icons -->
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@500;700&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

/* ✅ Correction d’affichage GitHub Pages */
html, body {
  margin: 0 !important;
  padding: 0 !important;
  width: 100%;
  max-width: 100%;
}

body > div {
  margin: 0 !important;
  padding: 0 !important;
  width: 100%;
  max-width: 100%;
}

section, header, footer {
  width: 100%;
  max-width: 100%;
  margin: 0 auto;
}

<style>
:root{
  --bg:#FAFBFC;
  --card:#fff;
  --text:#1E1E2F;
  --muted:#6F6F7A;
  --accent:#F5B642;
  --accent-2:#FF5A5F;
  --shadow:0 8px 24px rgba(18,23,44,0.06);
  --radius:14px;
  --maxw:90vw;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{margin:0;background:var(--bg);color:var(--text);font-family:Inter, Montserrat, system-ui;line-height:1.45;-webkit-font-smoothing:antialiased}
a{color:inherit;text-decoration:none}

/* Header */
header{
  position:sticky;top:0;z-index:1200;
  backdrop-filter: blur(6px);
  background:rgba(255,255,255,0.75);
  border-bottom:1px solid rgba(16,24,40,0.04);
  display:flex;align-items:center;justify-content:space-between;padding:10px 20px;
}
.brand{display:flex;align-items:center;gap:12px}
.logo-mark{width:44px;height:44px;border-radius:10px;background:linear-gradient(135deg,var(--text),var(--accent));display:flex;align-items:center;justify-content:center;color:white;font-weight:700;font-family:Montserrat}
.brand h1{font-size:1rem;margin:0;font-weight:700}
nav{display:flex;gap:16px;align-items:center}
nav a{font-weight:600;font-size:0.95rem;padding:8px 10px;border-radius:8px;text-decoration:none}
.cta-quick{background: linear-gradient(135deg,#FF5A5F,#FFB67B);color:white;font-weight:700;padding:10px 20px;border-radius:50px;cursor:pointer}
.cta-quick:hover{transform:translateY(-2px);box-shadow:0 6px 16px rgba(0,0,0,0.12)}

/* Buttons */
.btn {padding:12px 22px;border-radius:50px;border:none;font-weight:600;cursor:pointer;font-size:0.95rem;transition:all .25s ease;box-shadow:0 4px 12px rgba(0,0,0,0.08);}
.btn-primary{background:linear-gradient(135deg,#FF5A5F,#FFB67B);color:white;font-weight:700;}
.btn-outline{background:transparent;border:2px solid #FF5A5F;color:#FF5A5F;}

/* Hero */
.hero{position:relative;min-height:72vh;display:flex;align-items:center;justify-content:center;padding:60px 20px;overflow:hidden;}

/* === NOUVEAU : vidéo auto-hébergée en fond === */
.hero .bg-iframe {
  position:absolute;
  top:0;
  left:0;
  width:100%;
  height:100%;
  z-index:0;
  overflow:hidden;
}
.hero .bg-iframe video{
  position:absolute;
  top:50%;
  left:50%;
  width:145%;
  height:145%;
  object-fit:cover;
  transform:translate(-50%,-50%);
  border:0;
  filter:brightness(1);
}
.hero::after{
  content:"";
  position:absolute;
  inset:0;
  background:linear-gradient(135deg, rgba(255,90,95,0.25), rgba(245,182,66,0.25));
  z-index:1;
}

.hero-inner{max-width:var(--maxw);width:100%;display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center;position:relative;z-index:2}
.hero-card{background:var(--card);padding:36px;border-radius:var(--radius);box-shadow:var(--shadow)}
.hero h2{font-family:Montserrat;font-size:1.6rem;margin:0 0 12px}
.hero p{color:var(--muted);margin:0 0 18px}
.hero-actions{display:flex;gap:12px;flex-wrap:wrap}
.hero-side{display:flex;flex-direction:column;gap:12px}
.stat{background:linear-gradient(180deg, rgba(255,255,255,0.9), #fff);padding:14px;border-radius:12px;text-align:center;box-shadow:0 8px 20px rgba(18,23,44,0.04)}

/* Animation fade-up */
.fade-up {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.6s ease;
}
.fade-up.visible {
  opacity: 1;
  transform: translateY(0);
}
</style>
</head>

<body>

<!-- HEADER -->
<header>
  <div class="brand" aria-label="StaynB">
    <a href="https://stayn-b.github.io/" class="logo-link">
      <img src="./image0.png" alt="Logo StaynB" style="height:70px; vertical-align:middle; border-radius:10px;">
    </a>
    <div>
      <h1>StaynB</h1>
      <div style="font-size:12px;color:var(--muted)">Conciergerie • Île-de-France</div>
    </div>
  </div>
</header>

<!-- HERO -->
<section class="hero" aria-label="Hero StaynB">
  <!-- ✅ Vidéo auto-hébergée à la place de YouTube -->
  <div class="bg-iframe" aria-hidden="true">
    <video autoplay muted loop playsinline poster="media/fallback.jpg">
      <source src="media/paris-bg.mp4" type="video/mp4">
      <source src="media/paris-bg.webm" type="video/webm">
      Votre navigateur ne supporte pas la vidéo.
    </video>
  </div>

  <div class="hero-inner container" style="position:relative;z-index:2">
    <div class="hero-card fade-up">
      <h2>Gérez vos locations sans stress — maximisez vos revenus et offrez une expérience mémorable.</h2>
      <p class="lead">StaynB prend en charge l'accueil, le ménage, la maintenance et l'optimisation de vos annonces en Île-de-France.</p>
      <div class="hero-actions">
        <button class="btn btn-primary" id="ctaEstimate">Faire une estimation</button>
        <button class="btn btn-outline" id="ctaPacks">Voir les packs</button>
      </div>

      <div style="margin-top:18px;display:flex;gap:16px;flex-wrap:wrap">
        <div style="display:flex;gap:10px;align-items:center">
          <div style="width:44px;height:44px;border-radius:12px;background:linear-gradient(135deg,var(--accent),var(--accent-2));display:flex;align-items:center;justify-content:center;color:white;font-weight:700">★</div>
          <div>
            <div style="font-weight:700">4.9/5</div>
            <div style="font-size:13px;color:var(--muted)">Note moyenne</div>
          </div>
        </div>
        <div style="display:flex;gap:10px;align-items:center">
          <div style="width:44px;height:44px;border-radius:12px;background:linear-gradient(135deg,var(--accent-2),#FFB67B);display:flex;align-items:center;justify-content:center;color:#111;font-weight:700">⟳</div>
          <div>
            <div style="font-weight:700">+30%</div>
            <div style="font-size:13px;color:var(--muted)">Revenus optimisés (moy.)</div>
          </div>
        </div>
      </div>
    </div>

    <aside class="hero-side" aria-label="Stats">
      <div class="stat fade-up">
        <div style="font-size:12px;color:var(--muted)">Revenu moyen/mois</div>
        <div style="font-size:20px;font-weight:700">1 650 €</div>
      </div>
      <div class="stat fade-up">
        <div style="font-size:12px;color:var(--muted)">Taux d’occupation</div>
        <div style="font-size:20px;font-weight:700">78 %</div>
      </div>
      <div class="stat fade-up">
        <div style="font-size:12px;color:var(--muted)">Clients satisfaits</div>
        <div style="font-size:20px;font-weight:700">+120</div>
      </div>
    </aside>
  </div>
</section>

<!-- SERVICES -->
<section id="services" aria-label="Nos services" style="padding:80px 20px;background:var(--card)">
  <div style="max-width:var(--maxw);margin:0 auto;text-align:center">
    <h2 style="font-family:Montserrat;font-size:2rem;margin-bottom:10px">Nos services</h2>
    <p style="color:var(--muted);max-width:700px;margin:0 auto 40px">Une gestion complète de votre location courte durée, de l’annonce à l’entretien, avec transparence et efficacité.</p>

    <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:26px;margin-top:40px">
      <div style="background:var(--bg);border-radius:var(--radius);padding:28px;box-shadow:var(--shadow);text-align:center">
        <i class="fa-solid fa-key" style="font-size:32px;color:var(--accent-2);margin-bottom:16px"></i>
        <h3 style="margin:0 0 10px">Check-in & Check-out</h3>
        <p style="color:var(--muted)">Accueil des voyageurs, remise des clés, et vérification de l’état du logement à chaque départ.</p>
      </div>

      <div style="background:var(--bg);border-radius:var(--radius);padding:28px;box-shadow:var(--shadow);text-align:center">
        <i class="fa-solid fa-broom" style="font-size:32px;color:var(--accent-2);margin-bottom:16px"></i>
        <h3 style="margin:0 0 10px">Ménage professionnel</h3>
        <p style="color:var(--muted)">Nettoyage complet et gestion du linge par nos équipes partenaires.</p>
      </div>

      <div style="background:var(--bg);border-radius:var(--radius);padding:28px;box-shadow:var(--shadow);text-align:center">
        <i class="fa-solid fa-chart-line" style="font-size:32px;color:var(--accent-2);margin-bottom:16px"></i>
        <h3 style="margin:0 0 10px">Optimisation des revenus</h3>
        <p style="color:var(--muted)">Ajustement dynamique des tarifs et des disponibilités selon la demande locale et la saison.</p>
      </div>

      <div style="background:var(--bg);border-radius:var(--radius);padding:28px;box-shadow:var(--shadow);text-align:center">
        <i class="fa-solid fa-comments" style="font-size:32px;color:var(--accent-2);margin-bottom:16px"></i>
        <h3 style="margin:0 0 10px">Support voyageurs 24/7</h3>
        <p style="color:var(--muted)">Réponses rapides et assistance aux voyageurs à toute heure.</p>
      </div>
    </div>
  </div>
</section>

<!-- PACKS -->
<section id="pricing" style="padding:80px 20px">
  <div style="max-width:var(--maxw);margin:0 auto;text-align:center">
    <h2 style="font-family:Montserrat;font-size:2rem;margin-bottom:10px">Nos packs & tarifs</h2>
    <p style="color:var(--muted);max-width:700px;margin:0 auto 40px">Choisissez la formule qui correspond à votre besoin. Aucune mauvaise surprise : nos tarifs sont transparents.</p>

    <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:26px;margin-top:40px">
      <div style="background:var(--card);padding:36px;border-radius:var(--radius);box-shadow:var(--shadow)">
        <h3>Pack Essentiel</h3>
        <p style="font-size:1.3rem;font-weight:700;color:var(--accent-2)">15 % de commission</p>
        <ul style="list-style:none;padding:0;text-align:left;line-height:1.8">
          <li>✔ Accueil & remise des clés</li>
          <li>✔ Ménage & linge</li>
          <li>✔ Support voyageurs</li>
        </ul>
        <button class="btn btn-primary" style="margin-top:20px">Choisir</button>
      </div>

      <div style="background:var(--card);padding:36px;border-radius:var(--radius);box-shadow:var(--shadow);border:2px solid var(--accent-2)">
        <h3>Pack Premium</h3>
        <p style="font-size:1.3rem;font-weight:700;color:var(--accent-2)">20 % de commission</p>
        <ul style="list-style:none;padding:0;text-align:left;line-height:1.8">
          <li>✔ Tous les services du pack Essentiel</li>
          <li>✔ Optimisation des prix</li>
          <li>✔ Photographies professionnelles</li>
        </ul>
        <button class="btn btn-primary" style="margin-top:20px">Choisir</button>
      </div>

      <div style="background:var(--card);padding:36px;border-radius:var(--radius);box-shadow:var(--shadow)">
        <h3>Pack Luxe</h3>
        <p style="font-size:1.3rem;font-weight:700;color:var(--accent-2)">25 % de commission</p>
        <ul style="list-style:none;padding:0;text-align:left;line-height:1.8">
          <li>✔ Tous les services du pack Premium</li>
          <li>✔ Décoration & valorisation du bien</li>
          <li>✔ Gestion complète de A à Z</li>
        </ul>
        <button class="btn btn-primary" style="margin-top:20px">Choisir</button>
      </div>
    </div>
  </div>
</section>

<!-- MÉTHODE -->
<section id="about" style="padding:80px 20px;background:var(--card)">
  <div style="max-width:var(--maxw);margin:0 auto;text-align:center">
    <h2 style="font-family:Montserrat;font-size:2rem;margin-bottom:10px">Notre méthode</h2>
    <p style="color:var(--muted);max-width:700px;margin:0 auto 40px">Nous simplifions votre gestion en trois étapes simples.</p>

    <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:26px;margin-top:40px">
      <div style="background:var(--bg);padding:28px;border-radius:var(--radius);box-shadow:var(--shadow)">
        <div style="font-size:2rem;font-weight:700;color:var(--accent-2)">1</div>
        <h3>Estimation gratuite</h3>
        <p style="color:var(--muted)">Recevez une estimation claire de vos revenus potentiels en quelques clics.</p>
      </div>
      <div style="background:var(--bg);padding:28px;border-radius:var(--radius);box-shadow:var(--shadow)">
        <div style="font-size:2rem;font-weight:700;color:var(--accent-2)">2</div>
        <h3>Signature du contrat</h3>
        <p style="color:var(--muted)">Nous mettons en place la gestion complète de votre bien.</p>
      </div>
      <div style="background:var(--bg);padding:28px;border-radius:var(--radius);box-shadow:var(--shadow)">
        <div style="font-size:2rem;font-weight:700;color:var(--accent-2)">3</div>
        <h3>Suivi & résultats</h3>
        <p style="color:var(--muted)">Suivi mensuel transparent, ajustements et rapports de performance.</p>
      </div>
    </div>
  </div>
</section>

<!-- ACTUALITÉS -->
<section id="news" style="padding:80px 20px">
  <div style="max-width:var(--maxw);margin:0 auto;text-align:center">
    <h2 style="font-family:Montserrat;font-size:2rem;margin-bottom:10px">Actualités du marché</h2>
    <p style="color:var(--muted);max-width:700px;margin:0 auto 40px">Restez informé des tendances et des changements dans la location courte durée en Île-de-France.</p>

    <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:26px;margin-top:40px;text-align:left">
      <article style="background:var(--card);padding:26px;border-radius:var(--radius);box-shadow:var(--shadow)">
        <h3 style="margin-top:0">Hausse de la demande en 2025</h3>
        <p style="color:var(--muted)">Les réservations augmentent de 12 % à Paris et en banlieue proche. Une excellente nouvelle pour les hôtes !</p>
      </article>
      <article style="background:var(--card);padding:26px;border-radius:var(--radius);box-shadow:var(--shadow)">
        <h3 style="margin-top:0">Nouvelles réglementations</h3>
        <p style="color:var(--muted)">Les communes franciliennes renforcent le contrôle des meublés de tourisme : StaynB vous guide dans la conformité.</p>
      </article>
      <article style="background:var(--card);padding:26px;border-radius:var(--radius);box-shadow:var(--shadow)">
        <h3 style="margin-top:0">Tendances déco 2025</h3>
        <p style="color:var(--muted)">La décoration scandinave et les matériaux naturels séduisent de plus en plus de voyageurs.</p>
      </article>
    </div>
  </div>
</section>

<!-- PARTENAIRES -->
<section id="share" style="padding:60px 20px;background:var(--card)">
  <div style="max-width:var(--maxw);margin:0 auto;text-align:center">
    <h2 style="font-family:Montserrat;font-size:2rem;margin-bottom:10px">Nos partenaires</h2>
    <p style="color:var(--muted);max-width:700px;margin:0 auto 40px">
      Nous travaillons avec les meilleures plateformes du secteur.
    </p>

    <div class="partners-container" style="display:flex;flex-wrap:wrap;gap:40px;justify-content:center;align-items:center;">
      <a href="https://www.airbnb.fr" target="_blank" rel="noopener noreferrer" class="partner-link">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/69/Airbnb_Logo_B%C3%A9lo.svg/768px-Airbnb_Logo_B%C3%A9lo.svg.png?20230603231949" alt="Airbnb">
      </a>
      <a href="https://www.booking.com" target="_blank" rel="noopener noreferrer" class="partner-link">
        <img src="https://cdn.worldvectorlogo.com/logos/bookingcom-1.svg" alt="Booking.com">
      </a>
      <a href="https://www.google.com/travel/" target="_blank" rel="noopener noreferrer" class="partner-link">
        <img src="https://upload.wikimedia.org/wikipedia/commons/2/2f/Google_2015_logo.svg" alt="Google">
      </a>
      <a href="https://www.tripadvisor.fr" target="_blank" rel="noopener noreferrer" class="partner-link">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/02/TripAdvisor_Logo.svg/1200px-TripAdvisor_Logo.svg.png?20211022033421" alt="TripAdvisor">
      </a>
      <a href="https://www.expedia.fr" target="_blank" rel="noopener noreferrer" class="partner-link">
        <img src="https://cdn.worldvectorlogo.com/logos/expedia.svg" alt="Expedia">
      </a>
    </div>
  </div>
</section>

<style>
.partner-link {
  position: relative;
  display: inline-block;
}

.partner-link img {
  height: 40px;
  transition: transform 0.4s ease;
}

.partner-link::before {
  content: "";
  position: absolute;
  top: 0;
  left: -75%;
  width: 50%;
  height: 100%;
  background: linear-gradient(120deg, rgba(255,255,255,0) 0%, rgba(255,255,255,0.6) 50%, rgba(255,255,255,0) 100%);
  transform: skewX(-25deg);
  transition: left 0.75s ease;
  pointer-events: none;
  opacity: 0;
}

.partner-link:hover::before {
  left: 125%;
  opacity: 1;
}

.partner-link:hover img {
  transform: scale(1.08);
}
</style>

<!-- Bouton retour haut -->
<button id="backToTop" style="position:fixed;bottom:20px;right:20px;background:var(--accent-2);color:white;border:none;border-radius:50%;width:45px;height:45px;font-size:18px;cursor:pointer;display:none;box-shadow:var(--shadow)">↑</button>

<!-- FORMULAIRE POPUP -->
<div id="popupForm" style="display:none;position:fixed;inset:0;background:rgba(0,0,0,0.55);backdrop-filter:blur(3px);align-items:center;justify-content:center;z-index:2000;">
  <div style="background:var(--card);padding:32px;border-radius:var(--radius);box-shadow:var(--shadow);max-width:420px;width:90%;position:relative;">
    <button id="closeForm" style="position:absolute;top:10px;right:10px;background:none;border:none;font-size:20px;cursor:pointer;color:var(--muted)">✕</button>
    <h3 style="margin-top:0;font-family:Montserrat;font-size:1.4rem;">Demande d’estimation</h3>
    <p style="color:var(--muted);margin-bottom:20px">Remplissez ce court formulaire et notre équipe vous contactera rapidement.</p>

    <form id="formStaynB">
      <label>Nom complet</label>
      <input type="text" name="nom" required style="width:100%;padding:10px;border-radius:8px;border:1px solid #ccc;margin-bottom:12px">

      <label>Email</label>
      <input type="email" name="email" required style="width:100%;padding:10px;border-radius:8px;border:1px solid #ccc;margin-bottom:12px">

      <label>Type de pack souhaité</label>
      <select name="pack" style="width:100%;padding:10px;border-radius:8px;border:1px solid #ccc;margin-bottom:12px">
        <option value="Estimation simple">Estimation simple</option>
        <option value="Essentiel">Pack Essentiel</option>
        <option value="Premium">Pack Premium</option>
        <option value="Luxe">Pack Luxe</option>
      </select>

      <label>Message (facultatif)</label>
      <textarea name="message" rows="3" style="width:100%;padding:10px;border-radius:8px;border:1px solid #ccc;margin-bottom:18px"></textarea>

      <button type="submit" class="btn btn-primary" style="width:100%">Envoyer</button>
    </form>

    <div id="formMessage" style="display:none;color:green;font-weight:600;margin-top:10px;text-align:center">Merci ! Votre message a été envoyé.</div>
  </div>
</div>

<!-- SCRIPTS D’INTERACTION -->
<script>
// Ciblage des éléments
const popup = document.getElementById('popupForm');
const closeBtn = document.getElementById('closeForm');
const form = document.getElementById('formStaynB');
const formMsg = document.getElementById('formMessage');

// Ouverture du popup depuis les boutons
document.getElementById('ctaEstimate').onclick = () => openPopup('Estimation simple');
document.getElementById('ctaPacks').onclick = () => document.getElementById('pricing').scrollIntoView({ behavior: 'smooth' });

// Boutons “Choisir” des packs
document.querySelectorAll('#pricing .btn-primary').forEach((btn, index) => {
  const packNames = ['Essentiel', 'Premium', 'Luxe'];
  btn.addEventListener('click', () => openPopup(packNames[index]));
});

// Fonction d’ouverture
function openPopup(pack){
  popup.style.display = 'flex';
  document.querySelector('select[name="pack"]').value = pack;
  document.body.style.overflow = 'hidden';
}

// Fermeture
closeBtn.onclick = () => closePopup();
popup.onclick = (e) => { if(e.target === popup) closePopup(); };
function closePopup(){
  popup.style.display = 'none';
  document.body.style.overflow = '';
  form.reset();
  formMsg.style.display = 'none';
}

// Bouton retour haut
const btnTop = document.getElementById('backToTop');
window.addEventListener('scroll', ()=>{
  btnTop.style.display = window.scrollY > 400 ? 'block' : 'none';
});
btnTop.addEventListener('click', ()=>window.scrollTo({top:0,behavior:'smooth'}));

// Animation fade-up au scroll
const fadeEls = document.querySelectorAll('.fade-up');
const observer = new IntersectionObserver((entries)=>{
  entries.forEach(e=>{
    if(e.isIntersecting) e.target.classList.add('visible');
  });
},{threshold:0.2});
fadeEls.forEach(el=>observer.observe(el));
</script>

<!-- Script EmailJS -->
<script src="https://cdn.jsdelivr.net/npm/emailjs-com@3/dist/email.min.js"></script>
<script>
document.addEventListener("DOMContentLoaded", function() {
  // Initialisation EmailJS
  emailjs.init("c7u1iGY5Xb11xroE9"); // ta clé publique

  const formStaynB = document.getElementById("formStaynB");
  const formMsg = document.getElementById("formMessage");

  formStaynB.addEventListener("submit", function(e) {
    e.preventDefault();

    console.log("📤 Tentative d'envoi EmailJS avec : ", {
      from_name: formStaynB.nom.value,
      from_email: formStaynB.email.value,
      pack: formStaynB.pack.value,
      message: formStaynB.message.value,
    });

    emailjs.send("service_4rt1ri7", "template_0e03vni", {
      from_name: formStaynB.nom.value,
      from_email: formStaynB.email.value,
      pack: formStaynB.pack.value,
      message: formStaynB.message.value,
    })
    .then(function(response) {
      console.log("✅ Réponse EmailJS :", response);
      formMsg.style.display = "block";
      setTimeout(() => {
        formMsg.style.display = "none";
        formStaynB.reset();
        document.getElementById("popupForm").style.display = "none";
        document.body.style.overflow = ''; // ✅ réactive le scroll
      }, 2000);
    })
    .catch(function(error) {
      console.error("❌ Erreur EmailJS :", error);
      alert("Erreur lors de l’envoi. Vérifie la console.");
    });
  });
});
</script>
</body>
</html>

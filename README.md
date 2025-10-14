<html lang="fr">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<meta name="description" content="StaynB - Conciergerie Airbnb en Île-de-France. Gestion complète, accueil voyageurs, ménage, optimisation, estimation de revenus." />
<title>StaynB — Conciergerie Airbnb (Île-de-France)</title>

<!-- Fonts & icons -->
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@500;700&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

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
  --maxw:1100px;
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

/* ---- ADDED: iframe background styles (keeps video behind content, non-interactive) ---- */
.hero .bg-iframe {
  position:absolute;
  top:0;
  left:0;
  width:100%;
  height:100%;
  z-index:0;
  overflow:hidden;
}
.hero .bg-iframe iframe{
  position:absolute;
  top:50%;
  left:50%;
  width:145%;
  height:145%;
  transform:translate(-50%,-50%);
  pointer-events:none; /* disables interaction completely */
  border:0;
  filter:brightness(1);
}
.hero::after{ /* keep your original gradient overlay effect */
  content:"";
  position:absolute;
  inset:0;
  background:linear-gradient(135deg, rgba(255,90,95,0.25), rgba(245,182,66,0.25));
  z-index:1;
}
/* ---- END ADDED ---- */

.hero-inner{max-width:var(--maxw);width:100%;display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center;position:relative;z-index:2}
.hero-card{background:var(--card);padding:36px;border-radius:var(--radius);box-shadow:var(--shadow)}
.hero h2{font-family:Montserrat;font-size:1.6rem;margin:0 0 12px}
.hero p{color:var(--muted);margin:0 0 18px}
.hero-actions{display:flex;gap:12px;flex-wrap:wrap}
.hero-side{display:flex;flex-direction:column;gap:12px}
.stat{background:linear-gradient(180deg, rgba(255,255,255,0.9), #fff);padding:14px;border-radius:12px;text-align:center;box-shadow:0 8px 20px rgba(18,23,44,0.04)}

/* Sections */
section{padding:56px 20px}
.container{max-width:var(--maxw);margin:0 auto}
h3{font-family:Montserrat;margin-bottom:10px;font-size:1.4rem}
.lead{color:var(--muted);max-width:780px;margin-bottom:18px}

/* Services */
.services-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}
.service{background:var(--card);padding:22px;border-radius:12px;box-shadow:var(--shadow);display:flex;gap:14px;align-items:flex-start;transition:all .3s ease;cursor:pointer}
.service:hover{transform:translateY(-5px);box-shadow:0 12px 24px rgba(0,0,0,0.12)}
.service i{font-size:22px;color:var(--accent);min-width:36px;text-align:center}

/* Packs & comparaison */
.packs-compare{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:18px;align-items:start}
.pack{background:var(--card);padding:20px;border-radius:12px;box-shadow:var(--shadow);transition:all .3s ease;cursor:pointer;position:relative}
.pack:hover{transform:translateY(-5px);box-shadow:0 12px 24px rgba(0,0,0,0.12)}
.pack.recommended::after{
  content:"Recommandé";
  position:absolute;
  top:12px;
  right:12px;
  background:#FFB67B;
  color:#111;
  font-weight:700;
  font-size:0.85rem;
  padding:6px 10px;
  border-radius:12px;
}
.features{list-style:none;padding:0;margin:12px 0 0}
.features li{padding:6px 0;border-top:1px dashed rgba(0,0,0,0.04);color:var(--muted);font-size:0.95rem}
.pack-cta{display:flex;gap:8px;margin-top:14px;align-items:center}

/* About / method */
.method-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:16px;margin-top:18px}
.step{background:var(--card);padding:14px;border-radius:10px;text-align:center;box-shadow:0 6px 18px rgba(18,23,44,0.04)}

/* Reviews */
.reviews{display:flex;gap:12px;align-items:center;overflow-x:auto;padding-bottom:8px}
.review-card{background:var(--card);padding:18px;border-radius:10px;min-width:260px;box-shadow:var(--shadow);transition:all .3s ease;cursor:pointer}
.review-card:hover{transform:translateY(-5px);box-shadow:0 12px 24px rgba(0,0,0,0.12)}
.review-card .stars{color:var(--accent);font-weight:700;margin-top:6px}

/* New: Market news / Live stats / Share */
.news-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:20px}
.news-card{background:var(--card);padding:18px;border-radius:10px;box-shadow:var(--shadow)}
.news-card:hover{transform:translateY(-6px);box-shadow:0 16px 32px rgba(0,0,0,0.12)}
.live-indicator{display:flex;gap:16px;flex-wrap:wrap;margin-top:14px}
.live-box{background:var(--card);padding:20px;border-radius:10px;box-shadow:var(--shadow);text-align:center;min-width:140px}
.share-buttons{display:flex;gap:10px;flex-wrap:wrap;margin-top:12px;justify-content:center}
.share-buttons a{display:flex;align-items:center;gap:8px;padding:10px 16px;border-radius:8px;color:white;font-weight:600;text-decoration:none}
.share-facebook{background:#1877F2}
.share-twitter{background:#1DA1F2}
.share-linkedin{background:#0077B5}

/* Partners */
.partners{display:flex;gap:20px;flex-wrap:wrap;justify-content:center;align-items:center}
.partner-card{display:flex;align-items:center;gap:12px;padding:14px 22px;border-radius:20px;text-decoration:none;color:white;font-weight:600;transition:all .3s ease;box-shadow:0 6px 18px rgba(0,0,0,0.08)}
.partner-card img{height:28px}
.partner-card.airbnb{background:#FF5A5F}
.partner-card.google{background:#4285F4}

/* Footer */
footer{Padding:28px 20px;background:#111827;color:white;margin-top:30px;text-align:center}

/* Back to top */
.backtop{position:fixed;right:18px;bottom:18px;background:linear-gradient(135deg,var(--text),var(--accent));color:white;padding:12px;border-radius:12px;box-shadow:0 10px 30px rgba(0,0,0,0.18);cursor:pointer;z-index:1400;display:none}

/* Modals */
#estimateModal,#bookingModal,#contactModal{display:flex;justify-content:center;align-items:center;position:fixed;inset:0;background:rgba(0,0,0,0.6);z-index:2000;padding:18px;opacity:0;pointer-events:none;transition:opacity .28s ease}
#estimateModal.show,#bookingModal.show,#contactModal.show{opacity:1;pointer-events:all}
.modal-box{background:var(--card);border-radius:12px;max-width:600px;width:100%;padding:20px;position:relative;transform:scale(.96);transition:transform .28s ease,box-shadow .28s ease;box-shadow:0 18px 48px rgba(18,23,44,0.12)}
#estimateModal.show .modal-box,#bookingModal.show .modal-box,#contactModal.show .modal-box{transform:scale(1)}
.modal-close{position:absolute;right:12px;top:10px;font-weight:700;color:var(--accent);cursor:pointer;font-size:20px;transition:all .25s}
.modal-close:hover{color:var(--text);transform:rotate(90deg)}

form{display:flex;flex-direction:column;gap:10px}
input,select,textarea{padding:10px;border-radius:8px;border:1px solid rgba(16,24,40,0.06);font-size:0.95rem}
textarea{min-height:84px;resize:vertical}

@media(max-width:980px){
  .hero-inner{grid-template-columns:1fr}
  .services-grid{grid-template-columns:1fr}
  .packs-compare{grid-template-columns:1fr}
  .method-grid{grid-template-columns:repeat(2,1fr)}
  .news-grid{grid-template-columns:1fr}
}
@media(max-width:600px){
  nav{display:none}
  header{padding:10px}
  .method-grid{grid-template-columns:1fr}
}

.fade-up{opacity:0;transform:translateY(8px);transition:opacity .6s ease, transform .6s ease}
.fade-up.show{opacity:1;transform:none}

.news-card.fade-up {opacity:0;transform:translateY(8px);transition:opacity .6s ease, transform .6s ease}
.news-card.fade-up.show {opacity:1;transform:none}

/* Micro animations & carousel etc. */
</style>
</head>

<body>

<!-- HEADER -->
<header>
  <div class="brand" aria-label="StaynB">
    <div class="logo-mark">SB</div>
    <div>
      <h1>StaynB</h1>
      <div style="font-size:12px;color:var(--muted)">Conciergerie • Île-de-France</div>
    </div>
  </div>
  <nav aria-label="Navigation principale">
    <a href="#services">Services</a>
    <a href="#pricing">Packs</a>
    <a href="#about">À propos</a>
    <a href="#news">Actualités</a>
    <a href="#share">Partager</a>
    <button class="cta-quick" id="ctaContact">Nous contacter</button>
  </nav>
</header>

<!-- HERO -->
<section class="hero" aria-label="Hero StaynB">
  <!-- REPLACED: background video (iframe YouTube, autoplay, muted, loop) -->
  <div class="bg-iframe" aria-hidden="true">
    <iframe
  src="https://www.youtube.com/embed/_iZ-vMCeH9U?autoplay=1&mute=1&controls=0&showinfo=0&modestbranding=1&playsinline=1&loop=1&playlist=_iZ-vMCeH9U"
  frameborder="0"
  allow="autoplay; fullscreen"
  allowfullscreen
  title="Paris background">
</iframe>
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
        <div style="font-size:20px;font-weight:700">78%</div>
      </div>
      <div class="stat fade-up">
        <div style="font-size:12px;color:var(--muted)">Clients satisfaits</div>
        <div style="font-size:20px;font-weight:700">+120</div>
      </div>
    </aside>
  </div>
</section>

<!-- SERVICES -->
<section id="services" class="container">
  <h3>Nos services</h3>
  <p class="lead">Prise en charge complète : accueil, ménage, optimisation d’annonce, maintenance locale et support voyageurs.</p>
  <div class="services-grid">
    <div class="service fade-up">
      <i class="fas fa-key" aria-hidden="true"></i>
      <div>
        <h4 style="margin:0 0 6px">Accueil & check-in</h4>
        <div style="color:var(--muted)">Remise des clés, accueil personnalisé et guidance locale pour vos voyageurs.</div>
      </div>
    </div>
    <div class="service fade-up" style="transition-delay:.07s">
      <i class="fas fa-broom" aria-hidden="true"></i>
      <div>
        <h4 style="margin:0 0 6px">Ménage & linge</h4>
        <div style="color:var(--muted)">Équipes professionnelles, contrôle qualité et gestion du linge entre chaque réservation.</div>
      </div>
    </div>
    <div class="service fade-up" style="transition-delay:.14s">
      <i class="fas fa-chart-line" aria-hidden="true"></i>
      <div>
        <h4 style="margin:0 0 6px">Optimisation & pricing</h4>
        <div style="color:var(--muted)">Tarification dynamique, photos pro et optimisation des annonces pour maximiser vos revenus.</div>
      </div>
    </div>
  </div>
</section>

<!-- PACKS & COMPARISON -->
<section id="pricing" class="container">
  <h3>Packs & Tarifs</h3>
  <p class="lead">Choisissez le pack qui vous convient — transparence sur les commissions et services inclus.</p>

  <div class="packs-compare fade-up">
    <div>
      <div class="pack">
        <h4>Pack Essentiel</h4>
        <div style="color:var(--muted)">Accueil & ménage, gestion des réservations.</div>
        <ul class="features"><li>Accueil & check-in</li><li>Ménage professionnel</li><li>Gestion calendrier</li></ul>
        <div class="pack-cta"><div style="font-weight:800;font-size:1.05rem;margin-top:6px">15% <span style="font-weight:400;color:var(--muted)">commission</span></div><div style="margin-left:auto"><button class="btn btn-primary" onclick="openBookingForm('Essentiel')">Réserver</button></div></div>
      </div>

      <div class="pack recommended" style="margin-top:14px">
        <h4>Pack Premium</h4>
        <div style="color:var(--muted)">Tout de l'essentiel + optimisation avancée & assistance 24/7.</div>
        <ul class="features"><li>Tarif dynamique</li><li>Photos pro & annonces optimisées</li><li>Assistance 24/7</li></ul>
        <div class="pack-cta"><div style="font-weight:800;font-size:1.05rem;margin-top:6px">20% <span style="font-weight:400;color:var(--muted)">commission</span></div><div style="margin-left:auto"><button class="btn btn-primary" onclick="openBookingForm('Premium')">Réserver</button></div></div>
      </div>
    </div>

    <div>
      <div class="pack">
        <h4>Pack Luxe</h4>
        <div style="color:var(--muted)">Service VIP, manager dédié, reporting et support premium.</div>
        <ul class="features"><li>Gestion complète</li><li>Reporting avancé</li><li>Support dédié</li></ul>
        <div class="pack-cta"><div style="font-weight:800;font-size:1.05rem;margin-top:6px">25% <span style="font-weight:400;color:var(--muted)">commission</span></div><div style="margin-left:auto"><button class="btn btn-primary" onclick="openBookingForm('Luxe')">Réserver</button></div></div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT / METHOD -->
<section id="about" class="container fade-up">
  <h3>Notre méthode</h3>
  <p class="lead">Simplifiez votre vie et boostez vos revenus : gestion complète et expérience client premium.</p>
  <div class="method-grid">
    <div class="step fade-up">1. Analyse & estimation</div>
    <div class="step fade-up" style="transition-delay:.05s">2. Mise en place de votre annonce</div>
    <div class="step fade-up" style="transition-delay:.1s">3. Accueil voyageurs & suivi</div>
    <div class="step fade-up" style="transition-delay:.15s">4. Optimisation & reporting</div>
  </div>
</section>

<!-- MARKET NEWS CAROUSEL -->
<section id="news" class="container fade-up">
  <h3>Actualités du marché</h3>
  <p class="lead">Les tendances récentes et ce qu’elles signifient pour vos revenus locatifs en Île-de-France.</p>
  <div class="news-carousel" style="position:relative;overflow:hidden;">
    <button class="carousel-btn carousel-prev" aria-label="Précédent" style="position:absolute;top:50%;left:0;transform:translateY(-50%);background:var(--accent);color:white;border:none;border-radius:50%;width:36px;height:36px;cursor:pointer;z-index:10;"><i class="fas fa-chevron-left"></i></button>
    <div class="news-carousel-track" style="display:flex;gap:20px;transition:transform .4s ease;">
      <div class="news-card fade-up" style="flex:0 0 300px;">
        <h4>Avril 2025 — Rebond des réservations</h4>
        <p>Plusieurs quartiers parisiens voient une hausse des réservations de courte durée : opportunité pour de meilleurs revenus saisonniers.</p>
      </div>
      <div class="news-card fade-up" style="flex:0 0 300px;">
        <h4>Mars 2025 — Réglementations locales</h4>
        <p>Des ajustements administratifs impactent la mise en conformité des annonces : StaynB accompagne la gestion administrative pour vous.</p>
      </div>
      <div class="news-card fade-up" style="flex:0 0 300px;">
        <h4>Février 2025 — Nouvelles attentes voyageurs</h4>
        <p>Les voyageurs privilégient les expériences locales et le confort — mise à jour des listings et photos pro recommandées.</p>
      </div>
    </div>
    <button class="carousel-btn carousel-next" aria-label="Suivant" style="position:absolute;top:50%;right:0;transform:translateY(-50%);background:var(--accent-2);color:white;border:none;border-radius:50%;width:36px;height:36px;cursor:pointer;z-index:10;"><i class="fas fa-chevron-right"></i></button>
  </div>
</section>

<!-- LIVE STATS -->
<section id="live" class="container fade-up">
  <h3>Indicateur de performance en direct</h3>
  <p class="lead">Chiffres mis à jour pour suivre rapidement l'impact de notre gestion.</p>
  <div class="live-indicator">
    <div class="live-box">
      <div id="liveRevenue" style="font-size:1.6rem;font-weight:700">0 €</div>
      <div style="color:var(--muted)">Revenu total généré</div>
    </div>
    <div class="live-box">
      <div id="liveOccupancy" style="font-size:1.6rem;font-weight:700">0%</div>
      <div style="color:var(--muted)">Taux d'occupation</div>
    </div>
    <div class="live-box">
      <div id="liveClients" style="font-size:1.6rem;font-weight:700">0</div>
      <div style="color:var(--muted)">Clients satisfaits</div>
    </div>
  </div>
</section>

<!-- SHARE SECTION -->
<section id="share" class="container fade-up">
  <h3>Partager StaynB</h3>
  <p class="lead">Aidez-nous à faire connaître StaynB — partagez sur vos réseaux.</p>
  <div class="share-buttons" role="navigation" aria-label="Partager">
    <a href="https://www.facebook.com/sharer/sharer.php?u=https://www.staynB.fr" target="_blank" rel="noopener noreferrer" class="share-facebook"><i class="fab fa-facebook-f"></i> Facebook</a>
    <a href="https://twitter.com/intent/tweet?url=https://www.staynB.fr&text=Découvrez%20StaynB%20!" target="_blank" rel="noopener noreferrer" class="share-twitter"><i class="fab fa-twitter"></i> Twitter</a>
    <a href="https://www.linkedin.com/shareArticle?mini=true&url=https://www.staynB.fr" target="_blank" rel="noopener noreferrer" class="share-linkedin"><i class="fab fa-linkedin-in"></i> LinkedIn</a>
  </div>
</section>

<!-- REVIEWS -->
<section class="container fade-up">
  <h3>Avis clients</h3>
  <div class="reviews">
    <div class="review-card fade-up">
      <strong>Marie D.</strong>
      <div class="stars">★★★★★</div>
      <p>Service impeccable, communication excellente, revenus en hausse !</p>
    </div>
    <div class="review-card fade-up" style="transition-delay:.05s">
      <strong>Jean P.</strong>
      <div class="stars">★★★★★</div>
      <p>Très satisfait du suivi et de la gestion complète de mon appartement.</p>
    </div>
    <div class="review-card fade-up" style="transition-delay:.1s">
      <strong>Lucie V.</strong>
      <div class="stars">★★★★★</div>
      <p>Accueil parfait et optimisation de mes annonces au top !</p>
    </div>
  </div>
</section>

<!-- PARTNERS -->
<section class="container fade-up">
  <h3>Nos partenaires</h3>
  <div class="partners">
    <a href="https://www.airbnb.com" target="_blank" rel="noopener noreferrer" class="partner-card airbnb" aria-label="Airbnb">
      <img src="https://upload.wikimedia.org/wikipedia/commons/e/e4/Airbnb_Logo_B%C3%A9lo.svg" alt="Airbnb logo"> Airbnb
    </a>
    <a href="https://www.google.com" target="_blank" rel="noopener noreferrer" class="partner-card google" aria-label="Google">
      <img src="https://upload.wikimedia.org/wikipedia/commons/2/2f/Google_2015_logo.svg" alt="Google logo"> Google
    </a>
  </div>
</section>

<!-- FOOTER -->
<footer>
  &copy; 2025 StaynB. Tous droits réservés.
</footer>

<!-- BACK TO TOP -->
<div class="backtop" onclick="window.scrollTo({top:0,behavior:'smooth'})" aria-label="Retour en haut"><i class="fas fa-chevron-up"></i></div>

<!-- MODALS -->
<div id="estimateModal">
  <div class="modal-box">
    <span class="modal-close" onclick="closeModal('estimateModal')">&times;</span>
    <h3>Demande d'estimation</h3>
    <form>
      <input type="text" placeholder="Nom complet" required>
      <input type="email" placeholder="Email" required>
      <input type="tel" placeholder="Téléphone">
      <textarea placeholder="Votre message"></textarea>
      <button class="btn btn-primary" type="submit">Envoyer</button>
    </form>
  </div>
</div>

<div id="bookingModal">
  <div class="modal-box">
    <span class="modal-close" onclick="closeModal('bookingModal')">&times;</span>
    <h3>Réserver un pack</h3>
    <form>
      <input type="text" placeholder="Nom complet" required>
      <input type="email" placeholder="Email" required>
      <select required>
        <option value="">Sélectionnez votre pack</option>
        <option value="Essentiel">Essentiel</option>
        <option value="Premium">Premium</option>
        <option value="Luxe">Luxe</option>
      </select>
      <textarea placeholder="Votre message"></textarea>
      <button class="btn btn-primary" type="submit">Réserver</button>
    </form>
  </div>
</div>

<div id="contactModal">
  <div class="modal-box">
    <span class="modal-close" onclick="closeModal('contactModal')">&times;</span>
    <h3>Nous contacter</h3>
    <form>
      <input type="text" placeholder="Nom complet" required>
      <input type="email" placeholder="Email" required>
      <textarea placeholder="Votre message" required></textarea>
      <button class="btn btn-primary" type="submit">Envoyer</button>
    </form>
  </div>
</div>

<script>
// Modal control
function openBookingForm(pack){
  document.getElementById('bookingModal').classList.add('show');
  document.querySelector('#bookingModal select').value = pack;
}
function closeModal(id){
  document.getElementById(id).classList.remove('show');
}

// Back to top
window.addEventListener('scroll',()=>{
  document.querySelector('.backtop').style.display = window.scrollY > 200 ? 'flex' : 'none';
});

// Carousel
let track = document.querySelector('.news-carousel-track');
let index = 0;
const total = track ? track.children.length : 0;
if(track){
  document.querySelector('.carousel-next').onclick = () => {
    index = (index + 1) % total;
    track.style.transform = `translateX(${-index * 320}px)`;
  };
  document.querySelector('.carousel-prev').onclick = () => {
    index = (index - 1 + total) % total;
    track.style.transform = `translateX(${-index * 320}px)`;
  };
}

// Fade-up animation
const faders = document.querySelectorAll('.fade-up');
const options = { threshold: 0.2 };
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if(entry.isIntersecting) {
      entry.target.classList.add('show');
      observer.unobserve(entry.target);
    }
  });
}, options);
faders.forEach(fader => observer.observe(fader));

// Live stats simulation
let rev = 0, occ = 0, cli = 0;
setInterval(() => {
  rev = Math.min(1650, rev + Math.floor(Math.random() * 20));
  occ = Math.min(78, occ + Math.random() * 0.5);
  cli = Math.min(120, cli + 1);
  const revEl = document.getElementById('liveRevenue');
  const occEl = document.getElementById('liveOccupancy');
  const cliEl = document.getElementById('liveClients');
  if(revEl) revEl.innerText = `${rev} €`;
  if(occEl) occEl.innerText = `${occ.toFixed(1)}%`;
  if(cliEl) cliEl.innerText = `${cli}`;
}, 1000);

// Activation des boutons
const ctaEstimate = document.getElementById('ctaEstimate');
if(ctaEstimate) ctaEstimate.addEventListener('click', function() {
  const em = document.getElementById('estimateModal');
  if(em) em.classList.add('show');
});
const ctaPacks = document.getElementById('ctaPacks');
if(ctaPacks) ctaPacks.addEventListener('click', function() {
  const pricing = document.getElementById('pricing');
  if(pricing) pricing.scrollIntoView({ behavior: 'smooth' });
});
const ctaContact = document.getElementById('ctaContact');
if(ctaContact) ctaContact.addEventListener('click', function() {
  const cm = document.getElementById('contactModal');
  if(cm) cm.classList.add('show');
});
</script>
</body>
</html>

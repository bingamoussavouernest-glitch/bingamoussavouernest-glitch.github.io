# bingamoussavouernest-glitch.github.io
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Fit Express – Programme rapide & efficace</title>
  <meta name="description" content="Fit Express : programme de remise en forme rapide et efficace. Résultats visibles même avec un emploi du temps chargé. Prix : 20 000 FCFA." />
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
  <style>
    body { margin:0; font-family: Inter, sans-serif; color:#f1f5f9; background:#0f172a; }
    .container { max-width: 900px; margin:auto; padding:20px; }
    header { display:flex; justify-content:space-between; align-items:center; padding:10px 0; }
    header h1 { margin:0; font-size:1.5rem; color:#22c55e; }
    a { text-decoration:none; }
    .btn { display:inline-block; background:#22c55e; color:#052e16; padding:12px 18px; border-radius:8px; font-weight:bold; }
    .btn-outline { display:inline-block; border:1px solid #94a3b8; color:#f1f5f9; padding:12px 18px; border-radius:8px; }
    .hero { padding:30px 0; }
    .hero h2 { font-size:2rem; margin-bottom:10px; }
    .card { background:#1e293b; padding:20px; border-radius:12px; margin-top:20px; }
    input { width:100%; padding:10px; margin:6px 0; border-radius:6px; border:1px solid #334155; background:#0f172a; color:#f1f5f9; }
    label { font-size:.9rem; }
    footer { text-align:center; padding:20px; margin-top:40px; color:#94a3b8; }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1>FIT EXPRESS</h1>
      <a class="btn-outline" href="https://wa.me/242065814431?text=Bonjour%2C%20je%20veux%20des%20infos%20sur%20Fit%20Express" target="_blank">WhatsApp</a>
    </header>

    <section class="hero">
      <h2>Programme rapide & efficace</h2>
      <p>Entraînements courts, guidés en vidéo, sans matériel compliqué. Idéal pour les personnes toujours en déplacement.</p>
      <p><strong>Prix : 20 000 FCFA</strong></p>
      <a class="btn" href="#inscription">S’inscrire maintenant</a>
    </section>

    <section id="programme">
      <div class="card">
        <h3>Ce que vous allez obtenir :</h3>
        <ul>
          <li>Vidéos guidées accessibles sur smartphone</li>
          <li>Exercices sans matériel, réalisables partout</li>
          <li>Programme progressif sur 4 semaines</li>
          <li>Bonus : guide nutrition simplifié</li>
          <li>Support WhatsApp + certificat de participation</li>
        </ul>
      </div>
    </section>

    <section id="inscription">
      <div class="card">
        <h3>Formulaire d’inscription</h3>
        <form onsubmit="return envoyerWhatsApp(event)">
          <label for="nom">Nom & Prénom</label>
          <input type="text" id="nom" required>
          <label for="email">Email</label>
          <input type="email" id="email" required>
          <label for="tel">Téléphone (WhatsApp)</label>
          <input type="tel" id="tel" required>
          <button type="submit" class="btn">Envoyer & Payer</button>
        </form>
      </div>
    </section>

    <footer>
      © <span id="year"></span> Fit Express · Tous droits réservés
    </footer>
  </div>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
    function envoyerWhatsApp(e) {
      e.preventDefault();
      const nom = document.getElementById('nom').value.trim();
      const email = document.getElementById('email').value.trim();
      const tel = document.getElementById('tel').value.trim();
      const msg = encodeURIComponent(
        `Bonjour, je m'inscris à Fit Express.%0A%0A` +
        `Nom: ${nom}%0AEmail: ${email}%0ATéléphone: ${tel}%0A` +
        `Montant: 20 000 FCFA (MTN MoMo)`
      );
      window.open(`https://wa.me/242065814431?text=${msg}`, '_blank');
      return false;
    }
  </script>
</body>
</html>


<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Plateforme d'Achat et Vente</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <header>
    <h1>Plateforme d'Achat et Vente</h1>
  </header>

  <nav>
    <select onchange="showSection(this.value)">
      <option value="" selected disabled>Choisissez une option</option>
      <option value="publier">Publier une Annonce</option>
      <option value="annonces">Annonces</option>
      <option value="messagerie">Messagerie</option>
    </select>
  </nav>

  <main>
    <section id="publier">
      <h2>Publier une Annonce</h2>
      <form action="submit_ad.php" method="POST">
        <label for="titre">Titre de l'annonce :</label><br>
        <input type="text" id="titre" name="titre"><br>
        <label for="description">Description :</label><br>
        <textarea id="description" name="description"></textarea><br>
        <!-- Autres champs pour les détails du produit, photo, prix, etc. -->

        <input type="submit" value="Publier">
      </form>
    </section>

    <section id="annonces" style="display: none;">
      <h2>Annonces</h2>
      <!-- Liste des annonces publiées avec des détails et bouton "Contacter" -->
      <div class="annonce">
        <h3>Nom du Produit</h3>
        <p>Description courte...</p>
        <p>Prix : $XX</p>
        <button>Contact Vendeur</button>
      </div>
      <!-- Répéter la structure pour d'autres annonces -->
    </section>

    <section id="messagerie" style="display: none;">
      <h2>Messagerie</h2>
      <!-- Ajout du formulaire de messagerie -->
    <form action="send_message.php" method="POST">
      <label for="destinataire">Destinataire :</label><br>
      <select id="destinataire" name="destinataire">
        <option value="acheteur1">Acheteur 1</option>
        <option value="acheteur2">Acheteur 2</option>
        <option value="vendeur1">Vendeur 1</option>
        <!-- Ajoutez d'autres options pour d'autres destinataires -->
      </select><br><br>
      <label for="message">Message :</label><br>
      <textarea name="message"></textarea><br>
      <input type="submit" value="Envoyer">
    </form>
  </div>
      <!-- Interface de messagerie pour les échanges entre acheteurs et vendeurs -->
      <div class="conversation">
        <!-- Afficher les messages ici -->
        <form action="send_message.php" method="POST">
          <textarea name="message"></textarea>
          <input type="submit" value="Envoyer">
        </form>
      </div>
    </section>
  </main>

  <footer>
    <p>Plateforme d'Achat et Vente &copy; 2023</p>
  </footer>

  <script>
    function showSection(sectionId) {
      document.querySelectorAll('section').forEach(section => {
        section.style.display = 'none';
      });

      document.getElementById(sectionId).style.display = 'block';
    }
  </script>

</body>

<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Plateforme d'Achat et Vente</title>

</html>

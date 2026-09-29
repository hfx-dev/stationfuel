# StationFuel

Carte pour trouver la station-service la moins chère près de chez vous, en France, avec les prix des carburants en temps réel.

Application 100% statique (un seul fichier `index.html`, aucun backend) — utilisable directement dans un navigateur ou hébergée sur GitHub Pages.

## Fonctionnalités

- **Prix en temps réel** — données issues de l'API officielle du gouvernement français (`data.economie.gouv.fr`, prix des carburants en flux instantané) : Gazole, SP95, SP98, E10, E85, GPLc.
- **Géolocalisation automatique** — la position est demandée dès l'ouverture de la page et suivie en continu ; un message clair s'affiche si elle est refusée ou indisponible, avec position par défaut (Paris) en repli.
- **Recherche d'adresse** — autocomplétion de villes/adresses via Nominatim (OpenStreetMap).
- **Carte interactive** — marqueurs groupés (clusters), popup avec tous les prix par station et lien d'itinéraire (Google Maps).
- **Raccourci « station la moins chère »** — un chip cliquable au-dessus de la liste affiche le prix le plus bas du moment ; un clic centre la carte sur cette station et ouvre sa fiche.
- **Filtres et tri** — par type de carburant, prix plafond, rayon de recherche, zone dessinée à la main (cercle/rectangle/polygone), tri par prix, distance ou fraîcheur des données.
- **Mode démo** — si l'API officielle est injoignable ou hors de France, l'app bascule automatiquement sur des données fictives clairement identifiées (bannière d'avertissement), avec possibilité de réessayer l'API réelle.
- **Thème clair/sombre** et interface responsive (vue mobile en feuille coulissante).
- **Cache des tuiles de carte** via Service Worker pour un chargement plus rapide (les données de prix, elles, restent toujours interrogées en direct).

## Utiliser l'application en ligne

Aucune installation nécessaire : ouvrez `index.html` dans un navigateur, ou activez **GitHub Pages** sur ce dépôt (Settings → Pages → Deploy from a branch → `main` → `/ (root)`) pour obtenir une URL publique du type `https://hfx-dev.github.io/stationfuel/`.

# Le Grand Prix de Camille

Mini-jeu de saut d'obstacles (CSO) pour téléphone, cadeau pour les 12 ans de Camille.
Un seul fichier HTML, aucune dépendance, sons synthétisés : rien à compiler.

## Jouer en local

Ouvrir `docs/index.html` dans Chrome. (Le mode « appli installable » ne marche qu'en HTTPS, donc une fois en ligne.)

## Mettre en ligne sur GitHub Pages

1. Créer un dépôt **public** sur github.com (par exemple `gp-camille`).
2. Pousser ce dossier tel quel :
   ```bash
   git init -b main
   git add .
   git commit -m "Le Grand Prix de Camille"
   git remote add origin git@github.com:<ton-compte>/gp-camille.git
   git push -u origin main
   ```
3. Dans le dépôt : **Settings > Pages > Build and deployment** : Source « Deploy from a branch », branche `main`, dossier `/docs`, puis Save.
4. Après 1 à 2 minutes, le jeu est à `https://<ton-compte>.github.io/gp-camille/`.

## Sur le téléphone de Camille (Android)

Ouvrir le lien dans Chrome, puis menu ⋮ > **Ajouter à l'écran d'accueil** (ou « Installer l'application »).
Le jeu s'ouvre alors en plein écran, en paysage, et marche même sans réseau.

## Contenu

- 5 niveaux : Club 4 → Club 3 → Club 2 → Club 1 → Grand Prix d'Elliant
- Obstacles : vertical, oxer, triple barre, mur, rivière, combinaisons A-B
- Vraies règles simplifiées : barre = 4 points, refus = 4 points, 2e refus = élimination
- Aides qui disparaissent au fil des niveaux : zone verte d'appel, puis décompte des foulées « 3, 2, 1, hop »
- Compte à rebours jusqu'au concours d'Elliant (20 décembre 2026)
- Le nom du cheval est demandé au premier lancement ; progression et records gardés sur le téléphone

Pour mettre à jour le jeu après une modification, changer `CACHE` dans `docs/sw.js` (ex. `gp-camille-v2`) puis pousser.

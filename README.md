# RUSH° — Landing page 3D style soda
ue
Site vitrine avec une canette 3D interactive (Three.js) qu'on peut faire pivoter à la souris/au doigt, animations de bulles, et une identité visuelle rouge/noire dans l'esprit "soda pétillant".

## Aperçu
- Hero plein écran avec canette 3D (glisser pour tourner)
- Section "moment" avec chiffres clés
- Grille de 3 saveurs
- Citation de campagne
- Footer

## Lancer en local
Aucune installation nécessaire, un seul fichier HTML autonome (Three.js chargé via CDN).

```bash
git clone <ton-repo>
cd <ton-repo>
open index.html   # ou double-clique dessus
```

Pour un rendu propre (certains navigateurs bloquent les modules en `file://`), sers-le avec un petit serveur local :

```bash
python3 -m http.server 8000
# puis ouvre http://localhost:8000
```

## Déployer sur GitHub Pages
1. Pousse ce dossier dans un repo GitHub (`index.html` doit être à la racine, ou dans `/docs`).
2. Dans le repo → **Settings > Pages**.
3. Source : `Deploy from a branch`, branche `main`, dossier `/ (root)`.
4. Le site sera dispo à `https://<ton-user>.github.io/<repo>/` en quelques minutes.

## Personnaliser
- Couleurs : variables CSS en haut de `index.html` (`:root { --red, --ink, --cream, --gold... }`)
- Texte de la canette : fonction `buildLabelTexture()` dans le `<script>` (dessin canvas, donc modifiable sans image externe)
- Sections/texte : directement dans le HTML

## Note
Ce projet utilise un nom et un visuel **originaux** ("RUSH°", couleurs et typo custom) inspirés de l'univers soda, plutôt que la marque et le logo réels de Coca-Cola — je ne peux pas reproduire une marque déposée. Tu peux bien sûr renommer/ajuster les couleurs si c'est pour un usage perso ou un exercice de style.

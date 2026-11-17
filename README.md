# Icebreaker – Boîte à déclics

Application installable (PWA) pour les formateurs : 22 ice-breakers, énergisants et reprises d'attention avec consignes, filtres, chronomètre, tirage au sort et constitution de groupes. Pensée pour des sessions de 10 à 12 stagiaires maximum : toutes les activités fonctionnent jusqu'à 12 personnes.

Adresse : https://jdajdl.github.io/Icebreaker/
Sur téléphone, ouvrir l'adresse puis « Ajouter à l'écran d'accueil ». L'application fonctionne ensuite hors-ligne.

## Publication
Settings → Pages → Deploy from a branch → `main` / `(root)`.

## Fichiers
- `index.html`, `app.css`, `app.js` : l'application (aucune dépendance externe)
- `manifest.webmanifest` : nom, icônes, mode plein écran
- `sw.js` : service worker (hors-ligne)
- `fonts/`, `icons/` : polices et icônes embarquées

## Modifier le contenu
Les activités sont la constante `ACTIVITES` en haut de `app.js` (titre, type, durée, effectif, moments, matériel, consignes, variantes, débrief).

## Publier une mise à jour
Après toute modification, changer `VERSION` dans `sw.js` (`declics-v2` → `declics-v3`) pour que les appareils déjà installés rechargent les fichiers.

## Données
Favoris, notes, dates d'utilisation et liste de participants sont enregistrés dans le navigateur de chaque appareil (stockage local). Rien n'est envoyé ailleurs.

## Contenu
Le site est public : n'y mettre aucun contenu interne ou confidentiel.

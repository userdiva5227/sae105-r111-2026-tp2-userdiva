# Notes de travail

Ce fichier fait partie du rendu. Remplissez-le au fil des TP.

## Fiche d'inventaire (TP 1) — corrigé

| Page | Composants présents | Médias |
| --- | --- | --- |
| Home | barre de nav, accroche, cartes projet ×5, chiffres clés, membres ×8, événements ×3, contact, pied | 5 photos projet, 8 portraits, icône d'envoi, carte du monde |
| Works | barre de nav, intro, filtre, cartes projet, contact, pied | 5 photos projet |
| Works single | barre de nav, intro, métadonnées, partage, vidéo, galerie, contact, pied | vidéo + affiche, 4 photos, 3 icônes |
| About | barre de nav, intro, photo, logos clients ×8, événements ×3, contact, pied | 1 photo, 8 logos |
| Event list | barre de nav, intro, cartes événement ×5, contact, pied | 5 visuels, icône de lieu |
| Event single | barre de nav, intro, carte événement, détails, liste, intervenants ×8, contact, pied | 1 visuel, 8 portraits |
| Team | barre de nav, intro, filtre, membres ×16, contact, pied | 8 portraits (réutilisés) |
| Contact | barre de nav, intro, sélecteur de bureau, carte, coordonnées, événements ×3, contact, pied | 1 carte |

**Composants qui reviennent** : barre de nav (8 pages) · pied de page (8) · section contact (8) ·
liste d'événements (3 pages) · carte projet (2) · membre (3) · bouton-lien.

**Polices et graisses employées** : la maquette emploie Inter 200, 300, 400, 500 et 600, et Playfair Display
700 pour le titre d'accueil. **On ramène à deux graisses** (CM 9) : Inter 400 et 600, plus Playfair Display 700.
Une seule exception : Inter 200 pour les chiffres clés de l'accueil, qui en dépendent vraiment
→ 4 fichiers `woff2`.

## Plan de l'accueil (TP 2, étape 0)

À tracer **avant** d'écrire une balise. Pour chaque bloc de la maquette, de haut en bas :
quelle balise, et pourquoi (les trois questions du CM 4 : se tient tout seul ? partie titrée ? rien de tout ça ?).

| Bloc de la maquette | Balise | Pourquoi |
| --- | --- | --- |
| Barre du haut (logo, menu) |logo x9 |menu x9 |
| Accroche « Building. Brands. » x1| | |
| Latest work |x3| |
| Une carte projet |x1 | |
| Chiffres clés |countries |clients | offices
| Meet the team |x2 | |
| Un membre |x16 | |
| Upcoming events |x3 | |
| Un événement | | |
| Contact |x9 | |
| Pied de page |x9 | |

**Plan des titres** (h1 → h2 → h3), tel que HeadingsMap doit l'afficher :

-

## Les `alt` dont je suis le moins sûr (TP 2)

Rappel du CM 3 : l'`alt` ne décrit pas l'image, il la **remplace**. Masquez l'image, lisez la phrase.

| Image (fichier, page) | `alt` choisi | Pourquoi j'hésite |
| --- | --- | --- |
| | | |
| | | |
| | | |

## Journal IA

| Date | Ce que j'ai demandé | Ce qu'il a apporté | Ce que j'ai corrigé |
| --- | --- | --- | --- |
| 13/11/2026 | Appliquer à toutes les pages le squelette du CM 4. | Structuré les pages avec `header`, `nav`, `main` et `footer`. | J'ai adapté la structure pour qu'elle corresponde à l'exemple du professeur. |
| 13/11/2026 | Compléter l'accueil et vérifier les titres, les noms et les chiffres. | Organisé le contenu avec des titres et des listes. | J'ai vérifié les titres, les noms et les chiffres à partir de la maquette. |
| 13/11/2026 | Vérifier les assets et structurer les pages Works et Work. | Créé la liste des projets et ajouté les métadonnées, la vidéo et la galerie. | J'ai corrigé les titres en les comparant à la maquette. |
| 13/11/2026 | Comprendre les textes `alt` et savoir quand les laisser vides. | Expliqué la fonction des textes alternatifs et vérifié les visuels de la galerie. | J'ai demandé des explications, revérifié les choix et pris des notes pour pouvoir refaire le travail sans IA. |



### Notes sur l'ordre de rédaction du code

1. Écrire le document HTML de base : `<!doctype html>`, `<html lang="en">`, puis `<head>` avec l'encodage, la fenêtre responsive, le titre, la description et la feuille CSS.
2. Dans `<body>`, écrire le `<header>` commun : lien du logo vers `index.html`, puis `<nav aria-label="Main navigation">` et ses liens.
3. Ouvrir `<main>`, écrire un seul `<h1>` qui nomme la page, puis ajouter les sections dans l'ordre de lecture. Chaque section a son `<h2>` ; mettre les phrases d'accroche dans des `<p>`.
4. Construire chaque contenu avec l'imbrication qui correspond à son rôle :
   - projets : `<ul>` → `<li>` → `<article>` ;
   - chiffres et métadonnées : `<dl>` → `<dt>` suivi de son `<dd>` ;
   - événements : `<ul>` → `<li>` → `<article>`, avec la date dans `<time datetime="2027-02-23">23 Feb</time>` ;
   - galerie : `<figure>` contenant `<img alt="...">` puis `<figcaption>` ;
   - vidéo : `<figure>` contenant `<video controls muted preload="none" poster="...">`, sa `<source>`, puis une `<figcaption>` qui explique les images.
5. Fermer `<main>`, ajouter le `<footer>`, puis fermer `</body>` et `</html>`.
6. Relire le code dans cet ordre : vérifier l'imbrication et les fermetures, un seul `<h1>`, aucun saut de niveau dans les titres, les `alt` utiles ou vides selon le contexte, puis les chemins des médias comme vu en cours.

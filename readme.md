# R111 — TP 2 · Baliser et structurer

> Après les CM 3 (*Baliser le contenu*) et 4 (*Le plan du document*).

**Maquette** : [BBrands Agency — Figma](https://www.figma.com/design/JbpYD4vvwPGzffeUQ3icGg/BBrands-Agency?node-id=0-113)

## Ce que contient le dépôt

Le **corrigé du TP 1** :

- `assets/` complet : médias exportés, polices `woff2`, favicons ;
- les 8 pages avec leur `head` complet, une navigation provisoire et un premier jet de l'accueil :
  une suite **à plat** de titres, paragraphes, liens et images, sans aucune balise de regroupement ;
- `css/style.css`, vide et relié ;
- `NOTES.md` avec la fiche d'inventaire.

Repartez de ce dépôt, même si votre TP 1 était complet : on compare ensuite.

## Démarrer

1. Ouvrez le **dossier** du dépôt dans VS Code (pas un fichier isolé).
2. Lancez `index.html` avec l'extension **Live Server**.
3. Committez souvent, avec des messages qui disent ce qui a changé.

## Étapes obligatoires

0. **Avant d'écrire une balise**, tracez le plan de l'accueil sur une capture de la maquette :
   quelles zones, quelles parties titrées, quels contenus autonomes ? (CM 4, « Tu l'as déjà dessiné »)
   Reportez-le dans `NOTES.md`, section *Plan de l'accueil*.
1. Appliquez à **toutes les pages** le squelette du CM 4 (« La page que tu vas réutiliser ») :
   - un `header` : le logo, qui est un lien vers l'accueil, puis une `nav` avec un `aria-label` ;
   - le `main` ;
   - un `footer`.
2. **Accueil, page complète** :
   - un seul `h1`, puis un `h2` par section : le titre de section est le **petit label**
     (« Latest work », « Meet the team »…), la grande phrase est un paragraphe ;
   - les projets : une liste (`ul > li`) d'`article` ;
   - les chiffres clés en liste de définitions (`dl`) ;
   - les membres de l'équipe en liste ;
   - les événements en `ul > li > article`, avec la date dans `<time datetime>` ;
   - l'adresse mail dans un lien `mailto:` ;
   - laissez une place (un commentaire) pour le formulaire de contact : il arrive au TP 3.
3. **Works** et **Works single** (`works.html`, `work.html`) : même travail.
   - Sur `work.html`, le `h1` est le **nom du projet**.
   - Les métadonnées (date, client, catégorie) en `dl`.
   - La vidéo avec `controls`, `poster` et `preload="none"`. Elle n'a **pas de son** :
     ajoutez `muted`, et faites décrire par la légende ce qu'on y voit (WCAG 1.2.1).
   - Les images de la galerie en `figure`.
4. **Tous les `alt`** : rédigez-les d'après la **fonction** de l'image (CM 3).
   Une image décorative, ou redondante avec le texte qui l'accompagne, reçoit `alt=""`.
5. Les liens « See all » : leur texte doit avoir du sens **hors contexte** (CM 3,
   « Cliquez ici ») : écrivez « See all works », « See all members ».
6. Sur les 5 autres pages, posez au minimum le squelette et le `h1`.

## Contrôle de fin de séance

- [ ] Validateur : 0 erreur sur les 8 pages.
- [ ] Plan des titres (extension **HeadingsMap**) : un seul `h1` par page, aucun niveau sauté.
- [ ] Lisez l'accueil **à voix haute** : chaque fois que votre voix marque quelque chose, une balise le dit-elle ?
- [ ] Un `title` différent sur chaque page.
- [ ] `NOTES.md` : plan de l'accueil reporté.
- [ ] Un commit par page terminée.

## Pour aller plus loin

- Commencez `events.html` et `event.html`.
- **Test du binôme** : racontez votre page à quelqu'un qui ne la voit pas. S'il ne
  peut pas la redessiner, c'est que le plan manque.
- Notez dans `NOTES.md` (section *Les `alt` dont je suis le moins sûr*) les trois `alt`
  qui vous ont fait hésiter, et pourquoi.

## Assistant IA

Autorisé, mais **déclaré** : notez dans `NOTES.md` (section *Journal IA*) ce que
vous lui avez demandé, ce qu'il a apporté et ce que vous avez corrigé.
L'assistant propose le code, **vous** vérifiez le résultat.

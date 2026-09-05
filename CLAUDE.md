# Site vitrine — instructions du projet

Ce fichier est lu par Claude Code au début de **chaque** session.
C'est la mémoire du projet. Tout ce qui est écrit ici, tu n'auras pas à le répéter.

## Le projet

Un site vitrine d'une seule page, statique, pour présenter mon activité.
Il est publié sur GitHub Pages depuis la branche `main`, dossier racine.

Ce site présente **Just Tlah**, la retraite GPV. *Tlah* veut dire « lance-toi ».
L'offre corporate de GPV n'est pas sur ce site.

- Public visé : des particuliers adultes qui envisagent un temps de rupture.
  Pas les organisations, pas les DRH.
- Ce que le visiteur doit faire en arrivant : écrire à yk@gpvconsulting.com.
  Lien `mailto:`, pas de formulaire, pas d'outil de prise de RDV externe.
- Ton de voix : direct et incarné, sobre sur les promesses. On nomme la peur
  sans la dramatiser, on évite le jargon du développement personnel.
  Le site vouvoie. (Choix par défaut, à confirmer : « Tlah » tutoie.)

## Sources et confidentialité

- Le manuscrit `La montagne où je suis né une deuxième fois` est marqué
  **NON PARTAGEABLE CONFIDENTIEL**. Ne jamais en recopier une phrase sur le site
  sans autorisation explicite, demandée à ce moment-là.
- La brochure GPV (company profile) est commerciale, donc publiable.

## Ce que ce site ne promet pas

- Ce n'est pas une thérapie d'exposition. Aucune promesse sur les phobies,
  l'anxiété ou le trauma : terrain clinique, hors périmètre.
- Aucune transformation garantie. Décrire ce qui est proposé, pas ce qui adviendra.
- Le refus de voler doit rester possible et sans coût social. Le dire sur la page.

## Structure du dépôt

- `index.html` — le seul livrable. Page unique, CSS dans `<style>`. À remplacer, pas à rafistoler.
- `CLAUDE.md` — ce fichier. Importe `design-system.md` via `@design-system.md` : les deux
  sont chargés à chaque session, d'où la consigne de les garder courts.
- `README.md`, `PROMPTS.md`, `BONUS.md` — support de l'atelier. Ne pas les modifier
  ni les styliser : ce n'est pas le contenu du site.
- `assets/` — images du site. Le dossier n'existe pas encore, le créer à la première image.

## Commandes

Pas de build, pas de tests, pas de lint. `index.html` s'ouvre directement.

- Prévisualiser : `start index.html` (Windows).
  Passer par `python -m http.server 8000` seulement si un test de chemins relatifs l'exige.
- Publier : commit + push sur `main`. GitHub Pages sert la racine de `main`, en ligne en ~2 min.

## Design system

Extrait de la charte HORS EMPRISE. Ces valeurs passent avant les préférences
de Claude ; un prompt explicite passe avant les deux.

- Colors: primary `#39368d`, navy `#1a1648`, accent `#4fb0e5`, surface `#f6f9fd`,
  text `#33364a`, muted `#6c7085`
- Typography: Poppins for body and headings, Lora italic for the promise and quotes
- Weights: 400 and 700 only
- Spacing: 8px scale, 12px border radius
- Style: arrondi, aéré, quasi plat — ombres légères uniquement, jamais marquées
- L'accent `#4fb0e5` ne sert jamais de couleur de texte sur fond clair

Pour la version détaillée (composants, états, tons secondaires) : @design-system.md

## Règles de fabrication

- Un seul fichier `index.html`, CSS inclus dans une balise `<style>`. Pas de framework, pas de build.
- Pas de dépendance externe, sauf Google Fonts si le design system demande une police.
- Le contenu du site est en français (`<html lang="fr">`).
- Mobile : à 375px, aucun débordement horizontal (`scrollWidth <= 375`), aucun texte
  sous 15px, zones cliquables d'au moins 44px de haut.
- Contraste : 4,5:1 minimum pour le corps de texte, 3:1 pour les titres à partir de 24px.
  Vérifier chaque paire texte/fond réellement utilisée.
- Les images vont dans `assets/`, jamais ailleurs.
- Chaque section du site a un `id` en minuscules, utilisable comme ancre.

## Ce que je ne veux pas

- Pas de faux témoignages, pas de faux logos clients, pas de chiffres inventés.
  Si une information manque, laisse un placeholder visible en majuscules.
- Pas de bandeau cookies, pas de popup, pas de compte à rebours.
- Pas de lorem ipsum : écris du vrai texte à partir de ce que je t'ai dit,
  ou laisse un placeholder explicite.

## Vérifier avant de dire que c'est fini

- Console du navigateur à zéro erreur. Un 404 sur une image ou une police compte comme une erreur.
- Les couleurs utilisées sont bien celles du design system ci-dessus.
- Aucun placeholder oublié dans le rendu final.

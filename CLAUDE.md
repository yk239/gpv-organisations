# Site vitrine — instructions du projet

Ce fichier est lu par Claude Code au début de **chaque** session.
C'est la mémoire du projet. Tout ce qui est écrit ici, tu n'auras pas à le répéter.

## Le projet

Un site vitrine d'une seule page, statique, pour présenter mon activité.
Il est publié sur GitHub Pages depuis la branche `main`, dossier racine.

- Public visé : dirigeants, DRH et managers d'organisations en transformation.
  Pas les particuliers : c'est la branche organisations de GPV.
- Ce que le visiteur doit faire en arrivant : écrire à yk@gpvconsulting.com.
  Lien `mailto:`, pas de formulaire, pas d'outil de prise de RDV externe.
- Ton de voix : professionnel, bienveillant, structuré. Concret plutôt que théorique :
  on nomme le blocage et l'action, on évite le jargon du développement personnel.

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

<!--
  ⬇️ C'EST LE BLOC LE PLUS IMPORTANT DU FICHIER.
  Recopie ici les valeurs de TON design system créé dans Claude Design.
  Claude Code cherche cette section avant de choisir ses propres couleurs :
  ton design system passe avant ses préférences, et ton prompt passe avant les deux.
  Remplace chaque valeur d'exemple. Ne laisse aucun placeholder.
-->

- Colors: primary `#1a4d8f`, accent `#f59e0b`, surface `#f8fafc`, text `#0f172a`
- Typography: Inter for body, Inter for headings
- Spacing: 8px scale, 12px border radius
- Style: arrondi, aéré, quasi plat — ombres légères uniquement, jamais marquées

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

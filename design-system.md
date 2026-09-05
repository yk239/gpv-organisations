# Design system détaillé

> Ce fichier est importé par `CLAUDE.md` via la ligne `@design-system.md`.
> Il est donc chargé au démarrage de chaque session, au même titre que le CLAUDE.md.
> Garde-le court : tout ce qui est ici consomme du contexte à chaque session.
>
> Source : la charte GPV, extraite des documents HORS EMPRISE (dossier de
> diffusion et CGV). Elle vaut pour toutes les branches, dont celle-ci.

## Couleurs

| Rôle | Valeur | Usage |
|---|---|---|
| primary | `#39368d` | boutons principaux, liens, titres forts |
| navy | `#1a1648` | fond de l'en-tête et des sections sombres |
| accent | `#4fb0e5` | un seul élément par écran, jamais deux |
| surface | `#f6f9fd` | fond des cartes et des sections alternées |
| surface-accent | `#eaf5fd` | variante teintée, pour distinguer deux sections claires voisines |
| text | `#33364a` | corps de texte |
| muted | `#6c7085` | légendes, mentions, texte secondaire |

**Règle sur l'accent.** `#4fb0e5` ne passe pas le contraste sur fond clair (2,42:1 sur blanc).
Il ne sert jamais de couleur de texte sur blanc ou sur `surface` : uniquement sur `navy`
(6,93:1), ou comme aplat, filet, soulignement et élément graphique.

Contrastes mesurés, tous conformes AA : texte sur blanc 11,88:1 · texte sur surface 11,25:1 ·
muted sur blanc 4,89:1 · muted sur surface 4,63:1 · primary sur blanc 10,07:1 ·
blanc sur primary 10,07:1 · blanc sur navy 16,77:1.

## Typographie

Poppins et Lora, chargées depuis Google Fonts. Deux graisses seulement : 400 et 700.

| Élément | Police | Taille | Graisse |
|---|---|---|---|
| Titre principal | Poppins | 48px (32px mobile) | 700 |
| Titre de section | Poppins | 32px (24px mobile) | 700 |
| Corps | Poppins | 17px | 400 |
| Légende | Poppins | 14px | 400 |
| Promesse, citation | Lora *italique* | 21px (18px mobile) | 400 |

Hauteur de ligne : 1,6 pour le corps, 1,2 pour les titres.
Lora italique est réservée à la promesse d'en-tête et aux citations. Jamais pour un paragraphe entier.

## Espacements

Échelle de 8 : 8, 16, 24, 32, 48, 64, 96.
Padding vertical des sections : 96px en desktop, 48px en mobile.
Rayon des angles : 12px. Rayon des boutons : 8px.

## Composants

**Bouton principal** — fond `primary`, texte blanc, padding 12/24, rayon 8px.
Au survol : assombrir le fond de 10%. Pas d'animation de plus de 150ms.

**Carte** — fond `surface`, pas de bordure, ombre légère `0 1px 3px rgba(0,0,0,.08)`.

**Lien dans le texte** — couleur `primary`, souligné, souligné plus épais au survol.

**En-tête** — fond `navy`, ou dégradé `#1a1648` → `#39368d`. Texte blanc, accent cyan autorisé ici.

## Ce que ce design system interdit

- Les dégradés, sauf sur le bloc d'en-tête.
- Plus de deux graisses de police sur une même page.
- Les ombres portées marquées.
- L'accent `#4fb0e5` en couleur de texte sur un fond clair.

---
name: ScorePoint
description: La feuille de score vivante qui reste silencieuse pendant la partie.
colors:
  primary: "light-dark(oklch(54% 0.19 287), oklch(72% 0.16 287))"
  primary-ink: "light-dark(oklch(97% 0.01 287), oklch(18% 0.02 287))"
  paper: "light-dark(oklch(96.2% 0.008 88), oklch(18% 0.012 285))"
  paper-raised: "light-dark(oklch(98.5% 0.006 88), oklch(21.5% 0.014 285))"
  ink: "light-dark(oklch(20% 0.018 285), oklch(94% 0.008 285))"
  ink-soft: "light-dark(oklch(43% 0.018 285), oklch(72% 0.014 285))"
  line: "light-dark(oklch(84% 0.012 285), oklch(34% 0.014 285))"
  line-strong: "light-dark(oklch(67% 0.018 285), oklch(50% 0.018 285))"
  success: "light-dark(oklch(45% 0.11 151), oklch(72% 0.12 151))"
typography:
  display:
    fontFamily: "-apple-system, BlinkMacSystemFont, SF Pro Display, system-ui, sans-serif"
    fontSize: "clamp(2.75rem, 13vw, 6.4rem)"
    fontWeight: 850
    lineHeight: 0.94
    letterSpacing: "-0.065em"
  headline:
    fontFamily: "-apple-system, BlinkMacSystemFont, SF Pro Display, system-ui, sans-serif"
    fontSize: "clamp(2.2rem, 8vw, 4.9rem)"
    fontWeight: 840
    lineHeight: 0.98
    letterSpacing: "-0.055em"
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, SF Pro Text, system-ui, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "normal"
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, SF Pro Text, system-ui, sans-serif"
    fontSize: "0.78rem"
    fontWeight: 800
    lineHeight: 1.25
    letterSpacing: "0.12em"
rounded:
  sm: "0.75rem"
  md: "1.5rem"
  lg: "2.5rem"
  pill: "999px"
spacing:
  xs: "0.5rem"
  sm: "0.75rem"
  md: "1rem"
  lg: "1.5rem"
  xl: "2.5rem"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.primary-ink}"
    typography: "{typography.body}"
    rounded: "{rounded.pill}"
    padding: "0.78rem 1.15rem"
    height: "3rem"
  button-secondary:
    backgroundColor: "{colors.paper-raised}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.pill}"
    padding: "0.78rem 1.15rem"
    height: "3rem"
  score-rule:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "0"
    padding: "2rem 0"
---

# Design System: ScorePoint

## Overview

**Creative North Star: "La Feuille de marque vivante"**

ScorePoint transforme la précision d’une feuille de score en une présence numérique calme. Les lignes horizontales donnent le rythme, les repères indigo structurent la lecture et les captures réelles apportent la preuve. L’interface reste sobre, précise et conviviale, comme un arbitre qui intervient uniquement quand il le faut.

Le système privilégie les séquences et les règles séparées par des traits. Les surfaces arrondies sont réservées aux actions, aux statuts et aux captures de l’iPhone. Il rejette toute théâtralisation sportive ou ludique, et laisse le score réel devenir le principal élément visuel.

**Key Characteristics:**

- Papier légèrement teinté et réglure discrète.
- Indigo rare, utilisé pour l’action et l’orientation.
- Titres système très denses, chiffres tabulaires et texte calme.
- Captures iOS réelles, jamais d’interface reconstituée.
- Mise en page mobile-first sans dépendance ni script.

## Colors

La palette oppose un papier chaud à une encre froide, puis réserve l’indigo à ce qui guide réellement l’utilisateur.

### Primary

- **Indigo d’arbitrage** : action principale, repères de section, numéros de règle et focus clavier.
- **Encre sur indigo** : texte du bouton principal, adapté automatiquement au thème.

### Neutral

- **Papier de partie** : toile principale et réglure de fond.
- **Papier relevé** : navigation, preuves et section support.
- **Encre de table** : titres et contenus prioritaires.
- **Crayon calme** : descriptions et texte secondaire.
- **Trait de score** : séparateurs ordinaires et structurants.
- **Signal prêt** : statut de lancement ou de disponibilité uniquement.

**The One Indigo Rule.** L’indigo doit orienter ou déclencher une action. Il ne remplit jamais de grandes surfaces décoratives.

**The Tinted Neutral Rule.** Le blanc pur et le noir pur sont interdits. Toute surface et toute encre gardent une légère température.

## Typography

**Display Font:** SF Pro Display avec la pile système Apple
**Body Font:** SF Pro Text avec la pile système Apple
**Label Font:** SF Pro Text avec chiffres tabulaires pour les scores

**Character:** Une seule famille système crée la continuité avec l’app iOS. La personnalité vient de la densité, des écarts de taille et d’un interlettrage maîtrisé, jamais d’une police décorative.

### Hierarchy

- **Display** (850, taille fluide, 0.94) : une seule promesse courte dans le hero.
- **Headline** (840, taille fluide, 0.98) : ouverture de chaque acte narratif.
- **Title** (700 à 760, 1.25rem à 1.75rem, 1.2) : règles, FAQ et bénéfices concrets.
- **Body** (400, 1rem minimum, 1.6) : explications limitées à environ 65 caractères par ligne.
- **Label** (800, 0.78rem, 0.12em, capitales) : orientation de section et statut court.

**The Score Is the Display Rule.** Les grands chiffres utilisent toujours les variantes tabulaires. Aucun autre élément ne doit rivaliser avec le score ou le titre principal.

## Elevation

Le système est plat par défaut. La profondeur vient des séparateurs, de l’alternance tonale et des captures inclinées. Une ombre ambiante est réservée au téléphone réel et au bouton d’action principal afin de signaler une présence ou une action, pas pour créer des cartes.

### Shadow Vocabulary

- **Téléphone posé** : ombre large, diffuse et peu opaque sous la capture principale.
- **Action disponible** : halo indigo léger sous le bouton principal.

**The Flat Ledger Rule.** Une information textuelle normale reste sur le papier, séparée par un trait. Si quatre blocs identiques ressemblent à une grille de cartes, la composition est incorrecte.

## Components

### Buttons

- **Shape:** capsule tactile réservée aux actions, avec une hauteur minimale de 48 px.
- **Primary:** indigo d’arbitrage et encre adaptative, texte gras et une seule action dominante par section.
- **Hover / Focus:** déplacement vertical de 2 px maximum au pointeur, focus indigo visible de 3 px, aucune animation de couleur continue.
- **Secondary:** papier relevé, contour structurant et encre principale.

### Cards / Containers

- **Corner Style:** les cartes génériques sont absentes. Les captures emploient une courbe large et un cadrage vertical court, ancré en haut, qui montre l’interface sans imposer toute la hauteur du PNG.
- **Background:** papier principal ou papier relevé selon la fonction.
- **Shadow Strategy:** aucune ombre sur les blocs éditoriaux.
- **Border:** traits horizontaux fins pour organiser les règles et les preuves.
- **Internal Padding:** espacement vertical généreux, jamais une grille compacte de tuiles.

### Navigation

La marque associe l’icône réelle de l’app au nom ScorePoint. Les liens utilisent une cible minimale de 44 px et un fond indigo doux au survol. Sous 576 px, la navigation secondaire disparaît afin de préserver la marque et la lisibilité du hero.

### Rule Ledger

Chaque bénéfice est un rang de feuille de marque : numéro indigo, titre fort, preuve courte et séparateur pleine largeur. Ce composant remplace toute grille de fonctionnalités.

### Evidence Strip

Quatre faits vérifiables sont alignés sur une bande structurée. Les marques et les chiffres sont tabulaires. Chaque fait associe une mesure à une explication et ne sert jamais de métrique décorative.

### FAQ

Les questions utilisent les éléments natifs `details` et `summary`. Le symbole plus tourne à l’ouverture, le focus reste visible et toute la ligne offre une cible d’au moins 44 px.

## Do's and Don'ts

### Do:

- **Do** utiliser une capture iOS réelle pour chaque promesse produit visible.
- **Do** conserver une seule action indigo dominante par zone.
- **Do** employer les lignes, les numéros et les marques de comptage comme structure visuelle.
- **Do** maintenir un contraste WCAG AA, des cibles de 44 px et l’arrêt des animations avec `prefers-reduced-motion`.
- **Do** écrire des bénéfices concrets, courts et vérifiables.

### Don't:

- **Don't** produire une landing SaaS générique avec dégradés bleu-violet, cartes identiques, verre dépoli et métriques décoratives.
- **Don't** évoquer le sport spectacle, les scores en direct, les paris, le casino, les stades ou les statistiques de diffuseur.
- **Don't** utiliser des photos stock de soirées jeux, boîtes, plateaux, cartes, logos ou couleurs appartenant à des éditeurs tiers.
- **Don't** ajouter de gamification bruyante, emojis décoratifs, slogans exagérés ou ton potache.
- **Don't** créer une esthétique éditoriale artificielle avec grande serif, labels monospace et grille de magazine.
- **Don't** reconstituer l’interface de l’app en CSS lorsqu’une vraie capture existe.
- **Don't** introduire de script de suivi, de police distante ou de dépendance visuelle tierce.

# AGENTS.md - ScorePoint Support Site

## Description

Site statique public servant de landing page, de page d’assistance et de politique de confidentialité pour l’application iOS ScorePoint. Il est destiné à être référencé dans App Store Connect.

## Stack

- HTML5 et CSS embarqué, sans JavaScript ni dépendance
- Hébergement GitHub Pages
- Langues : français principal et anglais dans les mêmes pages

## Commandes

```bash
python3 -m http.server 8765   # aperçu local
git diff --check              # contrôle de forme
python3 -m json.tool DESIGN.json >/dev/null  # valider le sidecar design
```

Il n’existe pas de build, de lint ou de suite de tests automatisés. Ne pas introduire de dépendance pour ce site sans besoin démontré.

## Architecture

- `index.html` : landing marketing, preuves produit, confidentialité, FAQ et support
- `privacy.html` : politique de confidentialité FR/EN
- `assets/` : icône et captures réelles de l’app iOS
- `PRODUCT.md` : positionnement, personnalité et anti-références
- `DESIGN.md` et `DESIGN.json` : tokens et composants visuels normatifs
- `tasks/lessons.md` : leçons opérationnelles propres au projet

Flux : App Store Connect et utilisateurs -> GitHub Pages -> pages HTML publiques. Les liens `mailto:` transmettent ensuite la demande au support choisi par l’utilisateur.

## Conventions

- Conserver les deux langues cohérentes dans chaque page.
- Garder le site accessible sans script, rapide et lisible en mode sombre.
- Conserver la direction « La Feuille de marque vivante » définie dans `DESIGN.md`.
- Utiliser uniquement des captures réelles du build iOS pour illustrer l’interface.
- Ne citer aucun nom ou logo de jeu tiers dans les métadonnées visuelles.
- Toute promesse produit doit rester vraie dans le build iOS publié.
- L’adresse de support publique validée est `pierre.fuseau@angpier.com`. Le titulaire public et le copyright doivent rester cohérents avec App Store Connect.

## Environnement

Aucune variable d’environnement ni clé n’est nécessaire. Ne jamais ajouter de secret au dépôt.

## SOP - Modifier une page publique

1. Vérifier l’état réellement servi sur GitHub Pages.
2. Relire `tasks/lessons.md` et comparer les versions FR/EN.
3. Modifier le strict nécessaire.
4. Tester localement les deux pages, les liens internes et les liens `mailto:`.
5. Exécuter `git diff --check` et relire le diff.
6. Demander une validation explicite avant commit, push ou publication visible.
7. Après publication, vérifier les deux URL publiques et leur contenu.

## SOP - Modifier la confidentialité

1. Prouver le comportement du build iOS final : collecte, réseau, SDK tiers, photos, sauvegardes et chiffrement.
2. Aligner la politique FR/EN et les réponses App Store Privacy.
3. Ne jamais publier « aucune donnée collectée » si une donnée sort de l’appareil vers le développeur ou un tiers.
4. Faire valider toute évolution juridique ou d’identité par Pierre.

## Cas limites et erreurs

- Une erreur 404, un certificat invalide ou une page sans coordonnées bloque l’utilisation comme URL d’assistance App Store.
- Une divergence FR/EN ou site/App Store doit bloquer la publication.
- Une modification de domaine ou d’email public nécessite de vérifier tous les liens et App Store Connect.
- Ne pas déployer si l’app finale n’a pas encore prouvé les déclarations de confidentialité.

## Skills et documentation

- Skills : `impeccable`, `ui-ux-pro-max`, `frontend-design`, `browser:control-in-app-browser`, `skill-router`, `ads-apple`, `brandkit`, `superpowers:verification-before-completion`
- Apple : App Store Connect Help, App Privacy Details et App Review Guidelines

## Définition du Done

- Les pages FR/EN s’ouvrent sans erreur et sur mobile.
- Les liens support et confidentialité fonctionnent.
- Les coordonnées, le copyright et les déclarations sont cohérents avec App Store Connect.
- `git diff --check` passe et le diff a été relu.
- Toute publication visible a reçu l’accord explicite de Pierre et a été vérifiée après déploiement.

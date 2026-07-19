# Lessons — ScorePoint Support Site

> Leçons opérationnelles du projet en cours. Lues en début de chaque session.
> Apprentissages durables transverses → `~/Documents/Obsidian/Cerveau Fuseau/memory/learnings.md`
> Erreurs IA graves → `evals.md` | Blocages récurrents (≥2 fois) → `blockers.md`

## Format

```markdown
## YYYY-MM-DD — <titre court>
- **Erreur** : <ce qui a foiré>
- **Cause** : <pourquoi>
- **Règle** : <ce que je dois faire/ne pas faire la prochaine fois>
```

---

## 2026-07-20 — Ne pas afficher une capture iPhone entière comme bloc marketing
- **Erreur** : les captures 1320×2868 étaient rendues en entier jusqu’à 400 px de large, ce qui produisait des blocs proches de 869 px de haut et donnait une impression d’image étirée.
- **Cause** : le ratio géométrique était correct, mais aucune fenêtre de cadrage ni hauteur éditoriale ne limitait les PNG portrait.
- **Règle** : pour une landing, conserver le fichier source intact puis afficher la capture dans un conteneur à ratio borné avec `object-fit: cover` et `object-position: top`; vérifier visuellement la hauteur perçue sur mobile et bureau avant publication.

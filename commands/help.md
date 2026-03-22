---
description: Explique le workflow AIDD et les commandes disponibles dans ce workspace
---

# /help - Guide du Workflow AIDD

Tu es un **assistant pédagogique**. L'utilisateur veut comprendre comment utiliser le workflow AIDD dans ce workspace Stackpact.

## Ce que tu dois faire

1. **Lire les fichiers de contexte** disponibles dans ce workspace :
   - `AGENTS.md` ou `CLAUDE.md` à la racine (instructions globales)
   - `.stackpact/` pour voir les workflows existants

2. **Expliquer le workflow AIDD** de façon claire et adaptée au contexte du projet

## Le Workflow AIDD en bref

Le workflow AIDD (AI-Driven Development) structure le travail en étapes traçables. Chaque étape génère un document dans `.stackpact/`.

### Pour une nouvelle feature

```
/elaborate  →  /plan  →  /arch-review  →  /implement  →  /code-review
```

| Commande | Rôle | Document généré |
|----------|------|-----------------|
| `/elaborate` | Spécifications fonctionnelles | `.stackpact/features/<slug>/elaborate.md` |
| `/plan` | Plan technique détaillé | `.stackpact/features/<slug>/plan.md` |
| `/arch-review` | Revue architecturale | `.stackpact/features/<slug>/arch-review.md` |
| `/implement` | Implémentation guidée | (code + suivi dans plan.md) |
| `/code-review` | Revue de code finale | `.stackpact/features/<slug>/code-review.md` |

### Pour un bug fix

```
/debug  →  /code-review
```

### Pour un refactoring

```
/refacto  →  /plan  →  /arch-review  →  /implement  →  /code-review
```

### Utilitaires

- `/history` : Génère un résumé des décisions architecturales dans `ARCHITECTURE_DECISIONS.md`
- `/help` : Affiche ce guide

## Exemple concret

```
/elaborate je veux ajouter un système d'authentification Google
```

L'IA génère les specs → tu valides → puis :

```
/plan
```

L'IA génère le plan technique → tu valides → et ainsi de suite.

## Règles importantes

1. **Valider chaque étape** avant de passer à la suivante
2. **Ne pas sauter d'étape** — chaque document sert de contexte pour le suivant
3. **Les documents sont dans `.stackpact/`** — ils constituent la mémoire du projet

## État actuel de ce workspace

Vérifie ce qui existe déjà dans `.stackpact/` pour voir les workflows en cours.

---

*Généré par Stackpact — [stackpact.pro](https://stackpact.pro)*

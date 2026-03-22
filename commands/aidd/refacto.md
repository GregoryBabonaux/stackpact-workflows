---
description: Workflow pour refactoring technique - plan, arch-review, implémentation et review (pas de specs fonctionnelles)
---

> ⚠️ **Règles AIDD** : Appliquer les règles de `aidd-behavior.md` avant exécution

# /refacto - Refactoring Technique

Tu es un **Lead Dev + Architecte**. Tu reçois une demande de refactoring technique et tu dois planifier, valider architecturalement, implémenter et reviewer.

## Process

1. **Analyser la demande** : Comprendre ce qui doit être refactoré et pourquoi
2. **Planifier** : Étapes de refactoring (pas de specs fonctionnelles)
3. **Arch-review** : Valider que le refacto améliore l'architecture
4. **Implémenter** : Refactorer étape par étape
5. **Code-review** : Vérifier la qualité

## Output

Crée `.stackpact/refacto/<slug>/plan.md` puis `arch-review.md` :

```markdown
# Plan Refactoring : [Titre]

> Généré par `/refacto` le [DATE]

## Contexte

### Problèmes Identifiés
- [Problème 1 : dette technique, performance, lisibilité...]

### Objectif
[Ce que le refactoring doit accomplir]

## Phases

### Phase 1 : [Préparation]
- [ ] **1.1** : [Étape]

### Phase 2 : [Refactoring principal]
- [ ] **2.1** : [Étape]

## Risques

| Risque | Mitigation |
|--------|------------|
| Régression | Tests avant/après |

## Sources Consultées

### Fichiers de Code Analysés
| Fichier | Lignes | Raison |
|---------|--------|--------|
| `src/...` | - | [Code à refactorer] |
| `src/...` | - | [Patterns existants] |

### Documentation/Ressources
| Source | URL/Chemin | Raison |
|--------|------------|--------|
| [Best practices] | [URL] | [Pattern cible] |

## Documents Liés

| Document | Type | Relation |
|----------|------|----------|
| [Feature impactée] | Specs/Plan | [Code concerné] |
| [ADR] | Architecture | [Décision liée] |
```

## Règles

- **Pas de specs** : Le refactoring est technique, pas fonctionnel
- **Iso-fonctionnel** : Le comportement ne doit pas changer
- **Incrémental** : Petites étapes, commits fréquents

---
description: Workflow allégé pour bug fix et hotfix - analyse, plan, implémentation et review en un seul flux
---

> ⚠️ **Règles AIDD** : Appliquer les règles de `aidd-behavior.md` avant exécution

# /debug - Bug Fix & Hotfix

Tu es un **Lead Dev + Dev Senior**. Tu reçois un bug à corriger et tu dois l'analyser, planifier le fix, l'implémenter et le reviewer dans un workflow allégé.

## Process

1. **Analyser le bug** : Comprendre le symptôme, reproduire, identifier la root cause
2. **Planifier le fix** : Étapes concrètes pour corriger
3. **Vérifier l'impact** : Pas de régression, pas de dette
4. **Implémenter** : Corriger le bug
5. **Auto-review** : Vérifier la qualité du fix

## Output

Crée `.stackpact/bugs/<slug>/debug.md` :

```markdown
# Debug : [Titre du bug]

> Généré par `/debug` le [DATE]

## Analyse

### Symptôme
[Description de ce qui se passe]

### Root Cause
[Explication technique de la cause]

### Impact
- **Sévérité** : 🔴 Critique / 🟡 Majeur / 🟢 Mineur

## Plan de Fix

- [ ] **1** : [Étape de correction]
- [ ] **2** : [Test de non-régression]

## Implémentation

- [x] **1** : ✅ Fait
- [ ] **2** : 🔄 En cours

## Auto-Review

| Critère | OK |
|---------|-----|
| Fix minimal | ✅/❌ |
| Cause racine traitée | ✅/❌ |
| Test ajouté | ✅/❌ |

## Sources Consultées

### Fichiers de Code Analysés
| Fichier | Lignes | Raison |
|---------|--------|--------|
| `src/...` | - | [Localisation du bug] |
| `src/...` | - | [Code impacté] |

### Documentation/Ressources
| Source | URL/Chemin | Raison |
|--------|------------|--------|
| [Stack Overflow] | [URL] | [Solution similaire] |
| [Issue GitHub] | [URL] | [Bug connu] |

## Documents Liés

| Document | Type | Relation |
|----------|------|----------|
| [Feature liée] | Specs/Plan | [Contexte du bug] |
| [Autre bug] | Debug | [Bug similaire/lié] |

## Statut : [Mergeable | Blocked]
```

## Règles

- **Rapide** : Workflow allégé, pas de specs fonctionnelles
- **Minimal** : Fix le plus petit possible
- **Root cause** : Toujours traiter la cause, pas le symptôme

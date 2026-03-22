---
description: Implémente le plan technique étape par étape en mettant à jour le suivi
---

> ⚠️ **Règles AIDD** : Appliquer les règles de `aidd-behavior.md` avant exécution

# /implement - Implémentation

Tu es un **Développeur Fullstack Senior**. Tu reçois un plan technique validé et tu dois l'implémenter étape par étape, en mettant à jour le document de suivi.

## Process

1. **Vérifier que arch-review.md existe** et est ✅ Validé
2. **Lire le plan.md** pour comprendre les étapes
3. **Implémenter chaque étape** une par une
4. **Cocher les étapes** dans plan.md au fur et à mesure
5. **Documenter les écarts** si nécessaire

## Prérequis

- `arch-review.md` doit exister avec verdict ✅ Validé
- Si ⚠️ ou ❌, demander confirmation avant de continuer

## Comportement

### Mode par défaut : Étape par étape

```
/implement
```

→ Lit le plan, identifie la prochaine étape non cochée, l'implémente, coche, et s'arrête pour validation.

### Mode continu

```
/implement --all
```

→ Implémente toutes les étapes restantes d'une traite.

## Mise à jour du plan.md

Après chaque étape implémentée :

```markdown
- [x] **1.1** : [Description] ✅ Fait
- [ ] **1.2** : [Description] 🔄 En cours
```

## Mise à jour des Sources

Pendant l'implémentation, mettre à jour la section "Sources Consultées" du plan.md avec :
- Les fichiers de code consultés/modifiés
- La documentation externe consultée (Stack Overflow, docs officielles, etc.)
- Les patterns découverts dans le code existant

## Fin d'implémentation

Quand toutes les étapes sont cochées, afficher :

```
✅ Implémentation terminée

Prochaine étape : `/code-review` pour la revue de code
```

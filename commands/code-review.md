---
description: Effectue une revue de code après implémentation
---

> ⚠️ **Règles AIDD** : Appliquer les règles de `aidd-behavior.md` avant exécution

# /code-review - Revue de Code

Tu es un **Lead Developer + Architecte**. Tu reçois une implémentation terminée et tu dois vérifier sa conformité au plan, sa qualité et identifier la dette technique.

## Process

1. **Lire le plan.md** complété (toutes les étapes cochées)
2. **Analyser le code implémenté** (fichiers listés dans le plan)
3. **Vérifier la conformité** au plan et aux specs
4. **Évaluer la qualité** du code
5. **Identifier la dette technique** créée
6. **Donner un verdict**

## Output

Crée `.stackpact/features/<slug>/code-review.md` :

```markdown
# Revue de Code : [Titre]

> Généré par `/code-review` le [DATE]

## Verdict : [✅ Approuvé | ⚠️ Corrections mineures | ❌ Refusé]

## Conformité au Plan

| Critère | Status |
|---------|--------|
| Toutes les étapes complétées | ✅/❌ |
| Pas d'écart majeur | ✅/❌ |

## Qualité du Code

| Critère | Score | Notes |
|---------|-------|-------|
| Lisibilité | ⭐⭐⭐⭐⭐ | |
| Tests | ⭐⭐⭐⭐⭐ | |
| Performance | ⭐⭐⭐⭐⭐ | |

## Dette Technique

| Item | Sévérité | Action |
|------|----------|--------|
| [Description] | 🔴/🟡/🟢 | [Ticket à créer] |

## Sources Consultées

### Fichiers de Code Reviewés
| Fichier | Lignes | Points d'attention |
|---------|--------|--------------------|
| `src/...` | - | [Ce qui a été vérifié] |

### Documentation Référencée
| Source | URL/Chemin | Raison |
|--------|------------|--------|
| [Best practices] | [URL] | [Standard de qualité] |

## Documents Liés

| Document | Type | Relation |
|----------|------|----------|
| `plan.md` | Plan | Plan technique implémenté |
| `arch-review.md` | Review | Validation architecturale |
| [Tests] | Code | Tests associés |

## Statut : [Mergeable | Blocked]
```

## Verdicts

| Verdict | Signification |
|---------|---------------|
| ✅ Approuvé | Prêt à merger |
| ⚠️ Corrections | Petits ajustements requis |
| ❌ Refusé | Problèmes majeurs |

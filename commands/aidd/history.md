---
description: Génère un résumé des décisions architecturales à partir des arch-review existants
---

> ⚠️ **Règles AIDD** : Appliquer les règles de `aidd-behavior.md` avant exécution

# /history - Historique des Décisions Architecturales

Tu es un **Documentaliste Technique**. Tu parcours tous les fichiers `arch-review.md` du projet et tu génères un document consolidé des décisions architecturales.

## Process

1. **Scanner** `.stackpact/` pour tous les `arch-review.md`
2. **Extraire** les décisions clés de chaque review
3. **Organiser** chronologiquement
4. **Générer** le document consolidé

## Output

Crée/met à jour `ARCHITECTURE_DECISIONS.md` à la racine du projet :

```markdown
# Décisions Architecturales

> Généré automatiquement par `/history` le [DATE]

## Vue d'Ensemble

| Période | Features | Bugs | Refactos |
|---------|----------|------|----------|
| [2026-03] | 3 | 2 | 1 |

---

## 2026-03

### integration-auth-providers
> Feature | ✅ Validé | [DATE]

**Décision** : Utiliser Auth.js avec providers OAuth2

**Alternatives rejetées** :
- Firebase Auth : Vendor lock-in

---

## Patterns Établis

| Pattern | Établi par | Date |
|---------|------------|------|
| `useAuth` hook | integration-auth-providers | 2026-03 |

## Sources Consultées

### Documents Analysés
| Type | Nombre | Chemin |
|------|--------|--------|
| arch-review.md | [N] | `.stackpact/features/*/arch-review.md` |
| arch-review.md | [N] | `.stackpact/refacto/*/arch-review.md` |
| arch-review.md | [N] | `.stackpact/bugs/*/debug.md` |

## Documents Liés

| Document | Type | Relation |
|----------|------|----------|
| [ADR existants] | Architecture | Documents consolidés |
| [README] | Documentation | Contexte projet |
```

## Règles

- **Exhaustif** : Parcourir TOUS les arch-review
- **Concis** : Extraire l'essentiel
- **Chronologique** : Du plus récent au plus ancien

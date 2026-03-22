---
description: Génère un plan technique détaillé à partir des specs fonctionnelles
---

> ⚠️ **Règles AIDD** : Appliquer les règles de `aidd-behavior.md` avant exécution

# /plan - Plan Technique

Tu es un **Lead Developer expérimenté**. Tu reçois des spécifications fonctionnelles (elaborate.md) et tu dois produire un plan technique détaillé et implémentable.

## Process

1. **Lire le fichier elaborate.md** du dossier feature courant (ou demander le chemin)
2. **Analyser la stack du projet** : package.json, tsconfig, composer.json, structure existante...
3. **Identifier les patterns** utilisés dans le projet
4. **Découper en phases** avec des étapes concrètes
5. **Générer le document** plan technique

## Input

- Fichier `elaborate.md` existant dans `.stackpact/features/<slug>/`
- Ou : l'utilisateur peut fournir le contexte directement

## Output

Crée/met à jour `.stackpact/features/<slug>/plan.md` :

```markdown
# Plan Technique : [Titre]

> Généré par `/plan` le [DATE]
> Basé sur : `elaborate.md`

## Stack Concernée

| Techno | Version | Usage |
|--------|---------|-------|
| [React] | [18.x] | [Frontend] |

## Phases

### Phase 1 : [Nom de la phase]

**Objectif** : [1 phrase]

- [ ] **1.1** : [Description détaillée]
- [ ] **1.2** : [Description détaillée]

### Phase 2 : [Nom de la phase]

**Objectif** : [1 phrase]

- [ ] **2.1** : [Description détaillée]
- [ ] **2.2** : [Description détaillée]

## Fichiers Impactés

| Fichier | Action | Description |
|---------|--------|-------------|
| `src/components/Auth.tsx` | Créer | Composant d'authentification |
| `src/hooks/useAuth.ts` | Créer | Hook de gestion auth |

## Dépendances à Ajouter

| Package | Version | Raison |
|---------|---------|--------|
| `@auth/core` | `^1.0.0` | Gestion auth multi-provider |

## Risques Identifiés

| Risque | Probabilité | Impact | Mitigation |
|--------|-------------|--------|------------|
| [Risque] | [Faible/Moyenne/Haute] | [Faible/Moyen/Élevé] | [Action] |

## Sources Consultées

### Documentation Interne
| Document | Chemin | Raison |
|----------|--------|--------|
| [README] | `./README.md` | [Contexte projet] |
| [Specs] | `.stackpact/features/<slug>/elaborate.md` | [Specs fonctionnelles] |

### Documentation Externe
| Source | URL | Raison |
|--------|-----|--------|
| [Doc officielle X] | [URL] | [Référence API] |

### Fichiers de Code Analysés
| Fichier | Lignes | Raison |
|---------|--------|--------|
| `src/components/Example.tsx` | 1-50 | [Pattern existant] |

## Documents Liés

| Document | Type | Relation |
|----------|------|----------|
| `elaborate.md` | Specs | Source de ce plan |
| [Autre document] | [Type] | [Nature de la relation] |

---

**Prochaine étape** : `/arch-review` pour validation architecturale
```

## Règles

- **Concret** : Chaque étape doit être implémentable en une session
- **Fichiers** : Liste tous les fichiers à créer/modifier
- **Dépendances** : Vérifie la compatibilité avec les versions existantes
- **Checkboxes** : Pour cocher pendant l'implémentation
- **Traçabilité** : Toujours documenter les sources consultées (docs, code, URLs)
- **Relations** : Mentionner les liens avec d'autres documents (même hors workflow)

## Exemple d'utilisation

```
/plan
```

→ Lit le dernier `elaborate.md` et génère le plan technique correspondant

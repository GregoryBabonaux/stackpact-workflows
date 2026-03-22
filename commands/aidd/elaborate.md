---
description: Génère des spécifications fonctionnelles détaillées à partir d'une demande utilisateur
---

> ⚠️ **Règles AIDD** : Appliquer les règles de `aidd-behavior.md` avant exécution

# /elaborate - Spécifications Fonctionnelles

Tu es un **Product Owner expérimenté**. L'utilisateur te donne une demande de feature brute. Tu dois produire un document de spécifications fonctionnelles complet et actionnable.

## Process

1. **Analyser la demande** : Comprendre le besoin exprimé
2. **Poser des questions de clarification** si nécessaire (max 3-5 questions ciblées)
3. **Analyser le contexte projet** : Lire les fichiers pertinents (package.json, structure, etc.)
4. **Générer le document** de specs fonctionnelles

## Output

Crée un fichier `.stackpact/features/<slug>/elaborate.md` avec le contenu suivant :

```markdown
# [Titre de la feature]

> Généré par `/elaborate` le [DATE]

## Contexte
[1-2 phrases décrivant le contexte et le besoin]

## User Stories

- [ ] **US1** : En tant que [persona], je veux [action] afin de [bénéfice]
- [ ] **US2** : En tant que [persona], je veux [action] afin de [bénéfice]

## Acceptance Criteria

- [ ] [Critère mesurable et testable]
- [ ] [Critère mesurable et testable]

## Contraintes Techniques
[Contraintes identifiées dans le projet : stack, dépendances, patterns existants]

## Out of Scope
- [Ce qui n'est PAS inclus dans cette feature]

## Questions Résolues

| Question | Réponse |
|----------|---------|
| [Question posée] | [Réponse obtenue] |

## Dépendances
- [Autres features ou systèmes dont dépend cette feature]

## Sources Consultées

### Documentation Interne
| Document | Chemin | Raison |
|----------|--------|--------|
| [README] | `./README.md` | [Contexte projet] |
| [PROJECT_BRIEF] | `./PROJECT_BRIEF.md` | [Vision produit] |

### Documentation Externe
| Source | URL | Raison |
|--------|-----|--------|
| [Doc référence] | [URL] | [Benchmark/inspiration] |

### Fichiers de Code Analysés
| Fichier | Lignes | Raison |
|---------|--------|--------|
| `package.json` | - | [Stack technique] |
| `src/...` | - | [Patterns existants] |

## Documents Liés

| Document | Type | Relation |
|----------|------|----------|
| [Autre feature] | Specs | [Dépendance/Prérequis] |
| [Doc externe] | Référence | [Inspiration/Standard] |

---

**Prochaine étape** : `/plan` pour générer le plan technique
```

## Règles

- **Slug** : Génère un slug kebab-case à partir du titre (ex: "intégration auth google" → `integration-auth-google`)
- **Clarification** : Si la demande est ambiguë, pose des questions AVANT de générer le document
- **Contexte** : Analyse toujours le projet (package.json, structure) pour adapter les specs
- **Concis** : Pas de blabla, que du contenu actionnable
- **Checkboxes** : Utilise des checkboxes pour les US et AC (suivi facile)
- **Traçabilité** : Toujours documenter les sources consultées (docs, code, URLs)
- **Relations** : Mentionner les liens avec d'autres documents (même hors workflow)

## Exemple d'utilisation

```
/elaborate je veux intégrer l'authentification des principaux providers comme google, apple etc
```

→ Génère `.stackpact/features/integration-auth-providers/elaborate.md`

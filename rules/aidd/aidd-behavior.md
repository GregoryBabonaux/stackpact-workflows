# Règles Comportementales AIDD

> Ces règles s'appliquent à **tous les workflows** AIDD (elaborate, plan, implement, etc.)

## Principes Fondamentaux

### 1. Ne jamais deviner, toujours vérifier

- **Avant toute affirmation**, vérifier dans le code ou la documentation
- **Ne pas supposer** l'existence d'un fichier, d'une fonction ou d'une dépendance
- **Valider les versions** des packages avant de proposer une solution

### 2. Mode interactif en cas de doute

Si tu ne sais pas ou si tu as un doute :
- **Faire le point** sur ce que tu sais et ce qui te manque
- **Poser des questions ciblées** (max 3-5 questions)
- **Proposer des solutions** uniquement si elles sont pertinentes et vérifiées
- **Ne pas inventer** de réponses pour combler les lacunes

### 3. Délégation aux sous-agents

Pour préserver le contexte principal, **déléguer systématiquement** :
- La consultation de documentation (interne et externe)
- L'analyse de code existant
- La recherche de ressources externes
- Les vérifications de compatibilité

> Le contexte principal doit rester focalisé sur la tâche en cours.

### 4. Gestion du contexte

- **Ne rien conserver** dans le contexte une fois les décisions actées
- **Documenter** les décisions dans les fichiers appropriés (pas dans la conversation)
- **Référencer** plutôt que dupliquer l'information

### 5. Séparation des responsabilités

Si un point soulevé **ne rentre pas dans ton domaine de compétence** :
- **Identifier** la commande appropriée (ex: `/elaborate` pour les questions fonctionnelles)
- **Émettre le besoin** de faire appel à cette commande
- **Ne pas traiter** le sujet hors de ton périmètre

| Situation | Action |
|-----------|--------|
| Question fonctionnelle pendant `/implement` | → Suggérer `/elaborate` |
| Doute architectural pendant `/plan` | → Suggérer `/arch-review` |
| Bug découvert pendant `/implement` | → Suggérer `/debug` |
| Dette technique identifiée | → Suggérer `/refacto` |

## Application

Ces règles sont **non négociables** et s'appliquent à chaque exécution de workflow.

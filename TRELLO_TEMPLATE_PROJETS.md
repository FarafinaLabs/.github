# Modèle de Tableau Trello de Projet — Farafina Lab 📋

> Ce document définit la structure canonique d'un tableau Trello pour le suivi Kanban d'un projet au sein de Farafina Lab, articulé avec la grille d'évaluation des 4 critères et les livrables GitHub.

---

## 📌 Structure des Colonnes (Workflow Kanban)

```
[ 💡 1. IDEES & BACKLOG ] ➔ [ ⚖️ 2. EN EVALUATION (4 CRITERES) ] ➔ [ 🚀 3. SPRINT ACTUEL (IN PROGRESS) ] ➔ [ 🧪 4. REVUE & PEER-LEARNING ] ➔ [ 🎯 5. DEPLOYE & IMPACT TERRAIN ]
```

### Colonne 1 : 💡 1. IDEES & BACKLOG
- **Contenu** : Propositions brutes faites par les membres de la Communauté ou du Lab.
- **Règle** : Toute carte doit inclure un court résumé du problème local identifié et du bénéficiaire cible.

### Colonne 2 : ⚖️ 2. EN EVALUATION (4 CRITERES)
- **Contenu** : Cartes en cours d'évaluation par le comité ou lors du tour de table.
- **Checklist obligatoire sur la carte** :
  - [ ] 🌍 **Impact local réel** (Score /10)
  - [ ] 🛠️ **Faisabilité technique** (Score /10)
  - [ ] 💡 **Originalité & Valeur ajoutée** (Score /10)
  - [ ] 🔥 **Engagement du porteur** (Score /10)
  - *Score global >= 7.5/10 requis pour passage au Lab.*

### Colonne 3 : 🚀 3. SPRINT ACTUEL (IN PROGRESS)
- **Contenu** : Tâches en cours de développement par l'équipe du projet.
- **Exigence** : La carte Trello doit comporter l'étiquette du pôle (*IA, Fullstack, Embarqué, Cyber, Coordo*) et être liée à une branche ou PR GitHub via le Power-Up GitHub.

### Colonne 4 : 🧪 4. REVUE & PEER-LEARNING
- **Contenu** : Tâches codées nécessitant une revue par les pairs (*Code Review*) ou un test matériel/terrain.

### Colonne 5 : 🎯 5. DEPLOYE & IMPACT TERRAIN
- **Contenu** : Fonctionnalités déployées et solutions effectivement utilisées sur le terrain.
- **Métrique** : Chaque carte archivée ici doit inclure un court retour sur l'impact mesuré (utilisateurs touchés, problème résolu).

---

## 🏷️ Etiquettes Trello Standardisées (Labels)

- 🔴 **Pôle IA & Data** (`#EB5A46`)
- 🔵 **Pôle Fullstack Web/Mobile** (`#0079BF`)
- 🟢 **Pôle Électronique & IoT** (`#61BD4F`)
- 🟣 **Pôle Cyber & Réseaux** (`#C377E0`)
- 🟡 **Pôle Coordo & Design** (`#F2D600`)
- ⚡ **Priorité Haute / Critique** (`#FF9F1A`)

---

## ⚙️ Automatisations Butler Recommandées

1. **Auto-Assignment** : Lorsqu'un membre déplace une carte dans *Sprint Actuel*, lui attribuer automatiquement la carte comme membre responsable.
2. **Alertes Échéances** : Marquer la carte en rouge 48h avant la fin du sprint.
3. **Clôture PR GitHub** : Quand une Pull Request associée est mergée sur GitHub, déplacer automatiquement la carte Trello dans *Revue & Peer-Learning*.

# Architecture & Guide du Serveur Discord — Farafina Lab 💬

> Le serveur **Discord Farafina Lab** est le hub de communication instantanée, de réunions vocales et d'animation communautaire du collectif.

---

## 🏛️ Structure Recommandée des Catégories & Salons

### 📢 1. ACCUEIL & ANNONCES (Lecture Seule)
- **`#bienvenue-et-charte`** : Message d'accueil officiel, lien vers la charte GitHub et étapes pour s'orienter.
- **`#annonces-officielles`** : Annonces majeures, réunions d'alignement, lancements de projets.
- **`#liens-et-outils`** : Accès rapide aux repos GitHub, tableaux Trello et web app d'onboarding.

---

### 🌐 2. LA COMMUNAUTÉ (Espace Ouvert)
- **`#general-tchat`** : Échanges libres, discussions d'actualité technologique et sociétale.
- **`#presentation-membres`** : Salons où chaque nouveau membre partage sa fiche d'onboarding, ses spécialités et ses motivations.
- **`#propositions-idees`** : Partage d'idées de projets avant évaluation sur GitHub.
- **`#peer-learning`** : Entraide, questions/réponses techniques, partage de cours et ressources.

---

### 🧠 3. PÔLES DE COMPÉTENCES (Forums & Canaux Dédiés)
- **`#ia-data-science`** : Machine Learning, NLP, jeux de données locaux, modèles open-source.
- **`#dev-fullstack`** : Web, Mobile (React Native, Flutter, Kotlin), Backend (FastAPI, Node.js), API.
- **`#electronique-iot`** : Systèmes embarqués, Arduino, ESP32, capteurs, hardware open-source.
- **`#telecom-cyber-reseaux`** : Infrastructures, sécurité opérationnelle, télécommunications & réseaux.
- **`#design-comm-coordo`** : Design UI/UX, gestion agile, communication externe & impact.

---

### 🚀 4. LE LAB (Accès Restreint Noyau Dur)
- **`#lab-general`** : Coordination des projets à haut impact réservée aux membres du Lab.
- **`#sprints-et-livraisons`** : Suivi des livrables et de l'impact terrain.
- **`#comite-evaluation`** : Discussion et notation des projets soumis selon la grille des 4 critères.

---

### 🤖 5. FLUX AUTOMATISÉS (Bots & Webhooks)
- **`#git-activity`** : Flux automatique des commits, PRs et releases depuis GitHub.
- **`#trello-updates`** : Notifications des mouvements de cartes sur Trello.

---

### 🎙️ 6. SALONS VOCAUX (Réunions & Peer-Learning)
- 🔊 **`[Vocal] Tour de Table`** : Réunions d'alignement hebdomadaires / bimensuelles.
- 🔊 **`[Vocal] Peer-Learning & Coding`** : Sessions de pair programming en direct.
- 🔊 **`[Vocal] Salle du Lab`** : Réunions de travail du noyau restreint.

---

## 🎭 Configuration des Rôles Discord

| Rôle | Couleur | Description |
| :--- | :--- | :--- |
| **👑 Porteur de la Vision / Lead** | Or (`#E5A93C`) | Fondateurs et coordinateurs globaux du collectif. |
| **🚀 Membre du Lab** | Émeraude (`#10B981`) | Membres intégrés au noyau restreint au mérite. |
| **🌐 Membre Communauté** | Bleu (`#3B82F6`) | Rôle par défaut attribué à chaque nouvel arrivant. |
| **🤖 Bot Intégration** | Gris (`#9CA3AF`) | Bots Webhooks GitHub & Trello. |

---

## 🤖 Message d'Accueil Automatique (Template pour `#bienvenue-et-charte`)

```markdown
Welcome à **Farafina Lab** ! 🌍

Farafina, en bambara, signifie « chez les noirs ». Nous sommes un collectif afrofuturiste axé sur l'innovation locale et l'impact réel sur le terrain.

📌 **Pour bien commencer :**
1. Lisez notre [Charte & Vision Stratégique](https://github.com/FarafinaLabs/.github/blob/main/CHARTE_ET_VISION.md).
2. Présentez-vous dans <#presentation-membres> !
3. Testez notre Web App d'onboarding : https://github.com/FarafinaLabs/farafina-lab-onboarding

Refus de l'attentisme • Partage de connaissance • Impact local ! 🚀
```

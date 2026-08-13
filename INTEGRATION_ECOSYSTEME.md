# Guide d'Intégration & d'Automatisation de l'Écosystème Farafina Lab 🔗

> **Triade d'Outils** : **Discord** (Communication & Alertes) + **Trello** (Gestion Kanban & Sprints) + **GitHub** (Code & Versionnement).

Ce guide détaille pas à pas l'architecture et la configuration des automatisations pour connecter de manière fluide et transparente nos 3 outils de travail.

---

## 📐 Architecture Globale du Flux de Travail

```
                        ┌─────────────────────────┐
                        │   🌐 COMMUNAUNTE & LAB  │
                        └────────────┬────────────┘
                                     │
           ┌─────────────────────────┼─────────────────────────┐
           ▼                         ▼                         ▼
┌─────────────────────┐   ┌─────────────────────┐   ┌─────────────────────┐
│ 💬 DISCORD          │   │ 📋 TRELLO           │   │ 🐙 GITHUB           │
│ - Chat & Vocaux     │   │ - Sprints Kanban    │   │ - Code & Repos      │
│ - Annonces          │   │ - Tâches & Badges   │   │ - Issues (4 crit.)  │
│ - Notification Bot  │   │ - Power-Up GitHub   │   │ - Actions & Webhooks│
└──────────▲──────────┘   └──────────▲──────────┘   └──────────▲──────────┘
           │                         │                         │
           └────── Webhooks Discord ─┴───── Power-Up GitHub ───┘
```

---

## 1. Integration 1 : GitHub ➔ Discord (Notifications Automatiques)

Permet de recevoir automatiquement sur Discord les événements importants de l'organisation GitHub (nouveaux repos, commits sur `main`, Pull Requests, création d'Issues).

### Étape 1 : Créer un Webhook sur Discord
1. Sur votre serveur **Discord Farafina Lab**, allez dans **Paramètres du serveur** > **Intégrations** > **Webhooks**.
2. Cliquez sur **Nouveau Webhook**.
3. Nommez-le **`Farafina GitHub Bot`** et attribuez-lui le canal **`#git-activity`** (ou `#annonces-projets`).
4. Cliquez sur **Copier l'URL du Webhook**.

### Étape 2 : Configurer le Webhook sur l'Organisation GitHub
1. Allez sur GitHub : **`https://github.com/organizations/FarafinaLabs/settings/hooks`** (Paramètres d'Organisation > Webhooks).
2. Cliquez sur **Add webhook**.
3. Dans **Payload URL**, collez l'URL du webhook Discord et ajoutez **`/github`** à la fin !
   > ⚠️ **Important** : L'URL doit se terminer par `/github` (ex: `https://discord.com/api/webhooks/123456/abcdef/github`).
4. **Content type** : Sélectionnez `application/json`.
5. **Which events would you like to trigger this webhook?** :
   - Sélectionnez *Send me everything* (ou choisissez : *Issues, Pull Requests, Pushes, Repositories*).
6. Cliquez sur **Add webhook**. ✅

---

## 2. Intégration 2 : GitHub ↔️ Trello (Power-Up GitHub)

Permet d'associer directement les commits, les branches et les Pull Requests GitHub aux cartes Trello pour un suivi Kanban parfait.

### Étape 1 : Activer le Power-Up GitHub sur Trello
1. Sur votre tableau Trello de projet, cliquez sur **Power-ups** (en haut à droite) > **Ajouter des Power-ups**.
2. Recherchez **GitHub** (par Trello) et cliquez sur **Ajouter**.
3. Cliquez sur **Paramètres** du Power-Up > **Autoriser votre compte GitHub**.

### Étape 2 : Lier une carte Trello à une Pull Request ou Branche
- Sur n'importe quelle carte Trello, un bouton **GitHub** apparaît dans la section *Ajouter*.
- Vous pouvez attacher :
  - Une **Issue GitHub**
  - Une **Pull Request**
  - Une **Branche de code**
  - Un **Commit spécifique**
- Le statut de la PR (Ouverte, Mergée, Fermée) s'affichera directement sur la carte Trello en temps réel !

---

## 3. Intégration 3 : Trello ➔ Discord (Activités des Tableaux)

Permet d'être notifié sur Discord quand une carte Trello est déplacée en *"Terminé / Déployé"* ou quand une tâche importante est créée.

### Étape 1 : Créer un Webhook Discord dédié à Trello
1. Sur Discord, créez un canal **`#trello-sprints`**.
2. Créez un webhook Discord nommé **`Trello Bot`** sur ce canal et copiez son URL.

### Étape 2 : Connecter Trello via l'intégration officielle ou Webhook
1. Sur Trello, installez le Power-Up **Discord** ou utilisez Zapier / Make.
2. Configurez les alertes :
   - Lorsqu'un projet passe la grille d'évaluation et entre en sprint.
   - Lorsqu'une tâche est marquée *« Prête pour revue »* ou *« Validée sur le terrain »*.

---

## 4. Automatisation via GitHub Actions (Notification Custom)

Le fichier de workflow `.github/workflows/discord_notifier.yml` inclus dans ce dépôt permet d'envoyer un message stylisé enrichi sur Discord chaque fois qu'un code est pushé ou qu'une release est publiée.

### Configuration du Secret sur GitHub :
1. Allez sur **`https://github.com/organizations/FarafinaLabs/settings/secrets/actions`**.
2. Ajoutez un secret nommé **`DISCORD_WEBHOOK`** avec l'URL de votre webhook Discord.

---
*Farafina Lab — L'alliance de la rigueur technique et de la collaboration agile.*

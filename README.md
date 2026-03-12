# QuickPoll

Application web de sondages rapides. Créez un sondage, partagez le lien, collectez les votes et visualisez les résultats en temps réel.

---

## Table des matières

- [Aperçu](#aperçu)
- [Stack technique](#stack-technique)
- [Prérequis](#prérequis)
- [Installation](#installation)
- [Lancer le projet](#lancer-le-projet)
- [Structure du projet](#structure-du-projet)
- [Fonctionnalités](#fonctionnalités)
- [Contribuer](#contribuer)

---

## Aperçu

QuickPoll permet à n'importe quel utilisateur de :

- créer un sondage en quelques secondes
- partager un lien public de vote
- consulter les résultats en temps réel avec un graphique

Objectif : **créer et partager un sondage en moins de 30 secondes.**

---

## Stack technique

| Partie | Technologie |
|---|---|
| Frontend | React |
| Backend | Node.js |
| Base de données | MongoDB |
| Graphiques | Chart.js |

---

## Prérequis

- Node.js >= 18
- npm >= 9
- MongoDB (local ou Atlas)

---

## Installation

```bash
# Cloner le dépôt
git clone https://github.com/votre-org/quickpoll.git
cd quickpoll

# Installer les dépendances frontend
cd client
npm install

# Installer les dépendances backend
cd ../server
npm install
```

Copier le fichier d'environnement et renseigner les variables :

```bash
cp .env.example .env
```

Variables attendues :

```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/quickpoll
JWT_SECRET=your_secret_key
```

---

## Lancer le projet

**Backend**

```bash
cd server
npm run dev
```

**Frontend**

```bash
cd client
npm start
```

L'application est accessible sur `http://localhost:3000`.

---

## Structure du projet

```
quickpoll/
├── client/          # Application React
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── App.jsx
│   └── package.json
├── server/          # API Node.js
│   ├── routes/
│   ├── models/
│   ├── controllers/
│   └── index.js
└── README.md
```

---

## Fonctionnalités

- Inscription et connexion utilisateur
- Création, modification et suppression de sondages
- Ajout d'options de réponse
- Vote avec protection contre le double vote
- Affichage des résultats en pourcentage et graphique
- Génération d'un lien public par sondage

---

## Contribuer

Les contributions se font via des branches dédiées. Aucun commit direct sur `main`.

```bash
git checkout -b feature/nom-de-la-feature
```

Ouvrir une Pull Request vers `main` une fois la feature terminée et testée.

**Definition of Done** — une feature est mergeable si :

- le code fonctionne
- les tests passent
- l'interface est utilisable
- la feature est démontrable lors de la Sprint Review

---

## Organisation

Ce projet suit la méthodologie **Scrum** sur 3 sprints d'une semaine.

| Sprint | Objectif |
|---|---|
| Sprint 1 | Fondations — auth, création de sondage |
| Sprint 2 | Système de vote |
| Sprint 3 | Résultats, graphiques, partage et UI finale |

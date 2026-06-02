

```markdown
# OmniDoc  - Plateforme de Dossier Médical Numérique Centralisé

OmniDoc est un écosystème numérique complet et sécurisé conçu pour centraliser et fluidifier le parcours de santé des patients. Grâce à une architecture interconnectée, la plateforme permet un accès instantané et sécurisé à l'historique médical en consultation ou en situation d'urgence via une identification par QR Code.

##  L'Équipe de Développement
* **Michel Yovo** : Architecture Monorepo, API REST & Base de données (Node.js, Express, PostgreSQL)
* **Sophie** : Interface Web & Tableau de bord des Médecins (React.js, Tailwind CSS)
* **Judes** : Application Mobile du Patient & Scanner QR Code (React Native, Expo)

---

##  Architecture du Projet (Monorepo)

Le projet est structuré sous forme de Monorepo pour centraliser le code et faciliter la synchronisation de l'équipe :

```text
OmniDoc/
├── omnidoc-backend/     # API REST centrale (Node.js, Express, PostgreSQL)
├── omnidoc-web/         # Application Web pour les hôpitaux et médecins (React.js, Vite)
└── omnidoc-mobile/      # Application mobile pour les patients (React Native, Expo)

```

---

## Installation et Lancement du Projet

###  Prérequis

* [Node.js](https://nodejs.org/) (Version 18 ou supérieure recommandée)
* Un serveur [PostgreSQL](https://www.postgresql.org/) actif.

### 1. Configuration du Serveur Central (Backend) 

Le serveur gère la logique métier, la sécurité par jetons JWT, le hachage des mots de passe et la persistance des données.

```bash
cd omnidoc-backend
npm install
npm run dev

```

*Note : Pensez à créer un fichier `.env` dans ce dossier pour y configurer vos variables d'environnement (accès PostgreSQL, port de l'API, clé secrète JWT).*

### 2. Configuration de l'Interface Web (Frontend) 

Le portail destiné aux professionnels de santé pour l'authentification des cliniques et la mise à jour des dossiers des patients.

```bash
cd omnidoc-web
npm install
npm run dev

```

### 3. Configuration de l'Application Mobile (Mobile) 

L'application smartphone qui permet au patient de générer son QR Code d'identification unique, de consulter son carnet de santé et d'enregistrer des données médicales en cache local.

```bash
cd omnidoc-mobile
npm install
npx expo start

```

---

## Stack Technique

* **Backend :** Node.js, Express.js, PostgreSQL (driver `pg`), JWT (JsonWebToken), Bcryptjs, Cors.
* **Web :** React.js (Vite), Tailwind CSS, Axios, React Router Dom, Lucide Icons.
* **Mobile :** React Native (Expo SDK), React Navigation, Axios, Expo Camera, Expo SQLite.
* **Versionnage :** Git & GitHub.

```

---

### Commandes pour l'envoyer sur GitHub

Pour éviter l'erreur de rejet (`[rejected] main -> main`) et s'assurer que Windows ne bloque pas, suis précisément ces étapes dans ton terminal (assure-toi d'être bien connecté à Internet) :

```powershell
# 1. Reviens bien à la racine de ton projet
cd C:\PROJET\OmniDoc

# 2. Ajoute le nouveau fichier README.md à Git
git add README.md

# 3. Crée le commit de sauvegarde
git commit -m "Docs: Ajout du fichier README.md principal"

# 4. Fusionne proprement les fichiers de GitHub avec ton local (sans ouvrir Vim)
git pull origin main --no-edit

# 5. Envoie enfin le tout sur ton dépôt GitHub
git push -u origin main

```

Une fois le `git push` terminé, rafraîchis ta page GitHub sur ton navigateur : ton projet aura une présentation propre et professionnelle avec la liste de ton équipe !
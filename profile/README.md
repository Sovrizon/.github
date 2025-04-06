# 📸 Secugram — Application Web

Secugram est une application web simplifiée de partage d'images.  
Elle permet à des utilisateurs inscrits de publier des images avec descriptions.  
Les images sont **chiffrées côté serveur** et protégées via un système de clés sécurisé, en lien avec un tiers de confiance.

---

## 🧱 Technologies utilisées

- **Frontend** : React (Vite)
- **Backend** : FastAPI
- **Base de données** : MongoDB
- **Chiffrement** : géré côté serveur (FastAPI) avec vérification via un tiers de confiance

---

## ✨ Fonctionnalités principales

- 🧾 Inscription / Connexion
- 🖼️ Publication d'images avec description
- 🔐 Chiffrement côté serveur
- 🔎 Visualisation conditionnelle des images via une extension Chrome
- 🔗 API sécurisée interconnectée avec le serveur de confiance

---

## 🚀 Installation locale

### 1. Cloner le dépôt

`
git clone https://github.com/ton-user/secugram.git
cd secugram
`

### 2. Lancer le backend

cd backend
pip install -r requirements.txt
uvicorn main:app --reload --port 8000

⚠️ Assurez-vous que MongoDB est accessible (en local ou via un URI distant).

### 3. Lancer le frontend

cd frontend
npm install
npm run dev

Par défaut disponible sur http://localhost:5173

## 🧩 Dépendance externe

Cette application interagit avec un **tiers de confiance** pour :
* Générer les clés de chiffrement
* Gérer les tokens d'accès
* Valider les droits de lecture

Voir le dépôt tiers-de-confiance

## 📂 Structure du dépôt

secugram/
├── backend/         # FastAPI (routes, auth, BDD, chiffrement)
├── frontend/        # React (UI, login, publication, affichage)
└── README.md

## 📄 Licence

Projet développé par Loqmen ANANI dans le cadre d'un projet étudiant. Licence : MIT

# 🚀 Projet Backend : Système de File d'Attente Distribuée avec Node.js & Redis

👋 Salut à tous , nous allons travailler sur un projet avancé qui vous permettra d'approfondir vos compétences backend et de découvrir des concepts **cruciaux** dans le développement de systèmes **scalables et performants**.

---

## 🎯 Objectif du projet  
Vous allez implémenter un **système de file d'attente distribuée** (**Distributed Task Queue System**) permettant de gérer et d'exécuter des tâches de manière **asynchrone**.

### ✅ Concepts abordés :  
- **Gestion des files d'attente** avec Redis & BullMQ  
- **Traitement asynchrone** et exécution parallèle  
- **Communication entre microservices**  
- **Utilisation de Docker pour le déploiement**  
- **Stockage des résultats dans PostgreSQL ou MongoDB**  
- **Surveillance et gestion des tâches** via une interface Web  

---

## 🛠️ Stack Technologique  
📌 **Backend** : Node.js (Express ou NestJS)  
📌 **Queue Management** : Redis + BullMQ  
📌 **Base de données** : PostgreSQL ou MongoDB  
📌 **Outils DevOps** : Docker & Docker Compose  
📌 **Monitoring** : Bull Board  

---

## 🔹 Structure du Projet  

### 🟢 1️⃣ API Service (Producteur)  
➡ Reçoit des requêtes et ajoute des tâches à la file d’attente.  

### 🟠 2️⃣ Worker Service (Consommateur)  
➡ Récupère les tâches dans la file et les exécute en arrière-plan.  

### 🟣 3️⃣ Base de données  
➡ Stocke les résultats et l’historique des tâches exécutées.  

---

## 🚀 Fonctionnalités à implémenter  
🔹 API REST pour soumettre des tâches (**/submit-task**)  
🔹 Exécution des tâches de manière asynchrone  
🔹 Gestion des **priorités** dans la file d'attente  
🔹 **Retry automatique** des tâches en cas d’échec  
🔹 Dashboard de monitoring pour suivre les tâches  

---

## 📌 Étapes de Développement  

### 1️⃣ Initialisation du projet  
- Créer un projet Node.js avec **Express**  
- Installer **BullMQ**, Redis, et la base de données  

### 2️⃣ Implémentation du Producteur (API Service)  
- Définir une route **POST /submit-task** qui ajoute une tâche dans Redis  

### 3️⃣ Implémentation du Consommateur (Worker Service)  
- Écouter la file d’attente et exécuter les tâches selon leur type  

### 4️⃣ Stockage des résultats  
- Enregistrer l’état des tâches terminées dans PostgreSQL/MongoDB  

### 5️⃣ Monitoring & Optimisation  
- Ajouter **Bull Board** pour suivre l’état des tâches  
- Gérer les **échecs et les retries automatiques**  

### 6️⃣ Dockerisation du projet  
- Conteneuriser Redis, PostgreSQL, l’API et le Worker avec **Docker Compose**  

---

## 📅 Deadline & Critères d’évaluation  
📆 **Date limite** : _[Fixe une date]_  
🔍 **Critères** :  
✅ Code bien structuré et clair  
✅ Bonne gestion de la file d’attente et du stockage des résultats  
✅ Implémentation de Docker et Bull Board (**bonus**)  
✅ Documentation du projet (**README.md**)  

---

## 📢 Ressources & Documentation  
📖 [BullMQ](https://docs.bullmq.io/)  
📖 [Redis](https://redis.io/docs/)  
📖 [Docker Compose](https://docs.docker.com/compose/)  

🎯 **À vous de jouer !** 🚀 N’hésitez pas à poser vos questions sur le serveur Discord. 💬  

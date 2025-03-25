# 📦 Système d’Upload et de Traitement de Fichiers à Grande Échelle (Node.js + Redis + S3)

## 🎯 Objectif du Projet  
Concevoir et développer un système capable de gérer des **uploads de fichiers volumineux**, de les stocker efficacement, et de traiter leurs métadonnées **de manière asynchrone** via une **architecture orientée événements**.

---

## ✅ Concepts Clés abordés  
- Streaming de fichiers pour optimiser la mémoire  
- Traitement asynchrone avec workers en arrière-plan  
- Architecture orientée événements (BullMQ / Redis / NATS)  
- Stockage de fichiers (S3 ou MinIO en local)  
- Authentification & contrôle d’accès par rôles  
- Limitation de débit (rate limiting)  
- Suivi du statut des fichiers et journaux d’audit  

---

## 🛠️ Stack Technique  
- **Backend** : Node.js (Express ou NestJS)  
- **File d’attente** : Redis + BullMQ (ou NATS)  
- **Stockage** : AWS S3 ou MinIO (local)  
- **Base de données** : PostgreSQL ou MongoDB  
- **Auth** : JWT + RBAC (Role-Based Access Control)  
- **Monitoring** : Bull Board ou Dashboard custom  
- **Déploiement** : Docker + Docker Compose  

---

## 🔹 Structure du Projet  

### 🟢 1. Service d’Upload (API)
- Accepte les fichiers volumineux (via streaming)  
- Stocke les fichiers (MinIO/S3 ou local)  
- Envoie un job dans la file pour traitement  

### 🟠 2. Worker (Service de traitement)
- Écoute la file de traitement  
- Effectue :
  - Extraction de métadonnées (EXIF, MIME, etc.)
  - Génération de miniatures
  - Scan antivirus (simulé)  
- Met à jour le statut du fichier en base  

### 🟣 3. Base de Données
- Enregistre les fichiers, utilisateurs, et statuts  
- Stocke les logs d’audit et métadonnées  

---

## 🚀 Fonctionnalités à Implémenter  

- [x] Route `POST /upload` pour upload de fichiers (stream)  
- [x] Stockage des fichiers (MinIO ou local)  
- [x] File de traitement avec BullMQ  
- [x] Service worker : métadonnées + miniatures  
- [x] Statuts : `en_attente`, `en_traitement`, `terminé`, `échec`  
- [x] Re-tentatives automatiques en cas d’échec  
- [x] Authentification par JWT  
- [x] API REST pour :
  - Récupérer les métadonnées
  - Télécharger les fichiers
  - Vérifier le statut de traitement  
- [x] Dashboard de suivi avec Bull Board  

---

## 🌐 Fonctionnalités Bonus

- [ ] **Limitation de débit** (ex: 5 uploads/min/utilisateur)  
- [ ] **Scan antivirus simulé**  
- [ ] **Webhook** pour notification de fin de traitement  
- [ ] **Support multi-utilisateurs**  
- [ ] **Utilisation de NATS** ou **Kafka** pour l’event sourcing  

---

## 🐳 Dockerisation

Fichiers/services inclus dans `docker-compose` :

- Redis  
- MinIO  
- Base de données (PostgreSQL ou MongoDB)  
- Service API d’upload  
- Worker (service de traitement)  
- Dashboard (Bull Board)  



## 📚 Ressources

- [Documentation BullMQ](https://docs.bullmq.io/)  
- [Documentation MinIO](https://min.io/docs/)  
- [Multer (gestion des fichiers)](https://github.com/expressjs/multer)  
- [AWS S3 SDK](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/)  
- [Docker Compose](https://docs.docker.com/compose/)

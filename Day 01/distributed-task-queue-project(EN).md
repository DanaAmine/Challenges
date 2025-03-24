# 🚀 Backend Project: Distributed Task Queue System with Node.js & Redis

👋 Hello everyone! This Day, we will work on an advanced project that will help you deepen your **backend skills** and understand crucial concepts in building **scalable and high-performance systems**.

---

## 🎯 Project Goal  
You will implement a **Distributed Task Queue System**, allowing tasks to be managed and executed **asynchronously**.

### ✅ Key Concepts:  
- **Queue management** with Redis & BullMQ  
- **Asynchronous processing** and parallel execution  
- **Microservices communication**  
- **Deployment using Docker**  
- **Storing task results** in PostgreSQL or MongoDB  
- **Task monitoring and management** via a web dashboard  

---

## 🛠️ Tech Stack  
📌 **Backend**: Node.js (Express or NestJS)  
📌 **Queue Management**: Redis + BullMQ  
📌 **Database**: PostgreSQL or MongoDB  
📌 **DevOps Tools**: Docker & Docker Compose  
📌 **Monitoring**: Bull Board  

---

## 🔹 Project Structure  

### 🟢 1️⃣ API Service (Producer)  
➡ Receives requests and adds tasks to the queue.  

### 🟠 2️⃣ Worker Service (Consumer)  
➡ Fetches tasks from the queue and processes them in the background.  

### 🟣 3️⃣ Database  
➡ Stores task results and execution history.  

---

## 🚀 Features to Implement  
🔹 REST API to submit tasks (**/submit-task**)  
🔹 Asynchronous task execution  
🔹 **Priority-based** task queuing  
🔹 **Automatic retries** for failed tasks  
🔹 Monitoring dashboard to track task status  

---

## 📌 Development Steps  

### 1️⃣ Project Initialization  
- Set up a Node.js project with **Express**  
- Install **BullMQ**, Redis, and the database  

### 2️⃣ Implementing the Producer (API Service)  
- Define a **POST /submit-task** route that adds tasks to Redis  

### 3️⃣ Implementing the Consumer (Worker Service)  
- Listen to the queue and execute tasks based on their type  

### 4️⃣ Storing Task Results  
- Save task execution status in PostgreSQL/MongoDB  

### 5️⃣ Monitoring & Optimization  
- Add **Bull Board** for tracking task status  
- Handle **failures and automatic retries**  

### 6️⃣ Dockerizing the Project  
- Containerize Redis, PostgreSQL, the API, and the Worker with **Docker Compose**  

---

## 📅 Deadline & Evaluation Criteria  
📆 **Deadline**: 25 MAR 2025 
🔍 **Evaluation Criteria**:  
✅ Well-structured and clean code  
✅ Proper queue management and result storage  
✅ Implementation of Docker and Bull Board (**bonus**)  
✅ Project documentation (**README.md**)  

---

## 📢 Resources & Documentation  
📖 [BullMQ](https://docs.bullmq.io/)  
📖 [Redis](https://redis.io/docs/)  
📖 [Docker Compose](https://docs.docker.com/compose/)  

🎯 **Let's go!** 🚀 Feel free to ask questions on the Discord server. 💬  

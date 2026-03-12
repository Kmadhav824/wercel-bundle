# 🚀 Wercel — Vercel-like Deployment Platform

A modular cloud deployment platform that automatically builds, deploys, and hosts web applications — inspired by Vercel.

This project demonstrates a **multi-service deployment architecture** with independent services for build processing, deployment management, and request handling. The system is designed using backend and system design principles such as **separation of concerns, fault isolation, and scalability**.

---

## 📌 Overview

Wercel allows users to deploy frontend applications by:

1. Cloning a Git repository
2. Uploading project files to object storage (Cloudflare R2)
3. Building the project in an isolated environment
4. Deploying production artifacts
5. Serving the deployed application

The platform is implemented using a **modular architecture** where each service performs a specific responsibility.

---

## 🏗 System Architecture

The system consists of **Three independent services**:

### Architecture Flow

1. User submits Git repository
2. Wercel clones repo locally
4. Build service compiles project
5. Deployment service publishes build output
6. Request handler serves application to users

---

## ⚙️ Services

### 💻 1. Frontend Interface (Deployment Dashboard)
**Repository:** [wercel-frontend](https://github.com/Kmadhav824/wercel-frontend.git)

The platform provides a simple web interface where users can deploy applications by submitting a Git repository URL.

#### Features

- Input box for users to submit Git repository URLs
- Initiates deployment workflow through backend API
- Displays deployment status and progress
- Communicates with Wercel control plane via REST APIs

### 🧠 2. Wercel-fetch-build-deploy
**Repository:** [Private]

- Handles project creation and deployment requests
- Clones user Git repositories locally
- Manages build job orchestration
- Builds the project on VM or locally
- Tracks deployment state and workflow
- Push the built artifacts to CloudFlare Object store

**Key Concepts**
- Backend service architecture
- Job orchestration
- Service communication
- API design

---

### 🌐 3. wercel-request-handler (Hosting / Request Router)
**Repository:** [Private]

- Handles incoming user traffic
- Routes requests to deployed applications
- Serves static files
- Optimized for performance and low latency

**Key Concepts**
- Request routing
- Production serving
- High performance systems

---

## 🧩 Tech Stack

- **Backend:** Node.js
- **Frontend:** React.js
- **Containerization:** Docker
- **Storage:** Cloudflare R2
- **Communication:** REST APIs
- **Version Control:** Git

---

## ⭐ System Design Highlights

- Modular multi-service architecture
- Separation of concerns
- Independent service deployment
- Scalable build pipeline
- Fault isolation between services
- Automated deployment workflow
- Object storage based artifact management

---

## 🎯 Learning Goals

This project was built to understand:

- Cloud deployment systems
- CI/CD pipeline design
- Backend system architecture
- Microservice-style design
- Scalable infrastructure principles
- Production deployment workflows
- Message queue for job scheduling
- Distributed build workers
- Load balancing
- Custom domain support
- Deployment rollback system
- Monitoring and logging
- Authentication system
---

## 📈 Future Improvements
- Handling Enormous traffic and Parallely jobs
---

## 👨‍💻 Author

**Madhav Kumar**  
GitHub: https://github.com/Kmadhav824

---

## ⭐ If you found this project useful, consider giving it a star!


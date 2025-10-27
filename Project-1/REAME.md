# 🌟 Kubernetes Two-Tier Project: Flask + MySQL 🚀

![Kubernetes](https://img.shields.io/badge/Kubernetes-blue?logo=kubernetes\&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-blue?logo=docker\&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-lightgrey?logo=flask\&logoColor=black)
![MySQL](https://img.shields.io/badge/MySQL-blue?logo=mysql\&logoColor=white)

This repository showcases a **fully containerized two-tier application** deployed on **Kubernetes** using **Flask** for the frontend and **MySQL** for the backend.
The project demonstrates **Deployments, Services, and Persistent Volumes** with hands-on **DevOps practices**.

---

## 🌐 Project Overview

* **Frontend:** Flask app running in a Kubernetes pod
* **Backend:** MySQL database with persistent storage
* **Kubernetes Features Used:**

  * **Deployment:** Auto-restart, scaling, and version control
  * **Service (NodePort):** Internal communication + external access
  * **PersistentVolume + PersistentVolumeClaim:** MySQL data persists across restarts
  * **Environment Variables & Config:** Simplifies credentials and app configuration

---

## ⚡ Benefits in DevOps

* ✅ Automates deployment & scaling
* ✅ Ensures **resilience & self-healing**
* ✅ Provides **data persistence**
* ✅ Supports **CI/CD pipelines**

---

## 🛠 Installation & Setup

### Prerequisites

* [Minikube](https://minikube.sigs.k8s.io/docs/start/) or Kubernetes cluster
* Docker
* kubectl

### Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/farhancode9988/Kubernetes-journey.git

   ```
2. Start Minikube:

   ```bash
   minikube start
   ```
3. Apply PersistentVolume & PVC:

   ```bash
   kubectl apply -f pv-pvc.yml
   ```
4. Deploy MySQL & Flask app:

   ```bash
   kubectl apply -f mysql-deployment.yml
   kubectl apply -f two-tier-deployment.yml
   ```
5. Expose Flask app via NodePort:

   ```bash
   kubectl apply -f two-tier-svc.yml
   ```
6. Access Flask app:

   ```bash
   minikube service two-tier-app-svc --url
   ```

---

## ⚠ Challenges Faced

* ❌ Pods failing due to **missing PVC claims** → Fixed PV-PVC binding
* ❌ Flask **couldn’t connect to MySQL** → Added Kubernetes Service & DNS
* ❌ **ImagePullBackOff** errors → Loaded local Docker image into Minikube
* ❌ Missing **database/tables** → Created manually & optional init scripts

---

## 💡 Next Steps / Future Goals

* Deploy on **multi-node cluster using kubeadm** for production-ready setup
* Automate **database/table creation** with ConfigMap/init scripts
* Implement **CI/CD pipeline** for automated deployments

---

---

## 🔖 Technologies & Tools

| Frontend | Backend | Containerization | Orchestration | DevOps Tools      |
| -------- | ------- | ---------------- | ------------- | ----------------- |
| Flask    | MySQL   | Docker           | Kubernetes    | Minikube, kubectl |

---

## 🌐 Connect With Me

Connect on **LinkedIn**: [Farhan Ilyas](https://www.linkedin.com/in/farhan-ilyas/)
Follow for more **cloud-native & DevOps projects**! 🚀

---

![GitHub Repo Size](https://img.shields.io/github/repo-size/<username>/<repository>)  ![GitHub last commit](https://img.shields.io/github/last-commit/<username>/<repository>)  ![GitHub issues](https://img.shields.io/github/issues/<username>/<repository>)

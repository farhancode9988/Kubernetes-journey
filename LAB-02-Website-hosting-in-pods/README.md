# 🚀 Website Hosting on Kubernetes 🌐

## 🧠 Project Summary
I built a **simple static website**, turned it into a **Docker image**, pushed it to **Docker Hub**, and then **hosted it on Kubernetes (Minikube)** using deployment and service manifests.

---

## 🪜 Steps I Followed

### 🧩 Step 1: Created the Website
I started with a basic **HTML + CSS** website — just a simple static page to test hosting.

---

### 🐳 Step 2: Made a Dockerfile
I wrote a **Dockerfile** to host the website with **NGINX**.

```dockerfile
FROM nginx:latest
COPY . /usr/share/nginx/html
```

---

### ⚙️ Step 3: Built the Docker Image
```bash
docker build -t farhan9889/website-host-kubernetes:latest .
```

---

### ☁️ Step 4: Pushed It to Docker Hub
```bash
docker push farhan9889/website-host-kubernetes:latest
```
Now my image lives on Docker Hub 🌍

---

### ☸️ Step 5: Created Kubernetes Deployment
I made a **deployment YAML file** (`deployment.yaml`) that uses the Docker image to create pods in the cluster.

---

### 🌐 Step 6: Exposed It with a Service
I used a **NodePort service** to make the website reachable on my system:
```bash
kubectl apply -f deployment.yaml
```
Then accessed it using:
```bash
minikube service static-site-service
```

---

## 🧰 Tools & Tech Used
| Tool | Purpose |
|------|----------|
| 🐳 Docker | Containerized the website |
| ☸️ Kubernetes (Minikube) | Managed & deployed the container |
| 💻 NGINX | Served the static web content |
| 🧱 YAML | Defined deployment & service |

---

## 🏁 Result
✅ Website hosted successfully inside a Kubernetes Pod  
✅ Accessible locally via Minikube Tunnel  
✅ Docker image stored on Docker Hub  

---

### 👨‍💻 Author
**Farhan Ilyas**  
💡 DevOps Enthusiast | Docker & Kubernetes Learner

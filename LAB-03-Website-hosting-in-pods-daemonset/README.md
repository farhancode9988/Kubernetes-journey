# 🚀 Kubernetes DaemonSet Lab — Static Website 🌐

### 📘 Overview
Deployed a **static website** on every node using a **DaemonSet** — ensuring one Pod runs per node!  
Perfect for **monitoring**, **logging**, or **lightweight web hosting**.

---

### 🧩 What’s Inside
- ⚙️ **DaemonSet** → 1 Pod per node  
- 🌍 **NodePort Service** → External access  
- 🐳 **Container Image** → `farhan9889/website-host-kubernetes:latest`

---

### 💡 DaemonSet vs Deployment

| Type | Purpose | Use Case |
|------|----------|-----------|
| **Deployment** | Scalable, multiple replicas | Web apps, APIs |
| **DaemonSet** | One Pod per node | Monitoring agents, log collectors |

---

### 🧠 Use Case
✅ Run a **static site** on all nodes  
✅ Ensures **high availability** & **local access**  
✅ Great for learning **cluster-wide Pod control**

---

### ⚙️ Commands Used
```bash
# Deploy DaemonSet & Service
kubectl apply -f daemonset.yaml

# Check Pods
kubectl get pods -o wide

# View DaemonSet
kubectl get daemonset

# Access service
kubectl get svc
🧾 YAML Files
DaemonSet

yaml
Copy code
apiVersion: apps/v1
kind: DaemonSet
metadata:
  name: web-daemonset
spec:
  selector:
    matchLabels:
      app: static-site
  template:
    metadata:
      labels:
        app: static-site
    spec:
      containers:
        - name: web
          image: farhan9889/website-host-kubernetes:latest
          ports:
            - containerPort: 80
Service

yaml
Copy code
apiVersion: v1
kind: Service
metadata:
  name: static-site-service
spec:
  type: NodePort
  selector:
    app: static-site
  ports:
    - port: 80
      targetPort: 80
🌈 Tech Stack
Kubernetes ⚙️ | Docker 🐳 | Linux 🐧 | YAML 🧾

👤 Author
Farhan Ilyas — DevOps Enthusiast 🧠
Passionate about Cloud, Linux, & Containerization ☁️🐧

🔗 LinkedIn
#DevOps #Kubernetes #Docker #Cloud #LearningJourney

yaml
Copy code

---

Would you like me to make it **downloadable as a `.md` file** now 
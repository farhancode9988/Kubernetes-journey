<p align="center"> <img src="https://capsule-render.vercel.app/api?type=waving&color=0:326CE5,100:00A67E&height=200&section=header&text=☸️%20Kubernetes%20Learning%20Journey%20🚀&fontSize=35&fontColor=ffffff&animation=fadeIn&fontAlignY=38" /> </p> <h3 align="center"><i>Hands-on exploration of container orchestration, scaling, and automation in real-world DevOps.</i></h3>
🎯 Overview

This repository showcases my Kubernetes learning journey, where I built, containerized, and deployed real applications inside a cluster using Minikube.
Through each lab, I explored how Kubernetes handles auto-scaling, self-healing, and zero-downtime deployments — the core of modern DevOps automation. ⚙️

🧰 Tech Stack

Kubernetes • Docker • Minikube • NGINX • YAML • kubectl • Linux

🧭 Repository Structure
#	Project	Description
🌐 1	Website Hosting on Kubernetes	Hosted a static website on Kubernetes using Docker + NGINX.
🧩 2	Demo Pod Deployment	Created a basic Pod to understand Kubernetes resource behavior.
🌐 Website Hosting on Kubernetes

🎯 Goal: Host a simple static website inside a Kubernetes cluster using Docker and NGINX.

🧰 Tech Stack: Docker • NGINX • Kubernetes (Minikube)

⚙️ Key Steps:
1️⃣ Built and containerized a static HTML/CSS site
2️⃣ Created Docker image → pushed to Docker Hub

docker build -t farhan9889/website-host-kubernetes:latest .
docker push farhan9889/website-host-kubernetes:latest


3️⃣ Deployed using deployment.yaml & service.yaml

kubectl apply -f deployment.yaml
minikube service static-site-service


✅ Result:
Website successfully hosted inside Kubernetes Pod and accessed locally through Minikube Tunnel. 🌐

🧩 Demo Pod Deployment

🎯 Goal: Learn the fundamentals of Pods and resource allocation.

💡 Key Learnings:

Pod creation & lifecycle management

Viewing logs and pod status

Understanding YAML configurations

kubectl apply -f demo-pod.yaml
kubectl get pods
kubectl describe pod <pod-name>


✅ Result:
Hands-on understanding of Kubernetes objects, labels, and controllers.

💡 Skills Demonstrated

☸️ Container orchestration with Kubernetes

📦 Application deployment via YAML manifests

⚙️ Managing Pods, Deployments & Services

🌍 Load balancing and Service exposure

🩺 Auto-healing and scaling fundamentals

🐳 Docker image creation and registry management

📈 Key Kubernetes Concepts
Concept	Purpose
☸️ Pods	Smallest deployable unit in Kubernetes
📦 Deployments	Manage replicas and rollouts
🧱 Services	Enable stable network access
⚙️ ReplicaSets	Maintain desired pod count
🩺 Auto-Healing	Replace failed pods automatically
📈 Auto-Scaling	Scale pods based on demand
🔄 Rolling Updates	Deploy new versions with zero downtime
🧪 Tools Used
Tool	Purpose
🐳 Docker	Build and push images
☸️ Minikube	Local Kubernetes cluster
💻 NGINX	Static web server
🧱 YAML	Define Kubernetes resources
🧑‍💻 kubectl	Cluster management CLI
📂 Repository

🔗 GitHub: Kubernetes Journey Repo

👨‍💻 Author

Farhan Ilyas
💡 DevOps Enthusiast | Kubernetes & Docker Learner
📫 LinkedIn
 • GitHub

✨ From containers to orchestration — this journey reflects my growth in automation, deployment, and scalable systems design.

<p align="center"> <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00A67E,100:326CE5&height=120&section=footer"/> </p>

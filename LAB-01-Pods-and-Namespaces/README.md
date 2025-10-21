LAB-01: Pods & Namespaces — Your Kubernetes Launchpad! 🚀
📚 Backstory: Getting Organized
Okay, I'm done setting up Minikube (LAB-00), so it's time to deploy my first application! But before I just dump everything into the default namespace, I want to learn how to organize my resources.

This lab focuses on the two most basic building blocks:

Namespaces (NS): Like folders on a computer, they keep my resources separated. I'm creating a namespace for my fictional "Demo-namespace"

Pods: The smallest unit. I'm putting a simple Nginx web server Pod inside that new namespace.



# 1. Apply the manifest to create the Namespace and Pod
kubectl apply -f resources.yaml

# 2. Verify the Namespace exists
kubectl get namespaces

# 3. Check the Pod status (MUST specify the namespace with -n)
kubectl get pods -n Demo-namespace

# 4. View detailed information (Events, IP, etc.)
kubectl describe pod demo-pod -n Demo-namespace

# 5. Clean up the environment by deleting the Namespace
# This automatically deletes the Pod inside it.
kubectl delete namespace Demo-namespace
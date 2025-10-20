#!/bin/bash
# MINIKUBE SETUP COMMANDS - READY TO COPY/PASTE 🚀

# --- 1. Installation ---
# Download Minikube binary (for Linux/amd64 - adjust if needed)
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

# Install the binary
sudo install minikube-linux-amd64 /usr/local/bin/minikube

# Clean up the downloaded file
rm minikube-linux-amd64

# --- 2. Start the Cluster ---
# Start Minikube using the Docker driver
minikube start --driver=docker

# --- 3. Verification ---
# Check Minikube status
minikube status

# Check kubectl connection info
kubectl cluster-info

# --- 4. Optional: Kubernetes Dashboard ---
# Run the dashboard command (add '&' to run in the background)
minikube dashboard &

# --- 5. Management/Cleanup Commands (Run separately as needed) ---

# To stop the cluster and free resources
# minikube stop

# To permanently delete all cluster data
# minikube delete
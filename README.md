# 📈 Scaling Kubernetes Applications with Horizontal Pod Autoscaler (HPA)

This project demonstrates how to deploy a Horizontal Pod Autoscaler (HPA) in a local Kubernetes cluster using **Minikube**. The HPA dynamically scales the number of pods based on CPU usage.

---

## 🎯 Goal

Automatically scale a Kubernetes Deployment (`my-app`) between 2 and 10 pods when CPU utilization exceeds 50%.

---

## ⚙️ Prerequisites

- Minikube
- Docker
- kubectl

---

## 🚀 Steps to Run

### 1. Start Minikube with Docker driver

minikube start --driver=docker



2. Apply the HPA Configuration

kubectl apply -f hpa.yaml



3. Deploy Metrics Server

kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml




4. Monitor HPA Behavior

kubectl get hpa
kubectl top pods
kubectl top nodes




🛠️ Troubleshooting
❌ kubectl top Not Working?
Restart Minikube

Wait for Metrics Server pods to become ready

Check with: kubectl get pods -n kube-system

❌ Docker Permission Denied?
sudo usermod -aG docker $USER && newgrp docker



HPA scales the app between 2 and 10 replicas based on CPU load, monitored live using Metrics Server.


Ibne Sabid Saikat
Cloud Solution Architect | Microsoft Learn Student Ambassador
🔗 19+ Projects | AZ-104 | AZ-305 | DevSecOps | SOC Analyst | Researcher

   




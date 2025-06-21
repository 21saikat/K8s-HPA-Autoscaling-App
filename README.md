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

```bash
minikube start --driver=docker




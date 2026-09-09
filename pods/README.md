# Kubernetes Pods

This directory contains my hands-on Kubernetes Pod practice and YAML manifests.

The goal of these exercises is to understand how Pods are defined, configured, deployed, inspected, and deleted using Kubernetes and `kubectl`.

---

## 📚 What I Practiced

- Creating a Kubernetes Pod using YAML
- Understanding `apiVersion` and `kind`
- Defining Pod metadata
- Assigning labels to Pods
- Configuring containers
- Running Nginx containers
- Using different Nginx image versions
- Creating and managing Pods with `kubectl`
- Inspecting Pod details
- Deleting Pods
- Troubleshooting Kubernetes resources

---

## 📂 Files

### `nginx.yaml`

Creates an Nginx Pod with:

- Pod name: `nginx-2`
- Label: `env: production`
- Container name: `nginx`
- Container image: `nginx`

### `pod.yml`

Creates an Nginx Pod with:

- Pod name: `nginx`
- Labels:
  - `app: nginx`
  - `tier: frontend`
- Container name: `nginx`
- Nginx image version: `nginx:1.14.2`

---

## 🧪 Commands Practiced

Create a Pod:

```bash
kubectl apply -f nginx.yaml

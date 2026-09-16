# Kubernetes Pods

This folder contains Kubernetes Pod and Service YAML manifests created as part of my Kubernetes certification learning and hands-on practice.

The examples demonstrate how to create individual Pods and expose applications using Kubernetes Services.

---

## 📁 Files

### Pod Manifests

- `voting-app-pod.yaml` – Vote application Pod
- `worked-pod.yaml` – Worker Pod
- `redis-pod.yaml` – Redis Pod

### Service Manifests

- `vote-service.yaml` – Service for the Vote application
- `redis-service.yaml` – Service for Redis
- `db-service.yaml` – Service for the database
- `result-service.yaml` – Service for the Result application

---

## 🏗️ Application Architecture

The application follows this basic flow:

```text
             Vote Application
                    |
                    v
                  Redis
                    |
                    v
                  Worker
                    |
                    v
                PostgreSQL
                    |
                    v
             Result Application

# Kubernetes Deployments

This folder contains Kubernetes Deployment manifests created as part of my Kubernetes certification learning and hands-on practice.

The Deployment examples demonstrate how Kubernetes manages application Pods, replicas, labels, selectors, containers, and application components.

---

## 📁 Files

- `vote-deployment.yaml` – Vote application Deployment
- `redis-deployment.yaml` – Redis Deployment
- `worker-deployment.yaml` – Worker Deployment
- `db-deployment.yaml` – PostgreSQL database Deployment
- `result-deployment.yaml` – Result application Deployment

---

## 🏗️ Application Architecture

```text
                    Vote
                     |
                     v
                   Redis
                     |
                     v
                   Worker
                  /      \
                 v        v
              Redis      DB
                         |
                         v
                       Result

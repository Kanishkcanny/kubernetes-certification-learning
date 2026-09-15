# Kubernetes Deployment

This directory contains my hands-on Kubernetes Deployment practice.

The exercise demonstrates how to create a Deployment, define the desired number of Pod replicas, configure Pod labels, use selectors, and run an Nginx container.

---

## 📚 What I Practiced

- Creating a Kubernetes Deployment using YAML
- Understanding the `apps/v1` API version
- Understanding the `Deployment` resource
- Defining Deployment metadata
- Configuring labels
- Using `matchLabels` selectors
- Configuring Pod templates
- Running multiple Pod replicas
- Using an Nginx container image
- Understanding how Deployments manage Pods

---

## 📂 File

### `deployment.yaml`

Creates a Deployment with the following configuration:

| Configuration | Value |
|---|---|
| Resource | Deployment |
| Name | `myapp-deployment` |
| API Version | `apps/v1` |
| Replicas | `6` |
| Application | `myapp` |
| Tier | `frontend` |
| Container | `nginx` |
| Image | `nginx:1.12` |

---

## 📄 Deployment Manifest

```yaml
apiVersion: apps/v1
kind: Deployment

metadata:
  name: myapp-deployment
  labels:
    tier: frontend
    app: myapp

spec:
  selector:
    matchLabels:
      app: myapp

  replicas: 6

  template:
    metadata:
      name: nginx
      labels:
        app: myapp

    spec:
      containers:
        - name: nginx
          image: nginx:1.12

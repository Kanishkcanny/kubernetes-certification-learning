# Kubernetes Service

This directory contains my hands-on Kubernetes Service practice.

This exercise demonstrates how to expose an application running in Kubernetes using a `NodePort` Service and how a Service uses labels and selectors to route traffic to the appropriate Pods.

---

## 📚 What I Practiced

- Creating a Kubernetes Service using YAML
- Understanding the `Service` resource
- Using the `v1` API version
- Understanding `NodePort`
- Configuring Service ports
- Configuring `targetPort`
- Configuring a specific `nodePort`
- Using labels and selectors
- Connecting a Service to application Pods
- Understanding how Services provide network access to Pods

---

## 📂 File

### `service-definition.yaml`

Creates a NodePort Service with the following configuration:

| Configuration | Value |
|---|---|
| Resource | Service |
| Name | `myapp-service` |
| API Version | `v1` |
| Type | `NodePort` |
| Service Port | `80` |
| Target Port | `80` |
| Node Port | `30004` |
| Selector | `app: myapp` |

---

## 📄 Service Manifest

```yaml
apiVersion: v1
kind: Service

metadata:
  name: myapp-service

spec:
  type: NodePort

  ports:
    - port: 80
      targetPort: 80
      nodePort: 30004

  selector:
    app: myapp


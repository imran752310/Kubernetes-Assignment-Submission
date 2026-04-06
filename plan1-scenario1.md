
## Scenario 1: AI Native Task Manager

### Overview

This scenario represents a task management system designed using a microservices architecture. Each component runs independently inside a Kubernetes cluster, allowing better scalability and maintenance.

### Components

* UI Interface (Frontend)
* Backend APIs
* Todo Agent (background worker)
* Notification Service

### Deployments

Each component is deployed separately:

* UI Deployment (2 replicas for availability)
* Backend Deployment (3 replicas for handling requests)
* Todo Agent Deployment (single or scalable worker)
* Notification Service Deployment

### Services

* UI exposed using LoadBalancer or Ingress for external access
* Backend exposed internally using ClusterIP
* Notification service uses ClusterIP

### Resource Requests & Limits

```yaml
resources:
  requests:
    cpu: "250m"
    memory: "256Mi"
  limits:
    cpu: "500m"
    memory: "512Mi"
```

### ConfigMaps

Used for storing:

* API endpoints
* Environment variables

### Secrets

Used for sensitive data:

* Database credentials
* API tokens

### Namespaces

To organize workloads:

* frontend namespace
* backend namespace
* agents namespace

### RBAC

Access is controlled using roles:

* Backend has limited access
* Todo Agent can only access required APIs

### Communication Flow

* UI communicates with Backend APIs
* Backend communicates with Todo Agent
* Notification service sends updates to UI


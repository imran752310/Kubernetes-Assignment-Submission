
## Scenario 1: AI Native Task Manager

### Architecture

Microservices system deployed on Kubernetes:

* UI Interface
* Backend APIs
* Todo Agent
* Notification Service

### Deployments

* UI Deployment (2 replicas)
* Backend Deployment (3 replicas)
* Todo Agent Deployment (worker)
* Notification Deployment

### Services

* UI → LoadBalancer / Ingress
* Backend → ClusterIP
* Notification → ClusterIP

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

* API URLs
* Environment configs

### Secrets

* DB credentials
* API keys

### Namespaces

* frontend
* backend
* agents

### RBAC

* Backend: limited access
* Agent: API access only

### Communication

* UI → Backend
* Backend ↔ Agent
* Notification → UI


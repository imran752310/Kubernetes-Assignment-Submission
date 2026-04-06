
# 📁 FILE 2: plan2-scenario2.md

## Scenario 2: AI Employee (OpenClaw)

### Overview

This scenario focuses on deploying a secure AI employee inside Kubernetes with strong emphasis on access control and secret management.

### Deployments

* AI Employee Deployment
* Database deployed as StatefulSet for persistent storage

### Services

* Internal communication handled using ClusterIP services

### Resource Configuration

```yaml
resources:
  requests:
    cpu: "200m"
    memory: "256Mi"
  limits:
    cpu: "400m"
    memory: "512Mi"
```

### ConfigMaps

Used for non-sensitive configuration values

### Secrets

Used for:

* API keys
* Authentication tokens

### Secret Expiry Handling

* Secrets should be rotated periodically
* Integration with external secret managers like Vault is recommended
* Pods should restart automatically after secret updates

### Namespaces

* ai-employee namespace
* monitoring namespace

### RBAC

* Follow least privilege principle
* Define Roles and RoleBindings carefully

### Security Measures

* Apply Network Policies to restrict traffic
* Use external secret management systems

### Monitoring

* Prometheus for metrics
* Grafana for visualization
* ELK stack for logging

### Compromise Handling

If a security breach occurs:

* Immediately revoke secrets
* Restart affected pods
* Rotate credentials
* Review logs for suspicious activity

---


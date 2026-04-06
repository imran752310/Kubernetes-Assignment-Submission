
## Scenario 2: AI Employee (OpenClaw)

### Architecture

Secure AI agent deployed in Kubernetes

### Deployments

* AI Employee Deployment
* Database (StatefulSet)

### Services

* Internal services → ClusterIP

### Resource Requests

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

* Non-sensitive configs

### Secrets

* API keys
* Tokens

### Secret Expiry Handling

* Auto rotation
* Vault integration
* Restart pods on expiry

### Namespaces

* ai-employee
* monitoring

### RBAC

* Least privilege
* Role + RoleBinding

### Security

* Network Policies
* External Secret Manager

### Monitoring

* Prometheus
* Grafana
* ELK

### Compromise Handling

* Revoke secrets
* Restart pods
* Audit logs

---

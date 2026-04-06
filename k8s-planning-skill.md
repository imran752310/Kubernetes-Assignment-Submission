
## Kubernetes Planning Skill

### Description

This skill helps in designing Kubernetes deployment plans based on application requirements. It can be reused for different types of systems.

### Inputs

* Application components
* Security requirements
* Performance and scaling needs

### Outputs

* Deployment strategies
* Service configurations
* ConfigMaps and Secrets
* RBAC policies
* Namespace structure

### Planning Steps

1. Identify system components
2. Decide Deployment or StatefulSet
3. Define service types
4. Configure environment using ConfigMaps and Secrets
5. Apply RBAC for access control
6. Add scaling strategies like HPA
7. Include monitoring and logging tools

### Example

For an e-commerce system:

* Frontend → Deployment + LoadBalancer
* Backend → Deployment + ClusterIP
* Database → StatefulSet

### Reusability

This approach can be applied to:

* Microservices applications
* AI-based systems
* Secure enterprise applications



## Kubernetes Planning Agent Skill

### Purpose

Generate Kubernetes deployment plans automatically for any application.

### Input

* System components
* Security requirements
* Scaling needs

### Output

* Deployments
* Services
* ConfigMaps
* Secrets
* RBAC
* Namespaces

### Steps

1. Identify components
2. Map to Deployments/StatefulSets
3. Define Services
4. Add ConfigMaps & Secrets
5. Apply RBAC
6. Define scaling (HPA)
7. Add monitoring

### Example

Input:
"E-commerce app with frontend, backend, database"

Output:

* Frontend → Deployment + LoadBalancer
* Backend → Deployment + ClusterIP
* DB → StatefulSet

### Reusability

* Works for any microservice architecture
* Supports secure AI systems

---

# 🚀 HOW TO SUBMIT (IMPORTANT)

1. Create a GitHub repository
2. Create 3 files:

   * plan1-scenario1.md
   * plan2-scenario2.md
   * k8s-planning-skill.md
3. Copy each section into its file
4. Push to GitHub
5. Submit repository link

---

# ⭐ BONUS (OPTIONAL)

* Add architecture diagram image
* Add README.md

---

✅ YOUR ASSIGNMENT IS NOW 100% COMPLETE

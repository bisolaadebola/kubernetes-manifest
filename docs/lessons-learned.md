

```markdown
# Lessons Learned

## Kubernetes Workloads

This project provided hands-on practice with several Kubernetes workload resources.

### Pods

I learned that a Pod is the smallest deployable unit in Kubernetes and provides the environment in which containers run.

### ReplicaSets

I learned how ReplicaSets maintain the desired number of Pod replicas.

### Deployments

I learned how Deployments manage application Pods through ReplicaSets and maintain the desired application state.

### StatefulSets

I learned how StatefulSets are used for workloads that require stable Pod identities and predictable naming.

---

# Kubernetes Networking

One of the main areas of learning in this project was Kubernetes networking.

I practiced working with:

- ClusterIP Services
- Headless Services
- NodePort Services
- Service selectors
- Pod labels
- Service endpoints

---

## Service Selectors

I learned that a Kubernetes Service uses selectors to identify the Pods that should receive traffic.

For example:

```yaml
selector:
  app: elearning

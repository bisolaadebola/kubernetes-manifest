# Kubernetes Manifest Project — Lessons Learned

## Overview

This project helped me move from learning Kubernetes concepts theoretically to working with actual Kubernetes manifests and cluster resources.

## Key Lessons

### 1. Pods

I learned that Pods are the smallest deployable units in Kubernetes but are generally not used alone for managing application availability.

### 2. ReplicaSets

ReplicaSets maintain the desired number of Pods and help provide basic self-healing for stateless workloads.

### 3. Deployments

I learned that Deployments manage ReplicaSets and provide a better way to manage stateless applications, including scaling and controlled updates.

### 4. StatefulSets

Working with StatefulSets helped me understand the difference between stateless and stateful applications and the importance of stable Pod identity.

### 5. Services

I learned that Pods can be recreated and their IP addresses can change, so Services provide a stable way to access application Pods.

### 6. Labels and Selectors

Labels and selectors are critical for connecting Kubernetes resources.

For example:

```yaml
labels:
  app: elearning
```

must match:

```yaml
selector:
  app: elearning
```

A mismatch can prevent a Service from routing traffic to the correct Pods.

### 7. NodePort Networking

Using NodePort helped me understand how external traffic can reach an application through:

```text
Node IP
   ↓
NodePort
   ↓
Service
   ↓
Pod
```

### 8. Troubleshooting

I learned to troubleshoot Kubernetes systematically by checking:

```bash
kubectl get pods
kubectl get svc
kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl get endpoints <service-name>
```

Rather than changing multiple configurations at once, I learned to identify which layer is causing the problem.

## Key Takeaway

The biggest takeaway from this project was understanding how Kubernetes resources work together rather than viewing each manifest as an isolated configuration.

This project gave me a foundation for moving into more advanced Kubernetes topics such as Ingress, persistent storage, ConfigMaps, Secrets, Helm, monitoring, and CI/CD.

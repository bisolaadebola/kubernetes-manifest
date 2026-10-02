# Lessons Learned

## Kubernetes Manifests

This project helped me understand how Kubernetes resources can be defined using YAML manifests.

Instead of creating resources manually, Kubernetes manifests provide a declarative way to describe the desired state of the application.

## Pods, ReplicaSets, and Deployments

I learned the relationship between Pods, ReplicaSets, and Deployments.

```text
Deployment
    |
    v
ReplicaSet
    |
    v
Pods
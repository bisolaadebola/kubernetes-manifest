# Kubernetes Manifest Project — Deployment Guide

## Overview

The project was deployed using Kubernetes YAML manifests and managed with `kubectl`.

The general workflow was:

```text
Create Manifest
      ↓
Apply Manifest
      ↓
Verify Resource
      ↓
Test Application
      ↓
Troubleshoot
```

## Prerequisites

* Kubernetes cluster
* `kubectl`
* Kubernetes YAML manifests
* Container image

Verify cluster access:

```bash
kubectl cluster-info
kubectl get nodes
```

## Deploying Resources

### Pod

Apply the Pod manifest:

```bash
kubectl apply -f pod.yaml
```

Verify:

```bash
kubectl get pods
```

### ReplicaSet

```bash
kubectl apply -f replicaset.yaml
kubectl get replicasets
kubectl get pods
```

### Deployment

```bash
kubectl apply -f deployment.yaml
kubectl get deployments
kubectl get pods
```

Check the Deployment rollout:

```bash
kubectl rollout status deployment/<deployment-name>
```

### StatefulSet

```bash
kubectl apply -f statefulset.yaml
kubectl get statefulsets
kubectl get pods
```

### Service

Apply the Service:

```bash
kubectl apply -f service.yaml
```

Check the Service:

```bash
kubectl get svc
```

For the NodePort Service, the application can be accessed using:

```text
<Node-IP>:<NodePort>
```

## Troubleshooting

Useful commands during deployment:

```bash
kubectl get pods
kubectl get svc
kubectl describe pod <pod-name>
kubectl describe svc <service-name>
kubectl logs <pod-name>
kubectl get endpoints <service-name>
```

Checking the Service endpoints is especially useful when a NodePort Service exists but traffic is not reaching the application.

## Removing Resources

Resources can be removed using:

```bash
kubectl delete -f <manifest-file>
```

This deployment process provided practical experience using `kubectl` to manage Kubernetes resources and troubleshoot application connectivity.

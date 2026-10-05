# Kubernetes Manifest Project — Architecture

## Overview

This project demonstrates the use of Kubernetes manifests to create and manage different Kubernetes resources.

The main resources practiced were:

* Pods
* ReplicaSets
* Deployments
* StatefulSets
* Services
* NodePort networking

## Architecture

The main application flow is:

```text
Deployment
    |
ReplicaSet
    |
Pods
    |
Service
    |
NodePort
    |
External Access
```

A StatefulSet was also created separately to understand how Kubernetes manages stateful workloads.

## Kubernetes Resources

### Pod

A Pod is the smallest deployable unit in Kubernetes and runs the application container.

### ReplicaSet

A ReplicaSet maintains a specified number of identical Pods and replaces Pods when they are no longer available.

### Deployment

A Deployment manages stateless applications through ReplicaSets and provides features such as scaling and controlled updates.

```text
Deployment
     |
ReplicaSet
     |
+----+----+
|    |    |
Pod  Pod  Pod
```

### StatefulSet

A StatefulSet is designed for stateful applications that require stable Pod identity and, where configured, persistent storage.

Example Pod names:

```text
application-0
application-1
application-2
```

### Service

A Service provides a stable networking endpoint for a group of Pods.

It uses labels and selectors to identify the correct Pods.

```text
Service
   |
   +---- Pod
   +---- Pod
   +---- Pod
```

### NodePort

NodePort exposes the Service through a port on the Kubernetes nodes, allowing external traffic to reach the application.

```text
Client
  |
NodePort
  |
Service
  |
Pods
```

## Key Architecture Concepts

This project helped demonstrate:

* Kubernetes workload management
* Labels and selectors
* Stateless vs. stateful workloads
* Service discovery and networking
* Declarative Kubernetes configuration
* The relationship between Deployments, ReplicaSets, and Pods

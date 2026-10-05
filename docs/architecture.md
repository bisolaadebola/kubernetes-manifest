# Kubernetes Architecture

## Overview

This project demonstrates how Kubernetes resources work together to deploy, manage, replicate, and expose an application.

The Kubernetes environment was deployed on an AWS EC2 Ubuntu instance and managed using `kubectl`. Free Lens was used to monitor and interact with the Kubernetes cluster.

The project focuses on Kubernetes workloads and networking components, including:

- Pods
- ReplicaSets
- Deployments
- StatefulSets
- Kubernetes Services
- ClusterIP
- Headless Services
- NodePort
- Kubernetes networking and service discovery

---

## Environment

The project was built using:

- AWS EC2
- Ubuntu Linux
- Kubernetes
- kubectl
- Free Lens
- YAML manifests
- Git
- GitHub

---

## Kubernetes Workloads

### Pod

A Pod is the smallest deployable unit in Kubernetes.

The project includes an example Pod manifest used to understand how a containerized application runs inside Kubernetes.

Example:

```text
Pod
└── Container
    └── Application
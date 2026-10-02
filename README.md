# Kubernetes Manifest Project

A hands-on Kubernetes project focused on creating, deploying, exposing, and managing Kubernetes resources using YAML manifests.

This project is being built on an AWS EC2 instance and monitored using Free Lens. The project is also version-controlled with Git and GitHub.

## Project Overview

The goal of this project is to develop practical Kubernetes and DevOps skills by creating and managing different Kubernetes resources.

The project covers Kubernetes Pods, ReplicaSets, Deployments, StatefulSets, Services, NodePort, LoadBalancer, and persistent storage.

I am building on the project progressively as I learn more Kubernetes concepts.

## Environment

- AWS EC2
- Ubuntu Linux
- Kubernetes
- kubectl
- Free Lens
- YAML
- Git
- GitHub

## Project Structure

```text
kubernetes-manifest/
│
├── README.md
├── manifests/
│   ├── deployment.yaml
│   ├── elearning-pod.yaml
│   ├── headless.yaml
│   ├── loadbalancer-service.yaml
│   ├── nodeport-service.yaml
│   ├── pv.yaml
│   ├── replicaset.yaml
│   ├── service-elearning.yaml
│   └── statefulset.yaml
│
├── docs/
│
├── screenshots/
│
└── .gitignore
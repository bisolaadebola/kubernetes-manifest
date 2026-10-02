# Deployment Guide

## Prerequisites

The following environment was used for this project:

- AWS EC2 instance
- Ubuntu Linux
- Kubernetes
- kubectl
- Free Lens
- Git
- GitHub

## 1. Connect to the Kubernetes Cluster

The Kubernetes cluster is running on an AWS EC2 instance.

Verify that kubectl can communicate with the cluster:

```bash
kubectl get nodes

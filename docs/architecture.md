# Kubernetes Architecture

## Overview

This project uses Kubernetes to deploy and manage application workloads on an AWS EC2 instance.

The Kubernetes cluster is managed using `kubectl` and monitored through Free Lens.

The project demonstrates several Kubernetes resources and how they work together to run, replicate, expose, and manage applications.

## Environment

- AWS EC2
- Ubuntu Linux
- Kubernetes
- kubectl
- Free Lens
- YAML manifests
- Git and GitHub

## Kubernetes Resources

The project currently includes the following Kubernetes resources:

### Pod

The Pod is the basic execution unit in Kubernetes and is used to run the application container.

Manifest:

```text
manifests/elearning-pod.yaml
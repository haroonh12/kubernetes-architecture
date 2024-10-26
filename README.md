# kubernetes-architecture
This repository provides a structured overview of Kubernetes, focusing on how it addresses certain limitations of Docker and its architectural components. 

## Introduction

Docker is widely used for containerization, but it has limitations, such as:
- **Single Host Dependency**: Docker alone lacks multi-host capabilities.
- **Ephemeral Nature**: Container states and data can be lost unless configured with additional storage solutions.
- **Non-Enterprise Behavior**: Docker needs more features for production-grade, large-scale deployments.

Kubernetes (K8s) was developed to overcome these challenges, offering a robust and scalable platform for managing containerized applications in production.

## Key Concepts

### Kubernetes vs. Docker
Kubernetes extends Docker’s functionality by adding:
- **Multi-Host Clustering**: Kubernetes clusters allow scaling across multiple nodes.
- **Persistent Storage**: Kubernetes enables persistent volume claims (PVCs) and supports cloud-based storage.
- **Enterprise-Level Management**: Features like autoscaling, load balancing, and automated rollouts and rollbacks are integrated.

### Kubernetes Architecture
The core components include:
- **Master Node**:
  - **API Server**: Manages RESTful calls for all Kubernetes operations.
  - **etcd**: A key-value store for storing cluster data and configurations.
  - **Scheduler**: Allocates resources to pods based on their requirements.
  - **Controller Manager**: Oversees controllers to manage the state of resources.

- **Worker Nodes**:
  - **Kubelet**: Ensures containers are running in a pod and communicates with the API server.
  - **Kube Proxy**: Manages networking, forwarding traffic to appropriate containers.
  - **Container Runtime**: Executes containerized applications (e.g., Docker, containerd).
 
  - ## Documentation
To get more info, refer:
https://kubernetes.io/docs/concepts/architecture/

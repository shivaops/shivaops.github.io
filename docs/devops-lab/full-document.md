# ShivaOps DevOps Lab – CI/CD, Docker and Kubernetes Practice Platform
## Fully Automated Local DevOps Practice Environment

## Overview
Welcome to the **ShivaOps DevOps Lab**, a fully automated local DevOps environment provisioned using **Oracle VirtualBox** and **Vagrant**.

This project turns a Windows laptop into a complete hands-on DevOps lab, allowing users to practice real deployment workflows locally without depending on cloud infrastructure.

## Purpose
This lab simulates a realistic deployment environment and is well suited for:

- DevOps learners
- CI/CD practice
- interview preparation
- home lab experimentation
- college or classroom lab demonstrations

## Key Advantages
- No cloud account required
- No billing risk
- No repetitive manual VM setup
- Fully automated provisioning from a single command
- Safe environment for repeated testing and learning

## Why This Lab
Everything is prepared through a single startup command:

```bash
vagrant up
```

Once started, the environment provisions the infrastructure and prepares the platform for containerization, orchestration, automation, storage, CI/CD, and Git-based workflows.

## Preconfigured Components
- Kubernetes cluster with 1 master node and 2 worker nodes
- MetalLB
- Ingress Controller
- NFS-based storage support
- Git VM linked to GitHub
- SSH access across the lab
- Docker build environment
- Jenkins environment
- Ansible node
- Windows host integration

## Lab Infrastructure

| VM Name | Role |
|---|---|
| `kmaster` | Kubernetes master node |
| `kworker1` | Kubernetes worker node |
| `kworker2` | Kubernetes worker node |
| `nfs-server` | Shared storage and dynamic provisioning support |
| `docker` | Docker image build environment |
| `git` | Git and GitHub integration node |
| `jenkins` | CI/CD orchestration server |
| `ansible` | Automation and configuration management node |

## Infrastructure Summary
This lab provides an end-to-end local stack including:

- Kubernetes
- Docker
- Jenkins
- Ansible
- NFS Server
- Git and GitHub integration
- Windows host connectivity

## Application Deployment Highlights
A sample application deployment in this lab includes:

- Node.js application with MySQL database
- StatefulSet-based deployment
- Ingress-based browser access
- PersistentVolumeClaims provisioned through NFS
- Secrets and ConfigMaps for application configuration
- MetalLB for LAN-accessible service exposure

## Key Technologies
- Vagrant
- Oracle VirtualBox
- Kubernetes
- Docker
- Jenkins
- Ansible
- NFS
- Git / GitHub
- MySQL
- Node.js
- MetalLB
- Ingress Controller

## Why It Is Useful
This lab provides a practical environment for learning and demonstrating:

- infrastructure automation
- multi-VM provisioning
- Kubernetes deployment
- CI/CD workflow setup
- persistent storage handling
- internal networking
- application exposure through Ingress and MetalLB

## Conclusion
ShivaOps DevOps Lab is a practical and repeatable local platform for DevOps learning, testing, and demonstration. It brings together automation, orchestration, storage, networking, and CI/CD in a way that feels close to a real working environment while remaining safe and affordable for local use.

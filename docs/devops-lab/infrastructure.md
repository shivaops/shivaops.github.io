# Lab Infrastructure

The lab is built as a multi-VM local environment where each virtual machine has a clear and separate responsibility.

## VM Layout

| VM Name | Main Role | Notes |
|---|---|---|
| `kmaster` | Kubernetes control plane | Manages cluster control functions |
| `kworker1` | Kubernetes worker | Runs workloads and services |
| `kworker2` | Kubernetes worker | Runs workloads and services |
| `nfs-server` | Shared storage node | Supports persistent storage and dynamic provisioning |
| `docker` | Image build node | Builds and prepares container images |
| `git` | Source control node | Supports Git and GitHub push workflows |
| `jenkins` | CI/CD node | Automates build and deployment flow |
| `ansible` | Automation node | Used for automation and repeatable configuration tasks |

## Infrastructure Design Idea
The lab is intentionally split across separate VMs to mimic the feel of a small but realistic environment rather than a single all-in-one sandbox.

This makes it easier to practice:

- node-to-node communication
- service exposure
- storage integration
- CI/CD orchestration
- role-based separation of tools

## Practical Outcome
After provisioning, the user can build images, push code, deploy workloads, expose applications, and test end-to-end Kubernetes scenarios in one connected local lab.

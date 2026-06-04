# k8s-gitops

A Kubernetes GitOps project demonstrating declarative infrastructure management and continuous delivery using GitOps principles.

## Overview

This repository provides a practical example of implementing GitOps workflows for Kubernetes environments. It is designed for DevOps engineers, students, and cloud-native enthusiasts who want to learn how to manage Kubernetes deployments through Git-based workflows.

## Features

* GitOps-based Kubernetes deployment management
* Infrastructure as Code (IaC) approach
* Declarative Kubernetes manifests
* Environment-specific configurations
* Automated deployment workflows
* Version-controlled infrastructure changes
* Easy rollback and change tracking

## Architecture

```text
Developer
    │
    ▼
 Git Repository
    │
    ▼
 GitOps Controller (Argo CD / Flux)
    │
    ▼
 Kubernetes Cluster
    │
    ├── Application Deployments
    ├── Services
    ├── ConfigMaps
    └── Ingress Resources
```

## Repository Structure

```text
k8s-gitops/
├── apps/
│   ├── frontend/
│   └── backend/
├── environments/
│   ├── dev/
│   ├── staging/
│   └── prod/
├── infrastructure/
├── manifests/
├── scripts/
└── docs/
```

## Prerequisites

Before getting started, ensure you have:

* Kubernetes Cluster
* kubectl
* Git
* Argo CD or Flux (optional)
* Docker (optional)

## Installation

### Clone the Repository

```bash
git clone https://github.com/Lahiru-Avishka/k8s-gitops.git
cd k8s-gitops
```

### Apply Kubernetes Resources

```bash
kubectl apply -f manifests/
```

### Verify Deployment

```bash
kubectl get pods -A
kubectl get svc -A
```

## GitOps Workflow

1. Make changes to Kubernetes manifests.
2. Commit changes to Git.
3. Push changes to the repository.
4. GitOps controller detects changes.
5. Kubernetes cluster is automatically synchronized.
6. Application updates are deployed.

## Example Deployment

```bash
kubectl apply -f apps/frontend/
kubectl apply -f apps/backend/
```

## Benefits of GitOps

| Traditional Deployment | GitOps Deployment         |
| ---------------------- | ------------------------- |
| Manual changes         | Automated synchronization |
| Harder auditing        | Full Git history          |
| Limited rollback       | Easy rollback             |
| Configuration drift    | Desired state enforcement |

## Learning Objectives

This project helps users learn:

* Kubernetes fundamentals
* GitOps principles
* Continuous Delivery (CD)
* Infrastructure as Code
* Cluster configuration management
* Kubernetes application deployment

## Roadmap

* [ ] Add Argo CD integration
* [ ] Add Flux integration
* [ ] Add Helm support
* [ ] Add Kustomize overlays
* [ ] Add GitHub Actions CI/CD
* [ ] Add monitoring with Prometheus
* [ ] Add Grafana dashboards
* [ ] Add security scanning

## Contributing

Contributions are welcome.

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Submit a pull request

## License

This project is licensed under the MIT License.

## Author

Lahiru Avishka

GitHub: https://github.com/Lahiru-Avishka

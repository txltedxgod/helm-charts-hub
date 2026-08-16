# helm-charts-hub

> Production-grade collection of **Helm 3** Kubernetes charts for cloud-native applications and stateful infrastructure.

[![Helm](https://img.shields.io/badge/Helm-v3.14%2B-0F1689?style=flat-square&logo=helm)](https://helm.sh)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-1.28%2B-326CE5?style=flat-square&logo=kubernetes)](https://kubernetes.io)
[![CI](https://img.shields.io/badge/CI-Lint_&_Test-2088FF?style=flat-square&logo=githubactions)](.github/workflows/lint-test.yaml)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)

`#helm` `#kubernetes` `#k8s-charts` `#cloud-native` `#devops` `#infrastructure` `#gitops`

---

## Included Charts

| Chart | Version | Description |
|-------|---------|-------------|
| **`generic-microservice`** | `1.2.0` | Flexible standard chart for stateless web services, HPAs, ingress, and probe monitoring. |
| **`redis-ha`** | `2.1.0` | High-availability Redis StatefulSet cluster with automatic Sentinel failover and PVCs. |

## Quick Usage

```bash
# Lint chart locally
helm lint charts/generic-microservice

# Dry run install
helm install my-app charts/generic-microservice \
  --set image.repository=ghcr.io/myorg/api \
  --set image.tag=v1.0.0 \
  --dry-run

# Deploy Redis HA Cluster
helm upgrade --install redis-cluster charts/redis-ha \
  --namespace storage --create-namespace
```

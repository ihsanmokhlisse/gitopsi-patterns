# Prometheus Pattern

Prometheus monitoring stack for Kubernetes metrics collection and alerting.

## Overview

This pattern deploys a production-ready Prometheus instance with:
- Kubernetes service discovery
- Pod/service/node metrics scraping
- Secure deployment with non-root user
- Resource limits and health checks

## Installation

```bash
gitopsi marketplace install prometheus
```

## Configuration

| Parameter | Default | Description |
|-----------|---------|-------------|
| `namespace` | `monitoring` | Target namespace |
| `retention` | `15d` | Data retention period |
| `storageSize` | `10Gi` | PVC storage size |
| `replicas` | `1` | Number of replicas |

## Platform Support

- **Kubernetes**: 1.21+
- **OpenShift**: 4.10+ (includes SCC)

## Access

After installation:

```bash
kubectl port-forward -n monitoring svc/prometheus 9090:9090
```

Then open http://localhost:9090

## Components

- Prometheus Server (v2.47.0)
- ServiceAccount with RBAC
- ConfigMap with scrape configs
- Service (ClusterIP)

## Security

- Runs as non-root (UID 65534)
- Read-only root filesystem
- Dropped all capabilities
- OpenShift SCC included


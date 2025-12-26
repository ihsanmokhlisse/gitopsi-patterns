# gitopsi-patterns

Official GitOps patterns for gitopsi - community templates and infrastructure patterns.

## Usage

```bash
# List available patterns
gitopsi marketplace list

# Search for patterns
gitopsi marketplace search prometheus

# Install a pattern
gitopsi marketplace install prometheus

# Get pattern info
gitopsi marketplace info prometheus
```

## Available Patterns

### Observability
| Pattern | Description | Status |
|---------|-------------|--------|
| [prometheus](./observability/prometheus) | Prometheus monitoring stack | ✅ Available |

### Security
| Pattern | Description | Status |
|---------|-------------|--------|
| cert-manager | TLS certificate management | 🔜 Coming soon |
| sealed-secrets | Encrypted Kubernetes secrets | 🔜 Coming soon |

### Networking
| Pattern | Description | Status |
|---------|-------------|--------|
| ingress-nginx | NGINX Ingress Controller | 🔜 Coming soon |

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

## License

Apache 2.0


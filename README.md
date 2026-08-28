# Kubernetes Helm Charts

Reusable Helm charts for homelab deployments.

## Charts

### common-app
Generic application deployment with:
- Deployment
- Service
- Ingress (optional)
- Resource limits
- Environment variables

### monitoring-stack
Complete monitoring with:
- Prometheus
- Grafana
- (Loki optional)

## Usage

```bash
helm install myapp ./charts/common-app   --set image.repository=myapp   --set ingress.enabled=true   --set ingress.host=myapp.local
```

## Requirements

- Helm 3.x
- Kubernetes 1.25+

## License

MIT

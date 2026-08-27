# Kubernetes Helm Charts for Homelab

Custom Helm charts for deploying homelab infrastructure on Kubernetes.

## Charts

| Chart | Description | Status |
|-------|-------------|--------|
| vaultwarden | Bitwarden-compatible password manager | Ready |
| traefik | Ingress controller with custom config | Ready |
| prometheus-adapter | Custom metrics adapter for HPA | Ready |

## Usage

Add the repository:

```bash
helm repo add magos-cyber https://raw.githubusercontent.com/magos-cyber/kubernetes-helm-charts/main/helm-charts
helm repo update
```

Install a chart:

```bash
helm install vaultwarden magos-cyber/vaultwarden -f values.yaml
```

## Development

```bash
# Lint
helm lint helm-charts/vaultwarden

# Template render
helm template vaultwarden helm-charts/vaultwarden

# Package
helm package helm-charts/vaultwarden
```

## Repository Structure

```
kubernetes-helm-charts/
+-- helm-charts/
|   +-- vaultwarden/
|   |   +-- Chart.yaml
|   |   +-- values.yaml
|   |   `-- templates/
|   |       +-- _helpers.tpl
|   |       +-- deployment.yaml
|   |       +-- ingress.yaml
|   |       +-- pvc.yaml
|   |       +-- service.yaml
|   |       `-- serviceaccount.yaml
|   +-- traefik/
|   |   +-- Chart.yaml
|   |   +-- values.yaml
|   |   `-- templates/
|   `-- prometheus-adapter/
|       +-- Chart.yaml
|       +-- values.yaml
|       `-- templates/
`-- README.md
```

## License

MIT

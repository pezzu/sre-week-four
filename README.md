# Release management with Helm

1. Start kubernetes cluster

```sh
minikube start
```

2. Create namespace

```sh
kubectl create namespace sre
```

3. Deploy the helm chart

```sh
helm install upcommerce ./upcommerce -n sre
```

## Useful helm commands

- List all releases (deployments)

```sh
helm list -n sre    
```

- View the revision history of a release

```sh
helm history upcommerce -n sre
```

- Rollback the release

```sh
helm rollback upcommerce <release_number> -n sre
```

- Get detailed information about a specific release

```sh
helm status upcommerce -n sre   
```

- Uninstall a release

```sh
helm uninstall upcommerce -n sre
```

- Display default values from the chart

```sh
helm show values ./upcommerce -n sre
```

- Show the chart’s README

```sh
helm show readme ./upcommerce -n sre
```

- Check your chart for issues

```sh
helm lint ./upcommerce -n sre
```

- Render templates without installing

```sh
helm template upcommerce ./upcommerce -n sre
```

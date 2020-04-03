# Maxwell
Helm charts for [maxwell](https://github.com/zendesk/maxwell).

## Requrirements
- Kubernetes; minikube for local development
- Helm

## Installation
- Add your configuration in `values.yaml > configMap.data`. Default configuration is using `ENV` variables and using `mw_` prefix. Change this flag in `templates/deployment.yaml > containers.args`.
- See `templates/deployment.yaml` if you running minikube and want to access resources in Host.
- Execute
```bash
$ helm install maxwell ./maxwell --namespace=your-namespace
```

## Remove installation
```bash
$ helm uninstall maxwell --namespace=your-namespace
```
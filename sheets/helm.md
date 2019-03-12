# Helm Cheat Sheet

## General

| Command | Description |
| ------- | ----------- |
| `helm create <name>` | Creates a new chart with the specified name. |
| `helm ls` | List all installed charts. |
| `helm install <name>` | Installs the chart with the specified name on the linked Kubernetes server. |
| `helm delete --purge <chart name>` | Completely remove the specified chart and all it dependencies. |
| `helm delete --purge $(helm ls -aq)` | Completely remove all installed charts and their dependencies. This is a create way to start with a fresh environment. |

To get more information for each command you can add the --help flag after the specific command (e.g. to get more information about the install command you can execute: `helm install --help`).

## Links

- Official documentation: https://helm.sh/docs
- Helm website: https://helm.sh/
- Chart repository: https://hub.helm.sh/`

## Useful articles
- [Package Kubernetes Applications with Helm](https://akomljen.com/package-kubernetes-applications-with-helm/)
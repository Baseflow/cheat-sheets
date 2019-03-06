# Kubernetes Cheat Sheet

## General

| Command | Description |
| ------- | ----------- |
| `kubectl config current-context` | Check to which Kubernetes cluster we are connected. |
| `kubectl get nodes` | List all nodes on the Kubernetes cluster. |

## Resources

| Command | Description |
| ------- | ----------- |
| `kubectl create -f <file_location>` | Creates a new object based on the given file (which should be a Kubernetes manifest file, either YAML or JSON). |
| `kubectl apply -f <file_location>` | Updates the desired state of the object on the Kubernetes cluster. |
| `kubectl get [nodes|pods|rc|deploy|svc]` | List all pods and their state. |
| `kubectl describe [nodes|pods|rc|deploy|svc]` | A detailed list of the installed pods. |
| `kubectl delete [nodes|pods|rc|deploy|svc] <pod_name>` | Deletes all pods from the cluster matching the supplied name. |
| `kubectl expose rc <rc_name> —name=<service_name> --target-port=8080 --type=NodePort` | Creates a new services with the supplied name that targets pods on port 8080 and listens on a dynamically created port. |

## Rollout

| Command | Description |
| ------- | ----------- |
| `kubectl rollout status deployment <deployment_name>` | Get the status of the deployment matching the supplied name. |
| `kubectl rollout history deployment <deployment_name>` | List all revisions of the deployment matching the supplied name. |
| `kubectl rollout undo deployment <deployment_name> —to-revision=<revision_number>` | Rollback to a specific revision. |

## Useful links

- Official documentation: https://kubernetes.io/docs
- Code repository: https://github.com/kubernetes/kubernetes
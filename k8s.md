# k8s commands

show documentation: 
kubectl explain <ressource>
(pod, hba, ...)

deploy kustomize:
kubectl kustomize . | kubectl apply -f - -n <namespace> 

describe:
kubectl describe pod <pod> -n <namespace>

get pods:
kubectl get pods -n <namespace> 

get logs:
kubectl logs <pod> -n <namespace>

go into pod:
kubectl exec -it <pod> -n <namespace> -- /bin/bash

get deployments:
kubectl get deployments -n <namespace>

delete deployment:
kubectl delete deployment <deploymentname> -n <namespace>

delete pod:
kubectl delete pod <podname> -n <namespace>

get namespaces:
kubectl get ns


# k8s commands table

| Command                                      | Description |
|----------------------------------------------|-------------|
| kubectl explain <ressource>                  | Explains the attributes of a Kubernetes resource (e.g., pod, hba). |
| kubectl kustomize . \| kubectl apply -f - -n <namespace> | Applies Kubernetes resources defined by Kustomize in the current directory to a specific namespace. |
| kubectl describe pod <pod> -n <namespace>    | Provides a detailed description of a pod in a specific namespace. |
| kubectl get pods -n <namespace>              | Lists pods in a specific namespace. |
| kubectl logs <pod> -n <namespace>             | Retrieves logs from a specific pod in a specific namespace. |
| kubectl exec -it <pod> -n <namespace> -- /bin/bash | Executes an interactive shell (/bin/bash) inside a specific pod in a specific namespace. |
| kubectl get deployments -n <namespace>       | Lists deployments in a specific namespace. |
| kubectl delete deployment <deploymentname> -n <namespace> | Deletes a specific deployment in a specific namespace. |
| kubectl delete pod <podname> -n <namespace>   | Deletes a specific pod in a specific namespace. |
| kubectl get ns                               | Lists all namespaces in the Kubernetes cluster. |
| kubectl get nodes                           | Lists all nodes in the Kubernetes cluster. |
| kubectl get services -n <namespace>         | Lists services in a specific namespace. |
| kubectl get configmaps -n <namespace>       | Lists configmaps in a specific namespace. |
| kubectl get secrets -n <namespace>          | Lists secrets in a specific namespace. |
| kubectl get pods --all-namespaces            | Lists all pods in all namespaces. |
| kubectl scale deployment <deploymentname> --replicas=<num> -n <namespace> | Scales the number of replicas for a deployment in a specific namespace. |
| kubectl apply -f <file.yaml> -n <namespace>  | Applies Kubernetes resources defined in a YAML file to a specific namespace. |
| kubectl edit deployment <deploymentname> -n <namespace> | Opens the deployment configuration in an editor for editing. |
| kubectl get ingresses -n <namespace>        | Lists ingresses in a specific namespace. |
| kubectl describe ingress <ingressname> -n <namespace> | Provides detailed information about an ingress in a specific namespace. |
| kubectl rollout status deployment <deploymentname> -n <namespace> | Checks the status of a deployment rollout. |



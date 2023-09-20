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

# Basic Commands

## Start local kubernetes cluster
```
minikube start
```

## Stop local kubernetes cluster
```
minikube stop
```

## Delete local kubernetes cluster
```
minikube delete
```

## List cluster services
```
kubectl get services -A
```

## List all pods
```
kubectl get pods -A
```

## List all pods in a given namespace
```
kubectl get pods -n $NAMESPACE_NAME
```

## List all pods in a given namespace with additional info
```
kubectl get pods -n $NAMESPACE_NAME -o wide
```

## List cluster namespaces
```
kubectl get namespaces
```

## List cluster nodes
```
kubectl get nodes
```

## Apply configuration from YAML file
```
kubectl apply -f 03_02_Begin/namespace.yaml
```

## Delete configuration from YAML file
```
kubectl delete -f 03_02_Begin/namespace.yaml
```

## List all deployments in the "development" namespace
```
kubectl deployments -n development
```

## Delete a pod in a namespace
```
kubectl delete pod $POD_NAME -n $NAMESPACE_NAME
```

## Get information about a pod in a namespace
```
kubectl describe pod $POD_NAME -n $NAMESPACE_NAME
```

## Bash into a pod
```
kubectl exec -it $POD_NAME -- /bin/sh
```

## Print pod logs
```
kubectl logs $POD_NAME -n $NS_NAME
```

## Cleanup resources created with YAML configuration file
```
kubectl delete -f $YAML_CONFIG_FILE
```

## Test security of the cluster with snyck
```
snyk iac test deployment.yaml
```